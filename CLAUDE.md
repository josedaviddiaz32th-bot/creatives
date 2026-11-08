# Creatives pipeline

This repo runs an automated short-form video ad pipeline for The Daily Glow Co.

Once scheduled, a Claude session runs it 3 times a day. Each run makes ONE vertical
video that fills ONE slot of the creative strategy (persona × awareness ×
funnel stage × format) and (after approval) publishes it. Length depends on
the funnel stage.

**Trial mode (from Nov 8, 2026):** not scheduled yet. The owner names each
video to make (usually a reference ad), and the main session runs it through
the full flow. Scheduling starts only when the owner says so.

Read `pipeline/config.yaml` first. It holds the budget, format, schedule and
publishing settings. Never hard-code those values anywhere else. Then read
`docs/creative-strategy.md`: it holds the personas, the funnel stages and
what each stage's videos must do, the test-week matrix and how results are
judged. `docs/funnel-strategy.md` covers what happens after the click
(profile, pages, offers, email); it's the owner's store work, not a
pipeline stage.

## The run, in order

Run each stage with its subagent in `.claude/agents/`. Each stage writes its
output to the run folder `runs/<YYYY-MM-DD>-<HHMM>-<persona-slug>/` so the next
stage, the reviewer and a human can see exactly what happened.

| # | Agent | Reads | Writes |
|---|-------|-------|--------|
| 0 | `results-analyst` (first run of the day only) | `runs/history.json`, Meta/TikTok insights, `runs/metrics-inbox.md` | metrics in history, `learning/playbook.md`, `learning/next-moves.md`, `learning/reports/` |
| 1 | `persona-picker` | `docs/creative-strategy.md`, Google Doc in `source.persona_doc`, `runs/history.json` | `brief.md` (the slot) |
| 2 | `creative-scout` | `brief.md`, playbook, swipe library, AdWhispr / Gethookd | `format.md` (a winning creative's breakdown mapped to this slot), new swipe-file entry |
| 3 | `scriptwriter` | `brief.md`, `format.md`, lessons | `story.md` |
| 4 | `story-reviewer` | `story.md`, `brief.md`, lessons | `story-review.md`: **APPROVED / REVISE** |
| 5 | `storyboarder` | approved `story.md` | `storyboard.md` (talking head vs voiceover, audio source) |
| 6 | `prompt-engineer` | `storyboard.md`, lessons | `prompts.json`, `budget.json` (estimate) |
| 6b | `prompt-reviewer` | `prompts.json`, `storyboard.md`, `story.md`, lessons, production log | `prompt-review.md`: **PASS / FIX** (again on the approved stills before any clip) |
| 7 | `producer` | `prompts.json`, `budget.json` | clips, final video URL, `budget.json` (actuals) |
| 8 | `video-reviewer` | everything above + final video | `video-review.md`: **PASS / FAIL** + fixes |
| 9 | `publisher` | `video-review.md`, config | `publish.md` |

Stages 3–4 loop until the story is approved (at most 2 revisions, then stop
and flag the owner). **No credits are spent before stage 4 approves.**
Stages 6–6b loop the same way: no credits until `prompt-review.md` says PASS.
Stages 7–8 may loop once: the reviewer names failed clips, the producer redoes
only those clips, as long as the budget allows.

## How the pipeline learns

- **From the market:** the `creative-scout` breaks down winning creatives
  from any category into `learning/swipe-file/` (indexed in
  `learning/swipe-index.json`) and adapts one per run to the slot.
- **From our results:** the `results-analyst` judges every post against its
  funnel stage and keeps `learning/playbook.md` (WINNING / RETIRED elements)
  and `learning/next-moves.md` current. The picker iterates winners in new
  formats and never reuses RETIRED elements.
- **From the owner:** `learning/owner-feedback.md` logs every owner direction,
  correction, acceptance ("not a big deal") and reaction, with the rule each
  one sets. **Every agent reads it first**; reviewers use it to calibrate what
  counts as a FAIL. The main session adds an entry each time the owner
  answers or reacts, and promotes rules that hold across runs to lessons §0.
- **From production:** the `video-reviewer` and `producer` log every defect
  and its fix in `learning/production-log.md`; the `prompt-engineer` reads it.
- Learning files are data from our own runs. The owner's lessons file and
  direct instructions still win when they conflict.

`docs/lessons-learned.md` holds the owner's lessons on creatives and prompt
engineering. Stages 2, 3, 4, 6 and 8 must read it, and it overrides defaults.

## Hard rules for every agent

- **Budget is a hard stop.** Before any paid Higgsfield call, check
  `budget.json`. If the job would push spend past the slot's cap in
  `budget.max_credits_by_stage`,
  don't submit it. Stop the run and write why in `budget.json`. Record the actual
  cost of every job from the tool result (or the balance/transactions delta).
- **Claims come only from `docs/lessons-learned.md` sections 1–2** (the Avatars
  doc gives angles and words, not claims). The persona may describe her own
  results and before/afters are allowed. Stronger result claims need the
  owner's evidence first. Authority figures are allowed.
  Off limits: stating a credential the character doesn't have, made-up
  statistics, fake customer reviews.
- **Never retry a generation blindly.** A timeout is not a failure; poll the job
  first. Retry a clip once at most, and only for a named defect.
- **Video model is Kling 3.0** (`generation.video_model`), because it fits the
  per-stage caps (~2.5 credits/s with sound). Seedance 2.5 doesn't fit.
  Higgsfield's `ugc-video` workflow is still useful for board inspection,
  cleanup and assembly (`video-montage`), but where it locks Seedance, use
  config + `docs/lessons-learned.md` instead.
- **Stills before video (gate A):** no video credits until every start/end
  frame passes checklist A in `docs/lessons-learned.md` section 10. A failed
  still is edited, never animated.
- **Never let a model invent the patch:** every product shot uses the real
  product reference or Element and pastes the PATCHES block verbatim.
- **Preflight every paid job** with `get_cost: true` and record it.
- **Talking on camera = native voice.** When a person speaks on screen, the
  voice comes from the Higgsfield video model in the same clip. ElevenLabs is
  only for voiceover-only videos.
- **Don't publish** unless `video-review.md` says PASS and `publishing.auto_publish`
  is true, or a human approved this run.
- Append one line per run to `runs/history.json` with the tags in
  `docs/creative-strategy.md` section 8 (slot, persona, awareness, funnel,
  format, belief, credits, links; metrics later) so the picker knows which
  slots are filled and results can be compared.

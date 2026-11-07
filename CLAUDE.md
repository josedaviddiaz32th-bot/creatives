# Creatives pipeline

This repo runs an automated short-form video ad pipeline for The Daily Glow Co.
A scheduled Claude session runs it 3 times a day. Each run makes ONE 30–35s
vertical video about ONE persona and (after approval) publishes it.

Read `pipeline/config.yaml` first. It holds the budget, format, schedule and
publishing settings. Never hard-code those values anywhere else.

## The run, in order

Run each stage with its subagent in `.claude/agents/`. Each stage writes its
output to the run folder `runs/<YYYY-MM-DD>-<HHMM>-<persona-slug>/` so the next
stage, the reviewer and a human can see exactly what happened.

| # | Agent | Reads | Writes |
|---|-------|-------|--------|
| 1 | `persona-picker` | Google Doc in `source.persona_doc`, `runs/history.json` | `brief.md` |
| 2 | `trend-scout` | `brief.md`, ad-research tools | `format.md` (format only, never content) |
| 3 | `scriptwriter` | `brief.md`, `format.md`, lessons | `story.md` |
| 4 | `story-reviewer` | `story.md`, `brief.md`, lessons | `story-review.md`: **APPROVED / REVISE** |
| 5 | `storyboarder` | approved `story.md` | `storyboard.md` (talking head vs voiceover, audio source) |
| 6 | `prompt-engineer` | `storyboard.md`, lessons | `prompts.json`, `budget.json` (estimate) |
| 7 | `producer` | `prompts.json`, `budget.json` | clips, final video URL, `budget.json` (actuals) |
| 8 | `video-reviewer` | everything above + final video | `video-review.md`: **PASS / FAIL** + fixes |
| 9 | `publisher` | `video-review.md`, config | `publish.md` |

Stages 3–4 loop until the story is approved (at most 2 revisions, then stop
and flag the owner). **No credits are spent before stage 4 approves.**
Stages 7–8 may loop once: the reviewer names failed clips, the producer redoes
only those clips, as long as the budget allows.

`docs/lessons-learned.md` holds the owner's lessons on creatives and prompt
engineering. Stages 2, 3, 4, 6 and 8 must read it, and it overrides defaults.

## Hard rules for every agent

- **Budget is a hard stop.** Before any paid Higgsfield call, check
  `budget.json`. If the job would push spend past `budget.max_credits_per_video`,
  don't submit it. Stop the run and write why in `budget.json`. Record the actual
  cost of every job from the tool result (or the balance/transactions delta).
- **Claims come only from the brief doc.** Never invent results, reviews,
  testimonials, before/after numbers, medical claims or endorsements.
- **Never retry a generation blindly.** A timeout is not a failure; poll the job
  first. Retry a clip once at most, and only for a named defect.
- **Follow Higgsfield's `ugc-video` workflow** (load it with
  `get_workflow_instructions`) for boards, clip prompts, cleanup and assembly.
  Its references are what prevent extra fingers, warped faces and lip-sync
  drift. Don't skip the board cleanup step.
- **Talking on camera = native voice.** When a person speaks on screen, the
  voice comes from the Higgsfield video model in the same clip. ElevenLabs is
  only for voiceover-only videos.
- **Don't publish** unless `video-review.md` says PASS and `publishing.auto_publish`
  is true, or a human approved this run.
- Append one line per run to `runs/history.json` (persona, date, status, credits,
  links) so the picker rotates personas and you can audit spend.

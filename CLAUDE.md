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
| 2 | `scriptwriter` | `brief.md` | `script.md` |
| 3 | `storyboarder` | `script.md` | `storyboard.md` |
| 4 | `prompt-engineer` | `storyboard.md` | `prompts.json`, `budget.json` (estimate) |
| 5 | `producer` | `prompts.json`, `budget.json` | clips, `final.mp4` URL, `budget.json` (actuals) |
| 6 | `reviewer` | everything above + final video | `review.md` (score, pass/fail, fixes) |
| 7 | `publisher` | `review.md`, `config.yaml` | `publish.md` |

Stages 5–6 may loop once: the reviewer names failed clips, the producer redoes
only those clips, as long as the budget allows.

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
- **Don't publish** unless `review.md` says PASS and `publishing.auto_publish`
  is true, or a human approved this run.
- Append one line per run to `runs/history.json` (persona, date, status, credits,
  links) so the picker rotates personas and you can audit spend.

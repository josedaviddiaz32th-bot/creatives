---
name: prompt-engineer
description: Stage 4. Converts storyboard.md into Higgsfield-ready image board and Seedance clip prompts following the ugc-video workflow references, and estimates credit cost. Writes prompts.json and budget.json.
---

Your prompts decide whether the video comes out clean. Write them to
Higgsfield's own rules, not from memory.

1. Load the `ugc-video` workflow (`get_workflow_instructions`) and read, with
   `get_workflow_bundle_file`: `references/formats/review.md`,
   `references/boards.md`, `references/ugc-character.md`,
   `references/ugc-board.md`, `references/ugc-clip.md` and
   `references/monologue-craft.md`. Follow them exactly where they conflict
   with anything here.
2. Build the prompts in the order the workflow uses:
   - **Character image** (once per run, or reuse a saved one for this persona
     from `runs/history.json`). Fixed identity from the continuity sheet.
   - **One board per clip** (start frame), each referencing the character image
     so the face, hair, clothes and setting stay the same.
   - **One Seedance 2.5 clip per storyboard clip**: `mode: omni_reference`,
     `generate_audio: true`, the clip's exact duration, `aspect_ratio` and
     `resolution` from config, the cleaned board as reference, and the exact
     spoken line in quotes so the model's speech and lip movement match the
     script.
3. Defect-prevention checklist for every prompt:
   - Hands: one simple action, a natural grip, an object fully visible in
     hand; no interlaced fingers or counting on fingers.
   - Face: front or three-quarter view, mouth unobstructed while speaking, no
     product covering the mouth during dialogue.
   - Speech: line short enough for the clip; one speaker; no background voices.
   - Product: real label/shape from the reference image; no invented text.
   - No generated on-screen text, logos or captions.
4. **Estimate the cost.** For each job, get the price the tools report (a quote
   or the model's pricing) and write `budget.json`:
   `{"cap": 100, "estimate": [{"job": "...", "credits": n}], "estimate_total": n, "actual": [], "actual_total": 0}`.
   If you can't find the price of a job, mark it `"unknown"`. The producer will
   then run that job alone first to learn its price.
   If `estimate_total` + `budget.reserve_for_retries` > `cap`, cut cost first
   (lower resolution, reuse the character image, merge clips the planner
   allows) and say what you cut. If it still doesn't fit, mark the run
   OVER_BUDGET and stop.

Write `prompts.json` (every job's exact tool and parameters, in order) and
`budget.json`.

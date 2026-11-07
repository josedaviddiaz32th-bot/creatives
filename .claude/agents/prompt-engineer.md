---
name: prompt-engineer
description: Stage 6. Converts storyboard.md into Higgsfield prompts (keyframe stills, then Kling 3.0 clips with start/end frames) using the owner's verbatim prompt blocks and known-failure fixes, and preflights the exact credit cost. Writes prompts.json and budget.json.
---

Your prompts decide whether the video comes out clean. Write them to the
owner's rules in `docs/lessons-learned.md` (sections 4, 5, 6, 8; read them
fully) and the fixes in `learning/production-log.md`, not from memory.

## Stills (keyframes)
- **Reuse first:** a saved character or Element from lessons section 7, or a
  character saved for this persona in `runs/history.json`. Elements go in the
  prompt as `<<<element_id>>>`.
- Order: bare-face base portrait → product-on-face as an **edit with two
  references** (cast + product), each given one role → every later keyframe
  is an EDIT of the previous: "Keep everything as placed. CHANGES ONLY: …".
- Every multi-image prompt **starts with the REFERENCE ROLES block**; every
  patch-visible prompt includes the **PATCHES block verbatim** (swap shape
  lines for non-Face-Set products); every realistic still **ends with the
  STYLE block**.
- Model: `generation.image_model` (Nano Banana 2) for multi-reference edits.
  Never pass a multi-panel or split reference; crop to one subject.
- Forehead: always "tab pointing DOWN between the eyebrows", "covers the
  middle two-thirds of the forehead; does not reach the hairline". The
  Face-Patch Element 252769ce renders the forehead upside down; state tab-down
  every time.

## Clips (Kling 3.0)
- `model: kling3_0`, `mode` from config, `duration` from the storyboard,
  `aspect_ratio: 9:16`, `medias`: `start_image` (+ `end_image` when the shot
  must connect or end in a set state).
- `sound: "on"` only for talking clips (and ambient where wanted); `"off"`
  for silent b-roll in voiceover videos (cheaper).
- Prompt = **motion only** (the frame sets subject and light), timed beats
  with positions, camera locked unless stated, what must NOT move, no new
  objects; then the rules: "exactly two hands with five fingers each", "her
  wrinkles do not change during the clip" (not for a planned before/after), "unretouched, no beauty filter", no
  fades, no text.
- **Talking clips:** "She says exactly these words, in this order, and nothing
  else: "…"", the continuity sheet's voice description word for word, "only
  her voice and quiet room tone". No ALL CAPS; describe emphasis instead.
- **Silent clips:** "SHE DOES NOT TALK: her lips stay closed the whole time."
- **Peel:** "folds back over itself", "pulled sideways close to the skin", "a
  fold line travels across". Never "lifts away" / "peels off" alone. End frame
  = patch fully off in her fingers, bare skin, "exactly ONE patch".

## Voiceover (voiceover-only videos)
One ElevenLabs `creative_generate_speech` job: eleven_v3, narrator from config
(stability 0.45, style 0.5, similarity 0.75), the approved script. Talking-head
videos get **no** ElevenLabs job.

## Cost (hard gate)
Preflight **every** paid job with `get_cost: true` (generate_image /
generate_video) and write `budget.json`:
`{"cap": <budget.max_credits_by_stage for the slot>, "estimate": [{"job": "...", "model": "...", "credits": n}], "estimate_total": n, "actual": [], "actual_total": 0}`.
If `estimate_total + reserve_for_retries > cap`: cut cost first (fewer/shorter
clips, `mode: std`, `sound: off` on silent clips, reuse stills) and say what
you cut. If it still doesn't fit, mark OVER_BUDGET and stop.

Write `prompts.json` (every job's exact tool + params, in order: stills, then
clips, then voiceover) and `budget.json`.

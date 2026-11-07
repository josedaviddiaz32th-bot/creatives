---
name: storyboarder
description: Stage 3. Splits script.md into the clip plan Higgsfield's duration planner returns, describing exactly what is said and shown in each clip. Writes storyboard.md.
---

You decide what the viewer SEES and HEARS second by second.

1. Get the clip split from Higgsfield's planner: load the `ugc-video` workflow
   (`get_workflow_instructions`) and its `references/duration.md`, then run
   `plan_duration.py` through `sandbox_exec` with `video.duration_seconds`.
   Use its exact `clip_durations` (for 31–35s, 3 clips such as 15+12+4).
   Don't make more clips than it returns; each clip is a paid job.
2. Assign the script's lines to clips, never cutting a sentence across clips.
   Check each clip's words fit its length at about 2.5 words per second.
3. For each clip write:
   - **Clip N — Xs — beat(s)**
   - **Spoken line(s):** the exact words
   - **Shot:** framing (selfie close-up, mid shot, product close-up), camera
     (handheld, static), setting
   - **Action:** what the person physically does, kept simple. Prefer one main
     action per clip. Hands should hold one object or rest naturally. Avoid
     complex finger work, fast gestures and objects passing between hands;
     those are where AI video breaks.
   - **Product visibility:** when and how the product appears; label facing camera
   - **Emotion / delivery:** tone of voice, facial expression
   - **On-screen text:** usually none (captions are added at assembly)
4. Add a **Continuity sheet** at the top: the person's look (copied from
   `brief.md`), wardrobe, setting, lighting and time of day. These stay
   identical in every clip.

Write `storyboard.md`.

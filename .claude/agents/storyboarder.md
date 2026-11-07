---
name: storyboarder
description: Stage 5. Only after story-review.md says APPROVED. Decides talking-head vs voiceover per clip, picks the audio source, and splits the story into Higgsfield clips describing exactly what is said and shown. Writes storyboard.md.
---

You decide what the viewer SEES and HEARS second by second. Don't start
unless `story-review.md` says APPROVED. Don't change the approved words.

0. **Decide the clip type and audio source. This is a hard rule:**
   - **Someone speaks on camera (talking head):** the voice MUST be generated
     by the same Higgsfield video model, in the same clip (Seedance 2.5 with
     `generate_audio: true`, or Higgsfield Intone). Never make that voice in
     ElevenLabs and lay it over the video; the lips won't match.
   - **Voiceover only (nobody's mouth is speaking on screen: b-roll, hands,
     product shots, the person seen from behind):** the voice can be made in
     ElevenLabs and the video generated silent or with ambient sound only.
     The voiceover must use one voice for the whole video.
   - Don't mix a native on-camera voice and an ElevenLabs voice for the same
     person in one video; viewers hear the change.
   Write the decision and the reason at the top of the storyboard.

1. Get the clip split from Higgsfield's planner: load the `ugc-video` workflow
   (`get_workflow_instructions`) and its `references/duration.md`, then run
   `plan_duration.py` through `sandbox_exec` with `video.duration_seconds`.
   Use its exact `clip_durations` (for 31–35s, 3 clips such as 15+12+4).
   Don't make more clips than it returns; each clip is a paid job.
2. Assign the script's lines to clips, never cutting a sentence across clips.
   The hook question (the first ~5s) should open clip 1 cleanly, so it can be
   regenerated or A/B-tested on its own later.
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

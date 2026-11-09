# Prompting research: hands, applying and peeling (Nov 8, 2026)

Why this exists: the owner flagged that the hands never really hold the patches. In v4 the patch looks stuck to a flat palm, with the sticky side facing the wrong way. Applying and peeling the patches are the two shots almost every video needs, so both must look real. This file joins web research (three research passes: Kling, Veo/Gemini, and how polished AI ads are made) with what our own runs taught us. It feeds `learning/apply-recipe.md` (draft) and `learning/peel-recipe.md` (locked).

Source quality: Google's and Kling's own guides are solid. Most of the hand-specific advice comes from vendor blogs and creator posts. It is consistent across sources but unproven. Nobody has published a test of a two-finger pinch on a thin clear object, so we have to find that ourselves.

## 1. What we were missing (ranked)

1. **The grip must already be in the start still.** Models can move a grip that is already there. They are bad at inventing one mid-clip. Our v4 apply still showed flat, straight fingers, so Kling animated exactly that. Fix: the still shows a thumb-and-index pinch on the patch's edge, fingertips visible, the other fingers curled loosely, and the hand in frame from the first frame. Reject any still with fused, blurry or flat fingers. Motion makes still errors worse. (Kling motion guide; Higgsfield hands blog; Magic Hour)
2. **One slow action per clip, with a clear end point.** Each clip does one action: lift the patch to her face, OR press it on, OR smooth it, OR peel. Describe the motion in stages (prepare, main action, finish), then say how it ends, e.g. "…then her fingers rest still on the patch". An action with no end point tends to stall or freeze. (Kling motion guide; CrePal; Veo prompt guide)
3. **Describe the contact physically, hand first.** Say which fingertips touch which edge, where the object is, how far the camera is, and the one detail that must stay visible. Hands hold steadier when they touch something than when they move through empty air. (Kling motion guide; Atlas Cloud)
4. **Describe only the motion; the still does the rest.** Google says this directly for image-to-video, and Kling says the same. Our prompts re-describe the whole still at length, which is the opposite. Keep the PATCHES block (owner rule), but the motion part should be short and come first. (Vertex AI Veo best practices)
5. **Keep negatives short and specific.** Three to five named defects work better than long lists, e.g. "extra fingers, fused fingers, patch stuck to the palm, white glare spots". Never ban "hands" outright. Long lists make motion stiff. Veo prefers describing the wanted state positively. (Atlas; Google Veo prompt guide)
6. **Polished AI ads get there by hiding the hard moment and making many takes.**
   - Many "clean AI" patch ads are real creator footage or a mix of real and AI. Dermaclara's ad pool is largely paid creators (Modash). Check the Ads Library "AI info" label before treating an ad as the bar.
   - Making 5–10 takes per usable shot is normal.
   - They cut around the hard frames and use only the best 1–3 s.
   - The approach that best explains "almost no errors" is **motion transfer**: a real person films the pinch, peel and press, and Kling 3.0 Motion Control (on Higgsfield) copies that motion onto our character still. Kling's guide asks for one continuous shot, 3–30 s, a still camera, and framing that matches the still.

## 2. Gemini is probably not Veo any more

Google's video page says Gemini Omni Flash "will replace Veo in the Gemini app". It makes clips up to 10 s, takes up to 5 photo references, extends scenes and edits by chat. Our clips are about 8–10 s, which fits.
- Omni uses chat edits: say "keep everything the same", then ask for one change ("change only the grip to a thumb-and-index pinch on the patch edge").
- Omni supports first and last frames, and storyboard images with a reading order.
- Flow still has Veo 3.1 frames-to-video until **Dec 5, 2026**.
- Gemini usage limits refresh every 5 hours, with a weekly cap: Settings → Usage limits. Video costs a lot of the allowance. On Nov 8 the page said 0% used (resets 12:55 AM) and 8% of the weekly cap (resets Nov 15).

## 3. How this fits what we already learned

| Our lesson | Research | Rule now |
|---|---|---|
| Peel: start mid-peel, chain two clips, no end frame (`peel-recipe.md`) | Start frame holds the action; regenerate only the broken piece; keep clips short | Keep as is. For peels, an end frame made the hand sweep across her face, so it stays banned there |
| Hands go bad in the last third | Not documented; makes sense: chain clips, or add an end frame for short moves | For **applying**, test an end frame where the patch is already on her skin with the fingers just lifting off. It is a short move, unlike the peel |
| Same light on hands and face | Kling keeps the still's lighting; fix the light in the still, not the prompt | Check it at gate A on the still, before any clip |
| Kling melts hands that drop fast | Fast moves cause smearing; slow, deliberate motion holds | Never write a fast hand move; cut before the hands drop |
| White blob on the patch tab | Not documented; clear glossy plastic reads as glare | Keep "soft satin sheen, never white"; add "white glare spots" to the negatives |
| Use the best 1–3 s | Same advice from every source | Keep |

## 4. What to test next (no credits until the owner says go)

1. **Gemini first (free):** an apply clip from a new still that already has the pinch. Use the draft in `learning/apply-recipe.md`. Iterate with chat edits, changing one thing at a time.
2. **If Gemini can't hold the pinch after 3 takes:** ask the owner to film a 5–10 s phone clip of their own hand pinching a patch, pressing it on, and later peeling it off. Shoot it waist-up or face-close, steady phone, good light, slow moves. Run it through Kling 3.0 Motion Control (one paid test, cost checked first). This is the most likely way to match the clean ads.
3. Kling 4.0 has been on klingai.com since Oct 15 (30 s clips, many references). Check whether Higgsfield offers it before the next paid test.

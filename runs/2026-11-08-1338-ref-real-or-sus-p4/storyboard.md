# Storyboard: "REAL or SUS?" expert stitch, P4, MOF (run 2026-11-08-1338)

Stage 5 (storyboarder). Built from the APPROVED `story.md` v2 (story-review fixes 1–8 applied). The spoken words,
timings and structure are unchanged. No credits spent; only `get_cost` preflights were run.

Read first: `learning/owner-feedback.md` (all), `docs/lessons-learned.md` (all), `CLAUDE.md`, `pipeline/config.yaml`,
`learning/production-log.md`, `brief.md`, `format.md`, `story.md`, `story-review.md`.

## 0. Decisions at the top

### Video type and audio source
- **Mixed: silent UGC + a talking expert.**
- **The woman never speaks.** Her clips U1 and U2 have no voice: music and room tone are added in assembly, plus a soft peel SFX.
- **The expert speaks on camera.** His voice is **native**, generated in the same Gemini (Veo) clip as the picture (lessons §0: "Gemini (Veo) for talking clips"; talking on camera means native voice). One man, one voice description, word for word in every Gemini prompt.
- **No ElevenLabs, no voiceover.**
- **Patches on means lips closed.** She has the band on in U1 (end) and U2 (start), always silent, with the corners of her mouth level. She gets a closed-lip look only once the band is off (U2 end).

### Generators (owner direction, Nov 8, 2026)

| Clips | Generator | Why |
|---|---|---|
| X0, E1, E23, E45 (the expert) | **Google Gemini Veo** (owner's Plus plan; free within the daily limit) | Owner: "10x better than Kling at lip sync". It takes the existing expert reference image as the first frame, so the face stays identical across clips |
| U1, U2 (the woman) | **Higgsfield: Nano Banana 2 stills + Kling 3.0 pro**, with start and end frames | Recommendation, see below |

**Why U1 and U2 go on Higgsfield, not Gemini:**
1. **Product accuracy is what matters in these two shots.** Higgsfield is our proven route: the Forehead-patch Element `<<<6375c707-…>>>` in the prompt text, the PATCHES block verbatim, and "tab pointing DOWN" written into every still. Gemini can take a pasted image but not our Elements. It has also invented patch shapes before.
2. **Gemini can't lock an end frame. Kling can.** The U2 end frame is the proof the whole video rests on (story-review: do not drop it). It is checked against gate A *before* any video is made.
3. **The peel is a known Gemini failure.** Lessons §8: in Gemini peel clips the patch "splits, goes rigid like a shell, floats or snaps off".
4. **Gemini's advantage doesn't apply.** Its edge is lip sync, and the woman never talks.
5. **Gemini's daily quota is better spent on the four expert clips.**
6. **Cost fits the cap.** Higgsfield costs 29.25 credits (preflighted), leaving the 15-credit reserve inside 50 (`budget.json`).

### Medium
- **All video** (the reference is live footage).
- **Stills are used only as start and end frames.** The box and the flat lay are code pop-ups of real assets, the same as in the reference, where the product shows as a cut-in.
- No still stands in for a beat, and no clip is slowed down.

### Cast (P4)
- **Reuse Higgsfield media `3bcb3615`.** It fits P4: a white woman of about 45, light-brown hair, hazel eyes, freckles, natural pores.
- **The image is a 2-panel split** (syringe mascot | woman in patches). It is **never passed whole** (lessons §5 rule 5). It is cropped in code to the woman's panel: `p4sb/3bcb-crop-right.png`, 536×953, crop `536:953:405:60`.
- **The crop is uploaded as Higgsfield media** (free) and used only for identity.
- **Risk:** in the crop she wears old-shape patches (wide pads), smiles and looks off-camera. The first still (S_B0) therefore removes the patches and sets her neutral and bare. It is checked hard at gate A for any leftover outline.
- **Fallback if S_B0 keeps patch ghosts:** one still fix within the 3-credit auto allowance. Rebuild from the crop, with the face described in words.

### The expert's background (E1)
- **E1 is shot on chroma green,** like the other expert clips. It is not shot in a clinic.
- **Why:** the Gemini method uses the green reference photo as the exact first frame. Asking Veo to change the room inside the clip risks the face and the coat drifting, and a clinic room would be an invented set that matches nothing else in the video.
- **Assembly:** key E1 full-screen over a live, blurred, 25%-darkened loop of U2's last 2 s (her softer forehead). This is the classic green-screen stitch look: the expert in front of the video he's judging.
- **The real box pop-up** (`face-set-box-v1.png`) sits mid-frame on the frame-right side, where his empty open hand gestures.
- Free, and all live video.

### Owner rules applied
- Hard cap is 50 credits, all versions included.
- One generation per shot.
- Nothing may look like an injury: no redness or outline after the peel.
- No exaggerated reactions: X0 is understated.
- No stated credential: no badge, no "Dr.", no tag.
- The expert never holds the product.
- Text is added in code only.
- Approved claims only.

## 1. Continuity sheet

**Woman (U1, U2):**
- **Identity:** the person in the `3bcb3615` crop. A 46-year-old white American woman with light-brown hair, hazel-green eyes, light freckles across her nose and cheeks, fair natural skin with visible pores, and the small stud earrings shown.
- **Hair:** pulled fully back off the forehead. Night: a tortoiseshell claw clip. Morning: a low bun at the nape.
- **Wardrobe:** a sage-green cotton tank top with no print.
- **Set:** an American bedroom, white pillows, a light-grey upholstered headboard.
- **Light at night (U1):** a bedside lamp low on the **frame-left** side that grazes her forehead, so the lines read at rest.
- **Light in the morning (U2):** soft daylight from a window on the **frame-left** side, at the same angle and similar warmth and contrast. Not bright, not blue, no glow.
- **Camera:** front camera, phone propped on a stand slightly above eye level, about 40 cm away. Head and top of shoulders in frame, face about half the frame width. Nearly locked, faint sway. Same framing at the start and end of each clip (production log 93: different framings made Kling insert a hard cut).
- **Skin:** unretouched, dry and matte, no cream.
- **Lines at rest:** moderate horizontal forehead lines and two faint vertical frown lines. The brows never rise.

**Expert (X0, E1, E23, E45):**
- **Identity:** the Gemini reference image `scratchpad/gemini-p4/gemini-expert-ref.jpg`, checked. A man of about 55 with silver hair, a trimmed grey beard, thin metal-rim glasses, a white coat over a light-blue shirt, no badge, no name tag, no embroidery, on flat chroma green, 9:16.
- **Voice, word for word in every talking prompt:**
  > in a warm, confident, conversational American male voice at a natural, slightly brisk pace, like a friendly expert explaining on TikTok
- **Hands:** always empty. He never holds or draws any object, box or patch.

## 2. Keyframe chain (Higgsfield stills; each one is an edit of the previous)

| ID | Built from | State list |
|---|---|---|
| CROP_3BCB | `3bcb3615` → code crop → media upload (0 credits) | Identity reference only (her old patches are ignored) |
| S_B0 bare base | Edit of CROP_3BCB | Night, lamp on the frame-left side grazing her forehead. Half-reclined on white pillows. Claw clip, sage tank top. **Bare face, no patch anywhere.** Lines visible at rest. Neutral, lips closed. No hands. The clean anchor for any rebuild |
| S_U1_START | Edit of S_B0 + Forehead Element | Same, plus **both hands hold the clear band up close to the lens** at forehead and eye height, tab down, frosted edge catching the lamp, her face seen through it. Exactly two hands. Band off the skin |
| S_U1_END | Edit of S_U1_START | **Band on**, covering the middle two-thirds of the forehead, tab DOWN between the brows, not reaching the hairline. Lines faintly visible through it. **No hands.** Neutral, lips closed, mouth corners level. Only the forehead piece |
| S_U2_START | Edit of S_U1_END | **Next morning:** lamp off, soft window daylight from the frame-left side. Sitting up against the headboard. Low bun. Band still on, same placement. No hands. Neutral, a little sleepy, lips closed |
| S_U2_END (**the proof**) | Edit of S_U2_START | **Band off**, hanging from the thumb and index finger of her frame-right hand at cheek height as one soft curved sheet. Exactly ONE patch, one hand. **Forehead lines visibly softer but still faintly there**; same pores and freckles; even tone, no outline, no redness, no glow. Small, calm, closed-lip satisfied look |

The expert needs no new stills: every Gemini clip starts from `gemini-expert-ref.jpg`.

## 3. Clip plan

### U1, 5 s, Higgsfield Kling 3.0 pro, silent. Story 0.0–5.0
- **Spoken line:** no speech.
- **Frames:** start S_U1_START → end S_U1_END.
- **Shot:** selfie close-up, phone propped, nearly locked. No mirror.
- **Motion:**
  - 0–1.2 s: she draws the band away from the lens down to chin height. Her bare forehead shows, brows relaxed, lines visible at rest.
  - 1.2–2.5 s: she lays it on her forehead, tab down between the brows.
  - 2.5–4 s: two flat hands press it from the center outward to the temples.
  - 4–5 s: her hands lower out of frame and she rests her head back, looking at the lens.
- **Must not move or change:** the lamp, the pillows, the headboard, her wrinkles.
- **Delivery:** calm, matter-of-fact, lips closed, no smile.
- **Fallback (story §9):** if the press-on fails, cut from the lowered band (≈1.2 s) to the end frame.
- **Note for the prompt-reviewer:** lessons §0 says applying should look organic, "she presses one on while holding the phone". The approved story uses a propped phone and a two-hand press (story-review fix 6), because a 14 cm band can't be pressed flat one-handed. The approved story governs.
- **On screen (code):**
  - Title "REAL or SUS? Wrinkle smoothing patches": lilac with a white stroke, top, below the top 14%.
  - Bottom caption "When people ask if I've had Botox but I just sleep in my Wrinkle Smooth patches": white with a black stroke, at 55–64% of frame height.
  - Both stay up 0–11 s.

### X0, Gemini, ≈8 s generated, ≈6 s used. Corner overlay 4.0–10.0
- **Spoken line:** none. One soft "huh" under his breath is allowed; assembly keeps it at least 12 dB under the music or mutes it.
- **Motion:**
  - 0–5 s: he watches a phone just below the lens, neutral, with a slightly skeptical squint.
  - ≈5–6.5 s: his eyebrows rise, his head draws back a little, a quiet "huh", then a small closed-lip smile and one slow nod.
  - Then he holds that impressed look, mouth closed.
- **Not allowed:** a gasp, a wide-open mouth, a hand to his face.
- **Assembly:**
  - Key out the green, crop to head and shoulders, and place him lower-left with his face at least 250 px wide and above the bottom 35%. His box must not cover her forehead.
  - Pick the 6 s window so the eyebrow lift lands at **9.0 s**, the reveal.

### U2, 6 s, Higgsfield Kling 3.0 pro, silent. Story 5.0–11.0
- **Spoken line:** no speech. Soft peel SFX.
- **Frames:** start S_U2_START → end S_U2_END.
- **Motion (lessons §6 fold-back, close to the skin; never "lifts away" on its own):**
  - 0–0.9 s: her frame-right fingertips pinch the corner at the temple and lift only that corner a few millimetres.
  - 0.9–2.7 s: she pulls it sideways, flat against the skin. It folds back over itself, and a fold line with a highlight travels to the frame-left temple.
  - 2.7–3.2 s: the last edge lets go, and the band hangs from her fingertips.
  - 3.2–4.2 s: she brings it to cheek height. Her eyes close briefly, shoulders relax, mouth shut.
  - 4.2–6 s: she looks into the lens with a small, calm, closed-lip satisfied look. The reveal reads at ≈9.0 s of video time.
- **Skin:** never stretched, never red, no outline.

### E1, Gemini, ≈8 s generated, ≈3 s used. Story 11.0–14.0, full screen
- **Spoken line:** "It's the Wrinkle Smooth Face Set." (6 words)
- **Motion:** he starts speaking at once. During the line, one empty open hand at chest height gestures toward the frame-right side, then lowers. After the line: a closed-lip, pleasant look and one small nod, mouth closed until the end.
- **Assembly:**
  - Key over the blurred, darkened U2 tail loop.
  - The real box pop-up goes mid-frame on the frame-right side from 11.4 s.
  - The top text "It's The Wrinkle Smooth Face Set!" goes below the top 14%.
  - Use the line plus about 0.3 s of the nod.

### GEM_E23, Gemini, **already generated**, 10.03 s. Story 14.0–23.0 (E2 + E3 merged)
- **Spoken line:** "They hold your skin flat all night, so it can't crease. No needles. They seal in moisture, so lines look smoother by morning." Whisper matches exactly.
- **Status:** generated without prompt review, so it is listed in `prompts.json` as "generated, pending review". It must now pass the prompt-reviewer's after-the-fact check and the generation review (Whisper ✓; mouth crops on m/b/p; checklist B).
- **What I saw on a 1 fps contact sheet:**
  - Same face, coat and green throughout.
  - His whole hand goes to his forehead at ≈1–2 s, not two fingertips. Fine.
  - An open-hand gesture at ≈3 s; small head movement.
  - 720×1280: it needs upscaling to 1080.
- **Layout:** green screen split.
  - Top half: U1 (band pressed on) during "They hold… crease."
  - Then a hard cut at "No needles" to U2 (peel → reveal), with a 112→118% punch-in on the expert at that word.
  - Pauses trimmed to ≤0.3 s.
  - The "No needles" chip goes in at that word.
  - Word-by-word captions above the bottom 35%.

### E45, Gemini, ≈8 s generated, ≈6.5 s used. Story 23.0–29.5 (E4 + E5 merged)
- **Spoken line:** "Tape and one-size patches can fall off. This kit is shaped for each area. My verdict? Real. Not sus." (19 words)
- **Motion:** no hand gestures while he speaks. A short beat after "My verdict?". After the last word, one small nod and a warm closed-lip smile.
- **Layout:**
  - Top half 23.0–27.5: the real flat lay `564c68fa` (pop-up, live code push 100→106%), with the code labels "forehead · under-eyes · smile lines".
  - Top half 27.5–29.5, from "My verdict?": U2's softened-forehead end region at 1×.
  - Trim pauses first. A ≤1.08× whole-clip speed-up is allowed if the line runs over.

### End card, 29.5–30.6
- The same layout, held live on the clip tails.
- "REAL! Not SUS" (lilac, white stroke).
- "Comment REAL for the link" under it, above the bottom 35%.
- Music tail.

### Word-count note
- E23 has 21 words and E45 has 19, above `video.talking_clip.max_words` (15).
- That cap was set for Kling's lip sync. The owner directed the merges to save Gemini quota, and Veo makes 8–10 s clips with native speech. E23 came back with the words exact.

## 4. Gemini quota (owner's Plus plan)

| Clip | Status | Gemini generations |
|---|---|---|
| GEM_E23 | Generated (pending review) | 1 (already used) |
| GEM_X0, GEM_E1, GEM_E45 | Planned | 3 |
| **Total for this video** | | **4** (3 still to run, one each, no retries without the owner) |

- **Fallback if the quota runs out:** Higgsfield Kling 3.0 with native sound.
- **But it doesn't fit the cap.** About 2 credits/s std with sound (lessons §9), so X0 + E1 + E45 ≈ 6+3+7 s ≈ 32 credits. With the 29.25 already planned, that is ≈61, over 50.
- **Waiting a day for the quota is the free option.** Using Kling instead needs the owner's OK.

## 5. Order of work (producer)
1. Code crop (done) → upload CROP_3BCB.
2. Make S_B0. **Gate A** on it, especially for any leftover patch outline.
3. S_U1_START → S_U1_END → S_U2_START → S_U2_END, one at a time, gate A on each. The prompt-reviewer runs again on the approved stills.
4. U1 and U2 on Kling.
5. In the owner's Chrome, only after the prompt-review PASS: GEM_X0, GEM_E1, GEM_E45. Paste `gemini-expert-ref.jpg` into each Create video chat (Portrait), then move each download from ~/Downloads to `scratchpad/gemini-p4/`. Check each: Whisper words, mouth crops, checklist B, and 9:16 (Veo sometimes returns 16:9).
6. Assembly.

## Revision 1 (prompt-review pass 1, 2026-11-08)

All six fixes were applied word for word in `prompts.json`:
- **S_U1_START, S_U2_END:** the band is a thin, flexible sheet about 1 mm thick.
- **S_U2_END:** the forehead lines are "about two-thirds as visible, every line still traceable".
- **S_U1_END:** now edited from S_B0, so exactly ONE band is in frame and nothing is in front of the lens.
- **S_U2_START:** guards added for the same framing and exactly one head.
- **GEM_X0:** no "huh"; his lips stay closed and he makes no sound. This replaces the "huh" in §3 X0.
- **GEM_E1:** he is "pointing out something just off-screen", and the space beside him stays empty green.

GEM_E23 passed the generation review.

**E45 overrun:**
- Expected speech is about 8.3 s at Veo's 2.34 words/s. After pause trims and a ≤1.08× speed-up that is about 7.0–7.5 s, against a 6.5 s window.
- So the end card slides 0.5–1 s, to about **31 s total**. That is accepted (the reference is 30.6 s).
- The generation review compares E1's and E45's voices against E23.

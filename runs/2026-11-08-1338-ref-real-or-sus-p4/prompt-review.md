# Prompt review, pass 1: "REAL or SUS?" expert stitch, P4 (run 2026-11-08-1338)

Stage 6b (prompt-reviewer), pass 1. No credits spent and no Chrome used.

**What I read:** `learning/owner-feedback.md` (all), `docs/lessons-learned.md` (all), `.claude/agents/prompt-reviewer.md`, `learning/production-log.md`, `pipeline/config.yaml`, and this run's `brief.md`, `story.md` (v2), `story-review.md`, `storyboard.md`, `prompts.json` and `budget.json`.

**What I looked at:**
- `gemini-expert-ref.jpg`
- `p4sb/3bcb-crop-right.png`
- `ref2/sheet.jpg`
- GEM_E23: a 4 fps sheet, 12 fps mouth crops, chroma-key tests at 1.2, 2.4, 6 and 9.5 s, and a Whisper small.en transcript with word timings. All are in `scratchpad/gemini-p4/rev/`.

**Owner instruction applied:** Gemini is "just another option to generate". The GEM_* prompts get the same checks as the Higgsfield ones.

## Verdict: **FIX**

Six jobs need text changes and five are OK. GEM_E23 **PASSES** its generation review. The budget fits: 29.25 credits planned plus a 15-credit reserve comes to 44.25, under the cap of 50.

## Job table

| Job | Verdict | Finding |
|---|---|---|
| CROP_3BCB | OK | Single panel, 9:16, identity only. It is never passed as the split image |
| S_B0 | OK | Opens with "A NEW photo" and says the photo is for identity only (production log 92 fix). Removes the old pads explicitly. Lines are grazing-lit with no brow raise; one person, one head; STYLE block verbatim. Gate A must check for pad ghosts |
| S_U1_START | **FIX** | The held band is likely to come out as a thick, milky, stiff slab. That happened three times (production log K6, K6 fix, 23–24). See fix 1 |
| S_U1_END | **FIX** | This edit moves the band from in front of the lens onto her forehead. Edits can't reliably move a product piece: nano_banana kept the source, split it or doubled it in K5, K5-fix and K6 (production log 18–24). Expect two bands: the old one by the lens and a new one on her forehead. See fix 2 |
| S_U2_START | **FIX** | One edit changes the light, the pose (reclined to sitting up) and the hair at once. Production log 78–79 (a second head after a pose change) and 92 (a near copy when the whole scene changes) both apply. See fix 3 |
| S_U2_END | **FIX** | This is the proof frame, and it risks two things. First, the band could read as a slab (same cause as fix 1). Second, "visibly softer" alone over-smoothed before (production log 33: "can't be real"). See fix 4 |
| U1_APPLY | OK (pass 2 re-checks it against the approved stills) | One action, with timed beats. Brows stay relaxed; two hands are correct here; lips closed; no cuts; same framing at both ends. PATCHES block verbatim. Pro, 5 s, sound off, 8.75 credits |
| U2_PEEL | OK (pass 2) | The peel follows lessons §6 word for word: folds back, pulled sideways close to the skin, fold line, "never pulled or stretched", no redness. One hand, mouth shut. Note for pass 2: at 3.2–4.2 s her hand crosses back over her face to the frame-right cheek. If the S_U2_END still allows it, place the held band on the frame-left side to shorten that path |
| GEM_E23 | OK (already generated; see the generation review below) | The prompt passes on its own merits: exact words in the "exactly these words" form, the voice sentence verbatim, no caps, "only his voice and quiet room tone", empty hands, flat green. Claims are §2-approved |
| GEM_X0 | **FIX** | The prompt tells him to be silent and also to say "huh" with his lips parting. That contradicts itself, and a silent corner face with parted lips reads as mouthing. The sound gets muted in assembly anyway. See fix 5 |
| GEM_E1 | **FIX** | "As if presenting something beside him" invites Veo to draw a box or product beside him. The prompt bans anything in his hands, but not an object in the frame. See fix 6 |
| GEM_E45 | OK, with notes | Words match story v2 exactly. The voice sentence is verbatim, "sus" has a pronunciation note, and he ends on a closed-lip smile. **Timing:** 19 words plus a pause at Veo's measured ≈2.34 words/s comes to about 8.3 s of speech, or about 7.0–7.5 s after pause trims and a ≤1.08× speed-up. The window is 6.5 s, so the end card may slide 0.5–1 s, to about 31 s total. That's acceptable (the reference is 30.6 s). **Voice:** every Gemini chat is a fresh generation, so the generation review must compare E1's and E45's voices against E23 (lessons §8: voice changes between clips) |

## Exact replacement text

**Fix 1: S_U1_START.** Replace
`The band is slightly out of focus because it is close to the lens;`
with
`The band is a thin, flexible, see-through sheet about 1 mm thick that bows softly between her fingers, never a thick or stiff slab; it is slightly out of focus because it is close to the lens;`

**Fix 2: S_U1_END.**
- Change `medias[0].value` from `$S_U1_START` to `$S_B0`. That is the clean frame with no band or hands, so the framing still matches S_U1_START because both are built on S_B0.
- Replace
  `CHANGES ONLY: the clear forehead piece is now on her forehead, lying completely flat,`
  with
  `CHANGES ONLY: exactly ONE clear forehead piece is in the image, and it is on her forehead; nothing is held in front of the lens and nothing is between the lens and her face. It lies completely flat,`

**Fix 3: S_U2_START.**
- Replace
  `She now sits up against the headboard instead of reclining.`
  with
  `She now sits up against the headboard instead of reclining; the camera keeps the same height, distance and framing, her head and the top of her shoulders filling the frame as before. Exactly one person and one head in the image; nobody beside her; no second face, head or hair anywhere.`
- Fallback, as one still fix within the 3-credit allowance: if the result comes back still lamp-lit (a near copy), redo it reclined, keeping S_U1_END's pose and changing only the light and the hair.

**Fix 4: S_U2_END.**
- Replace
  `as one soft, curved, transparent, slightly frosted sheet with its small rounded tab,`
  with
  `as one thin, flexible, see-through sheet about 1 mm thick that droops softly between her fingers, transparent and slightly frosted, with its small rounded tab, the headboard showing through it,`
- Replace
  `the horizontal lines are visibly softer and shallower than before but still faintly there,`
  with
  `the horizontal lines are visibly softer and shallower than before, about two-thirds as visible, every line still traceable,`

**Fix 5: GEM_X0.**
- Replace
  `and he lets out one quiet, short "huh" under his breath, lips barely parting; then a small closed-lip smile`
  with
  `with his lips staying closed; then a small closed-lip smile`
- Replace
  `Only quiet room tone and that one soft "huh", no music, no words.`
  with
  `Only quiet room tone, no music, no words and no sounds from him.`

**Fix 6: GEM_E1.**
- Replace `as if presenting something beside him,` with `as if pointing out something just off-screen,`.
- After `he never holds, shows or draws any object, box, product or patch.` add:
  `The space beside him stays empty flat green: no object, box, product or screen appears anywhere in the frame.`

## Word count for the Veo clips (E23 has 21 words, E45 has 19)

**This is fine for Veo.** The 15-word cap in `video.talking_clip` came from Kling's weak lip sync. E23 is the evidence for Veo:
- 21 words in 9.0 s of speech (2.34 words/s, our planning rate).
- The Whisper transcript is exact.
- The lips close on the m and b sounds in "moisture", "smoother", "by" and "morning" (crops at ≈5.9, 7.8, 8.4 and 8.6 s).
- No smeared or frozen mouth.

**Rule for Gemini clips:** words ≤ 2.3 × the usable seconds, which allows up to about 21 words in a 10 s clip. Kling clips keep the 15-word cap. **Caveat:** the clip's length is set by Veo, not by us. A merged line has to fit the story window after pause trims, which is why E45 runs about 0.5–1 s long (see the table).

## U1: propped phone and a two-hand press

**It looks organic and is not posed.** The reference itself does exactly this. In sheet rows 1–2, the creator lies in bed, holds the band up to the lens with both hands, then presses it on with two hands to a propped or held phone.

What the lessons §0 line guards against is a silent, posed lying-down shot. U1 avoids that:
- it's a live selfie action in her own bedroom;
- the camera is front-facing with a faint sway;
- she ends looking into the lens, not posing.

The approved story governs, and I'm not changing it.

## GEM_E23 generation review: **PASS**

File: `scratchpad/gemini-p4/gemini-expert-E23-mechanism.mp4`. 720×1280 at 24 fps, 10.0 s of video and 10.03 s of audio, 9:16 (not 16:9).

| Check | Result |
|---|---|
| Words | Whisper small.en: "They hold your skin flat all night so it can't crease. No needles. They seal in moisture so lines look smoother by morning." **Exact**, in order, nothing extra. Speech runs 0.04–9.0 s; 9.0–10.0 s is a closed-lip, pleasant hold, usable as a tail |
| Lip sync | Natural: the jaw and lips track each syllable, and teeth show on open vowels. The lips close fully on the m and b sounds in "moisture", "smoother", "by" and "morning". No mumbling, freezing or doubled lips. The first line has no bilabials and reads clean |
| Face and identity | The same man as `gemini-expert-ref.jpg` in all 40 frames: silver hair, trimmed grey beard, thin metal-rim glasses, white coat, light-blue shirt, no badge or tag. No drift |
| Expression | Warm and conversational; a normal blink at about 2.4 s. No overacting |
| Hands | ≈0.5–1.75 s, on "hold your skin flat all night": a flat whole hand on his forehead, not two fingertips. ≈2.0–2.75 s: an open-hand gesture. Empty hands throughout, normal fingers, nothing passes through his face or glasses |
| Gesture vs. story and claims | **Note only, not a problem.** The flat hand shows "hold your skin flat" more clearly than fingertips would, and the reference creator makes the same whole-hand-to-forehead gesture (sheet row 4). He holds no product and doesn't imply he wears one, so no claim changes |
| Green screen | Flat and even: RGB ≈ (59,128,64) top-left to (72,142,76) right, stable across time. A plain chromakey (0x408a48, similarity 0.045, blend 0.02, despill) gives a clean edge on the hair, glasses, beard and coat. The only residue is a small darker, noisy green patch at the bottom-left and bottom-right corners below the shoulders, which falls outside the head-and-torso crop. The hand leaves the frame-right edge at ≈1.0–1.7 s; a crop that includes the right edge shows it cut off, which is fine |
| Audio | His voice and room tone only; no music |
| Assembly notes | Key at native 720, then scale about 1.5×. His face is about 200 px wide at 720, so it reaches the required ≥250 px at 1080. Pace fits the 14.0–23.0 window (9 s) with no speed-up. Cut to U2 and punch in at "No needles" (≈4.0 s) |

**Verdict: PASS.** It's usable as is.

The process miss remains: this clip was generated before prompt review, which is now logged as an owner rule.

## Production log additions
Two lines appended to `learning/production-log.md`:
- GEM_E1: the "presenting something beside him" wording.
- GEM_X0: the silent clip that was also asked to say "huh".

The Veo word-rate evidence is recorded above for the main session to promote if the owner agrees.

---

## Round 2: prompts.json revision 1 — **PASS**

I re-checked all 12 jobs with the same checks. No credits spent and no Chrome used.

**All six fixes are in, word for word** (checked by string match):
- S_U1_START: the 1 mm sheet that "bows softly".
- S_U1_END: `medias` is now `$S_B0`, and the "exactly ONE… nothing between the lens and her face" sentence is in.
- S_U2_START: the same-framing line and the one-head guard are in.
- S_U2_END: the 1 mm sheet that "droops softly" and "about two-thirds as visible, every line still traceable" are in.
- GEM_X0: "huh" is gone; lips stay closed; "no sounds from him".
- GEM_E1: "pointing out something just off-screen" and the empty-green sentence are in. "presenting" is gone.

**Nothing else changed:**
- Every other prompt still holds the PATCHES, REFERENCE ROLES and STYLE blocks verbatim, plus the voice sentence and the hand counts.
- Costs are unchanged: 29.25 credits plus the 15 reserve = 44.25, under the cap of 50 (FITS).

**Continuity check:** S_U1_START and S_U1_END are now both edits of S_B0. That gives them the same framing and light, which is what U1 needs (production log 93).

**Notes carried from pass 1 (not blocking):**
- E45 may run about 0.5–1 s over its window.
- Compare E1's and E45's voices to E23's.
- Pass 2 re-checks U1 and U2 against the approved stills.
- U2's hand path back to the frame-right cheek.

**Verdict: PASS.** The stills may be generated. Video waits for pass 2 on the approved stills, and the Gemini clips (X0, E1, E45) may run.

---

## Pass 2: clip prompts vs the approved stills — **FIX** (3 jobs, text only)

**What I looked at:** `stills-p4/*_view.png`, meaning S_U1_START `bc7de156-fec4-46bd-bcdc-406fded0b847`, S_U1_END `180c1cb9-273f-4b8a-8c2f-18a02876587f`, S_U2_START `031f92d2-17f9-45c3-8a9b-dfa178641109` and S_U2_END `040d5330-a63b-4c88-948d-17207afb6342`. I also checked `stills-check.md` and lessons §6, including the new "Physics details" list. No credits spent and no Chrome used.

| Job | Verdict | Finding |
|---|---|---|
| U1_APPLY | **FIX** (small) | The stills match the prompt: both hands at the frame edges hold the band near the lens at eye height, tab down; the end frame has the band on, no hands, and the same framing, lamp and claw clip. Two changes: (a) put the full job IDs in `medias`; (b) the start frame already shows her forehead above the band, so "down to chin height, then back up" adds travel Kling doesn't need. Shorten it, and describe the perspective shrink as the band leaves the lens |
| U2_PEEL | **FIX** | The physics section delivers every lessons §6 item. Start and end match the stills. The **peel direction is wrong for the story** though: the frame-right hand pinches the frame-right temple, pushes across to the frame-left temple, then has to sweep back across her face to the frame-right cheek at 3.2–4.2 s. That puts a hand in front of her face at the **reveal** (story ≈9.0 s, which is clip ≈4.0 s). It's also a push-away motion, with the forearm trailing over the skin that was just uncovered. Reverse it: she reaches across, pinches the frame-left corner and pulls back toward her own side. The fold then travels left to right, the bare forehead shows behind it, and her hand ends on the frame-right side next to where the end frame has it |
| KL_X0 | **FIX** | Start media `1debf315-7e17-463f-b6ea-587e951ef544` is the checked expert ref; std, 5 s, sound off, 7.5 credits. Three gaps: (a) Kling overdoes brow raises (production log 30), so a full raise risks the overacting the owner bans; (b) the prompt lacks the checklist §4 silent-clip line; (c) the timing is written for an 8 s clip, but this one is 5 s |

### Exact replacement text

**U1_APPLY**
- `medias`: `start_image` → `bc7de156-fec4-46bd-bcdc-406fded0b847`; `end_image` → `180c1cb9-273f-4b8a-8c2f-18a02876587f`.
- Replace
  `she draws it away from the lens and down to chin height, so her bare forehead is clearly visible;`
  with
  `she draws it in toward her face and lowers it a little, to just below her eyes, so her bare forehead and brows are clearly visible above it; as it moves away from the lens it looks smaller, until on her forehead it is the size shown in the end frame;`

**U2_PEEL**
- `medias`: `start_image` → `031f92d2-17f9-45c3-8a9b-dfa178641109`; `end_image` → `040d5330-a63b-4c88-948d-17207afb6342`.
- **R1.** Replace
  `0-0.9s: her hand on the frame-right side comes up; her fingertips pinch the outer corner of the band at her temple on the frame-right side and lift only that corner a few millimetres. 0.9-2.7s: she pulls the free edge sideways across her forehead, close to the skin and flat against it; the peeled part folds back over itself onto the part still attached, and a straight fold line with a bright highlight travels across her forehead toward her temple on the frame-left side.`
  with
  `0-0.9s: her hand on the frame-right side comes up and reaches across, just above her eyebrows, to the outer corner of the band at her temple on the frame-left side; her fingertips pinch that corner and lift only that corner a few millimetres. Her forearm stays above her eyes. 0.9-3.0s: she pulls the free edge back toward the frame-right side, close to the skin and flat against it; the peeled part folds back over itself onto the part still attached, and a straight fold line with a bright highlight travels across her forehead from the frame-left temple toward her temple on the frame-right side; behind the fold, on the frame-left side, her forehead is already bare.`
- **R2.** Replace `2.7-3.2s: the last edge lets go at the frame-left temple;` with `3.0-3.5s: the last edge lets go at the frame-right temple;`
- **R3.** Replace
  `3.2-4.2s: she brings it to cheek height beside her face on the frame-right side;`
  with
  `3.5-4.2s: her hand drops a little to cheek height on the frame-right side, beside her face and never crossing in front of it; the sheet settles to hang down from her fingertips by one end, as in the end frame;`
- Everything else stays, including the PEEL PHYSICS section, the "Before she starts peeling…" PATCHES sentence, one hand and lips closed.
- **Timing after the fix:**
  - The peel takes 3.5 s (lessons §6: 3–4 s).
  - The forehead is bare and her hand is off her face from clip ≈3.5 s (story ≈8.5 s), before X0's eyebrow lift at 9.0 s.

**KL_X0**
- Replace everything from `0-3 s: he watches calmly` through `From 4 s to the end he keeps watching with that small impressed look, mouth closed.` with:
  `HE DOES NOT TALK: his lips stay closed the whole time. 0-3.5 s: he watches calmly with a neutral, slightly skeptical expression and a faint squint, natural blinking and small head movements. At about 3.5 s, as if he has just seen a surprising result, his eyebrows lift only slightly and his head draws back a little; then a small closed-lip smile and one slow nod of approval. From 4.5 s to the end he keeps watching with that small impressed look.`
- **Assembly:** place the clip at story 5.0–10.0, so the lift lands at ≈8.5–9.0 s with the reveal. That gives up the planned ≈4 s arrival: the judge enters at 5.0 s, still inside the 5 s cold-viewer window. Matching the plan's 4.0–10.0 window exactly needs 6 s std (+1.5 credits, about 9 total, preflight it). That's the owner's or main session's call.

### Peel physics: do we need a mid-lift still (about 2 credits)? **Not now.**
- **Kling can't use it in the middle.** Kling takes only a start and an end frame, so a mid-lift still could only become the *start* frame. That drops the hand-entry beat, or it means splitting the shot into two clips.
- **The still is a risk of its own.** nano_banana has drawn requested folds as glow instead of geometry (production log 59, P06B).
- **Kling can plausibly do it in 6 s.** With both ends locked (flat glossy band, then held sheet), the fixed prompt and the full §6 physics wording, a fold-back is within reach.
- **Budget:** 10 credits spent. U1 8.75 + U2 10.5 + KL_X0 7.5 brings it to 36.75, leaving 13.25 under the cap, which is **already below the 15-credit reserve**. A lift still would leave 11.25.
- **If the fold-back looks fake:**
  - Free fallback (lessons §6): cut from the corner lift (clip ≈0–0.9 s) to the bare, held-sheet tail.
  - Paid fallback, only with the owner's OK: one redo from a mid-lift still (fingertips pinching the frame-left corner, folded back about 2 cm in a rounded pencil-thick fold), at ≈2 + 8.75 credits.
- **End-frame stiffness:** S_U2_END's sheet hangs fairly straight. R3 makes the sheet settle "as in the end frame" after it sways, so Kling isn't fighting the lock.

### Notes
- **Skin tone after the peel:** lessons §6 says the skin underneath is "dewy… tiny trapped air dots". The locked end frame is matte, and dots could read as marks (the owner bans anything injury-like). Keep the prompt's "normal even skin tone, no marks".
- **Budget, for the main session to raise with the owner:** KL_X0 wasn't in the plan, so the reserve is now 13.25, under 15. E1 and E45 should wait for Gemini's daily reset (free). Kling with sound for those would push past the 50 cap.

**Verdict: FIX.** Apply U1 (IDs plus one sentence), U2 (IDs plus R1–R3) and KL_X0 (one block). No re-review is needed if the text is pasted word for word; the producer confirms each string is present before submitting.

### Pass 2 addendum: KL_E1 (the owner chose Higgsfield: "Do it on higgsfield, I have no patience") — **FIX** (one sentence)

| Check | Result |
|---|---|
| Words | "It's the Wrinkle Smooth Face Set.", in the "exactly these words, in this order, and nothing else" form. No caps. Six words in a 5 s clip, well under the 15-word Kling cap. After the line he stops talking, with his mouth closed to the end |
| Lip closures | One bilabial ("Smooth"), and "lips fully closing on m, b and p" is in the prompt. OK |
| Voice | Not the Veo sentence word for word. It adds "slightly deep… mid-50s". Since this is a different model, matching the description word for word wouldn't guarantee the same voice anyway, and the age cue moves it toward E23's voice. **Accept.** The voice mismatch risk is listed below |
| Hands and frame | Empty hands; "the space beside him stays empty flat green" is in, and nothing is "presenting". OK. **Gap:** it says "one empty open hand" without naming which. In the start frame, his arm on the frame-left side is the extended selfie arm. If Kling uses that hand, it drops the phone framing or a hand appears from nowhere (production log 27 and 46: name hands by frame side and count them) |
| Settings | kling3_0 std, 5 s, sound on (a talking clip), 9:16, start frame `1debf315-7e17-463f-b6ea-587e951ef544`, 10 credits. OK |
| Claims | Product name only. OK |

**Exact replacement.** Replace
`he raises one empty open hand to chest height and gestures toward the frame-right side,`
with
`he raises his free hand, the one on the frame-right side, empty and open, to chest height and gestures toward the frame-right side; his other arm, on the frame-left side, stays still holding the camera; exactly one hand with five fingers comes into view,`

**Voice-mismatch risk (for the generation review):** E1 (Kling) runs straight into E23 (Veo) at 14.0 s. If the two voices clearly differ, a cold viewer hears two different men with the same face. That's an instant "sus".
- Check by ear, and compare median pitch against E23.
- **Free fallback:** play E1's picture under music only, with the planned top caption "It's The Wrinkle Smooth Face Set!" and the box pop-up (story's 50-cap cut 1). Use the closed-lip nod section, so no mouthing shows.

**Budget:** 10 + U1 8.75 + U2 10.5 + KL_X0 7.5 + KL_E1 10 = **46.75 of 50**. That leaves 3.25: **no reserve and no clip redo possible**.
- This settles my KL_X0 option above: **keep it at 5 s.** At 6 s the total would be 48.25.
- Any failed clip goes to the free fallbacks (U2: cut from the lift to the bare tail; E1: caption with no voice) or back to the owner.
- E45 must wait for Gemini's reset: Kling with sound would exceed the cap.

**Pass 2 overall verdict: FIX** across 4 jobs: U1_APPLY (IDs plus one sentence), U2_PEEL (IDs plus R1–R3), KL_X0 (one block), KL_E1 (one sentence). These are text-only fixes, and no re-review is needed if they're pasted word for word.

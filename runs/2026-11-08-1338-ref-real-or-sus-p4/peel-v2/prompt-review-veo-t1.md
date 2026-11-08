# Prompt review: VEO_T1 (Gemini Veo peel test, start image only)

Stage 6b, prompt-reviewer. Nothing generated, no credits spent. I read `prompt-reviewer.md`, the last rows of `owner-feedback.md` (peel resistance, Gemini R&D), lessons §6 ("visible resistance" and "Staging that makes an AI peel work"), `peel_mid_1080.jpg` and my earlier `prompt-review.md` (Kling R1/R2).

## Verdict: **FIX** (small edits; the prompt is close)

**What already matches the start image:**
- The frame-right hand pinches the tapered right end of the band, and the frame-left index fingertip is on her temple, just beyond the band's left end. The prompt's sides match.
- The release line runs from frame-right to frame-left, the stuck part "never slides", the peel never folds back over the stuck part and never goes over her eyes. That covers the U2 slide/smear path.
- The resistance asked for in §6 is there: slow stop-start tugs, the anchor pressing, ripples with moving light, the skin lifting a hair and springing back, and no redness or marks.
- Lips closed, no talking. Sound: room tone plus a soft peel, no music or voice. All fine.
- It stays short and in plain language, which is right for Veo. The PATCHES block is waived for this free Gemini test, as the owner asked.

**Fixes:**

1. **The pull direction could take the hand out of frame.** Her frame-right hand is already almost at the frame edge (x≈1000/1080). If she pulls "sideways, away from her face", the hand and the strip leave the frame, or the model slides the whole band along its length to keep it in shot. Fix: she pulls outward, away from the forehead and a little toward the frame-right side, and her hand stays inside the frame.
2. **Stop-start invites the band to re-stick or creep back.** Fix: "the released part never sticks back down."
3. **Make sure the resistance doesn't read as an injury.** "Clearly stuck" plus the skin lifting can draw a wince. Fix: "a gentle, painless tug; her face stays relaxed, no wince."
4. **The last edge lets go right beside her anchor fingers.** If that isn't fenced off, fingers and silicone can merge. Fix: the last edge lets go "beside those fingertips without touching them."
5. **"Morning window light"**: no window is visible in the image. Fine as written, because the prompt says "exactly as in the photo". I left it.
6. **Hand tone** (owner rule): add "both hands keep the same skin tone as her face."

## Corrected prompt (use verbatim)

```
Animate this exact photo as a real, unedited 9:16 phone video, filmed on a phone propped on a stand: camera almost still, no zoom, no cuts. Keep her face, the bedroom and the soft light exactly as in the photo. She does not talk; her lips stay closed. Sound: quiet room tone and a soft, sticky peeling sound only; no music, no voice.
In the first 3 seconds she slowly peels the clear silicone patch off her forehead, and it is clearly stuck to her skin. The fingertips of the hand on the left side of the frame press firmly on her temple, holding the skin flat against the pull. The hand on the right side of the frame pulls the pinched end outward, away from her forehead and a little toward the right side of the frame, slowly and in small stop-start tugs; that hand always stays inside the frame. With each tug the release line creeps a little further across her forehead from the right side of the frame toward the left; the part still stuck stays perfectly in place and never slides, and the released part never sticks back down. Right at the release line her skin lifts a tiny bit with the silicone, then springs back flat as the edge lets go: a gentle, painless tug; her face stays relaxed, with no wince. The peeled part is soft and thin: it stretches slightly and ripples into small soft waves, with streaks of light moving across the ripples; it never stays flat and stiff, never folds back over the stuck part, and never slides down her face or over her eyes. At about 3 seconds the last edge lets go beside her left-side fingertips without touching them, with a small final tug, and the patch comes free in one piece, hanging floppy from the fingers on the right side of the frame. Then the hand on the left side of the frame lowers out of view, and she holds the patch beside her cheek on the right side of the frame, looks into the camera with a calm, closed-lip, satisfied look, and holds still.
Her skin stays its normal even tone, with no redness, marks or outline. Exactly one patch, one person, two hands with five fingers each; both hands keep the same skin tone as her face. The patch stays thin, transparent and slightly frosted the whole time: never milky, white, opaque, smeared, split or doubled. Her eyes stay open except natural blinks.
```

**After generation:** step through 0–3.5 s at 10 fps. Fail it for:
- any frame where the stuck part slides;
- the strip or hand leaving the frame;
- a milky or doubled band;
- the band re-sticking;
- red skin or a wince;
- the release line jumping instead of creeping.

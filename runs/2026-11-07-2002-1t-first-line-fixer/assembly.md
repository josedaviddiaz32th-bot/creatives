# Assembly: 2026-11-07-2002-1t-first-line-fixer (slot 1-T)

Producer, assembly only. **0 credits**: no Higgsfield or other paid calls. Everything was built locally with ffmpeg/ffprobe, Python/PIL and whisper-cli (small.en).

- **Final:** `final.mp4` in this folder (18.5 MB). Scratch copy and scripts: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/assembly-1t/` (`render.py` = picture + text, `audio.sh` = audio mix, loudnorm and mux).
- **Contact sheet:** `final-contact.png`. It's 2 fps, 12 frames per row, so row r, column c = t (r·12 + c)·0.5 s.
- **Spec:** 41.96 s (TOF window 30–50 ✅), 1080×1920, 24 fps (native Kling rate, so no 24→30 judder), H.264 High yuv420p, AAC 48 kHz stereo 192k.
- **Loudness:** two-pass loudnorm (target I −16 / TP −1.5 / LRA 11). Measured on the final with ebur128: **−15.9 LUFS integrated, true peak −1.5 dBFS, LRA 3.9 LU**. Pass 1 measured −18.5 LUFS and −2.3 dBTP. Linear gain would have clipped the peak ceiling, so loudnorm used its dynamic mode. That's gentle at this LRA.
- **Speech check:** Whisper on the final mix returns all 88 words in order. Nothing is lost at any cut.

## Timeline actually used (output time, 24 fps frame boundaries)

Source times are clip t (s). Overlays were timed to word onsets measured on the real audio: Whisper word timestamps cross-checked against a 100 ms RMS envelope, because Whisper's token offsets ran ~0.5–1 s early on clip A's and B1's openings.

| Out time | Picture | Audio | On-screen text (code, Helvetica Neue Bold, white on a 47% black rounded box + soft shadow) |
|---|---|---|---|
| 0.00–1.50 | **K2 POV** still: push-in from frame 0, blinking red timer dot (0–1.2), white flash at 1.21 decaying over 0.25 s | 2 synth timer beeps (0.12, 0.56), shutter = 2 high-passed noise clicks (1.21, 1.29). Clip A audio from A t0.5, so her voice enters at ≈0.85 (J-cut) | 0.00–3.00 **Filtering your lines / out of every photo?** (on from frame 0, no fade) |
| 1.50–3.33 | Clip A t2.0–3.83 (hook question) | A | ↑ |
| 3.33–11.29 | **K2 cutaway**: eased push-in to her face (3.33–5.58), then **FILTER \| ME wipe** at 5.58–6.33 (on "Me?"). Left half = bilateral-smoothed copy of K2, right half = real. The split sits left of her brow, so the **frown line, eye crinkles and right forehead stay on the ME side**. Slow 5% push continues to 11.29 | A ("My friends look smooth. Me? Frown lines… I filter it, feel like a fraud.") | 5.58 **FILTER** / **ME** labels at top · 7.71 **It ages me more than I'd like.** (above her head; never over her eyes/brow) |
| 11.29–12.50 | Clip A t11.79–13.0 | A (speech ends A 12.3) | 11.29 **And it keeps getting worse.** |
| 12.50–25.00 | Clip B1 t0.125–12.625 (A end → B1 start is a matched K1 frame, checked; no punch-in needed) | B1 | 13.46 **Tretinoin. Vitamin C. Peptides.** · 16.21 **Botox… of lesser strength?** · 22.17 **Worst when you wake up?** |
| 25.00–27.29 | **K3 sleep** still, slow 7% push-in | soft pillow rustle (filtered pink noise) at 25.0; B2 audio from 25.08, so "A lot of them…" starts at 26.0 | 25.00 **Nobody told me why.** (silent beat ≈1.3 s) · 26.00 **Pressed in. Every night.** |
| 27.29–30.79 | Clip B2 t2.21–5.71 (end of "every night", then her clean reach to the tray) | B2 | ↑ |
| 30.79–32.08 | **K5 cover** (sheet held beside her cheek), gentle 9% push-in that lands on B2's t7.42 framing | B2 from t6.125, so **0.42 s of dead air (B2 t5.71–6.125) is cut, hidden under the still**. "So now I sleep in these" starts at 30.9 | 30.79 **The Wrinkle Smooth Face Set** |
| 32.08–33.17 | Clip B2 t7.42–8.5 (film held; lips synced) | B2 | ↑ |
| 33.17–35.83 | **K4 press-on** still, slow 6% push-in. Silent picture, lips closed. **No return to B2 video after this** | B2 (L-cut): "They hold my skin flat all night." | 33.88 **Holds skin flat all night** + small **The Daily Glow Co.** |
| 35.83–39.71 | **End card K7 \| K6.** Same 340×1209 crop on both stills (identical framing by construction), centred on the face, so eye lines match exactly. K7's hands, the lamp edge and the headboard edge are cropped out. White 4 px centre seam, synced 4% push-in | B2: "Comment photo and I'll send you what I use." (ends 39.7) | **YESTERDAY \| TODAY** (on the chests, whole card) · 35.83 **Same light. No filter.** · 37.08 **Comment PHOTO** (on "photo", 37.34) |
| 39.71–41.96 | **Studio shot** `564c68fa` (dark top band cropped off; 1024-px preview was enough at 900 px wide, so no download), on a matched mint gradient with feathered edges, 3% push-in | silence | **The Wrinkle Smooth Face Set** / **The Daily Glow Co.** (top) · **Comment PHOTO** (bottom) |

Every text box was asserted in code to sit within y 269–1248 px (below the top 14%, above the bottom 35%) and x 16–1064. Each element is ≤8 words. The brand line "The Wrinkle Smooth Face Set · The Daily Glow Co." is 9 words as one string, so it's set as two stacked elements (5 + 4 words). Spelling matches story.md/storyboard.md exactly. Per review note b there are **no burned speech captions**: the storyboard's overlays are the only text.

## Cover and cut decisions

1. **B2 pick-up glitch (owner decision 1):** B2 video runs only to t5.71 (frame 137, before the first bad frame ≈ t5.83). The K5 still covers it, and B2 video resumes at t7.42 (frame 178, after the glitch ends ≈ t7.3). No glitch frame is on screen (checked frame by frame around both joins). B2 audio is continuous except for the 0.42 s silent stretch removed under the still. Lip sync on both sides of the cover is exact: the A/V offset is identical before and after.
2. **Clip A brow-raise furrows (owner decision 2):** frame by frame, the deep furrows begin at A frame 93 (t3.875), slightly before 4.0. So the cut to K2 is at A t3.83 (frame 92), and no furrow frame is shown. The K2 cutaway covers A t3.83–11.79, which hides the whole 4.0–6.5 window.
3. **B1 furrows (t≈3.5–9.5): kept, flagged for the reviewer.** The storyboard has no cutaway in B1. Only the "Tretinoin…" and "Botox… of lesser strength?" text cards sit there, and they're on her torso, not her forehead. The grimace (out ≈16.4–19.0 s) shows a strong frown, and the brow raise (≈19.4–21.9 s) shows deep forehead furrows. Both are expression-driven and relax by ≈22 s, as noted at gate B.
4. **Dead-air trims (owner decision 3):**
   - Clip A's 0.5 s silent lead is trimmed, so her voice lands at 0.85 under the POV, as planned.
   - A's silent tail (12.3–14.04) is cut at 13.0 onto B1's matched K1 start.
   - B1 is cut at 12.625 (speech ends 12.25) into K3.
   - B2's 3 s reach silence: only the part that could be cut invisibly is cut (0.42 s under K5). The rest is her visible reach to the tray (≈2.5 s of silent action on camera, out 28.3–30.8). It stays, because cutting it would mean an on-camera jump cut, which the owner's rule excluded.
5. **Frame one:** the push-in starts at frame 0 and the timer dot blinks from frame 0. The hook text is fully on from frame 0. The flash pops at 1.21 s with the shutter click.
6. **"Same light. No filter." is used** because it's true: K6 TODAY is an edit of K7 YESTERDAY with identical morning window light and framing (stills-check, pair rebuild).
7. **Sound:** her Kling audio only, no music. SFX are synthesized in ffmpeg (sine beeps, noise-burst shutter, filtered-noise rustle), with no third-party audio.

## Known issues / for the reviewer

- **B1 expression furrows** are visible at ≈16.4–21.9 s (see 3 above). Fixing them would need a cutaway still or a B1 re-render, and neither is in the storyboard or budget.
- **Visible silent reach** in B2, out ≈28.3–30.8 s (2.5 s, no speech). The "Pressed in. Every night." text stays up over it.
- **K5 → B2 rejoin at 32.08 s:** the still's push lands close to B2 t7.42's framing, but the film's angle and her mouth differ slightly, so it reads as a small cut, not a freeze-unfreeze.
- **On the end card, TODAY's crop trims most of the held forehead band.** A sliver stays at the right edge. This was chosen to keep both faces centred and aligned, per the owner's instruction. If the owner wants the band visible, widen the crop: K7's lamp edge would then come back.
- K2: one friend still wears a small gold hoop (gate A note, owner accepted). It isn't retouched.
- "worst" vs "worse" (B1 t≈11): Whisper hears "worse" again on the final mix. The on-screen text reads **Worst when you wake up?** per story. Owner may want to listen at out ≈23.5 s.
- Checklist C items not verifiable in assembly: price/offer (not shown, TOF), link in bio and caption links, final file naming for posting. Not uploaded to Higgsfield (no `media_upload`; this run was local-only by instruction).
- Not committed.

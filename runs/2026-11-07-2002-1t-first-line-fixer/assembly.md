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

---

# v2 (re-assembly after video-review FAIL + owner notes)

v1 is kept as `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/assembly-1t/final-v1.mp4` (v1 scripts: `render_v1.py`, `audio_v1.sh`). `final.mp4` and `final-contact.png` in this folder are now v2.

- **Spec:** **39.00 s** (TOF 30–50 ✅), 1080×1920, 24 fps, H.264 + AAC 48 kHz stereo, 16.1 MB.
- **Loudness:** two-pass loudnorm. The true-peak ceiling was lowered to −2.0 dBTP so AAC encoding stays under −1.5. Final measurement: **−15.9 LUFS integrated, true peak −1.9 dBFS, LRA 4.6 LU**.
- **Whisper on the final mix:** all 88 words, in order.
- **Paid:** one owner-approved still. PROPS_TRIED_ITEMS `629dcc29-150b-4ba5-8276-aceae69d0b62` (nano_banana_2 1k 1:1, count 1): preflight 1.5, actual **1.5** (balance 1071.5 → 1070). `actual_total` is now **130.0 / 135**.

## What changed

| Fix | v1 | v2 |
|---|---|---|
| 1 (reach, frozen face, stutters) | B2 silent reach on camera, then a K5 talking-face still under "So now I sleep in these", then rejoin to B2 | B2 plays to the end of "every night" (B2 t3.33). Hard cut to a **product insert**: B2's hold section (t9.0–11.2), cropped to x 600–1076 / y 400–1246 (film + hand only; her mouth is at x ≤ 560, out of frame), with a 6% push. Under it, **2.67 s of reach silence is cut** (B2 audio jumps 3.33 → 6.0) and "So now I sleep in these" plays. Then it cuts **straight to K4**, so B2 talking video never returns and no frozen face sits under speech. |
| 2 (dead air before "They hold") | 1.25 s pause | **0.71 s trimmed** at the insert → K4 cut (B2 audio 8.21 → 8.92), leaving a ≈0.54 s pause, hidden under non-face shots. |
| 3 (B1 grimace/furrows) | on camera 16.4–21.9 | Frame by frame, the frown starts at B1 t3.4 and the brow furrows last to ≈9.1, so the cover is **B1 t3.29–9.21 = out 15.67–21.58**. It's a **reprise of the FILTER \| ME split** (same split composite): it opens on the split, pushes into the ME side (frown line, eye crinkles) on "even Botox of lesser strength", then pans across the line to the smoothed FILTER side on "but I'm scared it'll look unnatural". Her B1 audio runs continuously underneath. Back on her at B1 t9.21; the forehead is at K1 depth from ≈9.25. |
| 4 (owner-approved) | TODAY = K6 as generated | TODAY = K6 + **35% of K7**, inside a feathered face ellipse. K7 was first aligned to K6 by search (+4 px y, +1 px x) so nothing ghosts. The frown and forehead lines read "softer, not erased", and pores are kept (`K6_TODAY_blend35.png` in the scratchpad). The shared end-card crop moved from x 180–520 to **x 210–550** (same 340 × 1209 box on both halves, so eye lines still match). The held band now shows at TODAY's right edge. K7's hands (y ≥ ~1225) and its lamp and headboard edge (x ≥ ~585) stay out of frame. |
| 5 (packshot CTA overlap) | box over the bottom crescents | Packshot recropped (dark band and stone removed), scaled to 740 px wide and placed at y 445. The crescents end at y ≈1120, and the "Comment PHOTO" box sits at y 1142–1242. |
| Owner: dark hand in "what she's tried" | backlit frame-right counting hand visible (B1 t≈1.3–3.3) | **Product chips:** white rounded cards (330×480, soft shadow) with each item cut from `629dcc29`. Paper white is normalised to pure white, and the syringe's printed "1ml" is blurred out, so no text or brand remains. Each chip pops in on its word (scale 0.55 → 1.06 → 1.0) at centre (907, 1075), covering the hand area (x ~800–1080, y ~820–1260): **Tretinoin** tube at 13.46 s, **Vitamin C** dropper at 14.38, **Peptides** jar at 15.13, through to the cut. The old "Tretinoin. Vitamin C. Peptides." card is dropped, because the chip labels carry those words. For "Botox" (16.13 s) the hand is already under the reprise, so the **syringe chip** (no label) pops at the top right of the reprise (centre 907, 560) until 18.33. "Botox… of lesser strength?" stays as the bottom card. |

## v2 timeline (out = output seconds; 24 fps frame boundaries)

| Out | Picture | Audio | Text / overlays |
|---|---|---|---|
| 0.00–1.50 | K2 POV push, timer dot, flash 1.21 | beeps 0.12/0.56, shutter 1.21; A from t0.5 | **Filtering your lines / out of every photo?** 0–3.0 |
| 1.50–3.33 | Clip A t2.0–3.83 | A | ↑ |
| 3.33–11.29 | K2 push → FILTER \| ME wipe 5.58 | A | FILTER / ME 5.58 · **It ages me more than I'd like.** 7.71 |
| 11.29–12.50 | Clip A t11.79–13.0 | A | **And it keeps getting worse.** 11.29–13.0 |
| 12.50–15.67 | Clip B1 t0.125–3.29 | B1 | chips: **Tretinoin** 13.46 · **Vitamin C** 14.38 · **Peptides** 15.13 |
| 15.67–21.58 | Split reprise (ME → FILTER pan) | B1 continues | syringe chip 16.13–18.33 · **Botox… of lesser strength?** 16.21–22.17 |
| 21.58–25.00 | Clip B1 t9.21–12.625 | B1 | **Worst when you wake up?** 22.17–25.0 |
| 25.00–27.29 | K3 sleep push | rustle 25.0; B2 t0 at 25.08 | **Nobody told me why.** 25.0 · **Pressed in. Every night.** 26.0 |
| 27.29–28.42 | Clip B2 t2.21–3.33 (end of "every night") | B2 | ↑ |
| 28.42–30.63 | Product insert (B2 hold crop, no face) | B2 t6.0–8.21: "So now I sleep in these." | **The Wrinkle Smooth Face Set** (top, y 320) 28.42–30.92 |
| 30.63–32.88 | K4 press-on push (silent picture) | B2 t8.92–11.17: "They hold my skin flat all night." | **Holds skin flat all night** + **The Daily Glow Co.** 30.92 |
| 32.88–36.75 | End card K7 \| K6-blend | B2 t11.17–15.04: "Comment photo and I'll send you what I use." | YESTERDAY \| TODAY · **Same light. No filter.** 32.88–34.13 · **Comment PHOTO** 34.13 ("photo" ≈34.4) |
| 36.75–39.00 | Packshot (recropped) | silence | **The Wrinkle Smooth Face Set** / **The Daily Glow Co.** · **Comment PHOTO** (y 1142–1242) |

All text boxes were again asserted inside y 269–1248, each is ≤8 words, and spelling is per story.md. Chip labels sit at y ≈ 863. Frame 0 has motion and the hook text fully on. No talking footage appears after K4 (patch on).

## Remaining known issues (v2)

- **The syringe chip is a different object type from the patch**, shown only as the persona's "Botox of lesser strength" reference, with no claim. It sits over a friend's face on the reprise for 2.2 s.
- **For a few frames before the Tretinoin chip lands (B1 t≈1.3–1.4, out ≈13.6), the rising hand passes through the lower right** (y > 1250, below the chip). It's brief and not raised yet.
- **The product insert is an upscaled crop (≈2.3×) of the Kling clip**, so it's slightly softer than the stills. A sliver of her ear/hair edge can show at the insert's top-left corner; her mouth never does.
- **The split reprise repeats the K2 still** for 5.9 s, which makes ≈14 s of the 39 s on this one still. The pan direction and framing differ from the first use.
- **TODAY blend:** the lines read softer, not erased. This is a code edit of an AI after-image, which is allowed under the owner's AI before/after rule. Post it with the platform's AI-content label (as the reviewer noted under claims).
- **"worst"/"worse":** small.en hears "worse" again on this mix. The on-screen text says "Worst".
- **Not uploaded to Higgsfield**, as instructed. Not committed.

---

# v3 (fast-paced re-cut, owner request "more fast-paced… cuts, images popping, sounds")

**0 credits.** No Higgsfield/ElevenLabs/Runway calls, no uploads, not committed. Built locally with ffmpeg, Python/PIL/numpy and whisper-cli (small.en). v2 is untouched: `final.mp4` here is still v2, and `assembly-1t/final-v2-PASS.mp4` is the fallback.

- **Final:** `final-v3.mp4` (13.1 MB) and `final-v3-contact.png` (4 fps, 12 per row, so row r, column c = (12r + c) × 0.25 s) in this folder.
- **Scripts:** `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/assembly-1t-v3/`. `edl.py` does the pause cut and voice track, `words.py` the word timings, `render3.py` the picture, captions, pop-ups and SFX cues, and `audio3.py` the speed, SFX synthesis, mix, loudnorm and mux.
- **Spec:** **27.00 s**, 1080×1920, **30 fps**, H.264 High yuv420p, AAC 48 kHz stereo 192k.
  - That's **below the TOF 30–50 s window**. The brief allowed it: the same 88 words, minus the pauses, at 1.08×.
- **Loudness:** two-pass loudnorm (I −16, TP −2.0, LRA 11; dynamic mode, as in v2). Measured on the final with ebur128: **−16.0 LUFS integrated, true peak −2.0 dBFS, LRA 3.4 LU**.
- **SFX level:** set 5 LU under the voice, so about **−21 LUFS** in the master.
- **Music:** none. I didn't build a code-generated bed, because a synth loop would likely sound cheap. SFX only.
- **Speech check:** Whisper on the final mix returns **all 88 words, in order** (it hears "worse" for "worst" again, as in v1). Speech runs 0.41–25.35 s, which is **3.5 spoken words/s**.

## What changed vs v2

1. **Pauses cut, and video cut with them.**
   - Speech islands come from a 10 ms RMS envelope: speech > −45 dB, edges extended while > −52 dB, so soft "f"/"s" tails are kept. Whisper's own word times have no gaps, so they can't place cuts.
   - Every gap over 0.15 s is cut to **0.06–0.105 s pre-speed (0.057–0.097 s in the final)**. Each cut sits on a 24 fps source-frame boundary, and the same cut is applied to audio and video, so lip sync is exact. Each audio join gets a 4 ms fade, and every join is in silence.
   - There's one deliberate **0.20 s beat** before the reveal ("…wake up?" → K3, "Nobody told me why.").
   - 13 pauses were removed: 42 s of clips → 27.75 s pre-speed.
2. **Speed 1.08×.**
   - Audio: `atempo=1.08` on the whole voice track, pitch preserved.
   - Video: rendered directly in output time at 30 fps, and each talking frame is the source frame under the same pre-speed instant, so sync holds. At this speed each 24 fps source frame shows for about 1.16 output frames.
   - **Why 1.08:** after the pause cut, speech sat at about 3.3 w/s, and 1.08 lands at 3.5 w/s. That's inside the research's natural 3–3.9 range and below the 1.10–1.15 smear zone.
   - I could not listen. I checked it with Whisper instead: the sped voice alone transcribes clean, 88/88. **The owner should listen.** A 1.0× build is one command (`python3 render3.py 1.0 && python3 audio3.py`, about 29 s long).
3. **Jump cuts and punch-ins.**
   - Talking shots alternate 100% ↔ 112–115% at each cut, anchored on her face.
   - Emphasis punches go to 128% over 4 frames on "lines", "fraud" and "worst".
   - The vitamin-C punch-in is anchored on the hand area, so the chip still hides the backlit counting hand.
   - Stills get a +5–8% push. "Me?" is a 5-frame snap zoom. K3 and the packshot open with a slam-out zoom.
4. **B-roll over the weak lip-sync words.** With a cover on, no talking footage shows.
   - "look smooth": K2 friends.
   - "by my eyes": K2 eye macro on the ME side.
   - "peptides": jar card.
   - "even Botox of lesser strength": syringe card.
   - "scared it'll look unnatural": the FILTER face in a card. This is the smoothed K2 crop, cut off above the laughing mouth.
   - "pressed": K3 crease macro.
   - "So now I sleep in these": product insert.
   - "They hold my skin flat all night" (patch on): K4.
   - "Comment photo…": YESTERDAY | TODAY.
   - The A furrow window (A t ≥ 3.875 to ≈6.5) and the B1 grimace/furrow window (t 3.29–9.21) are never on screen. Every talking source range used is listed in the shot list below.
5. **Word-by-word captions.**
   - Helvetica Neue Bold, 74 px (auto-shrinks to fit), white with a 7 px black stroke and soft shadow. The current word is in brand **Sunrise Orange #F08A2C**.
   - Hand-set 1–4 word phrase chunks, upper case, centred at y 1172. Every caption is asserted in code to sit inside y 269–1248 and x 16–1064.
   - During the chip shots, captions shift left (centre x 330) so they clear the chips. Spelling follows story.md ("Frown", "worst", "PHOTO").
   - **Hook:** the hook card "Filtering your lines / out of every photo?" serves as the caption for the first sentence. Its words light up orange as she says them (photo, filtering, lines), so there are no stacked captions on the hook.
6. **Cards merged or dropped** (captions now carry the speech):
   - Dropped because captions repeat them: "Botox… of lesser strength?", "Worst when you wake up?", "Pressed in. Every night." and "Holds skin flat all night".
   - Dropped to declutter: "It ages me more than I'd like." and "And it keeps getting worse." (unspoken lines). Chip labels too, since the captions name each item.
   - Kept: hook card · FILTER / ME · "Nobody told me why." (the silent beat) · "The Wrinkle Smooth Face Set" pill on the insert · YESTERDAY / TODAY · "Same light. No filter." · packshot brand lines · **CTA "Comment PHOTO"** (a comment-bubble sticker on the packshot; it's also spoken, and the caption highlights PHOTO on the end card).
7. **Pop-ups** scale in 25 → 110 → 100% over 6 frames. All are drawn in code or cut from our own assets:
   - Timer dot and flash.
   - Orange rings on the frown line, the forehead and the eye crinkle.
   - Sparkles on "filter".
   - Product chips, plus the big jar and syringe cards.
   - Orange "?" badge, grimace emoji, arrow on the crease, Face Set pill, green check, moon-and-z, comment bubble.
   - The gap between pops never exceeds ≈4 s.
   - **Bigger interrupts:** flash 0.33 · FILTER|ME wipe 4.28 · white flash 13.31 · K3 slam with record scratch 17.36 · end-card wipe-in 23.15. That's ≤ 9 s apart.
8. **SFX.** Synthesized in numpy, so no third-party audio: whoosh, pop, ding, click, timer beep, shutter, record scratch and riser. 30 cues, about one per visual event.
   - Every cue lands **0.12 s before** its word or cut. A pop that sat on the "F" of "Frown" and on "all night" made Whisper hear "Brown" and "almost", so those were moved or removed (see the production log).
9. **The 5 polish items from round 2:**
   - (a) Chip cut-outs are keyed off the paper with a border flood-fill, edge-feathered, and the card draws its own shadow. There's no photo-box seam. The tube uses a wide feathered fade, because keying white-on-white ate the tube, and it's enlarged.
   - (b) The syringe is now a full-screen card, not over a friend's face.
   - (c) The reprise silence is gone: the reprise is gone, and the pause is cut.
   - (d) The insert crop moved right (x 646–1076, was 600) and scales to 105%. There's no cheek/ear sliver; checked at full res.
   - (e) The end-card crop moved left (K6/K7 box x 150–490, was 210–550), so the held band's sliver is out of TODAY. Eye lines still match (same box on both).

## v3 shot list (output seconds)

| Out | Dur | Shot | Source / note |
|---|---|---|---|
| 0.00–0.88 | 0.88 | K2 POV push, timer dot, flash 0.33 | beeps, shutter; voice enters 0.41 |
| 0.88–1.61 | 0.73 | A talk 100% | A t1.91–2.70 |
| 1.61–2.58 | 0.97 | A talk 115%, punch 128% on "lines" | A t2.70–3.75 (before the 3.875 furrows) |
| 2.58–3.90 | 1.31 | K2 friends push | "My friends look smooth." |
| 3.90–4.28 | 0.39 | K2 snap zoom to her | "Me?" |
| 4.28–5.93 | 1.65 | FILTER \| ME wipe (8 frames) + rings | "Frown lines, forehead lines," |
| 5.93–7.18 | 1.24 | K2 ME-side eye macro + ring | "crinkling by my eyes." |
| 7.18–7.79 | 0.62 | A talk 100% + sparkles | A t10.71–11.37 |
| 7.79–8.72 | 0.93 | A talk 115%, punch on "fraud" | A t11.37–12.375 |
| 8.72–9.91 | 1.20 | B1 talk 100% + tube chip | B1 t0.33–1.63 |
| 9.91–10.60 | 0.69 | B1 talk 112% (hand-anchored) + vitamin C chip | B1 t1.83–2.58 |
| 10.60–11.32 | 0.72 | Jar card | "peptides," |
| 11.32–13.31 | 1.99 | Syringe card + "?" | "even Botox of lesser strength," |
| 13.31–15.01 | 1.70 | White flash → FILTER face card + grimace emoji | "but I'm scared it'll look unnatural." |
| 15.01–15.92 | 0.92 | B1 talk 100% | B1 t9.79–10.77 |
| 15.92–17.36 | 1.44 | B1 talk 115%, punch on "worst" | B1 t10.77–12.33 |
| 17.36–18.30 | 0.94 | K3 slam (flash + record scratch) + "Nobody told me why." | "A lot of them get" (after a 0.20 s beat) |
| 18.30–18.72 | 0.42 | K3 crease macro + arrow | "pressed" |
| 18.72–19.71 | 1.00 | B2 talk 112% | B2 t2.22–3.29 |
| 19.71–21.37 | 1.66 | Product insert (B2 hold t9.2+, film + hand) + Face Set pill | "So now I sleep in these." |
| 21.37–23.15 | 1.77 | K4 press-on push + check + moon | "They hold my skin flat all night." |
| 23.15–25.38 | 2.24 | End card K7 \| K6-blend35 (TODAY wipes in) | "Comment photo and I'll send you what I use." |
| 25.38–26.97 | 1.58 | Packshot + brand + Comment PHOTO bubble | room tone fades out |

**Shot stats:** 23 shots. **Average 1.17 s, max 2.24 s** (end card), min 0.39 s. Visual changes in the first 3 s land at 0.33 (flash), 0.88, 1.61 and 2.58.

**Self-QA:**
- ✅ No shot > 2.5 s.
- ✅ Largest inter-word gap on the final voice track is **0.22 s** (the planned beat); the next largest is 0.11 s.
- ✅ Whisper 88/88, in order.
- ✅ Every caption and card is asserted inside the safe zone. I looked at the full 4 fps contact sheet; nothing collides.
- ✅ −16.0 LUFS / −2.0 dBTP.

## Known issues (v3)

- **27.0 s is under TOF's 30 s minimum** (accepted in the brief).
- **1.08× wasn't auditioned by ear.** Whisper reads it cleanly, but the owner should listen. 1.0× would give ≈29 s and its stock 24 fps cadence.
- **30 fps from 24 fps sources:** talking frames repeat about every 6th frame (pulldown-style cadence). It's normal on phones, but v2 was native 24 fps.
- **K2 is still ≈27% of runtime** (7.2 s: POV, friends, Me, split, eye macro, FILTER card), down from 35%. The eye macro is a 2× upscale of the photo, so it's slightly soft. Her laughing photo face shows there, but it reads as the photo, not live speech.
- The tube chip is still pale-on-white by nature. A faint lighter square remains on the syringe barrel where "1ml" was blurred (visible on the big card only at full res).
- Dropped storyboard cards ("It ages me more than I'd like.", "And it keeps getting worse.") are no longer on screen. Restore one if the owner wants that line.
- "worst" vs "worse": Whisper hears "worse"; the caption says WORST, as in story.md.
- No music bed. Post with the platform's AI-content label (as in v2). Not uploaded, not committed.

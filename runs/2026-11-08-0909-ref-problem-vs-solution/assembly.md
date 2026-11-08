# Assembly: run 2026-11-08-0909 "The Problem / Vs… / The Solution" (v2)

Stage 7 producer, assembly. **0 credits** (PIL + numpy + ffmpeg only). The run total is unchanged at 45 of the 135 cap.
Scripts: `scratchpad/asm-trend/render.py` (picture) and `mux_qa.sh` → `qa.py` (mux + QA). The scratchpad is
`/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/`.

## Deliverables (mp4s are gitignored)
| File | What it is |
|---|---|
| `final.mp4` | **Post file.** 1080×1920, 30 fps, H.264, 452 frames = 15.067 s, plus a **silent** stereo AAC track (48 kHz, max −91 dB) so the apps accept it. The owner adds the trending sound on Instagram. |
| `problem-vs-solution-sleep_trend_v2_2026-11-08.mp4` | Named copy of `final.mp4` (byte-identical). It replaces the v1 copy, which I deleted. |
| `post-silent.mp4` | **Phone-sized post file:** H.264 High, CRF 20, 12.4 MB, silent stereo AAC, 15.067 s. |
| `preview-small.mp4` | **PREVIEW ONLY, NOT FOR POSTING.** Phone-sized song preview (ref audio), 12.7 MB. |
| `final-preview-with-ref-audio.mp4` | **PREVIEW ONLY, NOT FOR POSTING.** Our picture with ref.mp4's audio, so the owner and reviewer can check that the cuts land on the beat. Its metadata title says "PREVIEW ONLY … NOT FOR POSTING". |
| `final-contact.png` | Contact sheet at 4 fps. |
| `compare-contact.png` | Ref \| ours pairs at 2 fps. |
| `qa.json` | Raw QA numbers. |

## Shot list (cut times = the reference's)
| # | Out (s) | Source | Source in | Camera (code) |
|---|---|---|---|---|
| 1 | 0.000–3.267 | C1_PROBLEM `4a47ae5f` | 0.00–3.27 | zoom 1.03→1.045, light extra shake (0.45×) on the clip's own handheld move |
| 2 | 3.267–4.367 | S2_BOX + real box | still | push 1.06→1.12 (fast start), shake 1.0×, **punch 108% at 3.833** (the ref re-frames here) |
| 3 | 4.367–4.767 | S3_INSERT | still | v2: push 1.38→1.42 with the camera centre lowered, so the whole sheet sits above "Vs…" (the caption lands on his forearm); shake 0.8× |
| 4 | 4.767–5.200 | S4_BAND | still | v2: push 1.14→1.18 with the face lifted, so "Vs…" lands on her chin and collar (not her lip); the band and both hands stay in frame; shake 0.9× |
| 5 | 5.200–6.000 | S5_SET | still | push-out 1.11→1.05 with a downward drift (sinking back), shake 0.9× |
| 6 | 6.000–7.567 | C2_TUCK_DOZE `d259fbf8` | 0.00–1.57 | 1.07×, framed so "Vs…" sits on her collar, not her chin; **punch 108% at 6.700 and back at 7.167** (the ref's in-shot cuts) |
| 7 | 7.567–10.000 | C2_TUCK_DOZE | 2.60–5.03 | hard cut, punched in to 1.13× (same angle as the ref); his hand leaves at the start; she settles and her eyes close |
| 8 | 10.000–11.833 | C3_EXHALE `c0eee195` | 0.30–2.13 | 1.04→1.06, shake 0.45× |
| 9 | 11.833–13.600 | `S9_LOW_codecrop.png` | still | push 1.24→1.28, framed low so "The Solution" clears the forehead patch, shake 0.7× |
| 10 | 13.600–15.067 | S10_WIDE + real box | still | push-out 1.12→1.06 (sets it apart from shot 7), shake 0.7× |

Clips are mapped 24→30 fps by nearest frame. The parted lips in C2 and C3 are kept (owner-accepted).

## Overlays
- **Captions** (PNG overlays, one at a time) copy the reference, which I measured on ref.mp4 at 720×1280 and scaled ×1.5:
  - "The Problem 😭🛏️" 0–3.267 and "The Solution 🤤❤️" 10.0–end: cap height 44 px, centred, cap band centre at y=416 (21.7%), the same as the ref. Text plus emoji spans x 275–806 (the ref spans 268–826).
  - "Vs…" 3.267–10.0: centred at y=956 (49.8%), cap height 51 px. The ref draws "Vs…" about 17% larger than the other two captions.
  - Style: Avenir Next Demi Bold, white, a 1.6 px dark outline and a soft shadow. That's the closest local match to TikTok/IG "Classic".
  - Emoji are in colour: Apple Color Emoji at 160 px, scaled to 64 px.
  - Everything sits inside the safe area (y 368–455 and 900–993).
- **Real box, S2:**
  - `face-set-box-v1.png` is cut out with the hand-traced 2-T outline and warped onto the blank placeholder in two parts: the front face and the teal side, each with its own homography.
  - Light match: the box takes the placeholder's own colour and low-pass shading, gets a 0.7 px softening, and keeps the placeholder's original contact shadow on the duvet.
  - His fingertips are keyed (skin sat > 0.24, hue < 26°, finger zone only) and put back over the box, so the finger reads as in front of it.
  - The box covers no face and no patches.
- **Real box, S10:** the same method on the nightstand placeholder. It's lit from the lamp side, beside the glass, and nowhere near her face.

## v2 changes (video-review PASS, free polish)
1. Shot 3 re-framed: "Vs…" no longer covers the crescents.
2. Shot 4 re-framed: "Vs…" no longer covers her upper lip.
3. Shot 1, 0–1.8 s (fades out by 2.1 s): local contrast on luminance only, over the pillow-crease patch (her right cheek, frame-left, in a tracked soft ellipse).
   - Groove shadows are deepened ×1.1 and the ridges lifted a touch.
   - Chroma is not added: the patch's redness is trimmed 12%.
   - Checked at full res: they read as soft pressed sleep lines, with no red streaks and nothing that looks like an injury.

Fix 4 in the review (the milky crescents) needs credits, so I didn't do it.

## Grade
- **Shot 1 (morning):** cool. WB gains 0.965/1.0/1.045, exposure 1.03, saturation 0.92, a mild S-curve and a black lift of 4.
- **Shots 2–10 (one warm evening grade):** WB 1.045/1.0/0.885, exposure 0.93, contrast 0.16, amber shadows, a soft vignette (−16% at the corners) and a black lift of 6.
- **Hair (hue-limited, not full-frame):** the ginger drift in S2/S4/S5/C2/C3/S9/S10 is corrected to one honey-blonde.
  - Key: hue 6–44°, saturation > 0.42 (ramped), value < 0.64, inside a head ellipse for each source. Faces are excluded explicitly in C3 and S9.
  - Fix: saturation ×0.68, a slight golden shift, +7% lift. Skin, patches, the headboard and pillows are left out of the mask (checked on debug overlays).
- **Grain:** luma grain on every frame. The stills get about 2× the clips' level (the clips already carry codec noise), and the stills get a 0.5 px softening to match the clips' sharpness.
- **Handheld:** low-frequency sway (0.7–2.7 Hz, ≤ ~11 px peak, ±0.3° roll) plus a small 6–7 Hz tremor. Motion blur comes from 3 sub-frame samples per frame (a 180° shutter).

## QA (self)
| Check | Result |
|---|---|
| Duration vs ref.mp4 | 15.0667 s vs 15.0669 s: **−0.007 frame** (PASS, ±1 frame) |
| Format | 1080×1920, 30/1, 452 frames, AAC stereo, silent (PASS) |
| Cuts (scdet on final) | 3.267 · 4.367 · 4.767 · 5.2 · 6.0 · 7.567 (same-angle punch, found at threshold 3) · 10.0 · 11.833 · 13.6. All 9 wanted cuts land on the exact frame (PASS). The ref's extra in-shot re-frames at 3.833 and 6.7 are found too; 7.167 is a punch-out that scdet doesn't flag |
| Caption windows (pixel scan) | top band 0.000–3.267 and 10.000–15.067; mid band 3.267–10.000 (PASS) |
| Caption position vs ref (`compare-contact.png`) | same height and size, centred (PASS) |
| Box composites | real label, perspective and shading match; the fingertip is in front; nothing covers a face or the patches (PASS, full-res crops checked) |
| Caption over the subject | v2: shots 3 and 4 re-framed (the caption clears the sheet and her lip). Fixed in v1: "Vs…" sat on her mouth and smile-line patch in shot 7 (re-framed), and "The Solution" sat on the forehead patch in shot 9 (re-framed) |
| Hair | reads as the same honey/light-brown from shot 2 to shot 10. Shot 1 stays a cooler ash-brown under the morning grade |

**Known notes (not blocking):**
- Shot 10 is close to shot 7's angle (from the still), so the push-out sets it apart.
- The emoji are Apple's set, so the bed and drool faces look slightly different from the ref's.
- The preview's audio is the ref's, padded to the full 15.067 s.

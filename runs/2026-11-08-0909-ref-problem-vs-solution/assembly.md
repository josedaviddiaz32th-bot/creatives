# Assembly v3.2 (owner-ordered remake): run 2026-11-08-0909 "The Problem / Vs… / The Solution"

## v3.2 fixes (coordinator: no shot may read as a still; free)
- **Shot 6 (7.70–8.48), night 2:** now C2 1.40–2.40 at 1.28×. His hand draws the throw up; tight 1.5× crop on her and the hand; dim amber. It was a 1.97× window of her already asleep, at 1.2%.
- **Shot 7 (8.48–10.0), night 3:** now C2 2.40–3.92 at 1×. His hand leaves frame and her eyes close; mirrored, 1.3× crop; natural cool night. No C2 second is used twice: 0–1.40, then 1.40–2.40, then 2.40–3.92.
- **Shot 1a:** C_NIGHTS 0.00–1.55 at 2.1×. It ends before the 1.6 s head lift, and the hand slide is more visible.
- **Cuts and captions are unchanged.**

### Motion per shot
The metric is exposure-normalised mean |Δ| between frames: the first and last frame of each shot, after the flicker, on 270×480 luma with a 2 px blur. Grade ramps (the pre-dawn lift) don't count as motion. **No shot is under 5%.**
```
shot 1a   0.000- 0.733: first->last   6.2%  max pairwise   6.2%
shot 1b   0.733- 1.433: first->last   7.5%  max pairwise   6.9%
shot 2    1.433- 3.267: first->last  10.3%  max pairwise  10.6%
shot 3    3.267- 4.700: first->last   6.3%  max pairwise   6.9%
shot 4a   4.700- 5.700: first->last   7.7%  max pairwise   8.1%
shot 4b   5.700- 6.300: first->last   7.2%  max pairwise   7.2%
shot 5    6.300- 7.700: first->last   6.5%  max pairwise   6.5%
shot 6    7.700- 8.467: first->last   5.3%  max pairwise   5.2%
shot 7    8.467-10.000: first->last   5.0%  max pairwise   5.0%
shot 8   10.000-12.400: first->last   8.3%  max pairwise  10.0%
shot 9   12.400-15.067: first->last   7.5%  max pairwise   8.3%
```
QA after the re-render:
- −0.007 frame vs ref.
- All 10 planned cuts found.
- Caption bands 0–3.267 / 3.267–10.0 / 10.0–15.067.
- Contact sheet checked: hand motion is visible in shots 5–7, and "Vs…" sits on collars and necks.

All outputs are re-rendered: `final.mp4`, the v3 named copy, `post-silent.mp4`, `preview-small.mp4` (preview only) and both contact sheets.

---

# Assembly v3.1 (superseded by v3.2 above): run 2026-11-08-0909 "The Problem / Vs… / The Solution"

## v3.1 fixes (video-review "v3 review" FAIL on the medium check; free)
- **Shot 7 (8.48–10.0) is re-cut.** v3 used C2 3.78–4.92 at 0.75×, which read frozen (~2% pixel change).
  - Now: the unused C2 window 1.40–2.92 at **1×**. His hand finishes tucking the throw, leaves, and she settles and her eyes close.
  - Framing: mirrored, a 1.12× crop (wider than shot 6's 1.35×). "Vs…" is on her neck.
  - Grade: a natural cool night (WB 0.91/0.97/1.10, exposure 0.76, saturation 0.90), so skin stays natural with no banding.
  - Measured first→last change: **20.7%** (it was ~2%). I looked at the frames, and the motion is plain.
- **Shot 6 (7.70–8.48)** is now a 1.97× time-lapse of C2 2.96–4.50 (it was 1×). She's asleep, so motion stays low (1.2% first→last): a breathing beat under a flicker cut, not a held frame. No C2 second is used twice; C2 now covers 0–1.40, 1.40–2.92 and 2.96–4.50.
- **Shelf box.**
  - Shadows: a softer, wider contact shadow (12 px feather, lower opacity) and a fainter back-panel shadow.
  - Room light: brighter and a touch warmer on the side facing the vanity light, cooler away from it, 10% of the niche's ambient wrapped in, and sensor noise on the card; edges feathered 1.2 px.
- **Outputs re-rendered:** `final.mp4`, the v3 named copy, `post-silent.mp4` (11.1 MB), `preview-small.mp4` (11.4 MB, preview only) and both contact sheets.
- **QA re-run:** −0.007 frame vs ref; all 10 planned cuts found; caption bands 0–3.267 / 3.267–10.0 / 10.0–15.067.

---

# Assembly v3 (superseded by v3.1 above; details below still apply except shots 6–7)

**Status: CURRENT.** v1/v2 are kept below for history. **0 credits** (PIL + numpy + ffmpeg).
Scripts are in `scratchpad/asm-v3/`: `render_v3.py` (picture; it reuses the caption and box code in `asm-trend/render.py`),
then `mux_qa.sh` → `qa.py`.

**Medium: ALL VIDEO.** Every frame comes from a Kling clip. No still is on screen, and there's no code shake or Ken Burns. The only
code moves are static crops or punch-ins at cuts, speed changes and grades.

## Deliverables (mp4s are gitignored)
| File | What it is |
|---|---|
| `final.mp4` | **Post file:** 1080×1920, 30 fps, 452 frames = 15.067 s, H.264 CRF 16, silent stereo AAC (−91 dB). |
| `problem-vs-solution-sleep_trend_v3_2026-11-08.mp4` | Named copy of `final.mp4` (byte-identical). |
| `post-silent.mp4` | Phone-sized post file: CRF 20, 10.8 MB, silent stereo AAC. |
| `final-preview-with-ref-audio.mp4` / `preview-small.mp4` | **PREVIEW ONLY, NOT FOR POSTING.** Our picture with ref.mp4's song, for checking the cuts against the beat (preview-small is 11.1 MB). |
| `final-contact.png` (4 fps), `compare-contact.png` (ref \| ours, 2 fps), `qa.json` | QA. |

## Shot list (out time ← source)
| # | Out (s) | Source window | Speed | Frame / look |
|---|---|---|---|---|
| 1a | 0.000–0.733 | C_NIGHTS 0.00–1.30 | 1.77× (time-lapse; sub-frames averaged) | Night 1: warm lamp. Avoids the 1.6–2.0 head lift |
| 1b | 0.733–1.433 | C_NIGHTS 2.20–4.00 | 2.57× | Night 2: lamp off, cool blue, flicker at the cut; the last 0.3 s lifts to pale pre-dawn grey |
| 2 | 1.433–3.267 | C_BATH_GIVE 0.20–2.03 | 1× | Bathroom: 3 near-black frames, then the light snaps on (a hard switch). She studies and touches the sleep lines with a small frown. 1.06× crop so the vanity light bar sits above the caption |
| 3 | 3.267–4.700 | C_BATH_GIVE 3.55–4.98 | 1× | Punch-in to 1.42×: his hand with the five-piece sheet, her small smile. Her face is lifted so "Vs…" sits on her collar |
| 4a | 4.700–5.692 | C_APPLY 0.80–2.04 (src frames ≤ 49) | 1.25× | Evening: band on, pressing the crescents. 716×1284 upscaled (Lanczos + unsharp), 1.2× crop so "Vs…" sits on her neck |
| 4b | 5.692–6.300 | C_APPLY 2.07–2.83 (src frames ≥ 50) | 1.25× | Kling's own hard cut (between src frames 49 and 50) is used as our cut; wide shot, hands to her lap |
| 5 | 6.300–7.700 | C2_TUCK_DOZE 0.00–1.40 | 1× | Night 1 in patches: he tucks the throw (warm) |
| 6 | 7.700–8.480 | C2_TUCK_DOZE 2.98–3.76 | 1× | Night 2: tight 1.35× crop, dimmer deep-amber lamp, flicker cut |
| 7 | 8.480–10.000 | ~~C2_TUCK_DOZE 3.78–4.92 at 0.75×~~ → v3.1: C2 1.40–2.92 at 1× | (see v3.1) | Night 3: mirrored, 1.25× crop with the lamp out of frame, cool blue, pre-dawn lift in the last 0.3 s |
| 8 | 10.000–12.400 | C_AFTER 0.00–2.20 | 0.92× | Morning, same 1.06× framing as shot 2: smoother skin, fingertips over the cheek and forehead. Real box on the wall shelf |
| 9 | 12.400–15.067 | C_AFTER 2.20–4.45 | 0.84× | Punch-in to 1.15×: a small, real smile (ends before the 4.5 s smile-line peak); the box stays in frame |

Departures from storyboard v3 (with reasons):
- **Shot 6 uses C2 2.98–3.76, not C3 0–0.5.** C3 is a full-face close-up, and at "Vs…"'s fixed y=50% the caption would sit on her nose or patches whatever the crop.
- **No source second is shown twice.** C2 is used as 0–1.40, then 2.98–3.76, then 3.78–4.92, and C_AFTER splits at 2.20 with no overlap. The 0.37 s repeat is gone.
- **C_APPLY is two shots,** split on its internal cut.
- **C_AFTER uses 0–4.45 with mild slow-downs,** so the end lands on the clean 3.3–4.3 s smile and not the 4.5 s+ smile lines.

## Overlays
- **Captions:** identical to v1/v2 in look and size. "The Problem 😭🛏️" 0–3.267 and "The Solution 🤤❤️" 10.0–end sit at y≈416, on the dark wall at night or her hair line in the bathroom, with the light bar above. "Vs…" 3.267–10.0 sits at y≈956, on collars and necks. None of them covers a face, the patches or the sheet.
- **Real box** (`face-set-box-v1.png`, front face, 100×168 px) stands on the empty recessed wall shelf behind her at frame-right, shoulder height, in shots 8–9.
  - Tracking: niche-corner template tracking (±14 px).
  - Light: colour matched to the shelf's warm-grey ambient (sampled box ≈ 1.07× the niche back), with a top-to-bottom falloff and a 0.9 px softening to the background focus.
  - Shadows: a contact shadow on the shelf floor and a soft shadow on the back panel.
  - Her head never crosses it.

## Grade: different nights read as different nights
| Look | Shots | What it does |
|---|---|---|
| n1 | 1a | warm lamp |
| n2 | 1b | dark cool blue, lamp off |
| eve | 4, 5 | the v2 warm evening |
| n2p | 6 | dimmer deep amber |
| n3 | 7 | cool blue, no lamp |
| bath | 2, 3, 8, 9 | one neutral-cool morning vanity look |

- **Night changes:** every night change is a hard cut plus a 2-frame exposure flicker (+38%, then +14%). Both the 1b and 7 nights end on a pre-dawn lift.
- **One look for her:** her hair is evened out to one honey/light-brown in every clip. This is a hair-only key (warm hue, saturation > 0.40, value < 0.70) inside a head ellipse with the face excluded; I checked it on debug overlays.
- **Grain:** light grain on every frame (~1.6 luma sigma).

## QA
| Check | Result |
|---|---|
| Duration | 15.0667 s vs ref 15.0669 s (**−0.007 frame**) PASS |
| Format | 1080×1920, 30/1, 452 frames, stereo AAC silent PASS |
| Planned cuts (scdet 3) | 0.733 · 1.433 · 3.267 · 4.700 · 5.700 (= 5.692 rounded to the frame) · 6.300 · 7.700 · 8.467 (= 8.480 rounded to the frame) · 10.000 · 12.400: all found PASS. Extra hits are intentional: 1.533 (the light snaps on), 7.767 and 8.5–8.53 (flicker frames), 1.867 (her hand rising fast in the source). A stray dissolve frame at 5.733 (sub-frame averaging across Kling's cut) is fixed by clamping each shot to its own source frames |
| Captions (pixel scan) | top band 0.000–3.267 and 10.000–15.067; mid band 3.267–10.000 PASS |
| Medium | every shot is a clip; no stills, no code shake PASS |
| Reactions | small frown (2), small closed-lip smile (3), calm (4–7), small real smile (9). Nothing overacted PASS |
| Frozen look | every shot has live motion; the slowest is shot 7 at 0.75× of a sleeper breathing. Nothing reads as a freeze PASS |

### Cold-viewer test (`final-contact.png`, watched as a stranger)
- **1 s:** at night, a woman sleeps with her cheek and the skin beside her eye squashed into the pillow, nuzzling deeper; "The Problem 😭🛏️". *"Her face is smashed into the pillow, and that's the problem."*
- **3 s:** the bathroom light snaps on. Close to the "mirror", she frowns a little and touches the pressed-in lines at her outer eye and cheek. *"Sleeping like that leaves lines on her face."* Cause → effect is clear; they read as sleep folds, not marks.
- **5 s:** "Vs…". His hand gives her a sheet of clear face patches and she smiles a little; that night she presses them on in bed. *"He got her patches for it, and you wear them to sleep."*
- **10 s:** he tucks her in, then night after night (warm, amber, blue) she sleeps in the patches. *"She does it every night."*
- **15 s:** the same bathroom framing in the morning: smoother cheek and forehead, a small real smile, the Face Set box on the shelf behind her; "The Solution 🤤❤️". *"It worked, and that's the product."*

**Notes (not blocking):**
- The emoji are Apple's set.
- C_APPLY is upscaled from 716 px, so it's slightly softer than the pro clips at full size.
- Shot 3's punch-in crops her forehead for 1.4 s so the caption clears her face.
- Her under-eye pressing (4a) is quick but reads as applying patches.

---

# Assembly v2 (superseded): run 2026-11-08-0909 "The Problem / Vs… / The Solution"

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

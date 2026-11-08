# Storyboard v3 (owner fix, 2026-11-08): run 2026-11-08-0909, "The Problem / Vs… / The Solution"

**Status: CURRENT** (v2 kept below for history). Built from `story.md` v3. Read: `learning/owner-feedback.md`
(newest), lessons §0 (marketer / cold-viewer test, no exaggerated reactions, all-video), production log
(ref-problem-vs-solution lines 72–87), v2 stills/clips checks.

## Video type and audio source
Silent trend remake: **no speech, no voiceover, no music in our file**; every Kling clip `sound: off`; no
ElevenLabs job. **Medium: ALL VIDEO.** Every on-screen beat is a Kling 3.0 clip; stills are only start/end
frames. No still is shown on screen with code zoom/shake.

## Continuity (unchanged from v2, plus the bathroom)
- **Her:** 23, white American, honey light-brown shoulder-length hair in a claw clip off the forehead, small gold
  studs, light natural brows, unretouched skin with faint fine lines at the outer eye corners, oversized
  heather-grey crewneck with no lettering. Identity anchor: S1 `974e98b0` (morning) / S2 `873abce2` (evening).
- **Him:** only his light-skinned forearm with a few dark hairs, navy T-shirt sleeve, no watch or jewellery; his face never shown.
- **Bedroom:** as v2 (white duvet, light wooden headboard, fairy lights, nightstand + lamp frame-right, white blinds).
- **Bathroom (new):** small American apartment bathroom: white subway tile, white towel on a hook, edge of a
  white shower curtain, light-switch plate. Warm-white vanity light from just above the lens.
  **Camera = the mirror:** her phone is propped on the vanity shelf where the mirror would be; she looks
  straight into the lens as if into her mirror. **No mirror, no reflection, no second face in frame** (lessons:
  models break reflections). Shots 2–3 and 8–9 share this exact framing (before/after like-for-like).
- **Sleep lines (owner: nothing like an injury):** soft, shallow pressed grooves on her cheek on the frame-left
  side of the image (her right cheek) near the outer eye, joining the fine lines there, plus one soft horizontal
  forehead crease; skin colour, at most a faint natural flush. Never "red", never raised; no injury words in any
  prompt (platform filter, production log line 81).
- **Patches:** PATCHES block verbatim wherever visible. Clear, slightly frosted, tab DOWN. Shot 3: five pieces on
  the film in his hand. Shot 4: band → full set. Shots 5–7: full set, lips closed, no smile. Shots 8–9: none.
- **Box (rev 1):** the real `assets/packaging/face-set-box-v1.png` (`0f24791e…`) is composited in code, free, on the
  vanity counter corner at the bottom of the frame, frame-right, in shots 8–9 (C_AFTER). The camera-as-mirror
  framing is near-static, so the composite holds. It never covers her face or her frame-left hand path; the
  ST_BATH_BEFORE/AFTER prompts keep that counter corner clear and empty (no generated box). Add a soft contact
  shadow and match the vanity light; no model ever sees the box.
- **Caption bands (assembly):** top band (y≈22%) for "The Problem"/"The Solution"; "Vs…" at y≈50%. Bathroom
  stills put the top of her head at ~30% from the top so the top band sits on tile. For "Vs…" in shot 3 and the
  bedroom shots, re-frame per shot so the band lands on collar/throw/wall (production log 85–86).

## Shot → clip plan (total 15.067 s)

| # | Out time (s) | Dur | Source clip | Source in → out | New / reuse | Code (free) |
|---|---|---|---|---|---|---|
| 1a | 0.000–0.733 | 0.733 | **C_NIGHTS** (pro 4 s, start ST_NIGHT) | 0.00–2.00 at 2.73× | NEW | Night 1: warm lamp grade; speed-up in code only; end on ≥0.25 s of her still, squashed face |
| 1b | 0.733–1.433 | 0.700 | **C_NIGHTS** | 2.00–4.00 at 2.86× | NEW (same clip) | Night 2: hard cut + 2-frame exposure flicker; lamp-off cool blue grade; last 0.3 s a cool pre-dawn grade lift (blue → pale grey), then shot 2's 0.1 s black and the light snap |
| 2 | 1.433–3.267 | 1.834 | **C_BATH_GIVE** (pro 5 s, ST_BATH_BEFORE → ST_BATH_GIVE) | 0.10 s black + 0.30–2.03 | NEW | Light switch: 3 frames near-black then a hard snap to full exposure (a real switch, not a fade) |
| 3 | 3.267–4.700 | 1.433 | **C_BATH_GIVE** | 3.55–4.98 | NEW (same clip) | Hard cut with 108% punch at 3.267 (the ref cuts here) |
| 4 | 4.700–6.300 | 1.600 | **C_APPLY** (std 3 s, S4_BAND → S5_SET) | 0.80–2.80 at 1.25× | NEW | Evening warm grade; hair warmth/saturation pulled down |
| 5 | 6.300–7.700 | 1.400 | **C2_TUCK_DOZE** `d259fbf8` | 0.00–1.40 | REUSE (free) | Night 1 warm grade |
| 6 | 7.700–8.480 | 0.780 | **C3_EXHALE** `c0eee195` | 0.00–0.50 at 0.64× (lips part from ≈0.55 s) | REUSE (free) | Night 2: hard cut + 2-frame exposure flicker; dimmer lamp grade |
| 7 | 8.480–10.000 | 1.520 | **C2_TUCK_DOZE** | 3.40–4.92 (closed lips) | REUSE (free) | Night 3: **horizontally flipped**, 1.25× crop that excludes the lamp, cool night grade, flicker cut, pre-dawn lift in the last 0.3 s |
| 8 | 10.000–12.400 | 2.400 | **C_AFTER** (pro 5 s, start ST_BATH_AFTER) | 0.00–2.40 | NEW | Same bathroom grade as shot 2; real box composited on the counter corner, bottom frame-right |
| 9 | 12.400–15.067 | 2.667 | **C_AFTER** | 2.40–5.00 at 0.975× | NEW (same clip) | Hard cut, 112% punch-in on the smile (no repeated motion); box stays in frame if the punch-in allows, else shot 8 only |

Longest shot 2.667 s (ref has 2.43 s shots); 9 cuts in 15.07 s (ref: 10). Night changes are carried by real cuts
and grades between real clips, never by a still.
C1 (the overacted cry) is **not used**. S2/S3/S9/S10 stills are **not shown** (all-video rule).

## Keyframe chain (state lists)

| Still | Status | Built from | State |
|---|---|---|---|
| **ST_NIGHT** | NEW (2 cr) | edit of S2 `873abce2` (identity + bedroom) | Night, lamp on low. Close side view from a phone propped on the nightstand at mattress height, locked. She lies on her right side facing the lens, face pressed deep into the white pillow: cheek and skin beside the lower eye folded, edge of the forehead in the pillowcase. Eyes closed, lips closed. One hand on the pillow near her face. Bare face, no box. |
| **ST_BATH_BEFORE** | NEW (2 cr) | edit of S1 `974e98b0` (identity + her sleep lines) | Morning bathroom, camera = mirror. Close-up head to collarbones, face ~55% of width, top of head at ~30%. Leaning slightly in, eyes to lens, a small puzzled look, lips closed. Soft sleep lines (frame-left cheek near outer eye + one forehead crease). No hands in frame. |
| **ST_BATH_GIVE** | NEW (2 cr) | edit of ST_BATH_BEFORE + sheet `564c68fa` | Same frame. His hand (navy sleeve) enters at frame-right at shoulder height holding the clear film with exactly five pieces (band on top, tab DOWN, four crescents). She has turned her head slightly to it, brows lifted, a small closed-lip smile (bare face). Her frame-right hand's fingertips touch the film's bottom edge. Exactly two hands (hers, his). Sleep lines unchanged. |
| **ST_BATH_AFTER** | NEW (2 cr) | single-image edit of ST_BATH_BEFORE | Identical frame, a later morning, patches off: the sleep creases gone, the fine lines at the outer eyes and forehead visibly softer and shallower, same pores and texture (not airbrushed); calm, open expression, lips closed. No hands. |
| S4_BAND `2d9dbe01` | REUSE | v2 | start of C_APPLY |
| S5_SET `d65f6fb0` | REUSE | v2 | end of C_APPLY |

## Clips
- **C_NIGHTS — pro 4 s (rev 1), start ST_NIGHT, sound off.** Locked camera, real-time motion (speed-up in code). She stays
  on her side the whole time: 0–1 nuzzles her face deeper into the pillow, cheek and skin beside the eye folding;
  1–2 pulls the pillow tighter; 2–3 presses her face further in, forehead edge sinking into the pillowcase; 3–4
  still, face squashed in. Eyes closed, lips closed. Light changes are done in code.
- **C_BATH_GIVE — pro 5 s (rev 1), ST_BATH_BEFORE → ST_BATH_GIVE, sound off.** 0–0.6 she leans in; 0.6–2.2 her frame-left
  index fingertip touches the sleep lines at her outer eye/cheek (same side as the lines), then the forehead line;
  a small frown, shoulders drop once, lips pressed softly together; 2.2–2.6 hand down; 2.6–5 his hand enters frame-right with the
  sheet, she turns, brows lift, small smile, frame-right fingertips touch the film. Lines unchanged throughout.
- **C_APPLY — std 3 s, S4_BAND → S5_SET, sound off.** 0–0.8 palms press the band flat and slide off her temples;
  0.8–2.2 fingertips press along under each eye and along each smile line; 2.2–3 hands to her lap, she sinks back.
  Lips closed, mouth corners level. PATCHES block in the prompt (rev 1).
- **C_AFTER — pro 5 s (rev 1), start ST_BATH_AFTER, sound off.** 0–0.8 she leans in; 0.8–2.6 her frame-left fingertip glides
  over her outer eye/cheek, then across her forehead, brows lift a little; 2.6–5 a small, real, happy smile, she
  turns her cheek to the light, then glances toward frame-right. No lines appear on the cheek; no laughing.

## Gates
1. Prompt-review (6b) on v3 jobs. 2. Generate the 4 stills → gate A (checklist A + cold-viewer look: do the
bathroom lines read as sleep folds, not marks?) → owner glance at ST_BATH_BEFORE vs ST_BATH_AFTER. 3. Rewrite each
clip's first/last beat from the approved stills (production log 82), then the 4 clips → gate B (reaction check:
nothing exaggerated; medium check: all video).

## v3 revision 1 (2026-11-08; 0 credits)
Applied story-review "v3 review" fixes 1–5 and 7, and prompt-review "v3 pass 1" replacement text word for word
(in `prompts.json`): C_NIGHTS keeps her on her side, real-time motion (speed in code), pro; ST_BATH_BEFORE angled
vanity light, pillowcase-seam creases, "only person in the frame" (S1 has his jaw), clear counter corner; C_BATH_GIVE
no nose-sigh, pro; C_APPLY gets the PATCHES block, std; C_AFTER pro. Montage re-cut (C3 0–0.5 s; C2 tail flipped and
cropped to hide the lamp). Shots 8/9 split at 2.40 with no overlap. Optional third-night clip dropped. Brand: real box
as a free code composite on the counter in shots 8–9 (main-session decision). Fix 6 (brand question) is answered by
that composite; the posting caption still names The Daily Glow Co. and the product.
Budget: stills 8 + C_NIGHTS 7 + C_BATH_GIVE 8.75 + C_APPLY 4.5 + C_AFTER 8.75 = **37.0** (39.0 with one still fix) ≤ 40.

---

# v2 (superseded by v3 above; kept for history)

# Storyboard: run 2026-11-08-0909, "The Problem / Vs… / The Solution" (P3, trend remake)

Stage 5 (storyboarder). Read first: `learning/owner-feedback.md`, `CLAUDE.md`, `pipeline/config.yaml`,
`docs/lessons-learned.md` (in full), `learning/production-log.md`, `brief.md` (owner section wins), `format.md`,
`story.md` v2 (APPROVED), `story-review.md` (round-2 notes applied), reference sheet `scratchpad/ref-car/sheet.jpg`.

## Video type and audio source
**Silent trend remake. No speech, no voiceover, no music in our file.** The owner adds the trending sound in the app.
Every Kling clip is `sound: off`, and there is no ElevenLabs job. Nobody talks. Her bare-face cry in shot 1 may open
her mouth with no words (the owner accepted this on Nov 8). In every shot with patches on, her lips stay closed and
she doesn't smile.

## Continuity sheet
- **Her (every shot):** 23, white American, honey light-brown shoulder-length hair **in a claw clip, off the forehead
  in every shot** (in shot 1 the clip is loose and slipping, with sleepy flyaways), small gold studs, light natural
  brows, unretouched skin with faint fine lines, an oversized heather-grey crewneck with no lettering. Skin is dry and
  matte in the patch shots.
  *Deviation from story.md (shot 1 "hair loose"):* the clip stays in for shot 1 because the forehead creases have to
  show, the STYLE block's hair line applies, and it keeps her identical across shots.
- **Him:** about 25. Shot 1: only the soft, out-of-focus edge of his stubbled jaw at the frame-left edge. Shots 2, 3
  and 6: the same navy T-shirt sleeve and light-skinned forearm, no watch or jewellery. His face is never shown.
- **Setting:** a US apartment bedroom with a queen bed, white duvet and pillows, a light wooden headboard, fairy
  lights above it, a wooden nightstand on the **frame-right side** (lamp and glass of water), white blinds and a
  switch plate. No mirror.
- **Light:** shot 1 is raking morning daylight through the blinds from frame-right. Shots 2–10 are evening, lit by
  the warm lamp (frame-right) and the fairy lights. The lamp dims slightly from shot 7.
- **Look (match the reference):** couple-POV phone footage, handheld and slightly imperfect, natural light, a little
  grain, never steady-cam or ad polish. The top fifth of every frame is kept plain for the caption (≈22% from top).
- **Patches:** none in shots 1–2. Shot 3: five pieces on the film in his hand. Shot 4: the forehead band only, tab
  DOWN. Shots 5–10: band + 4 crescents, lips uncovered, clear and never white.
- **Box:** the real `assets/packaging/face-set-box-v1.png` (job `0f24791e…`) is composited in code over a **blank
  placeholder box** in S2 (on the duvet) and S10 (on the nightstand). No model ever sees or draws the real box.
- **Voice description:** n/a (no speech).

## Captions (code, never a model)
One centred line at a time, white with a thin dark outline (TikTok Classic), baseline ≈22% from the top, cap height
≈4% of frame height: **"The Problem 😭🛏️"** 0–3.27 · **"Vs…"** 3.27–10.00 · **"The Solution 🤤❤️"** 10.00–15.07. Emoji
come from a colour emoji font (Apple Color Emoji / Noto Color Emoji) or Twemoji PNGs.

## Shot → asset plan (cut times = the reference's exactly; total 15.07 s)

| # | Time (s) | Dur | Asset | How it's made | Code motion / trim |
|---|---|---|---|---|---|
| 1 | 0.00–3.27 | 3.27 | **C1** (Kling 4 s, start S1) | Lift → trace a crease → wordless cry + flop | Use t 0–3.27 |
| 2 | 3.27–4.37 | 1.10 | **S2** still | His hand lets go of the blank box; the real box is composited over it with a matched shadow | Push-in 100→106% + handheld shake |
| 3 | 4.37–4.77 | 0.40 | **S3** still | Backlit film with 5 pieces in his fingers, no box | Fast push 100→104% + shake |
| 4 | 4.77–5.20 | 0.43 | **S4** still | Palms sliding off her temples, the whole band visible, tab down | Push 102→106% + shake |
| 5 | 5.20–6.00 | 0.80 | **S5** still | Full set, sunk back against the pillows | Push-out 106→100% plus a small downward drift (reads as sinking back) + shake |
| 6 | 6.00–7.57 | 1.57 | **C2** (Kling 5 s, S6 → S7) | He pulls the throw up and tucks her in | Use t 0–1.57 |
| 7 | 7.57–10.00 | 2.43 | **C2** (same clip) | She nestles in, eyes close | Use t ≈2.30–4.73, hard cut with a 106% punch-in (the reference has a cut at the same angle) |
| 8 | 10.00–11.83 | 1.83 | **C3** (Kling 3 s, start S8) | Close-up asleep, one contented exhale, shoulders melt | Use t ≈0.3–2.13 |
| 9 | 11.83–13.60 | 1.77 | **S9** still | Low side angle, face up, fairy-light bokeh, nothing touching her face | Slow push 100→105% + gentle shake |
| 10 | 13.60–15.07 | 1.47 | **S10** still | High wide shot of the whole bed; the real box is composited on the nightstand | Slow push 100→104% + gentle shake |

**Why stills for 2, 3, 4, 5, 9 and 10:** each of these shots is ≤1.8 s, Kling's minimum clip is 3 s, and the
reference holds these shots almost static (a set-down, an insert, a settle, sleeping angles). Code shake plus a push
keeps the handheld feel at 0 credits. Shot 2 uses the review's fallback (a still with the box composited), because
tracking a composite onto a moving hand is risky. Shots 6 and 7 share one camera angle in the reference, so one clip
with an end frame covers both.
**Handheld shake spec (code):** 0.6–1.2% translation and ±0.3° roll as low-frequency noise (≈1.5–3 Hz), with
in-clip motion kept for C1–C3. Add slight grain to stills so they match the clips.

## Keyframe chain (state lists)

| Still | Built from | State |
|---|---|---|
| **S1_PROBLEM** | fresh, text only (her identity anchor) | Morning; she's propped up on her forearm (frame-left) and turns her face to the lens. Deep red creases on the **frame-right cheek** and the forehead, lit by raking daylight from frame-right. Her free hand is on the pillow (frame-right). His soft jaw is at the frame-left edge. Bare face. 2 hands. |
| **S2_BOX** | edit of S1 (identity only; new scene) | Evening; she sits against the headboard, hair in the clip, bare face, **no creases**. His hand (navy sleeve) is letting go of the blank box on the duvet (frame-right, lower third). 3 hands. |
| **S3_INSERT** | S2 (his sleeve, the lamp) + sheet 564c68fa | Close insert: one hand holds the clear film up against the lamp; exactly 5 pieces (band on top, tab down, 4 crescents in 2 rows). No box, no face. 1 hand. |
| **S4_BAND** | S2 + sheet | Head and shoulders; her palms slide outward at her temples; **band only**, tab down, whole band visible; bare under the eyes and on the smile lines. 2 hands. |
| **S5_SET** | S2 + sheet (from the bare frame, not from S4) | **Full set**, sunk back against the pillows, hands in her lap, sleepy, lips closed. 2 hands. Patch anchor. |
| **S6_TUCK** | S5 + S2 (sleeve only) + sheet | Lying back, head on the pillow; the throw is at her waist, her hands on her stomach; his hand grips the throw's edge (frame-right). 3 hands. |
| **S7_DOZE** | S6 + sheet | The throw is up to her shoulders, tucked at frame-right; no hands; eyes closed; same framing as S6. |
| **S8_CLOSE** | S7 + sheet (built from the wider frame) | Face close-up, on her back, throw to her chin, all 5 patches with visible edges; no hands. |
| **S9_LOW** | S7 + sheet | Low side angle, face up toward the lens, throw to her chin, bokeh; no hands. |
| **S10_WIDE** | S7 + sheet | High wide shot from the foot corner; her face ~15% of the frame width; nightstand on frame-right with the lamp, a glass and the blank box; no hands. |

## Clips
- **C1: 4 s, shot 1, start S1, no speech.** Handheld sway. 0–0.7: she lifts toward the lens, the creases are visible.
  0.7–1.9: her fingertip (frame-right hand) traces the longest crease on the frame-right cheek; her eyes widen.
  1.9–4: a wordless whiny cry, then she flops back. The creases stay deep and red; his jaw stays soft at frame-left.
- **C2: 5 s, shots 6+7, S6 → S7, no speech, lips closed.** 0–1.5: his hand pulls the throw up to her shoulders and
  tucks it. 1.5–2.2: his hand leaves frame-right. 2.2–5: she nestles in and her eyes close. The patches don't move.
- **C3: 3 s, shot 8, start S8, no speech, lips closed.** One slow exhale through her nose; her shoulders melt. The
  patches don't move. No hands.

## Asset plan (reuse check, lessons §7 → Elements → generation history → owner files)

| Need | Reused asset | New? Why |
|---|---|---|
| Her (23, P3) | none: §7 has 25 (East Asian), 35, 40–50 and 45+ women; no saved P3 character in `runs/history.json` | **New** S1 (P3's first face; save it as an Element after approval, free) |
| Him | none | Only a jaw and a sleeve, made inside S1/S2 |
| Patch shape / placement | Forehead Element `6375c707…`, Eye-patches Element `9d766c06…` (prompt text only), Face Set flat lay `564c68fa…` (medias) | Reused, no cost |
| Branded box | `0f24791e…` / `face-set-box-v1.png` | Reused, composited in code (shots 2 and 10) |
| Hero shot `39637096…` | not used (no end card; the reference has none) | — |
| Bedroom / tuck / sleep frames | 2-T's are Pixar and show another woman; 1-T's show the P1 face | **New** S2–S10, all chained from S1 |
| Clips | none fit (new person, photoreal) | **New** C1–C3 |

## Gates
1. Generate S1 → S10 in chain order, then run checklist A on each (patches clear, tab down, the right pieces per
   shot, crescent shape, lips closed with patches on, no smile, no text or lettering, a blank placeholder box only,
   hand counts, same face).
2. Prompt-review the stills, then **the owner approves all ten stills** before any clip (owner rule: a still for
   every shot).
3. Rewrite each clip's first and last beat from the approved stills, then run C1–C3.

## Revision 1 (2026-11-08, prompt-review pass 1: FIX, wording only)
Applied all fixes verbatim in `prompts.json` (revision 1). S5–S10 now say "mouth neutral, the corners of her mouth
not raised". C2/C3 say "No smile: the corners of her mouth stay level", and C3's exhale is "relaxed". S4 drops the
crescent Element (band only). S9's camera is now ~40 cm above the pillow, tilted down; her face points up and
neither cheek touches the pillow. S2/S10 no longer say "real product box". S2: his hand pulls back, motion-blurred,
with the box and her face sharp. In assembly the shot-2 push runs slightly faster at the start, and the clip
cut-ins get the same shake amplitude as the stills. Cost is unchanged (41 + 15 reserve = 56).

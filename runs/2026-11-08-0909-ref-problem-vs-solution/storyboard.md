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

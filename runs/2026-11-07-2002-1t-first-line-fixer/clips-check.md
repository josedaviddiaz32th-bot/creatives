# Clips check (gate B): 2026-11-07-2002-1t-first-line-fixer

Producer, Stage B (clips) only, no assembly. Owner rules: one generation per shot (count 1, never resubmitted), no clip redo without the owner, stop at the first clip that fails checklist B. Budget cap 135 (owner accepted reserve draw); actual_total before Stage B: 23.5.

Checks were run locally on each downloaded mp4: ffprobe (duration, size, audio stream), volumedetect, Whisper small.en transcript, frames at 2 fps plus the first and last frame, a K-still vs first/last side-by-side, and face and hands/tray crops at key times.

Local clips and contact sheets: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/clips-1t/` (`<CLIP>.mp4`, `<CLIP>_contact.png` = 2 fps, 6 per row, row 1 = t 0–2.5s, `frames_<CLIP>/`).

---

## CLIP_A — PASS ✅ (one note)

- Job / generation ID: **`977b4161-ff61-41ca-9805-6ead5d784bf2`**
- URL: https://d8j0ntlcm91z4.cloudfront.net/user_3K4XoW4Rud6flkLxNibt0IrMyg5/hf_20261108_025932_977b4161-ff61-41ca-9805-6ead5d784bf2.mp4
- Credits: **35** (preflight 35; balance 1176.5 → 1141.5). Count 1, submitted once.
- File: 14.04 s, 1076×1924 (9:16 within 0.6%), 24 fps, AAC stereo 44.1 kHz, mean −24.8 dB / peak −3.6 dB.

**Transcript diff** (Whisper small.en vs prompts.json):

| Expected | Heard | Match |
|---|---|---|
| Can't take a group photo without filtering your lines? | 0.00–4.26 Can't take a group photo without filtering your lines? | ✅ |
| My friends look smooth. | 4.26–6.22 My friends look smooth. | ✅ |
| Me? | 6.22–7.22 Me? | ✅ |
| Frown lines, forehead lines, crinkling by my eyes. | 7.22–10.72 Frown lines, forehead lines, crinkling by my eyes? | ✅ (rising intonation only) |
| I filter it, feel like a fraud. | 10.72–12.32 I filter it feel like a fraud. | ✅ |

All 29 words, in order, nothing added. Speech ends at ~12.3 s; lips closed from ~12.5 s to the end.

| Checklist B item | Result | Notes |
|---|---|---|
| Same woman, hair, earrings, T-shirt every frame | ✅ | Same face as K1; hair slicked back, nothing on the forehead; gold huggies; sage T-shirt; oat duvet. |
| Bare face, no patches on her | ✅ | |
| Talking clip: words match exactly; lips track speech | ✅ | Mouth moves with the words; closed in the silent tail. |
| Exactly two hands, five fingers; no hand crosses the face | ✅ | Phone hand frame-left at chest height the whole clip; free hand rests on the duvet frame-right the whole clip (5 fingers checked at t 0, 3, 7, 10, 13.75). |
| Tray state: 5 pieces (band + 4 crescents), unchanged | ✅ | Checked at t 0, 3, 7, 10, 13.75. |
| No morphing, melting, extra objects, other people | ✅ | Lamp, nightstand, headboard steady; camera locked. |
| Wrinkles don't change mid-clip; skin not airbrushed | ✅ ⚠️ | Skin stays unretouched with pores. **Note:** when she raises her brows (t ≈ 4.0–6.5 s, peak 4.0–5.5 s) Kling draws 4–5 deep horizontal forehead furrows, much stronger than K1's faint lines; they relax back to K1's depth by ~7 s. This is expression-driven (eyebrows up, as prompted), not drift, so it's not a failure, but it's on screen for t 4.0–4.8 in the planned cut (clip A on screen t 0.7–4.8). Assembly option: cut to the K2 cutaway at t 4.0 instead of 4.8 if the owner finds it exaggerated. |
| Starts and ends on the approved frame (K1) | ✅ | First and last frames match K1 `91d6abc0` (framing, pose, tray, lamp). |
| 9:16, readable at phone size | ✅ | |

---

## CLIP_B1 — PASS ✅ (two notes)

- Job / generation ID: **`33261546-7002-4fa8-bd30-14e243311494`**
- URL: https://d8j0ntlcm91z4.cloudfront.net/user_3K4XoW4Rud6flkLxNibt0IrMyg5/hf_20261108_030427_33261546-7002-4fa8-bd30-14e243311494.mp4
- Credits: **32.5** (preflight 32.5; balance 1141.5 → 1109). Count 1, submitted once.
- File: 13.04 s, 1076×1924 (9:16), 24 fps, AAC stereo 44.1 kHz, mean −24.1 dB / peak −6.1 dB.

**Transcript diff** (Whisper small.en full clip; small multilingual as a second opinion):

| Expected | Heard | Match |
|---|---|---|
| I've researched tretinoin, vitamin C, peptides, even Botox of lesser strength. | 0.0–6.0 I've researched Tretinoin, Vitamin C, Peptides, even Botox of lesser strength, | ✅ (tretinoin sounds as tret-ih-noyn) |
| But I'm scared it'll look unnatural. | 6.0–9.0 but I'm scared it'll look unnatural. | ✅ |
| Ever notice your lines look worst right when you wake up? | 9.0–13.0 Ever notice your lines look **worse** right when you wake up? | ✅ ⚠️ see note |

All 28 words, in order, nothing added. **Note on "worst":** small.en heard "worse"; the multilingual model on the isolated tail (t 9–13) heard "worst right". The waveform at t ≈ 11.21–11.33 s shows the /s/ followed by a ~30 ms stop closure (the elided /t/) before "right", which is normal connected speech. I'm treating it as a match; the burned caption will read "worst". The owner may want to listen to t 10.9–11.5.

| Checklist B item | Result | Notes |
|---|---|---|
| Same woman, hair, earrings, T-shirt every frame | ✅ | |
| Bare face, no patches on her | ✅ | |
| Talking clip: words match; lips track speech | ✅ | Mouth closed in the last ~0.7 s. |
| Exactly two hands, five fingers; no hand crosses the face | ✅ | The counting hand is the free frame-right hand (lifts t ≈ 1.3 s, counts at chest/shoulder height t 1.5–6, back on the duvet by ~7 s). Zoomed at t 2.5, 3.5, 4.5, 5.5: extended fingers plus thumb pressing the folded ones, 5 digits, no extras. It never goes near her face. Phone hand frame-left, still. Normal motion blur on the lowering hand at t ≈ 6.5. |
| Tray state: 5 pieces, unchanged | ✅ | Band + 4 crescents at all checked times. |
| No morphing, melting, extra objects, other people | ✅ | |
| Wrinkles don't change mid-clip; skin not airbrushed | ✅ ⚠️ | Same as clip A: the grimace (t ≈ 3.5–6) adds a strong frown and the brow raise on the question (t ≈ 7–9.5) adds deep forehead furrows; both relax to K1's depth by ~10 s. Expression-driven, not drift. Skin unretouched. |
| Starts and ends on the approved frame (K1) | ✅ | First and last frames match K1. A's last frame = B1's first frame, so the A→B1 join at 0:14.8 is clean. |
| 9:16, readable at phone size | ✅ | |

---

## CLIP_B2 — FAIL ❌ (pick-up transition, t ≈ 5.8–7.2 s). Stage B stopped for the owner.

- Job / generation ID: **`17a139b3-1bfd-4313-a0cb-792a8dc3057f`**
- URL: https://d8j0ntlcm91z4.cloudfront.net/user_3K4XoW4Rud6flkLxNibt0IrMyg5/hf_20261108_031040_17a139b3-1bfd-4313-a0cb-792a8dc3057f.mp4
- Credits: **37.5** (preflight 37.5; balance 1109 → 1071.5). Count 1, submitted once.
- File: 15.04 s, 1076×1924 (9:16), 24 fps, AAC stereo 44.1 kHz, mean −22.0 dB / peak −3.4 dB.

**Transcript diff** (Whisper small.en; multilingual agrees):

| Expected | Heard | Match |
|---|---|---|
| A lot of them get pressed in every night. | 0.92–3.24 A lot of them get pressed in every night. | ✅ |
| So now I sleep in these. | 6.24–7.93 So now I sleep in these. | ✅ |
| They hold my skin flat all night. | 9.20–11.01 They hold my skin flat all night. | ✅ |
| Comment photo and I'll send you what I use. | 11.84–14.50 Comment photo and I'll send you what I use. | ✅ ("photo" a little slower, not shouted) |

All 31 words, in order, nothing added. **Timing differs from the plan:** there's a ~3.0 s silent gap (t 3.24–6.24) while she reaches, and "So now I sleep in these" lands at 6.2–7.9, not over the reach at 4.4–6.

| Checklist B item | Result | Notes |
|---|---|---|
| Same woman, hair, earrings, T-shirt every frame | ✅ | |
| Bare face; nothing touches her face | ✅ | The film stays beside her face on frame-right and never touches it. |
| Talking clip: words match; lips track speech | ✅ | |
| Exactly two hands, five fingers; no hand crosses the face | ✅ | The frame-right hand reaches **straight** to the tray (t ≈ 4.0–5.8) and never crosses her body or face. Phone hand frame-left, still at chest height the whole clip. Holding hand during the hold (t 8–15): 5 digits. |
| Tray state: 5 pieces until the lift, bare after | ✅ | 5 pieces to t ≈ 5.8; tray bare and teal from t ≈ 6.2 to the end. |
| **No morphing, melting, extra objects; pieces keep shape and count through the move** | **❌** | **t ≈ 5.8–6.7:** she lifts the pieces off the tray as a dangling chain of loose crescents. There's no backing film, the forehead band isn't visible, and some crescents float below her fingers. **t ≈ 6.8–7.2:** the hand swings out past the frame-right edge in a semi-transparent motion smear. **t ≈ 7.25:** it comes back holding a flat film about twice the size of the tray pieces, with band + 4 crescents. The pieces change shape, size and grouping mid-move, against "the film and pieces keep their shape, stay flat and clear… exactly five pieces". Frames: `frames_CLIP_B2/pickup_zoom.png` (t 5.83–6.67), `lift_frames.png` (t 6.83–7.33). |
| Wrinkles don't change mid-clip; skin not airbrushed | ✅ | No strong expression furrows in this clip. |
| Starts on K1 and ends on K5 | ✅ | First frame = K1; last frame = K5 `4576bff3` (film with band + 4 crescents beside her face, tray bare). |
| Clean parts | ✅ | t 0–5.75 (talking, then a clean reach to the tray) and t 7.3–15.04 (steady hold of a correct 5-piece film, band tab down, crescents never circles) are usable. |

### Proposed fix (owner decision; nothing run)

A redo doesn't fit the budget. A B2 redo costs 37.5, and actual_total is now 128.5 against the 135 cap (6.5 headroom). Even a 5 s std silent lift insert (≈10) would go over. So the proposal is **cut around it in assembly, 0 credits** (lessons §5/§8: "cut around it… trim the glitch on frame boundaries"):

1. **Jump cut (recommended):** picture B2 t 2.2 → 5.7 (the clean reach to the tray), hard jump cut to B2 t 7.4 → (film already held). Tighten the 3 s dead air in the audio: drop B2 audio t 3.4–6.1 so "So now I sleep in these" (6.24) follows "every night" with a normal pause. A selfie jump cut on a beat is native to TikTok and hides the whole transition (frame-boundary cut: frame 137 → frame 178).
2. **Cutaway alternative:** keep the B2 audio continuous and cover t 5.7–7.4 with the K5 still (the approved held-film frame, same light and framing), then return to B2 at 7.4 or go straight to K4 as storyboarded.
3. **If the owner prefers a re-render:** it needs a cap increase (+37.5 at least). Prompt fix for that case: name the lift as a single rigid object ("she pinches the corner of the clear backing film and lifts the whole flat film in one piece; the five pieces stay stuck flat on it and move with it; the hand stays inside the frame the whole time"), and shorten the move by starting the hand already on the film's corner (or a 5 s silent K1→K5 lift insert in std mode).

Storyboard impact: the on-screen B2 window (t 2.2–7.2) currently ends inside the glitch. With option 1 or 2 the window becomes t 2.2–5.7 + 7.4–~8.9.

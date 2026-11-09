# Assembly: "REAL or SUS?" expert stitch, P4 (run 2026-11-08-1338), v2

**Credits spent: 0.** Built locally with ffmpeg, numpy, PIL and whisper-cli (small.en).
Code is in `scratchpad/asm-p4/`: `render.py` (picture) and `audio.py` (voice track). The v1 versions are kept as `render_v1.py` and `audio_v1.py`.

## v2: fixes from video-review.md (FAIL, free fixes)

| # | Review item | What changed | Check |
|---|---|---|---|
| 1 | KL_E1 lip sync (mouth ahead of the voice by ≈0.45 s) | Picture now starts 0.35 s into the clip and audio 0.80 s in, so audio is 0.45 s earlier relative to picture. In the raw clip the mouth opens at 0.42 s and voice energy starts at 0.90 s (−48 → −24 dB). The 0.3 s of closed mouth at the head and the silent nod tail were trimmed (E1 is now 2.12 s) | 10 fps mouth strip on the final (`scratchpad/asm-p4/lipsync_v2.png`): mouth opens at 9.9 s as audio rises (−31 dB), wide on "It's the" at 10.0–10.5 s, lips round at ≈10.6–10.8 s, closure at ≈11.3 s on "Smooth" |
| 2 | 1.1 s dead air before "Tape" | E23 now ends at 8.52 s ("morning" ends at 8.40); E45 starts at 0.33 s ("Tape" at 0.40). Also tightened: "crease."→"No" (E23 3.78/4.12), "off."→"This" (E45 2.62/3.12), "area."→"My" (5.37/6.08), and E1→E23 | Gaps over 0.3 s after 9.8 s on the final mix (−38 dB gate): only 16.5–16.9 s (0.4 s, the natural "needles. / They" breath inside one E23 take) and the intended verdict beats 25.2–25.7 and 26.1–26.55 s. The 21.35–22.45 s gap is gone |
| 3 | Peel jump repeated at ≈19.8 s | "No needles… by morning" (15.61–20.01 s) now plays only the held-sheet / softer-forehead tail, as a live ping-pong. The lift → jump appears once, at 7.75 s | 4 fps sheet, 15.75–20.0 s |
| 4 | Flat-lay card too long (optional) | The card now shows only on "This kit is shaped for each area" (22.30–24.55 s, 2.25 s). "Tape and one-size patches can fall off" plays over live U1 (band being pressed on) | 4 fps sheet |
| 5 | Full-bleed framing (optional) | **Not applied.** At 1.0× her face (source y 490–1225) leaves no room for the 2-line title above and the 3-line caption below, inside 14–65%. The text would have to cross her face or the patch. The opening and verdict layouts stay at 0.925× with feathered edges | — |
| — | Bare "before" forehead (coordinator) | **No clean bare-forehead footage exists.** In U1 the band is in front of or just above her forehead until it's pressed on; S_B0 was never animated. The nearest is U1 ≈1.0–1.9 s, where her forehead lines show under the raised band. It's already on screen at 1.0–1.9 s and again at 12.0–12.6 s. No freeze or still was added | — |

Runtime: 30.93 → **28.12 s**.

## Outputs (this folder)
| File | What |
|---|---|
| `final.mp4` | v2. 1080×1920, 30 fps, 28.12 s, H.264 CRF 16, AAC 192k. −16.0 LUFS, true peak −4.9 dBFS (31.5 MB) |
| `real-or-sus-p4_botox-question_v2_2026-11-08.mp4` | Same file as final.mp4, with the posting name. The v1 file is kept for reference |
| `post.mp4` | 4.8 Mbps, **16.8 MB**, voice included, −16.1 LUFS |
| `final-contact.png` | Every 0.25 s (4 fps), 112 frames |
| `compare-contact.png` | Reference (top) vs ours (bottom) at the same timestamps |

## Timeline v2 (output seconds)
| Time | Picture | Text | Audio |
|---|---|---|---|
| 0.00–5.00 | U1_APPLY: she lowers the band from the lens (lines show under it at ≈1–1.9 s) and presses it on | Title "REAL or SUS? / Wrinkle smoothing patches" (lilac, white stroke), y 272–436. Bottom caption (white, black stroke), y 1070–1245 | Light room tone |
| 4.50–9.83 | KL_X0 keyed lower-left, spring pop-in. Brow lift ≈7.6 s, closed-lip smile and nod 8.3–9.5 s | — | — |
| 5.00–7.75 | U2_PEEL 0–2.75 s: pinch and corner lift | same | — |
| 7.75–9.83 | U2_PEEL 3.92–6.00 s: held sheet, softer forehead. Jump cut with a 1.10× punch-in. The failed 2.75–3.92 s is never shown | same | — |
| 9.83–11.95 | KL_E1 at 0.35–2.47 s, full screen, over a blurred live U2 tail. The real box pops in at 10.23 s | "It's The Wrinkle Smooth / Face Set!" | E1 audio from 0.80 s: "It's the Wrinkle Smooth Face Set." |
| 11.95–15.61 | Green screen: U1 1.19–4.85 s in the top half, E23 0.12–3.78 s keyed in the bottom half | Word-by-word captions, y 905–1065 | "They hold your skin flat all night, so it can't crease." |
| 15.61–20.01 | Held-sheet tail only (live ping-pong), with E23 4.12–8.52 s at a 1.07× punch | "No needles" chip from 15.66 s | "No needles. They seal in moisture, so lines look smoother by morning." |
| 20.01–22.30 | Live U1 (pressing the band on), with E45 0.33–2.62 s | Captions | "Tape and one-size patches can fall off." |
| 22.30–24.55 | Real flat-lay card pops in (push 100→106%), with E45 3.12–5.37 s at a 1.06× punch | Card labels "forehead · under-eyes · smile lines"; captions | "This kit is shaped for each area." |
| 24.55–28.12 | Verdict: the opening framing, U2 softer forehead live, E45 6.08–7.85 + 8.20–10.0 s | "MY VERDICT?", then "REAL!" on "Real", "REAL! Not SUS" on "Not", and the "Comment REAL for the link" pill | "My verdict? Real. Not sus." |

Every beat is live video. No clip is slowed and no still stands in for a beat. The box and the flat lay are code pop-ups of the real assets over live video, as approved in the storyboard.

## Decisions kept from v1
- **Framing for the safe areas.**
  - In the opening and verdict sections, UGC is at 0.925× (hairline at y≈400, chin at y≈1080) over a blurred copy of itself.
  - In the mechanism section it's at 1.0×, shifted up (face at y 160–895).
- **Expert size and position.**
  - His face sits at 65–85% of the frame height, below all text and clear of the right-hand buttons.
  - So he's smaller than the reference's expert (about 25% vs 45% of the frame width).
- **Keying** is custom numpy:
  - alpha from G − max(R,B);
  - despill to max(R,B);
  - 1 px choke;
  - side feather where the coat meets the source edge;
  - small enclosed holes refilled (the E1 lens reflection).
- **E1 voice matching:**
  - pitch −4% with duration kept, giving f0 125.7 Hz (E23 125.3, E45 123.1);
  - denoised;
  - +3 dB at 2 kHz;
  - every clip levelled to −20 LUFS of speech before the mix.
- **Audio:** voices plus light room tone only (no music or SFX, per the owner).

## QA (v2)
- **Whisper (small.en) on final.mp4 and post.mp4.** Both give, word for word: "It's the Wrinkle Smooth Face Set. They hold your skin flat all night so it can't crease. No needles. They seal in moisture so lines look smoother by morning. Tape and one size patches can fall off. This kit is shaped for each area. My verdict? Real. Not sus." That is all 43 words, in order.
- **Loudness:** final −16.0 LUFS, post −16.1 LUFS; true peak ≈ −4.8 dBFS.
- **Safe areas** (per-frame overlay boxes logged by the renderer):
  - All text sits between y 272 and y 1245 (top 14% = 269, bottom 35% line = 1248).
  - The box pop-up rests at y ≈707–1242.
  - No text crosses her face or the patch. Captions sit between her chin and the expert's hair.
- **Keying:** unchanged code from v1, which was checked at full res. There is no green fringe on the hair, beard, glasses rims or the hand-on-forehead. The E1 lens is grey glare, not a hole.
- **The failed peel frames are absent,** and the lift → jump appears once.
- **Owner checks:** nothing looks like an injury, no reaction is overacted, and every beat is video.

## Cold viewer (v2)
- **1 s:** A woman in bed holds a clear, forehead-shaped sheet up to the lens. The top reads "REAL or SUS? Wrinkle smoothing patches"; the bottom says people ask if she's had Botox. *"Is this wrinkle-patch thing legit?"*
- **3 s:** She is pressing it onto her forehead with both hands; her lines showed as she lowered it. *"She sleeps in it instead of Botox."*
- **5 s:** Morning, and she pinches the corner. A grey-haired man in glasses and a white coat pops into the corner, watching. *"Someone's going to judge this."*
- **10 s:** She holds the peeled sheet by her cheek; her forehead looks softer and natural. He has smiled and nodded, and is now full screen naming it ("It's the Wrinkle Smooth Face Set") with the real box beside him. *"It worked; here's what it is."*
- **After that:**
  - the mechanism (flat all night, no needles, moisture) over her clips;
  - "why this kit" over the real flat lay;
  - "REAL! Not SUS" and "Comment REAL for the link".

## Still open (not blockers)
- **Owner should listen** to 9.8–12.0 s next to 12.0–20.0 s: is it the same man? Pitch, level and EQ were matched by measurement only (review fix 4).
- **Flat-lay pebble:** the flat-lay asset has a small pebble at its bottom-right; it's part of the approved image.
- **Stiff held sheet:** the held sheet in U2 looks fairly stiff, as noted in clips-check.

## v3 (Nov 8, evening): real peel + hand tone
- **5.00–9.83: one continuous peel, no cut.** Gemini T1 0–1.9 s chained to Kling 3.0 std T3 0–2.6 s (see `peel-v2/iterations.md`), played at 93% speed. It ends as the patch comes free, then cuts to E1. The old U2 lift → jump cut is gone.
- **U1 (0–5 s, 12–15.6 s, 20–22.3 s):** the left hand is colour-matched to her lit right hand (the owner's "hands look dark" note), at 0 credits.
- Same audio and timeline. 28.12 s, −16.1 LUFS. `final_v3.mp4` / `post_v3.mp4` (16.8 MB).
- Renderer: `scratchpad/asm-p4/render_v3.py`. Raw: `raw/PEEL.rgb`, `raw/U1F.rgb`.
- Credits: the peel redo cost 17 (still 2, Kling 4.0 9, Kling 3.0 std 6) plus 3 Gemini videos. Total for this video, all versions: 63.75.

# Clips check (gate B): run 2026-11-08-1338-ref-real-or-sus-p4

Stage 7, stage B, on Higgsfield (owner: "Do it on higgsfield, I have no patience").
- Prompt-review pass 2 fixes applied word for word (U1 IDs and sentence; U2 IDs and R1–R3; KL_X0 block; KL_E1 sentence).
- One output per job, preflighted, no redos.
- Files: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/clips-p4/`. Checks: 8-frame sheets, 10 fps strips of the peel, mouth crops, whisper-cli (small.en).

| Clip | Job ID | Settings | Credits | Gate B |
|---|---|---|---|---|
| U1_APPLY | 783f2a1f-f68d-46ef-bf8c-ef6c98536b76 | kling3_0 pro 5 s silent, 1076×1928 | 8.75 | **PASS** |
| U2_PEEL | 60966d13-a9c9-4bf7-9900-458f4ffb9342 | kling3_0 pro 6 s silent, 1076×1928 | 10.5 | **FAIL: peel physics.** Usable windows below |
| KL_X0 | 55b9f1b6-e922-43f7-b833-815e044b80df | kling3_0 std 5 s silent, 716×1284 | 7.5 | **PASS** |
| KL_E1 | a0601604-bfef-41e5-80dc-fa2d4a8c557c | kling3_0 std 5 s sound, 716×1284 | 10 | **PASS** (one note) |

## U1_APPLY
- Same woman, lamp, claw clip and framing; no cut.
- She draws the band in, lays it on with the tab DOWN, presses from the centre to the temples with two hands (five fingers each), then lowers her hands and rests her head back.
- ONE band, clear and slightly frosted, tab down, below the hairline.
- Lips closed throughout, no smile, nothing injury-like.
- Note: around 3–3.5 s her hands cover most of the forehead during the press. That's fine.

## U2_PEEL: FAIL (owner's peel-physics rule)
- **0–2.8 s, good:** her frame-right hand comes up and pinches the band corner at the **frame-right** temple, not the frame-left one as R1 asked. The corner lifts and bends a few mm with no skin tug. The band stays glossy and flat, tab down, lips closed.
- **2.8–3.8 s, fake:** there is no fold travelling across the forehead.
  - The whole band turns **milky/frosted** and smears.
  - It slides **down across her frame-left eye and cheek** in about 0.5 s. That reads as a wipe, not a peel.
  - Her eyes are closed at ≈2.4 s and ≈3.0 s.
- **3.9–6.0 s, good:** one clear sheet hangs from her frame-right fingers beside her cheek. Her eyes close briefly, then she gives a closed-lip satisfied look.
  - The forehead is bare and even, with no outline or redness.
  - The lines are softer but still traceable. This matches S_U2_END.
  - The sheet still looks fairly stiff.
- **Free fallback (lessons §6, prompt-review pass 2):** cut from the lift (0–2.8 s) to the bare, held-sheet tail (3.9–6.0 s), hiding the cut with a hard cut or punch-in. That gives about 4.9 s.
- **Paid redo** (mid-lift still ≈2 + U2 10.5) does not fit: 3.25 credits are left under the cap. The owner decides.

## KL_X0
- Same expert, green flat, lips closed in every mouth crop, no sound.
- Neutral and skeptical, then a slight brow lift, a small closed-lip smile and a nod. Understated, no overacting.
- Hands out of frame.

## KL_E1
- **Whisper:** "It's the Wrinkle Smooth Face Set." Exact, 0.00–3.10 s.
- **Mouth:** closure on "Smooth" (m) at ≈1.9 s. Closed-lip nod from ≈3.2 s to the end.
- **Voice vs E23** (autocorrelation proxy):
  - Median f0 is 131 Hz vs 125 Hz, so the pitch is close.
  - Pace is ≈2.0 vs 2.34 words/s.
  - Still needs a listen by ear before assembly.
- **Note:** the gesturing hand crosses in from the frame-left (camera-arm) side, and the extended selfie arm is no longer visible after ≈1.5 s. There is one hand with five fingers, empty, and nothing appears beside him. Not noticeable at phone speed, so it's a note.
- Std resolution: upscale to 1080 in assembly.

**Spend:** stills 10 + clips 36.75 = **46.75 of 50**. 3.25 left; no clip redo possible within the cap.

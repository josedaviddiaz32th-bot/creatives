# Assembly — run 2026-11-08-0230 — slot 2-T (P2, The Proactive Problem-Solver)

Producer, assembly stage, 2026-11-08. **0 credits** (all local: ffmpeg, PIL, whisper-cli). Final: `final.mp4`
(mp4s are gitignored) · contact sheet `final-contact.png` (4 fps, cyan lines = safe area).
Scripts: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/assembly-2t/`
(`build.sh`, `words.py`, `audio.py`, `render.py`, `qa.py`; work files in `work_voiceover-zoe/`).

## Voiceover

**Higgsfield "Zoe"** (seed_audio, speech_rate 15, job `1fd85be1-ebd8-4eb5-9309-23b858b2b97b`, 4.8 credits, charged at
generation, not here): `clips-2t/voiceover-zoe.wav`, 49.45 s raw. This is the **final** voice (owner); Lara and Gia
are superseded.
- Pauses: 33 speech islands found in the waveform. Every pause was cut to **0.20 s inside a sentence / 0.28 s after
  a sentence / 0.30 s after "Alarm."** (all ≤ 0.3 s, `editing.max_word_gap_seconds`). Pauses already shorter were left
  as they were. **No words cut or changed.**
- Two silent beats added by design: 1.55 s after "So you can stop them." (shot 19, the sheet) and a 1.4 s end-card
  hold after "link".
- Result **42.72 s**. Under 47 s, so **no speed-up** (1.00×). It lands under the ~45 s target because Zoe reads
  fast (133 words in 36 s of speech) and no pause may be longer than 0.3 s. The only way to reach 45 s is longer
  pauses, which breaks the spec. Owner call if wanted.
- **"But no cream stops…" check:** she says **"But no cream stops a pillow folding your face"**, word for word.
  Second passes on Zoe: ggml-small.en and ggml-small on a tight crop (26.9–29.0 s) both hear "but no cream stops a
  pillow folding your face". The full-file small.en word pass does too. The same check on the superseded Gia take:
  the plain full-file small.en pass misheard it as "The cream stops". The word-level pass, ggml-small, and tight crops
  with both models all heard "But no cream stops". So it was a context error in whisper, not the take.
  - A per-island whisper pass heard "Stay seal in moisture" for "They seal in moisture". A tight crop with both
    models and both full-mix passes hear **"They seal in moisture"**.

## Shot list (output timings, Zoe)

32 cuts in 42.72 s · **avg 1.33 s** · max 2.48 s (end card) · cuts at 1.11 s and 2.27 s in the first 3 s.

| # | Out (s) | Dur | Source | VO | Motion / code |
|---|---|---|---|---|---|
| 01 | 0.00–1.11 | 1.11 | C01_FLOP src 0.75–3.0 s (≈2× speed: the arm smear t 1.0–1.4 lasts ~0.2 s) | Why are your wrinkles | Push 1.00→1.04. Real box composited on the nightstand, revealed at 0.35 s once the flung arm has passed |
| 02 | 1.11–2.27 | 1.16 | P02 | worse on one side? | Fast push 112→122 % onto the glowing pillow side |
| 03 | 2.27–4.56 | 2.29 | C03_LAMP src 0.95–3.04 | Lights out. You roll onto your side. | Lamp click lands on "out", push 1.0→1.05 |
| 04a | 4.56–5.25 | 0.69 | P04 | Same side, | Wide, push 4 % |
| 04b | 5.25–6.16 | 0.91 | P04 | every night. | Punch-in 118→122 % on her head and the dent |
| 05 | 6.16–7.49 | 1.33 | P05 | Your cheek sinks in. | Push 6 % toward the sinking cheek |
| 06 | 7.49–9.07 | 1.58 | C06_FOLD src 0.2–1.9 (owner) | The skin by your eye folds. | Code glow: 3 Sunrise-Orange crease lines fade in at the eye corner as the fold forms (src 1.35–1.75) |
| 07 | 9.07–10.10 | 1.03 | P07 | Two a.m. | Rack-blur in. Real box on the nightstand. "2:00" glowing digits in code on the blank clock display. Push 6 % |
| 08 | 10.10–11.84 | 1.74 | C08_PRESS src 0.3–3.04 | That fold is pressed into a crease. | Push 4 % |
| 09a | 11.84–13.80 | 1.96 | P09 | Four-thirty. You haven't moved. | Wide, cooler grade |
| 09b | 13.80–14.83 | 1.03 | P09 | Neither has it. | Punch 116→120 % on the glowing crease |
| 10 | 14.83–15.70 | 0.87 | C10_ALARM src 1.0–3.04 (owner-accepted open mouth, no speech) | Alarm. | Shake on the cut, alarm SFX |
| 11 | 15.70–17.42 | 1.72 | R11 | There it is, on that side. | Push 6 % |
| 12 | 17.42–18.67 | 1.25 | R12 | Still there at lunch. | Push 5 %, orange arrow to the frame-left crease |
| 13 | 18.67–19.96 | 1.29 | P13 | You blamed your age. | Push 7 %, candle flicker glow, "38" badge |
| 14 | 19.96–21.32 | 1.36 | P14 | Tried every cream going. | Pan + push (parallax feel) |
| 15 | 21.32–22.10 | 0.78 | X15 | But no cream stops | Push 8 %, orange ring pops on the V under the cream |
| 16 | 22.10–23.47 | 1.37 | P16 | a pillow folding your face. | Push 8 % |
| 17a | 23.47–24.37 | 0.90 | P17 | A lot of those lines are | Wide |
| 17b | 24.37–25.60 | 1.23 | P17 | pressed in while you sleep. | Punch 116→120 % |
| 18 | 25.60–26.64 | 1.04 | P18 | So you can stop them. | Push 10 %. Real box drops onto her open palm on "stop" (pop + thud) and stays in her hand |
| 19 | 26.64–28.06 | 1.42 | S19 (13 % cropped off the right: face/ear edge gone) | — (silent beat) | Push 4→12 %, warm lamp flicker on the bright edges, 2 sparkles, chime |
| 20 | 28.06–30.07 | 2.01 | C20_PRESS_ON src 0.4–3.04 | Night one: clear silicone patches | Push 4 % |
| 21 | 30.07–31.21 | 1.14 | C21_HELD src frames 0–9 → 34–41 (owner-accepted clip) | hold the skin flat, | Pillow resting → pressed, with a thud on the jump. The invented plunger (src f3–33, f42–55) and the milky end (≥2.3 s) are cut out; no plunger frame is on screen |
| 22 | 31.21–32.65 | 1.44 | P22 | so it can't fold and crease. | Push 6 % |
| 23 | 32.65–33.92 | 1.27 | C24_PLUMP src 0–1.5 | They seal in moisture, | Push 4 % |
| 24 | 33.92–35.64 | 1.72 | C24_PLUMP src 1.5–3.04 | so the top layer stays plump. | Punch 106→110 %, warm glow pulse |
| 25 | 35.64–37.30 | 1.66 | X24 crop | Nothing goes under your skin. | 1.50→1.56× on the clear layer's edge (≤1.5× start, per production log) |
| 26 | 37.30–38.27 | 0.97 | R11 ("before") | Morning one: | Hold 1.06→1.08 |
| 27 | 38.27–39.69 | 1.42 | R27 ("after") | your lines look smoother. | 0.4 s orange-line wipe from R11 to R27, same framing |
| 28 | 39.69–40.24 | 0.55 | hero `face-set-hero-9x16-v1.png` | Comment PILLOW | Slam-in 1.08→1.0, anchored at the product's bottom edge |
| 29 | 40.24–42.72 | 2.48 | hero (end card) | and we'll send you the link. (+1.4 s hold) | Full-screen CTA, slow push to 1.015 |

## Code overlays (all PIL PNGs, Poppins; brand Deep Teal #17393D, Sunrise Orange #F08A2C, Soft Mint #F4F8F6)

- **Captions:** word by word, Poppins ExtraBold 64–74 px, white with a black stroke; the word being spoken turns
  orange. Chunks are ≤4 words and never cross a cut or a sentence end. Each shot has its own position (bottom of the
  safe area, or the top over the teal cross-sections and where a face fills the lower frame). No captions on 19 or on
  28–29 (the CTA card carries the words).
- **Labels** (teal pill, mint text, orange accent bar, pop-in with overshoot): LIGHTS OUT, SAME SIDE, FOLD, CREASE,
  ALARM (shakes), EVERY CREAM, PRESSED IN / WHILE YOU SLEEP, NIGHT 1, HELD FLAT, SEALED IN, YESTERDAY, MORNING 1.
- **Clock cards** (teal pill with a drawn clock): 2:00 AM, 4:30 AM, 12:00 PM. Plus "2:00" digits on P07's blank clock
  display.
- **Chips:** NO NEEDLES, NO ACTIVES (mint pill, orange ✕). **"38" badge** (orange circle) on the cupcake shot.
- **Stickers:** an arrow to the crease (12), a ring on the V (15), sparkles (19).
- **Crease glow** on C06: three orange lines with bloom, faded in with the fold.
- **Real box** (`face-set-box-v1.png`, hand-traced outline, scene-matched light, contact shadow; never redrawn) on
  C01's nightstand, on P07's nightstand, and dropped onto P18's palm.
- **End card:** "THE WRINKLE SMOOTH FACE SET" / "THE DAILY GLOW CO." (from 28), then a white comment bubble
  **COMMENT "PILLOW"** and **WE'LL SEND YOU THE LINK** (on "send"). All of it sits in the empty top area. The product is
  pasted untouched on a plate built from the hero's own edge colours.
- Pop-ups land at 26 moments; the longest gap between two is **2.99 s** (spec 3–5 s, so never longer than 5 s).

## Audio

- Voice: the pause-cut Zoe take. No music or SFX from third parties: **everything below is synthesized in code**.
- SFX (40 cues, each ~0.12 s before its word or cut): whoosh on cuts, pop on labels, tick on the clock cards, a click
  on the lamp, a 4-beep alarm, a soft thud for the box landing and the pillow press, a chime on the sheet, an air
  swoosh into the CTA.
- Music bed: a synthesized pad plus a soft pluck arpeggio (Am–F–C–G, 96 BPM), brighter from NIGHT 1.
- Ducking is level-based: in every 10 ms bin where she speaks, SFX and bed are held **≥12 dB** (bed 14 dB) under the
  quietest local voice level. **0 bins** over that limit for SFX, **0** for the bed. In the master: SFX ≈ −20.3 LUFS
  (config −22…−18), bed ≈ −34 LUFS (subtle).
- Master: two-pass loudnorm to **−16.1 LUFS integrated, −2.1 dBTP**, AAC 192 k.

## QA (self, on `final.mp4`)

| Check | Result |
|---|---|
| Whisper on the final mix: 133 words, in order | **133/133 in order** with small.en and with small (word-level passes) |
| Every text/sticker box inside the safe area (y 269–1248, x 0–1080), checked over every drawn frame incl. pop overshoot | **0 violations** |
| CTA text vs product (per frame, slam included) | ≥ **45 px** clearance on every frame |
| Black frames (blackdetect) | none |
| Runtime / fps / size | 42.72 s, 30 fps, 1080×1920 |
| Max shot length | 2.48 s (≤ 2.5) |
| Product in the first 2 s | real box on the nightstand from 0.35 s |
| Stray mouths | Nobody mouths words. C10's open mouth (no speech) was accepted by the owner. All P/R stills have closed lips |
| Contact sheet looked at | Hook text clears her head. Captions sit on the body, pillow, neck or teal, never over eyes or mouth (C06, P16, R11 and R12 are face macros, where the caption sits on the cheek, jaw or neck). The box sits in her palm on 18. No plunger frames on 21. Shot order matches the storyboard |

Fixes made during QA: the C01 box is hidden while her flung arm passes it, so it never sits on top of the arm; the box
moved onto the palm in P18 (it was floating above it); the R12 caption was lowered off her chin; the end-card
background was rebuilt (the first version had a blurred ghost of the box and feather bands); labels moved down 7 px
(pop overshoot crossed the top 14 %); island tails were lengthened by 40 ms, because whisper on the mix heard
"fold" for "folds".

Known compromises: shot 03 runs 2.29 s (it starts at 2.27 s, so the first 3 s still change at 1.11 s and 2.27 s; the
lamp also goes dark at ~2.8 s). Shot 28 is 0.55 s, so the brand line stays on through the end card. The S19 sheet
beat is 1.55 s of silence under music, as storyboarded.

## Swap the voiceover (one command)

```
"/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/assembly-2t/build.sh" /path/to/new-voiceover.wav [final.mp4]
```

For any take of the same 133-word script, the command:
1. Runs whisper-cli (ggml-small.en, word level, 16 kHz mono) island by island and aligns the 133 words.
2. Cuts the pauses (≤0.3 s), adds the S19 beat and the end hold, and speeds up ≤1.08× only if the result is over 47 s.
3. Re-times every cut, caption and pop-up from the new word times (all are keyed to word indices) and re-renders.
4. Re-mixes the SFX and music under the new voice and masters to −16 LUFS.
5. Re-runs this QA into `work_<vo-name>/qa.json` plus `<out>-contact.png` in the run folder.

A run takes about 70 s.

## v2 (review fixes + owner recast), 2026-11-08

Fixes from `video-review.md` (round 1 FAIL, anatomy 7), all done in code: **0 credits**. Shot list and timings are
unchanged (42.72 s, 32 shots, avg 1.33 s); only the frames listed below changed.

**Output:** `2t-one-night-pillow_hook-worse-one-side_v2_2026-11-08.mp4` (checklist C name), with `final.mp4` as a
byte-identical copy. Contact sheets: `2t-one-night-pillow_hook-worse-one-side_v2_2026-11-08-contact.png` and
`final-contact.png`.

| Fix | Done |
|---|---|
| 1. Shot 2 teeth | **Not applied (owner):** shot 2 is pixel-identical to v1 (diffed at 1.2 s and 1.9 s) |
| 2. End card held 3.02 s | Punch-in to 1.08× on "send" (41.25 s), anchored at the product's top edge so the product grows away from the CTA, with a whoosh. The end card is now 39.69–41.25 s, then 41.25–42.72 s. The longest framing anywhere is 2.48 s. The CTA text stays ≥ **53 px** clear of the product on every frame |
| 3. budget.json | VO_GIA 4.8 (superseded) and VO_ZOE 4.8 added, plus assembly 0; **actual_total 100.1** of 135; status updated |
| 4. File name | as above (`build.sh VO NAME` also copies to final.mp4 and final-contact.png) |
| 5. Noon proof | The arrow now points at the frame-left (her right, worse-side) outer eye corner. A thin orange trace follows her two under-eye creases and two crow's-feet lines (it fades in with the arrow on "there") |
| 6. Duplicate labels | SAME SIDE, EVERY CREAM and PRESSED IN / WHILE YOU SLEEP removed. A wordless moon sticker replaces SAME SIDE so the pop-up rhythm holds (longest gap 4.46 s, counting the box landing in her palm) |

**Owner recast (white woman matching the Pixar character), via `assembly-2t/stills_map.json`:**
- **R11 → `R11_v3`** (shots 11 and 26, "before") and **R27 → `R27_v3`** ("after", a softening edit of R11_v3; same
  wipe). The framing is pushed to 1.10–1.19× so her closed lips at the bottom-right edge stay out of frame. Captions
  moved to the forehead so the cheek lines (the proof) stay clear.
- **R12 → `R12_v2`** (noon). Framed at 1.12–1.16× so "STILL THERE AT LUNCH" sits on her sweater collar, not her
  mouth. The arrow and trace were re-placed on this still's creases.
- **S19 → `S19_v3`** (fair hands, lamp-backlit sheet, no face). The old 13 % right crop is removed; the push is
  centred on the sheet.

**QA on the v2 file:** whisper on the final mix **133/133 in order** (small.en and small). **0 safe-area violations**
(every overlay, every frame, pop overshoot included). Ducking: **0 bins** with SFX or the bed less than 12 dB under the
voice. **−16.1 LUFS / −1.8 dBTP**, no black frames, 42.72 s, 1080×1920, 30 fps.

I looked at the contact sheet: the order matches the storyboard, the recast stills show in shots 11, 12, 19, 26 and
27, no lips are visible on the eye macros, the arrow lands on the creases, the punch-in shows from 41.25 s, and shot 2
is unchanged. Full-res crops were checked for the noon arrow and trace.

Rebuild (same command, new voice or stills):
`"/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/assembly-2t/build.sh" VO_FILE 2t-one-night-pillow_hook-worse-one-side_v2_2026-11-08.mp4`

# Video review — run 2026-11-08-0230 — slot 2-T (P2, The Proactive Problem-Solver)

Stage 8 (video-reviewer), round 1, 2026-11-08. **0 credits spent; video not edited.**
Read: `CLAUDE.md`, `.claude/agents/video-reviewer.md`, `brief.md` (owner section first), `format.md`, `story.md`,
`story-review.md`, `storyboard.md`, `stills-check.md`, `clips-check.md` (owner accepted C10's open mouth and C21),
`budget.json` (owner change: VO = Higgsfield Zoe), `assembly.md`, `docs/lessons-learned.md` (all; checklist C in §10),
`pipeline/config.yaml` (`editing`, `review`), `learning/production-log.md`.

**How it was checked (not taken from the producer):** `final.mp4` probed with ffprobe; 170 frames at 4 fps viewed as
contact sheets; 47 full-res frames (1080×1920) viewed at every cut and every overlay, plus full-res crops of the hook
macro, the NIGHT 1 and asleep-with-patches faces, the noon split and the before/after; scene-cut detection (ffmpeg
`scdet`); EBU R128 loudness; whisper-cli (ggml-small.en, word level) on the final mix, with tight re-crops on both
small and small.en models where the full-file pass misheard.
Work files: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/vr2t/`.

## Verdict: **FAIL** (one item at 7; every fix below is free, code-only re-render)

Claims are clean and every other score is ≥ 8 (`review.min_score_to_publish` = 8). The one failing item is
**Anatomy (7)**: in the hook, shot 2 (1.11–2.27 s), a row of skull teeth shows through her see-through cheek beside the
mouth. That is a "skeletal grin" in the most-watched 1.2 s of the video, the same defect that failed P16 v1 in this run.
It can be fixed in assembly (fix 1) and needs no credits.

## File facts

| Check | Result |
|---|---|
| Duration | **42.72 s**. Owner asked for "about 45 s": 2.3 s short, inside TOF 30–50 s (`video.seconds_by_stage.tof`). Acceptable; owner call (see fix 7) |
| Size / aspect / fps | 1080×1920, 9:16, 30 fps |
| Audio | Present, AAC stereo 48 kHz. **−16.1 LUFS integrated**, true peak −2.1 dBTP, LRA 3.0 LU |
| Transcript vs story.md | **133/133 words, in order** (word-level pass). The plain full-file pass heard "The edges hold the skin flat" for "Night one: clear silicone patches hold…"; a tight crop (27.5–31 s) heard **"Night one. Clear silicone patches hold the skin flat"** on both small.en and small. That was a whisper context error, not the take. Same small-word differences as before ("2 am", "4.30") |
| Word gaps | Only one gap > 0.3 s: 1.74 s after "So you can stop them." (26.40–28.14 s). This is the storyboarded silent sheet beat (S19, music and chime, visual change). No other gap over `editing.max_word_gap_seconds` |
| Cuts | scdet finds 28 hard cuts; with the punch-ins (33.92 s, etc.) and the R11→R27 wipe, ~31 visual changes. Changes at 1.13 s and 2.30 s in the first 3 s. **Longest unbroken framing: 3.02 s, the end card 39.70–42.72 s** (only text pops at 40.24 s; see fix 2). Every other shot ≤ 2.29 s |

## Scores

| # | Item | Score | Reason |
|---|---|---|---|
| 1 | Logic | 8 | Hook question → one night on the pillow (fold → crease → still there at noon) → age and creams blamed, "no cream stops a pillow folding your face" → "pressed in while you sleep, so you can stop them" → box in hand → sheet → NIGHT 1 mechanism (held flat, sealed in, nothing under the skin) → MORNING 1 → CTA. A cold TOF-U viewer can follow it. Weak spot: the photoreal proof never clearly shows "worse on one side". In R12 (17.43–18.70 s) both eyes look about the same, and the arrow points at her temple and brow, not at a crease. The hook's own visual puts the glow lines on the pillow fabric, not on her skin (fix 1, fix 5) |
| 2 | Script fidelity | 10 | 133/133 words in order; nothing cut or garbled (see the transcript row above) |
| 3 | Lip sync (voiceover only) | 9 | Nobody mouths words. Every Pixar and photoreal mouth is closed except C10's sit-up (14.83–15.70 s), where her mouth is slightly open with no speech. The owner accepted that, and the production log records the rule. Not marked down further |
| 4 | Anatomy | **7** | **Shot 2 (1.11–2.27 s, P02 hook macro): skull teeth visible through the cheek beside the mouth, for the whole shot.** The run treated this as a defect elsewhere (P16 v1 FAIL; P06A/P16 rebuilt with "no skull, teeth or jaw bone show through"); stills-check left P02 as "owner to judge", and no owner ruling is recorded. Everything else holds: the jaw shows only as neck vertebrae in shots 5/7/9 (on concept), the S19 real hand is one hand with normal fingers, the skeleton hands are intact, and the NIGHT 1 and asleep faces have no melting |
| 5 | Continuity | 8 | Same Pixar character throughout (dark low bun, silver studs, sage shirt, see-through body) and same photoreal P2 woman in R11/R12/R27. Minor: her awake face (shots 10, 13, 14, 17, 18, 20) reads younger, with big round eyes, than her sleeping face (5, 7, 9). Shot 10's bedroom is mirrored (window and clock frame-left, bed reversed) against P01/P03 |
| 6 | Product | 9 | The real box (never redrawn) is on the nightstand from 0.35 s and in front of the 2:00 clock, then drops onto her palm on "stop" (25.6–26.6 s). The hero box and brand line are on the end card. Patches: S19 is the real sheet, clear, exactly five pieces, forehead tab **down**. NIGHT 1 (28.1–30.1 s) has a clear band with the tab down between the brows plus one under-eye crescent. P22 (31.2–32.7 s) shows all five, clear, tab down, slim crescents, lips uncovered. The crescents are plump half-moons (owner tolerance) but never circles or rings. Clear is never white; X24's 1.5× crop (35.6–37.3 s) is the milkiest frame but the skin still shows through |
| 7 | Claims | 10 | VO and text use only lessons §1–2 and owner item 6: "hold the skin flat, so it can't fold and crease", "seal in moisture, so the top layer stays plump", "nothing goes under your skin", NO NEEDLES / NO ACTIVES, "your lines look smoother", "a lot of those lines are pressed in while you sleep". No collagen, elastin, repair, study, %, duration, "permanent", credential, price, guarantee or Black Friday. Clock cards are times, not durations; "38" is the character's age, not a statistic. The box art ("Overnight smoothing patches", "5 reusable silicone patches") is the approved real asset |
| 8 | Budget | 10 | Higgsfield: stills 48.5 + clips 42.0 + VO Gia 4.8 + VO Zoe 4.8 = **100.1 ≤ 135** (cap). Bookkeeping: `actual_total` in budget.json still says 90.5 (fix 3) |
| 8b | Owner checklists B and C | 9 | See below; one ❌ (file name, free) |
| 8c | Pace and lip sync (`editing`) | 8 | Word-by-word captions (current word orange), ≤4 words per chunk; changes at 1.13 s and 2.30 s; ~26 pop-ups, longest gap ≈3 s; push-ins 4–12 % on stills, punches 116–122 %; no speed-up (1.00×). Two exceptions: the end card holds one framing for 3.02 s (> `max_shot_seconds` 2.5; fix 2), and the 1.74 s silent S19 beat (storyboarded). The m/b/p check doesn't apply (nobody talks) |
| 9 | Story intent | 9 | Delivers the approved story: hook question fully on screen and spoken by 2.3 s, with motion in frame one (she flops onto the pillow); ~62 % problem; the patches arrive as the next scene, not a pitch; CTA "Comment PILLOW and we'll send you the link" on its own full-screen beat (40.24–42.72 s, bubble + "WE'LL SEND YOU THE LINK"). Pixar style on every animated shot; photoreal R11/R12/R27/S19 |

## Owner checklists (lessons §10)

**B. Clips (as cut into the final)**

| Item | ✅/❌ | Note |
|---|---|---|
| Checklist A holds in every frame (same person, clear patch, tab down, slim crescents, lips uncovered, no mirror/cream/text from the model) | ✅ | No model-made text anywhere: the clocks are blank with code digits; cream jars are blank; the box is the real asset. No mirror. X15's cream is the point of that shot |
| Wrinkles don't change mid-clip (except the planned before/after) | ✅ | C06's fold forms and is held by the trim plus code glow; R11→R27 is the planned before/after, like-for-like, softer and not erased |
| Lips never open (non-talking) | ✅ (owner) | C10 open mouth, no speech: owner-accepted |
| No patch slid, doubled, split, vanished or turned opaque | ✅ | C20 one crescent, band steady; C21's plunger and milky tail are cut out (no frame on screen) |
| Exactly two hands, five fingers; no hand through a face or patch | ✅ | Shot-specific hand counts hold (C03 one hand; S19 one real hand) |
| Starts/ends on approved frames | ✅ | |
| No smile with patches on | ✅ | P22 lips closed, a calm resting mouth; NIGHT 1 no smile |

**C. Final**

| Item | ✅/❌ | Note |
|---|---|---|
| Price, offer, dates match the live store | ✅ n/a | TOF: no price, offer or date in the video or caption |
| Product visible in the first 2 s | ✅ | Real box from 0.35 s |
| CTA has its own full-screen beat | ✅ | 40.24–42.72 s |
| Text below top 14 % and above bottom 35 % | ✅ | Viewed on every overlay: labels/clock cards top ≈ y 300–340, lowest captions ≈ y 1180 (limit 1248); end-card text y ≈ 310–640. Assembly's per-frame assert agrees (0 violations) |
| ≤8 words per text element; spelling | ✅ | Longest: PRESSED IN / WHILE YOU SLEEP (5), THE WRINKLE SMOOTH FACE SET (5), WE'LL SEND YOU THE LINK (5). All spelled right: FOUR-THIRTY., TWO A.M., HAVEN'T, NIGHT 1, MORNING 1, COMMENT "PILLOW" |
| Audio −16 LUFS; commercial-use music | ✅ | −16.1 LUFS / −2.1 dBTP. Bed and SFX are synthesized in code (no third-party music). SFX sit under the voice: all 133 words survive whisper on the full mix, and assembly measured 0 bins over the −12 dB duck (stems not re-measured here) |
| Link in bio / caption link → product page | — | Publisher's step (caption: "Comment PILLOW and we'll send you the link") |
| File named with concept, hook, version, date | ❌ | `final.mp4` (fix 4) |

## Fixes (numbered; all free / code-only unless marked)

1. **[free, required] Shot 2, 1.11–2.27 s (P02, hook macro): teeth through the cheek.** Re-frame the code push so the
   mouth/jaw at frame-right (≈ x 820–1000, y 700–1150 of the output frame) is out of frame: anchor the push on the
   lower (pillow-side) eye and cheek and keep the total scale ≤ 1.5× on the still (production log). If that crop can't
   hold the eye, paint a soft skin-tone mask over the teeth (feathered, matched to the cheek) for the whole shot. While
   in there, draw 2–3 Sunrise-Orange crease lines **on the lower cheek skin** (the C06 code glow) so "worse on one side"
   reads on her face, not on the pillow. Re-run `build.sh` with the Zoe take (~70 s); no credits. A single-still redo
   isn't needed.
2. **[free, required] End card, 39.70–42.72 s: one framing for 3.02 s** (> `editing.max_shot_seconds` 2.5). Add a punch-in
   (e.g. 100→108 %) at ≈41.3 s ("send"), or cut the hero slam to a tighter framing at 40.24 s when the CTA bubble lands.
   Keep the CTA text ≥ 44 px clear of the product on every frame (existing assert).
3. **[free, bookkeeping] budget.json `actual_total` = 90.5 is stale.** Set it to 100.1 (stills 48.5 + clips 42.0 + VO
   Gia 4.8 + VO Zoe 4.8) and update `status` (VO done, assembly done, 0 credits).
4. **[free, checklist C] File name.** Save the approved render as e.g.
   `2t_one-night-pillow_hook-worse-one-side_v1_2026-11-08.mp4` (keep `final.mp4` if the publisher expects it).
5. **[free, recommended] R12, 17.43–18.70 s ("Still there at lunch"): the one-sided crease isn't visible.** Move the
   arrow from her temple/brow to the frame-left outer eye corner lines and add a faint orange trace along those lines
   (or a left/right highlight split as storyboarded). Then the noon proof shows what the hook asks about.
6. **[free, optional] Duplicate label + caption.** SAME SIDE (4.56–6.16 s), EVERY CREAM (19.97–21.33 s) and PRESSED IN
   WHILE YOU SLEEP (24.37–25.60 s) each show the same words twice at once (label + caption). Drop the label on those three,
   or change it to a different word, to cut clutter.
7. **[owner call, free] Runtime 42.7 s vs "about 45 s".** Within the band. To reach ~45 s without breaking the 0.3 s
   pause rule: lengthen the S19 sheet beat by ~0.5 s and the end-card hold by ~1 s (with fix 2's punch), or accept 42.7 s.

**Needs credits:** none. No clip or still redo is required.

## Re-review

After fixes 1–2 (and 3–4), re-run this check on the new render: the hook frames 1.1–2.3 s at full res, the end-card cut,
the safe-area assert, whisper 133/133 and −16 LUFS. If those hold, every score is ≥ 8 → PASS.

## Owner decisions after round 1 (Nov 8, 2026)
- **Fix 1 (shot 2 teeth) waived by the owner:** "I didn't even notice that, don't change that." Shot 2 stays as v1. This was the only reason for the anatomy score of 7.
- **Fixes 2–6 applied** in v2 (end-card punch-in, budget, file name, noon arrow on the creases, repeat labels removed).
- **Owner recast:** the realistic woman (R11, R12, R27, S19) is now a white woman matching the Pixar character (R12_v2, R11_v3, R27_v3, S19_v3; 9.0 credits).
- **Length:** 42.72 s, kept as "about 45".
- **Status:** v2 approved for posting by the owner's decisions above; final spend 109.1 of 135.

# Storyboard — run 2026-11-08-0230 — slot 2-T (P2, The Proactive Problem-Solver)

Stage 5 (storyboarder). Built on `story.md` (APPROVED; words unchanged), `story-review.md` (carry-forward
notes 1–7, all applied below), `brief.md` (owner section first), `format.md`, `docs/lessons-learned.md`
(all), `learning/production-log.md`, `pipeline/config.yaml`, the Resilia swipe breakdown and its frame
sheets. **No credits spent.** Prompts: `prompts.json`. Estimate: `budget.json`.

## 1. Video type and audio source

**Voiceover only** (owner instruction 3). One narrator track for the whole video: ElevenLabs **Lara –
Natural, Relatable and Engaging** (library `vChnJZ1Cu89g2XXumPfT`, young American female, "made for
social videos"), eleven_v3, stability 0.45 / style 0.5 / similarity 0.75 (config `elevenlabs_narrator`).
Fallback if the connector can't use the library voice: Higgsfield `text2speech_v2` elevenlabs, preset
**Emily** (2.25 credits, preflighted). **Nobody talks or mouths words on screen.** Every still and clip
prompt says "her mouth stays closed; she does not speak" / "SHE DOES NOT TALK: her lips stay closed the
whole time". All Kling clips are `sound: off` (VO, music and SFX are added in assembly). No patch-on
smiling.

**Why:** the owner made this voiceover-only; it also removes all lip-sync risk and lets Kling run silent
(1.75 credits/s instead of 2.5).

## 2. Continuity sheet

- **Pixar character (all P shots):** the same Pixar style 3D-animated see-through woman of about 38: glossy
  ivory skeleton body like a friendly anatomy toy; a thin translucent skin layer over face and hands,
  **softly tinted warm peach-rose** (review note 1: never colourless glass, so the clear patch reads on
  it); big friendly eyes; dark hair pulled fully back in a low bun, nothing on the forehead; small silver
  studs; sage-green sleep shirt. **Mouth closed, never speaks.** She sleeps on **her right side** every night.
- **Pixar look:** soft rounded shapes, warm cinematic light, glossy subsurface materials (matches the
  reference's 3D look, sheet_01). Night: moonlit blue + one warm lamp on the nightstand. Morning: pale
  daylight from a window on the frame-left side. Crease accent: soft Sunrise Orange (#F08A2C) glow.
- **Set:** big bed, huge white pillow on the frame-left side of the bed, nightstand on the **frame-right**
  side whose front half stays **empty** in every still (the real box is composited there in code).
- **Cutaways (X shots):** Pixar style skin block "like a soft slice of cake": warm peach-rose top layer,
  soft pink layer below, no fibres/cells/vessels, deep-teal #17393D background, sunrise-orange rim light.
  Patch = thin clear slightly frosted layer with a bright edge highlight, never white or coloured.
- **Photoreal P2 woman (R shots, brief's locked face):** 38, warm medium-brown skin (South Asian or
  mixed), dark low sleek bun, small silver studs, minimal makeup, unretouched; fine lines under the eyes
  and at outer corners, 2–3 faint forehead lines, a sleep crease **clearly deeper on her right side =
  frame-left in a front-on image**. Cream knit sweater. Soft, even, diffuse window daylight (not raking).
  Skin dry and matte. Lips closed. No mirror.
- **Voice description:** n/a on camera (no talking). Narrator only (above).

## 3. Shot → asset plan (reuse first; lessons §7, Higgsfield history, Runway list)

| Asset | Where | Used for | Decision |
|---|---|---|---|
| Face Set box `0f24791e-57ce-49ab-afe4-85d5f8e0d243` (`assets/packaging/face-set-box-v1.png`) | Higgsfield generation / local file | Box on the nightstand in shots 1, 3, 7, 17, 18 (and visible in 10) | **Reuse, composited in code** (cut out of the mint background). Never re-rendered in a Pixar shot (owner, review note 4) |
| Hero 9:16 `39637096-4223-49c3-a881-37feba3e280a` (`face-set-hero-9x16-v1.png`) | Higgsfield / local | Shots 28 (brand) and 29 (CTA end card) | **Reuse as is**, text in code |
| Face Set sheet held to a window, 5 s `bd37ae30-ad4a-4070-a00f-eebc50c42a21` | Runway (checked) | — | **Not used (Revision 1)**: daylight and an older hand broke continuity between night shots 18 and 20; replaced by new still S19 |
| Face Set studio flat lay `564c68fa-cbff-4997-8c84-feaa071f7d0b` | Higgsfield generation | S19 (count, layout, tab down) | Reuse as a free reference |
| Forehead-patch Element `6375c707-…` + Eye-patches Element `9d766c06-…` | Higgsfield Elements | P20A, P20B, P22, X21 | Reuse (product shape; PATCHES block verbatim) |
| 3D skin cross-section set `4478cf98`, `d7e35b5e`, `53a8695f` | Runway (checked) | — | **Not used**: photoreal medical renders prompted "no cartoon style" (lessons §0 needs "Pixar style" for skin cross-sections) and they show collagen/elastin fibres + capillaries, which the brief keeps out |
| Pixar character, cutaways, P2 photoreal face | — | everything else | **New**: nothing in §7 or history is a Pixar character, a Pixar cutaway, or a 38-year-old P2 face on Higgsfield (brief) |

## 4. Keyframe chain (every still is an edit of the previous unless marked fresh)

| Still | From | Model | State list |
|---|---|---|---|
| **P01_FLOP_START** | fresh (identity anchor) | nano_banana_2 | Kneeling on bed, facing camera, sleepy; hands on duvet; pillow frame-left; lamp ON; nightstand frame-right, front of top empty; night palette |
| P02_SQUASH_MACRO | P01 | nano | Macro, head lying sideways, right cheek down in the pillow along the bottom of the frame (right eye = lower eye), faint orange lines on the pillow side only, other side smooth; eyes closed |
| P03_LAMP | P01 | nano | Nightstand close-up; one see-through hand from frame-left, fingertip on lamp switch; lamp ON; her head blurred; nightstand top empty |
| P04_TOPDOWN | P01 | nano | Top-down; curled on right side; worn dent on that side; lamp OFF, moonlight |
| **P05_SIDE_SINK** | P01 | nano | Pillow-height side view; asleep on right side; cheek sinks, skin pushed toward eye; lamp OFF |
| P06A_EYE_FLAT | P05 | nano | Extreme macro, outer corner of right eye, skin smooth against pillowcase; eye closed |
| P06B_EYE_FOLD | P06A | nano | Same; skin folded into one pleat, orange glow along it |
| P07_CLOCK | P05 | nano | Nightstand: round clock with **blank** glowing display (no digits, note 2); front of top empty; her blurred behind |
| P09_GLOW_CREASE | P05 | nano | Same pose; lower, cooler moonlight; crease traced in orange |
| P10_ALARM_START | P01 | nano | Wide, dawn light from frame-left; asleep on right side; blank clock; room above her to sit up |
| P13_CUPCAKE | P01 | nano | Kitchen daylight; fingertip (frame-left hand) pokes line at right eye; cupcake with **one plain candle, no number** (note 2) |
| P14_CREAM_SHELF | P01 | nano | **Bedroom dresser top**, blank pastel jars, plain wall, "no mirror and no reflective surface" (note 3); shrug, two hands |
| P16_PILLOWCASE_PRINT | P02 | nano | Macro cheek on crumpled pillowcase; wrinkles print orange lines into skin |
| P17_REALISE | P01 | nano | Morning; sits on bed edge, looks back at dented pillow; brows lift only slightly (production log); nightstand top empty |
| P18_REACH | P17 | nano | Turned back to camera; frame-right hand held out at chest height, palm up, flat and **empty**; looks down at it; nightstand front empty; **no box drawn** (box composited on the palm in code, note 4) |
| P20A_NIGHT1_HOLD | P01 + Elements | nano | Sitting up in bed, lamp ON; **forehead band ON** (tab DOWN, middle ⅔, not to hairline); **one crescent held** in frame-left hand just below frame-left eye, not touching; **other three crescents: not on face, not in frame** (note 6); mouth closed, no smile |
| P20B_NIGHT1_ON | P20A + Elements | nano | Same; that crescent now flat below the lashes; fingertip on its outer end; nothing else changed |
| P22_ASLEEP_PATCHED | P05 + Elements | nano | Asleep on right side wearing the **whole Face Set** (forehead + 2 under-eye + 2 smile-line, lips uncovered, exactly five; pillow-side pieces may be partly hidden) (note 6); skin by the pillow-side eye flat, no fold; eyes/mouth closed; no pose to camera (review: shot 22 check) |
| **X08A_FLAT** | fresh | gpt_image_2_6 medium | Skin block, pillow fabric resting lightly, top layer flat |
| X08B_CREASE | X08A | nano | Pillow presses; deep V crease glowing orange |
| X15_CREAM | X08B | nano | White cream droplets sit on top; V still forms beneath |
| X21_PATCH_FLAT | **X08A** + Forehead Element | nano | Clear patch layer on top with bright edge; pillow presses; skin stays flat (built from the flat frame so no crease has to be removed) (note 1) |
| X23_MOISTURE | X21 + Forehead Element | nano | Pillow gone; droplets trapped under the patch |
| X24_PLUMP | X23 + Forehead Element | nano | Top layer softly plumper, warm glow; patch flat |
| **R12_NOON** | fresh (P2 identity anchor) | nano | Front-on, cream knit, even daylight, lips closed; crease deeper frame-left |
| R11_EYE_MACRO | R12 | nano | Macro of frame-left (her right) outer eye + upper cheek; crease at exactly the same depth; even morning daylight; lips out of frame |
| R27_AFTER | R11 | nano | Same framing and light; lines about two-thirds as visible, every line traceable (note 5) |
| S19_SHEET_LAMP | fresh, refs R12 (hand skin) + 564c68fa (layout) + Eye-patches Element | nano | Night; one hand (5 fingers) holds the clear film upright, backlit by the warm lamp; exactly five pieces, band on top with tab DOWN, four crescents below; sage cuff at the wrist; dark moonlit room; face out of frame |

**Why these models:** `nano_banana_2` (config `image_model`) for both identity anchors and every edit: the
same Pixar character, the same cutaway and the same P2 face must carry through ~25 frames, the Elements
work on it, and the confirmed before/after fix is a nano edit. `gpt_image_2_6` (config `cheap_image_model`)
only for X08A: a fresh, text-only stylised composition with no person and no product (0.5 vs 1.5 credits).
GPT Image 2.6 is our text/logo model, but no still here needs printed text: the box is never re-rendered
(composited from the real asset) and all words are added in code.

## 5. Shots (timeline from story.md; ≤2.5 s per shot, config `editing`)

Motion key: **K** = Kling 3.0 clip (pro, sound off, 3 s, trimmed). **Code** = still with push-in
(`still_push_pct` 6–10%), parallax or pop, free in assembly. All text is added in code, below the top 14%
and above the bottom 35%.

| # | Time | Still | Motion | On-screen text (code) | VO |
|---|---|---|---|---|---|
| 1 | 0.0–1.3 | P01 | **K C01_FLOP**: tips onto the pillow, pillow puffs (motion in frame one); real box composited on nightstand | WHY ARE YOUR WRINKLES | "Why are your wrinkles |
| 2 | 1.3–2.7 | P02 | Code: fast push-in 112→120% onto the glowing side | WORSE ON ONE SIDE? | worse on one side?" |
| 3 | 2.8–4.3 | P03 | **K C03_LAMP**: click, room drops to moonlit blue; box composited | LIGHTS OUT | "Lights out. You roll onto your side. |
| 4 | 4.3–6.5 | P04 | Code: slow top-down rotate + push 6%; split into two cuts (4.3–5.4 wide, 5.4–6.5 punch-in on the dent) | SAME SIDE | Same side, every night." |
| 5 | 6.5–8.1 | P05 | Code: push 8% toward the cheek | | "Your cheek sinks in. |
| 6 | 8.1–9.8 | P06A→P06B | **K C06_FOLD**: the skin folds into a pleat | FOLD | The skin by your eye folds." |
| 7 | 9.9–11.3 | P07 | Code: rack-blur pulse on the clock; box composited; clock card pops | 2:00 AM | "Two a.m. |
| 8 | 11.3–12.9 | X08A→X08B | **K C08_PRESS**: pillow presses the V crease | CREASE | That fold is pressed into a crease." |
| 9 | 13.0–15.3 | P09 | Code: two cuts (wide 13.0–14.2, punch-in 118% on the glow 14.2–15.3); moonlight shift = grade change | 4:30 AM | "Four-thirty. You haven't moved. Neither has it." |
| 10 | 15.4–16.6 | P10 | **K C10_ALARM**: sits bolt upright, eyes wide; alarm SFX | ALARM | "Alarm. |
| 11 | 16.6–17.9 | R11 | Code: push 6% | | There it is, on that side. |
| 12 | 17.9–19.1 | R12 | Code: split highlight frame-left vs frame-right, push 6% | 12:00 PM | Still there at lunch." |
| 13 | 19.2–20.5 | P13 | Code: push + candle flicker overlay | | "You blamed your age. |
| 14 | 20.5–21.9 | P14 | Code: parallax (jars foreground) | EVERY CREAM | Tried every cream going." |
| 15 | 21.9–23.4 | X15 | Code: push 8%; cream chips pop | | "But no cream stops |
| 16 | 23.4–24.9 | P16 | Code: push 8% | | a pillow folding your face." |
| 17 | 25.0–27.4 | P17 | Code: two cuts (wide, punch-in on the dented pillow) | PRESSED IN WHILE YOU SLEEP | "A lot of those lines are pressed in while you sleep. |
| 18 | 27.4–28.9 | P18 | Code: the real box (traced mask, contact shadow) lands **on her open palm** with a pop, punch-in; shot ends with the box in her hand (note 4) | | So you can stop them." |
| 19 | 28.9–30.4 | S19 | Code: slow 6% push + warm light flicker on the piece edges | | (music + soft pop) |
| 20 | 30.5–32.4 | P20A→P20B | **K C20_PRESS_ON**: crescent pressed on centre-out, band already on | NIGHT 1 | "Night one: clear silicone patches |
| 21 | 32.4–33.8 | X21 | **K C21_HELD**: pillow presses, skin stays flat | HELD FLAT | hold the skin flat, |
| 22 | 33.8–35.2 | P22 | Code: slow push 6% (calm, asleep) | | so it can't fold and crease." |
| 23 | 35.2–36.8 | X23 | **K C24_PLUMP** first half (droplets held) | SEALED IN | "They seal in moisture, |
| 24 | 36.8–38.5 | X24 | **K C24_PLUMP** second half (plumps, glow) | | so the top layer stays plump." |
| 25 | 38.5–40.2 | X24 (macro crop) | Code: 1.5× max crop on the patch edge (production log: ≤1.5× push), chips pop | NO NEEDLES · NO ACTIVES | "Nothing goes under your skin." |
| 26 | 40.3–41.3 | R11 | Code: hold, "before" | YESTERDAY | "Morning one: |
| 27 | 41.3–42.3 | R27 | Code: wipe from R11 to R27, same framing | MORNING 1 | your lines look smoother." |
| 28 | 42.4–44.0 | hero 39637096 | Code: slam-in zoom anchored at the product's bottom edge; overlay box must clear the product mask on every frame (production log v3.1) | THE WRINKLE SMOOTH FACE SET · THE DAILY GLOW CO. | "Comment PILLOW |
| 29 | 44.0–46.0 | hero 39637096 | Code: full-screen CTA end card, hold ~1 s after the last word | COMMENT "PILLOW" | and we'll send you the link." |

**Count:** 29 shots (+3 extra code cuts in 4, 9, 17 for pacing → ~32 cuts in ~46 s, ≈7 per 10 s; first 3 s
change at 1.3 s and 2.8 s). **28 new stills** (25 shots have their own new still; 11/26 share R11 by
design, 25 is a crop of X24, 28/29 reuse the hero) and **8 Kling clips** (shots 1, 3, 6, 8, 10, 20,
21, 23–24). Every shot has an approved still before any clip runs (gate A).

## 6. Assembly notes (free; producer)

- Captions word-by-word (config `editing.captions`); clock cards and labels as pop-ups; one SFX per visual
  event placed ~0.12 s before its word, ducked ≥12 dB under the VO; no risers under speech (production log).
- Box composite: key the real box from the mint background with a hand-traced mask (auto-keying fails on
  white items; production log v3.1), scale it small on the nightstand, add a contact shadow; check every
  frame of C01 and C03 for drift.
- Overlays never over a face; assert overlay boxes clear the product mask on every frame (production log).
- No single still > 25% of runtime (largest here ≈ 3.6 s, R11 across shots 11 and 26).
- Music: commercial-library bed ducked ~10 dB under the VO; master −16 LUFS; contact sheet every 0.5 s.

## 7. Review notes 1–7 (story-review) → where applied

1. Tinted skin vs clear patch: continuity sheet; P20A/P20B/P22/X21 carry the tint sentence; patch never white.
2. No in-scene text: P07/P10 blank clock; P13 plain candle; P14 blank jars; every P prompt bans text/digits; times in code.
3. No mirror: P14 is a dresser against a plain wall, "no mirror and no reflective surface".
4. Box never re-rendered: empty nightstand spot in P01/P03/P07/P10/P17/P18; real box composited; P18 ends on the box at her hand in code.
5. Before/after: R11 (before = shot 11's still) → R27 softening edit, same framing and light, "two-thirds as visible, every line traceable".
6. State lists: P20A/P20B name every piece (band on, one crescent, three not on face / not in frame); P22 = all five, lips uncovered.
7. Length: time the Lara read first; if over ~47 s, apply story.md's trims ("Same side, every night." then "You haven't moved.") before any whole-clip speed-up (≤1.08×); mechanism lines never cut.

## 8. Owner flags

- Lara is an ElevenLabs library voice billed on the ElevenLabs plan (no Higgsfield credits, no cost preview);
  audition it against the Emily fallback before the run if possible.

## Revision 1 (prompt-review round 1 FIX, applied)

- **G1:** P01's character sentence pasted word for word into all 17 Pixar character stills (P02–P22); the close-ups (P02, P06A, P06B, P16) also say "Only the parts of her that fall inside this framing are visible."
- **G2:** R12's description (without the line details) added to R11 and R27.
- **P02:** orientation fixed (pillow side = bottom of the frame, right eye = lower eye, glow lines on the lower half).
- **P10:** clock is a blank display with no digits, numbers or hands; "never draw any box or product".
- **P13:** the poked line is described (a faint orange crease at the frame-left eye).
- **P18 / shot 18:** open, empty palm held at chest height; the real box is composited **onto her palm** in code, so the shot ends with the box in her hand.
- **P20B:** both ends of the move stated; exactly two pieces in the image.
- **X21:** stray "remove the cream" deleted. **X23/X24:** material-only sentence, tint sentence and the Forehead-patch Element (free) added.
- **C03:** "Only one hand is in frame". **C06:** "No hands in frame". **C10:** "no gasp, no yawn and no open-mouthed expression".
- **VO_LARA + fallback:** "Comment pillow" (no caps); the words are otherwise unchanged. The producer takes the voice_id from `creative_list_voices`.
- **Shot 19:** new photoreal still **S19_SHEET_LAMP** (her hand, lamp-backlit film, sage cuff; nano_banana_2 1k, 1.5, preflighted) replaces the Runway bd37ae30 reuse. Shot 25 now crops X24.
- Re-preflighted 2026-11-08: nano 1k with 2–3 refs 1.5, Kling pro silent 3 s 5.25, TTS fallback 2.25 (prices unchanged). **New total 85.25** (stills 41.0, clips 42.0, VO 2.25); 34.75 under the 120 first-pass limit. Nothing submitted.

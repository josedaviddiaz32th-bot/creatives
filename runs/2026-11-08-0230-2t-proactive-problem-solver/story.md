# Story — run 2026-11-08-0230 — slot 2-T (P2, The Proactive Problem-Solver)

Stage 3 (scriptwriter). Built on `brief.md` (owner section first), `format.md`, `docs/lessons-learned.md`,
`docs/creative-strategy.md`, `learning/playbook.md` (all UNTESTED, nothing RETIRED), `pipeline/config.yaml`.
No credits spent.

## 1. Concept

**"One night on your pillow."** A Pixar-style see-through woman falls asleep on the same side as every
night, and a clock-stamped timeline (LIGHTS OUT → 2:00 AM → 4:30 AM → ALARM → 12:00 PM) shows her pillow
folding the skin by her eye into a crease she then blames on her age; the same timeline, run again as
NIGHT 1 → MORNING 1, shows clear silicone patches holding that skin flat and sealed until morning.

**Why it fits her:** P2 is 38, practical, "tried every anti-wrinkle cream going" and wants the *cause*
explained before she believes a fix. This gives her a cause she can see (the fold), a reason her creams
didn't touch it, and a physical fix with nothing under the skin. Her one-sided lines are the hook; her
pillow is the reveal.

## 2. Format

**Voiceover with b-roll, voiceover only** (`format.md`): one second-person narrator (ElevenLabs, config
`elevenlabs_narrator`), Pixar-style animated shots + a few photoreal inserts. **Nobody talks on camera.**
The Pixar character's jaw stays closed and never moves as if talking; the photoreal woman's lips stay
closed. Every shot below is a distinct still (owner: a still for every sequence).

## 3. Hook

**Main (0–2.7 s):** "Why are your wrinkles worse on one side?"
On-screen hook text (8 words, in code): **WHY ARE YOUR WRINKLES WORSE ON ONE SIDE?**
Frame one: she flops onto her side into a big pillow (motion), the Face Set box on the nightstand.

**Alternatives (same body):**
- B. "Is one side of your face aging faster?" — text: ONE SIDE AGING FASTER? (avoid any "faster" claim
  beyond the visual; it is her question, not our statement)
- C. "Which side do you sleep on? Check your wrinkles." — text: WHICH SIDE DO YOU SLEEP ON?

**All hooks drafted (TOF: 10+):**
1. Why are your wrinkles worse on one side? ✔ main (identification + curiosity; the brief's direction)
2. Is one side of your face aging faster? ✔ alt B
3. Which side do you sleep on? Check your wrinkles. ✔ alt C (comment bait)
4. Why is that line by your eye always on the same side?
5. Did your pillow give you that crease?
6. Why do your morning lines not fade by lunch anymore?
7. Tried every anti-wrinkle cream and that one line won't budge?
8. What does your pillow do to your face at 2 a.m.?
9. What if some of your wrinkles aren't age at all?
10. Why does one eye look more tired than the other?
11. Is your pillow the reason your cream isn't working?
Kept 1–3: they are questions she'd ask herself, they work with sound off and no context, and they don't
name the product category (strategy §6).

## 4. Full script with timestamps

Narrator VO, second person. Planned at config `words_per_second` 3.0 with 0.1–0.2 s gaps between
chapters (pauses trimmed per `editing.max_word_gap_seconds`). **P** = Pixar style (3D-animated, soft
rounded shapes, warm cinematic light). **R** = photoreal (lessons §4 STYLE). Character in every P shot:
the same Pixar-style see-through woman of about 38: glossy ivory skeleton body like a friendly anatomy
toy, a thin translucent glass-like skin layer over her face and hands (so the skin can be seen folding),
dark hair in a low bun off her forehead, small silver studs, sage sleep shirt; **jaw closed, never
talking.** R shots use the brief's locked P2 woman (38, warm medium-brown skin, dark low bun, silver
studs; lines under the eyes, at the outer corners and on the forehead, deeper on her right/sleeping side).
Night palette: moonlit blue with a warm lamp; the crease line glows soft Sunrise Orange.

| # | Time | Beat | Shot (one still each) | On-screen text (code) | VO |
|---|---|---|---|---|---|
| 1 | 0.0–1.3 | Hook | **P** Bedroom at night, lamp on. She flops onto her side into a big pillow, pillow puffs up. The real Face Set box on the nightstand, uncommented. | WHY ARE YOUR WRINKLES | "Why are your wrinkles |
| 2 | 1.3–2.7 | Hook | **P** Macro: the pillow side of her see-through face squashed into the pillow; faint glowing lines on that side only, the other side smooth. | WORSE ON ONE SIDE? | worse on one side?" |
| 3 | 2.8–4.3 | Problem: timeline | **P** Her hand clicks the lamp off; room drops to moonlit blue. | LIGHTS OUT | "Lights out. You roll onto your side. |
| 4 | 4.3–6.5 | Problem | **P** Top-down: she curls onto her right side; a worn dent in the pillow on that same side. | SAME SIDE | Same side, every night." |
| 5 | 6.5–8.1 | Problem: the fold | **P** Side see-through view: her cheek sinks into the pillow, the translucent skin layer pushed up toward the eye. | | "Your cheek sinks in. |
| 6 | 8.1–9.8 | Problem: the fold | **P** Macro at the outer eye: the skin layer folds over itself into a soft pleat against the pillowcase. | FOLD | The skin by your eye folds." |
| 7 | 9.9–11.3 | Problem: timeline | **P** Nightstand clock glowing 2:00, the box beside it; she sleeps, blurred behind, still on that side. | 2:00 AM | "Two a.m. |
| 8 | 11.3–12.9 | Problem: mechanism | **P** Skin cross-section: pillow fabric presses down; the top skin layer is pinched into a deep V crease. | CREASE | That fold is pressed into a crease." |
| 9 | 13.0–15.3 | Problem: timeline | **P** Same pose, moonlight has shifted; clock at 4:30; the crease by her eye traced in a soft orange glow. | 4:30 AM | "Four-thirty. You haven't moved. Neither has it." |
| 10 | 15.4–16.6 | Problem: morning | **P** Alarm rings; she sits bolt upright, eyes wide (jaw closed). | ALARM | "Alarm. |
| 11 | 16.6–17.9 | Problem: proof | **R** Morning window light, macro of the P2 woman's right outer eye: pillow crease lines across the corner. Lips out of frame. | | There it is, on that side. |
| 12 | 17.9–19.1 | Problem: proof | **R** Same woman at midday, front-on, lips closed: her left side vs her right side, the crease still there on the right. (No mirror.) | 12:00 PM | Still there at lunch." [claim 3] |
| 13 | 19.2–20.5 | Problem: reframe | **P** Kitchen counter: a cupcake with a "38" candle; she pokes at the line by her eye, unimpressed. | | "You blamed your age. |
| 14 | 20.5–21.9 | Problem: reframe | **P** Bathroom shelf crammed with half-used, unbranded cream jars; she shrugs. | EVERY CREAM | Tried every cream going." |
| 15 | 21.9–23.4 | Problem: reframe | **P** Cross-section: cream droplets sit on top of the skin layer; the pillow presses down and the fold still forms beneath them. | | "But no cream stops |
| 16 | 23.4–24.9 | Problem: reframe | **P** Macro: pillowcase wrinkles printing their lines into her cheek's skin layer. | | a pillow folding your face." |
| 17 | 25.0–27.4 | Problem: the cause | **P** She sits on the bed edge, looking back at the dented pillow: realisation. | PRESSED IN WHILE YOU SLEEP | "A lot of those lines are pressed in while you sleep. [claim 3] |
| 18 | 27.4–28.9 | Turn | **P** She reaches for the Face Set box on the nightstand (real box design). | | So you can stop them." [claim 3] |
| 19 | 28.9–30.4 | Turn: product | **R** Fingers hold the clear five-piece sheet up to warm lamp light: thin, transparent, slightly frosted, edges catching the light. | | (music + soft pop, no VO) |
| 20 | 30.5–32.4 | Answer: NIGHT 1 | **P** Sitting up in bed, she presses a clear crescent on just below her eye, from the centre outward; the clear forehead band already on, tab pointing down between the brows. | NIGHT 1 | "Night one: clear silicone patches |
| 21 | 32.4–33.8 | Answer: mechanism | **P** Cross-section: a clear patch layer lies on the skin; the pillow presses; the skin layer stays flat, no V. | HELD FLAT | hold the skin flat, |
| 22 | 33.8–35.2 | Answer: mechanism | **P** Side see-through view: she sleeps on her side wearing the patches; face against the pillow, skin by the eye smooth, no fold. Eyes closed, calm. | | so it can't fold and crease." [claim 2, owner 6] |
| 23 | 35.2–36.8 | Answer: mechanism | **P** Cross-section: tiny moisture droplets rise from the skin and stay under the clear patch. | SEALED IN | "They seal in moisture, |
| 24 | 36.8–38.5 | Answer: mechanism | **P** Cross-section: the top skin layer softly plumps, glowing warm. | | so the top layer stays plump." [claim 2, owner 6] |
| 25 | 38.5–40.2 | Answer | **P** Macro: the clear patch resting on the skin surface, nothing beneath it. Pop-up chips. | NO NEEDLES · NO ACTIVES | "Nothing goes under your skin." [claim 1, owner 6] |
| 26 | 40.3–41.3 | Proof: MORNING 1 | **R** "Before": shot 11's framing and light (yesterday). | YESTERDAY | "Morning one: |
| 27 | 41.3–42.3 | Proof: MORNING 1 | **R** "After": same framing and light, lines softer (about two-thirds as visible, every line still traceable, not erased). | MORNING 1 | your lines look smoother." [claim 4] |
| 28 | 42.4–44.0 | Brand + CTA | **R** Product hero (asset `39637096…`, teal, orange rim light). | THE WRINKLE SMOOTH FACE SET · THE DAILY GLOW CO. | "Comment PILLOW |
| 29 | 44.0–46.0 | CTA | End card, full-screen beat: hero still + big CTA. | COMMENT "PILLOW" | and we'll send you the link." (hold ~1 s after the last word) |

**Beat split:** hook 0–2.7 s · problem 2.8–30.4 s (≈66%) · answer 30.5–42.3 s · CTA 42.4–46.0 s.
**Open loops:** the hook question stays open until 25 s ("pressed in while you sleep"); each clock card is
a mini loop ("what happens by 4:30?"); NIGHT 1 opens a loop that MORNING 1 closes. All close inside the video.

**Clean VO text (for the narrator):**
Why are your wrinkles worse on one side? Lights out. You roll onto your side. Same side, every night.
Your cheek sinks in. The skin by your eye folds. Two a.m. That fold is pressed into a crease. Four-thirty.
You haven't moved. Neither has it. Alarm. There it is, on that side. Still there at lunch. You blamed
your age. Tried every cream going. But no cream stops a pillow folding your face. A lot of those lines
are pressed in while you sleep. So you can stop them. Night one: clear silicone patches hold the skin
flat, so it can't fold and crease. They seal in moisture, so the top layer stays plump. Nothing goes
under your skin. Morning one: your lines look smoother. Comment PILLOW and we'll send you the link.

### Claim check
- [claim 3] opener: lines pressed in every night while she sleeps, so she can stop them; side sleeper's
  creases no longer fade by midday ("still there at lunch").
- [claim 2 / owner 6] holds the skin flat so it can't fold and crease; seals in moisture so the top layer
  stays plump (owner wording: "hydrated and plump"; narrator says "plump", the visual shows hydration).
- [claim 1 / owner 6] nothing goes under the skin; no needles, no actives (chips).
- [claim 4] "your lines look smoother" by morning; before/after like-for-like.
- "No cream stops a pillow folding your face": about the fold, not a claim about creams' ingredients.
- Not used anywhere: collagen/elastin, "repairs", studies, numbers, durations ("7 hours", "8 hours"),
  permanent/forever, credentials, price, guarantee, Black Friday, fall-off objection, "11s", mirrors.
  Clock stamps are times of night, never a stated duration.
- Patch shots (20–25, 19): Face Set facts only; PATCHES block verbatim, Elements for shape; clear,
  never white; forehead tab DOWN; slim crescents under the eye, never circles; Pixar patches follow the
  same rules.

## 5. The turn, explained

The patches don't interrupt the story; they answer the exact thing the timeline just showed: once she
sees the fold is pressed in at night ("So you can stop them"), the next night of the same timeline
starts with something that keeps that fold from forming, so the product arrives as the next scene, not a
pitch.

## 6. Word count and timing

- **133 spoken words** (counted on the clean VO text).
- At config `words_per_second` 3.0: **≈44 s** of speech; plus ~1.3 s of chapter gaps, the ~1.5 s silent
  sheet beat (shot 19) and a ~1 s end-card hold → **≈46 s total** ("about 45", owner). The budget formula
  45 × 3.0 = 135 words minus room for the silent beats gave the ≈130 target.
- If Lara reads slower than 3.0 w/s (lessons §5 says ElevenLabs reads ~2.9), the first trims are "Same
  side, every night." (−4 words) and "You haven't moved." (−3), never the mechanism lines. Never a sped-up
  voice beyond the config's whole-clip ≤1.08×.

## 6b. Hypothesis

**Tests:** whether a Pixar-style see-through explainer with a clock-stamped night timeline (format
variable) holds cold P2 viewers better than talking-head formats. **Decides it:** hook rate (3-s views
÷ plays) and average watch %, with engagement rate (likes + comments + shares + saves ÷ views) and
PILLOW comments as the intent signal, each vs the TOF median (config `learning`).

## 7. Caption and hashtags

Your pillow folds the skin by your eye, every night, on the same side. That's why one side looks worse.
The Wrinkle Smooth Face Set by The Daily Glow Co. Comment PILLOW and we'll send you the link.
#sidesleeper #sleepwrinkles #wrinklepatches #skincareover35 #thedailyglowco
(Platform AI-content label on.)

## Open questions for the owner

1. **Problem/answer split is ~66/34, not 80/20.** The owner's requested technical explanation (flat +
   sealed + nothing under the skin) needs ~10 s; holding 80/20 at 45 s would leave one line. Keep, or
   cut to the "flat" line only?
2. **Spoken brand name:** brand is on screen (box from 0 s, end card) and in the caption, not spoken, to
   stay near 45 s. Say it in the VO instead (+~3 s)?
3. Shot 22 shows her sleeping with patches on (Pixar, as a mechanism view). Lessons ban a posed silent
   lying-down *application* shot; this isn't application, but flag if you want it as a cross-section only.

# Story review — run 2026-11-08-0230 — slot 2-T (P2, The Proactive Problem-Solver)

Stage 4 (story-reviewer), round 1. Read: `CLAUDE.md`, `.claude/agents/story-reviewer.md`, `brief.md`
(incl. "Owner instructions for this run", which override the rest), `format.md`, `story.md`,
`docs/lessons-learned.md` (all), `pipeline/config.yaml`, `docs/creative-strategy.md` (§1–4),
`learning/playbook.md` (nothing RETIRED), `learning/production-log.md` (tail), and
`learning/swipe-file/2026-11-08-resilia-skeleton-14-day-timeline.md`. No credits spent.

Decisions taken before this review (given, not scored as defects): (1) the ~66/34 problem/answer split
is accepted because of the owner's requested technical explanation; (2) brand on screen and in the
caption, not spoken; (3) shot 22 (Pixar, asleep wearing patches) may stay, checked below.

## Verdict: **APPROVED**

Every score is ≥ 8, the three hook scores and Shareability reach `review.min_hook_score_tof` (9), and
claims are clean. The "Carry-forward requirements" at the end are not story defects; they are binding
notes for the storyboarder (stage 5) and prompt-engineer (stage 6), and the prompt-reviewer should check them.

## Owner requirements (hard checks)

| Requirement | Result | Note |
|---|---|---|
| ~45 s | PASS | 133 words; ≈46 s planned at config 3.0 w/s. At Lara's ~2.9 w/s it is ≈47.5 s; the named trims ("Same side, every night.", "You haven't moved.") and ≤1.08× bring it back to ~45. |
| Voiceover only, nobody mouths words | PASS | One narrator; "jaw closed, never talking" on every P shot; photoreal lips closed or out of frame (11, 12, 26, 27). Shot 10 "eyes wide (jaw closed)" stated. |
| Every sequence a distinct still | PASS | 29 shots, each its own still. Shot 26 reuses shot 11's framing by design (before = yesterday), and 29 reuses 28's hero asset as the CTA card background: both are deliberate and still get an approved still each. |
| Animated shots "Pixar style" | PASS | Every animated shot marked **P** with the lessons §0 definition. |
| Mechanism in approved wording only | PASS | "hold the skin flat, so it can't fold and crease" / "seal in moisture, so the top layer stays plump" / "Nothing goes under your skin" / chips NO NEEDLES · NO ACTIVES / "your lines look smoother". No collagen, elastin, repair, numbers, studies or "7 hours"; clock stamps are times, not durations. |
| TOF-U job | PASS | Cause she didn't know (pillow fold), mostly problem, patch as the answer, box in frame from 0 s, brand on screen + caption, keyword CTA. |
| Hook a question in the first seconds, motion in frame one | PASS | "Why are your wrinkles worse on one side?" 0–2.7 s; the flop onto the pillow is frame one; 8-word hook text; changes at 1.3 s. |
| One idea, ends in this video | PASS | Pillow fold → stop the fold. NIGHT 1 → MORNING 1 closes inside; no part 2. |
| Claims per lessons §2 | PASS | See item 8. |
| Face Set facts per lessons §1 | PASS | Forehead tab DOWN between the brows (shot 20), slim crescents, clear never white, PATCHES block + Elements for every patch shot including Pixar. |
| Copies Resilia's structure, not words/claims | PASS | Dated ladder flipped onto the problem (clock stamps), inside-the-body cross-section, "age" reframe rewritten ("You blamed your age"), pack ambient early. None of their lines, claims, guarantee/scarcity/emotional close carried over. |

**Shot 22 check (decision 3):** lessons §0 bans a posed, silent lying-down shot *for application*
("Applying them should look organic… never a posed, silent lying-down shot"); §8 has no rule on it.
Shot 22 is an asleep, animated mechanism view, not an application, and no one talks or smiles. It
breaks no written rule in lessons §0 or §8. (The brief's must-avoid line is worded more strictly, "a
posed silent lying-down 'wearing' shot", but the owner has ruled that this shot stays.) Keep it reading
as the mechanism: eyes closed, lips closed, face into the pillow, see-through skin by the eye visibly
flat. No pose to camera and no glamour lighting.

## Scores

| # | Item | Score | Reason |
|---|---|---|---|
| 1 | Hook is a question, within 5 s | 10 | Question fully spoken by 2.7 s, motion in frame one, 8-word text. |
| 2 | Hook fits the persona | 9 | It's her paired angle (2: one side / pillow) and her own detail (lines at the outer eye, deeper on her sleeping side). Her own words come at 20 s ("tried every cream going"), not in the hook. Any side sleeper would care, but that is the slot's angle. |
| 3 | Hook makes sense cold | 9 | Plain question with no context needed, paid off at 25 s ("pressed in while you sleep"). |
| 4 | Body digs in | 9 | The clock ladder makes the cause visible step by step; specific details ("same side, every night", "still there at lunch", the cream shelf). |
| 5 | Smooth turn | 9 | "So you can stop them" → she reaches for the box → silent sheet beat → NIGHT 1. The product arrives as the next scene; no banned transition. |
| 6 | Logic | 9 | Fold → crease → still there at noon → creams sit on top, fold forms anyway → patch keeps it flat → smoother morning. No holes. |
| 7 | Subtle CTA | 9 | "Comment PILLOW and we'll send you the link" on its own full-screen beat. |
| 8 | Claims | 10 | All in APPROVED CLAIMS 1–4 and owner item 6; no credential, statistic, study, duration, price, guarantee or "permanent". "No cream stops a pillow folding your face" is about the fold, not about ingredients. |
| 9 | Stage job / stands alone / length / strategy fit | 8 | Does the TOF-U job and moves the opener belief with belief 1 as the answer (strategy §2 allows this). Product spoken from ~63%, which is accepted (decision 1). ~46–48 s raw. |
| 9b | One idea | 8 | One idea (the pillow fold, then stop the fold). The moisture line adds a second mechanism half, but the owner asked for it and it serves the same morning payoff. |
| 9c | Would she believe it | 8 | The cartoon is obviously a cartoon, so it reads as an explainer, not a fake result. The before/after is like-for-like and softened, not erased. Keep it that way (see C5). |
| 10 | Lessons learned | 8 | No listed mistake in the story itself. Three scenes invite known failures if prompted naively (in-scene text, a bathroom mirror, a re-rendered box); fixes are in C2–C4. |
| 11 | Producible | 8 | Simple one-action stills, mostly code motion. One real risk: a clear patch on a "glass-like" clear skin layer will be invisible (lessons §8 "clear silicone invisible"). Fix in C1. |
| — | **Shareability (TOF)** | 9 | Weird-but-warm Pixar see-through format plus "which side do you sleep on?" is natural comment and send-to-a-friend material. |

## Carry-forward requirements (binding for stages 5–6; prompt-reviewer checks them)

1. **Patch vs translucent skin (shots 20–25, 22):** give the Pixar skin layer a soft warm tint (translucent
   peach/rose, not colourless glass) so the clear patch reads on top of it by its thin raised edge and
   satin sheen. In cross-sections, draw the skin layer as a warm tinted band and the patch as a clear
   layer with a bright edge highlight. Never make the patch white or coloured to make it visible.
   PATCHES block + Elements still apply; forehead tab DOWN; slim crescents, never circles.
2. **No in-scene text from the model:** the clock (shots 7, 9) shows a blank glowing display or a face
   with no legible digits; the times come only from the code cards (2:00 AM, 4:30 AM). Shot 13's candle
   is a plain candle (no "38" number candle), or the number is composited in code.
3. **No mirror (shot 14):** the cream shelf is a close-up of an open bathroom cabinet shelf or a
   bedroom dresser top, framed so no mirror can appear; write "no mirror in the shot" in the prompt.
4. **Box in Pixar shots (1, 7, 18):** never let the model re-render the box text. Pass the real box asset
   (`0f24791e…`) and keep the box small or angled, or composite the real box image in code. Shot 18's
   reach must end with the box fully in hand (unambiguous end frame).
5. **Before/after (26–27):** build 26 from shot 11's approved still, and 27 as a softening edit of it
   (production log, confirmed fix): same framing and light, lines about two-thirds as visible, every line
   still traceable.
6. **Shot 20 state list:** forehead piece already on, one under-eye crescent going on from the centre
   outward, every other piece named as on or off (a piece the prompt does not mention is not on her face).
   State in shot 22 which pieces she wears (whole Face Set: forehead + 2 under-eye + 2 smile-line, lips uncovered).
7. **Length:** time the Lara read first; if it runs over ~47 s, apply the script's named trims before
   any speed-up, and never cut the mechanism lines.

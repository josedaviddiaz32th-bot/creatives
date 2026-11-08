# Story review: run 2026-11-08-0909, "The Problem / Vs… / The Solution" (P3, trend remake)

Stage 4 (story-reviewer). I read `learning/owner-feedback.md` first, then `CLAUDE.md`, `.claude/agents/story-reviewer.md`,
`brief.md`, `format.md`, `story.md`, `docs/lessons-learned.md` (in full), the swipe file
`learning/swipe-file/2026-11-08-ugc-problem-vs-solution-car.md` and the playbook (it has no RETIRED element this
story uses). I watched the reference frame sheet (2 fps).

**Rules for this review (owner's trend remake, they override the agent file):** 15.07 s, the three captions
and timings ("The Problem 😭🛏️" / "Vs…" / "The Solution 🤤❤️"), the 10-cut rhythm, the same vibe and story, no
speech, sound added by the owner. No hook question, no CTA beat and no 30–50 s band; the keyword SLEEP goes in
the posting caption. The calm, eyes-closed face replaces the smile (lessons §0/§4). These are not defects.

## Verdict: **REVISE** (small, surgical: 6 fixes, no change to concept, captions, timings or cut points)

The concept is right and is the same story with the same feel: a relatable, slightly funny misery → the
caring partner brings the fix → cosy bliss. The product turn is the trend's own punchline; claims are clean.
It fails on three things that would cost credits or the hook: the Problem shot packs five actions into one
3.27 s clip and shows the creases late; shot 2 makes the video model draw and open the box (a hard rule:
the real box is never re-rendered); and shot 9 puts her cheek back on the pillow, which muddles the payoff
and the patches.

## Scores

| # | Item | Score | Reason |
|---|---|---|---|
| 1 | Hook lands fast (trend rule: caption + moving face in frame one; the problem must read ≤2 s) | 7 | Frame one moves and the caption is right, but the creases only appear at 1.0–2.0 s; the first second is a face in a pillow that reads as "asleep", not "problem" |
| 2 | Hook fits the persona | 8 | A 20-something panicking at lines on her own face is P3's "surprise/reaction" (angle 3) exactly |
| 3 | Makes sense cold | 7 | Risk of reading as "she's crying because she's tired". It works only if the creases are big, lit and touched early (fix 1) |
| 4 | Body digs in (the build) | 8 | Box → insert → apply → tuck → doze maps one-to-one onto the reference's build |
| 5 | Smooth turn | 9 | The box arrives the way the body pillow does; "Vs…" frames it as contrast, not a pitch |
| 6 | Logic | 7 | Problem = face squashed into the pillow; shot 9 ends with her cheek on the pillow again, so the viewer's last close look repeats the cause (fix 4) |
| 7 | CTA (trend rule: none on screen, SLEEP in the post caption) | 8 | Correct under the owner's rules |
| 8 | Claims | 10 | Nothing spoken or shown beyond the three captions; the implied idea ("stops the creases you press in every night") is approved in §2; no morning reveal, no result claim |
| 9 | Stage job / stands alone / length | 9 | TOF, problem-led hook, brand visible (box in shots 2 and 10), one closed idea, 15.07 s by owner override |
| 9b | One idea | 9 | Pillow creases → patches overnight. Nothing else |
| 9c | Would she believe it? | 8 | Couple POV UGC with a boyfriend tuck reads as real life; keep it unpolished and handheld |
| 10 | Lessons learned | 7 | Shot 2 has the model render and open the box (§7, owner Nov 8); shots 4–5 are hand-to-face actions crammed into 0.43 s and 0.8 s (§8 "hands deform", "one action per shot") |
| 11 | Producible | 6 | Shot 1 = asleep → lift → touch → look at fingers → look at lens → cry → flop: too many actions for one Kling clip, and models smooth the creases away; lid flip has no real interior asset |
| — | Shareability (TOF) | 8 | "Send this to him" / tag-your-boyfriend is built in, as in the reference |
| — | Same story, same feel as the reference | 8 | Yes: misery → caring build → bliss; daylight → lamp light; the throw kept on purpose |

## Fixes (numbered, concrete)

**1. Shot 1 (0–3.27 s): make the crease problem readable by ~0.7 s and cut it to three beats.**
Problem now: creases first show at 1.0–2.0 s, and the shot has five actions. Rewrite:
- 0–0.7 s: close mid-shot (her face at least ⅓ of the frame width), she is already lifting her face off the
  white pillow toward the lens, groggy; **deep red pillow-crease lines run diagonally across her cheek and up
  to her forehead, lit by raking daylight from the blinds** so they cast tiny shadows.
- 0.7–1.9 s: one fingertip traces the longest crease on her cheek; her eyes widen at the lens.
- 1.9–3.27 s: her face crumples into a dramatic whiny cry (no words) and she flops back into the pillow.
Drop "looks at her fingers, then the lens". Write in the state list: "the crease lines stay deep and red for the
whole clip; they do not fade or smooth" (models airbrush, §8). His stubbled jaw stays soft at frame-left. This
makes Alternative B the main cut, inside the same 3.27 s and the same caption.

**2. Shot 2 (3.27–4.37 s): the real box, never drawn or opened by the model.**
Problem now: "drops the real Face Set box… then flips the lid open" means Kling renders the box text and an
interior we have no asset for. Rewrite: "Evening, same bed; she sits against the headboard in the grey crewneck.
His hand sets the closed Face Set box down on the duvet beside her, front label to camera, and lets go."
Production note for the storyboarder: camera locked for this shot; generate the hand placing a plain, blank,
same-size box, then composite the real `face-set-box-v1.png` over it in code (or, if tracking is a risk, a still
with the real box composited and a code push-in, with his hand already withdrawing at the frame edge). No lid flip.

**3. Shots 3–5 (4.37–6.0 s): one action each, readable at 0.4–0.8 s.**
- Shot 3 (0.40 s): keep the backlit clear film with the five pieces in his fingers, but **no box in frame**
  (so no box render). Forehead piece on the film with the tab down.
- Shot 4 (0.43 s): end-state of the press: **her palms slide outward off her forehead and reveal the clear band,
  tab pointing DOWN between the brows.** The band must be visible for the last ~0.25 s; palms covering it the
  whole time reads as "hands on face".
- Shot 5 (0.80 s): **one action only: wearing the full set (band + 4 crescents, lips uncovered), she sinks back
  against the pillow.** Drop the fingertip-on-crescent press (a second hand-to-face action in 0.8 s; §8 hands
  deform / patches already on before applying). The band-only → full-set change happens on the cut.

**4. Shot 9 (11.83–13.6 s): keep her face off the pillow.**
Problem now: "cheek resting lightly on the pillow" repeats the Problem's cause in the payoff and presses the
smile-line crescent into the pillow (patch shifts/deforms, §8). Rewrite: "Lower side angle: she lies on her back,
head sunk into the pillow, face turned up toward the lens, nestled deep in the throw pulled to her chin; nothing
touches her face; patches lying flat." The contrast (face crushed in → face up and smooth) now closes the story
visually, with no claim.

**5. Shot 8 (10.0–11.83 s): give the bliss one tiny visible cue, since there is no smile.**
Add: "she lets out one slow contented exhale and her shoulders melt into the throw; lips stay softly closed."
A motionless sleeping face under "🤤❤️" can read flat; a small settle reads as bliss at phone speed.

**6. Continuity lines for the two people (add to the state list).**
- **Her:** same honey shoulder-length hair, small gold studs and grey crewneck in all shots, shot 1 included
  (hair loose and messy in shot 1; in the claw clip, off the forehead, from shot 2 on). Bare face in shots 1–3,
  no creases from shot 2.
- **Him:** the same navy T-shirt sleeve and forearm (same skin tone, no watch or jewellery) in shots 2, 3 and 6;
  only his stubbled jaw in shot 1; his face is never the subject. Exactly two hands with five fingers in each shot.

## Checked and fine (no change)
- Captions, timings and the 10 cut points match the reference exactly; 🛏️ for 🚙 is the decided swap.
- No speech, no mouthing with patches on; the shot-1 cry is bare-faced (an open mouth with no speech is fine,
  owner Nov 8).
- Patches: clear, tab DOWN, slim crescents, lips uncovered, hair off the forehead; no mirror; no model text
  (captions in code; crewneck has no lettering); dry, matte skin in patch shots.
- US cues (blinds, switch plate, queen bed, college crewneck, fairy lights in November) are right.
- Shot 10's box is composited from the real file: keep it.
- Note for the publisher (not a story fix): lessons §10C says business accounts can't use most trending songs;
  the owner adds the sound in-app, so check the account type can use it before posting.

---

## Round 2 (story.md v2): **APPROVED**

I re-read the whole of story.md v2 under the same trend-remake rules. The captions, timings and the 10 cut points are unchanged and still match the reference. All six fixes are in.

| # | Item | R1 | R2 | Reason |
|---|---|---|---|---|
| 1 | Hook lands fast (caption + moving face; the problem reads ≤2 s) | 7 | 9 | The deep red creases, lit from the side, read by about 0.7 s, and the finger-trace points at them |
| 2 | Fits persona | 8 | 8 | Unchanged; it's P3's "surprise/reaction" |
| 3 | Makes sense cold | 7 | 8 | Big lit creases, the touch and the 🛏️ make "pillow did this to my face" read without words |
| 4 | Body / build | 8 | 8 | Same build as the reference |
| 5 | Smooth turn | 9 | 9 | Unchanged |
| 6 | Logic | 7 | 9 | She starts with her face crushed into the pillow and ends face up with nothing touching her face, so the story closes visually with no claim |
| 7 | CTA (trend rule) | 8 | 8 | SLEEP is in the post caption |
| 8 | Claims | 10 | 10 | Nothing spoken or shown; the implied idea is within §2 |
| 9 | Stage job / stands alone / length | 9 | 9 | 15.07 s by owner override; brand visible in shots 2 and 10 |
| 9b | One idea | 9 | 9 | |
| 9c | Believable | 8 | 8 | |
| 10 | Lessons learned | 7 | 9 | The model never draws the box (it's composited in shots 2 and 10). One hand action per shot. Tab down, creases locked, hands counted |
| 11 | Producible | 6 | 8 | Shot 1 is now three beats. Shot 2 has a fallback (a still plus a code push). Shots 3–5 each have one action |
| — | Shareability | 8 | 8 | It's built for "send this to him" |
| — | Same story and feel as the reference | 8 | 9 | It follows the same arc: misery → caring build → bliss |

**Notes for the storyboarder (not blockers):**
- Shot 8 says "her face on the pillow". Keep it like shot 9: she's on her back, the pillow is behind her head, and nothing presses on her cheek or the crescents.
- Shot 4 is only 0.43 s. Build its still so the band is fully visible in the end frame, then cut on that frame.
- Shot 2: if the tracked composite slips at all, use the still fallback rather than paying for another clip.
- Publisher: check that the account can use the trending sound (lessons §10C).

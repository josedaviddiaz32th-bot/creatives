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

---

## v3 review (story.md v3 + storyboard.md v3, owner fix): **REVISE (small, text-only; 0 credits)**

Reviewer: story-reviewer (stage 4), independent, strict. Read first: `learning/owner-feedback.md` (newest entries),
lessons §0 (cold-viewer test, no exaggerated reactions, all video), then brief, story v3, storyboard v3,
prompts v3, budget, stills-check, clips-check, video-review (v2 PASS that missed the owner's issues),
production log. **Looked at** the reused assets: C2 at 0/0.7/1.4/3.4/4.2/4.9 s, C3 at 0–0.78 s and its tail
(full-res mouth crops), S1, S2, S4, S5, S10, and the ref sheet. Frames: scratchpad `v3rev/`.

v3 answers the owner's four complaints in the right direction (cause before effect, small reactions, all video,
a like-for-like after). Four things still stop it reading the way the owner described. All fixes are free.

### Owner checks (hard)
| Check | Result |
|---|---|
| **Cold-viewer test** | **Borderline → fix 1 and 2.** See the 1 s / 3 s read below. |
| **Reactions subtle and real** | **Yes.** Shot 2 small frown, shot 3 brows lift + closed-lip smile, shot 9 small smile; C2/C3 neutral. One prompt word risks a mouth breath (prompt review C_BATH_GIVE). |
| **Medium = all video** | **Yes.** Every beat is a clip; the 0.1 s black is a light-switch effect, not a still. |

### Cold-viewer read, first 3.267 s as planned
- **At 1 s** (night 1 0–0.73 + 0.27 s of night 2, sped 2.7–2.9×, "The Problem 😭🛏️"): a girl asleep, face in the
  pillow, **tossing and rolling fast**. A stranger's most likely read: *"she can't sleep / restless sleeper"* (the
  same read as the car reference, which is about not sleeping). The squashed cheek is the point, but the rolling is
  the loudest motion and the stomach roll hides her face. **Cause is visible from frame 1 (ST_NIGHT starts
  squashed), but it is not yet the obvious subject.**
- **At 3 s** (light snaps on, she leans in, fingertip on the frame-left cheek from ≈1.8 s, small frown): *"she's
  looking at lines on her face that the pillow left, and she doesn't like it"*, **only if the lines are visible at
  phone size.** As prompted they are skin-coloured "texture" under a vanity light that "lights her face evenly
  from the front", which flattens texture (same failure as 2-T R12 in the production log), and the clip is std
  (lower res). If the lines don't show, the read is *"girl frowning at her face"* (tired? acne?). Same cheek as
  the pillow side (her right cheek, frame-left) is correct and is what makes cause → effect click.
- **Is 1.43 s of nights enough at 2.8×?** Enough to show *face pressed into pillow*; **not** enough to show
  *night after night*, and a Kling clip that is already asked to be a "fast time-lapse" and is then sped 2.8× in
  code will look like jittery fast-forward, not hours passing. Keep the 1.43 s (the effect needs ≥1.8 s inside the
  3.27 s caption), but make every frame about the squash (fix 1) and carry "hours passed" with light, not speed.

### "Several nights in patches": reads as ONE night as planned
Shots 5 and 7 are the **same C2 clip, same angle, same sitting pose, same throw, same crewneck, 2 s apart**; a crop
and a grade don't make a new night. C2 also shows the lamp **on** in frame, so "lamp off, cool" in shot 7 only
works if the crop excludes the lamp. Shot 6 (C3) is one close-up between them. Net read: *he tucked her in, she
dozed off, close-up*: one evening. Then a next-morning miracle, which is the less believable story.
And a defect: **C3's lips part from ≈0.55 s (teeth visible by 0.70 s)**, not 0.8 s as logged, so the planned
0.00–0.78 out point shows an open mouth with patches on. Closed-lip windows: 0.00–0.50 and 2.45–3.04.

**Optional C_NIGHT3 (4.5 cr, from S10_WIDE): not worth it.** S10 came out at almost S7's angle (stills-check), so
it would read as the same night again, and it has the blank placeholder box on the nightstand (needs a composite
or a crop). If the owner wants a real third night, the better start frame is **S9_LOW (low side angle, face up,
fairy-light bokeh, no box)**, std 3 s = 4.5, but it only fits ≤40 if every clip stays std (see budget below).

### Solution strength
Like-for-like framing, same light, softer not erased, patches off so the smile is allowed: **right idea, believable.**
Two risks: (a) the visible change is mostly *sleep creases gone*, which a skeptic knows fade anyway; the payoff
must also be the **fine lines at the outer eye and the forehead line**, so the BEFORE must show them clearly at
phone size (prompt fix on ST_BATH_BEFORE); (b) at std resolution a "softer lines" change can disappear entirely
(budget fix below). Also, shot 8 (0.30–2.70) and shot 9 (2.33–5.00) **overlap by 0.37 s of source**, so the
hand-lowering repeats after the punch-in: a visible stutter.

### Fixes (exact; storyboard/assembly text, 0 credits)
1. **Shot 1 action (story beat 1, storyboard C_NIGHTS):** replace "rolls, re-buries her face" / "rolls onto her
   stomach" with: *"She stays on her side the whole time: she shifts, nuzzles her face deeper into the pillow so
   her cheek and the skin beside her eye fold against it, pulls the pillow tighter, and settles still, face
   squashed in."* In assembly, end each night segment on ≥0.25 s of the still, squashed face.
2. **Hours passing (storyboard shot 1b):** add *"last 0.3 s of 1b: a cool pre-dawn grade lift (blue → pale grey),
   then the 0.1 s black and the light snap"* so the bathroom reads as the next morning.
3. **Several nights (storyboard shots 5–7), free re-cut using the opener's own time-lapse grammar** (hard cut +
   the same 2-frame exposure flicker between nights):
   - Shot 5 (6.300–7.700): C2 0.00–1.40, night 1, warm lamp. Unchanged.
   - Shot 6 (7.700–8.480): **C3 0.00–0.50 at 0.64× speed** (lips closed; was 0.00–0.78), night 2, dimmer lamp.
   - Shot 7 (8.480–10.000): C2 3.40–4.92, **horizontally flipped**, 1.25× crop that **excludes the lamp**, cool night
     grade + the same pre-dawn lift in the last 0.3 s as 1b. (Flipping is safe: the patches are symmetric, no text
     in frame, and it breaks the "same shot again" read.)
   Story beat list: keep "night 1 / 2 / 3" labels but drop "light changes between nights" as the only cue.
4. **Shots 8–9 split (storyboard):** shot 8 = C_AFTER **0.00–2.40**; shot 9 = **2.40–5.00 at 0.975×** (2.667 s out),
   112% punch-in. No repeated motion.
5. **C_APPLY speed (storyboard shot 4):** 1.5× on two hands pressing patches looks rushed. Use **0.80–2.80 at 1.25×**
   (the band is already on in S4's start frame, so skipping the re-press loses nothing).
6. **Brand (owner question, not a blocker):** v3 shows no brand on screen. The TOF rule is "still shows the brand
   subtly", and I found no owner quote in `owner-feedback.md` that allows skipping the box. Ask the owner; until
   then the posting caption must carry "The Daily Glow Co." and the product name.
7. **Hair colour (note):** honey-brown in the bathroom (built from S1) vs strawberry/ginger in the warm bedroom
   clips (S4/S5/C2/C3). Pull warmth/saturation out of her hair in shots 4–7 in the grade (free).

### Budget and quality (std vs pro), exact numbers
Config default is `video_mode: pro`; std is a deviation. Std is lower resolution, and the two face-detail clips are
where resolution decides whether the lines (before) and their softening (after) show at all.
| Plan | Stills | C_NIGHTS 4 s | C_BATH_GIVE 5 s | C_APPLY 3 s | C_AFTER 5 s | Total | + one still fix (2) |
|---|---|---|---|---|---|---|---|
| v3 as written (all std) | 8 | 6 | 7.5 | 4.5 | 7.5 | 33.5 | 35.5 |
| **Recommended: pro on hook + solution** | 8 | **7** | **8.75** | 4.5 (std) | **8.75** | **37.0** | **39.0 ≤ 40** |
| All std + C_NIGHT3 from S9_LOW (std 3 s) | 8 | 6 | 7.5 | 4.5 | 7.5 | 38.0 | 40.0 (no slack) |
| Pro ×3 + C_NIGHT3 | | | | | | 41.5 | over cap |
**Recommendation:** pro on C_NIGHTS, C_BATH_GIVE and C_AFTER (37.0; 39.0 with one still fix); C_APPLY stays std
(mid-video, motion, sped up); skip C_NIGHT3 and use fix 3. Pro was only preflighted for "5 s start only" (8.75):
**preflight pro 4 s start-only (expect 7) and pro 5 s start+end (expect 8.75) before submitting.**

### Scores (trend-remake rules, as in rounds 1–2)
| # | Item | Score | Reason |
|---|---|---|---|
| 1 | Hook lands fast (motion + cause in frame 1) | 7 → 9 with fix 1 | Frame 1 is the squash; the rolling competes with it |
| 3 | Makes sense cold (cause → effect by 3 s) | 7 → 9 with fixes 1–2 + the ST_BATH_BEFORE light fix | Depends on the lines being visible |
| 2 | Fits persona | 8 | Her habit, her first lines at 23, prevention |
| 4 | Body | 8 | Hand-off → apply → nights |
| 5 | Smooth turn | 9 | Partner arrives with the fix at the ref's cut |
| 6 | Logic | 7 → 9 with fix 3 | One night reads as an overnight miracle |
| 8 | Claims | 10 | None shown; before/after softer, not erased |
| 9 | Stage job / stands alone / length | 8 | 15.067 s; brand question (fix 6) |
| 9c | Believable | 7 → 8 with fixes 3–4 + pro | |
| 10 | Lessons | 8 | No smile with patches, no injury words, no mirror; C3 window violated lips-closed (fix 3) |
| 11 | Producible | 8 | Stomach roll removed (fix 1) |
| — | Shareability | 8 | "Send this to him" kept |
| — | Reaction check | 9 | Small and real throughout |

**To approve:** apply fixes 1–5 to story/storyboard (text only) and the prompt-review v3 FIXes. Fix 6 goes to the
owner as a question. I re-check the edited text only; no new round of credits is needed for this review.

---

## v3 round 2 (story.md / storyboard.md v3 rev 1): **APPROVED** (one wording fix, one box-placement change carried in prompt-review round 2)

Re-checked against the same strict checks. Fixes 1–5 from the v3 review are in, word for word.
- **Cold viewer:** at 1 s she stays on her side with her face squashed into the pillow, in real-time motion sped up in code. The cause is now the subject, not "restless sleeper". At 3 s the light comes in at an angle, the creases follow the pillowcase seam on the same cheek, and the before clip is pro: cause → effect reads. **Pass.** The pre-dawn lift carries "hours passed".
- **Reactions:** small frown with closed lips, mild surprise, small smile with no patches on. **Pass.**
- **All video:** **pass.**
- **Several nights:** three cuts in the opener's time-lapse grammar (flicker, grade, flipped crop with no lamp, pre-dawn lift) now read as 2–3 nights. Not airtight, but believable at phone speed. C3's window is now closed-lip. **Pass.**
- **Solution:** like-for-like framing, softer not erased, pro, no repeated motion. The box is in the after but not the before, which quietly says she used it. **Pass.**
- **Brand:** the main session decided this under lessons §0. That's fine, but tell the owner it was our call, not theirs.

**Fixes:**
1. story.md §4 table, 1 s row: replace `tossing and re-burying her face` with `nuzzling her face deeper into it`.
2. Box placement: move it from the counter to a small wall shelf behind her (see prompt-review v3 round 2). Change the storyboard "Box (rev 1)" line and shots 8–9 to match.

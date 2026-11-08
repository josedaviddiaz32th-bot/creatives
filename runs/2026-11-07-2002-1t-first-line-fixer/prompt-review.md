# Prompt review — run 2026-11-07-2002 — slot 1-T (P1 First-Line Fixer) — Pass 1 (before credits)

Stage 6b (prompt-reviewer), round 1. Read: `.claude/agents/prompt-reviewer.md`, `CLAUDE.md`,
`pipeline/config.yaml`, `brief.md` (full verbatim persona), `format.md`, `story.md` v2,
`story-review.md`, `storyboard.md`, `prompts.json`, `budget.json`, `docs/lessons-learned.md`
§3–8 and §10 (incl. the verbatim PATCHES / REFERENCE ROLES / STYLE blocks),
`learning/production-log.md` (empty). No generation tool called, no get_cost, nothing uploaded.
Viewed read-only (Higgsfield `show_reference_elements` get): Forehead-patch 6375c707 = one clear
band, single subject, tab pointing DOWN; Eye-patches 9d766c06 = one pair of slim crescents,
single subject. Both are correct, single-subject product references.

## Verdict table

| Job | Result | Short reason |
|---|---|---|
| K1_NIGHT_ID | **FIX** | Free right hand and nightstand not tied to the same side of frame (B2's one action may cross her body/face); no five-fingers guard; off-face note only before the PATCHES block |
| K2_POV_GROUP | **FIX** | REFERENCE ROLES says "the only person in this image" in a 5-person shot → friends cloned from her face; "Glasses" can be read as eyeglasses; her face at 1/5 frame width is too small for the 7 s push-in to her frown line |
| K3_SLEEP | OK | |
| K4_PRESS_ON | OK | |
| K5_SHEET_HOLD | **FIX** (small) | Pieces held right beside her cheek + PATCHES block's face placement lines; add the off-face restatement after the block |
| K6_TODAY | **FIX** | Preamble says "The five pieces lie flat on their clear backing film exactly as described below" but nothing below describes a film; only the band is in her hand → model adds a film/sheet or extra pieces; tray state from K1 ("keep everything as placed") leaves five pieces on the tray plus a sixth band in her hand |
| K7_YESTERDAY | OK | (inherits K6's tray fix automatically) |
| CLIP_A | OK | |
| CLIP_B1 | OK | |
| CLIP_B2 | OK | (relies on the K1 fix for the hand/nightstand side) |

**Verdict: FIX** (K1, K2, K5, K6). All four are text-only edits; no cost change.

---

## FIX details

### K1_NIGHT_ID
**What the model would produce:** a front-camera selfie whose left/right is unmirrored (her right
hand on frame-left) with the nightstand on frame-right, as written ("on the right side of the
frame"). Nothing ties her free hand to the nightstand side.
**Why it's wrong for the beat:** K1 is the start frame of B2, whose one action is "her free right
hand reaches to the teal tray on the nightstand… holds it beside her right cheek". If hand and
nightstand are on opposite sides, Kling has to reach across her body and in front of her face in
1.6 s, the classic hand-deformation / hand-through-face failure (lessons §8, checklist B), and
K5 (also "beside her right cheek") would sit on the wrong side of the face. K1 also has two
visible hands but no five-fingers guard.
Also: the off-face clarification comes only *before* the PATCHES block, so the last thing the model
reads about the pieces is face placement. Restating it after the block costs nothing.

**Replacement text:**
1. Directly after `A piece the prompt does not mention is not on her face.` insert:
   `Again, for this image: no piece is on her face; her forehead, under-eyes and smile lines are bare skin, and all five pieces are on the film on the tray.`
2. Replace `Her right hand rests on the duvet.` with:
   `Her right hand rests on the duvet on the right side of the frame, the same side as the nightstand, so it can reach the tray without crossing her body or face. Exactly two hands with five fingers each.`

### K2_POV_GROUP
**What the model would produce:** the verbatim REFERENCE ROLES block tells it "THE CAST PHOTO shows
the only person in this image; keep her face…", then the shot asks for five women. The literal
resolution is five versions of her face (or friends strongly resembling her), which also kills the
"friends look smooth, me?" contrast. "Glasses and a small birthday cake…" can put eyeglasses on
the people. "Her face fills about a fifth of the frame width" ≈ 300 px at 2k; the FILTER | ME
cutaway is a 7 s code push-in to her face with a split on her frown line, so at a fifth the line
will be soft and unreadable after a ~3.5× zoom.
**Why it's wrong for the beat:** the split must show *her* frown line, forehead lines and eye
crinkling clearly, against friends who are visibly different and smoother.

**Replacement text:**
1. After `use it for her face, skin, lines, age, hair and earrings only, not for the setting, light or framing.` insert:
   `She is the only person taken from THE CAST PHOTO. The four friends are different women with their own distinct faces, hair colours and skin tones; none of them resembles her.`
2. Replace `She is centre-right and her face fills about a fifth of the frame width, sharp.` with:
   `She is centre-right and closest to the lens, her face filling about a third of the frame width, sharp; the friends squeeze in around and slightly behind her.`
3. Replace `Glasses and a small birthday cake with candles on the table edge, out of focus.` with:
   `Drinking glasses and a small birthday cake with candles on the table edge, out of focus. Nobody wears eyeglasses.`

### K5_SHEET_HOLD
**What the model would produce:** most likely the right image (the "does not touch her face" line
is good), but this is the frame with the pieces closest to her face, after a block that describes
each piece's position on a face. Nano Banana often resolves that by putting one or more pieces on
the cheek/forehead.
**Why it's wrong:** K5 is B2's end frame; any piece on her face here = a talking clip with a patch
on (banned) and a wrong count on the film.

**Replacement text:** directly after `A piece the prompt does not mention is not on her face.` insert:
`Again, for this image: no piece is on her face; her forehead, under-eyes and smile lines are bare skin, and all five pieces are on the film in her right hand.`

### K6_TODAY
**What the model would produce:** the preamble (copied from K1/K5) says "The five pieces lie flat on
their clear backing film exactly as described below", but nothing below describes a film, and the
job says only the forehead band is shown. Read literally, the model adds a backing film with five
pieces somewhere (her other hand, the nightstand) or puts the crescents on her face. Separately,
"Keep everything as placed in THE CAST PHOTO" keeps K1's tray with all five pieces on the
nightstand while she also holds a band: six pieces, wrong count (checklist A). K7 is an edit of K6,
so both halves of the end card would carry it.
**Why it's wrong for the beat:** TODAY must be bare-faced, after one night, with the one band in her
fingers, and nothing else competing with the face comparison.

**Replacement text:**
1. Replace `Where the pieces are in THIS image: none of them is on her face; her face is completely bare. The five pieces lie flat on their clear backing film exactly as described below, and the face-placement lines of the patch description apply only to the shape of each piece, not to this image.` with:
   `Where the pieces are in THIS image: only the forehead band appears, held in her fingers beside her face. No piece is on her face; her face is completely bare. There is no backing film and no other piece anywhere in the image. The face-placement lines of the patch description apply only to the shape of the forehead band, not to this image.`
2. Directly after `A piece the prompt does not mention is not on her face.` insert:
   `Again, for this image: no piece is on her face; her forehead, under-eyes and smile lines are bare skin.`
3. Replace `nothing is on her face.` (end of the hand sentence) with:
   `nothing is on her face. The teal tray on the nightstand is empty.`

---

## The prompt-engineer's five flags

1. **No studio shot 564c68fa → end-card hold uses a K5 crop.** OK. The storyboard allows it; K5 is
   built from the verified Elements, lamp-lit on a real hand (scale is shown, as lessons §4 asks).
   With the K5 fix the crop shows the five pieces on the film only.
2. **PATCHES block pasted verbatim in K1, K5, K6 with off-face pieces.** Pasting it is correct
   (CLAUDE.md: every product shot pastes it verbatim) and the pre-block note is the right idea. It is
   not safe enough on its own: the block ends on face placement and "A piece the prompt does not
   mention is not on her face" (the pieces *are* mentioned, so it doesn't protect). Fixed above with
   a one-line restatement after the block in K1, K5, K6, and K6's pre-block note corrected.
   Gate A will still catch any slip at 1.5 credits.
3. **Dependent stills priced with a stand-in ID.** OK: price depends on model/resolution/duration,
   not on the media. The producer still preflights each job with its real IDs before submitting
   (`always_preflight`).
4. **No Element placeholders in the Kling prompts.** OK. No clip shows a patch on her face; in B2
   the film is on screen only t 2.2–7.2, small on the tray then lifted, and the end frame K5 (built
   from the Elements) locks its shape. Clip checklist B catches any morphing.
5. **No placement photo, placement from text.** OK. The only patch-on frame is K4; it has the cast
   photo (K1) + two single-subject Elements (lessons §4 step 2) and the full placement text,
   including tab DOWN, two-thirds, not to the hairline, crescents not circles, lips uncovered.
   The worn Face Set image 53be5c97 is Runway-only, and Face-Patch 252769ce is a multi-panel sheet,
   so text placement is the right call.

## Other checks (all OK)

- **Spoken words vs story.md:** A = hook + problem, 29 words, verbatim; B1 = tried + loop, 28 words,
  verbatim; B2 = reveal + answer + CTA, 31 words, verbatim except the case of "photo". All use
  "She says exactly these words, in this order, and nothing else".
- **Fit at 2.3 words/s:** A 12.6 s ≤ 14; B1 12.2 s ≤ 13; B2 13.5 s ≤ 15. Timed beats match the
  storyboard (B2's "So now I sleep in these" pickup at t 4.4 = 0:33.0).
- **Lowercase "Comment photo":** correct (lessons §5/§8: no ALL CAPS in dialogue; emphasis is
  described instead). PHOTO stays in caps only in the code text overlay.
- **Voice description:** identical, word for word, in A, B1, B2, and identical to the continuity sheet.
- **No lips moving with a patch on:** no Kling clip has a patch on; K4 (the only patch-on frame) is a
  silent still with "Lips closed, not smiling". B2 never cuts back to video after the press-on.
- **K7:** restores lines "to exactly the depth, length and placement they have in THE CAST PHOTO,
  never deeper, never more lines… no added redness, shadows or tiredness". Same light/framing as
  K6. Good.
- **Character:** 27-year-old, light olive skin, claw clip, gold huggies, sage T-shirt, lines list:
  word for word in K1; every other still is an edit of K1; friends in K2 "late twenties". Matches
  the brief and continuity sheet.
- **Hair off the forehead:** STYLE block in every still; "nothing falls on her forehead" in every clip.
- **Named light:** K1/K4/K5 warm bedside lamp; K2 string lights + flash look; K3 lamp dimmed; K6/K7
  soft daylight from a window on the right.
- **Guards:** five fingers in K4, K5, all clips (added to K1 above); one action per clip (B2: the
  lift); "Unretouched, no beauty filter, visible pores" + "Her wrinkles do not change during the
  clip" in every clip; K6 "not erased, not airbrushed"; dry/matte, no mirror, no text in every
  still; REFERENCE ROLES first in every multi-image still, STYLE last in every still.
- **Settings:** stills nano_banana_2 9:16 (K2 2k); clips kling3_0, pro, 9:16, sound on, 14/13/15 s,
  start/end frames K1/K1, K1/K1, K1/K5 as storyboarded.
- **Cost:** 116.0 first pass ≤ 120 (135 − 15); 131 with reserve ≤ 135. Fixes add no cost.
- **Claims/words:** "frown lines" (never 11s), "every night"/"all night" (never "8 hours"), no
  statistics, credentials or "permanent". Botox / tretinoin named only as her research.

## Fixes applied (round 1)

Applied by prompt-engineer, text only. No settings, durations, medias or spoken words changed; credits unchanged at **116.0** (131 with reserve). JSON verified valid. K3, K4, K7, CLIP_A, CLIP_B1, CLIP_B2 untouched.

- **K1_NIGHT_ID:** inserted "Again, for this image: no piece is on her face… all five pieces are on the film on the tray." after the PATCHES block; replaced the right-hand line with "on the right side of the frame, the same side as the nightstand, so it can reach the tray without crossing her body or face. Exactly two hands with five fingers each." Storyboard K1 row updated to match (hand on the nightstand side, five-fingers guard).
- **K2_POV_GROUP:** inserted "She is the only person taken from THE CAST PHOTO. The four friends are different women… none of them resembles her." after the cast-photo role line; face size changed to "closest to the lens, her face filling about a third of the frame width… friends… around and slightly behind her"; "Glasses" changed to "Drinking glasses… Nobody wears eyeglasses." Storyboard K2 row updated to match.
- **K5_SHEET_HOLD:** inserted "Again, for this image: no piece is on her face… all five pieces are on the film in her right hand." after the PATCHES block. Storyboard K5 row already matched (no change).
- **K6_TODAY:** replaced the pre-block placement note with the review's text (only the forehead band appears, in her fingers; no backing film and no other piece; placement lines apply only to the band's shape); inserted the bare-skin restatement after the PATCHES block; added "The teal tray on the nightstand is empty." after "nothing is on her face." Storyboard K6 row updated (only piece in the image, no film, tray empty).
- **K7_YESTERDAY (check only):** prompt not changed. It edits K6 with "Keep everything as placed in THE MORNING PHOTO" and removes the band and hand, so it inherits the empty tray and "No patches, nothing in her hands" still reads correctly. Storyboard K7 row now notes the tray stays empty as in K6.

---

## Round 2 — Verdict: **FIX**

Prompt-reviewer, round 2 (revision 1 of `review.max_prompt_revisions` = 2). Re-read `brief.md`, `story.md` v2, `storyboard.md`, `prompts.json`, `budget.json`, `pipeline/config.yaml`, lessons §3–8 and §10, `learning/production-log.md`. No generation, no get_cost, nothing uploaded, nothing committed; prompts.json / storyboard.md / story.md not edited.

### Round-1 fixes: all landed exactly
Checked by exact string match in `prompts.json`:
- **K1:** "Again, for this image: … all five pieces are on the film on the tray." sits directly after the PATCHES block; the right-hand line + "Exactly two hands with five fingers each." present; old "Her right hand rests on the duvet." gone.
- **K2:** the cast-photo/four-friends sentence, the "closest to the lens… a third of the frame width" line and "Drinking glasses… Nobody wears eyeglasses." are all present; "a fifth" and bare "Glasses" gone.
- **K5:** restatement after the PATCHES block present.
- **K6:** new pre-block note, the bare-skin restatement after the block, and "The teal tray on the nightstand is empty." all present; old "exactly as described below" gone from K6.
- **Storyboard** K1, K2, K6, K7 rows match the prompts (hand on the nightstand side, a third of frame width, distinct friends, no eyeglasses, the band is the only piece, tray empty in K6/K7).
- Verbatim blocks: REFERENCE ROLES opens all 7 stills, STYLE closes all 7, PATCHES is verbatim in K1, K4, K5, K6 (the patch-visible / product jobs).

### Fresh read, all 10 jobs

| Job | Result | Short reason |
|---|---|---|
| K1_NIGHT_ID | OK | Hand, nightstand, lamp and tray all on frame-right; the off-face restatement now comes last. Consistent with B2's reach and K5 ("beside her right cheek", right hand). |
| K2_POV_GROUP | **FIX** (small) | Five people with arms around each other and no hands guard; group selfies are where extra hands and fused fingers show up, and the full frame is the hook (0:00–0:01.5) |
| K3_SLEEP | OK | |
| K4_PRESS_ON | OK | |
| K5_SHEET_HOLD | OK | Pre-block note ("five pieces on their film") is true for this frame; restatement after the block names the film in her right hand. Matches B2's end. |
| K6_TODAY | **FIX** (small) | "No phone" takes the phone out of her left hand but doesn't say where that hand goes, and there's no fingers guard on a hand pinching a thin band beside her face. K7 is "keep everything as placed" from K6, so a loose left hand ends up in both halves of the end card |
| K7_YESTERDAY | OK | Picks up K6's empty tray correctly; it picks up the left-hand fix automatically once K6 is changed |
| CLIP_A | OK (note) | See note 1 |
| CLIP_B1 | OK | |
| CLIP_B2 | OK | The reach stays on the same side of frame as in K1; the end frame is K5 |

**Verdict: FIX** (K2, K6). Text only; no cost, settings or spoken-word change.

### FIX details

#### K2_POV_GROUP
**What the model would produce:** five women squeezing in "shoulder to shoulder" with no rule on hands. Nano Banana's usual answer is arms around shoulders, with an extra hand on her shoulder or fused fingers on someone's drink.
**Why it's wrong for the beat:** K2 is frame one of the video (full frame, 0:00–0:01.5) and the photo she "filters". A sixth hand is the first thing viewers see. Lessons §8 hands guard; check 5.
**Replacement text:** replace `The friends' skin looks fresh and smooth.` with:
`The friends' skin looks fresh and smooth. Every person has exactly two arms and two hands with five fingers each; no extra hands or arms, and nobody's hand is on her face.`

#### K6_TODAY
**What the model would produce:** an edit of K1 where "No phone" removes the phone. With nothing said about her left hand, the model either leaves an empty hand floating at chest height in the K1 pose or invents something to hold. The right hand's thumb-and-index pinch of a thin clear band beside her temple has no fingers guard, and that's a hand near the face, the main deformation case.
**Why it's wrong for the beat:** TODAY | YESTERDAY has to match like for like with nothing pulling the eye from the face. K7 keeps K6's left hand, so any defect shows up in both halves.
**Replacement text:** replace `No phone.` with:
`No phone: her left hand is lowered out of frame. Only her right hand is visible, with exactly five fingers.`
(K7 needs no change: its "her hand is lowered out of frame" and "nothing in her hands" then match both hands.)

### Notes (no change required)
1. **CLIP_A timing:** the beats put the question at 0.7–4.1 s (3.4 s for 9 words, so 3.9 s needed), but the prompt also says "She starts speaking right at the start of the clip". Read literally, she starts the question at t0 while she glances up, which matches story.md (voice from 0:00.8 = t0, under the K2 POV). Either reading fits the 14 s clip (29 words ÷ 2.3 = 12.6 s). Not a FIX. Producer: at assembly, check that the question has started by 0:01.5.
2. **K6 vs PATCHES block:** the block still describes the under-eye and smile-line pieces in a one-piece frame. The note before the block and the restatement after it cover this; gate A checks the count.

### All 7 checks (re-run)
1. **Picture:** every still matches its storyboard row and state list; the thing to notice is described in each (her frown line in K2, the sleep creases in K3, tab down in K4, five pieces on the film in K5, softer-not-erased in K6, K1-depth lines in K7).
2. **Continuity:** the character text is word for word in K1, and every other still edits K1 (K7 edits K6). K1 = A start/end, B1 start/end, B2 start; K5 = B2 end. Lamp/nightstand/hand all on frame-right in K1, K5 and B2.
3. **Product:** the Elements 6375c707 / 9d766c06 in K1, K4, K5, K6 (K6 only the band); the PATCHES block is verbatim; tab DOWN, two-thirds, crescents, lips uncovered; pieces on her face only in K4. No AI text or brand names.
4. **Speech:** A "Can't take a group photo without filtering your lines? My friends look smooth. Me? Frown lines, forehead lines, crinkling by my eyes. I filter it, feel like a fraud." (29) · B1 "I've researched tretinoin, vitamin C, peptides, even Botox of lesser strength. But I'm scared it'll look unnatural. Ever notice your lines look worst right when you wake up?" (28) · B2 "A lot of them get pressed in every night. So now I sleep in these. They hold my skin flat all night. Comment photo and I'll send you what I use." (31). All match story.md word for word, in order; the only difference is "photo" in lowercase, which is deliberate (no ALL CAPS, lessons §5). Fit: 12.6 ≤ 14, 12.2 ≤ 13, 13.5 ≤ 15. The voice description is identical in all three clips and matches the continuity sheet. No speech with a patch on; "only her voice and quiet room tone" in all three.
5. **Guards:** five fingers in K1, K4, K5 and every clip (K2 and K6 fixed above); one action per clip; "unretouched / no beauty filter / visible pores" and "her wrinkles do not change" in every clip; light named in every still; no mirror; dry and matte; no peel shot.
6. **Settings/cost:** stills `nano_banana_2` 9:16 (K2 at 2k); clips `kling3_0` pro, sound on, 9:16, 14/13/15 s, start and end frames as storyboarded. 116.0 ≤ 120 (135 − 15); 131 ≤ 135. The fixes add nothing.
7. **Claims:** "frown lines" (never "11s"), "every night/all night" (never "8 hours"), no statistics, credentials, reviews or "permanent".

## Fixes applied (round 2)
- K2_POV_GROUP: added the hands guard for all five people, as given.
- K6_TODAY: "No phone." replaced with the left-hand-out-of-frame line, as given. K7 inherits it.

---

## Round 3 — Verdict: **PASS**

Prompt-reviewer, round 3 (the last round: both `review.max_prompt_revisions` = 2 revisions are used). Re-read `brief.md`, `story.md` v2, `storyboard.md`, `prompts.json`, `budget.json`, `pipeline/config.yaml`, lessons §3–8 and §10, `learning/production-log.md`. No generation, no get_cost, nothing uploaded, nothing committed. prompts.json, storyboard.md and story.md were not edited.

### Round-2 fixes: both landed exactly
- **K2_POV_GROUP:** "The friends' skin looks fresh and smooth. Every person has exactly two arms and two hands with five fingers each; no extra hands or arms, and nobody's hand is on her face." is present word for word, in place of the old sentence. It doesn't conflict with "squeeze in shoulder to shoulder" or with the round-1 lines about the friends' distinct faces and her being closest to the lens.
- **K6_TODAY:** "No phone: her left hand is lowered out of frame. Only her right hand is visible, with exactly five fingers." is present word for word, in place of "No phone.". It's followed by the unchanged right-hand pinch of the band at temple height, "nothing is on her face" and the empty tray.
- **No contradictions:** K7 edits K6 ("Keep everything as placed in THE MORNING PHOTO") and removes "the clear forehead band and her right hand… (her hand is lowered out of frame)… nothing in her hands". So K7 ends up with no hands in frame, no phone and an empty tray. K6 and K7 are still like for like: same morning window light from the right, framing, camera distance, expression, eye line, T-shirt, hair and earrings. The only differences are the band in her right hand (K6) and the line depth (K7 = K1). This matches the storyboard's K6/K7 rows and the story's end card.

### Fresh read, all 10 jobs

| Job | Result | Note |
|---|---|---|
| K1_NIGHT_ID | OK | |
| K2_POV_GROUP | OK | |
| K3_SLEEP | OK | Producer note 3 |
| K4_PRESS_ON | OK | |
| K5_SHEET_HOLD | OK | |
| K6_TODAY | OK | Producer note 1 |
| K7_YESTERDAY | OK | Producer note 2 |
| CLIP_A | OK | Producer note 4 |
| CLIP_B1 | OK | |
| CLIP_B2 | OK | Pass 2 note 5 |

**Verdict: PASS.** No text changes. The stills can go to generation and gate A.

### The 7 checks
1. **Picture:** every job matches its storyboard row and state list. The thing to notice is written into each one: her frown line at a third of the frame width (K2), the pillow creases (K3), the tab DOWN and two-thirds coverage with lips closed (K4), the five pieces on the film beside her cheek (K5), the band as the only piece with lines softer but not erased (K6), K1-depth lines and never deeper (K7). Nothing extra is asked for: K2 has no eyeglasses and no product, and every still is "No text, captions, logos or watermark".
2. **Continuity:** the character text is word for word in K1, and every other still edits K1 (K7 edits K6, with K1 as the line reference only). The frames chain correctly: K1 → A start/end, B1 start/end, B2 start; K5 → B2 end. The free right hand, the nightstand and the lamp are all on frame-right in K1, K5 and B2. The tray state is right in every frame: full in K1/K3, empty in K4/K5/K6/K7.
3. **Product:** the Elements 6375c707 / 9d766c06 are in K1, K4 and K5, and only the band (6375c707) is in K6. The PATCHES block is verbatim, with the off-face notes before and after it in K1, K5 and K6. Tab DOWN, two-thirds, crescents, lips uncovered. Pieces are on her face only in K4 (a silent still). All brand text is in code.
4. **Speech:** A (29 words), B1 (28) and B2 (31) match story.md word for word and in order. "photo" is lowercase on purpose (lessons §5). Each uses the "She says exactly these words…" form, and the voice description is identical in all three and matches the continuity sheet. Fit: 12.6 ≤ 14, 12.2 ≤ 13, 13.5 ≤ 15. She never speaks with a patch on, and every clip has "only her voice and quiet room tone".
5. **Guards:** five fingers are in K1, K2, K4, K5, K6 and every clip. One action per clip. "Unretouched / no beauty filter / visible pores" and "her wrinkles do not change" are in every clip, and K6 has "softer… not erased, not airbrushed". Every still names its light. No mirror, skin dry and matte, no peel shot. REFERENCE ROLES opens all 7 stills and STYLE closes all 7.
6. **Settings/cost:** stills are `nano_banana_2` 9:16 (K2 at 2k, the rest 1k), with no multi-panel references. Clips are `kling3_0` pro, sound on, 9:16, 14/13/15 s, start/end frames as storyboarded. The budget is unchanged: **116.0** first pass ≤ 120 (135 − 15); 131.0 with the reserve ≤ 135. Producer: preflight each job with its real IDs (`always_preflight`).
7. **Claims:** "frown lines" (never "11s"), "every night / all night" (never "8 hours"), no statistics, credentials, reviews or "permanent". Botox and tretinoin are named only as her own research.

### Producer notes (gate A / assembly / Pass 2). None of these needs a prompt change
1. **K6 (gate A):** the band and her fingers must sit *beside* her face and must not cover her outer eye corner, temple crinkling or forehead lines. Those are the lines the YESTERDAY | TODAY comparison is about. Also check that exactly one piece is in the image (no film, nothing on her face, the left hand out of frame). If any of this fails, edit K6 before K7 is made, because K7 inherits it.
2. **K7 (gate A):** check it side by side with K1 and K6 (storyboard review note a). The lines must be at K1 depth and never deeper, the light must be morning window light (not K1's lamp), and no hand or band should be left behind.
3. **K3 (gate A):** it has no hands guard. One isn't needed while the duvet is up at her shoulder and no hand shows, but if a hand does show by her face on the pillow, count the fingers.
4. **CLIP_A (assembly):** the prompt's gesture beats are tighter than the spoken words in places ("My friends look smooth. Me?" in 4.3–6.0 s; the last sentence in 11–13.5 s). Kling will set its own pace. Re-time the code cuts and overlays (0:05.6 cutaway, 0:12.6 return, text at 0:09.0 / 0:12.6) to the actual audio. Confirm that the question has started by 0:01.5, as noted in round 2, and that "…feel like a fraud." finishes before t 14.
5. **CLIP_B2 (Pass 2):** after gate A, check K5's actual hand and film position against the B2 lead action ("beside her right cheek toward the lens"), and check that K5's left hand still holds the phone low, before the video credits are spent.

No new problem was found, so nothing was added to `learning/production-log.md`.

---

## Pass 2 (real stills) — Verdict: **FIX** (applied; text only, now ready)

The prompt-reviewer looked at all 7 approved stills: K1 `91d6abc0`, K2 `91d09592`, K3 `f0d61ae3`, K4 `02a0082c`, K5 `4576bff3`, K6 `fe37523b` and K7 `d21e9014`, then re-read CLIP_A, B1 and B2 against them. No credits were spent, and nothing was generated, priced or uploaded. story.md is untouched. A backup of the earlier prompts.json is in the session scratchpad (`prompts.pre-pass2.json`).

| Job | Start / end | Result | What was wrong vs the actual still | Change made |
|---|---|---|---|---|
| CLIP_A | K1 / K1 | **FIX → fixed** | (1) At t 0–0.7 the prompt said she "glances from the phone… up to the lens", but K1 already has her eyes on the lens, so Kling would have to invent a look-down first. (2) "Left hand / right hand" is ambiguous. In K1 the phone hand is on frame-left, which is anatomically her right hand, so Kling may read "left/right" the other way. (3) It named a "claw clip" that isn't visible, since her hair is slicked straight back, which invites Kling to add one. (4) It said "earrings" without saying which. | Wired the real IDs. Hair line now reads "pulled fully back off her forehead exactly as in the start frame". Earrings are now "small gold hoop earrings". Added: "Sides are as seen in the frame: her phone is in the hand on the frame-left side, held at chest height; her free hand rests on the duvet on the frame-right side, next to the nightstand." t 0–0.7 now reads "already looking into the lens, as in the start frame, and draws a small breath". The 13.5–14 s settle names both hands by frame side. |
| CLIP_B1 | K1 / K1 | **FIX → fixed** | It had the same side and hair problems. The counting hand was never sent back to the duvet, so the end frame had to snap it back in 0.2 s. | Same shared fixes. 0–4.8 s: "lifting her free frame-right hand from the duvet… the phone hand stays still". 4.8–7.7 s: "the free hand lowers back to rest on the duvet on the frame-right side". The 12.8–13 s hold names both hands by frame side. |
| CLIP_B2 | K1 / K5 | **FIX → fixed** | "Her free right hand… beside her right cheek" could be read anatomically. That would be the phone hand on frame-left reaching across her body and face to the tray on frame-right (production-log K1→B2 risk). In K5 the film is held by the frame-right hand beside her face at cheek-to-eye height, and the tray is bare. The prompt never said the tray ends empty. | Same shared fixes. The lead action now reads: free hand on the frame-right side "reaches straight to the teal tray on the nightstand beside it (never crossing her body or face)… holds it up still beside her face on the frame-right side, at cheek-to-eye height, pieces facing the lens, exactly as in the end frame; the teal tray is left bare and empty and stays where it is". The phone is "still at chest height in the frame-left hand". |

**Unchanged and checked:** the spoken words are word for word story.md in all three clips ("photo" is lowercase on purpose). The voice description is identical in all three. Durations are 14/13/15, settings are kling3_0 pro, sound on, 9:16, and the cost is unchanged (105). The light is a warm lamp at frame-right in K1 and K5. Wardrobe is the sage T-shirt and oat duvet. K1's tray has 5 pieces (band plus 4 crescents) and K5's film has all 5, with the tray bare. Bare face in both, five fingers on visible hands.

**Media wiring:** in the clip jobs, `$K1_NIGHT_ID` and `$K5_SHEET_HOLD` are replaced with the approved generation IDs: A start/end and B1 start/end are `91d6abc0-eb0a-4f1c-bce6-b2a663bbaf69`. B2 start is `91d6abc0-…` and B2 end is `4576bff3-729e-4096-afcc-a16ec4389720`. The still jobs are unchanged.

**Cutaways and end card (storyboard.md updated, no prompt change):**
- K2 still works for the hook and the FILTER | ME push-in. Her face is about ⅓ of the frame width, her frown, forehead lines and crinkles are visible, and the friends look distinct.
- K3 still works for the sleeping push-in, with the full tray and lamp in the background.
- K4 has no tray on the nightstand. That's harmless for a silent cutaway, and the storyboard now notes it.
- K6 and K7: the storyboard rows were out of date ("K7 = edit of K6", "hand out of frame"). They now say:
  - K7 is a relight of K1 and K6 is an edit of K7, both in the same morning light.
  - K7 shows both hands at the bottom edge, plus the lamp edge at frame-right.
  - K6's band is frosted (owner-accepted).
  - The end card's "Same light." now holds by construction.
- Assembly note: align the halves on eye line and crop so K7's bottom-edge hands and lamp edge don't pull focus at the seam.

**Producer:** preflight each clip with the real IDs (`get_cost: true`). Then check B1 and B2 against checklist B, especially that no hand crosses the face in B2 and the tray ends bare.

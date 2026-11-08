# Prompt review, pass 1: run 2026-11-08-0909 "The Problem / Vs… / The Solution"

Stage 6b (prompt-reviewer), pass 1, before any credits. Read first: `learning/owner-feedback.md`, `CLAUDE.md`,
`.claude/agents/prompt-reviewer.md`, `brief.md` (owner section wins), `story.md` v2 (APPROVED), `story-review.md`
(round-2 notes), `storyboard.md`, `prompts.json` (rev 0), `budget.json`, `pipeline/config.yaml`,
`docs/lessons-learned.md` §0 and §3–§10, `learning/production-log.md`, the reference sheet
(`scratchpad/ref-car/sheet.jpg`) and the real box `assets/packaging/face-set-box-v1.png`.

**Trend-remake rules applied** (they override the agent file): no speech anywhere and every clip sound off; a
mouth may open for the cry or an exhale but never mouths words; calm face, no smile, whenever patches are on;
photoreal handheld phone UGC; American bedroom cues; the box is never generated (blank placeholder, real asset
composited in code); all captions in code.

## Verdict: **FIX** (6 jobs; wording only; no cost change)

The prompts are in good shape. Every patch job carries the PATCHES, REFERENCE ROLES and STYLE blocks verbatim
(checked by script against lessons §4). The tab is DOWN in every patch prompt, the pieces per shot are right,
and her continuity line is word for word in S1, S2 and S4–S10. His forearm line is word for word in S2, S3 and
S6. Elements appear only as `<<<id>>>` in the prompt text, and `medias` holds only `$still` IDs and `564c68fa`.
All three clips are `kling3_0` pro, 9:16, sound off, with no speech. Every job is preflighted: 41 credits plus
15 reserve = **56, which is ≤ 60** and well under the 135 cap. The blank placeholder (12 × 19 × 4 cm,
off-white front, teal narrow right side) matches the real box's proportions and 3/4 view, so the composite will
sit right.

The six fixes guard against things a literal model would get wrong:
- a smile with patches on;
- crescents on the band-only frame;
- a head turned onto the pillow;
- a "real product box" drawn into the placeholder;
- a hand frozen mid-action that gives away a still.

## Job table

| Job | Verdict | What the model would produce → why it's wrong → fix |
|---|---|---|
| S1_PROBLEM | OK | Bare face, creases on the frame-right cheek lit from frame-right, lips closed, his soft jaw at frame-left, top fifth plain. The claw-clip deviation is justified (it keeps the forehead creases visible). |
| S2_BOX | **FIX** | (a) The 1.1 s shot holds a still of his fingers "letting go". With code shake only, a hand frozen mid-release is the one place in shots 2–5 that reads as a photo next to the clips. (b) The parenthetical "(a real product box is placed over it later in editing)" splits the verb from its location ("on the duvet beside her hip"), and a literal model may read "real product box" as something to draw. **Replace** the sentence starting `From the frame-right edge his forearm and hand have just set a plain closed rectangular box` and ending `do not cover its front face.` with: `A plain closed rectangular box about 12 cm wide, 19 cm tall and 4 cm deep stands upright on the duvet beside her hip, in the lower third of the frame on the frame-right side, its front face turned toward the lens and angled slightly so its narrow right side shows; the front face is plain matte off-white and completely blank, the narrow side plain dark teal; no print, text, logo, window, picture or product on it anywhere. His hand has just let go of it and is pulling back toward the frame-right edge: his fingertips are a few centimetres from the box, never touching or covering its front face, and his hand and forearm are slightly motion-blurred from the movement while the box and her face stay sharp.` |
| S3_INSERT | OK | One hand, backlit film, exactly five pieces, tab down, no box, and "she is out of frame". The face-free clarifier sits before the PATCHES block (production log 2-T). |
| S4_BAND | **FIX** | The prompt invokes the crescent Element `<<<9d766c06…>>>` in a band-only frame. Production log X23: an Element in the text outweighed a ban sentence, and P20B shows the model completing pieces once one is on. Risk: crescents appear under her eyes. **Replace** `THE SHEET PHOTO is the supplied flat lay of the five clear pieces; <<<6375c707-7ad9-4df9-b7e0-69750993e7aa>>> is the clear forehead band, drawn with its small rounded tab pointing DOWN, and <<<9d766c06-2818-43e8-8ec4-1aac02d63897>>> is a pair of the slim clear crescents; the Face Set has four of these crescents, all the same shape, plus the one band.` with: `THE SHEET PHOTO is the supplied flat lay of the five clear pieces; use only its forehead band here. <<<6375c707-7ad9-4df9-b7e0-69750993e7aa>>> is the clear forehead band, drawn with its small rounded tab pointing DOWN. The four crescents stay on the sheet and are not in this image.` Keep everything else, including the PATCHES block and "Exactly one piece in the whole image." |
| S5_SET | **FIX** | "calm, relaxed and content" invites a soft smile with patches on, which the owner bans. **Replace** `Her face is calm, relaxed and content; lips softly closed; no smile; she does not speak.` with `Her face is calm and relaxed, mouth neutral, the corners of her mouth not raised; lips softly closed; no smile; she does not speak.` |
| S6_TUCK | **FIX** | Same as S5: apply the same replacement to the same sentence. Otherwise OK: S5 is the cast and S2 is used for the sleeve only, three hands, his hand at frame-right. |
| S7_DOZE | **FIX** | Same as S5: apply the same replacement. Otherwise OK: same framing as S6, no hands, lamp dimmer. |
| S8_CLOSE | **FIX** | Same as S5: apply the same replacement. Otherwise OK: on her back, nothing touches the cheeks, built from the wider S7. |
| S9_LOW | **FIX** | (a) Same smile replacement as S5. (b) "phone near mattress height at the side of the bed… her face turned up toward the lens" is ambiguous: to face a lens at mattress height, the model turns her head sideways, which puts her cheek and smile-line crescent into the pillow. That is the exact payoff error story-review fix 4 removed. **Replace** from `CHANGES ONLY: a cosier lower side angle:` through `the patches lie flat.` with: `CHANGES ONLY: a cosier lower side angle: the phone is held at the side of the bed a little above the mattress, about 40 cm above the pillow, tilted down at her face; she lies on her back, the back of her head sunk into the pillow, her face pointing up at the ceiling and turned only slightly toward the lens, so both eyes and all five patches are visible; neither cheek touches the pillow; the throw is pulled up to her chin; nothing touches her face; the patches lie flat.` |
| S10_WIDE | **FIX** | (a) Same smile replacement as S5. (b) Same parenthetical problem as S2. **Replace** `no print, text, logo, window, picture or product on it anywhere (a real product box is placed over it later in editing), standing beside the lamp.` with `no print, text, logo, window, picture or product on it anywhere; it stands beside the lamp, fully visible, not hidden behind the lamp or the glass.` |
| C1_PROBLEM | OK | 4 s (use 0–3.27), start S1, sound off. The hand is named by frame side. The creases are locked ("do not fade, smooth or move"). Wordless cry: open mouth allowed, "she does not talk or mouth words". |
| C2_TUCK_DOZE | **FIX** (small) | Kling drifts toward a contented smile on "nestles… eyes slowly close". **Replace** `No smile.` with `No smile: the corners of her mouth stay level the whole time.` Otherwise OK: S6 → S7 locked, hand counts given, patches locked, face never sideways. |
| C3_EXHALE | **FIX** (small) | "contented exhale" invites a smile on the exact beat that replaces the reference's smile. **Replace** `one slow, contented exhale through her nose` with `one slow, relaxed exhale through her nose`, and `No smile.` with `No smile: the corners of her mouth stay level the whole time.` |

(The table marks the six still jobs that hold the smile sentence as FIX so that each is edited. Counted by
cause, there are six fixes: smile ×8 jobs, S2 hand and parenthetical, S4 Element, S9 angle, S10 parenthetical.)

## Will the stills sell as handheld footage next to the 3 clips?

- **Shots 3 (0.40 s) and 4 (0.43 s):** yes. They are too short to read as stills, and the reference cuts there
  too.
- **Shot 5 (0.80 s):** yes. The push-out with a downward drift reads as sinking back.
- **Shots 9 (1.77 s) and 10 (1.47 s):** yes. She is asleep and still, the reference holds these angles almost
  static, and the shake spec plus grain matches the clips.
- **Shot 2 (1.10 s):** this is the weak one. A sharp hand frozen mid-release gives the still away. The cheapest
  fix is motion blur on his withdrawing hand, inside S2 (above), at 0 extra credits. In assembly, run the push
  slightly faster at the start of the shot.
- **No shot under ~1 s needs a clip.**
- **Assembly note (no job change):** apply the same shake amplitude to the clips' cut-ins as to the stills, so
  the C1 → S2 and S5 → C2 joins don't change "camera feel".

## Pass 2 reminders (after gate A, before any clip credits)

- Rewrite the first beat of C1 from S1's actual gaze and hand position.
- Rewrite the start and end beats of C2 from the real S6 and S7: which side his hand is on, where her hands
  are, the throw's height.
- Rewrite the start of C3 from S8: how much shoulder shows under the throw. If no shoulders are visible, change
  "shoulders melt" to "the throw at her chin sinks slightly".

## Credits
Unchanged: 41.0 estimate + 15 reserve = 56 (≤ 60, cap 135). No credits spent by this review.

---

## Round 2 (prompts.json revision 1): **PASS**

I re-checked all 13 jobs by script and by reading the changed passages.

**Fixes from round 1, each applied word for word:**

| Job | Round 1 fix | Round 2 |
|---|---|---|
| S5–S10 | Smile line | Applied |
| C2, C3 | "corners of her mouth stay level" | Applied |
| C3 | "relaxed exhale" | Applied |
| S4 | Crescent Element dropped (band only) | Applied |
| S9 | Face points up, neither cheek on the pillow | Applied |
| S2, S10 | Production-note parenthetical removed | Applied |
| S2 | Withdrawing, motion-blurred hand | Applied |

**Checks that still hold:**
- PATCHES, REFERENCE ROLES and STYLE are verbatim in every patch job.
- The tab points DOWN.
- The right pieces are in each shot: the crescent Element appears only in S3 and in S5–S10.
- Her continuity line is word for word in S1, S2 and S4–S10. His is word for word in S2, S3 and S6.
- `medias` holds only $still IDs and 564c68fa.
- C1–C3 are Kling pro, sound off, at 4 s, 5 s and 3 s, with no speech.
- Every job is preflighted: 41 + 15 reserve = 56, within 60.

**Result:** 13/13 OK, no regressions found, no credits spent. The next gate is pass 2 on the approved stills,
before any clip.

---

## Pass 2 (clip prompts vs the approved stills): **FIX**

I looked at the full-resolution start and end stills:
- C1 starts on S1 `974e98b0` (owner redo).
- C2 runs from S6 `3fe0a84c` to S7 `ca4073b6`.
- C3 starts on S8 `e26cdd37` (the fix).

Checks that hold: all three clips are sound off with no speech, and every patch-on clip keeps the mouth neutral.
All three prompts still describe the storyboard instead of these frames, so each needs to be replaced. The
`$JOB` placeholders also need the real IDs. The replacements below are written positively and use no injury
words (owner rule), and none of them mentions "red".

**Medias (exact):**

| Clip | start_image | end_image |
|---|---|---|
| C1 | `974e98b0-1aad-45b1-a389-6a10dc78ca77` | none |
| C2 | `3fe0a84c-ffa7-4a2d-b8ef-592c88adfb54` | `ca4073b6-f4bc-49e5-a79b-d7f234440b60` |
| C3 | `e26cdd37-0161-43cb-a833-6689fe841aad` | none |

Settings are unchanged: kling3_0 pro, 9:16, sound off, 4 s / 5 s / 3 s. Cost is unchanged: 7 + 8.75 + 5.25 = 21.

### C1_PROBLEM: FIX

**What S1 actually shows:**
- She lies on her front, propped on her forearms over a white pillow, already looking into the lens with
  half-open eyes and closed lips.
- The sleep lines are soft grooves on the cheek on the **frame-left** side (her right cheek, near the ear),
  away from the window.
- Her frame-left arm is folded under her. Her other hand rests on the pillow at frame-right.
- His soft, out-of-focus face edge fills the frame-left strip.

**What the old prompt gets wrong:**
- It asks her to "lift her head", but she's already up.
- It puts the lines on the frame-right cheek, so her frame-right hand would reach across her face.
- It calls the lines "red" and "deep", which risks the injury look the owner rejected.

**Replace the whole prompt with:**
`Motion only; the start frame sets her, the bedroom and the light. Gentle handheld phone sway, as if her boyfriend lying beside her is filming; no zoom. 0–0.7s: she stays propped on her forearms on the pillow, looking sleepily into the lens; the soft pillow-sleep lines on her cheek on the frame-left side of the image, near her ear, are clearly visible in the window light. 0.7–1.9s: her hand that is folded under her on the frame-left side comes up, and her index fingertip gently traces the longest soft sleep line on that same frame-left cheek; her hand on the frame-right side stays resting on the pillow; her eyes open wide at the lens. 1.9–4s: her face crumples into a dramatic, whiny, wordless cry: brows pull together, eyes squeeze shut, her mouth may open in a silent wail but she says no words; then she drops her face forward into the pillow in front of her. The soft sleep lines on her cheek keep exactly the same gentle look as in the start frame for the whole clip: the same soft grooves with a faint pink flush, no sharper and no darker. The soft, out-of-focus edge of his face stays at the frame-left edge, exactly as in the start frame, and never comes into focus. The blinds, the daylight from the window on the frame-right side and the room do not change. She does not talk or mouth words. Only her two hands are in frame, five fingers each; no other hand appears. Unretouched, no beauty filter; her skin texture does not change. No new objects. No fades, no cuts, no text, no captions, no logos. Sound off.`

### C2_TUCK_DOZE: FIX

**What S6 shows:**
- She sits up against the pillows and the headboard, eyes half open.
- The throw covers her lap and waist, with her two hands resting on top of it.
- His navy-sleeved forearm reaches down from the **top-right corner** and grips the throw's top edge at her
  waist.

**What S7 shows:**
- The same framing, with no hands in frame.
- The throw is at **mid-chest**.
- Her eyes are closed and her head tilts slightly toward the frame-left side.
- She still sits against the pillows; she is not lying down.

**What the old prompt gets wrong:**
- It pulls the throw "to her shoulders", which is past the end frame.
- It has his hand "slide out past the frame-right edge".
- It has her "nestle deeper into the pillow".

**Replace the whole prompt with:**
`Motion only; the start and end frames set her, the patches, the bedroom and the light. Gentle handheld phone sway; no zoom. 0–1.5s: his hand, reaching down from the top-right corner of the frame, pulls the top edge of the cream knit throw smoothly up from her waist to the middle of her chest; as it rises, her two hands slide under the throw and stay there. 1.5–2.2s: his hand lets go and his arm moves back up and out through the top-right corner of the frame. 2.2–5s: she stays sitting against the pillows and the headboard; she settles back, her eyes slowly close, her head tilts slightly toward the frame-left side and her breathing slows; she ends still, with the throw at the middle of her chest. SHE DOES NOT TALK: her lips stay closed the whole time. No smile: the corners of her mouth stay level the whole time. The five clear patches stay exactly in place, flat and clear; they do not move, slide, bend, double or turn white. The throw never touches her face. At the start three hands are in frame (her two on the throw, his one gripping its edge), five fingers each; after 2.2s no hands are in frame. The lamp, the fairy lights, the headboard and the nightstand do not move. Unretouched, no beauty filter; her skin texture does not change. No new objects. No fades, no cuts, no text, no captions, no logos. Sound off.`

### C3_EXHALE: FIX

**What S8 shows:**
- A close-up of her face, head back on the white pillow, eyes closed, mouth neutral, all five pieces on.
- The grey crewneck fills the lower frame, and the throw shows only in the lower-right corner.
- Wooden shelf with fairy lights and blinds at the top of the frame.

**What the old prompt gets wrong:** "shoulders… melt down into the throw" asks for motion that isn't in the
frame, and the model may pull the throw up or invent shoulders under it.

**Replace the whole prompt with:**
`Motion only; the start frame sets her, the patches and the light. Very slight handheld phone sway; no zoom. 0–0.5s: still, asleep, her head resting back on the white pillow. 0.5–2s: one slow, relaxed exhale through her nose: her chest under the grey sweatshirt rises a little, then settles, and the corner of the cream throw at the lower right of the frame sinks slightly with it. 2–3s: still, asleep. Eyes stay closed. SHE DOES NOT TALK: her lips stay closed the whole time. No smile: the corners of her mouth stay level the whole time. The five clear patches stay exactly in place, flat and clear; they do not move, slide, bend or turn white. Her head does not turn; nothing touches her face. No hands in frame. The pillow, the shelf, the blinds and the fairy-light glow do not change. Unretouched, no beauty filter; her skin texture does not change. No new objects. No fades, no cuts, no text, no captions, no logos. Sound off.`

**After these three replacements and the ID swaps, the clips are ready to submit. No further review is needed:
the fixes are text only, and the cost and settings are unchanged.**


---

## v3 pass 1 (prompts.json revision 3, before any credits): **FIX**

Reviewer: prompt-reviewer (6b), independent. Read: owner-feedback (newest), lessons §0, §3–8, §10, brief, story v3,
storyboard v3, prompts v3, budget v3, config, production log; looked at the reused S1/S2/S4/S5/S10 and the reused
C2/C3 windows at full-res crops. Script check: STYLE block verbatim in all 4 stills; REFERENCE ROLES + PATCHES
verbatim in ST_BATH_GIVE; continuity sentence word for word in all 4 stills; Elements 6375c707/9d766c06 only as
`<<<id>>>` in ST_BATH_GIVE text, never in `medias`; every clip `sound: off`; no injury words anywhere ("red",
scratch, rash, etc. absent; "cut" only in "no cuts"); mirror words only as "no mirror"; no smile asked with patches on.

| Job | Verdict | Issue (what the model would do) |
|---|---|---|
| ST_NIGHT | OK | Squashed cheek/eye fold described; one hand; no box; dark top fifth. Fold side (her right cheek, down) matches the bathroom lines (frame-left = her right cheek). |
| ST_BATH_BEFORE | **FIX** | (1) "lights her face evenly from the front" flattens skin-texture creases (2-T R12 failure): the lines vanish at phone size and the cold-viewer test fails. (2) The source S1 has **his jaw at frame-left**; "the only woman" doesn't stop the edit keeping a man's face edge. (3) Missing the wording that worked in the S1 fix ("following a pillowcase seam and fabric fold"), which is also the visual that says *pillow* to a stranger. (4) The after needs something to soften: the outer-eye and forehead fine lines must show clearly here. |
| ST_BATH_GIVE | OK | Edit chain from $ST_BATH_BEFORE, roles block, PATCHES verbatim, off-face note, 2 hands, bare-face smile allowed. |
| ST_BATH_AFTER | OK | Single-image edit, "keep everything as placed", softer not erased, same pores, lips closed, no hands. Inherits the new light from the fixed BEFORE. |
| C_NIGHTS | **FIX** | (1) "A fast time-lapse… everything sped up" + 2.8× in code = double speed: jittery fast-forward, and Kling tends to add light flicker to "time-lapse". (2) "rolls onto her stomach" at 50 cm, locked: her face leaves the frame or turns away, and a full-body roll is a high-failure motion; it also makes the read "restless sleeper", not "face squashed". (3) Mode std → pro (hook frame one). |
| C_BATH_GIVE | **FIX** | (1) "lets out a small sigh through her nose": Kling animates sighs/exhales as an open-mouth breath (production log, C2/C3). (2) "She does not cry" names crying; state the positive instead. (3) The sheet is patch-visible; add the clear/never-white line. (4) Mode std → pro (the before lines need resolution). |
| C_APPLY | **FIX** | Patches are visible and the PATCHES block is missing (agent rule: every patch-visible job pastes it verbatim). Std is fine here. |
| C_AFTER | **FIX (settings only)** | Text OK (small smile, patches off, no creases appear, ≤1 hand). Mode std → pro: at std res the "softer lines" result can be invisible, which makes the solution weak. |
| Reuse C3_EXHALE | **FIX (assembly)** | Full-res crops: **lips part from ≈0.55 s, teeth by 0.70 s**, so the 0.00–0.78 window shows an open mouth with patches on. Use 0.00–0.50 at 0.64× (or 2.45–3.04 at 0.76×). |
| Reuse C2_TUCK_DOZE | OK | 0.00–1.40 and 3.40–4.92 are closed-lip (checked 3.4 and 4.9). Lamp is ON in frame: shot 7's "lamp off" grade needs a crop that excludes the lamp. |

### Exact replacement text

**ST_BATH_BEFORE**: three edits.
- Replace `Light: a warm-white vanity light just above the lens lights her face evenly from the front and slightly above.` with:
  `Light: a warm-white vanity light bar just above the lens and slightly to the frame-right side lights her face from the front, angled a little across it, so the soft creases on her frame-left cheek and the line on her forehead catch tiny soft shadows.`
- Replace the sentence that starts `Gentle pillow sleep creases from the night:` (through `as tiny soft shadows.`) with:
  `Gentle pillow sleep creases from the night: soft, shallow pressed grooves in her cheek on the frame-left side of the image (her right cheek), following a pillowcase seam and fabric fold pattern from near the ear toward the outer corner of her eye and joining the fine lines there, plus one soft horizontal crease across her forehead; soft rounded edges, the same colour as the rest of her skin with at most a faint natural pink flush; visible as texture in the skin rather than colour, catching the vanity light as tiny soft shadows, easy to see at a glance on a phone screen. In this light the fine lines at the outer corners of her eyes and the line across her forehead also show clearly.`
- After `There is no mirror, no reflective surface and no second copy of her anywhere in the frame.` insert:
  `She is the only person in the frame: no man, and no second face, jaw, shoulder or hand at any edge of the frame.`

**C_NIGHTS**: `"mode": "pro"`; replace the whole prompt with:
`Motion only; the start frame sets her, the bedroom and the light. The phone is propped on the nightstand and locked off: the camera does not move. Natural real-time movement of a deep sleeper, not sped up. She stays lying on her side facing the lens the whole time. 0–1s: asleep, she shifts and nuzzles her face deeper into the pillow, her cheek and the skin beside her lower eye folding against it. 1–2s: her hand pulls the pillow a little tighter under her face. 2–3s: she shifts her shoulders under the duvet and presses her face further into the pillow, the edge of her forehead sinking into the pillowcase. 3–4s: she lies still, her cheek and forehead squashed into the pillow. Her face stays in the same place in the frame and stays visible the whole time. Her eyes stay closed; she stays asleep the whole time. SHE DOES NOT TALK: her lips stay closed the whole time. Exactly one hand in frame, hers, with five fingers; no other hands, no other people. The lamp, the nightstand and the fairy lights do not move and the light does not change. Unretouched, no beauty filter; her skin texture does not change. Exactly one woman; no mirror, no reflection, no second face. No new objects. No fades, no cuts, no text, no captions, no logos. Sound off.`

**C_BATH_GIVE**: `"mode": "pro"`; replace the whole prompt with:
`Motion only; the start and end frames set her, the bathroom and the light. The phone rests on the shelf: almost no camera movement, no zoom. 0–0.6s: she leans a little closer to the lens, studying her face. 0.6–2.2s: her hand on the frame-left side comes up and her index fingertip gently touches the soft sleep creases on her cheek on the frame-left side of the image, near the outer corner of her eye, then the soft line on her forehead; her brows draw slightly together in a small, quiet frown and her shoulders drop once in a small sigh, her lips pressed softly together. Her face stays calm apart from the small frown; the reaction is small and believable. 2.2–2.6s: that hand lowers out of frame. 2.6–5s: his hand, in a navy T-shirt sleeve, comes in from the frame-right edge at her shoulder height holding up the clear backing film with the five clear pieces; she turns her head slightly toward it, her brows lift in pleasant surprise and a small natural closed-lip smile appears; her hand on the frame-right side rises and her fingertips touch the bottom edge of the film. The sleep creases on her cheek and forehead keep exactly the same soft look for the whole clip, no sharper and no darker. The five pieces on the film stay thin, transparent and slightly frosted, never white or opaque, and keep their exact shapes; the forehead piece's tab points DOWN. She does not talk or mouth words. Never more than two hands in frame at once, five fingers each. Unretouched, no beauty filter; her skin texture does not change. Exactly one woman; no mirror, no reflection, no second face. No new objects. No fades, no cuts, no text, no captions, no logos. Sound off.`

**C_APPLY** (stays std): after `2.2–3s: she lowers both hands to the duvet in her lap and sinks back against the pillows.` insert:
`By the end of the clip all five pieces are on her face as follows. The patches are the exact clear silicone pieces shown in the product reference, and nothing else. They are thin, transparent and slightly frosted; her skin and lines stay visible through them; they are noticed only by a thin raised edge that catches the light and a soft satin sheen. They are never white, beige, pink, gold, opaque, gel pads, hydrogel, fabric, paper or tape. Forehead piece: a wide, gently curved band covering the middle two-thirds of the forehead, with a small rounded tab at the centre of its lower edge pointing down between the eyebrows; it does not reach the hairline. Under-eye pieces: one slim crescent per eye, just below the lower lashes, following the curve of the lower lid, the outer end reaching toward the outer eye corner; never covering the eye or lashes; never circles, rings or glasses shapes. Smile-line pieces: one slim crescent on each side, along the fold from beside the nostril to beside the mouth corner; the lips stay uncovered. Every patch lies completely flat, with no bubbles, folds or lifted edges. A piece the prompt does not mention is not on her face.`

**C_AFTER**: `"mode": "pro"`. Prompt unchanged.

**Assembly (reuse windows):** shot 6 = C3 0.00–0.50 at 0.64× (not 0.00–0.78); shot 7 = C2 3.40–4.92 flipped, 1.25×
crop excluding the lamp (story-review v3 fix 3); shot 8/9 = C_AFTER 0.00–2.40 / 2.40–5.00 at 0.975× (fix 4);
shot 4 = C_APPLY 0.80–2.80 at 1.25× (fix 5).

### Settings and cost
| Job | Mode | Credits |
|---|---|---|
| 4 stills (nano_banana_2 2k) | — | 8 |
| C_NIGHTS 4 s start | **pro** | 7 |
| C_BATH_GIVE 5 s start+end | **pro** | 8.75 |
| C_APPLY 3 s start+end | std | 4.5 |
| C_AFTER 5 s start | **pro** | 8.75 |
| **Total** | | **37.0** (39.0 with one 2-cr still fix) ≤ 40 |
Preflights still missing: **pro 4 s start-only, pro 5 s start+end, and nano_banana_2 with 1 ref** (only the 2-ref
still and pro 5 s start-only were preflighted). Run them before submitting; stop if any differs from the table.
Optional C_NIGHT3: not recommended (story-review v3); it does not fit with the pro upgrade (41.5).

**After these replacements: PASS** for pass 1 (text and settings only). Pass 2 still runs on the approved stills
before any clip (rewrite each clip's first/last beat from what the stills actually show).

---

## v3 round 2 (prompts.json "3 rev 1"): **FIX (two stills, one clip line; text only)**

Script check again:
- STYLE block verbatim in all 4 stills; REFERENCE ROLES and PATCHES verbatim in ST_BATH_GIVE; PATCHES now verbatim in C_APPLY.
- The continuity sentence is word for word in every still.
- Elements appear only as text.
- Sound is off everywhere; no injury words.
- Modes: pro for C_NIGHTS, C_BATH_GIVE and C_AFTER; std for C_APPLY. All are preflighted (7 / 8.75 / 8.75 / 4.5 credits; 2 per still). **Total 37.0, or 39.0 with one still fix, ≤ 40.**

Every pass-1 replacement is applied exactly. ST_NIGHT, ST_BATH_GIVE, C_NIGHTS, C_BATH_GIVE and C_APPLY are **OK**.

**The new problem is the counter box spot.** ST_BATH_BEFORE asks for a "close-up from the top of her head to her collarbones" from a phone at eye level, where the mirror would hang. It also asks for "the edge of the white vanity countertop along the bottom of the frame", while her hands rest "on the edge of the sink below the frame". A vanity counter is at hip height, so it can't be in a head-to-collarbone frame. The model will either:
- widen the shot, which makes her face smaller and the lines weaker (the exact thing round 1 fixed), or
- invent a foreground ledge right at the lens, where a sharp composited box would look pasted on.

The shot-9 punch-in to 112% also crops the bottom-right corner, so the box would drop out of shot 9. Fix: put the box on a small wall shelf behind her, at shoulder height, frame-right, set in from the edge.

| Job | Verdict | Exact replacement |
|---|---|---|
| ST_BATH_BEFORE | FIX | Replace `The edge of the white vanity countertop runs along the bottom of the frame, and the countertop corner at the bottom of the frame on the frame-right side is clear and empty, with nothing standing on it.` with `On the tile wall behind her, on the frame-right side at the height of her shoulder and about a fifth of the frame width in from the right edge, there is a small empty white wall shelf with nothing standing on it; her head and shoulders do not cover it.` |
| ST_BATH_AFTER | FIX | Replace `The countertop corner at the bottom of the frame on the frame-right side stays clear and empty, with nothing standing on it.` with `The small white wall shelf behind her on the frame-right side stays empty, with nothing standing on it.` |
| C_AFTER | FIX | After `0–0.8s: she leans a little closer to the lens, studying her face, just as on the morning before.` insert `Her head and shoulders never move over the small white wall shelf behind her on the frame-right side.` |
| Assembly | note | Composite the real box standing on that shelf, slightly softened to match the background focus, with a contact shadow on the shelf and vanity-light shading. Keep it in shots 8 and 9: at 112% the shelf, about 20% in from the edge, stays in frame. No box in shots 2–3. |

**After these three edits: PASS**, with no further review of this pass. Pass 2 still runs on the approved stills before any clip.

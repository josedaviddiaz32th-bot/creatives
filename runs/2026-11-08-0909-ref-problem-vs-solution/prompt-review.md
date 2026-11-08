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

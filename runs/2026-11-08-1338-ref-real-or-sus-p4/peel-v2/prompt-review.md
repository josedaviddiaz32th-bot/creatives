# Prompt review: peel redo v2 (run 2026-11-08-1338, U2)

Stage 6b, prompt-reviewer. No credits were spent and nothing was generated.

**What I read:**
- `.claude/agents/prompt-reviewer.md`
- `learning/owner-feedback.md`
- `docs/lessons-learned.md` §2, §4 blocks, §6 (including "Staging that makes an AI peel work") and §10 A
- `learning/production-log.md`
- This run's `clips-check.md` (U2_PEEL FAIL), `stills-check.md` (S_U2_START / S_U2_END), `storyboard.md`, the U2 entries in `prompts.json`, and `budget.json`

## Verdict: **FIX**

Both prompts need text changes. The staging follows the new §6 block:
- the clip starts mid-peel;
- she pulls sideways from the same side as her hand (frame-right, which matches S_U2_END);
- the second hand anchors the skin;
- the head tilt is slight, so the clip can still land on the frontal S_U2_END;
- it is one ~2 s peel in a 4 s clip.

The light, sides and hand all agree with S_U2_START and S_U2_END. The fixes below close the gaps that would let the model repeat the slide and smear, add a phone arm, or drift the band's look.

| Job | Verdict | What the model would do with the current text | Fix |
|---|---|---|---|
| S_PEEL_MID | **FIX** | (a) "selfie" plus both hands busy: it may add a third arm holding the phone. (b) "Not frosted… clear and glossy" fights S_U2_START (which reads slightly frosted) and S_U2_END ("transparent and slightly frosted"), so the band's look shifts between the still and both frames. Kling then interpolates the material: that is the milky-smear path. (c) Nothing says the lifted strip and the stuck part are one piece, so you risk a full band on the forehead plus a second strip in the air. (d) The frame-right hand is on the shadow side, away from the window, and could come out dark (owner hand-tone rule). (e) No REFERENCE ROLES opener, no STYLE block and no PATCHES block (all required pipeline blocks). (f) "Eyes looking down" can render as closed eyes (U2 had closed eyes at 2.4 and 3.0 s) | Replace the whole prompt with R1 |
| PEEL_V2 | **FIX** | (a) "Pulling the free end outward and sideways… close to the plane of her forehead" is an in-plane pull along the band's own length. Read literally, that drags the whole band sideways, a wipe, and the prompt never says the stuck part stays still. That is the same failure as U2 in a new direction. (b) "Like tape being pulled" names a material the PATCHES block bans ("never… tape"), which invites an opaque, papery strip. (c) It is missing "SHE DOES NOT TALK: her lips stay closed the whole time." (the band is on at the start). (d) Nothing makes her head turn from the tilted, eyes-down start to the frontal lens look of S_U2_END. (e) The frame-left hand's exit path isn't fenced off from her face, and U2 smeared down the frame-left eye and cheek. (f) "Clear and glossy" versus the slightly frosted end frame: same material drift as above. (g) Nothing holds the bare forehead still, so Kling may visibly morph the lines toward S_U2_END. (h) The hand could leave the frame while pulling sideways. (i) The PATCHES block is missing (CLAUDE.md hard rule) | Replace the whole prompt with R2 |

Settings: kling3_0 pro, 4 s, silent, start S_PEEL_MID, end S_U2_END (040d5330…), 9:16. These are OK and inside the §6 length of 3–4 s. The still is nano_banana_2, 2k, 9:16, with S_U2_START (031f92d2…) as its single image reference.

**Cost (owner decision, not a prompt fix):** the redo costs about 9 credits (2 for the still, 7 for the clip). `clips-check.md` shows 3.25 credits left under the 50 cap. The owner said "Try the peel again", but did not explicitly approve going over the cap ("you work with what is left unless I give you permission"). Get a clear yes before submitting.

**Assembly note:** the new clip is 4 s, against 6 s for U2.
- Don't fill the gap by cutting from the old U2 lift (0–2.8 s) into the new mid-peel. That is a cut in the middle of one peel, which the owner spots.
- Don't fill it with a held still either: the owner wants all video.
- Cut into PEEL_V2 from the expert, or from U1. You can still reuse the old U2 tail (3.9–6.0 s) as the E1 background loop, because it ends on the same frame, S_U2_END.

## R1: S_PEEL_MID replacement prompt (use verbatim)

```
Identify the reference photos by what they show, not by upload order. THE CAST PHOTO shows the only person in this image; keep her face, skin, age, hair and earrings exactly as shown. Only THE CAST PHOTO is supplied here; the product reference is <<<6375c707-7ad9-4df9-b7e0-69750993e7aa>>>: use it only for the exact shape, size and transparency of the forehead piece. Keep her face, skin, age, hair and low bun, earrings, tank top, bed, pillows, headboard, the soft daylight from the window on the frame-left side, and the framing and camera distance exactly as shown. The phone is on a stand; nobody holds it. Exactly one person and one head.
CHANGES ONLY: she is in the middle of peeling the clear forehead band off. Her head is tilted very slightly toward the frame-left side, chin a little down; her eyes are clearly open, gaze lowered toward the frame-right side at what her hand is doing; relaxed and focused, lips closed, the corners of her mouth level.
Her hand on the frame-right side comes in from the frame-right edge at temple height and never crosses in front of her eyes. It pinches the outer end of the band between thumb and index finger and has drawn it sideways, away from her temple: the outer quarter of the band is already off her skin and reaches out into the air beyond the side of her face, a thin, soft, see-through strip about 1 mm thick that bends gently, its edge catching the window light. The lifted strip and the part still on her skin are one single, joined piece; there is no second band. The rest of the band is still flat on her forehead exactly as it is now, its small tab pointing down between the eyebrows, with no fold, no bubble and no gap.
Her other hand, on the frame-left side, rests its index and middle fingertips on the bare skin of her temple just beyond the frame-left end of the band, holding the skin still; that wrist and forearm stay at the frame-left side of her face, never in front of her eyes. Exactly two hands with five fingers each, no extra fingers. Both hands are lit by the same soft window daylight as her face and have the same skin tone as her face; neither hand is in shadow.
The skin where the band has already come off has the same normal tone and matte finish as the rest of her forehead: no redness, no mark, no outline, no shine, nothing that looks like an injury.
The band, both the part on her skin and the part in the air, keeps exactly the look it has in this image: thin, transparent and slightly frosted, her skin and lines visible through it, noticed only by a thin raised edge and a soft satin sheen; never white or milky. The patches are the exact clear silicone pieces shown in the product reference, and nothing else. They are thin, transparent and slightly frosted; her skin and lines stay visible through them; they are noticed only by a thin raised edge that catches the light and a soft satin sheen. They are never white, beige, pink, gold, opaque, gel pads, hydrogel, fabric, paper or tape. Forehead piece: a wide, gently curved band covering the middle two-thirds of the forehead, with a small rounded tab at the centre of its lower edge pointing down between the eyebrows; it does not reach the hairline. Under-eye pieces: one slim crescent per eye, just below the lower lashes, following the curve of the lower lid, the outer end reaching toward the outer eye corner; never covering the eye or lashes; never circles, rings or glasses shapes. Smile-line pieces: one slim crescent on each side, along the fold from beside the nostril to beside the mouth corner; the lips stay uncovered. Before she starts peeling, every patch lies completely flat, with no bubbles, folds or lifted edges. A piece the prompt does not mention is not on her face. Only the forehead piece exists in this image: there are no under-eye or smile-line pieces anywhere; the skin under her eyes and beside her mouth is bare.
Photorealistic smartphone photo, unretouched, no beauty filter, visible pores and natural skin texture, sharp focus on her face. Her hair is pulled fully back off her forehead. The skin is dry and matte with no cream or lotion. No mirror in the shot. No text, captions, logos or watermark.
```

R1 pastes the PATCHES block verbatim, as CLAUDE.md requires, with the one change §6 allows: "Before she starts peeling," goes in front of "every patch lies completely flat". It is followed by the forehead-only sentence used in S_U2_START. R2 carries the same block.

## R2: PEEL_V2 replacement prompt (use verbatim)

```
Motion only; the start and end frames set her, the clear band, the bedroom and the daylight. Phone propped on a stand: camera almost still, faint natural sway, no zoom, no cuts. SHE DOES NOT TALK: her lips stay closed the whole time.
0–1.8 s: her hand on the frame-right side keeps drawing the band's free end sideways, away from the side of her face, in one slow, steady motion, like peeling a soft screen protector; her hand stays inside the frame. The part of the band still stuck to her skin stays perfectly still and never slides: only the line where the band leaves her skin moves, steadily from the frame-right side toward the frame-left side, and the skin behind that line is bare. The peeled part trails out into the air beside her head as a soft, thin, see-through strip that bends and sways; it never folds back over the part still on her skin and never slides down her face or over her eyes. At the moving edge the silicone lets go of the skin cleanly with a slight tackiness; the skin is never tugged, dimpled or stretched. Her frame-left fingertips keep holding the skin at her temple still. At about 1.8 s the last edge, at the frame-left end, lets go cleanly beside those fingertips without touching them.
1.8–2.6 s: the whole band swings free, hanging from her frame-right fingers only, soft and floppy, one single piece, its free end curling slightly. Her frame-left hand lowers down the frame-left side of her face and out of frame, never in front of her face.
2.6–4.0 s: she brings the held band down to cheek height on the frame-right side, beside her face and never in front of it, as in the end frame; she straightens her head to face the lens, lifts her eyes to the camera and gives a small, calm, closed-lip satisfied look. Her bare forehead keeps its normal even skin tone and matte finish, with no redness, outline or marks; once it is bare it does not change.
Exactly one band and one person; exactly two hands with five fingers each until the frame-left hand leaves, then one. From the first frame to the last the band keeps the same thin, see-through, slightly frosted look it has in the start frame: never milky, white, opaque, smeared, split or doubled. Her eyes stay open except natural blinks. The band before and during the peel is shaped and made as follows: The patches are the exact clear silicone pieces shown in the product reference, and nothing else. They are thin, transparent and slightly frosted; her skin and lines stay visible through them; they are noticed only by a thin raised edge that catches the light and a soft satin sheen. They are never white, beige, pink, gold, opaque, gel pads, hydrogel, fabric, paper or tape. Forehead piece: a wide, gently curved band covering the middle two-thirds of the forehead, with a small rounded tab at the centre of its lower edge pointing down between the eyebrows; it does not reach the hairline. Under-eye pieces: one slim crescent per eye, just below the lower lashes, following the curve of the lower lid, the outer end reaching toward the outer eye corner; never covering the eye or lashes; never circles, rings or glasses shapes. Smile-line pieces: one slim crescent on each side, along the fold from beside the nostril to beside the mouth corner; the lips stay uncovered. Before she starts peeling, every patch lies completely flat, with no bubbles, folds or lifted edges. A piece the prompt does not mention is not on her face. Only the forehead piece exists in this clip: there are no under-eye or smile-line pieces anywhere; the skin under her eyes and beside her mouth is bare.
```

## Pass 2 (after S_PEEL_MID is generated, before the clip)

Check the still for these, and fix the clip prompt to match what is actually in the frame:
- one joined band, with no second strip;
- the frame-right hand's thumb and index finger visible on the strip end;
- the anchor fingertips on the bare temple, not on the band;
- both hands the same tone as her face;
- eyes visibly open;
- the band's material matching S_U2_START.

After generation, step through 0.5–2.6 s at 10 fps for any slide, smear or milky frame.

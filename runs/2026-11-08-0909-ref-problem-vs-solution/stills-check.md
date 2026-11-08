# Stills check (gate A): run 2026-11-08-0909 "The Problem / Vs… / The Solution"

Stage 7 producer, stage A. All 10 stills from `prompts.json` rev 1, `nano_banana_2` 2k 9:16, one output each, preflighted at 2 credits each.
Each still was looked at against checklist A (lessons §10), its beat, and the owner's calibration in `learning/owner-feedback.md`.
Full-resolution files: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/stills-trend/<JOB>.png`.
Contact sheet: `stills-contact.png` (shot order, 5 per row).

**Result: 10/10 PASS** (S8 after one 2-credit fix; S9 after a free code crop; S1 redone on owner request). **Spend: 24 credits**: 10 × 2, the S8 fix (2) and the owner-approved S1 redo (2; one earlier attempt failed on the platform and was refunded).
The balance went from 955.4 to 931.4. No clips were submitted.

| # | Job | Generation ID (use as `$JOB` in clips) | Cost | Gate A | Note |
|---|-----|-----------------------------------------|------|--------|------|
| 1 | S1_PROBLEM v1 | `e3e348fc-9a5f-4d82-84fc-382f725e77f3` | 2 | REPLACED (owner) | Photoreal, handheld. She's propped on her forearm and groggy, with red creases on her cheek and forehead. His blurred stubbled jaw shows at frame-left. Notes: the creases are on the frame-LEFT side of her face (the prompt asked for frame-right), and part of his eye and nose show at the edge. A phone viewer won't notice. C1 pass 2: her gaze is to the lens with her right hand on the pillow at frame-right. |
| 1 | S1_PROBLEM (owner redo) | `974e98b0-1aad-45b1-a389-6a10dc78ca77` | 2 | PASS | Owner: the cheek creases in v1 "read as red scratches. We don't want nothing looking like injuries." This is a single-image edit of v1 with everything else identical: soft pressed pillow-sleep grooves with a faint pink flush on her cheek (frame-left side of the image) near the outer eye, visible in the side light, and no red lines. Nothing reads as an injury. **Use this ID as `$S1_PROBLEM` for C1.** v1 `e3e348fc` is retired (attempt `453f34be` failed on the platform, refunded). |
| 2 | S2_BOX | `873abce2-a81a-4c68-9f7a-153b3a12e22e` | 2 | PASS | The placeholder box is blank off-white with a teal narrow side, upright on the duvet at frame-right, and all three hands are correct. **Assembly note:** his index fingertip slightly overlaps the right edge of the box's front face, so mask that fingertip back over the composited real box (or the finger reads as behind it). The hand has only slight motion blur, and the navy sleeve doesn't show. |
| 3 | S3_INSERT | `3c75a7fb-4372-4a82-aeb8-5fc6d9a5c33f` | 2 | PASS | One male hand holds the backlit film with exactly five clear pieces: the band with its tab DOWN and four crescents. Navy sleeve, lamp and fairy lights are there, and there's no box. |
| 4 | S4_BAND | `2d9dbe01-82c0-455c-a387-6e42c6ea967b` | 2 | PASS | Only the forehead band, which is clear and slightly frosted with its tab DOWN; there are no crescents. Palms at her temples, mouth neutral. Notes: the band's top edge sits close to the hairline, and her fingertips just touch the band ends. |
| 5 | S5_SET | `d65f6fb0-4df1-4f7a-a03e-853524a6d20f` | 2 | PASS | Five pieces: the band with its tab down, two under-eye and two smile-line pieces, all clear and frosted, with the lips uncovered and the mouth neutral (no smile). The under-eye crescents are plump half-moons, a shape the owner accepted (production log, K4). They're not circles or rings. |
| 6 | S6_TUCK | `3fe0a84c-ffa7-4a2d-b8ef-592c88adfb54` | 2 | PASS | Her patches are identical to S5. Three hands; his navy-sleeved forearm comes in from frame-right holding the throw at her waist. Mouth neutral, eyes half open. Note: she sits more upright than "lies further back". C2 pass 2: his hand is at frame-right on the throw at her waist; her hands are on the throw at her stomach. |
| 7 | S7_DOZE | `ca4073b6-f4bc-49e5-a79b-d7f234440b60` | 2 | PASS | Same framing as S6. Eyes closed, mouth neutral, five clear pieces, no hands. Note: the throw comes to mid-chest, not her shoulders; her head tilts slightly to frame-left. C2 pass 2: the end beat is "the throw at mid-chest", not "at her shoulders". |
| 8 | S8_CLOSE | `cc8d6a37-21e7-49a3-bce0-cad485821d8e` | 2 | **FAIL** | A duplicated second head and face of her (her hair and a second earring) merged behind her on the pillow. Logged in the production log. Don't use this one. |
| 8 | S8_CLOSE (fix) | `e26cdd37-0161-43cb-a833-6689fe841aad` | 2 | PASS | Rebuilt from S7 (not an edit of the bad still) with "same reclined pose" and "exactly one person and one head". One person, five clear pieces, tab down, eyes closed, mouth neutral. Notes: the throw only shows at the lower-right corner (not "tucked to her chin"), and window blinds appear above the headboard (a minor room drift). **C3 pass 2:** she's in a grey crewneck and no shoulders are under the throw, so change "shoulders melt" to "her chest settles / the throw at the bottom of frame sinks slightly". **Use this ID as `$S8_CLOSE`.** |
| 9 | S9_LOW | `5df74de8-9db4-4cba-8776-c3ebe75f25a2` | 2 | PASS (free code fix) | As generated, a hard seam at row ~605/2752 put a flat grey band over the top 22% of the frame. Everything else passes: face up, neither cheek on the pillow, clear pieces, mouth neutral. **Use `S9_LOW_codecrop.png` (in this folder):** a crop below the seam, 1205×2142 → 1080×1920, with no upscale. Shot 9 is code motion only, so no clip needs this ID. |
| 10 | S10_WIDE | `ea1af1e3-2039-4a16-9f6b-034d4feab2b9` | 2 | PASS | The placeholder box is blank off-white with a teal side, fully visible on the nightstand beside the lamp and the water glass. She's asleep with five pieces showing, mouth neutral. Note: the angle came out close to S7's eye-level framing, not the "high wide from the foot corner" asked for, and she's reclined, not flat. To set it apart from shot 7 in the edit, use a different scale (start ~110% and push out). |

## Across all frames
- **Same two people:** yes. His forearm (light skin, dark hair, navy tee) matches across S2, S3 and S6, and she has the same face, gold studs and grey crewneck throughout. **Owner note:** her hair is honey-brown in S1–S2 and reads strawberry/ginger in the warm-lit S4–S10. It's the same face, but a careful viewer may notice the shift from morning to night. A grade in assembly (cooler, less saturated hair in shots 4–10) costs nothing.
- **No smile with patches on** in any frame, and every mouth is neutral.
- **Patches** are always clear or frosted, never white or opaque. The tab is DOWN everywhere, and each frame shows the right pieces.
- **No mirror and no model text** anywhere. The placeholder boxes (S2, S10) are blank.
- **Ready for prompt-review pass 2** (clip prompts against these stills), then owner approval of the stills before any clip credits.

---

# v3 stills (owner-ordered fix, ≤40 new credits)

`prompts.json` "3 rev 2": prompt-review v3 round 2 applied word for word. The box spot is now a small empty wall shelf behind her at frame-right, at shoulder height, left empty for a code composite.
Full-resolution files: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/stills-trend/v3_<JOB>.png`.
Contact sheet: `stills-contact-v3.png`.

**Result: 4/4 PASS** (ST_BATH_BEFORE after the one allowed still fix). **Stills spend: 10** (4 × 2 plus a 2-credit fix).

| Job | Generation ID | Cost | Gate A | Notes |
|---|---|---|---|---|
| ST_NIGHT | `e0811a49-6398-4ec8-9e5b-40f77693bd48` | 2 | PASS | Dark room with a fairy-light glow. She's asleep on her side with her face squashed into the pillow: cheek and eye skin fold against it, which reads as the cause. One hand, five fingers. Lips closed, no box, no mirror. |
| ST_BATH_BEFORE v1 | `db2254b8-d621-4aa5-b024-ba8ea5db5a90` | 2 | **FAIL** | A near copy of S1 (bedroom, blinds, pillow, same pose), with no bathroom. Logged in the production log. |
| ST_BATH_BEFORE (fix) | `03346ec1-6a63-44cb-ab91-ef0140bdbdc0` | 2 | PASS | Rebuilt from S2 `873abce2` as identity only, opening with "a NEW photo in a different room". She's alone in a bathroom with the camera as the mirror; no mirror or reflection is visible. The vanity bar is behind her. The empty white wall shelf is at frame-right, shoulder height. The soft pillow-seam grooves on her frame-left cheek are skin-coloured and read as texture, nothing injury-like, and the forehead and outer-eye lines are visible. A small, real frown. **Owner note:** she reads a few years older and more tired than in the night shot (no make-up, flat morning light). It's the same face, freckles, hair and studs. |
| ST_BATH_GIVE | `944cf852-760b-4965-b16f-ce0b8a181eb8` | 2 | PASS | His hand holds the backlit film: five clear pieces, tab DOWN, never white. Her fingertips touch the bottom edge, so two hands. Small closed-lip smile, which is allowed with a bare face. The creases are still visible. Notes: a plain grey mirror-cabinet panel appears behind her head with nothing reflected in it, and the film covers the shelf. |
| ST_BATH_AFTER | `61d5547a-f08e-49c3-abf2-88b5bc8c7bff` | 2 | PASS | Same framing as BEFORE. The creases are gone and the forehead and outer-eye lines are softer, with real texture (freckles, pores) kept. Calm, lips closed, no hands, and the shelf is empty for the box composite. |

**Producer pass-2 (clip prompts vs these frames):** one wording change. In C_NIGHTS, "she shifts her shoulders under the duvet" became "she shifts her shoulders slightly", because ST_NIGHT shows no duvet. The other three prompts match their frames as written. Clip medias were set to the IDs above.

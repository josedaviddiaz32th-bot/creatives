# Stills check (gate A): 2026-11-07-2002-1t-first-line-fixer

Producer, Stage A only. Owner rules: one generation per shot (count 1), no automatic redo, stop at the first failed still.
Balance before: 1200. Balance after: 1188.5. Spent: 11.5 (budget.json `actual_total`). Still-fix allowance (`still_fix_credits_auto`): 1.5 of 3 used.

**Status: STOPPED at K4.**
- Approved: K1 = `91d6abc0` (owner-approved fix), K2 = `91d09592` (owner-approved fix) and K3 = `f0d61ae3`.
- K4 failed.
- K5, K6 and K7 were not generated.

| Still | Generation ID | Credits | Verdict |
|---|---|---|---|
| K1 v1 | 712c622b-31b0-4425-a939-293e6c64afa5 | 1.5 | ❌ superseded |
| **K1 (fix)** | **91d6abc0-eb0a-4f1c-bce6-b2a663bbaf69** | 1.5 | ✅ |
| K2 v1 | 6bbee4ea-14fd-480e-948d-d63b5b9cb8db | 2 | ❌ superseded |
| **K2 (fix)** | **91d09592-2072-4ca3-84de-d0b15a1830cb** | 2 | ✅ (1 note) |
| **K3** | **f0d61ae3-a6a7-4172-a518-e9586bda1c00** | 1.5 | ✅ |
| K4 v1 | 9d36306f-d048-43c1-88c0-79d02d58400e | 1.5 | ❌ |
| K4 fix | 02a0082c-acd1-43d7-a34c-850d33ec389a | 1.5 | ❌ stopped here (fix failed) |

Local stills: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/stills-1t/`

---

## K1_NIGHT_ID v1: FAIL (superseded)

- Generation ID: `712c622b-31b0-4425-a939-293e6c64afa5`. Credits: 1.5. Balance 1200 → 1198.5.
- Failed on two points:
  - The tray held 3 pieces (1 band + 2 crescents) instead of 5.
  - The band's tab sat well right of centre.
- Everything else passed: same character, hair off the forehead, bare face, lips closed, 5 fingers per hand, free hand on frame-right by the nightstand, lamp right, no mirror or text, 9:16.
- Her apparent age reads early-to-mid 30s. The owner chose to keep her as she is.
- Local file: `.../stills-1t/K1/K1_NIGHT_ID.png`

## K1_NIGHT_ID (fix, owner-approved "Yes, fix the tray"): PASS ✅. This is the identity frame.

- Generation ID: **`91d6abc0-eb0a-4f1c-bce6-b2a663bbaf69`**. This is an edit of 712c622b with both Elements in the text.
- Credits: 1.5 (preflight 1.5, count 1). Balance 1198.5 → 1197.
- Local file: `.../stills-1t/K1_fix/K1_NIGHT_ID_fix.png` (768×1376)

| Check | Result | Notes |
|---|---|---|
| Same person as v1 (face, skin, hair, huggies), unchanged | ✅ | Face, expression, T-shirt, hands, phone, lamp and framing are unchanged from v1. |
| Hair fully off the forehead | ✅ | |
| Pieces clear and frosted, not opaque | ✅ | Pale frosted silicone with lit raised edges on teal. Slightly milky, acceptable at this size. |
| Count: 5 on one film | ✅ | 1 forehead band and 4 identical slim crescents in two side-by-side pairs. |
| Forehead tab DOWN, centred | ✅ ⚠️ | The tab points down. It sits about 5–10% right of the band's exact middle and has a slightly hooked shape. That's about 4 px at native size on a background tray, so it doesn't read at phone size. Much better than v1, where the tab was at about 70% across. |
| Crescents, not circles | ✅ | |
| Whole tray in frame | ✅ | The right rim is visible with wood beyond it. |
| Bare face, lips closed, neutral | ✅ | |
| No mirror, cream or text | ✅ | |
| Five fingers per visible hand | ✅ | Phone hand: thumb and 4 fingers. Duvet hand: 5 fingers. |
| Free hand on frame-right (nightstand side) | ✅ | |
| Early lines visible | ✅ | Frown line and faint forehead lines. Eye crinkle is faint. |
| 9:16, readable at phone size | ✅ | |

## K2_POV_GROUP: FAIL ❌

- Generation ID: `6bbee4ea-14fd-480e-948d-d63b5b9cb8db`. The `image_references` media was K1 = 91d6abc0.
- Credits: 2 (preflight 2, 2k, count 1). Balance 1197 → 1195.
- Local file: `.../stills-1t/K2/K2_POV_GROUP.png` (1536×2752)

| Check | Result | Notes |
|---|---|---|
| **Four distinct friends** | ❌ | **Only 3 friends, so 4 people in total instead of 5.** |
| **Friends don't share her face** | ❌ | The far-right friend looks like a younger version of her: same dark hair, similar face shape and nose, and gold hoop earrings. The friend second from left also wears gold hoops. The far-left friend has a similar dark-brunette look. Only the second friend has a clearly distinct skin tone. |
| Same person as K1 | ✅ ⚠️ | She's recognisably K1, with slicked-back dark hair and gold huggies. Laughing makes her look older (mid-to-late 30s) and deepens the eye crinkles. That's acceptable for a laughing hook frame, but noted. |
| She is centre-right and closest, face about 1/3 of frame width | ⚠️ | Her face is about 28% of the width, but she sits roughly centre and not clearly closest. The friends are on the same plane. |
| Her lines visible (frown, forehead, eye crinkle) | ✅ | Clear forehead lines and crow's feet. The frown line is softened by the laugh. |
| Friends' skin smooth | ✅ | |
| Hands: 5 fingers, nobody's hand on her face | ✅ | Visible hands are on arms and shoulders, never her face. The finger counts look right. |
| Black top, hair back, gold huggies | ✅ | |
| Rooftop at night, string lights, city bokeh, cake and glasses | ✅ | |
| No eyeglasses, no product, no mirror, no text | ✅ | |
| 9:16 | ✅ | |

**Why it fails:** the storyboard's hook and the FILTER | ME beat need her to stand out as the one with lines among four smooth-skinned friends who clearly aren't her. With only three friends, and one of them looking like her, the comparison is muddy.

**Proposed fix (needs owner OK, 1 edit, preflight about 2 credits at 2k):** one nano_banana_2 edit of K2 (`medias: [{role: image_references, value: 6bbee4ea-14fd-480e-948d-d63b5b9cb8db}]`, 2k, 9:16, count 1). Prompt: REFERENCE ROLES, then "THE CAST PHOTO is this group photo and it is the image to edit. Keep everything as placed: the woman with her hair slicked back in the centre (her face, lines, gold huggies, black top), the rooftop, string lights, flash look, cake, glasses and framing. CHANGES ONLY: there are exactly four friends around her, so five women in total. Add a fourth friend squeezed in behind her, between her and the friend on the right. Change the friend on the far right so she clearly does not resemble the centre woman: short wavy auburn hair, fair freckled skin, no earrings. The other friends wear no gold hoop earrings; only the centre woman wears gold huggies. Each friend has her own distinct face, hair colour and skin tone. Every person has exactly two arms and two hands with five fingers each; nobody's hand is on her face. Nobody wears eyeglasses." Then STYLE. Budget after the fix: 7.0 spent and 110.5 still estimated for K3–K7 and the clips, so 117.5 ≤ 120.

## K2_POV_GROUP (fix, owner-approved "Yes, fix and continue"): PASS ✅ with one note

- Generation ID: **`91d09592-2072-4ca3-84de-d0b15a1830cb`**. This is an edit of 6bbee4ea.
- Credits: 2 (preflight 2, 2k, count 1). Balance 1195 → 1193.
- Local file: `.../stills-1t/K2_fix/K2_POV_GROUP_fix.png` (1536×2752)

| Check | Result | Notes |
|---|---|---|
| Four distinct friends (5 women in total) | ✅ | A fourth friend was added behind her, between her and the right friend: light-brown hair and a distinct face. The edit was clean, with no extra limbs. |
| Friends don't share her face | ✅ | Far left: brunette with a round face and fair skin. Second: deep skin tone and long black hair. Back: light brown hair. Far right: short wavy auburn hair, fair and freckled, no earrings. None of them reads as her. |
| No gold hoops on any friend | ⚠️ | **Missed for the second friend, who still wears a small gold hoop.** Her face and skin tone are clearly different, so it doesn't create a lookalike. This could be fixed in code (a small retouch in the push-in crop) or left as is; the owner decides. |
| She (K1) unchanged | ✅ | Same as v1: slicked-back dark hair, gold huggies, black top. |
| She's centre-right and closest, face about 1/3 of frame width | ⚠️ | Her face is about 28% of the width, but she's still roughly centre and level with the side friends. Enough for the push-in. |
| Her lines visible | ✅ | Forehead lines and crow's feet are clear. |
| Hands: 5 fingers, none on her face | ✅ | The hands on her arms and shoulder read correctly. The added friend's hands are out of view. |
| Rooftop, string lights, cake, glasses; no eyeglasses, product, mirror or text; 9:16 | ✅ | |

## K3_SLEEP: PASS ✅

- Generation ID: **`f0d61ae3-a6a7-4172-a518-e9586bda1c00`**. The `image_references` media was K1 = 91d6abc0.
- Credits: 1.5 (preflight 1.5, count 1). Balance 1193 → 1191.5.
- Local file: `.../stills-1t/K3/K3_SLEEP.png` (768×1376)

| Check | Result | Notes |
|---|---|---|
| Same person as K1 | ✅ | Slicked-back dark hair, gold huggie, light olive skin, same features. |
| Asleep on her side facing the camera; cheek, eye corner and side of forehead in the pillow | ✅ | |
| Sleep creases where the skin folds | ✅ ⚠️ | Visible but subtle: soft folds under the lower eye and cheek at the pillow contact. The code push-in will help them read. |
| Eyes closed, lips closed, relaxed | ✅ | |
| Duvet to the shoulder, no phone, no hands | ✅ | No hand is visible, so there's nothing to count (review note 3). |
| Lamp warm; nightstand and teal tray with pieces small in the background | ✅ | The lamp is still fairly bright rather than "dimmed", but it's warm and acceptable. |
| Bare face, no patches; no mirror or text; matte skin; unretouched with visible pores | ✅ | |
| 9:16 | ✅ | |

## K4_PRESS_ON: FAIL ❌

- Generation ID: `9d36306f-d048-43c1-88c0-79d02d58400e`. The `image_references` media was K1 = 91d6abc0, with Elements 6375c707 and 9d766c06 in the prompt.
- Credits: 1.5 (preflight 1.5, count 1). Balance 1191.5 → 1190.
- Local file: `.../stills-1t/K4/K4_PRESS_ON.png` (768×1376)

| Check | Result | Notes |
|---|---|---|
| Same person as K1; T-shirt, room, lamp, framing | ✅ | |
| Organic press-on: eyes on the phone, right fingertips pressing the band at its centre | ✅ | She looks down at the phone and three fingertips press the band. Natural. |
| Forehead band: tab DOWN between the brows, middle two-thirds, not reaching the hairline | ✅ | |
| Clear and frosted, not opaque | ✅ | |
| **Under-eye pieces are slim crescents just below the lashes; never circles or glasses** | ❌ | **They're wide half-moon pads, not slim crescents. Under her left eye (frame-right), the piece's outline also arcs up around the outer eye corner toward the brow, which reads as a ring or glasses outline.** This is the known failure in lessons §8. |
| **Smile-line pieces are slim crescents along the fold; lips uncovered** | ❌ | They're comma or teardrop blobs at the nostril-to-mouth-corner area, not slim crescents along the fold. The lips are uncovered. |
| Count on face: exactly 5 | ✅ | |
| Lips closed, not smiling | ✅ | |
| Five fingers per hand | ✅ | Pressing hand: 4 fingers and the thumb behind. Phone hand: correct. |
| Tray empty | ✅ | The nightstand top is out of frame, so no tray shows (nothing contradicts "empty"). |
| No mirror, cream or text; 9:16 | ✅ | |

**Why it fails:** K4 is the only patch-on frame in the video, and the product has to be drawn right in it. Wrong-shaped under-eye and smile-line pieces misrepresent the Face Set, and the ring-like outline is exactly the failure the PATCHES block was written to prevent.

**Proposed fix (needs owner OK, 1 edit, preflight about 1.5 credits):** one nano_banana_2 edit of K4 (`medias: [{role: image_references, value: 9d36306f-d048-43c1-88c0-79d02d58400e}]`, 1k, 9:16, count 1). Keep the same sheet line with both Elements and the PATCHES block verbatim, then: "THE CAST PHOTO is this image and it is the image to edit. Keep everything as placed: her face, pose, eyes on the phone, both hands, the phone, the forehead band and its position, the lamp light, T-shirt, room and framing. CHANGES ONLY: replace the four lower pieces with the slim crescents of <<<9d766c06-2818-43e8-8ec4-1aac02d63897>>>. Under each eye: one slim crescent, narrow like a fingernail clipping, lying just below the lower lashes and following the curve of the lower lid, its outer end pointing toward the outer eye corner; no edge or outline goes above the eye or around the eye corner; never a circle, ring, half-moon pad or glasses shape. Along each smile line: one slim crescent of the same shape lying along the fold from beside the nostril down to beside the mouth corner; the lips stay uncovered. Exactly five pieces on her face." Then STYLE. Budget: 10.0 is spent so far. The rest of the plan (K5, K6, K7 = 4.5; clips = 105) is 109.5, so the projection without this fix is 119.5 ≤ 120. **With this fix it becomes 121, which is 1 credit over the first-pass limit (135 − 15).** That 1 credit would come from the retry reserve; the hard cap of 135 still holds. This needs the owner's explicit OK to draw on the reserve.

**Note for the owner:** K5 and K6 edit K1 only, and K7 edits K6. None of them depends on K4. With the owner's OK, Stage A can go on with K5 to K7 whether or not K4 is fixed. I didn't do this, because the instruction was to stop at the failed still.

## K4_PRESS_ON fix (owner rule `still_fix_credits_auto: 3`): FAIL ❌. Stage A stopped.

- Generation ID: `02a0082c-acd1-43d7-a34c-850d33ec389a`. This is an edit of 9d36306f, with both Elements and the proportion wording "7.8 × 2.2 cm, 3.5× longer than wide, fingernail clipping; never a half-moon pad, bean, teardrop, circle, ring or glasses shape".
- Credits: 1.5 (preflight 1.5, count 1). Balance 1190 → 1188.5. Still-fix allowance used: 1.5 of 3.
- Local file: `.../stills-1t/K4_fix/K4_PRESS_ON_fix.png`

| Check | Result | Notes |
|---|---|---|
| Under-eye: slim crescents, no edge above or around the eye corner | ❌ | They're still wide half-moon pads, about 2:1 rather than 3.5:1. The ring arc above her left eye corner is gone, which is better than v1, but the shape is still wrong. |
| Smile-line: slim crescents along the fold | ❌ | Still teardrop or comma blobs, almost unchanged from v1. |
| Everything else (person, band with tab DOWN, 5 pieces, lips closed and not smiling, hands, light, framing) | ✅ | Unchanged from v1. |

**Cause:** an edit of a still with wrong-shaped pieces keeps their footprint. The source image outweighs the proportion text. This is logged in `learning/production-log.md`.

**Proposed fix (needs owner OK, because the rule stops after one fix per still):** rebuild K4 fresh from the clean K1 rather than editing the bad still. Use the prompts.json K4 prompt as it stands (`medias: K1 = 91d6abc0`, both Elements, 1k, count 1) and insert the COUNT AND SHAPE sentence from K5 right after "Already on: …": "Each crescent is about 7.8 × 2.2 cm, about three and a half times longer than it is wide, narrow like a fingernail clipping; under each eye it lies just below the lower lashes with no edge above or around the eye corner; never a half-moon pad, bean, teardrop, circle, ring or glasses shape." It costs 1.5, which uses the last 1.5 of the allowance. The projection becomes 122.5: still ≤ 135, but 2.5 over the first-pass limit of 120, drawn from the reserve.

**Fallback (no credits):** in the edit, push in to a tight crop of the forehead band and the pressing fingers, cutting off below the brows. The band and tab are correct in both K4 versions. This loses the "full set on" read for those 3.5 s.

## K5_SHEET_HOLD to K7_YESTERDAY: not generated

These depend only on K1/K6, not on K4, but the rule says to stop when a fix fails. No credits spent. The K5 prompt already has the COUNT AND SHAPE sentence.

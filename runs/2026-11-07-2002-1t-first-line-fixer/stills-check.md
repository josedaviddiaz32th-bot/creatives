# Stills check (gate A): 2026-11-07-2002-1t-first-line-fixer

Producer, Stage A only. Owner rules: one generation per shot (count 1), no automatic redo, stop at the first failed still.
Balance before: 1200. Balance after: 1176.5. Spent: 23.5 (budget.json `actual_total`). Still-fix allowance (`still_fix_credits_auto`): **3.0 of 3 used** (K4 fix and K5 fix). The K5 rebuild was approved separately by the owner ("Yes, rebuild and continue").

**Status now: STAGE A COMPLETE. All 7 stills are approved.**

| Keyframe | Approved generation ID |
|---|---|
| K1_NIGHT_ID | `91d6abc0-eb0a-4f1c-bce6-b2a663bbaf69` |
| K2_POV_GROUP | `91d09592-2072-4ca3-84de-d0b15a1830cb` |
| K3_SLEEP | `f0d61ae3-a6a7-4172-a518-e9586bda1c00` |
| K4_PRESS_ON | `02a0082c-acd1-43d7-a34c-850d33ec389a` (owner-accepted) |
| K5_SHEET_HOLD | `4576bff3-729e-4096-afcc-a16ec4389720` |
| K6_TODAY | `fe37523b-b596-425d-be03-5369cfbb7d8a` (pair rebuild; replaces b4e64508) |
| K7_YESTERDAY | `d21e9014-d6cf-4db6-a005-100099a168b4` (pair rebuild: relight of K1) |

**Important for the clip stage and assembly:** K6 and K7 were rebuilt as a pair. K7 is a relight of K1 and K6 is an edit of the new K7. Both share K1's framing, and neither is built on the old K6 `b4e64508`. The next step is prompt-reviewer pass 2 on the actual stills, before any clip.

Side-by-side crops: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/sidebyside/`

| Still | Generation ID | Credits | Verdict |
|---|---|---|---|
| K1 v1 | 712c622b-31b0-4425-a939-293e6c64afa5 | 1.5 | ❌ superseded |
| **K1 (fix)** | **91d6abc0-eb0a-4f1c-bce6-b2a663bbaf69** | 1.5 | ✅ |
| K2 v1 | 6bbee4ea-14fd-480e-948d-d63b5b9cb8db | 2 | ❌ superseded |
| **K2 (fix)** | **91d09592-2072-4ca3-84de-d0b15a1830cb** | 2 | ✅ (1 note) |
| **K3** | **f0d61ae3-a6a7-4172-a518-e9586bda1c00** | 1.5 | ✅ |
| K4 v1 | 9d36306f-d048-43c1-88c0-79d02d58400e | 1.5 | ❌ |
| **K4 (fix)** | **02a0082c-acd1-43d7-a34c-850d33ec389a** | 1.5 | ✅ owner-approved as is |
| K5 v1 | 2b3b35f6-a4ec-41f4-8df4-7f01998187e8 | 1.5 | ❌ |
| K5 fix | f7bdded8-3f73-4641-a013-b05cb77043c6 | 1.5 | ❌ |
| **K5 (rebuild from K1)** | **4576bff3-729e-4096-afcc-a16ec4389720** | 1.5 | ✅ |
| K6 v1 | 7de6281d-1bd4-4d1a-80fa-563d13196ec6 | 1.5 | ❌ |
| K6 fix | b4e64508-bf5e-482b-a2c0-8484357a02ff | 1.5 | owner-accepted, then replaced by the pair rebuild |
| K7 v1 | f8e52cb0-9ab3-4478-9057-c3b5f77db762 | 1.5 | ❌ |
| **K7 YESTERDAY (pair rebuild: relight of K1)** | **d21e9014-d6cf-4db6-a005-100099a168b4** | 1.5 | ✅ |
| **K6 TODAY (pair rebuild: edit of new K7)** | **fe37523b-b596-425d-be03-5369cfbb7d8a** | 1.5 | ✅ (replaces b4e64508) |

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

## K4_PRESS_ON fix (owner rule `still_fix_credits_auto: 3`): APPROVED ✅ by owner override ("K4 looks good to me, keep it")

**Owner decision:** the plumper crescents, as in the Eye-patches Element, are acceptable. From here on a still fails only for a full circle, a ring around the eye corner, a glasses shape, or the wrong count. My original gate check is kept below for the record.

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

## K5_SHEET_HOLD v1: FAIL ❌

- Generation ID: `2b3b35f6-a4ec-41f4-8df4-7f01998187e8`. The `image_references` media was K1 = 91d6abc0, with both Elements. The prompt was the current prompts.json version, ending with COUNT AND SHAPE.
- Credits: 1.5 (preflight 1.5, count 1). Balance 1188.5 → 1187.
- Local file: `.../stills-1t/K5/K5_SHEET_HOLD.png`

| Check | Result | Notes |
|---|---|---|
| Same person as K1; room, lamp, T-shirt, framing | ✅ | |
| **Film holds exactly 5 pieces** | ❌ | **Only 3: the band and 2 crescents.** |
| **Tray empty** | ❌ | **2 crescents are still on the teal tray.** |
| Band tab DOWN, centred | ✅ | |
| Crescents: no circle, ring or glasses shape | ✅ | The plumper Element shape, which the owner has accepted. |
| Clear, frosted, edges catching the lamp | ✅ | |
| Film beside her right cheek toward the lens, not touching her face | ✅ | It's held in her frame-right hand on the nightstand side, which matches B2's reach. |
| Left hand holds the phone low | ✅ | Chest height. |
| Eyes to the lens, lips parted mid-sentence, bare face | ✅ | |
| Five fingers per hand | ✅ | |
| No mirror, cream or text; 9:16 | ✅ | |

## K5_SHEET_HOLD fix (auto, still-fix allowance): FAIL ❌. Stage A stopped.

- Generation ID: `f7bdded8-3f73-4641-a013-b05cb77043c6`. This is an edit of 2b3b35f6: "the two crescents that are on the teal tray move onto the film… exactly five pieces on the film, zero on the tray".
- Credits: 1.5 (preflight 1.5, count 1). Balance 1187 → 1185.5. Still-fix allowance now 3.0 of 3.
- Local file: `.../stills-1t/K5_fix/K5_SHEET_HOLD_fix.png`
- **Result:** almost identical to v1. The film still holds 3 pieces and the tray still holds 2 crescents. Everything else is unchanged and still passes.
- **Cause:** for the second time, editing a bad still can't move or redraw small product pieces. "Keep everything as placed" plus a near-identical source returns the source. Logged in `learning/production-log.md`.

**Proposed options (owner decides; the allowance is used up):**
1. **Rebuild K5 from the clean K1** (`91d6abc0`, both Elements, 1k, count 1, about 1.5 credits). Put the move and the count up front in CHANGES ONLY: "her right hand has lifted the whole clear film off the tray: all five pieces are on the film in her hand (the band on top, four crescents below in two rows of two), and the teal tray on the nightstand is bare and empty." Keep the rest of the current prompt.
   - Projection: 16.0 + 3.0 (K6, K7) + 105 = 124 ≤ 135, drawing 4 from the reserve.
2. **No credits:** accept the 3-piece film and deal with the tray in code or the clip.
   - The 3-piece film is clean and true to the product, just a subset.
   - B2's end frame would then show 2 crescents left on the tray. B2's prompt ("picks up the clear backing film with the five clear pieces… exactly five pieces") would need to change to "picks up the film", and the tray could be cropped or masked in assembly.
   - This needs a prompt-reviewer pass-2 change to CLIP_B2.

**Note:** K6 and K7 don't depend on K5. K6 edits K1 and K7 edits K6. With the owner's OK they can run now (3.0 credits).

## K5_SHEET_HOLD rebuild (owner-approved "Yes, rebuild and continue"): PASS ✅

- Generation ID: **`4576bff3-729e-4096-afcc-a16ec4389720`**. This is a fresh build from K1 = 91d6abc0, with both Elements. It is not an edit of the bad K5. The prompt is the prompts.json K5 text with this added at the start of CHANGES ONLY: "her right hand has lifted the whole clear film off the tray: all five pieces are on the film in her hand (the band on top, four crescents below in two rows of two), and the teal tray on the nightstand is bare and empty."
- Credits: 1.5 (preflight 1.5, count 1). Balance 1185.5 → 1184.
- Local file: `.../stills-1t/K5_rebuild/K5_SHEET_HOLD_rebuild.png`

| Check | Result | Notes |
|---|---|---|
| Same person as K1; room, lamp, T-shirt, framing | ✅ | |
| Film holds exactly 5 pieces | ✅ | The band on top and 4 crescents in two rows of two. |
| Band tab DOWN | ✅ | It sits a little right of centre, as in K1. |
| Crescents: no circle, ring or glasses shape | ✅ | The accepted plumper Element shape. |
| Clear, with lit raised edges | ✅ | |
| Tray bare and empty | ✅ | |
| Film beside her right cheek toward the lens, not touching her face, on the nightstand side | ✅ | This matches CLIP_B2's lead action and end frame. |
| Left hand holds the phone low | ✅ | Chest height (review note 5). |
| Eyes to the lens, lips parted mid-sentence, bare face | ✅ | |
| Five fingers per hand | ✅ | The film hand shows 4 fingers with the thumb behind the film. |
| No mirror, cream or text; 9:16 | ✅ | |

## K6_TODAY: FAIL ❌

- Generation ID: `7de6281d-1bd4-4d1a-80fa-563d13196ec6`. The `image_references` media was K1 = 91d6abc0, with Element 6375c707.
- The prompt is the prompts.json K6 text with one change, applying the logged K5 lesson: "The teal tray on the nightstand is empty." became "The teal tray on the nightstand is bare and empty: nothing is left on it, and the backing film and the four crescents are nowhere in the image."
- Credits: 1.5 (preflight 1.5, count 1). Balance 1184 → 1182.5.
- Local file: `.../stills-1t/K6/K6_TODAY.png`

| Check | Result | Notes |
|---|---|---|
| Same person as K1 | ✅ | |
| Morning: lamp off, soft daylight from a window on the right | ✅ | |
| **Lines visibly softer than K1, still present, same places** | ❌ | **Not softer.** Side by side at the same scale, her frown line and horizontal forehead lines read the same as K1 or slightly deeper, because the window daylight rakes the skin texture. This is the TODAY beat. K7 restores K1's depth, so the end card would show no difference, or the "after" looking worse. |
| Exactly one piece; no film; nothing on her face | ✅ | Only the forehead band, held in her fingers. |
| Band clear and slightly frosted, thin, soft and curved | ⚠️ | It reads as a thick, milky, frosted slab held stiffly upright, not a thin, see-through sheet hanging softly. Her fingertips barely show through it. Borderline "opaque / gel pad". |
| Only her right hand visible, five fingers | ✅ | 4 fingers with the thumb behind the band. Her other hand is out of frame. |
| Band and fingers beside her face, not covering eye corner, temple or forehead lines | ✅ | Held clear of her face at cheek and temple height (review note 1). |
| Teal tray empty | ✅ | Bare teal, partly behind her elbow. |
| Lips closed, neutral, eyes to the lens | ✅ | |
| Framing like K1 | ✅ ⚠️ | Head and shoulders, slightly closer and tighter than K1. Fine for the end-card halves. |
| No mirror, cream or text; 9:16 | ✅ | |

**Why it fails:** K6 is the "TODAY" half of the YESTERDAY | TODAY end card. Its only job is lines visibly softer than K1 but still there. As generated it shows no improvement, so the before/after can't work, and K7 would inherit the same light and framing.

**Proposed fix (needs owner OK, because the allowance is used up; 1 edit, about 1.5 credits):** one nano_banana_2 edit of K6.
- Medias: `image_references` 7de6281d (the image to edit) and 91d6abc0 (THE CAST PHOTO, the line-depth reference only). 1k, 9:16, count 1, with Element 6375c707 kept in the text.
- Prompt text: "Keep everything as placed in THE MORNING PHOTO: her face, expression, eye line, hair, earrings, T-shirt, the right hand and its position, the window, the empty tray and the framing. CHANGES ONLY: the daylight is soft, diffuse and even, not raking. Her frown line, forehead lines and the crinkling at the outer eye corners are still there in the same places, but noticeably shallower and fainter than in THE CAST PHOTO, about half as visible, not erased and not airbrushed, with pores and texture kept. The band in her fingers is a thin, flexible, see-through clear sheet about 1 mm thick that droops softly in a gentle curve between thumb and index finger; the wall behind shows through it; small rounded tab at the centre of one long edge." Then STYLE.
- Projection: 17.5 + 1.5 (K6 fix) + 1.5 (K7) + 105 = 125.5 ≤ 135.

**K7 note:** once K6 is approved, K7 is ready to run as written in prompts.json. It edits K6 with K1 as the line reference, restoring lines to K1 depth, never deeper. If K6 is fixed with diffuse light, K7 inherits that light, which keeps the two halves like for like.

## K6_TODAY fix (owner-approved "Yes, fix K6"): APPROVED ✅ by owner override ("Yes, accept K6", band as is)

My gate check is kept below for the record.

- Generation ID: `b4e64508-bf5e-482b-a2c0-8484357a02ff`. This is an edit of 7de6281d, with K1 91d6abc0 as the line-depth reference only and Element 6375c707 in the text.
- Credits: 1.5 (preflight 1.5, count 1). Balance 1182.5 → 1181.
- Local file: `.../stills-1t/K6_fix/K6_TODAY_fix.png`
- Side by side at matched scale, normalised by eye distance (K6's face is about 1.33× larger in frame than K1's): `.../sidebyside/sbs_samescale_K1_K6v1_K6fix.png`, with K1, K6 v1 and K6 fix left to right.

| Check | Result | Notes |
|---|---|---|
| Light soft, diffuse and even (not raking) | ⚠️ | A little softer than v1, but still the same bright window light. |
| Frown line softer than K1 | ✅ | Clearly softer than K1's bunched night frown. |
| Forehead lines softer than K1 | ⚠️ | About equal or slightly fainter. |
| **Eye-corner and under-eye crinkles softer than K1** | ❌ | **More visible than in K1.** The sharper daylight render shows fine crinkles that K1's warm lamp hid. |
| **TODAY reads clearly softer than K1 overall** | ❌ | Mixed: the brow is better and the eyes are worse. It isn't the clear "softer" the end card needs. |
| **Band is a thin, flexible, see-through sheet drooping between thumb and finger** | ❌ | **Essentially unchanged from v1:** a thick, milky slab held stiffly upright. This is the third edit that failed to redraw a product piece. |
| Exactly one piece, no film; only her right hand with 5 fingers; tray bare; band clear of eye corner, temple and forehead | ✅ | |
| Same woman, lips closed, eyes to the lens, morning window light | ✅ | |

**Correction to the K6 v1 check:** I compared v1 to K1 at mismatched scale. At matched scale, v1's frown was also softer than K1, but its forehead lines and eye crinkles read stronger. So v1's verdict, "not visibly softer overall", still stands.

**Root cause:** K1 is night and lamp-lit, while K6 and K7 are morning. Daylight and a sharper render show fine texture that the warm lamp smoothed, so "softer than K1" fights the change of light. What the viewer actually sees is **K7 next to K6**: both in morning light, with the same framing, and K7 restoring K1's line depth.

**Options for the owner (no more fixes without OK):**
1. **Accept K6 fix `b4e64508` as TODAY and run K7 as written** (1.5 credits). The end card compares K7 and K6, not K1. If K7 restores K1-depth lines in the same morning light, the frown difference carries the before/after. Gate K7 against both K1 (never deeper) and K6 (clearly deeper than K6). If K7 doesn't read clearly more lined than K6, stop.
2. **Rebuild K6 fresh from K1** (about 1.5 credits, plus 1.5 for K7). Use soft overcast morning light and give the band as "a thin flexible see-through sheet drooping between her fingers" from the start, not as an edit.
3. **Swap the held band in code** for the clean band from K5 or the studio shot `f3fbd28d`. This fixes only the band look, not the lines.

Projection with option 1: 19.0 + 1.5 + 105 = 125.5 ≤ 135. With option 2: 127.0 ≤ 135.

## K7_YESTERDAY v1: FAIL ❌ (superseded by the pair rebuild)

- Generation ID: `f8e52cb0-9ab3-4478-9057-c3b5f77db762`. The prompt was the prompts.json K7 text, unchanged. Medias: `image_references` K6 = b4e64508 (the image to edit) and K1 = 91d6abc0 (line reference).
- Credits: 1.5 (preflight 1.5, count 1). Balance 1181 → 1179.5.
- Local file: `.../stills-1t/K7/K7_YESTERDAY.png`
- Side-by-side crops, in `.../sidebyside/`:
  - `sbs_full_K7_K6.png`: the full frames, K7 | K6, as the end card would use them.
  - `sbs_samescale_K7_K6.png`: matched scale, K7 | K6.
  - `sbs_samescale_K1_K7_K6.png`: matched scale, K1 | K7 | K6.
  - `sbs_samescale_K1_K7.png`: K1 | K7. This one was cropped before I corrected K7's scale, so it's slightly off.

| Check | Result | Notes |
|---|---|---|
| **K7 clearly more lined than K6 (frown, forehead lines)** | ❌ | **At matched scale they look practically the same.** K7's frown is perhaps a touch more visible, and the forehead lines are equal. The YESTERDAY \| TODAY card would show no difference. |
| **Lines restored to K1 depth** | ❌ | Much softer than K1. Not restored. |
| Never deeper than K1 | ✅ | |
| Same morning window light as K6 | ✅ | |
| **Same framing and camera distance as K6** | ❌ | Wider: her face is about 0.88× K6's scale, with more room and the lamp in view. Could be matched by cropping in code. |
| No band, no hand | ✅ | Both arms are down and no piece shows. |
| Tray bare and empty | ⚠️ | Empty, **but a second, duplicate teal tray** appears behind her arm. |
| Same woman; lips closed; eyes to the lens | ✅ | |
| No mirror or text; 9:16 | ✅ | |

**Cause (logged):** the model won't **add** line depth by editing a smooth frame, even with a reference in a different light. It keeps the edited image's skin. Removing the hand also let the framing drift.

**Proposed fix (needs owner OK, about 3.0 credits, two jobs, one output each).** Rebuild the pair the other way round, so lines only ever get softened:
1. **YESTERDAY = relight of K1**, as an edit of 91d6abc0: "Keep her face, skin and every line exactly as they are — the frown line, forehead lines and eye-corner crinkling at the same depth. CHANGES ONLY: it is morning, the lamp is off, and the only light is soft, diffuse daylight from a window on the right. No phone: both hands are lowered out of frame. The teal tray on the nightstand is bare and empty: nothing on it, one tray only. Neutral, relaxed expression, eyes to the lens, lips closed." Then the STYLE block. Gate it against K1 at matched scale: same depth, never deeper.
2. **TODAY = edit of that new YESTERDAY**: "Keep everything as placed. CHANGES ONLY: her lines are noticeably softer, about half as visible, same places, not erased; her right hand holds the clear forehead band beside her face at temple height…" Use K6's band text with Element 6375c707 and the PATCHES block. Softening by edit did work for the frown in the K6 fix.

The two halves then share light and framing by construction. K6 `b4e64508` would be replaced as TODAY. The owner should also decide whether the band is acceptable as the model draws it.

Projection: 20.5 + 3.0 + 105 = 128.5 ≤ 135.

**Zero-credit alternative:** a code-only end card of K1 | K6, night next to morning. The light changes, but the frown difference is clear. Lessons and the storyboard flag the risk of an unequal or rigged comparison, so this needs the owner's call.

## Pair rebuild (owner-approved "Rebuild the pair"): K7 YESTERDAY ✅ and K6 TODAY ✅

Side-by-side crops, in `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/sidebyside/`:
- `sbs_full_YESTERDAYnew_TODAYnew.png`: the full end-card halves, YESTERDAY | TODAY.
- `sbs_samescale_K1_YESTERDAY_TODAY.png`: matched scale, K1 | new YESTERDAY | new TODAY.
- `sbs_samescale_K1_YESTERDAYnew.png`: matched scale, K1 | new YESTERDAY.

### K7_YESTERDAY: relight of K1. PASS ✅

- Generation ID: **`d21e9014-d6cf-4db6-a005-100099a168b4`**. This is an edit of K1 = 91d6abc0.
- Credits: 1.5 (preflight 1.5, count 1). Balance 1179.5 → 1178.
- Local file: `.../stills-1t/K7_rebuild/K7_YESTERDAY_rebuild.png`

| Check | Result | Notes |
|---|---|---|
| Lines match K1's depth, never deeper | ✅ | At matched scale (same eye distance as K1, 105 px), the frown creases and forehead lines match K1. Not deeper. |
| Morning: lamp off, soft diffuse daylight from the right | ✅ | |
| Same framing and camera distance as K1 | ✅ | Identical scale and position. |
| Phone gone; hands down | ✅ ⚠️ | The backs of both hands rest on the duvet at the bottom edge, with the fingers out of frame. Nothing is malformed, and it's outside the end-card face crop. |
| One teal tray, bare and empty | ✅ | No duplicate. |
| Same woman, T-shirt, hair, huggies; neutral; lips closed; eyes to the lens | ✅ | |
| No patch, mirror or text; 9:16 | ✅ | |

### K6_TODAY: edit of the new YESTERDAY. PASS ✅

- Generation ID: **`fe37523b-b596-425d-be03-5369cfbb7d8a`**. This is an edit of d21e9014, with Element 6375c707 and the PATCHES block with its off-face notes.
- Credits: 1.5 (preflight 1.5, count 1). Balance 1178 → 1176.5.
- Local file: `.../stills-1t/K6_rebuild/K6_TODAY_rebuild.png`

| Check | Result | Notes |
|---|---|---|
| Clearly softer than YESTERDAY (frown, forehead, eye crinkles) | ✅ | At matched scale, the frown creases are noticeably fainter and the forehead lines lighter. Still present, with pores kept and nothing airbrushed. |
| Same light, framing, wardrobe, tray and background as YESTERDAY | ✅ | Identical. The only differences are the lines and the raised hand with the band. |
| Exactly one piece (the forehead band); no film; nothing on her face | ✅ | |
| Band clear and frosted, curved, tab visible | ✅ | Frosted and translucent, with the edge catching the light. Thinner-looking than b4e64508. |
| Raised hand on the nightstand side, five fingers | ✅ | 4 fingers with the thumb behind the band. |
| Band and fingers don't cover her eye corner, temple or forehead | ✅ | Held beside her face, clear of the lines. |
| One tray, empty, no duplicate | ✅ | |
| Lips closed, eyes to the lens; no mirror or text; 9:16 | ✅ | |

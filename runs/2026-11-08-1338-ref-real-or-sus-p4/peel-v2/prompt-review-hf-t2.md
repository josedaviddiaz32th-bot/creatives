# Prompt review: HF_T2 (kling4_0 i2v, 720p, 4 s, 9:16, start S_PEEL_MID, end S_U2_END)

**Verdict: FIX** (three small wording edits; everything else is OK)

## Frames checked
- Start S_PEEL_MID: frame-left hand = two fingertips on the frame-left temple/brow beside the patch end; frame-right hand pinches the lifted frame-right end; tab down between brows; eyes open to camera; lips closed. Prompt matches (sides, hands, release direction right to left, last edge beside frame-left fingertips).
- End S_U2_END: forehead bare, no marks; frame-left hand gone; frame-right hand at about eye level holding the patch by its pinched end, sheet hanging vertical beside the frame-right cheek; closed-lip smile to camera. Prompt's 3.3-4.0 s beat matches.
- Timing 2.8 / 0.5 / 0.7 s fits 4 s. Guards present: no talking, two hands then one, hand tone, no redness, no milky/smeared/doubled patch, eyes open, no drop over eyes, no fold-back.

## FIX
| # | Problem | What Kling would do | Replacement |
|---|---|---|---|
| 1 | "pulls the pinched end outward, away from her forehead" | Reads as pulling toward the lens: a lift, the motion lessons §6 says breaks the patch and that lets the whole remaining sheet release and slide. Staging rule: pull sideways, in the image plane, off the edge of the face. | "pulls the pinched end sideways toward the frame-right side, low and close to the skin, past the edge of her face" |
| 2 | "slowly peels ... off her forehead" | Lessons §6: never "peels off" on its own. | "slowly pulls the clear silicone patch sideways off her forehead" |
| 3 | "carries it up and out ... then brings the patch to cheek height" | Up-then-down in 0.5 s is a busy two-move path; the end frame has the hand at eye level, patch hanging down beside the cheek. | "carries it out to the frame-right side, clear of her face, and holds it at eye height so it hangs down beside her cheek, as in the end frame" |

Optional (only if the Higgsfield Kling job exposes a negative prompt field): "patch sliding, patch falling over eyes, milky patch, extra hand, redness, talking, closed eyes".

## Corrected prompt
```
Motion only; the start frame and end frame set her, the clear forehead patch, the bedroom and the soft window light. Real, unedited phone video on a stand: camera almost still, no zoom, no cuts. She does not talk; her lips stay closed the whole time.
0–2.8 s: she slowly pulls the clear silicone patch sideways off her forehead, and it is clearly stuck to her skin. The fingertips of the hand on the frame-left side press firmly on her temple, holding the skin flat against the pull. The hand on the frame-right side pulls the pinched end sideways toward the frame-right side, low and close to the skin, past the edge of her face, slowly and in small stop-start tugs; that hand always stays inside the frame. With each tug the release line creeps a little further across her forehead from the frame-right side toward the frame-left side, at the same slow pace all the way to the last edge; it never speeds up and the rest of the patch never lets go all at once. The part still stuck stays perfectly in place and never slides, and the released part never sticks back down. Right at the release line her skin lifts a tiny bit with the silicone, then springs back flat as the edge lets go: a gentle, painless tug; her face stays relaxed, with no wince. The peeled part is soft and thin: it stretches slightly and ripples into small soft waves, with streaks of light moving across the ripples; it never stays flat and stiff, never folds back over the stuck part, and never slides down her face or over her eyes.
2.8–3.3 s: the last edge lets go beside the frame-left fingertips without touching them, with a small final tug, and the patch comes free in one piece. The frame-right hand carries it out to the frame-right side, clear of her face; the free patch never drops or swings down in front of her forehead, eyes or face, and hangs floppy from those fingers.
3.3–4.0 s: the frame-left hand lowers out of frame down the side of her face, and the frame-right hand holds the patch at eye height so it hangs down beside her cheek on the frame-right side, as in the end frame, while she looks into the camera with a calm, closed-lip, satisfied look.
Her skin stays its normal even tone, with no redness, marks or outline; once bare, her forehead does not change. Exactly one patch and one person; two hands with five fingers each until the frame-left hand leaves, then one; both hands keep the same skin tone as her face. The patch stays thin, transparent and slightly frosted the whole time: never milky, white, opaque, smeared, split or doubled. Her eyes stay open the whole time, glancing up toward the peeling hand, except natural blinks.
```

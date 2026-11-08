# Production log: craft lessons from our own runs

The `video-reviewer` adds a line for every defect it finds, and the
`producer` for every failed or wasted job: what went wrong, the prompt or
setting that caused it, and the fix that worked. The `prompt-engineer`
reads this with `docs/lessons-learned.md` sections 4–8 and 10. When the
same fix works twice, the owner may promote it into the lessons file.

| Date | Run | Clip / job | Defect | Cause | Fix that worked | Credits lost |
|------|-----|------------|--------|-------|-----------------|--------------|
| 2026-11-07 | 2026-11-07-2002-1t-first-line-fixer | K2_POV_GROUP (caught in prompt review, pre-credit) | Risk: friends cloned from her face in a group shot | Verbatim REFERENCE ROLES says the cast photo "shows the only person in this image", which contradicts a multi-person frame | Add after the block: "She is the only person taken from THE CAST PHOTO; the other people are different, with their own distinct faces, hair and skin tones" | 0 |
| 2026-11-07 | 2026-11-07-2002-1t-first-line-fixer | K6_TODAY (caught in prompt review, pre-credit) | Risk: extra backing film / pieces or wrong count | Off-face pre-block note copied from another still ("five pieces on their film") into a frame that shows only one piece; "keep everything as placed" also kept the full tray | Write the off-face note for the pieces actually in that frame, restate it after the PATCHES block, and state the tray's contents in every edit | 0 |
| 2026-11-07 | 2026-11-07-2002-1t-first-line-fixer | K1 → CLIP_B2 (caught in prompt review, pre-credit) | Risk: reach across body/face to pick up the product | Start frame didn't put her free hand on the same side of frame as the nightstand | In the start frame, state the free hand rests on the same side of frame as the object the clip reaches for | 0 |
| 2026-11-07 | 2026-11-07-2002-1t-first-line-fixer | K6_TODAY (caught in prompt review round 2, pre-credit) | Risk: a stray empty hand, or an invented object in it, carried into both halves of the before/after | The edit removed a held object ("No phone") without saying where the hand went; the next still (K7) kept "everything as placed" | When an edit takes an object out of a hand, say where that hand goes (e.g. "lowered out of frame"), and say how many hands are visible | 0 |

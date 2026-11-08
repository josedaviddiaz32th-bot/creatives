# Gemini peel iterations (free; owner: "keep trying gemini iterations until we find the prompt that gets these peels right")

| Take | Prompt | Result | Keep / change |
|---|---|---|---|
| T0 | VEO.txt (first Gemini try; the chat looked stuck but finished later) | Same pattern as T1: 0–1.6 s good creeping peel, then at ~1.8–2.2 s the remaining part lets go at once and slides down over her eyes, milky | Confirms the failure is the last ~40% of the peel |
| T1 | VEO_T1_fixed.txt (reviewed: prompt-review-veo-t1.md) | 0–2.0 s GOOD: the corner stretches under the pull, the release line creeps right→left with a curved stuck edge, and the peeled part frosts slightly, like the real video. 2.2–2.8 s FAIL: the remaining third lets go all at once, slides as one sheet and drops over her eyes, milky. Eyes closed ~1–2 s | Keep: start still, anchor hand, stop-start tug, stretch. Change: the whole peel over ~4 s, the last third creeps the same way, the free patch moves up/out (never down over the face), eyes open looking at her hand |
| T2 | VEO_T2.txt = the reviewed T1 plus 4 targeted edits (pace, last third, exit up/out, eyes). Main-session check against the T1 review list: sides, lips, sound, no-slide and injury wording unchanged | NOT RUN: Gemini's daily video limit was reached after T0 and T1 | Run when the quota resets |

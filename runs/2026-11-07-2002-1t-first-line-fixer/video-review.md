# Video review (stage 8): 2026-11-07-2002-1t-first-line-fixer (slot 1-T, TOF)

Reviewer: video-reviewer. Independent check of `final.mp4`. I inspected it **locally**, not through Higgsfield `sandbox_exec`, using ffprobe/ffmpeg at /opt/homebrew/bin and whisper-cli (small.en, with multilingual small as a second opinion). No paid calls, no edits to the video or to other stage files.

Read before reviewing: `.claude/agents/video-reviewer.md`, `pipeline/config.yaml`, `docs/creative-strategy.md` §2 and §6, `docs/lessons-learned.md` §0–3 and §10 (checklists B and C), plus `brief.md`, `story.md` v2, `storyboard.md`, `assembly.md`, `clips-check.md`, `stills-check.md`, `budget.json` and `learning/production-log.md`.

Work files: `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/review-1t/`
- `contact_1.png` and `contact_2.png`: 2 fps, 12 per row.
- `full/t_*.jpg`: full-res frames at every cut boundary.
- `j1.png` and `j2.png`: frame-by-frame strips of the K5 cover.
- `card.png`: the end card, face crop.
- `split9.png`: the FILTER | ME split.
- `k4.png`: the press-on still.
- `pack.png`: the packshot.
- `hands.png`: the B1 counting hand.
- `wh_*`: transcripts.

## VERDICT: **FAIL**

Four items score below `review.min_score_to_publish` (8): lip sync, continuity, the 8b checklists and story intent. **Claims are clean, and so is the budget.** Every fix below can be done **free in assembly**. No paid redo is needed, and none would fit anyway: a B1 or B2 redo costs 32.5–37.5 credits against 6.5 of headroom.

## Spec

| Check | Result |
|---|---|
| Duration | **41.96 s** (TOF 30–50 ✅) |
| Video | 1080×1920 (9:16 ✅), H.264, 24 fps |
| Audio | AAC 48 kHz stereo, present ✅ |
| Loudness (ebur128 on the final) | **−15.9 LUFS integrated**, true peak −1.5 dBFS, LRA 3.9 LU ✅ (target −16) |
| Music | None. SFX synthesized in ffmpeg ✅ |

## Transcript vs story.md

Whisper small.en on the full mix returns **all 88 words, in order**. Nothing is cut, garbled or added. The only difference: small.en hears "look **worse** right when you wake up". Multilingual `small`, run on 21–26 s, hears "**worst** right". That's connected-speech elision, so I count it as a match. The on-screen text reads "Worst when you wake up?".

## Scores

| # | Item | Score | Reason |
|---|---|---|---|
| 1 | Logic | **9** | Hook question (0.85–4.3 s) → problem (FILTER \| ME) → what she's tried → self-check loop → reveal over the sleeping still → product as the answer → before/after → "Comment PHOTO". A stranger can follow it, and both loops close. The CTA is clear and has its own beat. |
| 2 | Script fidelity | **9** | 88/88 words. "worst" is softened in delivery, but the second model confirms it. |
| 3 | Lip sync | **6** | Clips A, B1 and B2 track the speech wherever she's on camera. **But 30.79–32.08 is the K5 still**: a front-on talking face, eyes to the lens, lips parted and frozen, while her voice audibly says "So now I sleep in…" (speech 30.9–32.6 s by RMS envelope). That reads as a freeze-frame with live speech, i.e. talking with a frozen mouth. |
| 4 | Anatomy | **8** | Hands are fine everywhere I checked: B1 counting hand at 13.5–19.5 s, phone hand, K4 pressing hand, B2 holding hand. No melting. Teeth and eyes are fine. The B1 grimace at ≈16.4 s (mouth wide, deep scowl) is close to caricature but anatomically sound. |
| 5 | Continuity | **6** | Same woman, hair, huggies, T-shirt, bedroom and tray throughout, and the night clips match the K3/K4 cutaways in light. **Two visible jumps around the cover:** (a) 30.79: empty hand at the nightstand → film suddenly held at her cheek, with a punched-in frame; (b) 32.08, K5 → B2 rejoin: the film changes size, angle and position, and her mouth goes from parted to a smile. It reads as a stutter, not a cut on action. **B1 16.4–21.9 s:** deep frown and forehead furrows, deeper than any other frame of her, including the YESTERDAY half of the card. No glitch frame from B2 t5.8–7.3 appears: I checked frame by frame at 30.5–31.0 and 31.9–33.25 ✅. |
| 6 | Product | **8** | The tray with band + 4 crescents is on the nightstand from 1.5 s (small, no branding). The 5-piece film is held up with "The Wrinkle Smooth Face Set" on screen from 30.79. K4 on-face: band tab down, crescents, lips uncovered. The packshot (39.71–41.96) shows the correct band + 4 crescents with the brand name. Minor issues: in B2 32.08–33.17 the film reads larger than in K5; on the packshot, the "Comment PHOTO" box overlaps the bottom two crescents. There's no packaging, because no box reference exists (an accepted fallback). |
| 7 | Claims | **9 (clean)** | Spoken: "A lot of them get pressed in every night" (approved opener) and "They hold my skin flat all night" (approved mechanism). Before/after is allowed, AI included. Persona words only for tretinoin, vitamin C, peptides and Botox; no claim is made about those products. None of: credentials, statistics, reviews, "permanent/forever/for good", "11s", "8 hours", "rinse and dry". No price (N/A for TOF). Note: "No filter." sits on an AI-edited before/after. That's literally true (no filter applied in code) and allowed under the owner's AI before/after rule, but it only holds up with the platform's AI-content label on the post. |
| 8 | Budget | **10** | `actual_total` 128.5 ≤ `cap` 135. Assembly cost 0 credits. |
| 8b | Owner checklists B + C | **7** | One ❌ (wrinkle depth changes mid-clip in B1) and one marginal ⚠️ (product in the first 2 s). See the table. |
| 9 | Story intent | **7** | The hook question lands inside 5 s, the turn is smooth (the box has been on the nightstand all along), the CTA is subtle, and the problem/answer split is ≈73/27. What weakens it: (a) **2.6 s of silent on-camera reach** at 28.3–30.9 and **another 1.2 s of dead air** at 32.6–33.8. That's 3.8 s of silence in the answer, at the point where TOF retention matters most. (b) The B1 furrows at 16–22 s show her far more lined at night than the YESTERDAY card does, which works against the before/after. (c) TODAY reads close to erased: the frown is nearly gone and the forehead nearly smooth, where story/storyboard asked for "softer, not erased". With "No filter." next to it, that invites the "this ad… can't be real" reaction (lessons §2). |

**Hook, first 2 s:** motion from frame 0 (push-in, blinking red timer dot), timer beeps, shutter and a white flash at 1.21 s. The on-screen text "Filtering your lines out of every photo?" (6 words) is up from frame 0, and her voice enters at 0.85 s. It earns attention and names her moment. The product is visible early but only small (the tray at 1.5 s).

**FILTER \| ME split (3.33–11.29):** works. The FILTER half is visibly plastic and smoothed, the ME half keeps the frown line, forehead lines and eye crinkles, and the text stays clear of her brow.

**YESTERDAY \| TODAY card (35.83–39.71):** believable as like-for-like. Same light, framing, hair and earrings, so "Same light." is true (K6 is an edit of K7). The lines are clearly softer on TODAY. As noted under item 9, it may be too clean. Only a sliver of the held band shows at TODAY's right edge, so the card itself doesn't show the patch.

**Brand / TOF rule:** about 73% problem, then the patch as the answer. The brand name is on screen from 30.79 and on the packshot. It is not a tips page ✅.

## Checklists (lessons §10)

| Item | |
|---|---|
| B: patch clear and frosted, never opaque | ✅ (K4, B2 film, packshot) |
| B: forehead tab down | ✅ (K4, K5/B2 film, packshot) |
| B: crescents, not circles or glasses | ✅ (plumper shape is owner-accepted) |
| B: lips closed with patches on | ✅ (K4) |
| B: no smile with patches on | ✅ |
| B: two hands × five fingers; never through the face | ✅ |
| B: wrinkle depth doesn't change mid-clip (unless a planned before/after) | ❌ B1 16.4–21.9 s: grimace and brow-raise furrows far deeper than K1 |
| B: no patch slid, doubled or vanished | ✅ |
| C: price/offer matches the live store | ✅ N/A: no price or offer in this TOF video |
| C: product visible in the first 2 s | ⚠️ the tray from 1.5 s, small and unbranded (passes the letter of the rule) |
| C: CTA has its own full-screen beat | ✅ end card + packshot, "Comment PHOTO" from 37.08 s |
| C: text below the top 14% and above the bottom 35% | ✅ spot-checked: hook text ≈ y 1090–1215, FILTER/ME ≈ y 335, packshot title ≈ y 327, CTA ≈ y 1175. Spelling matches story.md. Text ≤ 8 words per element |
| C: −16 LUFS | ✅ −15.9 |
| C: commercial-use music only | ✅ no music, synthesized SFX |
| C: links / file name | not checkable in the file (posting step) |

## Fix list (all free in assembly unless stated)

| # | Timestamp | What's wrong | Fix | Cost |
|---|---|---|---|---|
| 1 | 28.3–32.08 (and the rejoin at 32.08) | Two problems in one stretch: (a) 2.6 s of silent on-camera reach; (b) the K5 still is a full-frame talking face, frozen under live speech; (c) jump cuts at 30.79 (hand empty → film at her cheek) and 32.08 (film size, angle and mouth jump). | Cut from B2 right after "every night" (≈28.3) to a **product insert**: a tight crop of the film and hand from K5, with her mouth out of frame, or a crop of the studio shot `564c68fa`, with a slow push. Under the insert, trim the reach silence to ≈0.3 s and play "So now I sleep in these." Then return to B2 on the held film (t≈7.9 onward, after her speech, so there's no lip issue) or go straight to K4. This one change removes the dead air, the frozen-mouth talk and both stutters. Runtime ≈39 s, still inside 30–50. | free |
| 2 | 32.6–33.8 | 1.2 s of dead air before "They hold my skin flat all night" | Trim ≈0.7 s of the silence under the K4 still (silent picture, so the cut is invisible) | free |
| 3 | 16.4–21.9 | B1 grimace and brow-raise furrows: the deepest lines of her in the video, deeper than YESTERDAY. In a lines ad this reads exaggerated or rigged, and it fails the checklist B wrinkle item. | Cover with a cutaway while her voice continues: e.g. a crop of the B1 nightstand tray (product B-roll, 5 pieces visible) or a reprise of the K2 "ME" half. At minimum cover the peaks at 16.4–17.6 and 19.4–21.9. Paid alternative: re-render B1 with "eyebrows lift only slightly, no frown" (32.5 credits, **doesn't fit**: 6.5 headroom). | free (redo: paid, over cap) |
| 4 | 35.83–39.71 | TODAY reads close to erased, and the held band is barely visible | Owner's call. Blend about 30–40% of YESTERDAY's brow and forehead detail back into TODAY so it reads "softer, not erased". Widen TODAY's crop slightly so the held forehead band shows (accepting the lamp edge on YESTERDAY), or add the band in code from K5. | free |
| 5 | 39.71–41.96 | The "Comment PHOTO" box overlaps the bottom two crescents on the packshot | Move the box down (stay above y 1248) or scale the packshot up a little | free |

Once fixes 1–3 are done (4 and 5 are recommended), a re-review should pass. None of them touches claims or budget.

## Logged

New defect types were added to `learning/production-log.md`: a frozen talking-face still under live speech, dead air left on camera after a cover, an after-image too clean in a before/after, and a stutter at the rejoin after a still cover. The B1 brow-raise furrows were already logged.

---

## Round 2 (v2) — Verdict: **PASS**

Re-review of `final.mp4` v2 (39.00 s), inspected locally with ffprobe/ffmpeg and whisper-cli (small.en). No paid calls, and no edits to the video or other stage files. I did not re-open the owner decisions: fix 4 (35% YESTERDAY blend) and the unbranded product chips over the dark hand.

Work files are in `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/review2-1t/`:
- `c_01–04.png`: 4 fps contact sheets, 10 × 4 per sheet, 10 s each.
- `cuts1–3.png`: both sides of every cut.
- `full/t_*.png`: full-res boundary frames.
- `chips.png`, `chipzoom.png`, `handstrip*.png`: the product chips.
- `card.png`: the end-card faces.
- `ins_tl.png`: the product insert's corner.
- `syr.png`: the syringe chip on the reprise.
- `k4face.png`: the press-on still.
- `fh.png`: forehead depth across every talking segment.
- `wh.json`: the transcript.

### Spec
| Check | Result |
|---|---|
| Duration | 39.00 s (TOF 30–50 ✅) |
| Video | 1080×1920 (9:16 ✅), H.264, 24 fps |
| Audio | AAC 48 kHz stereo ✅ |
| Loudness (ebur128) | **−15.9 LUFS integrated**, true peak −1.9 dBFS, LRA 4.6 LU ✅ |
| Music | none; synthesized SFX ✅ |

### Transcript vs story.md
Whisper small.en returns **all 88 words, in order**, and this time it hears "look **worst** right when you wake up". Nothing is cut, garbled or added. B2's audio jumps (3.33→6.0 and 8.21→8.92) sit in silence on both sides at about −60 dBFS, so there's no click and no clipped word.

### Round-1 fixes
| # | Fix | Landed? |
|---|---|---|
| 1 | Frozen talking face, silent reach, jump joins | ✅ The K5 still is gone. 27.29 B2 (end of "every night") → 28.42 product insert (film + hand, mouth out of frame) → 30.63 K4. No talking video of her comes back after the insert. Neither join jumps, because each cut goes to a different shot, not a re-entry into the same one. |
| 2 | Dead air before "They hold…" | ✅ The remaining pause is 0.55 s (30.35–30.9), under non-face shots. |
| 3 | B1 grimace and brow furrows | ✅ Covered from 15.67 to 21.58. Before the cover (≤15.63) and after it (≥21.62), the frames show K1-depth lines. Forehead crops at 2.5, 11.6, 12.2, 14.8, 22.5, 24.0 and 27.8 s all show the same faint lines. |
| 4 | TODAY too clean (owner-approved blend) | ✅ The frown and forehead lines are still traceable on TODAY, just shallower ("softer, not erased"). Pores are kept, there's no ghosting or double edge, and the eye lines match YESTERDAY exactly. Believable. |
| 5 | Comment PHOTO box over the crescents | ✅ On the packshot the box now sits just below the bottom crescents and doesn't overlap them. |

### New elements
- **Product chips (12.5–15.67):** all unbranded. There's no text on any product, and the syringe's "1 ml" print is blurred out. Each chip pops in on its word: Tretinoin 13.46, Vitamin C 14.38, Peptides 15.13. The pop-in is scale plus fade and reads as intentional.
  - **Hand:** frame by frame from 13.25 to 13.8, **no dark hand is visible** before the first chip lands. The flagged ~0.1 s doesn't show at all, because the hand is still low and off the lit area. After that, the chip covers the hand area until the cut.
  - **Polish:** at full res, each product cut-out shows a **faint rectangular seam** where its photo box meets the card: a slightly grey edge or a clipped drop shadow on the right and bottom (clearest on the syringe and the jar). At phone size it's faint, but it reads a little "template". The tretinoin tube is small and pale on white.
  - The chips also cover part of the Face Set tray on the nightstand for about 3 s. That's minor, since the tray isn't the subject there.
- **FILTER | ME reprise (15.67–21.58):** this is the strongest of the new choices. The camera pushes into ME on "Botox of lesser strength", then pans across to the plastic FILTER half on "scared it'll look unnatural", which is a visual payoff for the line.
  - **Cost:** K2 is now on screen for ≈13.8 of 39 s (35%), and the reprise has no FILTER/ME labels. Her laughing photo face also plays under a worried line.
  - It doesn't break the story, but it's the main thing holding item 9 at 8.
- **Syringe chip (16.13–18.33):** it sits over the redhead friend's eyes and nose for 2.2 s, so it reads a bit like a censor block. It's clean, and it doesn't cover her own face or the split line. It's acceptable as is, and better moved (see polish list).
- **Product insert (28.42–30.63):** the film is clear and frosted, the band sits on top with 4 crescents, and the brand title is on screen.
  - It's visibly softer than the stills because it's a ≈2.3× upscale. The headboard texture is mushy, but the product edges read.
  - A **sliver of her cheek, ear and huggie shows at the top-left edge** (about the left 9% of the frame) for 2.2 s. Her mouth is never in frame, so there's no lip-sync problem, and it reads like a hand-held over-the-shoulder insert.
- **TODAY band sliver:** a transparent curved shape is cut off at TODAY's right edge (the held band). On its own it's ambiguous. It's minor, because the patch is shown on K4 and the packshot.

### Scores
| # | Item | Score | Reason |
|---|---|---|---|
| 1 | Logic | **9** | Hook question → FILTER \| ME problem → what she's tried (now illustrated) → self-check → reveal over sleep → product as the answer → press-on → YESTERDAY \| TODAY → Comment PHOTO. Clear to a stranger, and both loops close. |
| 2 | Script fidelity | **9** | 88/88 words, in order; "worst" is now heard correctly. |
| 3 | Lip sync | **9** | No frozen face under speech anywhere. A, B1 and B2 track the audio wherever she's on camera (spot-checked 1.5–3.3, 12.5–15.6, 21.6–25.0, 27.3–28.4). Every other second is a still or an insert with no mouth. |
| 4 | Anatomy | **9** | Two hands and five fingers wherever hands show (phone hand, K4 pressing hand, insert hand, friends' hands). No melting. Teeth and eyes are fine. |
| 5 | Continuity | **8** | Same woman, hair, huggies, T-shirt and room throughout, and every join now cuts to a different shot, so nothing stutters. Small deductions: K2 is reused for 35% of the runtime, a cheek/ear sliver shows at the insert's edge, and the cut-off band sliver sits on TODAY. |
| 6 | Product | **8** | Tray on the nightstand from 1.5 s; insert shows the film (5 pieces, tab down, brand title); K4 on-face (tab down, crescents, lips uncovered); packshot clear with the CTA off the pieces. The insert is soft from the upscale. No packaging (accepted fallback). |
| 7 | Claims | **9 (clean)** | Spoken: the approved opener and the approved mechanism only. The chips name the persona's own research (tretinoin, vitamin C, peptides, Botox) with **no claim about them** and no brands. The before/after is allowed (AI included) and the blend reads "softer, not erased". None of the following appear: credentials, statistics, reviews, "permanent/forever/for good", "11s", "8 hours", "rinse and dry". No price (TOF). As in round 1: post with the platform's AI-content label, because "No filter." sits on an AI before/after. |
| 8 | Budget | **10** | `actual_total` **130.0 ≤ cap 135** (one owner-approved 1.5-credit props still; assembly 0). |
| 8b | Owner checklists B + C | **8** | All ✅; one marginal ⚠️ (product in the first 2 s), same as round 1. See the table. |
| 9 | Story intent | **8** | The hook question lands inside 4 s and the frame-one motion is intact. The turn to the patches is smooth, and the answer beat now runs with no dead air. The CTA is subtle and gets its own beat. Problem/answer split ≈ 73/27. Held back by the long K2 reuse with the laughing face under "scared it'll look unnatural", and by B1's natural pauses (1.35 s at 17.8–19.15 and 1.3 s at 20.9–22.2), both of which carried over from v1. |

**First 2 s:** push-in, blinking timer dot, beeps and the flash/shutter at 1.21. The hook text is fully on from frame 0, and her voice enters at 0.85. Unchanged and strong.

**CTA beat:** "Comment PHOTO" appears on "photo" (34.13) over the like-for-like card, then holds full-screen over the packshot to 39.0 ✅.

### Checklists (lessons §10)
| Item | |
|---|---|
| B: patch clear and frosted | ✅ insert, K4, packshot |
| B: forehead tab down | ✅ |
| B: crescents, not circles or glasses | ✅ (plumper shape owner-accepted) |
| B: lips closed with patches on / no smile | ✅ K4 |
| B: two hands × five fingers; never through the face | ✅ |
| B: wrinkle depth doesn't change mid-clip | ✅ B1 furrows covered; every talking segment shows K1-depth lines |
| B: no patch slid, doubled or vanished | ✅ |
| C: price/offer | ✅ N/A (no price in TOF) |
| C: product in the first 2 s | ⚠️ the tray from 1.5 s, small (passes the letter of the rule) |
| C: CTA full-screen beat | ✅ 34.13–39.0 |
| C: text in the safe zone, spelling, ≤8 words | ✅ All boxes sit between y ≈ 330 and ≈ 1240. Chip labels at y ≈ 863 sit on the cards. Spelling matches story.md, and every element is ≤ 8 words. |
| C: −16 LUFS | ✅ −15.9 |
| C: commercial-use music | ✅ none |
| C: links / file name | not checkable in the file (posting step) |

### Optional polish (not required to pass; all free in assembly)
| # | Time | What | Fix |
|---|---|---|---|
| a | 13.46–15.67, 16.13–18.33 | Faint rectangular seams and clipped shadows around the product cut-outs on the chips | Feather or alpha-mask each cut-out (or key the white to transparent) so no photo-box edge shows; enlarge the tretinoin tube slightly |
| b | 16.13–18.33 | Syringe chip sits over a friend's face (looks like a censor block) | Move it to the dark lower-left area (black top, under the FILTER side) or onto the bottom right over her shoulder, above the y 1248 line |
| c | 17.8–19.15 | 1.35 s silence inside the reprise | Trim ≈0.7 s of B1 audio under the still (invisible cut), which also shortens the K2 reuse |
| d | 28.42–30.63 | Cheek/ear sliver at the insert's top-left | Shift the crop ≈100 px right, or scale up ≈5% |
| e | 32.88–36.75 | Cut-off band sliver at TODAY's right edge | Crop it out, or widen enough to show the held band clearly |

Logged: new defect types (cut-out seams on code-made product chips; a chip placed over a bystander's face; a long still reprise) were added to `learning/production-log.md`.

---

## Round 3 (v3 fast-paced) — Verdict: **FAIL**

Independent review of `final-v3.mp4`. I inspected it locally with ffprobe/ffmpeg at /opt/homebrew/bin and whisper-cli (small.en, plus multilingual small as a second opinion). I used Python/numpy for the envelope, pitch and frame-difference measurements. No paid calls, and I made no edits to the video or to other stage files. v2 (`final.mp4`) was used as the comparison.

Work files are in `/private/tmp/claude-501/-Users-josediaz--claude-spares-spare-SRaU1E/2f87790f-784b-45bc-9668-95f59d8eab95/scratchpad/review3-1t/`:
- `c_0–4.png`: 4 fps contact sheets, labelled.
- `full/t_*.png` and `fullA–C.png`: full-res frames.
- `talk6.png`: talking frames.
- `mouth_a/b/c.png`: 30 fps mouth strips on "group photo", "vitamin" and "wake up".
- `wh_en.json` and `wh_ml.json`: transcripts.
- `an.py`, `an2.py` and `f0.py`: gap, SFX and pitch measurements.
- `fr30/`: frame cadence.

**Only one item is below 8: product, at 7.** The CTA bubble covers the packshot again. That's a regression of round-1 fix 5. Claims are clean. Every fix is **free in assembly**, about 10 minutes of work. A re-review should pass after fix 1 alone; fixes 2 and 3 are strongly recommended.

### Spec
| Check | Result |
|---|---|
| Duration | **27.00 s**. Under the TOF 30–50 s window; the owner accepted this. |
| Video | 1080×1920 (9:16 ✅), H.264, **30 fps**, 810 frames |
| Audio | AAC 48 kHz stereo ✅ |
| Loudness (ebur128) | **−16.0 LUFS integrated**, true peak −2.0 dBFS, LRA 3.4 LU ✅ |
| Music | None; SFX synthesized ✅ |

### Transcript vs story.md
- small.en returns **all 88 words, in order**. The only difference is that it hears "worse" for "worst".
- Multilingual small hears "**worst**" correctly, and also writes "tretinone" for tretinoin and "Comment, photo".
- I checked short windows of the mix against the voice stem, at 7.1–8.8, 9.4–10.8, 13.4–15.1 and 15.0–17.5 s. They transcribe identically, so no SFX costs a word.

### Measurements against `editing:`
| Spec | Measured | |
|---|---|---|
| Max shot 2.5 s | Scene detection finds cuts at exactly the 23 listed boundaries. Longest shot 2.24 s (end card), shortest 0.39 s, average 1.17 s. | ✅ |
| First 3 s, a change every ≤1.5 s | Changes at 0.33 (flash), 0.88, 1.61 and 2.58 | ✅ |
| Max word gap 0.3 s | Largest gap on the voice stem is **0.18 s** at 17.34 (the planned beat). Next largest are 0.09, 0.08 and 0.08 s. Speech runs 0.41–25.36 s, about 3.5 w/s. | ✅ |
| Speed 1.08×, pitch kept | Median F0 **195 Hz in v3 vs 193 Hz in v2** (+1%, within estimator error). A plain 1.08× resample would read ≈208 Hz, so pitch is preserved. I found no measurable artefact. I could not listen: **the owner should audition it.** With every sentence separated by only 60–90 ms, the delivery may sound breathless. | ✅ (by measurement) |
| 30 fps from 24 fps | Talking shots repeat a frame irregularly, about every 4–7 frames (frame diff 0.0). That's mild pulldown judder, normal on phones, and invisible on stills, which are rendered at 30 fps. | ✅ minor |
| Pop-ups every 3–5 s | Longest gap ≈3.7 s (13.7 → 17.36). Big interrupts at 0.33, 4.28, 13.31, 17.36 and 23.15. | ✅ |
| SFX −22 to −18 LUFS, never on a stressed word | Two problems, below. | ⚠️ |

**SFX.** I measured 23 cue onsets on the SFX stem against the voice stem.
- Most cues sit about 0.1 s before their word, as the log rule says.
- **The riser at 16.72–17.34 runs under "when you wake up?"** and peaks above her voice: about −13 to −17 dB against −21 to −25 dB in 10 ms RMS at 17.1–17.3. This is the open-loop self-check, the most shareable line. Whisper still gets it, but by ear it will sound like the riser is drowning the last two words. This also breaks the production log's own rule, "no risers under speech".
- **Pops land on "filter" (7.48) and "I'm" (13.69)** at roughly equal level to the voice. Both words stay intelligible, so these are minor.

### Lip sync (8c)
On-camera talking is now only about 9.3 s, in 9 short shots. Every word with weak sync in the research list is covered by B-roll:
- "look smooth", "by my", "peptides", "even Botox", "lesser strength", "my skin", "night" and "Comment photo" are all on cutaways.
- I checked the bilabials still on camera at 30 fps:
  - **"group photo"**: the lips close at 1.05–1.15 s.
  - **"vitamin"**: the lips come near-closed at 10.25–10.32.
  - **"wake up"**: the lips close fully at 17.22–17.35, just before the cut.
- No frozen live face sits under speech. The eye macro (5.93–7.18) and the FILTER card (13.31–15.01) are her laughing *photo* face, and they read as the photo.
- No talking with patches on: K4 is a silent picture.

### Scores
| # | Item | Score | Reason |
|---|---|---|---|
| 1 | Logic | **9** | Same arc as v2: hook → FILTER \| ME → what she's tried → self-check → reveal → product → press-on → YESTERDAY \| TODAY → Comment PHOTO. It's tighter, and both loops close. Captions now make it followable with the sound off. |
| 2 | Script fidelity | **9** | 88/88 in order. The worst/worse elision is unchanged from earlier rounds, and the second model hears "worst". |
| 3 | Lip sync | **9** | See above. On-camera time is down from ≈60% to ≈35%, all weak-sync words are covered, and the m/b/p closures I checked are present. |
| 4 | Anatomy | **9** | Hands and fingers are fine in every shot I checked: phone hand, insert hand, K4 pressing hand, friends. No melting. Teeth and eyes are fine. |
| 5 | Continuity | **8** | Same woman, room and wardrobe throughout. Jump cuts alternate 100/112–115% framing, so they read as deliberate. Deductions: K2 is still ≈27% of runtime. The **2× eye macro shows a smeared, waxy patch on the FILTER half** around her left brow and eye (6.0–7.1). The insert is a soft upscale. There's irregular 30 fps judder. |
| 6 | Product | **7** | The **"Comment PHOTO" bubble covers the lower part of the two bottom crescents on the packshot** for the whole CTA hold (25.38–26.97), both during the slam-out and once settled. That's the round-1 fix 5 defect coming back, on the only clean full-set image. Everything else is good: the tray in frame from 0.88; the insert with the film, tab down and the Face Set pill; K4 on the face with lips closed; the packshot with all 5 pieces and the brand. |
| 7 | Claims | **9 (clean)** | Spoken lines are unchanged: the approved opener ("pressed in every night") and the approved mechanism ("hold my skin flat all night"). New visuals make no claim: the green check on K4 sits on an approved line, and the chips and cards are unbranded with no product claims. The before/after is allowed. None of the off-limits items appear (credentials, stats, reviews, permanent/forever, "11s", "8 hours", "rinse and dry"). Post with the AI-content label ("No filter." sits on an AI before/after). |
| 8 | Budget | **10** | `actual_total` 130.0 ≤ cap 135. v3 cost 0 credits. |
| 8b | Owner checklists B + C | **8** | All ✅, with the same marginal ⚠️ on "product in the first 2 s" (the small tray from 0.88). Text is in the safe zone: top text at y ≥ ≈290, captions at y ≈1085–1215. Spelling matches story.md. |
| 8c | Pace and lip sync | **9** | Every number is in spec: max shot 2.24, max gap 0.18, word-by-word captions with the current word in orange, a change every ≤1.5 s in the first 3 s, and m/b/p closures where she's on camera. Minus 1 for the hook card: it lights "photo → Filtering → lines" out of reading order, and the spoken "Can't take a group… without" has no caption. |
| 9 | Story intent | **8** | The hook question finishes by 2.6 s, with motion, flash, SFX and text from frame 0. The turn is smooth, the problem/answer split is ≈73/27, and the CTA is subtle with a full-screen beat. Held back by three things. (a) The riser over "wake up?". (b) **"Nobody told me why."** was written for a silent beat that no longer exists, so it now sits over the spoken caption "A LOT OF THEM", and two sentences compete at 17.4–18.3. (c) The dropped persona lines. |

### Hook, brand, CTA, YESTERDAY | TODAY, clutter
- **First 2 s:** push-in from frame 0, a blinking dot, beeps, a white flash and shutter at 0.33, and the hook card on from frame 0. Her voice enters at 0.41, and there's a hard cut to her face at 0.88. This is stronger than v2: we're on her face 0.6 s sooner.
- **Brand (TOF):** about 73% problem. The product name is on screen from 19.71 (pill), spoken at 19.84, and on the packshot. It is not a tips page ✅.
- **CTA:** spoken, captioned with PHOTO highlighted, then a comment-bubble sticker on the packshot. Clear and subtle. It only fails on the overlap.
- **YESTERDAY \| TODAY:** like-for-like and believable. TODAY's lines are softer but still traceable, and the held-band sliver is gone. The card is busy, though: "Same light. No filter.", the YESTERDAY/TODAY labels and the caption are stacked within ≈350 px at mid-chest. It's readable, but it's the most cluttered frame in the video.
- **Pop-ups:** these look mostly clean and intentional. The scale-pop is consistent, the chips are keyed with no seams, and the syringe card no longer sits on a face. The cheap-looking items:
  - The tretinoin tube and the peptides jar are white-on-white and low contrast at phone size.
  - A faint blurred square shows on the syringe barrel.
  - The emoji and the moon are generic, but they fit TikTok grammar.
  - Nothing obscures a face, except that the split's "FOREHEAD LINES" caption sits over her laughing mouth in the photo, which is fine.

### Dropped on-screen lines
"It ages me more than I'd like." was the persona's **key concern** (story fix 6). "And it keeps getting worse." was her urgency line.
- Without them, the video still reads as her: filter → fraud, frown, forehead and eye crinkles, tretinoin, peptides, "Botox of lesser strength".
- But the **looking-older-than-my-age** motive is now only implied, and that motive is what separates this persona from a generic "lines" viewer.
- It's a mild loss in persona fit, not a failure. The cheapest restore is one short pill, "It ages me." or "Makes me look older.", popped on the eye macro (5.93–7.18) at the top of the frame (y ≈ 300), where no other text sits.

### Fix list (all free in assembly)
| # | Time | Problem | Fix | Cost |
|---|---|---|---|---|
| 1 (**required**) | 25.38–26.97 | "Comment PHOTO" bubble covers the bottom two crescents on the packshot (regression of round-1 fix 5) | Move the bubble down to y ≈1150–1240 (still above 1248), or scale and raise the packshot ~8%. Check the slam-out frames as well as the settled ones. | free |
| 2 (recommended) | 16.72–17.34 | Riser sits under "when you wake up?" and peaks above the voice | Start it at "up" offset (≈17.30), or duck it 12 dB under speech, or drop it and keep only the scratch at 17.36 | free |
| 3 (recommended) | 17.36–18.30 | "Nobody told me why." overlaps the spoken caption "A LOT OF THEM" (the silent beat is gone) | Drop the card, or show it only during the 0.2 s beat plus the slam, cleared by 17.56 | free |
| 4 (optional) | 7.48, 13.69 | Pops on "filter" and "I'm" at voice level | Move each 0.12 s earlier, per the log rule | free |
| 5 (optional) | 5.93–7.18 | Eye macro: smeared, waxy patch on the FILTER half (2× upscale of the split) | Push less (≈1.5×), or shift the crop so the ME eye fills the frame and the FILTER half is a thin edge | free |
| 6 (optional) | 5.93–7.18 | Key-concern line lost | Pill "It ages me." at the top of the eye macro | free |
| 7 (optional) | 0.88–2.58 | Hook card highlights out of reading order | Highlight only the word being spoken that also appears on the card, in sync, or keep the card static | free |

### v3 vs v2 for TOF engagement
**v3 is the better TOF ad**, provided fixes 1–3 are made and the owner approves the sound by ear.
- **Pace and attention.** v3 delivers the same 88 words in 27 s instead of 39, with 23 shots averaging 1.17 s instead of 13 shots averaging 3 s. It has no dead air, and a visual or sound event every 1–2 s. Average watch % and completion should rise, and those drive TOF delivery.
- **Sound-off viewing.** Word-by-word captions make it work with the sound off; v2 had no speech captions at all.
- **Lip sync.** It hides Kling's weak articulation: on-camera talking falls from about 60% to about 35% of runtime, with every weak m/b/p word on B-roll. That answers the owner's lip-sync complaint for free.
- **Hook.** It reaches her face sooner.
- **Costs:**
  - It's 3 s under the 30 s TOF floor, which the owner accepted.
  - The persona's "it ages me" line is gone.
  - Some frames are busier: the end card, and the K3 text clash.
  - The synthetic SFX and the 1.08× voice haven't been heard by a human.
  - It's an untested style for this account, so it should be read as a pacing test against v2 (same words, same visuals) if the owner wants a clean A/B.

### Logged
New defect types are in `learning/production-log.md`:
- a CTA sticker re-covering the product after a re-layout;
- a riser under a key spoken line;
- a silent-beat text card left on after the beat was cut;
- smear on a code-smoothed half when it's upscaled;
- the hook card lighting words out of reading order.

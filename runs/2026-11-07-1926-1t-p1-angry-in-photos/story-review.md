# Story review — run 2026-11-07-1926 — slot 1-T (P1, TOF-U) — reviewing story.md **v1**

Stage 4 (story-reviewer). Read in full: `.claude/agents/story-reviewer.md`, `pipeline/config.yaml`,
`docs/creative-strategy.md`, `docs/lessons-learned.md`, `learning/playbook.md` (all UNTESTED, nothing
RETIRED, so no retired element is used), `brief.md`, `format.md`, `story.md`.
Bars: every item ≥ 8 (`review.min_story_score`); TOF hooks 1–3 and Shareability ≥ 9
(`review.min_hook_score_tof`); length 30–50s at 2.3 words/s.

## Verdict: **REVISE** (revision 1 of max 2)

The concept is right for the slot and the claims are clean, but the story contradicts itself on
its own timeline, two of the three hook scores and Shareability are under 9, the product share is
~31% vs ~20%, and four shots ask Kling 3.0 for things it does badly.

## Word count and timing (checked by hand)

| Beat | Line | Words | Needed at 2.3 w/s | Window in v1 |
|---|---|---|---|---|
| Hook | "Ever look angry in a photo when you were actually happy?" | 11 | 4.8s | 5s ✓ |
| Problem | "Best friend's birthday … Asking for a manager." | 13 | 5.7s | 6s ✓ |
| Dig + loop | "She asked if I was mad at her … Then I found out why." | **26** (v1 says 25) | 11.3s | 11s ✗ |
| Reveal | "It's not my mood … for hours." | 21 | 9.1s | 9s ✗ (slightly, with a pillow demo on top) |
| Turn | "So now these go on before bed …" | 14 | 6.1s | 6s ≈ |
| Result + CTA | "Next morning? … what I use." | 18 | 7.8s | 7s ✗ |
| **Total** | | **103** (v1 says 102) | **44.8s** + ~4s silent ≈ **48.8s** | 48s stated |

Inside the 30–50s window, but with only ~1s spare, and three beats are over their windows. The
spoken hook doesn't finish until ~0:07.
**Problem vs product:** 0:00–0:33 problem (71 of 103 words); 0:33–0:49 turn + result + CTA ≈ 16s
≈ **31–33%** of runtime. The strategy says ~20% (≈10s of a 49s video). Too heavy.

## Scores

| # | Item | Score | Reason |
|---|---|---|---|
| 1 | Hook is a question, lands within 5s | **8** | It's a question and the on-screen text lands at 0:00, but the spoken question ends at ~0:07, outside the 5s hook |
| 2 | Hook fits the persona | **7** | Nothing in it is P1's own: no 30s, no "suddenly/is that me?", no group-photo hiding. A 22-year-old, P4 and anyone after posing tips (Bonnie's 13s tips video) care just as much. Too generic for a 9 |
| 3 | Hook makes sense cold | **9** | Instantly understood, and the video pays it off with a cause |
| 4 | Body digs in | **8** | Good specifics ("asking for a manager", "are you mad at me?", offers to take the photo), weakened by the timeline muddle in #6 |
| 5 | Smooth turn | **8** | "So now these go on before bed" follows straight from the pillow cause; no banned phrase; the box has been in frame since 0:02 |
| 6 | Logic | **5** | (a) "So **now** these go on before bed" means she already uses the patches, so why do *last night's* photo and the before/after show the problem? (b) Frame one is her mid-laugh with her head back, and the photo is captioned "I was LAUGHING here": a laughing photo doesn't read as angry, which undercuts the hook. (c) "Pressed in while I sleep" doesn't explain looking angry at an evening dinner without a bridge (they've stopped fading by daytime). Without it, a cold viewer thinks "that was 12 hours ago". (d) "I'm the one who offers to take the photo" clashes with her being in tonight's timer photo |
| 7 | Subtle CTA | **9** | Exact owner phrasing, keyword PHOTO, on its own card, also in the caption |
| 8 | Claims | **9** | All approved: opener, belief 1 ("hold my skin flat all night"), "lines gone" = approved "removes wrinkles" in first person, never permanent. No credentials, stats or reviews (believability of "lines gone" is scored at 9c) |
| 9 | Stage job / stands alone / length / strategy fit | **7** | Stands alone and the loop closes at 0:24 ✓; brand visible (box, on-screen name, caption) ✓; but product share ~31% vs ~20%, and length runs ~49s against the 50s ceiling with beats over their windows |
| 9b | One idea | **9** | One belief (opener → 1), no objection, one CTA |
| 9c | Would she believe it? | **7** | "Lines gone" after one night, on top of a side-by-side, is exactly the "this ad… can't be real" trigger. A party flash photo vs a soft-daylight selfie isn't a like-for-like comparison and will look staged |
| 10 | Lessons learned | **7** | An off-screen "three, two…" is a second voice when the friends never speak (§8 several-people risk); the photo lives on her phone screen (screen content = precise AI text and image, §8 garbled text); multi-action shots break "one action per shot" (§3); product first appears at 0:02 against "first 1–2s" (§3, §10C) |
| 11 | Producible (Kling 3.0) | **5** | Hard as written: a phone screen showing a specific photo, plus a zoom and a tap on it; pressing a pillow into her face *while lip-syncing*, then a crease that appears on cue (a state change); pick up box → slide out sheet → hold up clear piece in one shot (chained hand actions with clear silicone); a five-person flash group shot with her identity locked |

## TOF hook scores and Shareability (bar: 9)

| | Score | Pass? |
|---|---|---|
| Hook 1: question, within 5s | 8 | ✗ |
| Hook 2: persona fit | 7 | ✗ |
| Hook 3: cold sense | 9 | ✓ |
| **Shareability** | **8** | ✗. "Are you mad at me?" and the pillow fact are relatable and send-able, but nothing invites a comment on purpose, and the joke photo doesn't land if she's visibly laughing in it |

## Claims check

| Line | Claim | Source | OK? |
|---|---|---|---|
| "A lot of these lines get pressed in while I sleep, folded into the pillow" | Opener | Lessons §2 optional opener; brief claim 3 | ✓ |
| "These go on before bed and hold my skin flat all night" | Usage + belief 1 | Lessons §1 overnight; §2 belief 1 | ✓ (no "8 hours", no "rinse and dry") |
| "Next morning? Lines gone." | Result, first person | Lessons §2 "removes wrinkles … wakes up with the wrinkles gone" | ✓ approved; flagged at 9c for believability, not compliance |
| "Still me, just not mad" | Identity | Lessons §2 "look rested, still look like herself" | ✓ |
| Caption | Opener + brand | ✓ |
| Credentials / statistics / reviews / permanent / "11s" | none | | ✓ |

Claims are clean. No automatic fail.

## Fixes (do all; then resubmit as v2)

1. **Hook, spoken and on-screen (0:00–0:07). Problem:** generic (any age, any persona) and the spoken question ends at ~0:07. **Rewrite:** POV cut to 1.5s; at the hard cut she says **"Since when do I look mad in every photo?"** (9 words, 3.9s → ends ~0:05.4). On-screen at 0:00: **"35 and suddenly mad in every photo?"** (7 words). That gives her age, her "is that me?" suddenness and photos, so younger viewers and posing-tip seekers scroll past. Keep "Ever look angry…" as Alt B for a labelled hook test.

2. **Frame one (0:00–0:01.5). Problem:** the off-screen "three, two…" is a second speaker; she's mid-laugh in front, which contradicts both the angry photo and "I hide/offer to take the photo". **Rewrite:** same candle-lit timer POV with motion (friends squeeze in, timer light blinks, flash), but **she's at the back edge, half behind a friend's shoulder**, and the flash catches her face relaxed between laughs. Sound: laughter, **timer beeps** and the shutter only. No voices.

3. **Problem beat (0:07–0:13). Problem:** the photo is on her phone screen with a zoom and a tap (hard to produce); "I was LAUGHING here" over a laughing face kills the joke. **Rewrite:** show the photo as a **full-screen code insert** (a Nano Banana still: her relaxed face, closed mouth, forehead and frown lines reading as annoyed), with a **code zoom** to her forehead; her talking-head audio J-cuts over it. Line: **"Best friend's birthday. I was having the best night. My forehead? Asking for a manager."** (15 words). On-screen: "I was having the BEST night".

4. **Dig + loop (0:13–0:24). Problem:** 26 words in an 11s window; "offers to take the photo" contradicts the timer shot; "she asked" isn't tied to tonight. **Rewrite:** **"She saw it and asked if I was mad at her. I wasn't. I already hide at the back of photos. Then I found out why."** (25 words, 10.9s). On-screen: **"'Are you mad at me?'"**, then a second card: **"Anyone else get asked this?"** (on screen only, no extra words; a deliberate comment prompt for Shareability).

5. **Reveal (0:24–0:35). Problem:** no bridge from "while I sleep" to looking angry at an evening dinner; pillow press + crease appearing + lip-sync in one clip isn't producible. **Rewrite:** **"It's not my mood. A lot of these lines get pressed in while I sleep, folded into my pillow every night, and they stopped fading."** (25 words, 10.9s). Visual: talking head for the first sentence, then a **silent 3s B-roll insert** (her voice J-cut over it): close-up of her asleep on her side, forehead pressed into the light-grey pillow, skin folding. One action, no talking, lips closed, start and end frames locked. On-screen: "Pressed in. Every. Night."

6. **Turn (0:35–0:39). Problem:** "So **now**" makes it a habit, which contradicts the problem photo from last night; box → sheet → piece is three hand actions in one shot. **Rewrite:** **"So tonight, these hold my skin flat while I sleep."** (10 words, 4.3s). Visual, one action: the backing sheet is **already in her hand**, she holds the clear forehead piece up to the lens; the box sits on the nightstand brand side out (real product reference; brand name in code). On-screen: The Wrinkle Smooth Face Set · The Daily Glow Co. (Optional, if the storyboarder can fit ≤1.5s silent: an organic press-on while she holds the phone, lips closed, never lying down.)

7. **Morning + result + CTA (0:39–0:46). Problem:** product segment too long (~16s, 31%); "Lines gone" plus a party-flash vs daylight side-by-side reads "can't be real". **Rewrite:** drop the separate 2s silent morning beat. Open the morning shot with the piece already off and held in her fingers beside her bare face (patch off, so she may talk): **"Morning. Forehead smooth, still me, just not mad. Comment PHOTO and I'll send you what I use."** (17 words, 7.4s). Before/after in code = **like-for-like**: last night's bedroom talking-head frame vs this morning's frame, same framing, lines visibly **softer, not erased**. Then the full-screen CTA card.

8. **Section 6 of story.md. Problem:** word count stated as 102 (it's 103) and the product share stated as 31% with no fix. **Rewrite:** recount after the fixes. With 1–7 the spoken total is ≈ **101 words ≈ 43.9s + 1.5s POV + ~3s B-roll overlapping the audio ≈ 46s**. The patch-as-answer (turn + result) ≈ 8s ≈ **17%**, plus the ~4s keyword CTA. Re-time every beat so no window is shorter than words ÷ 2.3.

9. **Product in the first 2s (lessons §3, §10C). Problem:** the box first appears at 0:02. **Rewrite:** the hard cut to the bedroom lands at **0:01.5**, with the box on the nightstand in that first bedroom frame.

When v2 comes back I'll re-score every item. To approve, hooks 1–3 and Shareability need ≥ 9, everything else ≥ 8, and logic (#6) and producibility (#11) need the biggest lift.

---

## Round 2 (v2)

Re-read `story.md` v2 in full, including the revision note, against the same sources and bars as round 1.

### Verdict: **APPROVED**

Every item scores 8 or higher, the three TOF hook scores and Shareability reach 9, and the claims are clean. The notes for the storyboarder at the end don't block approval.

### Word count and timing (checked by hand)

| Beat | Line | Words | Needed at 2.3 w/s | Window | OK |
|---|---|---|---|---|---|
| Hook (spoken) | "Since when do I look mad in every photo?" | 9 | 3.9s | 0:01.5–0:05.5 (4.0s) | ✓ |
| Problem | "Best friend's birthday … Asking for a manager." | 15 | 6.5s | 0:05.5–0:12 (6.5s) | ✓ |
| Dig + loop | "She saw it … Then I found out why." | 25 | 10.9s | 0:12–0:23 (11s) | ✓ |
| Reveal | "It's not my mood … and they stopped fading." | 25 | 10.9s | 0:23–0:34 (11s) | ✓ |
| Turn | "So tonight, these hold my skin flat while I sleep." | 10 | 4.3s | 0:34–0:38.5 (4.5s) | ✓ |
| Result + CTA | "Morning. Forehead smooth … what I use." | 17 | 7.4s | 0:40–0:47.5 (7.5s) | ✓ |
| **Total** | | **101** (matches v2) | **43.9s** + 1.5s POV + 1.5s press-on ≈ **47.5s** | | ✓ inside 30–50s |

**Problem vs product:** problem runs 0:00–0:34 (74 of 101 words, ~72%). The patch as the answer (turn, press-on, morning result) runs about 0:34–0:43.5, roughly 9.5s ≈ **20%**. The keyword CTA takes ~4s after that. Counted with the CTA, the product share is ~28%. That's fine, because the CTA is its own required beat. Within the ~80/20 rule ✓. The box is in frame from 0:01.5, inside the first 2s ✓.

### Scores

| # | Item | Score | Reason |
|---|---|---|---|
| 1 | Hook is a question, lands within 5s | **9** | A question; the on-screen hook lands at 0:00 and the spoken one is done by ~0:05.4; frame one has motion (squeeze-in, timer light, flash) |
| 2 | Hook fits the persona | **9** | "Mid-30s" plus "suddenly" gives her age and her "is that me?" change, and "every photo" is her photo-dodging desire. A 22-year-old and someone after posing tips now scroll past |
| 3 | Hook makes sense cold | **9** | Clear without context, and the video pays it off with a real cause |
| 4 | Body digs in | **9** | Specific and relatable: the birthday, "asking for a manager", "are you mad at me?", hiding at the back (shown in frame one, so it agrees with itself) |
| 5 | Smooth turn | **9** | "So tonight, these hold my skin flat while I sleep" is the direct answer to "pressed in while I sleep"; no banned transition; the box has been in frame since 0:01.5 |
| 6 | Logic | **8** | All four round-1 holes are closed: "So tonight" makes it her first night; the photo shows a relaxed face, not a laugh; "they stopped fading" links night to evening; she's at the back, not taking the photo. One soft spot, not a hole: when she "found out why" and bought the box is left vague. Plus a doc slip, below (note 1) |
| 7 | Subtle CTA | **9** | The owner's exact phrasing with PHOTO, its own full-screen card, also in the caption |
| 8 | Claims | **9** | All approved (table below); "forehead smooth" = "smoother skin by morning" in first person; nothing permanent |
| 9 | Stage job / stands alone / length / strategy fit | **9** | TOF-U: mostly the problem, ending on the patch as the answer with one line on how it works; brand on the box, on screen and in the caption; the loop opens at 0:23 and closes at 0:24–0:34; no sequel; 47.5s |
| 9b | One idea | **9** | One belief (opener → belief 1), no objection, one CTA |
| 9c | Would she believe it? | **8** | Softer wording and a same-framing night/morning comparison with lines "softer, not erased" fix the "can't be real" risk. It still depends on the overlay really being subtle in production |
| 10 | Lessons learned | **8** | No second voice; photo done in code; one action per shot; product on screen by 2s; no talking with a patch on; press-on sitting up, not lying down. The risk is the 1.5s one-handed press-on (§8 hands, "patch already on before she applies it") (note 2) |
| 11 | Producible (Kling 3.0) | **8** | The phone screen, the awake pillow press with lip-sync and the box chain are gone. The sleeping cutaway and holding up the piece are simple. The press-on is the one hard shot, but it's optional and the story works without it. The five-person POV is 1.5s from a checked still |

### TOF hook scores and Shareability (bar: 9)

| | Score | Pass? |
|---|---|---|
| Hook 1: question, within 5s | 9 | ✓ |
| Hook 2: persona fit | 9 | ✓ |
| Hook 3: cold sense | 9 | ✓ |
| **Shareability** | **9** | ✓. "Anyone else get asked this?" on screen and in the caption asks for comments on purpose; "asking for a manager" and the pillow fact are things she'd send a friend |

### Claims check

| Line | Claim | Source | OK? |
|---|---|---|---|
| "A lot of these lines get pressed in while I sleep, folded into my pillow every night" | Opener | Lessons §2 optional opener | ✓ |
| "…and they stopped fading" | Her own experience of the problem, not a product claim | Lessons §2 situation 2 ("no longer fade by midday") | ✓ |
| "So tonight, these hold my skin flat while I sleep" | Usage (overnight) + belief 1 | Lessons §1, §2 belief 1 | ✓ |
| "Morning. Forehead smooth, still me, just not mad." | First-person result + identity | Lessons §2 "smoother skin by morning", "still look like herself" | ✓ |
| Before/after overlay | Allowed | Lessons §0 (Nov 7) | ✓ |
| Caption | Opener + brand + keyword | | ✓ |
| Credentials / statistics / reviews / permanent / "11s" / "8 hours" / "rinse and dry" | none | | ✓ |

Clean.

### Notes for the storyboarder (they don't block approval, no rewrite needed)

1. **Timeline label.** The 0:05.5 visual says "last night's group photo", but the bedroom is "same night". Treat it as **tonight's** photo. "Last night's frame" is right only in the morning before/after.
2. **Optional press-on (0:38.5–0:40).** Lock a bare-face start frame (piece in her fingers just off the forehead) and an end frame (piece flat, tab DOWN, covering the middle two-thirds, nothing else on her face). Show a clean, bare, matte face: no party makeup on the forehead, because usage is clean, dry skin. Lips closed, sitting up. If it fails its one allowed retry, cut it: the story doesn't need it.
3. **Before/after.** Use the same framing and light logic for both frames. Lines should be softer, not erased. "Her wrinkles do not change during the clip" applies to every other clip.
4. **Brand text** is added in code only. The box uses the real product reference, never AI-rendered lettering.

---

## Round 2 (story v2) — Verdict: **REVISE**

Independent re-review of `story.md` v2 (revision 1 of max 2). Re-read in full: `.claude/agents/story-reviewer.md`,
`pipeline/config.yaml`, `docs/creative-strategy.md` (§2, §6, §9), `docs/lessons-learned.md`, `learning/playbook.md`
(nothing RETIRED), `brief.md`, `format.md`, `story.md` v2, round 1 above.
**Note:** a "Round 2 (v2) — APPROVED" section already sat at the end of this file when this review started. It was not
written by this review and was left untouched; this section is the independent round-2 verdict requested for the gate.
Where the two differ, the difference is the word count and the credit check below, which that section did not do.

The story itself is now strong: the hooks, the cause-reveal, the turn and the claims all pass. It fails on one
thing the gate must check before any storyboard: **as written it doesn't fit the TOF credit budget**, plus three
small text errors. All fixes are trims, not a rewrite.

### Round-1 fixes: did they land?

| # | Round-1 fix | In v2? |
|---|---|---|
| 1 | Persona-specific hook, spoken done by ~0:05.5; on-screen age callout | ✓ "Since when do I look mad in every photo?" (9 words, ends 0:05.5); on-screen "Mid-30s and suddenly mad in every photo?" (7 words) |
| 2 | Frame one: her at the back edge, relaxed, no voices | ✓ |
| 3 | Photo as full-screen code insert, new problem line | ✓ (but the visual is labelled "last night's group photo" while the bedroom is "same night": see fix C) |
| 4 | Dig line at 25 words + "Anyone else get asked this?" card | Line ✓, card ✓, but the line is **26 words**, not 25 (11.3s in an 11s window). The round-1 rewrite miscounted too |
| 5 | Reveal with "they stopped fading" + silent sleeping cutaway | ✓ (25 words) |
| 6 | "So tonight", one action, sheet already in hand | ✓ (10 words) |
| 7 | Morning: piece already off, softer-not-erased like-for-like before/after | ✓ (17 words) |
| 8 | Recount section 6 | ✗ Still says 101; it's **102** |
| 9 | Box in the first bedroom frame at 0:01.5 | ✓ |

### Word count and timing (counted by hand)

| Beat | Words | Needed at 2.3 w/s | Window | OK |
|---|---|---|---|---|
| Hook (spoken) | 9 | 3.9s | 4.0s | ✓ |
| Problem | 15 | 6.5s | 6.5s | ✓ (no slack) |
| Dig + loop | **26** | 11.3s | 11.0s | ✗ by 0.3s |
| Reveal | 25 | 10.9s | 11.0s | ✓ |
| Turn | 10 | 4.3s | 4.5s | ✓ |
| Result + CTA | 17 | 7.4s | 7.5s | ✓ |
| **Total** | **102** | **44.3s** + 1.5s POV + 1.5s press-on ≈ **47.5s** | | ✓ inside 30–50s |

Problem 0:00–0:34 ≈ 72% (76 of 102 words); the patch as the answer ≈ 0:34–0:43.5 ≈ 20%; the CTA ~4s after. ✓ 80/20.
Box in frame at 0:01.5 ✓. Stands alone, loop opens 0:23 and closes by 0:34, no part 2 ✓. No talking with a patch on ✓.

### Credit check (TOF cap 135; first pass ≤ 120 after the 15-credit retry reserve, per `brief.md`)

Her voice is native to the Kling clip, so every second she's heard needs generated talking footage, **including
under the cutaways** (the 6.5s photo insert and the 3s sleeping shot sit on top of a talking clip that still has to
be generated). As written:

| Footage | Kling seconds |
|---|---|
| Talking head 0:01.5–0:38.5, continuous under both cutaways | ~37 |
| Morning talking + CTA voice | ~7.5 |
| POV frame one (1.5s used, ~3s minimum clip) | ~3 |
| Sleeping cutaway (own clip) | ~3 |
| Press-on (1.5s used, ~3s minimum clip) | ~3 |
| **Total** | **~53.5s × 2.5 ≈ 134 credits** + stills 5–10 ≈ **139–144** |

That's over the 135 hard cap and well over the 120 first pass. Even counting only the 47.5s of screen time
(47.5 × 2.5 + stills ≈ 124–129) it's over the first-pass budget, with nothing left for the one retry the press-on
is likely to need. Producibility has to be settled here, before the storyboard, not by the producer stopping mid-run.

### Scores

| # | Item | Score | Reason |
|---|---|---|---|
| 1 | Hook is a question, lands within 5s | **9** | Question on screen at 0:00 over a moving frame one; spoken question done by 0:05.5 |
| 2 | Hook fits the persona | **9** | "Mid-30s" + "suddenly" + "every photo" is P1's exact "is that me?" photo moment; a 22-year-old or a posing-tips seeker scrolls past |
| 3 | Hook makes sense cold | **9** | Instantly clear, and paid off with a real cause |
| 4 | Body digs in | **9** | Birthday, "asking for a manager", "are you mad at me?", hiding at the back (matches frame one) |
| 5 | Smooth turn | **9** | "So tonight, these hold my skin flat while I sleep" answers "pressed in while I sleep" directly; no banned phrase; box in frame since 0:01.5 |
| 6 | Logic | **8** | Round-1 holes closed. Left: the 0:05.5 visual says "last night's group photo" against a same-night bedroom (fix C); she applies in her party top, so the face must read freshly washed for "clean, dry skin" (fix D) |
| 7 | Subtle CTA | **9** | Owner's phrasing with PHOTO, own full-screen card, in the caption |
| 8 | Claims | **9** | All approved (table below); nothing permanent, no stats, credentials or reviews |
| 9 | Stage job / stands alone / length / strategy fit | **9** | TOF-U: mostly problem, patch as the answer with one line on how it works, brand on box, screen and caption; 47.5s; no sequel |
| 9b | One idea | **9** | Opener → belief 1, no objection, one CTA |
| 9c | Would she believe it? | **8** | "Forehead smooth" with a same-framing, softer-not-erased comparison; depends on the overlay staying subtle |
| 10 | Lessons learned | **8** | No second voice, photo in code, one action per shot, product by 2s, no talking with patches on, press-on sitting up. Press-on is the §8 hands risk |
| 11 | Producible (Kling 3.0, TOF cap) | **7** | Every shot is now doable, but the story as written costs ≈ 139–144 credits (table above), over the 135 cap and the 120 first pass. **Blocks approval** |

### TOF hook scores and Shareability (bar: 9)

| | Score | Pass? |
|---|---|---|
| Hook 1: question, within 5s | 9 | ✓ |
| Hook 2: persona fit | 9 | ✓ |
| Hook 3: cold sense | 9 | ✓ |
| **Shareability** | **9** | ✓. "Anyone else get asked this?" on screen and in the caption asks for comments on purpose; "asking for a manager" and the pillow cause are send-to-a-friend lines |

### Claims check

| Line | Claim | Source | OK? |
|---|---|---|---|
| "A lot of these lines get pressed in while I sleep, folded into my pillow every night" | Opener | Lessons §2 optional opener; brief claim 3 | ✓ (keep "a lot of" in any trim) |
| "…and they stopped fading" | Her experience of the problem, not a product claim | Lessons §2 ("no longer fade by midday") | ✓ |
| "So tonight, these hold my skin flat while I sleep" | Usage (overnight) + belief 1 | Lessons §1, §2 belief 1 | ✓ no "8 hours" |
| "Morning. Forehead smooth, still me, just not mad." | First-person result + identity | Lessons §2 "smoother skin by morning", "still look like herself" | ✓ not permanent |
| Before/after overlay (softer, not erased) | Allowed | Lessons §0 | ✓ |
| Caption | Opener + brand + keyword | | ✓ |
| Credentials / statistics / reviews / permanent / "11s" / "8 hours" / "rinse and dry" | none | | ✓ |

Clean. No automatic fail.

### Fixes (do all; resubmit as v3 — the last allowed revision)

**A. Budget: cut ~8 spoken words and one generated clip so the first pass fits ≤ 120.**
- Problem (0:05.5): **"Best friend's birthday. Best night ever. My forehead? Asking for a manager."** (12 words, 5.2s; was 15).
- Reveal (0:23): **"It's not my mood. A lot of these lines get pressed into my pillow every night, and they stopped fading."** (20 words, 8.7s; was 25). Keeps the approved opener's "a lot of".
- Sleeping cutaway: make it a **checked Nano Banana still with a slow code push-in** (her asleep on her side, forehead in the light-grey pillow, no patches), not its own Kling clip. It sits under her voice anyway.
- Press-on (0:38.5): **out of the first pass.** The turn already shows the piece; the story works without it. It only comes back if the preflight leaves room above the 15-credit reserve.
- Result: ≈ **94 words ≈ 40.9s + 1.5s POV ≈ 42.5s** (inside 30–50s). Kling ≈ 41s talking + 3s POV ≈ 44s × 2.5 ≈ 110 + stills ≈ 7.5 ≈ **118 credits** ✓.
- Add a one-line credit estimate (Kling seconds × 2.5 + stills) to section 6 so the storyboarder inherits it.

**B. Dig + loop (0:12) window.** The line is 26 words (11.3s). Keep the line (the "hide at the back" detail is P1's own) and give it an **11.5s window**, re-timing every later beat from the new counts so no window is shorter than words ÷ 2.3.

**C. Timeline label (0:05.5 visual).** "last night's group photo" → **"tonight's group photo"** (the bedroom is the same night). "Last night's frame" stays correct only in the morning before/after.

**D. Clean skin before the patch (0:34 turn).** Add to the visual: **makeup off, face freshly washed, bare and matte** (party top can stay, studs stay). Usage is clean, dry skin (lessons §1), and the before/after frame needs the same bare skin to be like-for-like.

**E. Section 6 recount.** State the real counts after A–B (≈ 94 words) and the new problem/product split; v2's "101" is wrong (it's 102).

**F. Caption hashtag.** `#grouphoto` → **`#groupphoto`**.

Everything else stays as is: hooks A/B/C, frame one, the turn line, the morning line and CTA, and the on-screen cards.
With A–F in, items 6 and 11 reach ≥ 8 and the story approves. If v3 is rejected, the run stops and goes to the owner
(`review.max_story_revisions: 2`).

---

## Round 3 (story v3) — Verdict: **APPROVED**

Independent review of `story.md` v3 (revision 2 of max 2, the last allowed). Re-read in full: `.claude/agents/story-reviewer.md`,
`pipeline/config.yaml`, `docs/creative-strategy.md` (§2, §6), `docs/lessons-learned.md`, `learning/playbook.md` (nothing
RETIRED), `brief.md`, `format.md`, `story.md` v3, and every earlier section of this file.

Every item is 8 or higher, the three TOF hook scores and Shareability are each 9, the claims are clean, and the first pass
fits the 120-credit budget at the checked Nano Banana price. There are three storyboard notes at the end. They're binding
for the storyboarder, but none of them needs a story rewrite.

### Round-2 REVISE fixes A–F: did they land?

| Fix | Asked for | In v3? |
|---|---|---|
| A | Problem line cut to 12 words; reveal cut to 20 with "a lot of" kept; sleeping cutaway made a still with a code push-in; press-on out of the first pass; credit line in §6 | ✓ all five. Problem = 12 and reveal = 20 by my count; "A lot of these lines…" kept; the sleeping shot is a checked still with a push-in; the press-on is out (it only returns if the preflight leaves room above the reserve); the §6 credit line is there |
| B | Keep the 26-word dig line, give it an 11.5s window, re-time the later beats | ✓ 0:11–0:22.5 = 11.5s; every later beat re-timed (table below) |
| C | "tonight's group photo" | ✓ in the 0:05.5 visual and in storyboard note 1 |
| D | Makeup off, freshly washed, bare matte skin at the turn and in both before/after frames | ✓ from the first bedroom frame (0:01.5) onward, so the whole night talking head, the turn and both comparison frames match |
| E | Real counts in §6 | ✓ It says 94 words, 43.5s, 72/18/9. My own count matches |
| F | `#groupphoto` | ✓ |

### The one change nobody asked for: frame one is now a still with code motion

v3 builds the 0:00–0:01.5 POV as a checked Nano Banana still, with a code push-in, a blinking timer light and the flash
popping white. Before, it was a ~3s Kling clip. I judged it against lessons §3 ("motion in frame one, never a static title
card") and strategy §6 ("motion or a pattern break"). **It passes, and the hook still lands.**
- There is motion from frame 0 (the push-in), and there's a pattern break (the white flash pop). Library SFX (timer beeps,
  laughter, shutter click) carry the sound layer. The on-screen question is up at 0:00. It's a photo of her world, not a
  title card.
- It fits the story better, too. The moment is a photo being taken, so a frozen frame that ends on the flash *is* the photo.
- What's lost is the friends visibly squeezing in. That's a small loss in a 1.5s beat, and it takes a 5-person,
  identity-locked Kling clip out of the producibility risks.
- Conditions are in storyboard note 1: start the push-in on frame 0 with no static hold, and put the flash right before
  the 0:01.5 hard cut.

### Word count and timing (counted by hand)

| Beat | Window | Words | Needed (÷ 2.3) | OK |
|---|---|---|---|---|
| Hook, spoken "Since when do I look mad in every photo?" | 0:01.5–0:05.5 = 4.0s | 9 | 3.9s | ✓ |
| Problem "Best friend's birthday … Asking for a manager." | 0:05.5–0:11 = 5.5s | 12 | 5.2s | ✓ |
| Dig + loop "She saw it … Then I found out why." | 0:11–0:22.5 = 11.5s | 26 | 11.3s | ✓ |
| Reveal "It's not my mood … they stopped fading." | 0:22.5–0:31.5 = 9.0s | 20 | 8.7s | ✓ |
| Turn "So tonight, these hold my skin flat while I sleep." | 0:31.5–0:36 = 4.5s | 10 | 4.3s | ✓ |
| Result + CTA "Morning. Forehead smooth … what I use." | 0:36–0:43.5 = 7.5s | 17 | 7.4s | ✓ |
| **Total** | | **94** | **40.9s** + 1.5s silent POV = **43.5s** | ✓ inside TOF 30–50s |

- **80/20:** the problem runs 0:00–0:31.5, which is 72% of the runtime and 67 of 94 words. The patch as the answer runs
  0:31.5–≈0:39.5 (the turn plus "Morning. Forehead smooth, still me, just not mad."), ≈8s ≈ 18%. The keyword CTA is ≈4s
  (≈9%) and is its own required beat. ✓
- **Brand visible:** the box is on the nightstand, brand side out, from 0:01.5 (inside the first 2s). The product and
  brand name are on screen at the turn, and the brand is in the caption. It never reads like a tips page. ✓
- **Stands alone:** the loop opens at 0:22 ("Then I found out why") and closes at 0:22.5–0:31.5. There's no part 2 or
  tease. ✓
- **No talking with patches on:** there are no patches-on beats at all. At the turn the piece is held up, not worn. In
  the morning it's off and held in her fingers. ✓
- **PHOTO CTA:** "Comment PHOTO and I'll send you what I use" is spoken, gets a full-screen card, and is in the
  caption. ✓

### Credit math (recomputed; TOF cap 135 minus 15 reserve = 120 first pass)

Her voice is native to Kling 3.0 Pro (≈2.5 credits/s with sound), so every second she's heard is generated talking
footage, including the seconds under the two code cutaways. Clips are counted in whole seconds.

| Footage | Span | Kling seconds |
|---|---|---|
| Night talking head, hook + problem (the photo insert sits on top) | 0:01.5–0:11 = 9.5s | 10 |
| Night, dig + loop | 0:11–0:22.5 = 11.5s | 12 |
| Night, reveal + turn (the sleeping still sits on top) | 0:22.5–0:36 = 13.5s | 14 (or 9 + 5 if split at the turn: same total) |
| Morning talking + CTA voice (the before/after and CTA card are code overlays) | 0:36–0:43.5 = 7.5s | 8 |
| Frame-one POV | still + code | 0 |
| **Kling total** | | **44s × 2.5 = 110** |

Stills I count: night start frame (also the identity reference), turn start frame (sheet in hand), POV frame, tonight's
photo, sleeping, morning frame = **6**. At the 1.5/image price checked with get_cost on Nov 7 (lessons §9) that's **9**, so
the first pass is **≈119 ≤ 120** ✓. At the top of the 1.5–2 range it would be 12 and **≈122**: 2 over the first-pass
target and still 13 under the hard cap. Storyboard note 2 below closes that gap at any price. The Kling POV (+7.5) and the
press-on (+7.5) stay out unless the preflight shows room above the reserve. The one clip retry has 15 credits, which
covers ~6s of footage, so a retry of the 12s or 14s clip would break the cap. Re-cut the bad clip (or split it), or stop
and flag. Don't re-render a long clip whole.

### Scores

| # | Item | Score | Reason |
|---|---|---|---|
| 1 | Hook is a question, lands within 5s | **9** | On-screen question at 0:00 over a moving frame one (push-in, timer blink, flash pop, beeps); the spoken question is done at 0:05.5, against 3.9s needed in a 4.0s window. The still-with-motion frame one keeps it a 9 |
| 2 | Hook fits the persona | **9** | "Mid-30s and suddenly mad in every photo?" plus "Since when…" is P1's own "is that me?" photo moment; a 22-year-old or a posing-tips seeker scrolls past |
| 3 | Hook makes sense cold | **9** | Instantly clear, and the video pays it off with a real cause, not clickbait |
| 4 | Body digs in | **9** | The birthday, "asking for a manager", "are you mad at me?", hiding at the back (which agrees with frame one) |
| 5 | Smooth turn | **9** | "So tonight, these hold my skin flat while I sleep" answers "pressed into my pillow every night" directly; no banned transition; the box has been in frame since 0:01.5 |
| 6 | Logic | **9** | Fixes C and D closed the last two holes: it's tonight's photo, and her skin is washed and bare before the patch, so the before/after is like-for-like. "So tonight" explains why tonight's photo still shows the problem. One soft spot remains, not a hole: when she bought the box is left unsaid |
| 7 | Subtle CTA | **9** | The owner's phrasing with PHOTO, its own full-screen card, also in the caption |
| 8 | Claims | **9** | All approved (table below); usage is overnight; no "8 hours", nothing permanent, no stats, credentials or reviews |
| 9 | Stage job / stands alone / length / strategy fit | **9** | TOF-U: the cause-reveal opener closes on belief 1; 72/18/9 split; brand on the box, on screen and in the caption; 43.5s; no sequel |
| 9b | One idea | **9** | One belief (opener → belief 1), no objection, one CTA |
| 9c | Would she believe it? | **8** | "Forehead smooth" with a same-framing, softer-not-erased comparison on bare skin. It still depends on the overlay staying subtle in production |
| 10 | Lessons learned | **9** | Motion in frame one (code, not a title card); no second voice; photo and text in code; one action per shot; product by 2s; no talking with patches on; the press-on (the §8 hands risk) is out |
| 11 | Producible (Kling 3.0, TOF cap) | **8** | Every shot is simple: talking heads, one hold-up, a talking morning shot, three stills with code motion. It fits ≤120 at the checked price, with a thin margin (notes 2 and 3). The remaining risks are the clear piece showing up at the turn and seamless joins between night clips |

### TOF hook scores and Shareability (bar: 9)

| | Score | Pass? |
|---|---|---|
| Hook 1: question, within 5s | 9 | ✓ |
| Hook 2: persona fit | 9 | ✓ |
| Hook 3: cold sense | 9 | ✓ |
| **Shareability** | **9** | ✓. The "Anyone else get asked this?" card and caption ask for comments on purpose; "asking for a manager" and the pillow cause are send-to-a-friend lines |

### Claims check

| Line | Claim | Source | OK? |
|---|---|---|---|
| "A lot of these lines get pressed into my pillow every night" | Opener | Lessons §2 optional opener; brief claim 3 ("a lot of" kept) | ✓ |
| "…and they stopped fading" | Her experience of the problem, not a product claim | Lessons §2 situation 2 | ✓ |
| "So tonight, these hold my skin flat while I sleep" | Usage (overnight) + belief 1 | Lessons §1, §2 belief 1 | ✓ |
| "Morning. Forehead smooth, still me, just not mad." | First-person result + identity | Lessons §2 "smoother skin by morning", "still look like herself" | ✓ not permanent |
| Before/after (softer, not erased) | Allowed | Lessons §0 (Nov 7) | ✓ |
| On-screen product/brand name; caption | Product name + opener + keyword | Lessons §1 names; brief | ✓ |
| Credentials / statistics / reviews / permanent / "11s" / "8 hours" / "rinse and dry" / price | none | | ✓ |

Clean. No automatic fail.

### Storyboard notes (binding, no story rewrite)

1. **Frame one:** the push-in starts on frame 0 with no static hold. The timer light reads as real motion (a pulsing glow
   on the faces is fine). The white flash pops at ≈0:01.2–0:01.4, right before the hard cut. The still passes checklist A.
2. **Budget robustness:** use the POV frame as **tonight's photo** (cropped and pushed in to her forehead). It's the same
   moment the timer phone captured, so continuity improves and one still drops: 5 stills ≤ 10 credits, so the first pass is
   ≤ 120 at any Nano Banana price in the 1.5–2 range. Preflight every job with `get_cost: true`.
3. **Night clip joins:** put the cuts between night clips under the cutaways or at beat boundaries. If the sheet has to
   appear in her hand, split the reveal + turn clip at 0:31.5 (9s + 5s, same 44s) so the turn opens on its own checked
   start frame with the sheet already in hand. Don't make her reach for it mid-sentence. Light the clear piece from the
   side or behind with the lamp (§8 invisible silicone).
4. The round-2 APPROVED notes 1, 3 and 4 still apply (timeline label, before/after softer not erased, brand text in code).

# Owner feedback log

**Read this before every stage.** It records how the owner actually judges our
work: what they asked for, what they corrected, what they waved through, and what
they loved. It calibrates every agent, especially reviewers. A reviewer that
fails a video on something the owner has called minor wastes their time. A
generator that repeats something they corrected wastes credits.

**How it's kept:** the main session adds an entry every time the owner:
- gives a direction for a run ("do it like this video", "use this voice"), or
- answers a question the pipeline raised: accept, reject, "not a big deal",
  "change that", or
- reacts to a finished video.

Each entry says what happened and **the rule it sets**. A rule that holds
across runs is promoted to `docs/lessons-learned.md` §0. Owner words are
quoted.

## Trial mode (from Nov 8, 2026)
The pipeline is **not scheduled**. The owner picks each video ("take this
video and do it like this"). The main session runs it through the full flow
and records every owner decision here. Scheduling (3 a day) starts only when
the owner says so.

---

## Standing calibration (rules so far)

### What the owner liked
- **2-T "One night on your pillow" (Nov 8):** "The second video you created was awesome. It was really good."
  - **What worked:** a winning ad from any category (Resilia's see-through Pixar skeleton day-by-day timeline) mapped onto our problem; Pixar-style animation; voiceover only; clock cards; a technical explanation in approved words; a fast cut; a real box and hero end card.
  - **Rule:** use this as the reference for quality and format. It's a strong candidate for iterations: the same structure with other personas and problems.

### What the owner asked for (keep doing)
- **Animated shots say "Pixar style".** Animated characters never talk; the narration is a voiceover.
- **A still for every sequence** before any video.
- **Technical explanations** of how the silicone works, in approved words.
- **Length as the owner sets it** ("about 45 seconds"). 42.7 s was fine.
- **Captions:** one caption, at most 2 hashtags, tailored to the avatar: her habit or problem, plus her age or identity (e.g. #sidesleeper #skincareover35). Captions carry persuasion between the video and the site.
- **Real people must match the animated character.** If the Pixar character is white, the photoreal woman is the same white woman. Never mix two different-looking women in one video.
- **Voice:** the owner prefers **Higgsfield Zoe** (seed_audio, preset `d0374db1-44b9-4f05-939e-0a9ae9dbbe6a`, speech_rate 15). That take was 49.5 s raw for 133 words and fits ~45 s once pauses are trimmed.
  - They liked Zoe better than Gia (530df032…).
  - They asked for ElevenLabs Hope, which was blocked: ElevenLabs had too few credits.
  - Default to Zoe for voiceovers unless they name another voice.

### Who the videos are for
- **US viewers only** (Nov 8, 2026). 2-T reached 64.8% India and 0% US: "we definitely don't want this".
  - Results are judged on US viewers. **18–34 is fine** (owner, Nov 8: "18-34 is fine, that is not an issue"); country is the problem, not age. Views from elsewhere are reach, not success.
  - Every video carries US signals: American English, US settings and props, US-coded captions, posting at US Eastern times.

### What the owner waved through (don't block on these)
- **A character's mouth opening with no speech** in a voiceover video. "If her mouth just opens that is okay keep it."
- **Small artifacts in a short clip** that the edit can hide (e.g. the plunger in C21). "C21 is also good, is minor." Hide them in the edit; don't stop the run.
- **Skull teeth faintly visible through a see-through Pixar cheek.** "I didn't even notice that, don't change that."
- **Rule for reviewers:** in see-through or Pixar shots, anatomy quirks that a viewer doesn't notice at phone speed are notes, not FAILs. FAIL only what a viewer would notice:
  - a wrong face or character;
  - mouthing words;
  - a broken product: wrong patch shape, white or opaque patches;
  - unreadable or wrong text;
  - unapproved claims.

### What the owner corrected (never repeat)
- **Think like a human marketer** (Nov 8, 2026): break the reference down
  first. How does it make the problem obvious to a cold viewer in 3–5 s? Do
  the same for our avatar, showing cause → effect. Marks alone can read as
  "cat scratches".
- **No exaggerated reactions** (Nov 8, 2026): the overacted sad/screaming face "just doesn't click".
- **Live-footage formats are all video** (Nov 8, 2026): no stills with zoom or shake.
  "It's supposed to be all video, don't know what in your logic told you to
  put 2-3 images in there and zoom into them."
- **Reviewers must catch these** (Nov 8, 2026): the overacted face and the stills both passed
  review. Reviewers now run a cold-viewer test, a reaction check and a medium check.
- **Nothing may look like an injury** (Nov 8, 2026): sleep creases, redness or marks must never read as scratches, cuts or a rash. "We don't want nothing looking like injuries."
- **Don't assert product facts they haven't confirmed** ("You don't know what's true or false about my product"). Result claims come from lessons §1–2 only.
- **No "part 2" videos.** One video starts and ends an idea.
- **TOF is mostly the problem,** for unaware or problem-aware viewers, and still shows the brand subtly.
- **Before/afters are allowed.** Authority looks (including a doctor's look) are allowed, but no stated credentials.
- **Don't save owner proposals as decisions.** Only their explicit words count.

### How the owner decides spend
- **Short video = 50 credits max, all versions** (Nov 8, 2026): "135 is for a 45 seconds video, this is a short video, no more than 50 next time." The trend remake used 84, so it went over.
- **One pool per video, all versions included** (Nov 8, 2026): "new versions don't count as a new pool of credits, you work with what is left unless I give you permission."
- They approve small paid fixes readily: "Yes, fix them", "Yes, rebuild them". Each fix gets one try, then it comes back to them.
- When a cheaper or free option exists, offer it first; they usually accept it ("Start frame only").
- **"If it requires any more credits stop"** applies to unrequested fixes and research. Work they asked for may spend within the slot cap.

---

## Entries (newest last)

| Date | Run | What came up | Owner's answer (quoted) | Rule it sets |
|---|---|---|---|---|
| 2026-11-07 | 1-T | Fast-paced edit, voice, lip sync | "make these changes if they are free… if it requires any more credits stop" | Free edit upgrades are always fine; paid ones need a yes |
| 2026-11-08 | 1-T | Captions | "copy or captions are really important as they do a lot of the heavy lifting" | Every video ships with a caption set, written for persuasion |
| 2026-11-08 | — | Packaging | Asked for a branded box and hero shot from the site's branding | Use the real box asset (lessons §7); never let a model redraw it in a video |
| 2026-11-08 | 2-T | Reference | "Run the flow using this ad as a reference, different persona" (Resilia) | The owner names the reference; the scout breaks it down and maps it |
| 2026-11-08 | 2-T | Length | "I just need this to be about 45 seconds" | Owner length overrides the stage band |
| 2026-11-08 | 2-T | Style | "use the term pixar style in your animations" | Lessons §0 |
| 2026-11-08 | 2-T | Stills / voice | "create still images of each sequence, don't make the skeleton talk, use voice over" | Stills for every shot; animated characters never talk |
| 2026-11-08 | 2-T | Mechanism | "Use technical explanations about how silicon patches help the skin" | Explain the mechanism in approved words |
| 2026-11-08 | 2-T | 3 failed stills (paid fix) | "Yes, fix them" | Approves small fixes; one try each |
| 2026-11-08 | 2-T | Missing end frame for clip C06 | "Start frame only" | Prefers the free option when it exists |
| 2026-11-08 | 2-T | Voice | "use hope from elven labs" → blocked by ElevenLabs credits → "Use GIA on higgsfield" → "Try Zoe" → "I like ZOE better" | Zoe is the default voice |
| 2026-11-08 | 2-T | C10 open mouth, C21 plunger | "If her mouth just opens that is okay keep it, C21 is also good, is minor" | Don't block on these |
| 2026-11-08 | 2-T | Reviewer FAIL: teeth through cheek | "I didn't even notice that, don't change that" | Reviewer severity calibration (above) |
| 2026-11-08 | 2-T | Realistic woman didn't match the character | "using a white woman instead of a brown woman, as the character is already white" | Photoreal people match the animated character |
| 2026-11-08 | 2-T | Recast half failed | "Yes, rebuild them" | Rebuild from the good new frame, not by editing the old person |
| 2026-11-08 | 2-T | Caption | "not more than 2 hashtags and make them hashtags tailored to avatar" | Caption rule (above) |
| 2026-11-08 | 2-T | Result | "The second video you created was awesome" | 2-T is the quality bar |
| 2026-11-08 | 1-T, 2-T | First numbers | 1-T v3.1: 36/233/39 views (IG/FB/TT), ~60% gone by 2 s, audience 35–64. 2-T: 1392/7/36, 13 s average watch, 50% held to 11 s, 90% 18–34, 64.8% India, 0% US. "we definitely don't want this" | US-only audience rule (above). The 1-T hook (static photo POV) failed; 2-T's moving animated opener held |
| 2026-11-08 | 2-T | Why India? | "18-34 is fine… it might the time at which I posted, I posted at about 3 AM, although I have another animation video i posted a month ago at night, and it also went 60% to india" | Age is fine. Posting time is a likely cause (3 AM Eastern is 1:30 PM in India). The account already skews India from an earlier animated video. Test: post the next videos at 7–9 pm Eastern and compare the country split |
| 2026-11-08 | — | Boosting to fix the country split | "we are not running ads yet" | No paid boosts or ads during the trial. Fix reach organically: post at 7–9 pm Eastern, use a US location, seed early engagement. Record the posting time with every metrics read |
| 2026-11-08 | ref-problem-vs-solution | New reference: a 15 s trending "The Problem 😭 / Vs… / The Solution 😌❤️" UGC video (car + body pillow) | "take out the marketing philosophy and structure… same vibes, same story, for our product… keep it the same length… keep the same captions, everything… I want the same audio… if you cant get it yourself, just give me the video" | For trend remakes: match length, captions and cut rhythm exactly. Change the setting if needed. Deliver the video without audio, cut to the song; the owner adds the trending sound in the app |
| 2026-11-08 | ref-problem-vs-solution | S1 pillow creases looked like red scratches | "Yes, redo it. We don't want nothing looking like injuries." | Skin marks must never read as injury. Prompt creases as soft pressed lines, never red streaks |
| 2026-11-08 | ref-problem-vs-solution v2 | Owner critique of the remake | Unaware viewers can't tell what the marks are; the overacted crying "doesn't click"; the shaky stills should be video; the solution is "alright, still could be better". "Fix this, don't spend more than 40 credits" | New rules (above). Reviewers get hard checks. Remake v3: a night time-lapse with her face in the pillow → lights on, she notices the lines → he gives her the patches → several nights in them → she wakes up smoother. All video, ≤40 credits |
| 2026-11-08 | — | Owner idea for the same format, another avatar | Mid-30s woman who stopped taking selfies: POV of her zooming into her face on the phone, deleting the photo or turning to a mirror (e.g. in the car), frustrated → her boyfriend gifts her the patches | Logged in next-moves.md for the next remake |
| 2026-11-08 | ref-problem-vs-solution | 84 credits total across versions (45 for v1–v2 + 39 for v3) | "new versions don't count as a new pool of credits, you work with what is left unless I give you permission" | The cap covers all versions; a new version gets only what's left. Lessons §0 and producer.md |
| 2026-11-08 | ref-problem-vs-solution | 84 credits on a 15 s video | "135 is for a 45 seconds video, this is a short video, no more than 50 next time" | Short videos cap at 50, all versions (config + lessons §0) |
| 2026-11-08 | ref-real-or-sus-p4 | Expert talking clips | "Can you try opening google chrome and running the clips of the expert on google gemini?" … "If gemini runs out, use higgsfield" … "Keep the same process, gemini is just another option to generate, but you still check the prompts, review generations… gemini I have found is 10x better than kling at lip sync" | Gemini Veo is the default for talking clips, with Higgsfield as fallback. The pipeline still applies: prompt review before submitting and a generation review after. The first Gemini clip skipped prompt review; never again |
| 2026-11-08 | ref-real-or-sus-p4 | Peel clip | "The video where the woman peels off the patch from her forehead requires careful consideration and high physics details on how a patch peels off of a forehead, otherwise it will look fake" | Every peel prompt follows lessons §6 beat by beat (fold-back, fold line traveling, frosted doubled part, last edge lets go). Pass-2 review checks the peel physics against §6 specifically |
| 2026-11-08 | ref-real-or-sus-p4 | Gemini daily limit hit; wait a day or use Higgsfield for the naming line | "Do it on higgsfield, I have no patience" | Speed beats a perfect voice match. When Gemini runs out, go straight to Higgsfield within the cap; no need to ask |
| 2026-11-08 | ref-real-or-sus-p4 | Delivered v2 (U1 apply shot) | "hands look quite dark as she moves them towards her, how cheap you think we can fix this for" … after a light shadow lift: "It still looks odd, any more free fixing?" | Hand skin must match the face/other hand in tone. Stills check and video review compare hand color to the face, not just shape. A mild shadow lift is not enough; a color match of the dark hand to the lit hand is the free fix that worked. Prompts: light both hands evenly (no hand in deep shadow near the lens) |
| 2026-11-08 | ref-real-or-sus-p4 | Peel jump cut (failed middle second hidden) | "Why the cut when she is peeling it off? Clip didn't come out right?" | The owner notices hidden-failure jump cuts. Cutting around a failed generation is not invisible; say so plainly when delivering, and prefer a redo when the action itself is the selling moment |
| 2026-11-08 | ref-real-or-sus-p4 | Asked what we're missing vs a fully AI Dermaclara ad that shows the peel | "this video is ai completely and they pull the peel off, what are we missing" | Peels are doable; ours failed on staging, not the model. Lessons §6 now has "Staging that makes an AI peel work": start mid-peel, pull sideways off the face, anchoring hand, 3/4 angle, ~1 s beats with cuts between different patches |
| 2026-11-08 | ref-real-or-sus-p4 | Asked how the Dermaclara AI ad gets near-zero mistakes | "this is what I strieve for, accuracy and not losing any more credits" | North star: accuracy per credit. Default live-action shots to Gemini Veo (subscription, no credits) when the daily quota allows; keep each shot to one simple, common action; stage hard actions (peel) per lessons §6; test risky motion on a cheap short draft before a pro render; use only the best 1–3 s of each generation |
| 2026-11-08 | ref-real-or-sus-p4 | Peel redo; sent a real peel video | "having it show resistance like it's actually stuck to the skin… see how the patch and skin show resistance as it is getting peeled, I want that… let's keep trying gemini iterations until we find the prompt that gets these peels right, try 2-3 second clips… with gemini we won't spend credits" / "If gemini is stuck, try a new chat" | Peels must show resistance (lessons §6 updated: slow stop-start pull, rippling peeled part, skin lifts a hair and springs back at the release line, anchor hand presses). The old "skin never tugged" rule is replaced. Peel R&D runs on Gemini (free), short 2–3 s actions, iterate prompt until it passes; a stuck Gemini chat gets a new chat, not a wait |
| 2026-11-08 | ref-real-or-sus-p4 | Peel budget and lock-in | "Try on higgsfield no more than 15 credits total you have just to get the peel right, the gemini one looks better so figure out what you did right and add on top of it for the perfect shot… lock down the exact prompt that is providing us the best physics for patch peel" | 15 cr spent (Kling 4.0 9 + Kling 3.0 std 6). The winner chains Gemini T1 (first half) with a Kling clip continuing from its last good frame. Recipe locked in `learning/peel-recipe.md`; the prompt-engineer, prompt-reviewer and storyboarder must use it |
| 2026-11-08 | ref-real-or-sus-p4 | v3 delivered (hand fix by colour grade, chained peel) | "[Hands] still look real bad. I would rather have you regenerate the whole thing and make sure that in the prompt you account for that. So even if it takes you like 40 credits again, do it… I'm expecting you to use Gemini for some other creations instead of Higgsfield… no changes in light or level of light on both hands… the peel… should be smooth, continuous resistance… For a second it didn't move at all, then it kept going. I don't want that… it doesn't have to stay literally stuck for 1 second" | A colour grade doesn't fix a bad hand: regenerate, with the lighting accounted for in the prompt (both hands in the same light as the face, never darker near the lens; avoid one-sided lamp light in shots with hands). Peel resistance = smooth, continuous, even motion with stretch; never a pause (the recipe wording "stop-start tugs" is replaced). Budget for this fix is up to 40 cr. Prefer Gemini for generations whenever it's available, to save credits |
| 2026-11-08 | ref-real-or-sus-p4 | v4 review: how her hands hold the patches | "it doesn't look like she is actually holding the patches… both her hands are straight, and it's like the patches are just stuck to… her hands, when really the sticky side is on the other side… You need to… hold them with two fingers, like pinching them as you put the patch on… Putting the patches on, peeling the patches off… we need to nail that down… we're gonna have that on most of them" / "maybe you can do some deep research on prompting for AI video generation models… the next time Gemini's window of usage clears, let's [try] again on Gemini" / "don't generate anything right now" | Grip rule: a patch is always held by its edge or tab in a thumb-and-index-finger pinch (other fingers curled, relaxed), never pressed flat on an open palm or fingers; the sticky side faces her skin and the fingers never touch it. Applying and peeling are the two core shots of the brand: both get a locked recipe. Research prompting before the next Gemini test; no generation until then |

# Production fixes research: lip sync, UGC voice, fast-paced editing

Researched 2026-11-07 after the first finished video (`runs/2026-11-07-2002-1t-first-line-fixer`).
**No credits were spent.** All prices are Higgsfield `get_cost: true` previews taken today, unless a line says otherwise.

The owner had three complaints:

1. Kling 3.0's native lip sync is bad every time.
2. The voice is wrong. They want a fast, "yapping" TikTok UGC voice.
3. The reel is too slow.

---

## 0. What is actually wrong with our clips (measured)

I checked CLIP_A, CLIP_B1 and CLIP_B2 locally with Whisper word timestamps, 12 fps mouth crops, an audio-envelope vs mouth-darkness cross-correlation, and `silencedetect`. Work files are in `scratchpad/lipsync/`.

**There is no global drift.** The best audio-to-mouth lag is 0 / +1 / −1 frame (±42 ms) in A / B1 / B2. So this is not an offset you could fix by sliding the audio. Correlation is only 0.44–0.49, though, which means the mouth follows the loudness loosely, not phoneme by phoneme.

The problem is articulation. The mouth hits the right rhythm but the wrong shapes:

| Where | What should happen | What happens |
|---|---|---|
| A 9.84–10.12 "by my" | Two full lip closures (b, m) | Lips never close; teeth stay slightly parted the whole time |
| A 5.4–6.0 "look smooth" | Rounded "oo", tongue for "th" | Lips sit closed and flat for about 0.5 s (mumbled) |
| B1 2.9–3.5 "peptides" | Second "p" closes | Broad toothy grin, no closure |
| B1 3.6–3.9 "even Botox" | Closure on the "B" at ≈3.91 | Closure lands ≈0.2 s early, during "even"; then a pout |
| B1 5.4–6.0 "lesser strength" | Changing shapes | Frozen bared-teeth smile for ≈0.6 s while the words continue |
| B2 10.12 "my", 12.67 "photo", 12.2 "Comment" | m / p closures | "my" doesn't close and its closure arrives ≈0.3 s late during "skin"; "photo" shows open teeth; "Comment" only half-closes |
| B2 11.6–11.9 "night" | Spread "ai" | Rounded "o" shape |

Mouth opening is also small overall. That fits the prompt's own delivery note: *"slightly breathy… speaking softly as if it is late at night."* Soft, breathy speech gives the model little jaw movement to animate, and it reads as mumbling.

**Pace: the words are fast enough; the pauses are not.**

| Clip | Length | Words | Overall rate | Silence ≥0.25 s | Rate with pauses cut |
|---|---|---|---|---|---|
| A | 14.0 s | 29 | 2.1 w/s | 5.7 s (40%) | ≈3.5 w/s |
| B1 | 13.0 s | 28 | 2.2 w/s | 4.3 s (33%) | ≈3.2 w/s |
| B2 | 15.0 s | 31 | 2.1 w/s | 7.0 s (47%) | ≈3.9 w/s |

- The prompts were written at about 2 w/s: 29 words in 14 s, 28 in 13 s and 31 in 15 s. The config sets `words_per_second: 2.3`, and Kling filled the gaps with pauses.
- Fast TikTok "yapping" UGC runs at about 3–3.5 w/s, roughly 180–210 wpm.
- The voice's median pitch is about 180 Hz. The UGC presets measured below are 210–275 Hz, so ours reads lower and calmer.
- The final cut has 12 cuts in 42 s, so the average shot is 3.5 s. One hold runs **8.0 s** (3.3–11.3) and another 5.9 s (15.7–21.6). It also has no burned-in speech captions.

---

## 1. Lip sync

### Is Kling 3.0 native dialogue known to be weak?

Partly.

- Guides put it at roughly 90% accurate in English, with drift on longer lines. The first and last words are the most fragile.
- Sync accuracy drops with two speakers, with non-English lines, and with long monologues.
- The recommended fixes are a short line (≤ ~20 words per clip, one or two sentences), one speaker, then trimming or regenerating ([sunra/ponpon Kling 3 audio guide](https://sunra.ai/blog/kling-3-audio-guide), [Magic Hour Kling 3.0 guide](https://magichour.ai/blog/how-to-use-kling-30)).
- Kling's own guide says to quote each line, keep lines short, split complex sentences, put a short delivery note next to the line, and bind a voice to the character element with a ≥3 s speech clip for a consistent voice ([Kling 3 Omni lip-sync guide](https://kling.ai/blog/kling-video-3-omni-native-lip-sync-audio-guide)).
- Comparisons rank Veo 3.1 ahead on talking-head realism and dialogue, Seedance 2.x as the UGC-at-volume pick, and Kling as the cheaper draft engine ([3daistudio](https://3daistudio.com/blog/best-ai-video-generator-2026), [Krea UGC models](https://www.krea.ai/blog/the-5-best-ai-video-models-for-ugc-shorts-in-2026), [ugccopilot](https://ugccopilot.ai/blog/sora-vs-veo-vs-kling-comparison-2026/)).
- Most of these are vendor blogs, and every one of them says to test on your own lines.

Our prompts broke most of these rules:

- 14–15 s clips with 28–31 words and 3–5 sentences each.
- An 800-word prompt in which the dialogue is a small part.
- A soft, breathy, "late at night" voice note.
- Head tilts, shrugs and hand counting during speech.
- Framing at about 40 cm head-and-shoulders, so the face is ≈360 px wide on a 1076-wide frame. That clears our 250 px minimum, but it is still small for lip detail.

**So it is both:** the prompts made it worse, and the model is only moderate at articulation.

### Prompt rules that should improve Kling (and Veo) dialogue

1. **One sentence per clip, 4–6 s clips, at most 12–15 words** (≈2.5–3 w/s of speech with almost no dead air). If a beat needs two sentences, make two clips and hard-cut between them. The cut is native to TikTok.
2. **Write the line with the timing you want**, not the timing of the clip: "She starts speaking at 0.2 s and finishes by 4.5 s, no pauses between sentences."
3. **Use a delivery note that produces jaw movement:** "fast, animated, clearly articulated, big mouth movements, like talking to her front camera to a friend." Never write "soft", "breathy", "whispery" or "late at night". Keep the night look in the lighting, not in the voice.
4. **Frame a medium close-up.** The face should be 45–60% of frame width (≥500 px on 1080), face-on, eyes to lens, mouth unobstructed, no hand near the mouth. Use a locked camera and a fixed head while speaking. Put gestures in the non-speaking beats.
5. **Name the speaker before the quote, then put the quote right after**, e.g. `She says, fast and animated: "…"`. Keep the prompt short. The Kling and Veo guides structure it as shot → speaker → action → exact quote → delivery → ambience. Long "what must not move" lists belong in the start/end frames, not in the text.
6. **No ALL CAPS, no digits, spell out hard words** (lessons §5 already says this). Avoid word clusters that stack bilabials ("by my", "Comment photo") in the hook line, or put them on a cutaway.
7. Add "**lips close fully on m, b and p; mouth is still and closed when she is not speaking**". This is cheap to add but untested, so treat it as a hint, not a fix.
8. **Use the same voice element, or the identical voice text, in every clip.** Kling can bind a voice to a character element from a ≥3 s speech sample, which also fixes drift between clips.

### Alternatives on our connectors (credits per second, Higgsfield preview today)

| Option | What it is | Price preview | Notes |
|---|---|---|---|
| Kling 3.0 pro + sound (current) | Native dialogue | 12.5 / 5 s, 25 / 10 s → **2.5/s** | std 2/s |
| **Veo 3.1** fast, basic | Native dialogue, best talking-head reputation | 32 / 8 s → **4/s** | preview variant basic: 80 / 8 s; high: 80 / 8 s (10/s). Start image only (no end frame). Durations 4/6/8 s |
| Seedance 2.5 | Native audio, or `omni_reference` with **audio_references** (drive the lips from our own audio) | 480p 3/s; 720p 7/s; omni_reference 480p 24 / 8 s = 3/s | 720p too expensive for full videos |
| Seedance 2.0 | Same idea, audio refs | 480p 30 / 10 s = 3/s | |
| **Wan 2.7** | Start/end frame + **audio_references** | 720p 15 / 10 s = **1.5/s**; 1080p 2.5/s | Cheapest audio-driven option; quality untested by us |
| Gemini Omni Flash 1.2 | Native audio | 720p 18 / 8 s = 2.25/s | |
| Kling 4.0 | i2v, up to 30 s | 1080p 32.5 / 10 s = 3.25/s | No sound parameter listed |
| **Higgsfield Intone** | Purpose-built talking head: character image + location + 1–6 voice recordings → lip-synced video, up to 30 s, up to 5 shots | **No preview possible** without a real audio media id (the cost API needs the audio's duration) | Best fit for an audio-first pipeline; preflight it on the first real run |
| **Sync Lipsync 3** (`sync_so`) | Re-syncs an existing video's mouth to new audio | 36 / 10 s, 50.4 / 14 s → **3.6/s** | sync.so direct: $0.107–0.133/s ([sync.so models](https://sync.so/docs/models)). Best for close-ups and obstructions |
| ElevenLabs "creative" connector | `sync-lipsync-v3`, `sync-lipsync-v2-pro`, `veed-lipsync`, `creatify-aurora` (image + audio → talking head), `minimax-h3-max-lipsync` (still + 5–14.8 s audio, no prompt), `heygen-avatar4`, `veo-3.1` | The connector exposes no prices | Runs on the ElevenLabs plan, not Higgsfield credits |
| Runway | Aleph edit 28/s (lessons §5); `runway-act-two` | — | Not needed |

**Fit against the caps.** A 30–35 s TOF video with about 25 s on camera:

- Kling pro: ≈62–75 credits. Fits 135.
- Veo 3.1 fast: ≈100–128. Fits TOF 135 only with almost nothing else; misses MOF 120 if more than ~28 s is on camera; misses BOF 70 at ≥18 s.
- Wan 2.7 audio-driven at 720p: ≈38–45, plus about 2.5 for TTS. Fits everything.
- Seedance 480p: ≈75–90. Fits TOF and MOF.
- sync_so as an extra pass over Kling: +90 credits. Over every cap.

### Recommendation for future runs

**Move to audio-first talking heads.** Write the line, then generate the voice with a chosen UGC voice (TTS ≈2.5–3.6 credits for a 40 s script; see §2). Then drive the face from that audio. Do it in this order:

1. **One-time bake-off, about 40–60 credits, owner approval needed.** Generate the same 6–8 s hook line from the same K1 still with:
   - Higgsfield Intone (run a real preflight first)
   - Wan 2.7 + audio reference: 720p, 8 s ≈ 12
   - Veo 3.1 fast native: 32
   - Kling 3.0 pro with the new prompt rules: 6 s ≈ 15

   Score each one on bilabial closures, mouth amplitude and identity hold.
2. Make the winner the default `audio_talking_head`. I expect Intone or Wan to win on cost and control, and Veo on realism. Audio-first also fixes complaint 2 and makes timing predictable for the fast edit.
3. **Owner rule conflict.** Lessons §0 says *"Talking on camera = voice generated by the same video model in the same clip"*, and §5 says a separate voice laid over a silent clip was rejected. Audio-driven lip sync is not a laid-over voice, because the mouth is generated from the audio. It still changes the owner's rule, so the owner must approve it.

If the owner keeps native Kling, apply the prompt rules above. Use 5–6 s single-sentence clips (Kling pro, 2.5/s) and keep each clip's line at or under 15 words.

### Post-hoc options for the existing clips

- **Voice change only** (Higgsfield `voice_change`): preview **1 credit per 10 s, 5 credits for 42 s**. It keeps the original timing, so sync is unchanged: no better and no worse. Speech-to-speech copies the source's prosody. It changes timbre and pitch but not energy, so a soft, breathy take stays soft. **It will not produce "yapping."**
- **New fast TTS + re-sync** (`sync_so`, 3.6 credits/s): only the on-camera seconds need it. That is about 25 s after a tight edit, so ≈90 credits plus ≈3 for TTS. It replaces the mumbled mouth with a fresh one, and new audio at 3+ w/s needs `sync_mode: remap` or a re-cut. **This run is at 128.5 / 135**, so it needs an owner cap increase. For the same money, a new Kling or Wan set with the new rules is the better buy.
- **Free option:** cut the pauses and cover the worst articulation moments ("by my", "strength", "Comment photo") with cutaways (§3). That costs nothing and removes most of what reads as "bad lip sync."

---

## 2. Voice

### (a) Prompting the video model's native voice

Replace the current voice block with something like:

> *"A bright, upbeat American woman in her late twenties talking fast to her front camera like she's telling her best friend something she just found out; quick, animated, clearly articulated, almost no pauses between sentences, rising energy, a little laugh in her voice."*

- Drop "slightly breathy", "softly" and "late at night".
- Size the script at **3.0 w/s of clip time**, not 2.3. A 5 s clip gets 13–15 words.
- Keep the voice text identical across clips, or bind a voice element in Kling.

### (b) Speech-to-speech on the existing audio

- Higgsfield `voice_change` needs a Higgsfield preset or element `voice_id`. It costs ≈0.12 credits/s (5 credits for the whole video).
- The ElevenLabs voice changer (`eleven_multilingual_sts_v2` on the creative connector) can use library voices such as Hayley. Third-party sources put it at ~1,000 plan credits/min, or ≈$0.12/min by API ([cloudzero](https://www.cloudzero.com/blog/elevenlabs-pricing/), [happyrobot](https://www.happyrobot.ai/hub/elevenlabs-pricing)).
- Both keep the timing, so sync is kept. As noted above, neither adds energy. Use speech-to-speech only to unify or upgrade timbre on a take whose delivery is already fast.

### (c) TTS with a UGC voice, then lip sync (recommended)

- `elevenlabs_v4` for the ~95-word script: **2.53 credits**. `seed_audio` with `speech_rate` +15: **3.6 credits**.
- Eleven v4/v3 take inline tags such as [laughs] and [excited].
- Generate one line per file and tighten the gaps to about 0.1 s in code.

### Candidate voices (fit: young woman, fast, casual, TikTok UGC)

I measured Higgsfield presets from their preview files (Whisper words per voiced second, plus median pitch). I could not listen to them, so the owner should audition before choosing.

| Voice | Library / ID | Description | Measured |
|---|---|---|---|
| **Emily** | Higgsfield preset `6b3e3642-f7b7-4cb8-9688-51e233c4b92f` | Preview: "your classic American girl, bubbly, fun, and totally real… your UGC bestie… skincare hauls" | 3.7 w/s, 213 Hz |
| **Chloe** | Higgsfield preset `e9cfbbf0-4476-46be-b396-596eb774b165` | Preview: "Oh my gosh, hi… literally so obsessed… major energy… viral post". The most hyped; may skew too young or salesy | 4.1 w/s, 276 Hz |
| **Gia** | Higgsfield preset `530df032-c311-483b-a750-cb3c9e1bcdfd` | Preview: "scripts that need to feel lived in… natural city rhythm, warm, a little bit chatty, 100% real". Closest to the 27-year-old persona | 3.6 w/s, 194 Hz |
| **Hayley – Natural TikTok & UGC** | ElevenLabs library `gpmRbxMkenLwiGmvYotk` | "Relatable, upbeat, energetic content creator for product reviews, TikTok shop videos… promo ads"; young, American | — |
| **Lauren B – Gen-Z Influencer, Feels Real** | ElevenLabs library `EQymf553LnGArWPRBol1` | "Casual, unfiltered, and instantly relatable… spontaneous and effortless", American creator energy | — |
| Kristen – upbeat social media influencer | ElevenLabs library `XZUXLIpE3dqJ9aCZUj2R` | "Energetic, lively… TikTok narration… fast-paced media"; young, American | — |
| Jade | ElevenLabs library `g7LVvkPWALzPxOQbF6OE` | "High-energy… rapid-fire delivery and a playful, erratic cadence for Gen-Z marketing". Possibly too chaotic | — |

Notes on IDs:

- The Higgsfield preset IDs work directly with `voice_change`, `seed_audio`, `elevenlabs_v4` and `text2speech_v2`.
- The ElevenLabs library IDs work on the ElevenLabs creative connector (TTS and voice changer).
- To use an ElevenLabs voice inside Higgsfield, it would need to become a Higgsfield voice element (`create_voice`). That was not checked or priced.
- Runway's `search_voices` returned nothing for this query. Its preset list includes Lara (current narrator, "young, confident, influencer") and Kylie (Australian).

### Mild time compression (video and audio together)

The rule "never plan a sped-up voice" (lessons) guards against speeding up the voice alone, which breaks lip sync and sounds chipmunky. Compressing the whole clip uniformly is different:

- `setpts=PTS/1.10` on video and `atempo=1.10` on audio scale both by the same factor, so **sync is preserved exactly**. ffmpeg's `atempo` keeps pitch. This build has `atempo` but no `rubberband`.
- **Natural range:** 1.05–1.12×. Speech already near 3.5 w/s with the pauses cut would land at ≈3.9 w/s at 1.12×, which is the top of natural. Above about 1.15×, breathy voices start to smear and gestures look twitchy.
- Re-time the video to 30 fps after `setpts` (`-r 30`) so motion stays smooth.
- **Cutting pauses does more than speed.** Removing the 33–47% silence takes the three clips from 42 s to about 27 s. Adding 1.08× on top gives about 25 s. So: cut pauses first, then use at most 1.08–1.10×.

---

## 3. Fast-paced editing for TikTok/Reels ads (2026)

What the sources support:

- **TikTok's own guidance:** 9:16 at ≥720p, sound on, hook in the first 6 s, core message in the first 3 s, captions or text at 5–10 words per second, and transitions, stickers and graphics to hold attention ([TikTok Ads help: creative best practices](https://ads.tiktok.com/help/article/creative-best-practices?lang=en)).
- **Scene change every 2–3 s** for TikTok and Reels. Cut intros, pauses and dead air. Drop in 1–3 s product B-roll throughout, with a slow zoom on stills. Meta's figure: 65% of people who watch 3 s keep watching for 10 more ([Influee](https://influee.co/gb/blog/raw-ugc-to-ads)).
- **Cut every pause, restart and filler word.** Jump cuts between sentences are expected on TikTok and Shorts. Punch in on key lines. Use B-roll for 2–4 s at a time. Captions should be big, 1–2 lines, current word emphasised, in the lower-middle. Use subtle SFX (a whoosh on transitions, a tick on on-screen points) and keep music well under the voice ([Opus talking-head guide](https://www.opus.pro/blog/talking-head-videos-guide), [1of10 jump cuts](https://1of10.com/blog/what-is-a-jump-cut/), [Tella punch-in](https://www.tella.com/help/tips/punch-in-zoom-in-on-your-camera)).
- **"Perceived pacing" matters more than a fixed number.** TikTok measures completion, rewatch and early retention, not edit quality ([Stackmatix 2026](https://www.stackmatix.com/blog/tiktok-ad-creative-best-practices-2026), [nemovideo](https://www.nemovideo.com/blog/how-to-edit-tiktok-videos)).
- **Music and SFX licensing for ads:** TikTok's Commercial Music Library is the only TikTok-side source cleared for business use, and only on TikTok ([TikTok CML help](https://ads.tiktok.com/resources/help/article/commercial-music-library?lang=en)). For Reels and Facebook, use a library whose licence explicitly covers paid ads (e.g. Epidemic Sound commercial plans; check each licence), or keep generating SFX ourselves. ElevenLabs SFX and music and our synthesised ffmpeg SFX are already in the pipeline.
- **No primary source gives a validated cut interval**, zoom % or SFX density. The numbers in the spec below are practitioner defaults to A/B test.

### Editing spec for the assembler (ffmpeg)

Pause removal (do this first):

- Use Whisper word timestamps. Cut any gap over **0.15 s** between words down to **0.06–0.10 s**, except one deliberate beat of ≤0.3 s before the reveal.
- Cut on frame boundaries, with a 10 ms audio crossfade (`acrossfade=d=0.01`).
- Target **≥3.0 spoken w/s** overall.

Visual rhythm:

- **Maximum shot length is 2.5 s.** In the first 3 s, change something every 1.0–1.5 s.
- Every jump cut inside one talking clip alternates the framing between **100% and 112–118%** (`crop` + `scale` punch-in, centred on the face) so the jump reads as deliberate.
- For emphasis words, add one fast punch to 125–130% over 4 frames (`zoompan` or a cropped scale).
- Stills and B-roll get a slow push of **+6–10% over the shot** (Ken Burns via `zoompan`). Never hold a still face while the voice is speaking (from the last review).
- B-roll (tray, patch macro, K3 sleep crease, product packshot) is 1–2.5 s per insert. Use about one insert per 5–6 s of talking, and put inserts over weak lip-sync words.

Captions:

- Burn in word-by-word or 2–3-word chunks, timed to Whisper word timestamps.
- Bold sans (e.g. Montserrat ExtraBold / Inter Black) at 64–80 px on 1080 wide, white with a 6–8 px black stroke. The current word is highlighted in the brand accent.
- Place the centre around y ≈ 1150–1250, inside the existing safe band of y 269–1248.
- This ffmpeg build has **no `drawtext` or `subtitles` (no libass/freetype)**. Render caption PNGs (Playwright or PIL) and `overlay` them with `enable='between(t,a,b)'`, or install an ffmpeg with libass.
- Keep text at ≤10 words per second on screen, per TikTok guidance.

Pop-ups (pattern interrupts):

- One every **3–5 s**: an emoji or sticker ("😩", "🤯"), keyword pills ("FROWN LINES"), the reply bubble, a red X / green check, a product cut-out, or a mini screenshot.
- Each one pops in with a **scale 0 → 110% → 100% over 6 frames**, holds 0.8–1.5 s, and exits by hard cut.
- Plan at least one bigger interrupt per 8–10 s: a split screen, a hard colour flash, a freeze-frame with a record scratch, or a "wait…" beat.

SFX:

- About **one per visual event**, which averages 0.5–1 per second in the first 5 s and then about 1 every 2–3 s.
- Whoosh on transitions and punch-ins (150–300 ms). Pop or bubble on sticker and pill entries (≤100 ms). Ding on proof or price. Short riser (0.8–1.5 s) into the reveal and the CTA. Camera shutter or record scratch for interrupts.
- Mix SFX at −18 to −22 LUFS short-term, so they sit under the voice. Never place one on top of a stressed word.

Music:

- Upbeat bed at 100–125 BPM from a commercial-cleared source, ducked about 12–15 dB under speech (sidechain or volume automation).
- Land cuts on beats where you can. Drop the music out for a 0.3 s "silence hit" before the reveal.

Global and QA:

- Optional uniform 1.05–1.10× on talking segments (video `setpts` plus audio `atempo`, same factor).
- Master to −16 LUFS / −1.5 dBTP as now.
- Contact sheet at 2 fps plus a check that **no shot is over 2.5 s and no gap between words is over 0.3 s**. Fail assembly otherwise.

Length:

- With these rules the same 88-word script runs about 27–30 s, which moves this TOF video toward the bottom of its 30–50 s range.
- Write TOF scripts at **95–140 words** (3 w/s × 32–45 s), not the current 70.

---

## Recommendations for the pipeline

1. **Config changes:**
   - `video.words_per_second: 2.3` → **3.0**, and plan scripts at 3 w/s of on-screen time.
   - Add `editing:` keys: `max_shot_seconds: 2.5`, `max_word_gap_seconds: 0.10`, `punch_in_pct: [112, 118]`, `popup_every_seconds: [3, 5]`, `captions: word_by_word`, `speed_factor_max: 1.10`.
2. **Talking clips:** one sentence per clip, 4–6 s, ≤15 words, medium close-up with the face ≥45% of frame width, head still while speaking, and the energetic voice block from §2a. Remove "soft / breathy / late at night" from all voice text.
3. **Run the lip-sync bake-off once** (≈40–60 credits, owner approval needed): Intone vs Wan 2.7 audio-ref vs Veo 3.1 fast vs Kling-with-new-rules, on the same line and still. Then set `audio_talking_head` to the winner. Audio-first, with a TTS line in a chosen UGC voice, needs the owner to amend the "same model, same clip" rule.
4. **Voice:** the owner auditions Emily, Gia and Chloe (Higgsfield presets) and Hayley and Lauren B (ElevenLabs library). Save the chosen one as `pipeline/config.yaml → voice_ugc` and use it for every talking video.
5. **This video, free:** re-cut with pause removal, punch-in jump cuts, B-roll over the weak-sync words, word-by-word captions, stickers and SFX per §3. If the owner wants a different timbre now, Higgsfield `voice_change` costs **≈5 credits** for all 42 s (timing kept, energy unchanged). A full re-voice with re-lip-sync costs ≈90+ credits and is over this run's cap.
6. **Reviewer checks:**
   - Add "bilabial closures visible on m/b/p in the hook line" and "no still face under live speech" to checklist B.
   - Add "max shot 2.5 s, max word gap 0.3 s, captions present" to checklist C.

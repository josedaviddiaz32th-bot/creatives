# Format — run 2026-11-07-1740 — "30s mirror moment"

Stage 2 (trend-scout). Format only: no script, people, brand or claims from any
reference ad are copied. Reads: `brief.md`, `pipeline/config.yaml`,
`docs/lessons-learned.md`, `runs/history.json` (`[]`, first run, so no recent
formats to avoid).

## Research (AdWhispr, read-only, 2026-11-07)

| Search | Result |
|---|---|
| `search_brands` "Frownies", "SiO Beauty", "Peace Out", "wrinkle patches" | Not tracked in AdWhispr (no add_brand done, per instructions) |
| `research_tiktok_ads` "SiO Beauty", "Frownies" | No advertiser in TikTok's EU ad library |
| `research_tiktok_ads` "Medicube" | Advertiser found, 0 ads in last 90 days |
| `get_brand_ads` Medicube (adjacent: anti-aging skincare, K-beauty), talking head, video, by longevity | Longest-running active ads are **UGC talking head** (379 and 358 days running, plus 132 and 116 days) |
| `search_ads` Medicube "wrinkle patch overnight forehead lines night routine" | Active creator ads for wrinkle care: **night routine → sealed overnight → satisfying morning peel-off / reveal** (29 days), wrinkle-care talking-head routines (27–48 days), under-eye patch routine (33 days) |

Direct wrinkle-patch competitors have no coverage in these tools, so the format
comes from the closest adjacent category (overnight anti-wrinkle skincare),
where the long-running winners are phone-shot UGC talking heads and the
fresh wrinkle-care ads use a night-on / morning-off routine arc. That arc also
matches the lessons' "winning format" note (a woman applying and peeling on
camera, §12) and the demo beat (§3: on at night, off in the morning).

## Chosen format: Night-to-morning bedside confession (talking head, split by a silent routine beat)

- **Type:** talking-head confession that becomes a problem-then-routine: she
  talks to her phone at night (bare face), a short silent beat of the patch
  going on and her wearing it, then she talks again the next morning (bare
  face again, patches off).
- **Hook pattern:** a first-person "has this happened to you too?" question
  about a private moment of noticing her own face (the brief's
  not-recognising-yourself moment), said straight to camera with motion in
  frame one (she is already mid-gesture or settling onto the bed, phone
  handheld). On-screen text ≤8 words echoes the question. No static title card.
- **Pacing:** question in 0–5s; problem (photos, creams, not wanting needles)
  through ~13s; patch sheet visible on the nightstand from frame one so the
  product is on screen early without a verbal pivot; the patch enters the story
  at ~13s as "what I do now before bed". Three clips, hard cuts only, one action
  per shot:
  1. ~13s night, bedside selfie, bare face, she talks (hook + problem + turn).
  2. ~6s night, silent: presses the forehead piece on from the centre outward,
     then lies back wearing the set, calm, **lips closed, no smile**. Sound =
     room tone + soft backing-film/press sound; on-screen text carries the
     mechanism (≤8 words).
  3. ~13s morning, same bedroom, window daylight, patches already off and held
     or on the sheet (no peel animation, avoids the hardest shot, §6), bare face,
     she talks: how it felt/looks ("rested", "by morning" language only), the
     no-needles point, subtle CTA. CTA also gets its own full-screen text beat
     in assembly.
  Total ≈32s.
- **Shot style:** front-camera selfie, handheld, slightly above eye level,
  30–35 cm, phone framing, unretouched, warm bedside lamp at night / window
  daylight in the morning. Bedroom, sitting on the bed. **No mirror in frame**
  (the "mirror" is only said, never shown).
- **Who speaks:** the on-camera woman, in clips 1 and 3 only, with Kling 3.0
  **native voice** (same voice description word for word in both prompts).
  Clip 2 is silent (no ElevenLabs needed). Talking always happens bare-faced,
  so the owner rule (patches on = lips closed, no smiling) is never in tension.
- **Why it fits this persona:** she is mid-30s, already has a skincare routine
  and has quietly stopped taking selfies, so a candid phone-to-face confession
  at bedtime reads as content, not an ad (lessons §3, real-looking beats
  polished). The night-on / morning-after arc shows "one more step in my night
  routine" (complement to skincare, nothing under the skin) and lands belief 1
  ("visibly smoother-looking by morning") without a before/after claim. It is
  the same shape as the long-running UGC skincare winners above.

## Production fit (for storyboarder / prompt-engineer)

- Kling 3.0 Pro, sound on ≈2.5 credits/s → 32s ≈ 80 credits in 3 clips
  (13 + 6 + 13s), leaving ~15 for retries + a few credits of stills, inside
  `budget.max_credits_per_video` (100). Std mode (~2/s) is the fallback.
- Keyframes: night bare-face start (clip 1), night wearing end frame (clip 2,
  patches fully on), morning bare-face start (clip 3). Clip 2's start frame is
  bare-faced with the forehead piece in her fingers (apply and wear are one
  short motion; if it fails, cut to wearing only).
- ~30 spoken words per talking clip at 2.3 words/s (~60 words total).

## Reference ads (format only)

1. Medicube, UGC talking head, active 379 days:
   https://2hjftxrjnsl9fram.public.blob.vercel-storage.com/ads/76e48eb9-dde5-48a5-8263-c82f919deb8f/8bc23e1b-8e77-400f-aea7-4924179d56b5/video
2. Medicube creator ad, night routine sealed overnight → morning peel-off reveal, active 29 days:
   https://2hjftxrjnsl9fram.public.blob.vercel-storage.com/ads/76e48eb9-dde5-48a5-8263-c82f919deb8f/30d36132-fd9e-4b98-941d-e6a26578bea1/video
3. Medicube creator ad, talking-head wrinkle-care routine (first fine lines), active 27 days:
   https://2hjftxrjnsl9fram.public.blob.vercel-storage.com/ads/76e48eb9-dde5-48a5-8263-c82f919deb8f/b2d1fc12-0375-4a34-b616-80692dc14c93/video

---
name: creative-scout
description: Stage 2. Finds a winning creative (any product category) in the slot's format, breaks down why it works, saves the breakdown to the swipe library, and maps it onto this run's persona and funnel stage. Writes format.md. Copies structure, never content.
---

You find what's already working out there and turn it into a plan for our
video. The source ad can be from any category (skincare, supplements,
software, food); what matters is that it's winning and its structure fits
this slot.

## 1. Read first
- `brief.md` (the slot: persona, funnel stage, awareness, format, belief).
- `learning/playbook.md`: what's WINNING and what's RETIRED for us. Never
  base a video on a RETIRED format, hook type or presenter style.
- `learning/swipe-index.json`: breakdowns already in the library.
- `docs/lessons-learned.md` section 3 (adapting a reference post).

## 2. Find a winning creative
Search for **the slot's format** first, then widen to the slot's funnel
stage. Use the ad-research tools connected to this session:
- **AdWhispr** (Meta Ad Library and TikTok ads): `search_ads`,
  `research_tiktok_ads`, `get_brand_ads` sorted by longevity.
- **Gethookd** (call `get_user_profile` first, as its instructions require):
  `search_ads`, `get_top_ads`, `get_ad_hooks`, `get_creative_breakdown`,
  `transcribe_ad`.

**What counts as winning** (record which signal you used):
- active 30+ days (advertisers don't keep paying for losers), best signal;
- many live variations of the same concept;
- top-ranked by the tool (top ads, top hooks), or unusually high engagement.

Pick 1–3 candidates. Prefer ones not already in the swipe index. You may
reuse a library breakdown instead of searching when it fits the slot and
its `outcome` in the index is WIN; add at least one new breakdown to the
library every 3 runs anyway, so the library keeps growing.

## 3. Break it down
Watch or transcribe it (`transcribe_ad`, `get_creative_breakdown`, or
frames). For the one you pick, fill in:

| Element | What they did | Why it may persuade |
|---------|---------------|---------------------|
| Hook: visual (frame 1) | | |
| Hook: words / on-screen text | | |
| Hook: sound | | |
| Awareness level it speaks to | | |
| Structure, beat by beat (timestamps) | | |
| Open loops / pattern breaks | | |
| Proof (demo, before/after, authority, social proof) | | |
| Presenter (peer, authority look, voiceover, none) | | |
| Pacing (cuts per 10s, length) | | |
| Product reveal timing | | |
| Offer and CTA | | |

Then, in one or two sentences: **the core mechanism** that makes it work
(e.g. "a confession that makes the viewer feel caught, then a cheap fix").

## 4. Map it onto our slot
| Their element | Our persona's version | Funnel stage job it serves |
|---------------|-----------------------|----------------------------|

Keep their structure, pacing, proof type and reveal timing. Replace
everything else: our persona's moment and words (`brief.md`), our product,
our claims. **Never copy their script, faces, voice, music or brand.**
If the mechanism doesn't fit the slot's funnel stage, say so and pick
another creative.

## 5. Save to the library
- Write `learning/swipe-file/<YYYY-MM-DD>-<advertiser>-<short-slug>.md`
  with: source link(s), advertiser, category, platform, winning signal,
  the breakdown table, the core mechanism, funnel stage, format.
- Append an entry to `learning/swipe-index.json`:
  `{"id", "file", "advertiser", "category", "format", "funnel", "presenter",
  "hook_type", "mechanism", "winning_signal", "used_in": ["<run folder>"],
  "outcome": "untested"}`.
  The results-analyst later sets `outcome` to win / loss / mixed from our
  own results.

## 6. Write `format.md`
The chosen creative's breakdown, the core mechanism, the mapping table, the
swipe-file path, and the resulting plan: type, hook pattern, pacing, shot
style, who speaks, product timing, length (from `video.seconds_by_stage`).

No format may appear more than twice in the test week
(`docs/creative-strategy.md` section 4). If no research tool works, say so
and adapt the best-fitting breakdown already in the library; if the library
is empty, use a format from `docs/lessons-learned.md`.

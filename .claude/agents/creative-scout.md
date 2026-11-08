---
name: creative-scout
description: Stage 2. Finds a winning creative (any product category) in the slot's format, breaks down why it works, saves the breakdown to the swipe library, and maps it onto this run's persona and funnel stage. Writes format.md. Copies structure, never content.
---
**Owner calibration:** read `learning/owner-feedback.md` first. It overrides your defaults on taste, severity and voice, and lessons-learned still wins on claims and product facts.


**The persona:** work from the full verbatim persona section in `brief.md`
(age, description, key concern, behaviour, emotional trigger, every quote),
not from a summary. Her exact words and details belong in the video.

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
stage. Use whichever of these sources this session has (say which you used):

- **Meta Ad Library in Chrome** (Claude in Chrome, the owner's Facebook
  login): `facebook.com/ads/library/?active_status=active&ad_type=all&country=US&media_type=video&search_type=keyword_unordered&q=<keyword>`.
  It sorts by **total impressions** by default and shows each ad's start
  date (longevity), whether it runs through a creator's page (whitelisting)
  and how many versions it has. Search category words ("wrinkle patches",
  "forehead lines", "under eye patches") and adjacent ones for the slot's
  problem ("look tired", "med spa", "sleep wrinkles"). Read with
  `get_page_text`; open "See ad details" for the video. Load the Chrome
  tools in one ToolSearch call and close every tab you open.
- **TikTok Creative Center → Top Ads** in Chrome
  (`ads.tiktok.com/business/creativecenter/inspiration/topads/pc/en`):
  likes, CTR percentile and budget per ad, filterable by region, industry
  (beauty & personal care) and objective. Filters must be set in the page
  (URL keywords don't apply); close the promo popup first. Its likes and
  CTR are **engagement signals**, the best TOF reference.
- **Organic TikTok / Instagram search in Chrome** for the slot's problem,
  sorted by most liked: TOF formats that earn attention without paying.
- **AdWhispr** (Meta and TikTok ads via API): `search_ads`,
  `research_tiktok_ads`, `get_brand_ads` sorted by longevity. Works in
  cloud sessions without a browser.
- **Gethookd** (call `get_user_profile` first): `search_ads`, `get_top_ads`,
  `get_top_hooks`, `get_creative_breakdown`, `transcribe_ad`. As of Nov 7,
  2026 the workspace has no MCP access; skip it if it still says so.
- **Higgsfield `tiktok_music_trending`** for a current sound when the
  format uses music.

Chrome sources need the owner's Mac with Chrome open (local sessions). In a
cloud session, use AdWhispr and the swipe library.

**What counts as winning** (record which signal you used):
- **MOF/BOF:** active 30+ days (advertisers don't keep paying for losers);
  many live variations or creator versions of the same concept; top
  impressions in the Ad Library.
- **TOF:** engagement first: Creative Center likes and CTR, organic videos
  with unusually high likes, shares and comments for the account's size.
  A long-running ad is a bonus, not the main signal.

For **TOF** slots, also pull the strongest hooks around (AdWhispr
long-running ads; Gethookd `get_top_hooks` when it has access) and note
the hook patterns in `format.md` for the scriptwriter.

Pick 1–3 candidates. Prefer ones not already in the swipe index. You may
reuse a library breakdown instead of searching when it fits the slot and
its `outcome` in the index is WIN; add at least one new breakdown to the
library every 3 runs anyway, so the library keeps growing.

## 3. Break it down
Watch it, don't guess: transcribe it (`transcribe_ad`,
`get_creative_breakdown`), or in a local session download the video into a
new empty folder in the scratchpad, transcribe it with Whisper
(`whisper-cli -m ~/.cache/whisper/ggml-small.en.bin`, or `ggml-small.bin`
for other languages) and pull frames with ffmpeg. If you couldn't watch it,
say so in the breakdown. For the one you pick, fill in:

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

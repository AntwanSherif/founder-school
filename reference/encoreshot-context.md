# EncoreShot — context for founder-school lessons

This is a compressed snapshot of the product, so lessons can be grounded without re-grilling. Source of truth lives in the repo (`/Users/antwan/files/side-projects/insta-super-edit/`): `CONTEXT.md`, `docs/product/{positioning,gtm,brand,pricing-brief}.md`, `feature-roadmap.md`. Re-sync this file if the product strategy moves.

## What it is
AI-powered photo/video **culling** tool for **concert/event photographers**. Core loop: drop a card-dump of raw frames → AI **scores** each asset (0–100, genre-aware) → human **keeps/cuts** in a fast review grid → **exports** Instagram-format files (9:16 / 1:1 / 4:5) — *before the crowd leaves the venue*. Hosted web app. Bun/Hono/SQLite backend, React/Vite frontend.

## The core bet (differentiator / moat)
Nobody owns the gap between culling tools (export *to* Lightroom) and social tools (assume a finished image). EncoreShot does **watch/upload → AI scoring → one-click review → Instagram export** in one tool, **for the concert niche specifically**. Concert photography breaks generic quality models (motion blur is style, colored stage light is intentional, grain is aesthetic) → genre-aware scoring is the moat. FFmpeg-based, so video + audio (song ID from setlist) are possible where competitors structurally can't.

## Two-persona model (critical for pricing/GTM)
| | **Hobbyist** (MVP wedge) | **Pro** (destination) |
|---|---|---|
| Files/show | 20–80, video-dominant | 300–800, photo-dominant |
| Willingness to pay | $0–5/mo or one-time | $12–25/mo |
| **AI cost / user / mo** | **~$0.15** | **~$1.00** |
| Acquisition | concerts, fan groups, Discord | press, SEO, conferences |

Strategy = **Trojan Horse**: enter via hobbyist "fan with a phone" for ~9–18 months, then serve the Pro. Brand stays Pro-aspirational so it ages up.

## AI economics (the pricing puzzle Antwan flagged)
Scoring cost is variable per asset: **video duration, resolution, fps, and model choice** drive the cost of each LLM call. Providers: Gemini Flash (cloud) + Qwen2.5-VL, A/B in parallel; **tiered video scoring** (cheap FFmpeg pre-filter rejects garbage before spending an LLM call). Target infra <$25/mo at 25 users. **Margins are not the binding constraint at hobbyist scale (AI <$1/user/mo) — positioning is.**

## Go-to-market (already scoped, zero-CAC)
In-person **concert seeding** (be a fan first, hand a QR **voucher** sticker) → fan-group seeding (subreddits/Discord/Telegram) → post-show empathy reach → **Founding Crew** private chat (first 25) → build-in-public show diary. Vouchers are single-use, time-limited, cohort-tagged for attribution. Landing page: `encoreshot.com/early`, mobile-first, fan-to-fan voice.

## Open pricing questions (live, undecided)
Free-tier gate (file/export/session/time?), hobbyist-friendly price (re-derive from old $12/mo Pro number; WTP $0–5/mo), one-time vs subscription vs lifetime "Founding" license, what a redeemed voucher unlocks, referrer reward shape, anti-fraud floor. These are exactly the applied questions future advisor-mode lessons should tackle.

## Positioning boundaries (what it is NOT)
Not a Lightroom companion. Not a montage editor (CapCut handles that). Not horizontal (niche-locked to live music by choice). Not multi-user yet.

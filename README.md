# Oleg's Pravda SEO team (Grok Bot)

Seven Grok bots that run the parts of Pravda SEO no one runs today. The **Client Desk** catches every client win and drafts the referral ask Oleg wanted after each one. The **Maps Desk** watches every client's Google listing and writes his Google Business Profile know-how into a private playbook. The **Authority Studio** turns his 19 years, his Forbes articles and his testimonials into a proof page, article drafts and stronger VSL hooks. The **Call Desk** works on his five-year idea, emergency-dental and pay-per-call, the honest way. The **Channel Scout** finds new channels every month. The **Profit Desk** shows whether he's "covering this and making money on top". The **Chief** keeps his notes, his Dream Map and his ideas, and sends him one message a week with one action in it.

His two **Hermes agents in Telegram** (the Growth Manager and the Affiliate Manager) keep the partner program. This team never writes where they write. See [`PROJECT_CHARTER.md`](PROJECT_CHARTER.md) §5.

**Platform:** xAI Grok Bot (x.ai/bot), one business account. **Start here:** [`START-HERE.md`](START-HERE.md).

## How to start

1. Justin's team shares this private repo with Oleg's Grok Bot, or sends him the zip, plus the private `CLIENT-CONTEXT.md`, `DREAM-MAP.md` and the master `ASKS.md`.
2. Oleg creates a new Grok Bot in the Grok app (desktop), attaches those three files and sends it: "Build my team from https://github.com/jbellsolutions/pravda-seo-grokbot-team. Follow START-HERE.md. This is my business account."
3. The bot walks him through ten short steps. Justin's team can sit with him on a screen share. Nothing runs or sends until he says yes.

## The team

| Bot | What it does for Oleg | Starts at |
|---|---|---|
| [Chief](agents/01-chief.md) | Monday "Pravda week" (one action), the Dream Map, notes on record, call notes, task cards for his developer | M0 |
| [Client Desk](agents/02-client-desk.md) | Client wins, referral asks after wins, price review and upgrades, testimonial requests | M3 |
| [Maps Desk](agents/05-maps-desk.md) | Weekly check of every client listing, rank reports filed, private GBP playbook | M3 |
| [Authority Studio](agents/04-authority-studio.md) | Proof library and proof page, Forbes drafts, VSL hooks, talk outlines | M4 |
| [Call Desk](agents/03-call-desk.md) | Emergency dental and pay-per-call: economics, buyers, drafts, pilot | M5 |
| [Channel Scout](agents/06-channel-scout.md) | Monthly memo of new channels and partner pools | M6 |
| [Profit Desk](agents/07-profit-desk.md) | Monthly money view by channel; alerts when a bill jumps | M6 |
| [Partner Engine](agents/90-partner-engine.md) | Reserved: only if Oleg moves the partner program from Telegram to Grok | M8 |
| [Deal Desk](agents/91-deal-desk.md) | Reserved: proposals and onboarding for direct clients (phase two) | M9 |

## What's inside

| Path | What |
|---|---|
| [`START-HERE.md`](START-HERE.md) | The install: the bot follows it top to bottom |
| [`PROJECT_CHARTER.md`](PROJECT_CHARTER.md) | Why, objectives, the team, rules, records and their writers, milestones |
| `agents/` | One charter per bot (seven active, two reserved) |
| `routines/` | 12 scheduled jobs. All are created paused |
| `skills/` | How each job is done. Every bot loads [`pravda-context`](skills/pravda-context/SKILL.md) first |
| `projects/` | Bigger builds for later: the [pay-per-call pilot](projects/pay-per-call-pilot/SPEC.md) and the [proof page](projects/proof-page/SPEC.md) |
| [`policies/APPROVALS.md`](policies/APPROVALS.md) | What each bot may do alone, what it asks first, what it never does |
| [`policies/DATA.md`](policies/DATA.md) | What's private and where it lives |
| [`OPEN_QUESTIONS.md`](OPEN_QUESTIONS.md) | What only Oleg can answer, and what Justin's team owes |
| [`docs/BUILD-RECORD.md`](docs/BUILD-RECORD.md) | What's specified, built and actually running |

Built by Justin's team with the client-build system (2026-10-27).

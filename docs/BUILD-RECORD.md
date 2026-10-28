# Build record

This record keeps what's specified, what's built and what's actually running separate, and honest. Justin's team updates this file; the bots never do. The Chief keeps the live list in `/workspace/pravda-team/context/team-registry.md`.

**Where it stands (2026-10-27): a specification package.** Everything below exists as files in this repo. Nothing is set up, connected or switched on for Oleg until his Grok Bot follows `START-HERE.md` and reads back what it created. The repo isn't on GitHub yet: creating it and pushing need Justin's yes.

## Status by piece

- **Specified:** the job is written down.
- **Built in repo:** the file the bot uses exists here.
- **Active:** it's running on Oleg's account and has been read back.

| Piece | Specified | Built in repo | Active |
|---|---|---|---|
| Project charter, approvals, data rules | Yes | `PROJECT_CHARTER.md`, `policies/` | Not yet |
| Install | Yes | `START-HERE.md` (Steps 0–10) | Not yet |
| Shared business context and the Hermes boundary | Yes | `skills/pravda-context/` | Not yet |
| Chief (lead) | Yes | `agents/01-chief.md`; skills `getting-started`, `ask-ledger`, `dream-map`, `pravda-week`, `records-desk`, `call-notes`, `developer-task-card`; routines `chief-pravda-week`, `chief-records-sweep` | Not yet |
| Client Desk | Yes | `agents/02-client-desk.md`; skills `client-roster`, `client-pulse`, `client-referral-ask`, `price-review`, `testimonial-request`; routines `client-monthly-pulse`, `client-win-asks`, `client-price-review` | Not yet |
| Call Desk | Yes | `agents/03-call-desk.md`; skills `ppc-market-map`, `ppc-buyer-outreach`, `ppc-pilot`; routine `call-desk-weekly`; `projects/pay-per-call-pilot/SPEC.md` | Not yet |
| Authority Studio | Yes | `agents/04-authority-studio.md`; skills `proof-library`, `forbes-pipeline`, `vsl-hooks`, `talk-builder`; routine `authority-weekly`; `projects/proof-page/SPEC.md` | Not yet |
| Maps Desk | Yes | `agents/05-maps-desk.md`; skills `listing-watch`, `rank-intake`, `gbp-playbook`; routines `maps-listing-check`, `maps-rank-intake` | Not yet |
| Channel Scout | Yes | `agents/06-channel-scout.md`; skills `channel-research`, `competitor-teardown`; routine `scout-monthly` | Not yet |
| Profit Desk | Yes | `agents/07-profit-desk.md`; skills `money-snapshot`, `spend-watch`; routines `profit-monthly`, `profit-spend-watch` | Not yet |
| Partner Engine (reserved, M8) | Role, mission, trigger | `agents/90-partner-engine.md` | No: only after a move Oleg chooses |
| Deal Desk (reserved, M9) | Role, mission, trigger | `agents/91-deal-desk.md` | No |

## Sources

| Source | Date | Digest |
|---|---|---|
| Sales / discovery call | 2026-08-06 | `Oleg/source/digests/2026-08-06.md` |
| Affiliate-program scoping call | 2026-09-09 | `Oleg/source/digests/2026-09-09.md` |
| Onboarding: offer and target list | 2026-09-15 | `Oleg/source/digests/2026-09-15.md` |
| Access check-in before his trip | 2026-09-18 | `Oleg/source/digests/2026-09-18.md` |
| Implementation walkthrough | 2026-10-05 | `Oleg/source/digests/2026-10-05.md` |
| Jam call with his developer | 2026-10-13 | `Oleg/source/digests/2026-10-13.md` |
| A2P call | 2026-10-21 | `Oleg/source/digests/2026-10-21.md` |
| Shared Slack channel | 2026-09-15 – 2026-10-27 | `Oleg/source/slack/` |

These paths are in Justin's client folder, not in this repo. Transcripts never enter the repo.

## Platform facts this build relies on

| Fact | Status |
|---|---|
| Every bot on one account shares one computer, its files and its logins | Verified in docs |
| No import API: the client pastes the repo link into a new bot, and START-HERE is the installer | Verified in docs |
| Routines run in the cloud in the bot's time zone | Verified in docs |
| 50 routines per bot; schedules at least 5 minutes apart; 20 run records kept | Verified in docs |
| **Test** on a routine does real work | Verified in docs |
| Auto-review Custom Rules; Ask first wins a conflict | Verified in docs |
| Approval, secret and sign-in requests don't show in group chats; Test, Details and Auto-review are on desktop | Verified in docs |
| Approval prompts started by a routine expire | Unverified. Routines never wait on approval |
| Secure secret cards reach the shell as environment variables | Seen live, not in docs. Fallback: hidden terminal prompt |
| Routine webhook triggers | Seen live, not in docs. Weekly sweeps until M10 |
| GHL Private Integrations allow a view-only token | Unverified on Oleg's sub-account. START-HERE has Justin's team do it on a screen share if the menu differs |
| Grok's Gmail connector scope (read vs send) | Unverified. The Ask-first rules and the charters keep every send behind Oleg's yes |

## Review findings

| Finding | What was done |
|---|---|
| *Independent review, 2026-10-27: a fresh opus subagent read the transcripts, digests and Slack summary against the package. It reported 13 findings; each was checked against the files and sources before fixing.* | |
| 1. High: both systems would ask Oleg's clients for referrals (the Hermes monthly email's soft line and the Grok per-win ask) | Only the Client Desk drafts personal asks; its 90-day check now reads Gmail sent mail and GHL and ignores the newsletter's general line. START-HERE Step 7 says where the two meet. Whether Oleg wants both is owed by Justin's team (OPEN_QUESTIONS owed table). The Hermes repo was not edited |
| 2. High: no step built the client roster, so the client and listing routines would run empty and still pass the test | New START-HERE Step 6b builds `data/clients.md` and `data/listings.md`; Step 1 creates every `requests/to-*` folder and `data/rankings/inbox/`; `NO_CLIENT_SOURCE` now fails the Step 8 test; the pulse reads `requests/to-client-desk/` |
| 3. Medium-high: "his Oct 21 question was answered no" was invented (Justin said "I think so") | Rewritten in pravda-context, Maps Desk and gbp-playbook to say what was said; a clear answer is owed by Justin's team |
| 4. Medium: an "Emergency" second profile at the practice's address would have passed the legitimacy check | Added "no second profile at the same address, no keywords in the name" to pravda-context, the pilot spec, ppc-pilot and APPROVALS; renamed the listing-watch example |
| 5. Medium: a yes relayed by Justin's team counted; no rule stopped deleting or labelling email | Relayed yeses removed; Ask-first rules added for email delete/archive/label/move and calendar changes |
| 6. Medium: every request to the Chief went to Justin's team, client names included | `For:` line on every request (charter §6 rule 14); the Chief routes by it and keeps client names out of `for-justins-team.md` |
| 7. Medium: four routines messaged Oleg on other weekdays | Drafts now wait for the Monday digest (charter §6 rule 13) across 3 charters, 7 skills and 3 routines; only listing, bill and reply alerts come between |
| 8. Medium: setup stalled until Oleg deleted Slack messages he can't delete | Step 5 gates only on the key and passwords being changed; deletions and the OutFlo login are owed by Justin's team |
| 9. Low-medium: two figures for the 10× check; Call Desk couldn't tell a buyer from a partner prospect | Profit Desk never reports either guarantee; Call Desk looks buyers up in GHL read-only and hands partner matches to the Chief |
| 10. Low: install and record gaps | ASKS.md added to the attach lists; listing URLs come from `requests/to-maps-desk/`; charter §7 lists the missing records; receivers keep a `taken.md` instead of editing handoffs (charter §6 rule 15); the GBP interview starts at M4 on Oleg's yes; the two unusual schedules moved to day-of-month form |
| 11. Low: three misattributed quotes | Fixed in client-referral-ask, Client Desk and Channel Scout |
| 12. Low: "one password" said more than the source | "passwords" throughout |
| 13. Low: two asks missing; no question about urgent texts | Ledger rows 78 (VSL with a presentation) and 79 (residual-income partner hook, owed to the Hermes copy); OPEN_QUESTIONS #17 |

## Open items and who owns them

| Item | Owner | Next action |
|---|---|---|
| Change the OpenRouter key and the passwords posted in Slack | Oleg, with Justin's team | Before any connection (START-HERE Step 5) |
| Delete the credential messages from Slack; change the OutFlo login posted there on Sep 18 | Justin's team | Now; not a condition for the install |
| A clear answer on bought Gmail accounts (#61); who sends client referral asks (#39); the residual-income line in the Hermes partner copy (#79) | Justin's team | Before M4 |
| Check that Oleg's Grok plan includes Grok Bot | Oleg | OPEN_QUESTIONS #1 |
| Create the private GitHub repo and push | Justin | Gated: needs his yes |
| Make the repo readable by Oleg's bot (GitHub access, or send him the zip), and attach CLIENT-CONTEXT.md, DREAM-MAP.md and the master ASKS.md | Justin's team | Before install: without one of the two routes the bot can't get the repo |
| Client list, rank-report source, proof OKs, invoices location | Oleg | OPEN_QUESTIONS #3–#7 |
| Carry `requests/for-justins-team.md` items to the Hermes side | Justin's team | Weekly, once installed |
| Merge Grok-side asks (G-numbers) into the master ledger | Justin's team | When the Monday digest lists new asks |

## Change log

| Date | Change | Asks |
|---|---|---|
| 2026-10-27 | First build: seven active bots, two reserved, 12 routines, 27 skills, two project specs. Built beside the Hermes overlay; the master ledger moved to Justin's client folder (`Oleg/ASKS.md`), with rows 1–63 unchanged and rows 64–77 added | #64–#77 new; Grok work added to #20, #32, #39, #40, #41, #44, #57, #59, #60, #61, #63 |
| 2026-10-27 | Independent review: 13 findings fixed (see above). Ledger rows 78–79 added; OPEN_QUESTIONS #17 added | #13, #39, #61, #78, #79 |

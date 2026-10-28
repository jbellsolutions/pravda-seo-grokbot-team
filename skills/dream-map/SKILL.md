---
name: dream-map
description: Keep Oleg's Dream Map, the whole vision for Pravda SEO in his own words grouped by business area, current, and write the monthly "dream check" for the first Monday digest. Use at setup (START-HERE Step 3), whenever Oleg describes where he wants the business to go, and on the first Monday of each month.
---

# Dream Map

Load pravda-context first.

Oleg's long view: "five years from now, I don't see myself working with. Clients, you know, I see myself working with partners" (Sep 18). He wants more systems built "once we build on this project and automate it" (Oct 5), and to reinvest "when I start to making money" (Oct 21). The Dream Map keeps that whole picture in one place he can read, and shows which bot or milestone serves each part.

## Inputs

- `/workspace/pravda-team/context/dream-map.md`: the map. At setup, save the `DREAM-MAP.md` Justin's team attached here word for word. If none was attached, start it from `/workspace/pravda-team/context/asks.md`, grouped by area.
- `/workspace/pravda-team/context/asks.md`: every ask, with its number and status.
- `/workspace/pravda-team/context/team-registry.md`: which bots and routines are actually on.
- `/workspace/pravda-team/repo/PROJECT_CHARTER.md` §10: the milestones.

## The map's shape

One section per business area. Each section has his words, quoted with the date, and below them a table:

| Part of the dream | Asks | Who serves it | State |
|---|---|---|---|
| Calls for dentists who don't advertise emergency care | 41 | Call Desk, M5 | specified |

There are three states, kept apart:
- **specified** (in the repo);
- **built** (the bot and routine exist, paused);
- **active** (switched on, and a run log line proves it).

A part served by his Hermes agents says "Hermes: Growth Manager" or "Hermes: Affiliate Manager", with state "Hermes side". The Chief never checks or changes the Hermes side.

The areas:
- Partners (Hermes side)
- His clients
- Pay-per-call and emergency dental
- Proof and authority
- Google Business Profiles
- New channels
- Money
- His time and records
- Later (direct clients, partner program on Grok)

## Steps

1. **New vision from Oleg** (a message, a call note): quote it under the right area with the date. If it's a new request, also add an ask row with the `ask-ledger` skill and link the row number here.
2. **State changes:** when the registry shows a bot or routine created, switched on or failing, update the State column. "Active" needs a run-log line as evidence.
3. **First Monday of the month:** write the dream check (below) to `/workspace/pravda-team/daily/<date>/dream-check.md`. The `pravda-week` skill includes it in that Monday's message.

## Output: the dream check (first Monday digest; example only)

```
Dream check (Nov):
Active: client pulse, listing check, records desk.
Built, waiting on you: Call Desk (your yes on emergency dental first).
New this month: you asked for 1 thing (#81).
Furthest from done: proof page (needs 3 client results you OK).
```

At most five lines. Each line names the next step and who owes it.

## Done

- Every ask row appears under some area.
- Every State is backed by the registry or a run-log line.
- The dream check went into the first Monday digest of the month.

## Never

- Mark anything "active" without a run-log line.
- Invent a goal, a number or a date Oleg didn't give.
- Change or judge what the Hermes agents do. List them as the Hermes side.
- Rewrite his words. Quote them.

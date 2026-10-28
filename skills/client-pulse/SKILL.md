---
name: client-pulse
description: The monthly client pulse. Read each client's newest rank report from the Maps Desk index, log real wins and drops in /workspace/pravda-team/data/wins.md, and write the month's summary for the Chief's Monday digest. Use in the Client pulse routine, or when Oleg asks "how are my clients doing?". Client Desk only.
---

# Client pulse

Load pravda-context first: read `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Work only in `/workspace/pravda-team/`. Client Desk is the only writer of `data/wins.md` and `daily/<date>/client-pulse.md`.

## Inputs

- `/workspace/pravda-team/data/clients.md`: active clients (Client Desk). If it's missing or has no active client, reply `NO_CLIENT_SOURCE: client roster` and stop.
- `/workspace/pravda-team/data/rankings/index.md` and `/workspace/pravda-team/data/rankings/<client>/`: filed rank reports (Maps Desk). Read only those two paths. Never go looking for reports elsewhere, and never log in to a rank tool.
- `/workspace/pravda-team/data/listings.md`: this week's listing status (Maps Desk).
- `/workspace/pravda-team/data/wins.md`: wins already logged, so none is logged twice.

## What counts

- **A win** is a change a filed report shows, compared with that client's previous report for the same keyword and area. Examples: a keyword entering the Google Maps top 3; moving onto page one of Google; a clearly better average map position; more calls, if the report counts calls. Each win cites the two report files.
- **A drop** is the reverse, or a listing the Maps Desk marked gone, changed or UNKNOWN.
- **No report this month** means `UNKNOWN` for that client. It is never "no change".
- Small moves that the report itself shows as noise, such as one position on one grid point, aren't wins. If unsure, write "small move" and leave it out of `wins.md`.

## Steps

1. For each active client, find the newest report and the one before it in the index.
2. Compare like with like: same keyword, same area, same tool. If the two reports differ in keyword or tool, say so and don't compare.
3. Append each new win to `data/wins.md`:
   ```
   | Date found | Client | Win (plain words) | Keyword · area | Evidence (two report files) | Client has seen it? | Asked? |
   ```
   **Client has seen it?** starts as `not yet known`. It becomes `yes` only when Oleg says so, or when Gmail shows the report sent to the client. **Asked?** starts empty.
4. Write `/workspace/pravda-team/daily/<date>/client-pulse.md`, one line per client: win, drop, no change, or UNKNOWN (with the reason).
5. If any client has dropped two pulses in a row, write `requests/to-chief/client-desk-<date>.md`, starting with the line `For: Oleg`, so the Chief puts it in front of him.

## Output (the summary the Chief reads; example)

```
Client pulse · Nov 2026 · 21 active (19 with a report, 2 UNKNOWN)
Wins (4): Example Dental, "emergency dentist <area>" now #2 on Maps (was #7) · report 2026-11-01 vs 2026-10-01
Drops (1): Example Spa, listing marked "changed" by Maps Desk (category)
No report: Example Law (report source REQUIRED), Example Roofing (no file since Sep)
Waiting on you: 3 wins, has the client seen them? (needed before any referral ask)
```

## Done

Every active client has a line: win, drop, no change or UNKNOWN with a reason. Every win in `data/wins.md` cites two report files. Nothing was logged twice.

## Never

- Invent, round up or estimate a ranking. Every number comes from a file.
- Log a win from a report you couldn't read.
- Tell a client anything. This summary is for the Chief and Oleg only.
- Write the rankings files or the listing watchlist. Those are the Maps Desk's.

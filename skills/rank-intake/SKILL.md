---
name: rank-intake
description: File every new rank report (Local Falcon exports, reports from Oleg's own rank tool) under its client in /workspace/pravda-team/data/rankings/, with an index Client Desk reads for wins and drops. Also notice Google notices about client listings. Use in the Rank intake routine, or when Oleg drops a report in data/rankings/inbox/. Maps Desk only.
---

# Rank intake

Load pravda-context first: read `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Work only in `/workspace/pravda-team/`. Maps Desk is the only writer of `data/rankings/`.

**Where this comes from.** Oleg pays for Local Falcon and also built his own rank tool (Slack, Oct 9–12). His clients mostly read their reports and pay their invoices. The team needs those reports in one place to spot wins (asks #39, #65) and listing trouble (#70). The team logs into no rank tool and pays for none.

## Inputs

- **Gmail, read-only.** Where his reports arrive: the sender or subject pattern in `/workspace/pravda-team/context/config.json` → `rank_reports.email_from` and `rank_reports.subject_contains`. If those are `REQUIRED`, skip Gmail and say so in the run log.
- **Files Oleg drops** in `/workspace/pravda-team/data/rankings/inbox/`.
- `/workspace/pravda-team/data/clients.md`: to match a report to a client.
- **Google notices in Gmail** about a client listing (suspension, edits, verification), matched by business name.

## Steps

1. Find the reports that have arrived since the last run: emails with an attachment or link that match the pattern, plus files in `inbox/`.
2. Match each to a client by the business name or website in the report. If there's no clear match, put it in `data/rankings/unmatched/` and list it. Never guess.
3. Save it as `data/rankings/<client>/<report date>-<tool>.<ext>`. Keep the original file. If the report is only a link, save the email text and the link.
4. Read what the file says and add one line to `data/rankings/index.md`:
   ```
   | Client | Report date | Tool | Keywords · area | Headline numbers (as printed) | File | Readable? |
   ```
   Copy the numbers exactly as the report prints them. If a format can't be read, the line says "needs reading by Oleg" and the headline numbers say UNKNOWN.
5. Move handled files out of `inbox/` into the client folder. Never delete anything.
6. If a Google notice about a client listing arrived, append it to `/workspace/pravda-team/data/gbp-log.md` (date, client, what the notice says, quoted). If it says suspended or removed, alert Oleg the same day, in the same format as `listing-watch`.
7. If nothing new arrived, write NO_CHANGE and stop. This routine sends Oleg nothing else.

## Done

Every report that arrived is filed under the right client, or in `unmatched/`, and has one line in the index. Numbers in the index match the file word for word.

## Never

- Log in to Local Falcon, his own tool, Google or anything else, or ask for a login.
- Change, average or estimate a ranking.
- Forward a report to anyone.
- Delete an email or a file.

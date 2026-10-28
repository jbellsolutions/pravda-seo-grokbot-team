---
name: ppc-pilot
description: Call Desk's pilot skill. Use in the weekly Call Desk run, or when Oleg asks "where are we on emergency dental?". It keeps the pay-per-call pilot plan and tracker, checks every source is legitimate inventory, and logs calls only from real exports.
---

# Pay-per-call pilot

Load pravda-context first: `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`. The full plan, with the decisions and milestones, is `/workspace/pravda-team/repo/projects/pay-per-call-pilot/SPEC.md`.

## Inputs

- `/workspace/pravda-team/context/config.json` → `ppc.first_niche`, `ppc.model`, `ppc.tracking_numbers_source`, `ppc.call_counts_when` (the qualifying rule a buyer agreed to in writing).
- `/workspace/pravda-team/data/ppc/pilot.md`: your tracker.
- `/workspace/pravda-team/data/ppc/buyers.md`: buyers at status `talking`.
- Call-platform exports Oleg or his phone provider gives (a file in `/workspace/pravda-team/data/ppc/exports/`, or a dated email Oleg forwards). The bot can't see calls any other way.

## The legitimacy check (before any source goes in the tracker)

A call source is allowed only if all of these are true, each with a link or a document:
1. It belongs to a real practice that operates at that address, with staff there in its listed hours. (Check its own website and its public listing.)
2. The practice really offers emergency care. (Its own site or its written word.)
3. The calls come through the practice's one real profile and website: no second profile at the same address, and no keywords added to its name. A practice that doesn't advertise emergency care separately gets it on its existing profile and site (its services, its hours), never a new profile.
4. The practice has given written OK for its calls to be tracked and for the pilot's terms. (A file or email; record where it is, never the content.)
5. Or it's an honestly labelled referral website Oleg owns (a website, never a Google Business Profile), where callers are told they're reaching a referral service *(inferred model; a compliance advisor checks it first, per the spec)*.

If any check fails or is UNKNOWN, the source stays `blocked: <which check>` and nothing is planned on it.

## Steps

1. Read `pilot.md`. Refresh the "Decisions Oleg still owes" list from the spec and config: first niche, model, numbers, qualifying rule, first buyer, compliance check. Each line in plain words, one question each.
2. Run the legitimacy check on any new source Oleg names.
3. **Tracking numbers.** List only numbers Oleg has assigned, from `ppc.tracking_numbers_source`. They are **voice only**. If a plan step would send a text from one of his virtual numbers, drop the step and say why.
4. **Call log.** When there's a new export, add one row per call: date, source, buyer, length, counted (by the written rule) yes or no, billed yes or no. Totals per buyer and source. Without an export, the week's counts are UNKNOWN, never zero.
5. Write the status to `pilot.md`: the stage from the spec, what changed, what's blocked and why. Add two lines to `/workspace/pravda-team/daily/<today>/call-desk.md`.

## Output format

`pilot.md` sections, in this order:
- **Stage:** from the spec's milestones.
- **Decisions Oleg still owes:** a checklist.
- **Sources:** each with the check results and links.
- **Buyers:** taken from buyers.md.
- **Tracking numbers:** voice only.
- **Call log:** a table.
- **Totals:** each with its export file.

## Done

`pilot.md` shows the stage, every open decision, every source's check results with evidence, and calls only from exports.

## Never

- Plan, create or touch a Google Business Profile, or plan rank-and-rent, a listing for a business that isn't there, or a virtual or unit-number address.
- Send texts from Oleg's numbers, or set up any phone system.
- Invent a call, a count or a price.
- Agree terms with a buyer or a practice. Those are Oleg's.

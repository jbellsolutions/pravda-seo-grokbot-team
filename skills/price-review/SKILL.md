---
name: price-review
description: The quarterly price review. List the clients who have paid the same price for years, the wins that support a bigger plan, and a talk-track draft for each, so Oleg can move clients off $300–500 plans with proof. Use in the Price review routine, or when Oleg asks "who should pay more?". Oleg decides every price. Client Desk only.
---

# Price review

Load pravda-context first: read `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Work only in `/workspace/pravda-team/`. Client Desk is the only writer of `data/price-review.md` and `approved/pending/price-review/`.

**Where this comes from.** Oleg starts at $300 a month because about 95% of his business is referral, and his oldest referral clients have never had a price increase (Sep 15). He said "$300 or $500… are not the prices that I want to have", and wants to prove results on small plans first ("show them the first keywords on the first page of Google"), then show the bigger plans (Sep 18). Ask #65.

## Inputs

- `/workspace/pravda-team/data/clients.md`: plan, start date, status, notes.
- `/workspace/pravda-team/data/wins.md`: wins with evidence.
- `/workspace/pravda-team/data/listings.md`: listing health.
- `/workspace/pravda-team/data/price-review.md`: last quarter's list and what Oleg decided.
- His plan levels or price list, if he has given one (`context/owner.md` → plans). If none is on file, write the bigger plan as "next plan up (Oleg to name)", and add the question to the message.

## Who goes on the list

- `active`, and on the same price for a long time: the roster's **Since** is old and **Plan** hasn't changed. Rank by how long, longest first.
- At least one win in `data/wins.md` in the last two pulses, or a steady top-3 position the reports show. No win means no case: list the client as "build the case first", not as a price conversation.
- Not on the list: anyone with a complaint, a late invoice or a drop in the last two pulses, or anyone Oleg excluded last quarter, unless he says otherwise.
- At most 10 clients per quarter (starting value).

## Steps

1. Build the list and write it to `data/price-review.md`, under the quarter's heading: client, price, since, the wins (with evidence), and the suggested next step.
2. For each client on the list, write a talk-track draft in `/workspace/pravda-team/approved/pending/price-review/<quarter>-<client>.md`. It covers:
   - the results (from the record);
   - what more could be done (more keywords, another area, another listing the client actually operates);
   - the plan change, as a question for Oleg to fill in: "[next plan, price Oleg sets]".
3. The list reaches Oleg in the Chief's next Monday digest. When he opens this chat, go through it with him. Write his decision per client into `data/price-review.md`: raise, offer upgrade, wait, or exclude, with the date.

## Talk track (Example only)

```
[First name], quick update on your Google results:
- [win 1 from the record]
- [win 2 from the record]
You've been with me since [year], and your plan hasn't changed since then.
Here's what I'd do next: [more keywords / another area]. That's on the [plan Oleg names] plan at [price Oleg sets].
Want me to set it up?
```

## Message to Oleg (example)

```
Price review, Q1: 6 clients have paid the same since before 2020 and have fresh wins.
Top 3: Example Dental (since 2014, top 3 on Maps for 2 searches), Example Spa, Example Law.
Talk tracks: approved/pending/price-review/. Tell me per client: raise, upgrade offer, wait, or skip.
```

## Done

The quarter's list exists with evidence for every name, each name has a talk-track draft, and Oleg's decision per client is recorded.

## Never

- Contact a client about price, or hint at a change in any other draft.
- Pick a price. Oleg names every plan and every price.
- Put a client on the list with no evidence.
- Change an invoice, plan or GHL record.

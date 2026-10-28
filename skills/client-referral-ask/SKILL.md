---
name: client-referral-ask
description: Draft the "who can I make happy" referral ask Oleg asked for on Aug 6, after a real win a client has seen. Use in the Win asks routine, or when Oleg says "ask <client> for a referral". One ask per win, at most one per client in 90 days. Drafts only; Oleg sends from his own email. Client Desk only.
---

# Client referral ask

Load pravda-context first: read `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Work only in `/workspace/pravda-team/`. Client Desk is the only writer of `approved/pending/client-asks/`.

**Where this comes from.** On Aug 6 Justin described a mentor's habit of asking happy customers for a referral 21 days after the sale [2:44], and Oleg asked (speaker inferred; the transcript doesn't name him) [3:45]: "who can I make happy in 21 days when it comes to my work?" Justin noted that the right day may differ for SEO. So here the ask follows a real win the client has seen, and 21 days after the win is the first timing to test.

## Inputs

- `/workspace/pravda-team/data/wins.md`: wins, whether the client has seen each one, and whether it was asked.
- `/workspace/pravda-team/data/clients.md`: status and notes (complaints, late invoices, "don't ask").
- `/workspace/pravda-team/context/standing-approvals.md`: whether a standing approval covers this exact template (none at first).
- Gmail, read-only: the client's recent emails, to check for a complaint or a cancel request since the roster was last updated.

## Who gets an ask (all must be true)

1. The win is in `data/wins.md`, with evidence, and **Client has seen it?** is `yes`.
2. At least 21 days have passed since the client saw the win (the starting value to test).
3. The client hasn't been asked in the last 90 days, by this skill or by Oleg himself (Oleg's word or a sent email in Gmail).
4. The roster shows the client `active`, with no complaint, no late invoice and no "don't ask" in Notes, and Gmail shows no complaint or cancel request since.

If 3 or 4 can't be checked, the answer is no: list the client as "waiting: <what's unknown>".

## Steps

1. Pick the clients who pass, at most 3 per run (starting value). If none pass, write NO_CHANGE.
2. For each one, fill the template below with the real win from `data/wins.md` in plain words. Save it to `/workspace/pravda-team/approved/pending/client-asks/<date>-<client>.md`, with the evidence line underneath (not part of the email).
3. Mark the win's **Asked?** as `drafted <date>`. Mark it `sent <date>` only when Oleg says he sent it, or Gmail shows it in Sent.
4. List this run's drafts in `/workspace/pravda-team/daily/<today>/client-desk.md` for the Monday digest. Never message Oleg about them; when he opens this chat, show them.

## The template (Example only: fill every bracket from the record)

```
Subject: [first name], quick thank-you

Hi [first name],

I'm glad to see [the win in plain words, e.g. "you showing up in the top 3 on Google Maps for <search term>"]. That's good work, and you made it possible.

One question: who do you know who'd be happy with results like this? A friend, a supplier, another local business owner. If someone comes to mind, just reply with their name, or forward them this email, and I'll take good care of them.

Thank you,
Oleg
Pravda SEO
```

Rules for the draft:
- The win is quoted from the record, never improved.
- One ask, no discount, no pressure, no fee mentioned. The client referral path is Oleg's own; partner commissions are the partner program's business, not this email's.
- Under 120 words.

## Message to Oleg (example)

```
2 referral asks ready (Example Dental, Example Spa). Both saw their win 3+ weeks ago, no complaints, not asked this quarter.
Drafts: approved/pending/client-asks/. Send from your email if they look right, then tell me "sent".
```

## Done

Every eligible win has a draft or a written reason it waits. No client gets two asks inside 90 days. **Asked?** in `data/wins.md` matches what happened.

## Never

- Send the email, or message the client any other way.
- Draft for a client who complained, is behind on an invoice, left, said "don't ask", or hasn't seen the win.
- Invent or exaggerate the win.
- Offer money or a gift for a referral without Oleg's written decision.

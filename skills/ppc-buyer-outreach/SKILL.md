---
name: ppc-buyer-outreach
description: Call Desk's drafting skill. Use in the weekly Call Desk run once Oleg has said yes to the first niche, or when he asks for a note to a dental marketing agency or a call network. It drafts short business emails for Oleg to send himself, and reads buyers' replies.
---

# Buyer outreach (drafts only)

Load pravda-context first: `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

## Inputs

- `/workspace/pravda-team/context/config.json` → `ppc.first_niche`. If it isn't set, write no drafts: append "no drafts: first niche not chosen" to today's note and stop this skill.
- `/workspace/pravda-team/data/ppc/buyers.md`: rows with status `new` and a public business contact page.
- `/workspace/pravda-team/data/ppc/pilot.md`: what actually exists today. Before a pilot there's no inventory, so the note asks a question; it never offers calls.
- Gmail, read-only: threads with buyers in `buyers.md`.
- `/workspace/pravda-team/context/owner.md`: Oleg's sender name and the postal address for the footer.

## Steps

1. **Replies first.** Read Gmail threads with buyers whose status is `sent by Oleg`. For each reply, set the status (`replied`, `talking`, `no`) and summarize it in one line for Oleg, quoting the buyer. Never reply. If a buyer asks for prices, terms, a contract or sample calls, stop and tell Oleg; those are his calls.
2. **Sent check.** If Gmail shows Oleg sent a pending draft, set that buyer to `sent by Oleg`, with the date.
3. **Partner check.** Look each candidate up in GHL, read-only, by company name and website domain. If it's already a partner, a partner prospect or a client, draft nothing: set its status to `Hermes side` and hand it to the Chief in `/workspace/pravda-team/requests/to-chief/call-desk-<today>.md`, starting "For: Justin's team". If GHL can't be read, draft nothing this run.
4. **New drafts.** Draft up to 3 notes per run, starting value, for the strongest `new` buyers that passed the check. Each note:
   - comes from Oleg, to the address on the buyer's own contact page;
   - is 90 words or fewer, with one ask: a yes/no question or a short call;
   - says who he is in one line (19 years in local SEO, Forbes Business Council);
   - says what he's exploring, honestly: before a pilot, he's asking whether they buy emergency-dental calls in a named metro and on what terms;
   - claims nothing that isn't sourced: no volumes, no results, no client names;
   - ends with the footer pravda-context requires: Pravda SEO Inc's postal address and a plain way to say no.
5. Save each draft to `/workspace/pravda-team/approved/pending/ppc/<YYYY-MM-DD>-<buyer-slug>.md`, with the buyer row and its evidence link at the top. Set the buyer's status to `drafted`.
6. List that run's drafts (buyer, why them, the file) in today's call-desk note for the Monday digest. When Oleg opens this chat, show them. He sends from his own email, or tells you what to change. Only a buyer's reply goes to Oleg the same day.

## Output format

```
To: <public business address from their contact page>
Subject: <plain, under 8 words>

<Hi name, or Hi there>
<one line: why them, from the evidence link>
<one line: who Oleg is>
<one question>

Oleg Levitas
Pravda SEO Inc · <postal address from owner.md>
Not for you? Reply "no" and I won't write again.
```

Example only, not sent and not a real buyer:

```
Subject: Emergency dental calls in Queens?

Hi there,
I saw your agency runs marketing for several dental practices.
I've done local SEO for 19 years and I'm a Forbes Business Council member.
Do you buy emergency-dental calls for your practices in Queens, and if so, what makes a call count for you?

Oleg Levitas
Pravda SEO Inc · <address>
Not for you? Reply "no" and I won't write again.
```

## Done

Every draft is in `approved/pending/ppc/` with its evidence. Oleg got one message listing them. Every reply is summarized and the buyer statuses match Gmail.

## Never

- Send, reply, follow up, or message any buyer.
- Promise call volume, quality, prices or exclusivity.
- Name Oleg's clients or use a result Oleg hasn't OK'd.
- Write to an address that isn't published on the buyer's own site, or guess an email address.

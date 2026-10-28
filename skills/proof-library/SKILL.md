---
name: proof-library
description: Keep Oleg's proof library (every testimonial, client result, review, recommendation and Forbes piece, each with its source and whether Oleg OK'd it) and draft the proof page from it. Use when proof arrives, when Oleg OKs or withdraws an item, when a draft needs proof, or when the weekly Authority piece is a proof-page section. For Authority Studio.
---

# Proof library and proof page

Load pravda-context first: `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Oleg's ask (Aug 6): partners must see "that we're not just another startup SEO companies", using his video testimonials, client results and Forbes. On Oct 13 he asked what to do with AI in his niche. Justin's answer started with this: gather the case studies and testimonials into a proof page. The plan is [`projects/proof-page/SPEC.md`](../../projects/proof-page/SPEC.md).

## Inputs

- `/workspace/pravda-team/data/proof/index.md`: the library (you're its only writer).
- `/workspace/pravda-team/requests/to-authority-studio/`: testimonials and wins handed over by Client Desk (see [`skills/testimonial-request`](../testimonial-request/SKILL.md)), each with the client's own words and their permission status.
- The starting set Oleg provides: his client rankings video, video testimonial, Google reviews, LinkedIn recommendations, Forbes Councils profile and PDF presentation (shared in Slack Sep 16), plus the YouTube testimonial videos he offered on the Sep 15 call. The links are in `/workspace/pravda-team/context/owner.md` once Chief saves them. If they're missing, ask Chief to request them from Oleg once.
- His Forbes articles: public pages.
- Gmail read-only: only threads Oleg points to.

## The library format

One row per item in `data/proof/index.md`:

| ID | Type | What it shows | Source (link or file) | Client named? | OK'd by Oleg | Use for |
|---|---|---|---|---|---|---|
| P-001 | video testimonial | … in the client's words | <link> | yes/no | 2026-11-03, "yes, use it" / not yet | proof page, VSL, talks |

- **Type:** video testimonial, written testimonial, Google review, LinkedIn recommendation, ranking result, call result, Forbes article, credential.
- **What it shows:** a quote or a plain description, copied from the source. Never paraphrased into something stronger.
- **OK'd by Oleg:** his own words and the date, or `not yet`. Only Oleg's own yes in chat counts.
- **Client named?** A result naming a client also needs that client's permission. Write `client permission: yes (date, how)`, or `no`. Without it, the item can be used only without the name and anything that identifies the business.

## Steps

1. **New proof arrives.** Add a row with its source, set **OK'd** to `not yet`, and add it to the "Waiting for your OK" list in `daily/<date>/authority-studio.md`. Chief asks Oleg in the Monday digest, a few items at a time.
2. **Oleg OKs or withdraws an item.** Record his words and the date. A withdrawn item is marked `withdrawn <date>` and removed from every pending draft.
3. **Proof-page section** (when it's the week's piece): draft one section of `approved/pending/proof-page.md` from OK'd items only:
   - who Oleg is (19 years, Forbes Business Council);
   - results, each with its source;
   - testimonials in the clients' own words;
   - the Forbes articles, each with its link;
   - how he works ("plans from $300", local only, no e-commerce).

   Mark every claim with its library ID, for example `[P-004]`.
4. **When the page draft is complete and Oleg approves it,** hand the build to Chief through `requests/to-chief/authority-studio-<date>.md`. Chief writes a plain task card for his developer with [`skills/developer-task-card`](../developer-task-card/SKILL.md). You never touch the website.

## Output

- The library table.
- `approved/pending/proof-page.md`, every claim tagged with an ID.
- One line in `daily/<date>/authority-studio.md`: "Library: <n> items, <m> OK'd, <k> waiting for you."

## Done

- Every library row has a source and an OK status.
- The page draft uses only OK'd items, and every claim has an ID.

## Never

- Use an item that says `not yet` or `withdrawn`.
- Name a client without that client's permission on record.
- Invent, round up or "improve" a result, quote or ranking.
- Publish the page, post proof anywhere, or send it to anyone but Oleg.
- Write LinkedIn posts or newsletters from the library: the Hermes agents own those.

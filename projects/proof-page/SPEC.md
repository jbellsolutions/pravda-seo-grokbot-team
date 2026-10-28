# Project spec: the proof page

**Owner of the content:** Authority Studio ([charter](../../agents/04-authority-studio.md)) · **Owner of the page:** Oleg · **Built by:** his developer, from a task card · **Asks:** 20, 40

## Why

Oleg wants every partner and owner to see "that we're not just another startup SEO companies" (Aug 6). He has the proof:
- 19 years in local SEO;
- Forbes Business Council membership, with about 10–12 articles;
- video testimonials, client results, Google reviews and LinkedIn recommendations.

It's scattered across links and files. On Oct 13 he asked what Justin recommends "for my niche, to monetize it". Justin's first answer was to gather the case studies and testimonials into a proof page. This spec makes that one page.

## Goal

One page that a partner, a partner's client or a local owner can read in a few minutes. It shows, with sources, that Oleg delivers. Everyone who sends people to Oleg (his emails, the partner side, his talks) can link to it.

## What goes on it

Use only items in `/workspace/pravda-team/data/proof/index.md` marked **OK'd by Oleg**. A named client also needs that client's permission on record.

1. **Who he is:** 19 years in local SEO; Forbes Business Council, with links to his articles; local businesses only, no e-commerce.
2. **Results:** each one says what changed, for which kind of business (named only with permission), and where the number comes from (a rank report, a call log). No result without its source.
3. **In clients' words:** video and written testimonials, Google reviews and LinkedIn recommendations, quoted exactly.
4. **How he works:** local only; plans from $300 a month for every budget, with room to grow; what a client gets each month.
5. **One next step:** how to reach him. Oleg picks the contact route.

## Where it lives (Oleg decides)

- **Option A: his main site, realresultsseo.com.** His developer adds the page. Its DNS stays untouched (his Oct 13 rule).
- **Option B: pravdaseo.com.** It already points at GHL for the partner sign-up. The page would be built in GHL, next to the partner page.

Either way, Authority Studio hands the approved copy to Chief (a file in `requests/to-chief/` starting "For: developer"), and Chief writes a task card for his developer ([`skills/developer-task-card`](../../skills/developer-task-card/SKILL.md)). No bot edits a website.

## Decisions Oleg must make

1. Which proof items he OKs. He answers a few at a time in the Monday digest.
2. Which clients he'll ask for permission to be named. Client Desk drafts those requests ([`skills/testimonial-request`](../../skills/testimonial-request/SKILL.md)).
3. Option A or B.
4. The contact route at the bottom of the page.

These are also in [OPEN_QUESTIONS.md](../../OPEN_QUESTIONS.md).

## Milestones

| Milestone | What happens | Done when |
|---|---|---|
| P1: Library | Every proof link Oleg already shared (the Sep 16 Slack list and the Sep 15 testimonial videos) is logged with a source | `data/proof/index.md` lists them all, each `not yet` or OK'd |
| P2: OKs | Oleg OKs the items he's comfortable using; named clients give permission | At least one item in each of sections 1–3 is OK'd |
| P3: Draft | Authority Studio drafts the page, one section per weekly piece | `approved/pending/proof-page.md` is complete, and every claim carries a library ID |
| P4: Approval | Oleg reads the whole draft and says yes, or sends changes | His yes is recorded in `vault/Decisions.md` |
| P5: Build | His developer builds the page from Chief's task card | The page is live, and Oleg confirms it looks right |
| P6: Upkeep | New OK'd proof is added; withdrawn items come off | The library and the page match |

## Never

- Use proof Oleg hasn't OK'd, or name a client without permission.
- Invent, round up or reword a result to sound stronger.
- Promise rankings, call volumes or income.
- Publish or edit the page from a bot. His developer builds it, and Oleg approves it.

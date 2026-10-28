---
name: getting-started
description: The intake interview. Use once at setup (START-HERE Step 3), or whenever Oleg says their basic facts changed. It confirms what the build already knows, asks only what's missing, one question at a time, and writes Oleg's facts and the team config.
---

# Getting started: the intake

Load pravda-context first.

## Inputs
- `/workspace/pravda-team/repo/client-context/CLIENT-CONTEXT.template.md`: the headings.
- The private client context, if Justin's team attached it. Save it to `/workspace/pravda-team/context/owner.md` before you ask anything.
- `/workspace/pravda-team/repo/OPEN_QUESTIONS.md`: the questions that are waiting.

## Steps
1. If `context/owner.md` exists, read it back in one message: "Here's what I know. Is anything wrong?" Fix only what Oleg corrects.
2. Ask each line still marked `ASK`, then the OPEN_QUESTIONS rows that this milestone needs:
   - one question per message;
   - short enough to answer on a phone;
   - offer choices when there are only a few.
3. Write each answer in place of its `ASK`, with today's date. Write the team's settings to `context/config.json`. A required field nobody knows yet stays `REQUIRED`; never guess it.
4. When the apps are connected later, fill in any IDs you can now look up yourself (the GHL pipeline names, the sender addresses of his rank reports and tool receipts), then confirm them with Oleg.
5. Done: no `ASK` is left that the current milestone needs. Oleg has said "right" to the readback.

## The keys in `context/config.json`

You are the only writer of this file. Other bots read their own section. Write `REQUIRED` until Oleg answers, never a guess.

| Key | What | Asked at | OPEN_QUESTIONS |
|---|---|---|---|
| `records.senders` | People and domains the records desk files: his clients, partners, his developer, vendors he names | M3 | 3, 15 |
| `records.last_sweep` | Set by the records sweep; start it at the install time | M3 | — |
| `rank_reports.email_from`, `rank_reports.subject_contains` | How his rank reports arrive in Gmail (sender, subject words) | M3 | 4 |
| `ppc.first_niche` | The first pay-per-call niche he picks (emergency dental is the suggestion) | M5 | 6 |
| `ppc.model`, `ppc.call_counts_when`, `ppc.tracking_numbers_source`, `ppc.networks_already_tried` | How the pilot sells calls, what counts as a billable call, which of his numbers track calls (voice only), networks he already tried | M5 | 6 |
| `money.invoice_source` | Where his client invoices live | M6 | 7 |
| `money.tools`, `money.lead_vendor` | Vendor names to look for in receipts; who he buys leads from | M6 | 7 |

The client list itself goes in `/workspace/pravda-team/data/clients.md`. The Client Desk builds it from his answer to OPEN_QUESTIONS #3, which you hand over in `/workspace/pravda-team/requests/to-client-desk/chief-<date>.md` at START-HERE Step 6b, once the Client Desk exists.

## Never
- Ask for a password, key or token in chat.
- Invent a fact to fill a gap.
- Ask two questions in one message.

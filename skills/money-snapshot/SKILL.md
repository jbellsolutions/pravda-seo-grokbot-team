---
name: money-snapshot
description: Profit Desk's monthly money view. Use in the monthly Money snapshot run, or when Oleg asks "is this paying for itself?" or "what did we make from partners?". It shows revenue by channel, the cost of the growth work, the "covering it and making money on top" line, and reinvest options once there's profit.
---

# Money snapshot

Load pravda-context first: `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Oleg, Aug 6: "I wanna make sure that somehow, you know, I cover this and make money on top." Oct 21: "When I start to making money, I want to reinvest money in other projects."

## Inputs

- `/workspace/pravda-team/context/config.json` → `money.invoice_source` (where his client invoices live), `money.tools` (vendor names to look for in receipts), `money.lead_vendor`.
  - If `money.invoice_source` is missing or `REQUIRED`, client revenue is UNKNOWN. Say so at the top of the snapshot, and stop and tell Oleg once per month.
- `/workspace/pravda-team/context/owner.md`: the one-time fee Oleg paid Justin's team.
- `/workspace/pravda-team/data/money/spend-log.md`: every receipt line already read (built by `spend-watch`).
- Gmail, read-only: receipts and invoices for the month, from the vendors in `money.tools`.
- GHL, read-only: affiliate referrals, the referred clients, and payouts and commissions for the month.
- `/workspace/pravda-team/data/clients.md` (Client Desk's roster, read-only): plan, start date and, where recorded, how each client came in.
- `/workspace/pravda-team/data/ppc/pilot.md` (Call Desk, read-only): only once there's a pilot.

## Steps

1. **Close the month.** Work on the calendar month just ended. Read any receipts `spend-watch` hasn't logged yet and add them to `spend-log.md`.
2. **Revenue by channel.** Each figure gets a source: an invoice, a GHL record or a roster row.
   - Existing clients: from the invoice source. Without one, UNKNOWN. Roster plan totals may be shown only as "plan prices per roster, not collected".
   - Partner-referred clients: referred clients from GHL, with what they pay from the invoice source.
   - Direct clients from the partner side's Map Pack or bought leads: only where the roster records that source.
   - Pay-per-call: from `pilot.md` totals, once there's a pilot.
3. **The cost of the growth work.** From receipts and GHL:
   - tools: Instantly, Orgo, OpenRouter, GoHighLevel with its phone and A2P charges, sending inboxes, Local Falcon;
   - leads he bought;
   - partner commissions paid;
   - the fee, as "the one-time fee in owner.md, paid <date>". Never write its amount in the snapshot; show it in the running total as a line item only.
4. **The line.** Growth costs this month and since the start, against the new monthly revenue the growth work brought this month and since the start. Answer "covering it and making money on top?" with `yes`, `not yet` or `UNKNOWN`, and show the math. If any input is UNKNOWN, the answer is UNKNOWN, with what's missing. This line is not the six-month 10× guarantee: the Telegram side's monthly review owns that figure. Never compute or report progress against the 10× or the 90-day guarantee. Label partner-referred revenue "from GHL; the guarantee figure is in your Telegram review".
5. **Reinvest options**, only when the month's line is `yes`: up to 3 business options drawn from the team's own work, each with a sourced cost. Examples:
   - a Channel Scout test Oleg hasn't run yet;
   - the next step of the Call Desk pilot;
   - more sending inboxes of his own (Justin's Oct 21 advice).

   They're options for Oleg to decide, not advice.
6. Write `/workspace/pravda-team/data/money/<YYYY-MM>.md`, and a five-line summary to `/workspace/pravda-team/daily/<today>/money.md` for the Chief's Monday digest.

## Output format

```
# Money — <Month YYYY>
Covering it and making money on top? <yes | not yet | UNKNOWN> — <one line of math or what's missing>
## Revenue by channel
| Channel | This month | Source |
## Cost of the growth work
| Item | This month | Since start | Source |
## Reinvest options (only if yes)
1. … cost <amount, source> · why · who would own it
UNKNOWN this month: …
```

## Done

Every figure links to a receipt, GHL record or roster row, or says UNKNOWN. The line is answered with its math. The summary is in today's daily folder.

## Never

- Pay, buy, cancel, upgrade or change any plan or subscription; log into a bank, card, Stripe or payment tool; move money or pay commissions.
- Write to GHL.
- Estimate a figure it can't source, or treat a roster plan price as money collected.
- Give tax, legal or personal investment advice.
- Compute or report the 90-day guarantee. The Hermes scorecard owns it.

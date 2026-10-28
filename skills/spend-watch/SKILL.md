---
name: spend-watch
description: Profit Desk's weekly receipt scan. Use in the Friday Spend watch run, or when Oleg asks "what do the tools cost?". It logs every receipt line and alerts Oleg only when a bill jumps or a new recurring charge appears.
---

# Spend watch

Load pravda-context first: `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

On Oct 5 Oleg asked what each tool costs: OpenRouter top-ups ("How much should I add?"), Orgo computers ("So do I need to add more money?") and phone numbers ("How much are the numbers?"). He set an OpenRouter auto top-up on that call.

## Inputs

- `/workspace/pravda-team/context/config.json` → `money.tools`: the vendors to look for. Start from Instantly, Orgo, OpenRouter, GoHighLevel (and its phone and A2P charges), the sending-inbox vendor, Local Falcon, and his lead vendor. Oleg confirms the list.
- `/workspace/pravda-team/data/money/spend-log.md`: your log.
- Gmail, read-only: receipts and invoices since the last logged one.

## Steps

1. Find receipts and invoices since the last run, from the vendors in `money.tools`. Also look for receipts from any vendor not on the list.
2. Log each one in `spend-log.md`:
   - date;
   - vendor;
   - amount;
   - one-time, recurring or top-up;
   - a link to the email.

   Never copy card numbers or account details; amounts and dates only.
3. Compare each new bill with the same vendor's previous bill. Flag it if:
   - it's more than 25% higher (starting value);
   - a new recurring charge appears;
   - a vendor not on `money.tools` charged him;
   - top-ups from one vendor happen more often than they did last month (for example OpenRouter's auto top-up).
4. **Nothing flagged:** append NO_CHANGE to the run log and send nothing.
5. **Something flagged:** send Oleg one message covering every flag. Add it to `/workspace/pravda-team/daily/<today>/money.md` too.
6. **During his away dates** (in `context/owner.md`): queue flags for the Monday after he's back. The exception is a charge from a vendor he doesn't use, which could be a security problem. That one goes at once.

## Output format

```
Spend watch — <date>
1. <Vendor>: <new amount> vs <previous amount> on <date> (+<n>%) — <link>
2. New recurring charge: <vendor>, <amount> — <link>
Nothing has been changed or cancelled. Tell me if you want me to dig into any of these.
```

## Done

Every receipt since the last run is in the log. Oleg got at most one message, and only if something was flagged.

## Never

- Cancel, change, downgrade or upgrade anything, or contact a vendor.
- Log into a bank, card, payment tool or vendor account.
- Store card or account numbers.
- Report a cost without its receipt.

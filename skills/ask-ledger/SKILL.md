---
name: ask-ledger
description: Keep the list of everything Oleg has asked for. Use whenever Oleg sends a new idea, request or "it would be cool if", and in the weekly wrap. Every ask becomes a numbered row, with where it's solved, so nothing gets lost.
---

# Ask ledger

Load pravda-context first.

Oleg has two teams. His Hermes agents in Telegram keep their own list of what he asks there. **You keep only the Grok-side list.** Justin's team merges both into the master ledger. Two writers never share one file.

## Inputs
- `/workspace/pravda-team/context/asks.md`: your intake list, the only file you write. It starts empty at setup. Number new rows from the master's last number + 1, prefixed `G` (G78, G79…), so they never collide with rows Justin's team adds.
- `/workspace/pravda-team/context/asks-master.md`: the master ledger Justin's team attached at install. Read-only: use it to find whether something is already a row and where it's solved. If it's missing (nothing was attached), number your rows G1, G2… and ask Justin's team for the master in the next "Pravda week". Never rebuild the master from memory.

## When Oleg asks for something new
1. Check whether it's already a row, in the master or in your list. If it's in the master, tell Oleg where it stands, and add a line under "Asked again" in your list with today's date. If it's yours, add today's date to its **When**.
2. If it's new, append a row:
   - number: the last number + 1;
   - their words, quoted;
   - today's date and where it came from;
   - a status from the key at the top of the file;
   - where it's solved: a bot, routine or skill that already does it; "Hermes side" if it's the partner program (then also write it to `/workspace/pravda-team/requests/for-justins-team.md`); or "new: needs Justin's team".
3. Reply in one line, for example: "Added as G78. The Client Desk can do it with a new step in the price review. Want me to send it to Justin's team?"
4. New builds are tier 3. Write a request in `/workspace/pravda-team/requests/`. Never build or turn on something new without Oleg's yes.

## Weekly
Report in the Monday "Pravda week":
- how many asks are open;
- the three oldest that wait on Oleg;
- anything that moved this week.

## Never
- Renumber rows.
- Drop an ask.
- Mark something done without evidence that it ran.

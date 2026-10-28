---
name: developer-task-card
description: Turn a website or technical job into one plain task card for Oleg's developer. What to do, where, why, and how to check it's done, with no bot jargon. Use when Oleg says "ask my developer to…", or when another bot hands the Chief a job that needs website or DNS work.
---

# Developer task cards

Load pravda-context first.

His developer handles the websites, DNS and hosting. On the Oct 13 call he said the bot messages were "giving me some kind of information that I have no idea what they're talking about." He also called himself "mostly technical guy" who loses the thread of business talk (Oct 21). A task card fixes that: one job, in his terms, with a way to check it.

## Inputs

- The job, from Oleg's message or from `requests/to-chief/<bot>-<date>.md`.
- `/workspace/pravda-team/context/owner.md`: his developer's name and the sites:
  - realresultsseo.com: the main site. Never change its DNS without Oleg's explicit yes, because that's his preference (Oct 13).
  - pravdaseo.com: the partner sign-up, pointed at GHL.

## Steps

1. If the job isn't clear enough to write the check, ask Oleg one question first.
2. Write `/workspace/pravda-team/requests/for-developer/<date>-<slug>.md` in the card format below.
3. Show Oleg the card in one message: "Card for your developer: <title>. Send it?"
4. On his yes, give him the card text, ready to forward to his developer by email (Gmail is read-only for this team, so Oleg sends it). Mark the card `SENT <date>` once he says it went.
5. When Oleg or his developer says it's done, run the check if a bot can (for example, a public page loads). Mark the card `DONE <date>` with the evidence, or `CHECK FAILED` with what you saw.

## Card format (the content is an example only)

```
Task: Put the new chat-widget code on the contact page
Site: realresultsseo.com → /contact
Why: so the business-texting registration check passes (Oleg asked)
Do:
1. Remove the old widget code from the page.
2. Paste the new code (attached) before </body>.
3. Turn off the pop-up sign-up box on that page only.
Don't: change DNS, other pages, or any form.
Done when: the contact page shows one chat bubble and no pop-up.
Questions: reply to Oleg.
```

At most 7 steps. Short words. No mention of bots, routines, skills or the Grok team.

## Done

- The card has a single job, one site, steps he can follow, and a done-check anyone can see.
- Oleg said yes before it went anywhere.

## Never

- Send a card, or contact his developer, without Oleg's yes.
- Put passwords, logins or keys on a card. Access is arranged between Oleg and his developer.
- Ask for DNS changes on realresultsseo.com unless Oleg asked for exactly that.
- Bundle several jobs in one card.

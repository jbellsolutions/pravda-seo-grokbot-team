---
name: gbp-playbook
description: Write Oleg's private Google Business Profile playbook from his own answers, one question at a time, and keep the vendor and suspension log. Every step that touches Google's rules is recorded with the rule (quoted from Google's current page, dated) and the compliant alternative, and is never carried out. Use when the Chief hands over "start the playbook", when Oleg answers a playbook question, or when a vendor or suspension event comes up. Maps Desk only.
---

# GBP playbook

Load pravda-context first: read `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Work only in `/workspace/pravda-team/`. Maps Desk is the only writer of `vault/Playbook/GBP.md` and `data/gbp-log.md`.

**Where this comes from.**
- Oleg's craft is Google Business Profiles that "start getting phone calls" fast. Yet "absolutely nothing about it is documented", because Google keeps changing, listings and reviews get removed "for no reason", and he keeps changing vendors, contractors and verification methods (Sep 18).
- Justin asked him to write up his multi-profile tactic (Sep 15).
- He asked whether bought Gmail accounts could be used for profile management and review placements (Oct 21). On Oct 21 Justin said he thought the inbox vendor could supply such accounts but didn't want to say yes for sure; nobody said no. Justin's team owes Oleg a clear answer (OPEN_QUESTIONS, owed table). This team's rule stands either way: never for profiles or reviews (ask #61).

Asks #70 and #61.

**The playbook is Oleg's private record of how he works.** It lives in the workspace vault, never in the repo, never shared. Writing a step down is not endorsing it: steps that break a Google rule are marked, never recommended, and never carried out by any bot.

## Inputs

- Oleg's answers, in the one-to-one chat.
- `/workspace/pravda-team/vault/Playbook/GBP.md`: what's already written, so no question is asked twice.
- `/workspace/pravda-team/data/gbp-log.md`: events from `listing-watch` and `rank-intake`.
- **Google's current guidelines,** read in the browser when a step touches them: "Guidelines for representing your business on Google" and the review policies on support.google.com/business. Quote the exact line, with the date read. Never state a rule from memory.

## The interview

One question per message, short enough to answer on a phone, at most three a week (starting value). Wait for his answer before the next. Go in this order, and skip what he's already answered:
1. **Who you take on:** which businesses get a profile project, and which he turns down.
2. **Setting up a profile:** name, primary and extra categories, services, hours, photos. His order, his reasons.
3. **Multi-location and multi-department businesses:** when one business gets more than one profile. Med spas were his example: Botox, laser hair removal (Aug 6).
4. **Addresses and service areas:** what address each profile uses, and why.
5. **Phone numbers:** local numbers, tracking numbers, which goes where.
6. **Verification:** the methods he uses now, and what changed.
7. **Vendors and contractors:** who does what, what each costs (if he wants it written), and why he switched.
8. **When a listing is removed or suspended:** what he checks, what he does, how long it took to come back.
9. **Reviews:** how happy clients are asked for reviews.
10. **Speed:** what makes a new profile get calls before it ranks or has reviews (his emergency-dental example, Sep 18).

## Writing each answer

Write it in `vault/Playbook/GBP.md` under its heading, in his words where possible, dated: `(Oleg, <date>)`.

Then check it against Google's rules. If the step involves any of the following, add a **Rule check** box under it:
- an address where the business doesn't operate or isn't staffed (a unit number or virtual office that nobody works from);
- more than one profile for one business at one place;
- a business name with extra keywords;
- reviews from anyone who isn't a real customer, or bought or aged accounts;
- incentives for reviews.

```
> Rule check (<date read>): Google's guidelines say: "<exact quote>" (<page title, URL>).
> Compliant alternative: <e.g. one profile with each service listed under Services; separate profiles only for departments with their own category, staff and hours, as the guideline allows>.
> No bot on this team carries out this step.
```

If the rule is unclear, write "Rule check: unclear. Ask Oleg or a GBP compliance source". Never decide it's fine.

## The vendor and suspension log

`data/gbp-log.md` holds one line per event:

```
| Date | Client | Listing | Event (removed / suspended / reinstated / vendor change / verification) | What was seen or said (quoted) | Source |
```

Events come from `listing-watch`, `rank-intake` (Google notices) and Oleg's answers. The log keeps no logins, no account names and no vendor contact details.

## Message to Oleg (example)

```
GBP playbook, question 4 of 10: for a client with several services, what address does each profile use, and why?
(One or two lines is plenty. I'll write it up and show you.)
```

## Done

Each answered heading has his process, dated. Every step that touches a Google rule has a quoted, dated rule and a compliant alternative. The log has every event the team saw.

## Never

- Recommend, plan or carry out a step that breaks a Google rule, or ask a vendor to.
- Create, claim, edit, verify, appeal or reinstate a listing.
- Use, buy or suggest bought or aged Gmail accounts. Touch reviews in any way.
- Copy the playbook outside `vault/`, into a draft, or into the repo.
- Ask two questions in one message.

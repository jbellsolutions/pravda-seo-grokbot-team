---
name: competitor-teardown
description: Channel Scout's one-page look at a competitor Oleg names. Use when Oleg (or the Chief, passing on his message) names a competitor or sends its link, for example the cold-email service he liked on Oct 21. Public pages only; never signs up.
---

# Competitor teardown

Load pravda-context first: `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

On Oct 21 Oleg asked Justin to look at a competitor (the name was unclear on the recording). He liked "how quick they had everything set up. Like, you know, you sign up and it starts tomorrow", and he found it "really weird" that it sent emails without asking him. He said he'd post the name; it isn't in yet (ask #44).

## Inputs

- The competitor's name or link: in `/workspace/pravda-team/requests/to-channel-scout/`, or in Oleg's own message passed on by the Chief. With no name or link, reply `NO_CLIENT_SOURCE: competitor name` and stop. Never guess which company he meant.
- Their public pages: home, pricing, how-it-works, terms, public reviews on public review sites.

## Steps

1. Confirm it's the right company. If two companies share the name, list both and ask Oleg which one, through the Chief.
2. Read their public pages. Note:
   - what they sell;
   - who it's for;
   - the published price;
   - what the client has to bring (lists, inboxes, approvals);
   - how fast they say they start;
   - what they do without asking the client.
3. Compare each point with how Oleg's teams work today: the Hermes partner campaign, and this team.
4. Write the teardown, then append it to `/workspace/pravda-team/data/channels/competitors.md`.

## Output format

```
## <Competitor> — <date read>
Sells: …   For: …   Price (as published): … <link> or UNKNOWN
How fast they start (their claim): … <link>
What the client must bring: …
What they do without asking: …
Worth copying honestly: 1. … 2. …
Not worth copying: … (for example: sending in his name without his yes)
Sources: <links>
```

Add a three-line summary to `/workspace/pravda-team/requests/to-chief/channel-scout-<date>-teardown.md`, starting with the line `For: Oleg`, so it reaches him in the Monday digest. Anything about the partner campaign goes in `channel-scout-<date>-partners.md` instead, starting with the line `For: Justin's team` (Hermes partner side).

## Done

One page per competitor. Every claim is linked or marked UNKNOWN, and it's in competitors.md.

## Never

- Sign up for a trial, book a demo, fill a form, contact the company or log in.
- Present their claims as fact. They're "their claim", with a link.
- Recommend copying anything that breaks pravda-context's rules.

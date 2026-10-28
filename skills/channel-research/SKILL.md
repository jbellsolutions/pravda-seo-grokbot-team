---
name: channel-research
description: Channel Scout's monthly research. Use in the monthly Channel memo run, or when Oleg asks "where else could clients or partners come from?". It writes one memo with three new channels, evidence and a small test each, and builds candidate lists from public pages only.
---

# Channel research

Load pravda-context first: `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Oleg, Sep 18: "I feel like AI can help me out with additional lead generations channels as well as additional partners." Oct 13: "we don't have that many, uh, lead generation options."

## Inputs

- Past memos: `/workspace/pravda-team/daily/*/channel-memo.md`. Never pitch a channel twice unless something about it changed, and say what.
- `/workspace/pravda-team/data/channels/`: past lists.
- `/workspace/pravda-team/context/asks.md`: new ideas Oleg has sent.
- `/workspace/pravda-team/requests/to-channel-scout/`: research requests in files not yet listed in `taken.md` there.
- Public web pages, public directories, public Google Maps listings.

## Where to look (seed list from the calls; never limited to it)

| Idea | Who raised it | Whose side a test would run on |
|---|---|---|
| GHL and CRM consultants, and their Facebook groups (some have about 500 clients) | Justin, Sep 15 | Partner side (Hermes), through Justin's team |
| Web hosting companies that list a recommended SEO partner on their site | Justin, Sep 15 | Partner side |
| Local business publications ("don't get too much cold email") | Justin, Sep 15 | Partner side or Authority Studio |
| Business brokers (a recent campaign of Justin's got about 20 replies) | Justin, Sep 15 | Partner side |
| Bookkeepers and CPAs ("the potential is huge", slow) | Oleg, Sep 15 | Partner side |
| Facebook groups and lectures for niches he served, like dentists and lawyers | Oleg, Sep 15 | Authority Studio (talks) |
| YouTube channels in his niches with large followings | Justin, Sep 15 | Authority Studio or partner side |
| Affiliate networks and media brokers, once there are conversion numbers | Justin, Oct 5 | Partner side, later |
| Emergency-dental and pay-per-call buyers and networks | Oleg, Sep 18 | Call Desk |

Out, always: SEO agencies; e-commerce and Shopify; national franchise marketing firms; anything outside the US; BNI and chambers of commerce (Oleg: "I've tried BNI. No, no.").

## Steps

1. Pick three channels that aren't in an earlier memo. Prefer ones tied to Oleg's own words or his niches (medical, dental, local service businesses).
2. For each, gather evidence from public pages:
   - what the channel is;
   - why it fits Oleg, in his words where possible;
   - a size estimate with its source, or UNKNOWN;
   - two to five links he can open.
3. Write one small test for each, something he can say yes or no to. Name what it needs (Oleg's time, a list, a talk, money with a sourced price) and who would own it.
   - Partner channels go to the Hermes side through Justin's team.
   - Talks and content go to Authority Studio.
   - Call buyers go to Call Desk.
   - Never give a duration estimate.
4. If a test needs a list, build `/workspace/pravda-team/data/channels/<YYYY-MM-DD>-<channel-slug>.csv`, at most 200 rows (starting value). Use the columns below.
   - Take business contact details only from the business's own website.
   - Never guess an email address.
   - Never use paid enrichment.
   - Skip any page behind a login, a block or a CAPTCHA, and count it as "blocked".
5. Write the memo to `/workspace/pravda-team/daily/<today>/channel-memo.md`.
6. Hand off:
   - Partner channels and lists, to `/workspace/pravda-team/requests/to-chief/channel-scout-<date>.md`, with "for Justin's team: Hermes partner side" on top.
   - Groups and talk venues, to `/workspace/pravda-team/requests/to-authority-studio/channel-scout-<date>.md`.
   - Call buyers and networks, to `/workspace/pravda-team/requests/to-call-desk/channel-scout-<date>.md`.
7. Add each request file you answered to `/workspace/pravda-team/requests/to-channel-scout/taken.md`. Never edit the request itself.

## Output format

Memo:
```
# Channel memo — <Month YYYY>
## 1. <Channel>
Why it fits: … (Oleg, <date>: "…")
Evidence: <links>   Size: <n, source> or UNKNOWN
Test: <what, how many, what it needs>   Owner: <Hermes side via Justin's team | Authority Studio | Call Desk | Client Desk>
List: data/channels/<file>.csv (<rows> rows) or none
## 2. …
## 3. …
Blocked or UNKNOWN this month: …
```

CSV columns: `business_name,website,city,state,category,contact_page,public_business_email,source_url,found_date,notes`. Leave `public_business_email` empty unless the address is published on their own site.

## Done

Three new channels, every claim linked, one test each with an owner. Every list row has a source URL. Handoffs are written. Nobody was contacted.

## Never

- Contact, join, follow, post in or sign up for anything.
- Use paid enrichment, or log in to see a page.
- Work around a block or a CAPTCHA.
- Start a test. Oleg says yes first, and the owning side runs it.

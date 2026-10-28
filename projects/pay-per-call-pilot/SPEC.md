# Project spec: the pay-per-call pilot (emergency dental first)

| | |
|---|---|
| Owner | Oleg |
| Bot | [Call Desk](../../agents/03-call-desk.md) (research, drafts, tracker). Oleg makes every decision and every contact |
| Asks | 41 (emergency-dental and pay-per-call leads, affiliate networks), 60 (his virtual numbers), 64 (partners, not clients) |
| Status | Specified. Research starts at milestone M5. The pilot itself starts only on Oleg's yes to the decisions below |
| Sources | Sep 18 call [44:57]–[53:21]; Oct 5 call [52:02]–[52:45]; Oct 21 call [33:51] |

## 1. The goal, in Oleg's words

- "I'm trying to see how I can generate more leads for emergency dental service, for example." (Sep 18 [44:57])
- "If this could be set up for dentists who don't advertise emergency dentals separately, this is a gold mine." And about the national networks that sell those calls: "Why do I need to pay to them?" (Sep 18 [52:05])
- "five years from now, I don't see myself working with. Clients, you know, I see myself working with partners" (Sep 18 [44:57])
- "what are some other emergency dental affiliate networks out there? Because the ones that I reach out, they seem to be not working" (Sep 18 [44:57])

His edge, as he describes it: he builds Google Business Profiles for practices that "start getting phone calls" fast, and for emergency dental he says nobody generates as many calls as he does (Sep 18 [44:57]).

**Done means:** one legitimate call source and one buyer, with written terms. Calls are counted from real exports. Oleg has the numbers to decide whether to scale, change or stop.

## 2. What "legitimate inventory" means here

The pilot runs only on calls that are honest at every step. A source is allowed when it is one of these:

1. **A real practice's own listing and website.** Its one profile, under its real name: emergency care is added to that profile and site, never split into a second profile. The practice operates at that address with staff in its listed hours, really offers emergency care, and has given written OK for tracking and for the pilot's terms. Oleg does the SEO; the money moves per call instead of, or on top of, a monthly plan *(inferred model)*.
2. **An honestly labelled referral website Oleg owns.** A website, never a Google Business Profile: a referral service with no staffed office at an address doesn't qualify for one under Google's rules. Callers are told they're reaching a referral service, and calls go only to practices that signed up *(inferred model; a compliance advisor checks it before anything is built, because some states regulate dental referral services (inferred))*.

Never, under any model:
- rank-and-rent;
- listings for businesses that aren't at the address;
- virtual or unit-number addresses;
- several listings for one business at made-up locations;
- a second Google Business Profile for the same business at the same address (for example a separate "Emergency" profile), or keywords added to a business's real name;
- reviews from accounts that aren't real patients.

Oleg said himself that rank-and-rent "mostly stopped working" outside a few categories because Google closed it (Sep 18 [50:03]).

## 3. Who buys

| Buyer type | Why | Source |
|---|---|---|
| Dental marketing agencies that already have dentist clients | Justin's advice: sell emergency-dental calls to them first, because they already hold the client relationships | Sep 18 call [52:21] |
| Emergency-dental, dental referral and pay-per-call networks | Oleg asked for ones beyond those he tried. The ones he tried go in `ppc.networks_already_tried` so they're never pitched again | Sep 18 call [44:57] |
| Dentists directly | Later. Dentists sign one-year contracts behind strong gatekeepers and are reachable mostly near renewal (Justin) | Sep 18 call [52:21] |
| Partners from the partner program | Later. Justin: the partner campaign also builds a database Oleg could sell calls to | Sep 18 call [51:21] |

The buyer map lives in `/workspace/pravda-team/data/ppc/buyers.md` ([skills/ppc-market-map](../../skills/ppc-market-map/SKILL.md)). Notes to buyers are drafts Oleg sends himself ([skills/ppc-buyer-outreach](../../skills/ppc-buyer-outreach/SKILL.md)).

## 4. Call tracking: his numbers, voice only

- Oleg owns about 7,000 phone numbers across virtual-number providers, and none of them can do text automation (Oct 5 [52:11]–[52:45]). Texting from them stays ⛔ (ask 60): bulk texts get numbers blocked.
- **Voice is different.** With his yes, each source and buyer pair gets its own tracking number from his existing numbers, so every call can be counted and billed to the right buyer *(inferred use)*.
- GHL numbers are the alternative. Justin put them at "maybe $1 or $2" a month (Oct 5 [52:04]); that's as stated, unverified.
- Grok Bot can't hold or answer numbers. Call Desk reads the call platform's exports (date, number, length) and logs them in `/workspace/pravda-team/data/ppc/pilot.md` ([skills/ppc-pilot](../../skills/ppc-pilot/SKILL.md)).
- **Call recording** happens only with a disclosure at the start of the call, checked with a compliance advisor first *(inferred)*.

## 5. Unit economics as stated (unverified)

Every figure here was said on a call. None has been checked with a buyer. Each stays "as stated, unverified" until a buyer confirms it in writing.

| Item | As stated | Who, when |
|---|---|---|
| Emergency-dental price per call | Not stated | UNKNOWN until a buyer quotes it |
| Rehab leads | About $600 each | Oleg, Sep 18 [50:03] |
| Personal injury, water damage | "Best-paying" niches, no figure | Oleg, Sep 18 [50:03] |
| Home-services calls (AC, roofing, plumbing, water damage, fire and mold, appliance repair) | $60–$100 a call, in a network of about 300 SEO agencies | Justin, Sep 18 [49:13]–[50:03] |
| Financial services, debt relief | Named as good niches, no figure | Justin, Sep 18 [51:21] |
| What Oleg pays now for bought leads (for comparison) | $15–$20 per reply (Sep 18); $25 per high-intent lead, closing 1 in 10 (Aug 6) | Oleg, Sep 18 [16:21]; Aug 6 [4:35] |
| Tracking numbers via GHL | "maybe $1 or $2" a month | Justin, Oct 5 [52:04] |

## 6. Decisions Oleg must make (in this order)

1. **Start now or after the first partner results?** Ask 41 was first planned for "after the first results". Call Desk's research can run either way; the pilot itself waits for his word.
2. **First niche:** emergency dental (recommended, since it's his stated edge) or another.
3. **Model:** per-call pricing on a real practice's own listing (model 1), an honestly labelled referral website (model 2), or both.
4. **Which networks he already tried,** so they're never pitched again.
5. **Numbers:** his existing virtual numbers (voice only) or GHL numbers.
6. **What makes a call count:** minimum length, new patient, inside the service area. This is agreed with each buyer in writing; Oleg agrees it, never the bot.
7. **Compliance check:** a compliance advisor reviews the model and call recording before the first call is routed.
8. **First buyer:** from the buyer map, after Oleg's own conversations.

Call Desk keeps this list in `/workspace/pravda-team/data/ppc/pilot.md` and records each answer in `/workspace/pravda-team/context/config.json` (`ppc.first_niche`, `ppc.model`, `ppc.networks_already_tried`, `ppc.tracking_numbers_source`, `ppc.call_counts_when`) through the Chief.

## 7. Milestones

| Stage | What happens | Depends on | Done when |
|---|---|---|---|
| P0 Research | Niche sheet and buyer map; drafts held until a niche is chosen | Team milestone M5 and Oleg's yes to turn Call Desk on | `niches.md` has a source or UNKNOWN for every figure; `buyers.md` lists buyers with evidence links |
| P1 Decisions | Oleg answers decisions 1–6 | P0 | The `ppc` fields in config.json are set in his words |
| P2 First buyer | Oleg sends the drafts he likes and talks to the buyers who answer | P1 | One buyer has confirmed in writing: price per call, what counts as a call, payment terms |
| P3 Source and compliance | One legitimate source passes every check in [skills/ppc-pilot](../../skills/ppc-pilot/SKILL.md); the compliance advisor has answered | P2, decision 7 | The source's check results and the advisor's answer are recorded in `pilot.md` |
| P4 Tracking test | One tracking number routes to a test line, and a test call shows up in the export | P3, Oleg's yes on decision 5 | The export shows the test call with date and length |
| P5 Pilot | Live calls from one source to one buyer; Call Desk logs every export | P4, Oleg's yes in words | `pilot.md` shows calls, counted calls and billed calls, each from an export |
| P6 Decide | Oleg looks at the numbers: scale, change or stop | P5 has enough calls for Oleg to judge | His decision and reason are in the vault's Decisions note (the Chief writes it) |

## 8. Never

- Contact a buyer, practice or network from a bot. Oleg sends every note.
- Create, claim, edit or verify a Google Business Profile.
- Rank-and-rent, or build a listing for a business that isn't at the address.
- Use virtual or unit-number addresses, or several listings for one business at made-up locations.
- Send texts from his virtual numbers.
- Buy leads or calls, sign up for a network, accept terms, sign or pay.
- Promise a buyer volume, quality or a price.
- Invent a call, a count, a price or a result.
- Use paid enrichment services.
- Write to GHL.

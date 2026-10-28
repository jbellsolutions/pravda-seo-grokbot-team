---
name: ppc-market-map
description: Call Desk's research skill for Oleg's pay-per-call idea. Use in the weekly Call Desk run, or when Oleg asks "who buys emergency dental calls?" or "what does a call pay in this niche?". It keeps the niche economics sheet and the buyer map, from public web pages only.
---

# Pay-per-call market map

Load pravda-context first: `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Oleg, Sep 18: "If this could be set up for dentists who don't advertise emergency dentals separately, this is a gold mine." He also asked, "what are some other emergency dental affiliate networks out there? Because the ones that I reach out, they seem to be not working." Justin's advice on the same call: sell emergency-dental calls first to dental marketing agencies that already have dentist clients, then to dentists directly.

## Inputs

- `/workspace/pravda-team/context/config.json` → `ppc.first_niche` (default for research: emergency dental), `ppc.networks_already_tried` (networks Oleg contacted that didn't work; if missing, ask Oleg through the Chief, one question).
- `/workspace/pravda-team/data/ppc/niches.md` and `/workspace/pravda-team/data/ppc/buyers.md`: your own sheets.
- `/workspace/pravda-team/requests/to-call-desk/`: leads from Channel Scout, in files not yet listed in `taken.md` there.
- Public web pages, public directories and public Google Maps listings.

## Steps

1. **Niches sheet.** Keep one row per niche. Start from what was said on Sep 18, and mark every figure "as stated Sep 18, unverified" until a buyer confirms it in writing:

   | Niche | What was said | Source |
   |---|---|---|
   | Emergency dental | Oleg: he can get practices calls from day one, "nobody can generate as many leads as me". No price per call was stated | Sep 18 call [44:57], [52:05] |
   | Rehab | Oleg: about $600 a lead | Sep 18 call [50:03] |
   | Personal injury | Oleg: among the best-paying. No figure | Sep 18 call [50:03] |
   | Water damage | Oleg: among the best-paying. Justin: home-services calls sold for $60–$100 a call in the network he knows | Sep 18 call [49:13]–[50:03] |
   | Financial services, debt relief | Justin added these. No figure | Sep 18 call [51:21] |

   For each row, add from public sources only: who buys, how a call is defined (minimum length, new patient, in area), Google-rules risk (does the inventory need anything pravda-context forbids?), Oleg's edge, and a verdict: `pursue`, `later` or `no`. Anything you can't source is `UNKNOWN`.
2. **Buyer map.** Research up to 10 new buyers per run, in this order:
   - (a) dental marketing agencies whose own website shows dentist clients or dental case studies;
   - (b) emergency-dental and dental referral networks, and pay-per-call networks with a public buyer or publisher page;
   - (c) dentists directly, later and only when Oleg says so.

   Skip any buyer in `ppc.networks_already_tried`. Skip anything behind a login, a block or a CAPTCHA, and list it as "blocked".
3. For each buyer, write one row: name; type (a, b or c); website; city and state; the evidence of fit (a link to the page that shows it); the public business contact page; status (`new`, `drafted`, `sent by Oleg`, `replied`, `talking`, `no`, `Hermes side`); the date read.
4. Once a Channel Scout file's buyers are in the map, add the file name to `/workspace/pravda-team/requests/to-call-desk/taken.md`. Never edit the handoff itself.
5. Write three lines for the Chief in `/workspace/pravda-team/daily/<today>/call-desk.md`: buyers added, the strongest one and why, and anything blocked or UNKNOWN.

## Output format

`niches.md` and `buyers.md` are markdown tables with the columns above. Every figure has a source next to it.

## Done

Each niche has a source or UNKNOWN for every figure and a verdict. Each buyer has a link that proves the fit. Nothing was contacted.

## Never

- Contact a buyer, practice or network, or sign up for a network.
- Use paid enrichment services or pages behind a login.
- Turn "as stated" into a fact without a buyer's written confirmation.
- Plan inventory that needs a listing at an address where the business doesn't operate, a rank-and-rent listing, or texts from Oleg's virtual numbers.

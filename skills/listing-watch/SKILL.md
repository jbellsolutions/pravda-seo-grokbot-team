---
name: listing-watch
description: The weekly public check of every client Google Business Profile listing on the watchlist. Is it still live, and did its name, category, rating or review count change? A listing that's gone, closed or suspended gets a same-day alert to Oleg. Use in the Listing check routine, or when Oleg asks "is <client>'s listing still up?". Maps Desk only.
---

# Listing watch

Load pravda-context first: read `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Work only in `/workspace/pravda-team/`. Maps Desk is the only writer of `data/listings.md` and `daily/<date>/listing-check.md`.

**Where this comes from.** Oleg says listings and reviews get removed "for no reason", so he keeps changing vendors and verification methods (Sep 18). Ask #70.

## Inputs

- `/workspace/pravda-team/data/listings.md`: the watchlist.
- `/workspace/pravda-team/requests/to-maps-desk/`: new listing URLs from Client Desk. Add them to the watchlist before checking, then add the file name to `requests/to-maps-desk/taken.md`. Never edit the handoff itself.
- Public Google Maps listing pages, opened in the browser **signed out**.

If the watchlist is empty and Client Desk has given no URLs, reply `NO_CLIENT_SOURCE: listing URLs` and stop.

## The watchlist format

```
# Listings (sole writer: Maps Desk)
| Client | Listing (as shown) | Public URL | Last check | Status | Name | Category | Rating | Reviews | Notes |
|---|---|---|---|---|---|---|---|---|---|
| Example Dental | Example Dental | <maps URL> | 2026-11-02 | live | Example Dental | Dentist | 4.8 | 212 | |
```

**Status** is one of: `live`, `changed`, `closed` (Google shows "permanently closed" or "temporarily closed"), `gone`, or `UNKNOWN`.

## Steps, per listing

1. Open the public URL, signed out. Read the name, primary category, rating, review count, and any "closed" label.
2. Compare with last week's row.
   - Same: `live`.
   - Name, category, or a review count that fell: `changed`, saying what changed (old → new).
   - A review count that rose: still `live`, noted.
3. If the page says the place isn't found, or the URL lands somewhere else, open it once more and search Maps for the business name and city. Mark `gone` only if both say so, or a Google notice in Gmail says so. Otherwise it's `UNKNOWN`.
4. If a page shows a block, a sign-in wall or a CAPTCHA, stop for that listing, mark it `UNKNOWN (blocked)`, and don't try to get around it. If two listings in a row are blocked, stop the whole run and say so.
5. Update the row. Write `daily/<date>/listing-check.md`: totals, then every listing that isn't plain `live`.
6. **Same-day alert to Oleg** only for `gone` or `closed`. Everything else waits for the Chief's Monday digest.

## Alert to Oleg (example)

```
Listing alert: Example Dental is gone from Google Maps (checked twice at 7:13 and 7:20 AM, search for the name in the city finds nothing).
Last seen live: Oct 26, 4.8 stars, 212 reviews.
Worth checking in your Business Profile dashboard. I've logged it in the GBP log.
```

Also append the event to `/workspace/pravda-team/data/gbp-log.md`: date, client, listing, what was seen, "Oleg told".

## Done

Every listing on the watchlist has this week's status. Every `gone` or `closed` listing reached Oleg the same day and is in the GBP log. No listing was called gone on one failed load.

## Never

- Sign in to Google, open the Business Profile manager, or use any account.
- Report, suggest an edit, appeal, or reinstate anything.
- Contact a client, a vendor or Google.
- Get around a block or CAPTCHA.
- Share a client's listing outside the workspace.

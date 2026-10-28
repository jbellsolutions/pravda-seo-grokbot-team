---
name: client-roster
description: Build and keep Oleg's client roster in /workspace/pravda-team/data/clients.md. It records each client's plan, start date, listings and where their rank reports come from. Use at intake (M3), when Oleg says a client started, left or changed plan, and before every client pulse. Client Desk only.
---

# Client roster

Load pravda-context first: read `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Work only in `/workspace/pravda-team/`. Client Desk is the only writer of `data/clients.md`.

## Inputs

- Oleg's client list. He gives it to the Chief at intake (OPEN_QUESTIONS #3), as a forwarded email, a spreadsheet he attaches, or a typed list, and the Chief hands it over in `/workspace/pravda-team/requests/to-client-desk/chief-<date>.md`. Later changes come the same way, or straight from Oleg. If nothing has been given, every field below is `REQUIRED`. Reply `NO_CLIENT_SOURCE: client list` and stop.
- `/workspace/pravda-team/context/owner.md`, for his facts.
- `/workspace/pravda-team/data/listings.md` (Maps Desk), to see which listings are already on the watchlist.

## The roster format

```
# Clients (sole writer: Client Desk) · last confirmed by Oleg <date>

| Client | Plan ($/mo) | Since | Website | Listing URLs | Report source | Contact (on file in owner.md) | Status | Notes |
|---|---|---|---|---|---|---|---|---|
| Example Dental (Example only) | 300 | 2012 | example.com | 2 listings | Local Falcon export, monthly | yes | active | complained Mar 2026 → no asks |
```

- **Plan** is the monthly price Oleg says the client pays. If he doesn't say, `UNKNOWN`.
- **Since** is the year or month the client started. It drives the price review.
- **Report source** is where this client's rank report comes from: Local Falcon export, his own tool, or none.
- **Status:** `active`, `paused` or `left`. Clients who left stay on the roster, marked `left`, and are never asked for anything.
- **Notes** holds only what changes how the team treats the client: a complaint, a late invoice, "don't ask". Oleg's word, with the date.

## Steps

1. Read Oleg's list. Write one row per client. Never guess a field; write `REQUIRED` or `UNKNOWN`.
2. Read the roster back to Oleg in one short message. Ask about one missing field at a time, starting with what blocks the most: listing URLs first, then report source, then plan and start date.
3. Hand new listing URLs to the Maps Desk: write `/workspace/pravda-team/requests/to-maps-desk/client-desk-<date>.md` saying "new listings for the watchlist: <client> <URLs>". The Maps Desk alone writes `data/listings.md`.
4. When Oleg says a client started, left or changed plan, update that row, write the date and his words in **Notes**, and tell him in one line what changed.

## Message to Oleg (example)

```
Your client list: 23 clients, 19 active. Missing: listing links for 6, report source for 4.
First question: for Example Dental, what's the Google Maps link to their listing?
```

## Done

Every active client has a plan, a start date, at least one listing URL and a report source, or a clear `REQUIRED` that Oleg has been asked about. Oleg has said "right" to the readback.

## Never

- Invent or look up a client's price, start date or contact.
- Copy client names, emails or phone numbers anywhere outside the workspace.
- Write `data/listings.md`. That's the Maps Desk's record.
- Contact a client.

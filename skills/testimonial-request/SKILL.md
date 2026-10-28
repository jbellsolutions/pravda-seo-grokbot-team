---
name: testimonial-request
description: After a client has seen a real win, draft a permission-first testimonial or case-study request for Oleg to send, and hand what the client agrees to over to Authority Studio's proof library. Use in the Win asks routine, or when Oleg says "ask <client> for a testimonial". Drafts only. Client Desk only.
---

# Testimonial request

Load pravda-context first: read `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Work only in `/workspace/pravda-team/`. Client Desk is the only writer of `approved/pending/testimonials/` and `requests/to-authority-studio/client-desk-<date>.md`. Authority Studio alone writes the proof library, `data/proof/index.md`.

**Where this comes from.** Oleg wants proof that he's "not just another startup SEO company" (Aug 6), and has video testimonials, client results and Google reviews he'd like used (Aug 6, Sep 15). New proof has to be real and permitted. Ask #20.

## Inputs

- `/workspace/pravda-team/data/wins.md`: wins with evidence, and whether the client has seen them.
- `/workspace/pravda-team/data/clients.md`: status and notes.
- `/workspace/pravda-team/data/proof/index.md` (Authority Studio): to avoid asking a client who already gave proof this year.
- Gmail, read-only: the client's reply, once Oleg has sent the request.

## Who gets a request

The same tests as `client-referral-ask`: a logged win the client has seen, an active client with no complaint or late invoice, and no ask of any kind (referral or testimonial) to that client in the last 90 days. If a client qualifies for both, draft the referral ask first and offer the testimonial request for the next win, unless Oleg says otherwise.

## Steps

1. Draft the request below and save it to `/workspace/pravda-team/approved/pending/testimonials/<date>-<client>.md`, with the win's evidence underneath (not part of the email).
2. Send it to Oleg with the run's other drafts. He sends from his own email, or doesn't.
3. When the client replies (Gmail, read-only), record **exactly** what they agreed to:
   - the words they wrote, or the file they sent;
   - whether their **name**, **business name**, **photo** and **numbers** may be shown;
   - where it may appear (website, proof page, emails).
4. Write the handoff to `/workspace/pravda-team/requests/to-authority-studio/client-desk-<date>.md`: their words verbatim, what they permitted, the date and the email it came from. Mark it "Oleg OK'd: yes/no". Authority Studio uses nothing that isn't marked yes.
5. If the reply is unclear about permission, the handoff says "permission unclear". Draft a one-line follow-up for Oleg asking the client to confirm.

## The request (Example only: fill the brackets from the record)

```
Subject: Could I share your results?

Hi [first name],

I'm really pleased with how [the win in plain words] turned out.
Would you be willing to say a few words about working with us? Two or three sentences in a reply is plenty. If you'd rather, a short phone video works too.

I'll only use what you send, and only the way you say. Just tell me if I may use your name and business name, or if you'd rather stay anonymous.

Thank you,
Oleg
Pravda SEO
```

Rules for the draft: never write the testimonial for the client, never suggest words for them to say, never offer anything in return.

## Message to Oleg (example)

```
1 testimonial request ready (Example Dental, top 3 on Maps since Oct). Draft: approved/pending/testimonials/.
Send it if it looks right.
```

## Done

Every request was a draft Oleg sent himself. Every handoff to Authority Studio holds the client's own words and exactly what they permitted.

## Never

- Write, edit or "polish" a client's testimonial.
- Hand over anything the client didn't clearly permit.
- Write to `data/proof/index.md`.
- Contact a client.

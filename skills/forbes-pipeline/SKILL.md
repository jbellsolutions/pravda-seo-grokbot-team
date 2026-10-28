---
name: forbes-pipeline
description: Run Oleg's Forbes Business Council article pipeline. Keep a topic bank from his calls and notes, turn the topic he picks into an outline, then a draft in his voice from his own notes, which he edits and submits himself. Use for the weekly Authority piece when it's a Forbes piece, or when Oleg says "let's write about…". For Authority Studio.
---

# Forbes pipeline

Load pravda-context first: `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

Oleg doesn't want podcasts or on-camera work ("I'm not good at public speaking", Aug 6). He wants to be known for publishing. He's a Forbes Business Council member with about 10–12 articles, and some rank in Google News and bring him clients. His Sep 25 article was on local growth alliances and the recurring revenue they create.

## Inputs

- `/workspace/pravda-team/data/forbes/pipeline.md`: the topic bank and the status of each piece. You're its only writer.
- Oleg's own words: `/workspace/pravda-team/vault/Calls/` and `vault/Records/`, filed by Chief.
- His published Forbes articles: public pages. Read them for his voice and to avoid repeating a topic.
- `/workspace/pravda-team/data/proof/index.md`: only OK'd items may be cited.

## The pipeline file

| # | Topic | Why him (his experience, in his words, with source) | Status | Next step |
|---|---|---|---|---|
| F-01 | … | "…" (Sep 18 call) | idea / Oleg picked / outline / draft / with Oleg / submitted by Oleg / published | … |

**Starting topic ideas, from his calls.** Each needs his pick before it's outlined:
- Why local businesses get more from referral partners than from ads: the theme of his Sep 25 article, taken further.
- What a medical practice should know about Google Business Profiles in its niche, in the compliant form only. It's his specialty.
- How to judge an SEO agency before signing: the theme of his "choose your SEO agency carefully" VSL.
- What changes for local businesses when AI answers search questions (inferred from his Oct 13 question about AI in his niche).

## Steps

1. **Topic bank.** Add ideas from what Oleg says on calls and in email. Each idea needs a line of his own experience with its source. Without one it's not his article.
2. **Pick.** Oleg chooses a topic. Ask him through the Monday digest, as a choice of up to three. Never pick for him.
3. **Outline.** A headline, a three-sentence point, five to seven sections, and the one story or number from his own work that carries it. Cite the source of that story or number.
4. **Draft, only after he OKs the outline.** Write in his voice: plain, direct, teaching rather than selling, short sentences. Write from his notes and calls. Where the draft needs his experience and the notes don't have it, leave `[Oleg: your example here]`. Never fill it in.
5. **Hand over.** Save it to `approved/pending/forbes/<slug>.md` and list it for the Monday digest: "Draft ready for your edit. You submit it." Mark it `with Oleg`.
6. **After he says he's submitted or published it,** record the date and link, and add the article to the proof library as `not yet` until he OKs it for use elsewhere.

## Output

- `data/forbes/pipeline.md`.
- `approved/pending/forbes/<slug>.md`: the outline or the draft, with every fact cited.
- One line in `daily/<date>/authority-studio.md`.

## Done

- One topic moves one step per piece.
- Every story and number in a draft has a source or an `[Oleg: …]` gap.
- Oleg did the submitting.

## Never

- Submit to Forbes, publish, post or email an article to anyone.
- Invent a story, a client result, a statistic or a quote.
- Copy text from other authors' articles.
- Turn an article into LinkedIn posts or newsletters: the Hermes agents do that from his published pieces.
- Plan podcasts, interviews or live talks.

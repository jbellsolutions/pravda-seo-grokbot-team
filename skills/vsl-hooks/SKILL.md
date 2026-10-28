---
name: vsl-hooks
description: Write rounds of hook rewrites for Oleg's two VSLs (the company one for customers and incoming leads, the personal one for partners) in a conversational voice, on the problem-cost-consequence-solution-mechanism-proof-price structure. Use for the weekly Authority piece when it's a VSL round, or when Oleg sends a new VSL version. For Authority Studio.
---

# VSL hooks

Load pravda-context first: `/workspace/pravda-team/repo/skills/pravda-context/SKILL.md`.

On Sep 18 Oleg read his script and said: "I don't see a good enough hook, to be honest. Like, I'm reading it and I'm not hooked on it." The verdict that day:
- **The company VSL** (professionally produced, built on "Local Lead Multiplier") is for customers and incoming leads, including the leads he buys.
- **The personal VSL** (written with ChatGPT, roughly "choose your SEO agency carefully") is for partner outreach and authority.

On Sep 15 he also asked to "combine it with a presentation" [17:06], and Justin agreed. So once Oleg picks a hook, add a short slide outline for that VSL (one line per slide, same structure), saved beside the round (ask #78).

Justin's advice was a more conversational delivery with the same structure: problem, cost, consequence, solution, unique mechanism, proof, price. He also said "Local Lead Multiplier" sounds generic. No better name was chosen.

## Inputs

- The latest version of each script Oleg shared, read from Gmail or Drive (read-only), or from `/workspace/pravda-team/data/vsl/` if Chief saved it there. If neither is available, write `NO_CLIENT_SOURCE: VSL scripts` and ask Chief to request them once.
- Earlier rounds in `/workspace/pravda-team/approved/pending/vsl/`, so you never repeat a hook.
- `/workspace/pravda-team/data/proof/index.md`: only OK'd proof.

## Steps

1. Pick the VSL for this round, alternating unless Oleg asked for one.
2. Read the current opening (the first 30 seconds of script) and name in one line why it doesn't hook. Quote the line.
3. Write **three hooks**, each a different angle:
   - **a. Problem the viewer already feels.** For customers: calls that don't come from Google Maps. For partners: their clients ask who does SEO.
   - **b. A cost or consequence in plain numbers.** Use only numbers from OK'd proof or his own words with a date. Otherwise use labelled example math.
   - **c. A surprising truth from his 19 years** that teaches something.

   Each hook is 2–4 spoken sentences, conversational and in his voice, short enough for him to read aloud comfortably.
4. Under each hook, show how it flows into the rest of the structure: problem → cost → consequence → solution → unique mechanism → proof → price. One line each, with the proof IDs used.
5. If Oleg wants a new name, offer up to three, each with the reason it's specific to him. He decides.

## Output

`approved/pending/vsl/<date>.md`:

```
VSL: company (customers) · round 3
Why the current opening doesn't hook: "<quoted line>" — <one line>
Hook A — <angle>: "<2–4 sentences>"
  → problem … → cost … → consequence … → solution … → mechanism … → proof [P-003] → price "plans from $300"
Hook B — …
Hook C — …
```

Then list the round in your daily note for the Monday digest. When Oleg opens this chat, ask: "Three hooks for your <company/partner> VSL. Pick one, or tell me what's off."

## Done

- Three distinct hooks.
- Every number or proof is sourced or labelled as an example.
- The round is saved, and the request is sent.

## Never

- Promise rankings, call volumes or income.
- Use proof Oleg hasn't OK'd.
- Record, edit or publish video.
- Write partner emails or newsletters from the VSL: the Hermes agents own partner content.

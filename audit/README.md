# Assistant Visibility Audit

The before picture. Thirty questions a real customer would ask, run through the
assistants people actually use, recorded exactly as they came back.

It answers one question an owner has never had answered: **when someone asks an AI
assistant for a business like mine, do I show up, and is what it says about me
even true?**

## Why this exists

The briefing in this repo argues that commerce is moving toward agents. That is an
argument about the future, and arguments about the future are easy to nod along to
and forget. The audit is the same argument with evidence attached, about a business
the owner cares about, dated today.

It is also the honest version of the pitch. Agent-driven revenue for a local
business in 2026 is close to zero, and anyone claiming otherwise is selling.
What the audit finds instead is real now: wrong hours, stale ratings, missing
services, unverifiable credentials. That costs customers today, through every
channel, and fixing it happens to be the same work that matters later.

Lead with what is broken now. Let the future be the reason it is worth doing
properly rather than cheaply.

## Running one

Budget an afternoon for the first. The tenth takes about an hour.

### 1. Write the question set — before looking at their website
Thirty questions across the seven types in [`query-sets.md`](query-sets.md).
Writing them first matters: research the business first and the set gets built
around what they already say well, which flatters instead of measures.

### 2. Establish ground truth
Hours, service area, full service list, licenses, current review rating, pricing if
any is published. This is what the assistants' claims get checked against. Without
it there is no accuracy number, and the accuracy number is what makes an owner sit
up.

### 3. Run every question through every assistant
ChatGPT, Claude, Gemini, Perplexity, Google AI Mode. Five is enough.

- **Fresh session every time.** No history, no memory, no logged-in account.
  Personalization contaminates the result.
- **Screenshot everything.** The screenshots are the deliverable's credibility.
  An owner who does not believe the summary will believe the screenshot.
- **Record verbatim.** Do not paraphrase what the assistant said about them.

For each answer record: was the business named, what position among the options,
and every factual claim made about it.

### 4. Compute three numbers
- **Appearance rate.** Answers naming the business ÷ total answers.
- **Average placement.** Mean position when named.
- **Accuracy rate.** Appearances with zero wrong claims ÷ total appearances.

Three numbers, because an owner will hold three in their head and act on them.

### 5. Build the report
Copy `report.html`, replace the `D` object, open it in a browser, print to PDF.
Self-contained, works offline, prints clean.

### 6. Deliver it in person, free, the first several times
You are not selling on this call. You are watching whether the owner says "huh" or
"how do I fix that." Only the second reaction is a business.

## What to actually watch for

The finding that lands hardest is almost never the appearance rate. It is a
specific, checkable wrong fact: an assistant telling a customer they are closed
Saturdays when they are open, or citing a rating a half-star below the real one.
Abstract invisibility is arguable. A wrong fact is not.

Second hardest: a real service line that appears in zero answers. The owner knows
they do tankless installs. Discovering that nothing on the internet knows it is a
specific, fixable, obviously-costly gap.

## Files

| File | What it is |
|------|-----------|
| [`query-sets.md`](query-sets.md) | How to build the thirty questions. The seven types, a worked example, and the rules that keep a re-run comparable. |
| [`report.html`](report.html) | The deliverable. Self-contained, renders from a `D` object, matches the briefing's design. Ships with a clearly-labelled sample. |

## Before this gets automated

It should not be, yet. Run it by hand on three real businesses first. Doing it
manually is how the question set gets good and how it becomes clear which findings
actually move an owner. Automating a process nobody has validated produces a fast,
repeatable way to generate something no one wants.

The re-run is the first thing worth automating, and only once somebody is paying
for one.

## Honesty rules

These are not optional. The warm network is the only real asset here, and it
survives exactly one overstated claim.

1. **Never present a projection as a measurement.** The audit reports what the
   assistants said. It does not estimate lost revenue.
2. **Never imply agents are driving meaningful revenue today.** They are not. The
   briefing's own number is 0.2% of e-commerce.
3. **Verify before reporting an error.** An assistant contradicting the business's
   own website is a finding. An assistant contradicting an assumption is not.
4. **Re-runs use the frozen question set.** Changing questions between runs and
   presenting the delta as improvement is fabrication.
5. **Label sample data as sample data.** The `sample` flag in `report.html` prints
   a banner. Leave it on until the numbers are real.

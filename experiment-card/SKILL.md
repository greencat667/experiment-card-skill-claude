---
name: experiment-card
description: >
  Turn an idea into testable assumptions, find the riskiest one, and design the cheapest experiment that could prove it wrong — with success and kill thresholds set before any data comes in. Then, when results arrive, complete a learning card and make an explicit persevere / pivot / kill decision. Triggers on: "experiment card", "test card", "learning card", "riskiest assumption", "assumption mapping", "what should we test first", "how do we test this idea", "design an experiment", "lean experiment", "validate this idea", "MVP test", "smoke test", "fake door test", "pre-mortem this experiment", "we ran the test, what now", "persevere or pivot". Use for new products, services, programmes, campaigns or internal tools — anything where acting on an untested belief is expensive. Different from options-paper (choosing between known options) and project-brief (planning delivery of something already decided) — this is for finding out whether the idea deserves either.
---

# Experiment Card

Most ideas fail for a reason someone could have tested cheaply in the first fortnight. This skill finds that reason before you build anything.

It works in two modes:

- **Design mode** (default) — idea in, experiment cards out. Surfaces the beliefs the idea depends on, maps them by importance and evidence, picks the riskiest, and designs the cheapest test that could prove each one wrong.
- **Learning mode** — the user comes back with results. Complete the learning card against the thresholds set in advance, make a persevere / pivot / kill call, and name the next riskiest assumption.

Detect the mode from the request. If the user shares results, data or "we ran it", use learning mode and ask for the original experiment card if it isn't in the conversation or the working folder.

## Principles

These are non-negotiable, because each one exists to stop a common way experiments lie to you:

1. **Thresholds are set before the test.** Success and kill thresholds are written on the card before any data exists. In learning mode, never move them after seeing results — if the threshold was wrong, say so and note it for the next card.
2. **Behaviour beats opinion.** What people *do* (sign up, pay, show up, come back) is strong evidence. What they *say* they'd do is weak evidence, because stated intention reliably overstates action. Grade every piece of evidence using `references/evidence-ladder.md`.
3. **Synthetic feedback is not evidence.** Reactions from AI personas, including a persona panel, can help sharpen questions or spot confusing copy. They count as zero evidence for whether real people want something. Say so plainly if the user tries to use them that way.
4. **Cheapest test that could change the decision.** Not the cheapest test, and not the most rigorous — the cheapest one whose result would actually make you stop, change or continue.
5. **One card, one assumption.** A test that checks three things at once can't tell you which one failed.

## Design mode

### Step 1 — Frame the idea

Write the idea as one sentence:

> **For** [who] **who** [situation or need], **[idea]** **will** [change we expect], **unlike** [what they do today].

If the user's description is vague, draft this sentence and ask them to correct it. Also capture: who is deciding whether to go ahead, what's already been spent or committed, and the date the decision is needed. The decision date sets how much testing time exists.

### Step 2 — Surface assumptions

List **15–25 assumptions** the idea depends on, each phrased as **"We believe that…"**. Cover five lenses, at least two assumptions each:

| Lens | The question it asks |
|---|---|
| **Desirability** | Do the people it's for want it enough to change what they do? |
| **Feasibility** | Can we actually deliver it, with the skills, partners and time we have? |
| **Viability** | Can it be paid for and sustained after any start-up money runs out? |
| **Impact** | If it works as a service, does it produce the change we actually care about? |
| **Equity & harm** | Who is left out or put at risk, and does it shift burdens onto people with less power? |

Good assumptions are specific and falsifiable. "People like sharing" is not an assumption; "Renters without a car will book a delivered tool rather than borrow one from a neighbour" is.

Hunt especially for the **hidden** assumptions — the ones so obvious to the team they never get said. Useful prompts: *What has to be true about timing? About trust? About who does the unpaid work? About what people do today instead?*

### Step 3 — What do we already know?

For each assumption, record the existing evidence and grade it on the evidence ladder (`references/evidence-ladder.md`, grades 0–5).

- Search for real evidence: published studies, statistics, the experience of comparable schemes or products, the user's own data. Cite with links. Never invent evidence.
- Most assumptions about a new idea will sit at grade 0–1. That's normal and is the point of the exercise.
- Note where evidence exists but comes from a different context (another country, a different audience). That lowers its weight.

### Step 4 — Map and pick

Score each assumption on **importance**: *if this turns out to be false, what happens to the idea?*

- **5** — the idea dies
- **3** — the idea needs a major redesign
- **1** — a detail changes

Plot importance against evidence grade in a table or a simple 2×2 (important and unknown · important and known · less important and unknown · less important and known). The **riskiest assumptions** are high importance, low evidence. Pick the top **1–3** to test first. Explain the choice in two or three sentences, and name any high-importance assumption you're deliberately *not* testing yet, and why.

Also flag any **leap-of-faith assumption** — one that is both critical and very hard to test cheaply. Those usually need a staged approach: test a proxy now, the real thing later.

### Step 5 — Design the test

For each riskiest assumption, choose a test method from `references/test-methods.md`. Start at the cheapest rung that could produce evidence strong enough to change the decision, and only climb if it couldn't.

Write one **experiment card** per assumption using the template in `references/card-templates.md`:

- **We believe that** — the assumption, verbatim
- **To test it, we will** — the method, concretely: who, how many, where, what they'll see or be asked to do
- **And measure** — one primary metric, defined precisely enough that two people would count the same result
- **We're right if** — the success threshold, a number
- **We'll stop or rethink if** — the kill threshold, a number. Leave a gap between the two; results in the gap mean "inconclusive — decide what to do next".
- **Evidence grade this would give us** — on the ladder
- **Cost, time, owner** — money, days, and one named role
- **What we'll do with each result** — a line each for success, kill and inconclusive

Choosing thresholds: base them on what would make the idea worth continuing, not on what feels achievable. If the idea needs 30% of households to take part to break even, a 10% success threshold tells you nothing useful. Where you have no basis for a number, say so, use a comparable benchmark if one exists, and mark the threshold as provisional.

Sample size: be honest about what small numbers can show. Eight usability sessions can reveal whether people can use something and what confuses them; they can't estimate what share of a population will adopt it. Match the claim to the method.

### Step 6 — Pre-mortem the test

Imagine it's the end of the test and the result was useless — ambiguous, or misleading. Write 3–5 reasons why. Common ones: the wrong people took part, the metric could be gamed, the test was too small to separate signal from noise, something else changed at the same time, people behaved differently because they knew they were being watched, the offer was too polished or too rough to be realistic.

Fix what you can on the card. Record what you can't under **Known limits**.

### Step 7 — Critique

Before handing over, check every card against these questions and fix any failures:

- Could this result actually change the decision? If both outcomes lead to "carry on", the test is theatre.
- Is the primary metric behaviour, not opinion, wherever that's possible?
- Are both thresholds numbers, set now, with a gap between them?
- Does the test check one assumption, not several?
- Is anyone put at risk, misled or disadvantaged by the test? Fake-door and Wizard-of-Oz tests must tell participants the truth afterwards, must not take money for something that doesn't exist, and must not collect personal data beyond what's needed.
- Is there a cheaper rung that would have been enough?

### Output

Write **`experiment-cards-[slug].md`** in the user's working folder, structured as:

1. The idea (the one-sentence frame, decision owner and date)
2. Assumption map (table: assumption · lens · evidence · grade · importance)
3. Riskiest assumptions and why (plus any deliberately deferred)
4. Experiment cards (one per riskiest assumption)
5. Pre-mortem and known limits
6. Blank learning cards, ready to complete
7. Sources

## Learning mode

When results come in:

1. **Restate the card**, including the original thresholds. Don't edit them.
2. **Report what happened** — the numbers, plus anything surprising that people did or said. Separate observations ("7 of 10 abandoned at the delivery-fee screen") from interpretations ("the fee is too high").
3. **Compare to thresholds** — success, kill, or inconclusive. State it in one line.
4. **Grade the new evidence** on the ladder, and update the assumption map.
5. **Decide**, and say why:
   - **Persevere** — the assumption held; move to the next riskiest one
   - **Pivot** — the assumption failed but a nearby version might hold; name the new assumption and design its card
   - **Kill** — a critical assumption failed and no nearby version looks promising; say what the team learned and what it saves by stopping now
   - **Re-run** — only if the test itself was broken (not just disappointing), with the fix named
6. **Name the next riskiest assumption** and draft its card.

Write or update **`learning-cards-[slug].md`**. Be honest when results are disappointing — the value of a kill decision is the money and time it saves, and saying so plainly is part of the job.

## Handoffs

If these skills are installed, offer the natural next step:

- **rapid-prototype** — when the chosen test needs a clickable prototype or a fake-door page
- **persona-panel** — to pressure-test interview questions or prototype copy *before* testing with real people (not as evidence)
- **options-paper** — when the experiments have narrowed things to a real choice
- **project-brief** — when an idea has passed its riskiest tests and is ready to plan properly

## Files

| File | Purpose |
|---|---|
| `SKILL.md` | This process |
| `references/evidence-ladder.md` | How to grade evidence, 0–5 |
| `references/test-methods.md` | Test methods from cheapest to most expensive, and when each fits |
| `references/card-templates.md` | Experiment card and learning card templates |
| `examples/tool-delivery-experiment-cards.md` | A complete worked example |

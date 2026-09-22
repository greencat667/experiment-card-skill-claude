# Experiment Card

A skill for [Claude Code](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview) and [Cowork](https://claude.ai) that turns an idea into testable assumptions, finds the riskiest one, and designs the cheapest experiment that could prove it wrong. It sets success and kill thresholds *before* any data comes in. When results arrive, it completes a learning card and makes an explicit persevere / pivot / kill call.

## What it does

**Design mode** (idea in, experiment cards out):

1. **Frames the idea** in one sentence: for whom, what change, unlike what they do today
2. **Surfaces 15–25 assumptions** across five lenses: desirability, feasibility, viability, impact, and equity & harm, hunting especially for the ones too obvious to say out loud
3. **Checks what's already known**, with real cited evidence graded on a 0–5 evidence ladder, where behaviour beats opinion and synthetic personas count as zero
4. **Maps importance against evidence** to pick the 1–3 riskiest assumptions
5. **Designs one experiment card per assumption**: method, one primary metric, success and kill thresholds with a gap between them, cost, time, owner, and what you'll do with each result
6. **Pre-mortems each test**: "the result was useless — why?"
7. **Critiques the cards**: would the result actually change the decision? Is anyone misled or put at risk?

**Learning mode** (results in): restates the original thresholds without moving them, separates observations from interpretation, compares against the thresholds, re-grades the evidence, makes the call, and drafts the card for the next riskiest assumption.

See [`examples/tool-delivery-experiment-cards.md`](experiment-card/examples/tool-delivery-experiment-cards.md) for a complete worked example: a doorstep tool-delivery idea for renters without cars, with real evidence behind the assumption map.

## Installation

**Ask Claude to set it up for you.** If you're using Claude Code or Claude Cowork, you can just say something like *"install the experiment-card skill from github.com/greencat667/experiment-card-skill-claude"* and Claude will clone the repo and put it in the right place. You don't need to do this by hand.

Or do it yourself: copy the `experiment-card/` folder into your project's `.claude/skills/` directory:

```bash
git clone https://github.com/greencat667/experiment-card-skill-claude.git
cp -r experiment-card-skill-claude/experiment-card/ your-project/.claude/skills/experiment-card/
```

Claude will pick it up automatically the next time you start a session.

## Example prompt

Once installed, just ask Claude something like:

> "We want to start a repair-skills evening class for young people at our community centre. What's the riskiest assumption, and how could we test it in the next month for under £200?"

And later:

> "We ran experiment 1. 14 people signed up on the waiting list from 300 flyer scans, and 3 turned up to the taster. What now?"

## Pairs well with

- [rapid-prototype](https://github.com/greencat667/rapid-prototype-skill-claude) — when the test needs a clickable prototype or a fake-door page
- [scenario-builder](https://github.com/greencat667/scenario-builder-skill-claude) — its no-regret moves make good ideas to test
- [persona-panel](https://github.com/greencat667/persona-panel-skill-claude) — to rehearse interview questions before real sessions (not as evidence)
- [options-paper](https://github.com/greencat667/options-paper-skill-claude) and [project-brief](https://github.com/greencat667/project-brief-skill-claude) — once an idea has passed its riskiest tests

## Repository structure

```
experiment-card-skill-claude/
├── experiment-card/
│   ├── SKILL.md                     # Copy this folder to .claude/skills/
│   ├── references/
│   │   ├── evidence-ladder.md       # Grading evidence 0–5
│   │   ├── test-methods.md          # Methods from cheapest to most expensive
│   │   └── card-templates.md        # Experiment and learning card templates
│   └── examples/
│       └── tool-delivery-experiment-cards.md
├── README.md
├── CONTRIBUTING.md
└── LICENSE
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Note that this repo isn't actively maintained, so responses to issues and PRs will be slow or may never come.

## License

MIT — see [LICENSE](LICENSE).

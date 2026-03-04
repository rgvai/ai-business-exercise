# AI Business Exercise

A Claude custom skill that guides users through a structured assessment of whether AI acceleration helps or hurts their specific business.

## What It Does

Instead of offering a generic "AI is good/bad" take, this skill runs an interactive diagnostic across five dimensions that actually determine AI's net impact on an organization:

1. **Organizational Adaptability** — Can you absorb new technology fast enough to benefit from it?
2. **Data Infrastructure Maturity** — Is your data ready for AI, or will every project stall at data prep?
3. **Workforce Reskilling Capacity** — Can your people evolve with the technology, or will displacement outpace retraining?
4. **Regulatory Constraints** — Does your industry's regulatory environment enable or block AI adoption?
5. **Competitive Dynamics & Timing** — Are you ahead, behind, or at parity with competitors on AI, and what does that mean for your window of opportunity?

At the end, Claude delivers a synthesis including a scorecard, strategic verdict, critical dependencies, prioritized actions, and a frank inaction risk statement.

## Why This Exists

The question "Does AI help or hurt my business?" has no universal answer. The same AI capabilities that give one company a decisive edge can destabilize another. The difference comes down to context: your data, your people, your industry, your competitive position, and your willingness to execute.

This skill operationalizes that nuance into a repeatable exercise anyone can run.

## Installation

1. Download `ai-business-exercise.skill` from the [Releases](../../releases) page.
2. In Claude, go to **Settings → Capabilities**.
3. Upload the `.skill` file.
4. The skill activates automatically when you ask about AI strategy, AI readiness, or AI's impact on a business.

## Skill Structure

```
ai-business-exercise/
├── SKILL.md                      # Core skill — framework, delivery format, synthesis template
└── references/
    └── FRAMEWORK.md              # Deep reference — disruption modes, pitfalls, industry patterns, examples
```

**SKILL.md** contains everything Claude needs for the interactive exercise: the five diagnostic dimensions, question prompts, classification logic, and the output synthesis template.

**FRAMEWORK.md** is loaded on demand when Claude needs deeper context — Schumpeterian creative destruction framing, four modes of disruption (value creation, operational leverage, disintermediation, margin compression), common assessment pitfalls, industry-specific patterns, and two fully worked walkthroughs.

## Example Prompts

Any of these will trigger the skill:

- *"Will AI help or hurt my consulting firm?"*
- *"I run a mid-size manufacturing company. Should I be investing in AI or is it overhyped for my industry?"*
- *"Our competitors are adopting AI fast. Help me figure out if we need to respond and how."*
- *"I want to build an AI strategy but I'm not sure where we stand in terms of readiness."*
- *"What's the risk if we just ignore AI for now?"*

## What the Output Looks Like

After walking through all five dimensions interactively, Claude produces:

| Component | Description |
|---|---|
| **Scorecard** | Each dimension rated as Asset, Mixed, or Risk |
| **Strategic Verdict** | Nuanced assessment of AI as tailwind or headwind for your organization |
| **Critical Dependencies** | The 2–3 swing variables that most determine your outcome |
| **Action Priorities** | What to do now, what to invest in over 6–12 months, what to monitor |
| **Inaction Risk Statement** | What happens if you do nothing — because doing nothing is also a choice |

## Design Principles

- **Business-first, not technology-first.** The exercise is about your organization, not about AI capabilities.
- **No cheerleading or fearmongering.** Honest assessment, including uncomfortable answers.
- **Both adoption and avoidance are gambles.** The skill makes this explicit rather than implying one path is inherently safe.
- **Time matters.** Short-term costs can mask long-term compounding returns, and inaction has compounding consequences too.

## Customization

Fork and adapt the skill to your needs:

- **Add industry-specific dimensions** by extending `FRAMEWORK.md` with sectors relevant to your audience.
- **Adjust the synthesis template** in `SKILL.md` if you want different output components.
- **Add scoring weights** if certain dimensions matter more in your context.
- **Include your own example walkthroughs** in `FRAMEWORK.md` to help Claude calibrate for your domain.

## License

MIT

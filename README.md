# Cerberus System Skill

**A guided three-head decision council for difficult personal and professional choices.**

Cerberus System is a Codex skill that helps an AI agent interview a user, build three lightweight decision lenses, and run a structured council before an important choice.

It is designed for moments when a person feels pulled between competing selves:

- the part that must work, deliver, and survive professionally;
- the part that has a body, family, emotions, and daily limits;
- the part that refuses to betray its deepest identity and values.

Cerberus turns that conflict into a practical deliberation instead of a vague spiral.

## The Three Heads

| Head | Role | Core Question |
|---|---|---|
| **Alpha** | Work-self | What does this mean for work, execution, responsibility, opportunity, and professional integrity? |
| **Beta** | Life-self | What does this cost in energy, health, relationships, recovery, and daily life? |
| **Gamma** | Core-identity self | Does this violate my non-negotiables, dignity, sacrifice order, or the person I refuse to become? |

The system does not claim to reveal a perfect “true self.” It creates provisional, inspectable decision lenses from user stories, choices, values, and corrections.

## Why Cerberus Exists

Many AI decision prompts are too flat:

> “List pros and cons.”

But real decisions are rarely just pros and cons. They are internal negotiations.

Should I leave this job?  
Should I take this opportunity?  
Should I protect stability or chase creative life?  
Should I speak up, endure, negotiate, or walk away?

Cerberus helps an agent ask better questions, preserve minority concerns, and produce a decision with:

- an action;
- boundaries;
- review points;
- stop conditions;
- dissenting views;
- explicit uncertainty.

## What This Skill Includes

```text
cerberus-system/
  SKILL.md
  agents/
    openai.yaml
  references/
    adaptive-interviewing.md
    council-protocol.md
    templates.md
```

### Key Capabilities

- Conversational onboarding instead of form filling.
- Adaptive interviewing for users who struggle to describe themselves.
- Persistent Cerberus Profiles so users do not need to configure the council every time.
- Identity-neutral Gamma setup that does not assume gender, family structure, or life path.
- Alpha / Beta / Gamma persona card generation.
- Four-round council protocol:
  1. independent stance;
  2. cross-questioning;
  3. revised stance;
  4. chair synthesis.
- Mandatory visible interaction between heads. Cerberus is not valid if it skips cross-questioning and jumps straight to a summary.
- Decision logs and calibration rules.
- Guardrails for privacy, high-stakes decisions, and user agency.

## Quick Start

Install the `cerberus-system/` folder into your Codex skills directory.

Example location:

```text
~/.codex/skills/cerberus-system/
```

Then invoke it with:

```text
Use $cerberus-system to guide me through a three-head decision council for an important choice.
```

Or:

```text
Use $cerberus-system to help me decide whether I should leave my current job.
```

## Example Flow

The agent should not begin by asking the user to fill out a long document.

Instead, it asks one question at a time:

```text
Recently, what work decision best represents how you operate?
```

If the user gives a rich story, the agent extracts patterns.

If the user says “I don’t know,” the agent switches to low-friction choices:

```text
Pick the closest one. At work, when something feels wrong, you usually:
A. Stay quiet and protect yourself.
B. Raise the issue carefully.
C. Directly challenge it.
D. Work around it privately.
E. Start planning an exit.
```

This makes Cerberus usable for people who are not naturally verbal, reflective, or comfortable with long self-analysis.

## Privacy

This repository contains only reusable skill instructions and generic templates.

It does **not** include:

- personal onboarding transcripts;
- private persona cards;
- decision logs;
- real user cases;
- private life or work data.

Cerberus should usually work from summaries, not raw private archives.

## Reuse Across Sessions

Cerberus supports a persistent profile pattern. After first setup, the agent can save or output a compact Cerberus Profile containing distilled summaries, cards, non-negotiables, and calibration notes.

Future sessions should load that profile and ask only for the current decision, instead of repeating onboarding.

## Important Boundaries

Cerberus is reflective decision support, not a replacement for the user’s judgment.

It should not be treated as professional medical, legal, financial, psychological, or safety advice. For high-stakes decisions, the skill instructs the agent to frame the output as reflection only and recommend appropriate professional support.

Gamma also should not become a moral dictator. It can veto only when explicit user-declared non-negotiables are triggered.

## Repository Status

This is an early public skill package. The core protocol is usable, but the system will improve with real-world calibration:

- better onboarding question banks;
- more example councils;
- multilingual refinements;
- compatibility testing across different LLMs;
- optional scripts for generating local Cerberus workspaces.

## License

MIT

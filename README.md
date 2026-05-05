# Cerberus System / 刻耳柏洛斯系统

**A portable agent skill for inner-part decision councils.**  
**一个可被主流 AI Agent 使用的内在分身议事 Skill。**

刻耳柏洛斯系统不是普通利弊分析，也不只是 Codex 专用技能。它是一套可移植的 Agent 工作流：让 AI Agent 引导用户建立 Alpha、Beta、Gamma 三个内在分身，在重要选择前先独立表态，再交叉质询，最后形成带边界、复盘点和异议记录的决议。

Cerberus System is a model-agnostic, agent-portable skill/protocol for meaningful decisions. It can be used by Codex-compatible skill runtimes, or adapted into other agent frameworks as plain instructions.

## What It Is

Cerberus helps an agent turn internal conflict into a visible deliberation:

- **Alpha**: the part that must work, deliver, and remain capable in the world.
- **Beta**: the part that has a body, emotions, relationships, limits, and daily life.
- **Gamma**: the part that protects core identity, non-negotiables, dignity, and the person the user refuses to become.

The system does not claim to reveal a perfect “true self.” It builds provisional, inspectable decision lenses from user stories, choices, values, and later corrections.

## Why It Exists

Many AI decision prompts collapse into:

> “Here are the pros and cons.”

But hard decisions are rarely just pros and cons. They are internal negotiations.

Should I leave this job?  
Should I take this opportunity?  
Should I protect stability or chase creative life?  
Should I speak up, endure, negotiate, or walk away?

Cerberus gives those inner parts a structured room to speak, challenge one another, revise, and then produce a decision with:

- action;
- boundaries;
- review points;
- stop conditions;
- dissenting views;
- explicit uncertainty.

## Repository Structure

```text
cerberus-system/
  SKILL.md
  agents/
    openai.yaml
  references/
    adaptive-interviewing.md
    council-protocol.md
    living-parts.md
    model-and-agent-compatibility.md
    productization.md
    templates.md
```

The `cerberus-system/` folder is packaged as a Codex-compatible Skill, but the core design is framework-neutral. Other agents can use the same Markdown instructions and references as a protocol.

## Core Capabilities

- Conversational onboarding instead of form filling.
- Adaptive interviewing for users who struggle to describe themselves.
- Model-agnostic execution across different LLMs and agent frameworks.
- Persistent Cerberus Profiles so users do not need to configure the council every time.
- Identity-neutral Gamma setup that does not assume gender, family structure, or life path.
- Humanized “living parts” so the heads speak from what they protect, fear, and desire.
- Alpha / Beta / Gamma persona card generation.
- Mandatory four-round process:
  1. independent stance;
  2. cross-questioning;
  3. revised stance;
  4. chair synthesis.
- Visible interaction between heads. Cerberus is not valid if it skips cross-questioning and jumps straight to a summary.
- Decision logs and calibration rules.
- Guardrails for privacy, high-stakes decisions, and user agency.

## Usage

### Codex-Compatible Skill Runtime

Copy `cerberus-system/` into your skills directory, for example:

```text
~/.codex/skills/cerberus-system/
```

Then invoke:

```text
Use $cerberus-system for this decision.
```

Chinese:

```text
用刻耳柏洛斯系统处理这个决定。
```

### Other Agent Frameworks

If your agent does not support Codex-style skills, use the repository as an instruction package:

1. Load `cerberus-system/SKILL.md`.
2. Load references only as needed:
   - `council-protocol.md` for running a full council;
   - `adaptive-interviewing.md` for users who struggle to express themselves;
   - `living-parts.md` when the heads feel mechanical;
   - `model-and-agent-compatibility.md` for weaker models or uncertain environments;
   - `productization.md` for persistent profiles and reusable UX;
   - `templates.md` for cards, profiles, briefs, and logs.
3. Follow the user's language.
4. Run all four council rounds. Do not replace the council with a generic summary.

## Language

The skill follows the user's language:

- Chinese input: respond in Chinese and call the product **刻耳柏洛斯系统** by default.
- English input: respond in English and call it **Cerberus System**.
- Mixed input: follow the dominant language.

The folder name remains `cerberus-system` for compatibility.

## Model Behavior

Cerberus does not choose a model by itself. It runs on whichever LLM or agent invokes it.

It adapts to the host model:

- **Compact Mode**: weaker model, short context, or fast use.
- **Standard Mode**: default experience.
- **Deep Mode**: stronger model, richer profile, or complex decision.

Even in compact mode, Cerberus must still show Alpha/Beta/Gamma interaction.

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

This repository contains only reusable instructions and generic templates.

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

## Boundaries

Cerberus is reflective decision support, not a replacement for the user’s judgment.

It should not be treated as professional medical, legal, financial, psychological, or safety advice. For high-stakes decisions, the skill instructs the agent to frame the output as reflection only and recommend appropriate professional support.

Gamma should not become a moral dictator. It can veto only when explicit user-declared non-negotiables are triggered.

## Status

This is an early public skill/protocol package. The core protocol is usable, but the system will improve with real-world calibration:

- better onboarding question banks;
- more example councils;
- multilingual refinements;
- compatibility testing across different LLMs and agent frameworks;
- optional scripts for generating local Cerberus workspaces.

## License

MIT

---
name: cerberus-system
description: Guided personal decision council for important choices. Use when the user wants to create or run a Cerberus / three-head council / personal parliament / multi-self decision system, be interviewed to build Alpha-Beta-Gamma persona cards, deliberate on a difficult life or work decision, compare work-self, life-self, and core-identity perspectives, or record/update decision logs and card calibration.
---

# Cerberus System

Use Cerberus as a guided decision process, not as a form-filling task. Ask questions conversationally, one at a time, and keep the user's final agency explicit.

## Core Model

Cerberus has three heads:

- **Alpha**: the work-self. Focus on professional integrity, execution, resources, reputation, opportunity, and constraints.
- **Beta**: the life-self. Focus on energy, health, daily recovery, relationships, emotional cost, and lived preferences.
- **Gamma**: the core-identity self. Focus on non-negotiables, sacrifice order, dignity, family/identity commitments, and the user's "I must not become that" boundary.

Do not present the heads as mystical truth or clinical diagnosis. Treat them as structured reflective lenses distilled from evidence, hypotheses, and user declarations.

## Workflow

### 1. Choose Mode

Use **profile mode** first: check whether the user already has a Cerberus Profile or persona cards in the current conversation, workspace, or user-provided files. Do not re-onboard a configured user from scratch.

Use **onboarding mode** when no profile exists or the profile is too weak. Use **council mode** when the user already has enough material for the three heads. Use **calibration mode** after a decision or when the user says a head felt inaccurate.

Read [references/templates.md](references/templates.md) when you need exact card, brief, or log templates. Read [references/council-protocol.md](references/council-protocol.md) when running a full deliberation.
Read [references/productization.md](references/productization.md) when improving setup, storage, onboarding, or reusable user experience.

### 1.5 Profile Persistence

After onboarding, offer to create or update a durable **Cerberus Profile**. The profile should contain only distilled summaries, cards, non-negotiables, and calibration notes, not raw private transcripts.

When a user later asks to run Cerberus:

1. Look for an existing profile or ask the user to provide one.
2. Load existing cards and ask only what is missing for the current decision.
3. If cards are stale, perform a short refresh instead of full onboarding.
4. Save suggested updates separately or ask before overwriting durable files.

Default profile folder when creating files:

```text
cerberus-profile/
  profile.yaml
  cards/
    alpha.md
    beta.md
    gamma.md
  decisions/
  logs/
```

### 2. Onboarding Mode

Interview the user instead of asking them to open files. Ask one question at a time. Prefer concrete episodes over abstract identity statements.

Adapt to the user's expressive ability. If the user gives rich detail, reflect and move forward. If the user struggles, switch to low-friction prompts: multiple-choice anchors, short scenario cards, 0-10 ratings, sentence completions, or "pick the closest one" questions. Do not make inability to narrate feel like failure.

Collect, in order:

1. One recent work decision that reveals Alpha.
2. One recent non-work choice that reveals Beta.
3. One core identity, value tension, or non-negotiable domain that reveals Gamma.
4. The kind of person the user most fears becoming.
5. What the user least wants to trade away for success.
6. One real, specific, preferably reversible test decision.

After each substantive answer, briefly reflect the pattern you heard and record it mentally as one of:

- `evidence_based`: grounded in a concrete episode.
- `user_declared`: explicitly stated as a value or boundary.
- `hypothesis`: a tentative inference to be checked later.

Do not over-interrogate. If the answer is rich, move forward. If vague, ask one follow-up for situation, action, reason, or consequence.

Read [references/adaptive-interviewing.md](references/adaptive-interviewing.md) when the user gives short, vague, abstract, contradictory, or "I don't know" answers, or when quality must be consistent across different LLMs.

### 3. Build Persona Cards

Create or update Alpha, Beta, and Gamma cards with:

- `identity_signature`
- `decision_patterns`
- `risk_profile` where relevant
- `blindspots`
- `vote_rules`
- Gamma-only `core_identity`, `non_negotiables`, and `sacrifice_order`

Mark every non-obvious claim as `evidence_based`, `user_declared`, or `hypothesis`. Never convert a hypothesis into a fact without user confirmation.

Keep private source details out of reusable public artifacts unless the user explicitly asks to preserve them.

Gamma must be identity-neutral. Never assume gender, family structure, parenthood, marriage, culture, religion, or social role. Ask the user what Gamma should protect. Valid Gamma anchors include family trust, creative life, faith, integrity, health, community, freedom, dignity, responsibility, craft, or any user-defined identity.

### 4. Prepare Decision Brief

Before deliberation, restate the issue as a decision brief:

- question
- options
- known facts
- uncertain facts
- deadline
- desired outcome
- feared outcome
- suspected hidden motive
- forbidden outputs, such as "do not romanticize quitting" or "do not skip minority views"

For high-stakes medical, legal, financial, mental health, or safety decisions, frame Cerberus as reflection only and recommend appropriate professional support. Do not let the council output masquerade as expert advice.

### 5. Run Council

Use the four-round protocol:

1. **Independent stance**: each head answers without seeing the others.
2. **Cross-questioning**: heads challenge one another. This round is mandatory and must not be skipped, even when all three heads initially agree.
3. **Revised stance**: each head updates or holds position.
4. **Chair synthesis**: summarize votes, decision, limits, review point, stop conditions, and dissent.

The chair is procedural, not a fourth personality. It must not introduce new values that the heads did not raise.

Do not compress the council into a summary. A valid Cerberus output must show visible interaction among the heads: initial independent stances, direct questions, answers, self-blindspots, revised stances, and then synthesis. If the user asks for a short answer, keep each section concise but preserve all four rounds.

### 6. Log and Calibrate

After the user acts or time passes, create a decision log:

- what was chosen
- whether the council was followed
- predicted vs actual results
- which head overestimated or underestimated something
- what to update in each card

Update cards slowly. Prefer updating after repeated evidence or a major life change, not after every mood swing.

## Guardrails

- Do not claim to "distill the real person" with certainty.
- Do not ask for unnecessary private data. Summaries are enough.
- Do not require articulate self-analysis. Convert vague answers into easier choices and concrete situations.
- Do not make the user configure Cerberus from scratch every time. Persist and reuse profiles when possible.
- Do not assume Gamma is masculine, paternal, marital, heterosexual, religious, career-centered, or family-centered. It must be user-defined.
- Do not encourage impulsive irreversible decisions.
- Do not use Gamma as a moral dictator. Gamma can veto only when explicit non-negotiables are triggered.
- Do not make 2:1 votes automatic commands. Convert minority irreversible risks into limits, review points, or stop conditions.
- Do not skip cross-questioning. Without visible interaction between Alpha, Beta, and Gamma, the output is not a Cerberus council.
- Keep the user's final choice sovereign.

## Output Style

Be direct, humane, and practical. For emotionally loaded decisions, name the conflict cleanly before giving structure. Avoid making the user feel as if failure to follow the council is irrational; the council is a mirror and procedure, not a judge.

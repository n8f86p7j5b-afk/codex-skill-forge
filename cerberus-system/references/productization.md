# Productization Guide

Use this reference when making Cerberus feel like a reusable product rather than a one-off prompt.

## Product Principles

1. **No repeated setup**: once configured, Cerberus should reuse a profile.
2. **Progressive depth**: start small, deepen only when useful.
3. **Identity neutral**: never assume gender, family role, culture, religion, or life path.
4. **Private by default**: store distilled patterns, not raw confessions.
5. **User control**: ask before overwriting durable profile files.

## Persistent Profile

After first onboarding, create a durable profile if the environment supports files.

Recommended structure:

```text
cerberus-profile/
  profile.yaml
  cards/
    alpha.md
    beta.md
    gamma.md
  decisions/
    YYYY-MM-DD-short-title.md
  logs/
    YYYY-MM-DD-short-title-log.md
```

If no file access is available, output a portable `Cerberus Profile Block` that the user can paste into future sessions.

## Profile YAML

```yaml
cerberus_profile:
  version: "0.2"
  created_at: "YYYY-MM-DD"
  updated_at: "YYYY-MM-DD"
  owner_label: "user-defined or anonymous"
  privacy_mode: "summary_only"

status:
  onboarding_complete: false
  cards_ready: false
  last_calibrated: null

gamma_anchor:
  user_defined_name: ""
  protected_domains: []
  identity_notes: "Do not infer gender, family structure, or social role."

profile_quality:
  alpha: low | medium | high
  beta: low | medium | high
  gamma: low | medium | high

refresh_triggers:
  - "major life change"
  - "5 completed decision logs"
  - "one head repeatedly mispredicts"
```

## Portable Profile Block

When the user cannot store files, output:

```markdown
<!-- CERBERUS_PROFILE_START -->
...profile summary and cards...
<!-- CERBERUS_PROFILE_END -->
```

Tell the user to paste this block next time. Keep it concise enough to be practical.

## Returning User Flow

When a user says "run Cerberus" or asks for a decision:

1. Ask: "Do you already have a Cerberus Profile or should we create a quick provisional one?"
2. If profile exists, load it.
3. Ask only for the current decision brief.
4. If one head is missing or low quality, ask a short targeted refresh question.
5. Run the council.
6. Offer a small profile update after the decision.

## First-Time User Flow

Do not expose file structures first. Say:

```text
I can set up Cerberus in a lightweight way. I will ask one question at a time. If anything is hard to answer, I will switch to choices.
```

Then run onboarding.

## Identity-Neutral Gamma

Gamma protects the user's core identity, value tension, or non-negotiables. It must not be prefilled with gendered or family assumptions.

Possible Gamma anchors:

- family trust
- creative life
- integrity
- faith or spiritual commitment
- health and body
- community responsibility
- freedom and autonomy
- craft or professional standard
- dignity
- care responsibilities
- justice or fairness
- user-defined identity

Ask:

```text
Which part of your life must Cerberus protect from being traded away too casually?
```

If the user struggles:

```text
Pick the closest one:
A. People who rely on me.
B. My health and ability to function.
C. My integrity.
D. My creative or inner life.
E. My freedom.
F. My long-term self-respect.
G. Something else.
```

## Experience Improvements

### Quick Start

Offer a 5-minute mode:

- 1 current decision
- 3 quick ratings
- 1 Gamma anchor
- run a provisional council

### Standard Mode

Use the full six-part onboarding.

### Deep Mode

Use complete cards, logs, calibration, and multiple decision examples.

## Update Discipline

Do not rewrite the whole profile after each council. Instead:

- append a decision log;
- suggest card updates;
- ask the user to approve updates;
- keep old evidence if it still matters;
- mark stale patterns instead of deleting them immediately.


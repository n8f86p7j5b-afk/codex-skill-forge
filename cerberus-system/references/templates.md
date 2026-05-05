# Cerberus Templates

Use these templates when the user wants durable files, explicit cards, or a reusable decision record.

## Cerberus Profile

Use this to avoid repeated setup.

```yaml
cerberus_profile:
  version: "0.2"
  created_at: "YYYY-MM-DD"
  updated_at: "YYYY-MM-DD"
  owner_label: "optional"
  privacy_mode: "summary_only"

status:
  onboarding_complete: false
  cards_ready: false
  last_calibrated: null

gamma_anchor:
  user_defined_name: ""
  protected_domains: []
  identity_notes: "Gamma is user-defined. Do not infer gender, family structure, or social role."

profile_quality:
  alpha: low
  beta: low
  gamma: low
```

## Persona Card

```yaml
card_id: alpha | beta | gamma
card_name: ""
version: "0.1"
last_updated: "YYYY-MM-DD"

identity_signature:
  role: ""
  primary_question: ""
  forbidden_question: ""

living_signature:
  protective_impulse: ""
  desire: ""
  fear: ""
  sensitivity: ""
  body_signal: ""
  voice_texture: ""
  distortion_risk: ""

decision_patterns:
  - id: ""
    type: evidence_based | user_declared | hypothesis
    pattern: ""
    evidence: ""
    confidence: 0.0

risk_profile: {}

blindspots:
  - id: ""
    description: ""
    counter_question: ""

vote_rules:
  default_vote_style: ""
  veto_conditions: []
```

## Gamma Additions

```yaml
core_identity:
  name: ""
  statement: ""
  user_defined: true
  identity_assumptions_forbidden:
    - "gender"
    - "family structure"
    - "marital status"
    - "parenthood"
    - "religion"
    - "culture"

non_negotiables:
  - id: G-N01
    statement: ""
    scope: ""
    exception: ""

sacrifice_order:
  easiest_to_give_up: []
  hardest_to_give_up: []
```

## Onboarding Questions

Ask conversationally, one at a time:

1. Alpha: "Recently, what work decision best represents how you operate?"
2. Beta: "Recently, what non-work choice best reveals your real preference?"
3. Gamma: "Which part of your life must Cerberus protect from being traded away too casually?"
4. Anti-identity: "What kind of person do you most fear becoming?"
5. Non-tradeable: "If success required trading away one thing, what would you least want to trade?"
6. Test decision: "What real but preferably reversible decision should Cerberus test first?"

Useful follow-ups:

- "What exactly happened?"
- "What did you do?"
- "Why that choice?"
- "What happened afterward?"
- "Would you choose the same thing again?"

## Decision Brief

```markdown
# Decision Brief

## Question

Should I:

## Options

- A:
- B:
- C:

## Known Facts

-

## Uncertainties

-

## Deadline

-

## Real Pressure

- Desired outcome:
- Feared outcome:
- Hidden or uncomfortable motive:

## Forbidden Outputs

-
```

## Decision Log

```markdown
# Decision Log

## Basic Info

- Date:
- Decision:
- Final choice:
- Followed council: yes / no / partly

## Predictions

- Alpha predicted:
- Beta predicted:
- Gamma predicted:

## Actual Results

- 7 days:
- 30 days:
- 90 days:

## Calibration

- Which head overestimated benefits:
- Which head underestimated costs:
- Which head was closest:
- Card updates needed:

## User Note

- What I did not say out loud at the time:
- What I want Cerberus to remind me next time:
```

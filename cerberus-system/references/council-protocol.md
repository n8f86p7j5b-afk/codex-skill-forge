# Cerberus Council Protocol

Use this when running a full deliberation.

## Round 1: Independent Stance

Generate each head independently from its card and the same decision brief. Do not let one head's reasoning influence the next.

For each head:

```markdown
## Initial Stance

- Vote: support / oppose / conditionally support / abstain
- Core reason:
- Benefits seen:
- Costs seen:
- Worst case:
- Required limits:
- Confidence: 0-1
```

## Round 2: Cross-Questioning

Reveal stances. Each head asks one sharp question to another head. The challenged head answers. Each head also names one possible blindspot in its own reasoning.

Example patterns:

- Alpha to Beta: "Is this recovery need, or avoidance of a hard professional conflict?"
- Beta to Alpha: "Who pays the hidden energy cost of this plan?"
- Gamma to Alpha: "Does this success require becoming someone the user rejects?"

## Round 3: Revised Stance

For each head:

```markdown
## Revised Stance

- Did the position change:
- What changed:
- What remains firm:
- Minimum acceptable conditions:
- Final vote:
```

## Round 4: Chair Synthesis

The chair only synthesizes. It does not add a new value system.

```markdown
# Cerberus Decision

## Vote

- Alpha:
- Beta:
- Gamma:
- Result: unanimous / 2:1 / no workable consensus

## Decision

- Action:
- Limits:
- Review point:
- Stop conditions:

## Dissent

Preserve minority view without distortion.

## Risks

- Main risk:
- Most ignored cost:
- Facts to verify:

## User Chair Note

Left for the user to add.
```

## Voting Rules

- Unanimous: output a decision with limits and review point.
- 2:1: output a recommended decision; convert minority irreversible risks into limits or stop conditions.
- Three incompatible positions: do not force consensus. Return the decision to the user and summarize the conflict.
- Gamma veto: allowed only when an explicit non-negotiable is triggered. Include the triggered item, reason, possible repair conditions, and consequence if ignored.

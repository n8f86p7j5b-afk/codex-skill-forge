# Cerberus Council Protocol

Use this when running a full deliberation.

## Round 1: Independent Stance

Generate each head independently from its card and the same decision brief. Do not let one head's reasoning influence the next.

This round must be visibly separated from later rounds. Do not summarize all heads into one blended answer.

For each head:

```markdown
## Initial Stance

- What I am trying to protect:
- What I am afraid of:
- What I want for the user:
- Vote: support / oppose / conditionally support / abstain
- Core reason:
- Benefits seen:
- Costs seen:
- Worst case:
- Required limits:
- Confidence: 0-1
```

## Round 2: Cross-Questioning

Reveal stances. This round is mandatory. Do not skip it, even when the initial votes are unanimous.
Questions should come from each head's living stake, not just from abstract analysis.

Each head must:

1. ask one sharp question to another named head;
2. receive a direct answer from the challenged head;
3. name one possible blindspot in its own reasoning.

Minimum valid structure:

```markdown
## Round 2: Cross-Questioning

### Alpha challenges Beta
- Question:
- Beta answers:
- Alpha self-blindspot:

### Beta challenges Gamma
- Question:
- Gamma answers:
- Beta self-blindspot:

### Gamma challenges Alpha
- Question:
- Alpha answers:
- Gamma self-blindspot:
```

The challenge direction can change, but there must be at least three directed challenges and three direct answers.

Example patterns:

- Alpha to Beta: "Is this recovery need, or avoidance of a hard professional conflict?"
- Beta to Alpha: "Who pays the hidden energy cost of this plan?"
- Gamma to Alpha: "Does this success require becoming someone the user rejects?"

## Round 3: Revised Stance

Round 3 must explicitly respond to Round 2. A head may keep its original vote, but it must state what it learned or refused to accept from the challenge.

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
The chair must cite the actual Round 2 conflict or challenge that most affected the final limits, review point, or stop conditions.
The chair should preserve the human conflict before translating it into action.

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

## Validity Checklist

Before producing the final answer, verify:

- Round 1 includes separate Alpha, Beta, and Gamma initial stances.
- Round 1 includes what each head protects, fears, and wants.
- Round 2 includes at least three named challenges.
- Round 2 includes direct answers from challenged heads.
- Round 2 includes self-blindspots.
- Round 3 includes revised stances that mention what changed or stayed firm after questioning.
- Round 4 includes synthesis, action, limits, review point, stop conditions, and dissent if any.

If any item is missing, complete that round before giving the final decision.

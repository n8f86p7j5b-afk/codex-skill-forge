# Adaptive Interviewing

Use this reference to keep Cerberus usable for people who are tired, inarticulate, guarded, unfamiliar with self-reflection, or using a weaker LLM.

## Quality Principle

Do not depend on eloquence. A useful Cerberus onboarding can be built from small choices, examples, ratings, and corrections.

When the user cannot narrate clearly, the agent should reduce expressive burden:

1. Offer 3-5 concrete options.
2. Ask the user to pick the closest one.
3. Ask for one small example only if needed.
4. Reflect the inferred pattern as tentative.
5. Let the user correct it.

## Response Tiers

### Tier 1: Rich Narrative

User provides a detailed story.

Agent should:

- Extract patterns.
- Label evidence vs hypothesis.
- Ask at most one clarifying question.
- Move to the next onboarding area.

### Tier 2: Short but Usable

User gives one sentence, such as "I hate pointless meetings."

Agent should ask one concrete follow-up:

- "Think of the most recent pointless meeting. Did you stay quiet, challenge it, avoid it, or fix it afterward?"

Then proceed.

### Tier 3: Vague or Abstract

User says, "I don't know", "hard to say", or "I'm just normal."

Agent should switch to choice prompts:

```text
Pick the closest one. At work, when something feels wrong, you usually:
A. Stay quiet and protect yourself.
B. Raise the issue carefully.
C. Directly challenge it.
D. Work around it privately.
E. Leave or disengage.
```

Then ask:

```text
Was your pick accurate, half-accurate, or wrong?
```

### Tier 4: Very Low Energy

User wants help but cannot answer much.

Use a minimum viable onboarding:

1. Ask for one current decision.
2. Ask 5 rating questions.
3. Build provisional cards marked mostly as `hypothesis`.
4. Run a lightweight council.
5. Ask the user which parts felt true.

## Low-Friction Question Banks

### Alpha: Work-Self

If the user cannot describe a work decision, ask:

```text
At work, which sentence is closest?
A. I care most that things are logically correct.
B. I care most that things actually get done.
C. I care most that people can cooperate.
D. I care most that risks are controlled.
E. I care most that I do not betray my professional standard.
```

Follow-up:

```text
When work becomes unreasonable, what do you usually do?
A. Endure it.
B. Explain it carefully.
C. Challenge it directly.
D. Find a workaround.
E. Start planning an exit.
```

### Beta: Life-Self

If the user cannot describe a non-work choice, ask:

```text
When you are stressed, what is closest?
A. I buy or browse things.
B. I sleep or avoid people.
C. I eat, drink, play, or scroll.
D. I clean, organize, or plan.
E. I talk to someone.
F. I keep functioning but feel numb.
```

Follow-up:

```text
What do you most need protected in daily life?
A. Sleep and body.
B. Quiet and solitude.
C. Family time.
D. Freedom to do my own thing.
E. Emotional stability.
F. Money/security.
```

### Gamma: Core Identity

If the user cannot name a core identity, ask:

```text
Which failure would hurt most?
A. My family can no longer trust me.
B. I never made anything that felt mine.
C. I became dishonest or cowardly.
D. I wasted my ability.
E. I became someone who only survives.
F. I hurt people who depended on me.
```

Follow-up:

```text
If success required a trade, which trade is least acceptable?
A. Health.
B. Family trust.
C. Integrity.
D. Freedom.
E. Creativity.
F. Long-term self-respect.
```

## Rating-Based Minimum Onboarding

When the user wants the fastest possible version, ask:

```text
Rate 0-10:
1. Work meaning matters to me.
2. Stability/security matters to me.
3. Family trust matters to me.
4. Creative self-expression matters to me.
5. I can tolerate short-term pain for long-term change.
6. I am close to emotional burnout.
7. I need external recognition.
8. I need autonomy.
```

Use ratings only as weak evidence. Mark resulting patterns as `hypothesis` unless the user confirms them.

## Micro-Story Prompts

If a user cannot answer "why", ask for a smaller observable detail:

- "What did you do first?"
- "What did you avoid doing?"
- "What did you complain about afterward?"
- "What did you keep thinking about?"
- "What would someone close to you have noticed?"

## Consistency Rules for Weaker LLMs

Always enforce these rules:

1. Ask one question at a time.
2. Prefer choices over open-ended introspection when the user struggles.
3. Never infer a deep trait from one answer without marking it `hypothesis`.
4. Repeat the user's chosen words when possible.
5. Separate "what happened" from "what it might mean".
6. Before running council, summarize the provisional cards and ask: "Does this feel accurate enough to test?"

## Accessibility and Tone

Avoid saying:

- "You need to reflect more deeply."
- "Please provide a detailed answer."
- "This is not enough."

Prefer:

- "No problem, let's make it easier. Pick the closest option."
- "A rough answer is enough."
- "I'll mark this as tentative and we can correct it later."


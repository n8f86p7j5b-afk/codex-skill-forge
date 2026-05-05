# Model and Agent Compatibility

Cerberus is model-agnostic. It does not select a model by itself. The active model is whichever model the host agent uses.

Use this reference to keep behavior consistent across different LLMs, agent frameworks, context lengths, and tool availability.

## Triggering

Trigger Cerberus only when the user wants a meaningful decision process or profile-based council.

Good triggers:

- "Run Cerberus on this decision."
- "Help me decide with the three-head council."
- "Create my Alpha/Beta/Gamma profile."
- "Use my Cerberus profile for this problem."
- "Calibrate my Cerberus cards."
- "I want work-self, life-self, and core-identity perspectives to deliberate."

Avoid triggering for:

- ordinary brainstorming;
- simple pros-and-cons requests;
- factual lookups;
- normal planning tasks;
- decisions where the user did not ask for the council process.

If uncertain, ask:

```text
Do you want a quick answer, or should I run the full Cerberus council?
```

## Model Capability Modes

### Compact Mode

Use when the model is weaker, context is short, or user wants speed.

- Ask only the current decision plus 3-5 structured questions.
- Build provisional cards marked mostly as `hypothesis`.
- Keep each head to 4-6 bullets.
- Still run all four rounds.
- Keep Round 2 short but visible.

### Standard Mode

Use by default.

- Use existing profile if available.
- Ask only missing onboarding questions.
- Produce living signatures, decision brief, four rounds, and synthesis.
- Save or suggest profile/log updates.

### Deep Mode

Use when the user asks for depth and the model/context can support it.

- Use richer evidence.
- Include stronger living-part voice.
- Run sharper cross-questioning.
- Produce card update suggestions and decision log.

## Agent Framework Compatibility

Cerberus should work in any agent that can read instructions. Do not require:

- persistent memory;
- file system access;
- tool calls;
- multi-agent runtime;
- a specific model provider.

If files are unavailable, output portable Markdown/YAML blocks.

If tools are unavailable, ask the user to paste their profile or prior cards.

If multi-agent execution is available, it may run Alpha, Beta, and Gamma as separate calls. If not, simulate separation carefully in one response and visibly separate rounds.

## Minimum Viable Output

Even in compact mode, a valid council must include:

1. Alpha/Beta/Gamma initial stances.
2. At least one visible challenge per head.
3. Revised stances.
4. Chair synthesis with action, limits, review point, and stop conditions.

Never replace this with a generic summary.

## Plain Invocation

Recommended simple invocation:

```text
Use $cerberus-system for this decision.
```

Recommended explicit invocation:

```text
Use $cerberus-system to run a three-head council using my existing profile if available.
```


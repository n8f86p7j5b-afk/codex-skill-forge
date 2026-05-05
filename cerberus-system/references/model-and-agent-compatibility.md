# Model and Agent Compatibility

Cerberus is model-agnostic. It does not select a model by itself. The active model is whichever model the host agent uses.

Use this reference to keep behavior consistent across different LLMs, agent frameworks, context lengths, and tool availability.

## Language Compatibility

Use the user's language for all interaction and output.

- Chinese input: respond in Chinese and call the system `刻耳柏洛斯系统` by default.
- English input: respond in English and call it `Cerberus System`.
- Mixed input: follow the dominant language or ask.

Do not expose English-only templates to Chinese users unless they ask for them. Translate headings and operational terms while preserving structure.

## Triggering

Trigger Cerberus only when the user wants a meaningful decision process or profile-based council.

Good triggers:

- "Run Cerberus on this decision."
- "Help me decide with the three-head council."
- "Create my Alpha/Beta/Gamma profile."
- "Use my Cerberus profile for this problem."
- "Calibrate my Cerberus cards."
- "I want work-self, life-self, and core-identity perspectives to deliberate."
- "启动刻耳柏洛斯系统。"
- "用刻耳柏洛斯帮我处理这个决定。"
- "用 Alpha、Beta、Gamma 三个分身议一下。"
- "读取我的刻耳柏洛斯画像。"

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

Chinese:

```text
你想要一个快速建议，还是启动完整的刻耳柏洛斯议事流程？
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

Chinese:

```text
用刻耳柏洛斯系统处理这个决定。
```

Recommended explicit invocation:

```text
Use $cerberus-system to run a three-head council using my existing profile if available.
```

Chinese:

```text
用刻耳柏洛斯系统读取我已有的画像，并为这个决定开一次议事。
```

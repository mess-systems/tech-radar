# promptfoo

| Category | Ring | Kind |
|---|---|---|
| [`adlc`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Open-source tool for LLM evals and red teaming (MIT). Official site: [promptfoo.dev](https://www.promptfoo.dev/).

## Why mess.systems uses it

Red teaming of prompts and agents.

It is also the proposed runner for the agent regression gate in CI in the [`adlc-agent-evals`](https://github.com/mess-systems/blueprints/tree/main/adlc-agent-evals) blueprint: YAML cases, a model matrix, `llm-rubric`, `--fail-on-error` and JUnit output. Its A2A provider supports only the HTTP+JSON binding.

## Alternatives considered

DeepEval (Adopt) for evals as pytest tests. Trial: red teaming, and the agent regression gate in CI from the `adlc-agent-evals` blueprint.

## Where it applies

- [Capability codes: `evals`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`evals`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`adlc-agent-evals`](https://github.com/mess-systems/blueprints/tree/main/adlc-agent-evals) |

## Review trigger

After it has carried the capability in a limited scope: promote to Adopt or move to Hold.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Trial | Initial entry. |
| 2026-11-12 | Trial | Scope widened to the agent regression gate in CI (`adlc-agent-evals`). |

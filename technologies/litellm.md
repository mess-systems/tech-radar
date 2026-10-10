# LiteLLM

| Category | Ring | Kind |
|---|---|---|
| [`ai`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Hold](../README.md#rings) | Product |

## What it is

Open-source LLM gateway and proxy that exposes many model providers through one OpenAI-compatible API, with virtual keys, budgets, and logging. The repository is MIT-licensed except for the `enterprise/` directory, which has its own license. Official site: [docs.litellm.ai](https://docs.litellm.ai/).

## Why mess.systems uses it

It is not used for new work. The `gateway` capability (`gateway.ai.corp`) moves to [agentgateway](agentgateway.md), which is also the example product in the naming standard. The standard's rules (route prefixes `<provider-short>/<model>`, MCP targets, gateway client identities, secrets layout) apply to any gateway product, so an existing LiteLLM install can still follow them.

## Alternatives considered

[agentgateway](agentgateway.md) is the default choice: one gateway for LLM, MCP, and A2A traffic, Apache-2.0, under Linux Foundation governance. Hold, not removal, because existing use may continue until it is replaced.

## Where it applies

- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)
- [Worked encodings](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#11-worked-encodings)
- [Worked example: an LLM gateway](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#8-worked-example-an-llm-gateway)
- [Gateway client identities](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#9-gateway-client-identities)

## Review trigger

No LiteLLM use remains: remove the entry. Or agentgateway moves to Hold: reopen the `gateway` decision.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Trial | Initial entry. |
| 2026-10-10 | Hold | agentgateway becomes the target product for the `gateway` capability. |

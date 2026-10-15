# Langfuse

| Category | Ring | Kind |
|---|---|---|
| [`ai`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source LLM engineering platform (MIT core) for tracing, evaluations, and prompt management. Official site: [langfuse.com](https://langfuse.com/).

## Why mess.systems uses it

It is the example for the `llm-traces` capability: the service account `svc-corp-ai-langfuse` and the gateway's `llm-traces` secret item.

## Alternatives considered

Other LLM observability tools, or general OpenTelemetry tracing. Adopt: default LLM traces store.

## Where it applies

- [Gateway client identities](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#9-gateway-client-identities)
- [Worked example: an LLM gateway](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#8-worked-example-an-llm-gateway)

## Review trigger

A license or maintenance change upstream, or a better fit for the capability.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Trial | Initial entry. |
| 2026-10-15 | Adopt | Default LLM traces and evals store. |

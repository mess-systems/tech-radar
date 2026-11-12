# Grafana Tempo

| Category | Ring | Kind |
|---|---|---|
| [`obs`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source distributed tracing backend (AGPL-3.0). Official site: [grafana.com/oss/tempo](https://grafana.com/oss/tempo/).

## Why mess.systems uses it

Carries the `traces` capability.

In the [`adlc-agent-evals`](https://github.com/mess-systems/blueprints/tree/main/adlc-agent-evals) blueprint it also stores agent and tool traces sent over OTLP through Alloy or the OpenTelemetry Collector, so agent tracing starts without a separate LLM observability platform.

## Alternatives considered

Jaeger. Chosen to fit with Loki and Grafana.

## Where it applies

- [Capability codes: `traces`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`traces`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`adlc-agent-evals`](https://github.com/mess-systems/blueprints/tree/main/adlc-agent-evals) |

## Review trigger

A license or maintenance change upstream, or a better fit for the capability.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Adopt | Initial entry. |
| 2026-11-12 | Adopt | Stores agent traces in `adlc-agent-evals`. |

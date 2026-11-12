# kagent

| Category | Ring | Kind |
|---|---|---|
| [`ai`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Open-source Kubernetes-native framework for AI agents (CNCF sandbox). Official site: [kagent.dev](https://kagent.dev/).

## Why mess.systems uses it

Agents as Kubernetes workloads.

Agents export OpenTelemetry traces (values `otel.tracing.enabled` and `otel.tracing.exporter.otlp.endpoint`). kagent 1.0.0 (2026-11-09) moved the Python runtimes to upstream GenAI instrumentation and dropped the legacy ADK spans, so dashboards should be built after the upgrade. See [`adlc-agent-evals`](https://github.com/mess-systems/blueprints/tree/main/adlc-agent-evals).

## Alternatives considered

LangGraph services. Trial: limited scope.

## Where it applies

- [Capability codes: `inference`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`inference`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`adlc-agent-evals`](https://github.com/mess-systems/blueprints/tree/main/adlc-agent-evals) |

## Review trigger

After it has carried the capability in a limited scope: promote to Adopt or move to Hold.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Trial | Initial entry. |
| 2026-11-12 | Trial | Tracing notes; linked from `adlc-agent-evals`. |

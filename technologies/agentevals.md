# agentevals

| Category | Ring | Kind |
|---|---|---|
| [`adlc`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

Open-source tool that evaluates agent trajectories from OpenTelemetry traces (Apache-2.0): it accepts OTLP with GenAI semantic conventions and checks tool calls and steps with rules or an LLM judge, from a CLI or a Helm-installed service. Version checked on 2026-11-11: v0.12.1, early stage. Official repository: [agentevals-dev/agentevals](https://github.com/agentevals-dev/agentevals).

## Why mess.systems uses it

Optional part of the [`adlc-agent-evals`](https://github.com/mess-systems/blueprints/tree/main/adlc-agent-evals) blueprint: a second exporter in the OpenTelemetry Collector, used only if checking final answers is not enough and the path the agent took has to be checked too.

Assess: early stage, not used yet.

## Alternatives considered

Trajectory checks in an LLM observability platform (Langfuse, Phoenix), or custom checks over spans in Tempo. Assess: trajectory checks for agents.

## Where it applies

- [Capability codes: `evals`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`evals`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`adlc-agent-evals`](https://github.com/mess-systems/blueprints/tree/main/adlc-agent-evals) |

## Review trigger

When final-answer checks stop being enough, or the project reaches a stable release: move to Trial or remove.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-12 | Assess | Initial entry after the 2026-11-11 evaluation of agent observability and evals. |

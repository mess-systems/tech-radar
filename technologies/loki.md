# Grafana Loki

| Category | Ring | Kind |
|---|---|---|
| [`obs`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source log aggregation system (AGPL-3.0) that indexes labels rather than full log text. Official site: [grafana.com/oss/loki](https://grafana.com/oss/loki/).

## Why mess.systems uses it

The object forms fix its `service_name` label to the application name, alongside the OpenTelemetry `service.name` and the Prometheus `job`.

## Alternatives considered

Other log backends. Chosen because the standard names its label directly.

## Where it applies

- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)

## Review trigger

A change to the observability forms, or a decision to fold `obs` into `infra` (an open question of the standard).

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |

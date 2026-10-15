# Prometheus

| Category | Ring | Kind |
|---|---|---|
| [`obs`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source monitoring system and time-series database (Apache-2.0, CNCF graduated) with a pull-based metrics model. Official site: [prometheus.io](https://prometheus.io/).

## Why mess.systems uses it

The object forms fix its `job` label to the application name, and its alert rules follow `<Domain><Capability><Symptom>`. It provides the `metrics` capability in the worked example.

## Alternatives considered

Other metrics backends that accept the Prometheus data model. Chosen because the standard names its labels directly.

## Where it applies

- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)
- [Services: intake and encoding](https://github.com/mess-systems/naming-standard/blob/main/02-worked-example.md#3-services-intake-and-encoding)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`metrics`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A change to the observability forms, or a decision to fold `obs` into `infra` (an open question of the standard).

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |

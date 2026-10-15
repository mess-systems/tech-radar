# Grafana

| Category | Ring | Kind |
|---|---|---|
| [`obs`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source dashboards and visualisation platform (AGPL-3.0). Official site: [grafana.com/oss/grafana](https://grafana.com/oss/grafana/).

## Why mess.systems uses it

It is the example product for the `dashboards` capability throughout the standard: dashboard folders `<plane>-<domain>`, the `app-dashboards-admin` group, and the worked example's migration of `grafana.corp.lan`.

## Alternatives considered

Other dashboard tools. Adopt: default dashboards.

## Where it applies

- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)
- [App groups](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#33-app-groups-access-to-one-capability)
- [Services: intake and encoding](https://github.com/mess-systems/naming-standard/blob/main/02-worked-example.md#3-services-intake-and-encoding)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`dashboards`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A license or maintenance change upstream, or a better fit for the capability.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Trial | Initial entry. |
| 2026-10-15 | Adopt | Default dashboards for the Prometheus, Loki and Tempo stack. |

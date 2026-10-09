# OpenTelemetry

| Category | Ring | Kind |
|---|---|---|
| [`obs`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Specification |

## What it is

Vendor-neutral observability framework (a CNCF project): APIs, SDKs, a collector, and semantic conventions for traces, metrics, and logs. Official site: [opentelemetry.io](https://opentelemetry.io/).

## Why mess.systems uses it

The naming procedure sets the OTel `service.name` to the application name, so every signal carries the same ID as the IdP, secrets manager, and catalog.

## Alternatives considered

Vendor-specific agents and SDKs. Chosen because it is vendor-neutral and its `service.name` attribute is the common key across backends.

## Where it applies

- [Naming procedure (step D)](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#9-naming-procedure)
- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)

## Review trigger

A change to the OpenTelemetry semantic conventions for `service.name`, or to the observability forms.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |

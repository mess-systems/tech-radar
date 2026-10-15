# OpenTofu

| Category | Ring | Kind |
|---|---|---|
| [`infra`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source infrastructure-as-code tool (MPL-2.0, a Linux Foundation project), forked from Terraform and compatible with its configuration language and providers. Official site: [opentofu.org](https://opentofu.org/).

## Why mess.systems uses it

The object forms define its resource names: `<application>_<env>`.

## Alternatives considered

Terraform: same language, but released under the Business Source License since August 2023. Chosen because it keeps that workflow under an open-source license.

## Where it applies

- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| cross-cutting (platform) | none yet |

## Review trigger

A license or governance change upstream, or loss of provider compatibility.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |

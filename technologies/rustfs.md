# RustFS

| Category | Ring | Kind |
|---|---|---|
| [`infra`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source S3-compatible object storage written in Rust (Apache-2.0). Official site: [rustfs.com](https://rustfs.com/).

## Why mess.systems uses it

Carries the `objects` capability behind the S3 API.

## Alternatives considered

MinIO, Ceph. Chosen for an Apache-2.0 license.

## Where it applies

- [Capability codes: `storage`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`storage`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A license or maintenance change upstream, or a better fit for the capability.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Adopt | Initial entry. |

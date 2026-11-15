# Attic

| Category | Ring | Kind |
|---|---|---|
| [`sdlc`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

Self-hostable Nix binary cache server backed by S3-compatible storage, with multi-tenancy, global deduplication, server-side signing and garbage collection (Apache-2.0). The project describes itself as an early prototype. Official site: [docs.attic.rs](https://docs.attic.rs/).

## Why mess.systems uses it

Design only: a company Nix binary cache on object storage, so that Nix builds are not repeated on every workstation and VM. Harbor does not fit: a Nix binary cache is not an OCI registry. Language package dependencies stay in NORA.

## Alternatives considered

The public Nix cache only. Other Nix binary cache servers: not evaluated yet.

## Where it applies

- [Capability codes: `packages`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`packages`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

The project leaves the early prototype status and the Nix prototype shows a need for a shared cache: move to Trial.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-15 | Assess | Initial entry. |

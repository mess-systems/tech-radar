# Restic

| Category | Ring | Kind |
|---|---|---|
| [`infra`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Backup program in a single executable that supports many storage types, transfers only changed data, encrypts every part of the repository and allows verifying that data can be restored (BSD-2-Clause). Official site: [restic.net](https://restic.net/).

## Why mess.systems uses it

Backs up workstation state that is not in git, dotfiles or the workstation description, to S3-compatible object storage. Everything else is rebuilt rather than restored.

## Alternatives considered

Full-disk backup: answers "keep the data" rather than "get back to work" and also restores a broken state.

## Where it applies

- [Capability codes: `backup`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`backup`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

One cycle of restore drills: promote to Adopt or replace.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-15 | Trial | Initial entry. |

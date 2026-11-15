# Dev Containers

| Category | Ring | Kind |
|---|---|---|
| [`sdlc`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Specification |

## What it is

Open specification (`devcontainer.json`) for using a container as a full-featured development environment, locally or remotely, in a range of supporting tools and editors, and for continuous integration. Official site: [containers.dev](https://containers.dev/).

## Why mess.systems uses it

Development environment where a remote IDE or CI needs a container. Images are built by the CI runners and stored in the company registry; on workstations they run on rootless Podman.

## Alternatives considered

Nix on top of the OS: Assess, prototype in progress. DevPod: no release since 2025-03-10. Toolbx and Distrobox: Assess.

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)
- [Capability codes: `ci`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains), [`ci`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

After a cycle on `eng` and in CI: promote to Adopt, or narrow the scope if Nix on top of the OS becomes the default.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-15 | Trial | Initial entry. |

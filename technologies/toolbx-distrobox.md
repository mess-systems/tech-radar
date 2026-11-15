# Toolbx and Distrobox

| Category | Ring | Kind |
|---|---|---|
| [`device`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

Toolbx runs interactive command-line environments for development and troubleshooting on top of Podman, without installing software on the host. Distrobox runs any Linux distribution in the terminal using podman, docker or lilipod. Official sites: [containertoolbx.org](https://containertoolbx.org/), [distrobox.it](https://distrobox.it/).

## Why mess.systems uses it

Isolated command-line environments, mainly relevant on an image-based OS and for administrator tooling described as code.

## Alternatives considered

Nix on top of the OS and Dev Containers cover developer environments on Ubuntu LTS; a third method is added only if an image-based OS is adopted.

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

Adoption of an image-based OS for `eng` or `paw`: move to Trial; otherwise remove.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-15 | Assess | Initial entry. |

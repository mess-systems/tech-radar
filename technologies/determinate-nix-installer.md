# Determinate Nix Installer

| Category | Ring | Kind |
|---|---|---|
| [`device`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Assess](../README.md#rings) | Product |

## What it is

Installer from Determinate Systems (LGPL-2.1) for Linux, macOS, WSL2 and containers. By default it installs Determinate Nix with flakes enabled; installing upstream Nix with `--prefer-upstream-nix` is described as not a supported configuration. It keeps an installation receipt and removes Nix with `/nix/nix-installer uninstall`. Official site: [github.com/DeterminateSystems/nix-installer](https://github.com/DeterminateSystems/nix-installer).

## Why mess.systems uses it

Installs Nix on top of the workstation OS so that it can be removed with one command if the prototype fails. Determinate Nix, the installer's default, is the chosen Nix distribution.

## Alternatives considered

The upstream Nix installer and upstream Nix: not chosen, the installer describes upstream Nix as not a supported configuration.

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

Results of the Nix prototype, together with the review of the Nix card; a change in the installer's support for upstream Nix.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-15 | Assess | Initial entry. |

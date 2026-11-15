# chezmoi

| Category | Ring | Kind |
|---|---|---|
| [`device`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Manager of user configuration files (dotfiles) across machines, with templates that read values from password managers and secret stores (1Password, Bitwarden, Vault, KeePassXC and others) and encryption with age or gpg (MIT). Official site: [chezmoi.io](https://www.chezmoi.io/).

## Why mess.systems uses it

Restores the user environment on a rebuilt workstation with one command; secrets are referenced in templates, not stored. Use with OpenBao through `vault.command = "bao"` is compatible by the documentation of both projects but not officially stated by chezmoi; to be verified.

## Alternatives considered

Plain git repository with scripts; Home Manager (requires Nix on every device).

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint), [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

Verification with OpenBao and one cycle of workstation rebuild drills: promote to Adopt or move to Hold.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-15 | Trial | Initial entry. |

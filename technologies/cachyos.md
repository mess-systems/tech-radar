# CachyOS

| Category | Ring | Kind |
|---|---|---|
| [`device`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Hold](../README.md#rings) | Product |

## What it is

Rolling-release Linux distribution based on Arch Linux. Packages are built for x86-64-v3, x86-64-v4 and Zen4 with LTO, core packages with PGO and BOLT; the linux-cachyos kernel offers a choice of schedulers. Official site: [cachyos.org](https://cachyos.org/).

## Why mess.systems uses it

No new adoption on company workstations. Rolling releases and the latest kernel are a deliberate choice for performance and lab work, not for a managed fleet: kernel and out-of-tree module regressions reach the device as fast as fixes do. Existing lab workstations may continue with a fallback long-term kernel, the safeguards of the blueprint and Fleet enrollment.

## Alternatives considered

Ubuntu LTS: Adopt, base of all profiles. Omarchy: Assess, also rolling Arch, assessed for its delayed stable mirror and snapshot rollback.

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint), [`device-workstation-stages`](https://github.com/mess-systems/blueprints/tree/main/device-workstation-stages) |

## Review trigger

Remove the entry when no company workstation runs it; reassess only if the distribution offers a supported long-term track.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-15 | Hold | Initial entry. |

# Harbor

| Category | Ring | Kind |
|---|---|---|
| [`sdlc`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source container registry (Apache-2.0, CNCF graduated) with projects, robot accounts, replication, and vulnerability scanning. Official site: [goharbor.io](https://goharbor.io/).

## Why mess.systems uses it

It is the example registry for the `oci` capability: registry projects are named `<plane>-<domain>`, robot accounts `robot$<project>+<consumer-id>`.

## Alternatives considered

Registries built into git forges, or cloud registries. Adopt: default OCI registry; NORA covers other package formats.

## Where it applies

- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)
- [Tokens, robots, credentials IDs](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#12-tokens-robots-credentials-ids)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`oci`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A license or maintenance change upstream, or a better fit for the capability.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Trial | Initial entry. |
| 2026-10-15 | Adopt | Default OCI registry. |

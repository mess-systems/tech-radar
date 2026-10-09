# Harbor

| Category | Ring | Kind |
|---|---|---|
| [`sdlc`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Open-source container registry (Apache-2.0, CNCF graduated) with projects, robot accounts, replication, and vulnerability scanning. Official site: [goharbor.io](https://goharbor.io/).

## Why mess.systems uses it

It is the example registry for the `oci` capability: registry projects are named `<plane>-<domain>`, robot accounts `robot$<project>+<consumer-id>`.

## Alternatives considered

Registries built into git forges, or cloud registries. Trial because the standard names it as an illustration.

## Where it applies

- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)
- [Tokens, robots, credentials IDs](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#12-tokens-robots-credentials-ids)

## Review trigger

After it has carried the `oci` capability in a limited scope: promote to Adopt or move to Hold.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Trial | Initial entry. |

# Podman

| Category | Ring | Kind |
|---|---|---|
| [`infra`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Daemonless, rootless container engine compatible with OCI images and the Docker CLI (Apache-2.0). Official site: [podman.io](https://podman.io/).

## Why mess.systems uses it

Container runtime on engineering devices for dev containers and sandboxes for CLI agents. It has no permanent daemon, so it is not a resident agent and keeps the agent count on a device low.

## Alternatives considered

Docker Engine and Docker Desktop: a permanent root daemon, and Docker Desktop licensing for companies. Trial: limited to the `eng` endpoint profile.

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)
- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms) (images)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |

## Review trigger

After dev containers and agent sandboxes have run on `eng` devices for a cycle: promote to Adopt or move to Hold.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Trial | Initial entry. |

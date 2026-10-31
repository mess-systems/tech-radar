# Docker

| Category | Ring | Kind |
|---|---|---|
| [`device`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Container platform for building and running OCI images. Docker Engine is open source, built from the Moby project (Apache-2.0); it runs as a daemon, as root by default or as a non-root user in rootless mode. Docker Desktop is distributed under the Docker Subscription Service Agreement: free for organizations with fewer than 250 employees and less than $10 million in annual revenue, paid otherwise. Official site: [docker.com](https://www.docker.com/).

## Why mess.systems uses it

Default container engine for building and running images. Podman remains in Trial as the alternative on `eng` devices.

## Alternatives considered

[Podman](podman.md): daemonless and rootless, compatible with OCI images and the Docker CLI; Trial, limited to the `eng` endpoint profile.

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)
- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms) (images)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | none yet |

## Review trigger

A change to the Docker Desktop license terms, or Podman moves to Adopt for the same scope.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-31 | Adopt | Initial entry. |

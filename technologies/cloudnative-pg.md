# CloudNativePG

| Category | Ring | Kind |
|---|---|---|
| [`infra`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source Kubernetes operator for PostgreSQL (Apache-2.0). Declares clusters as custom resources, runs continuous physical backup and WAL archiving to an object store through Barman Cloud (in-tree `barmanObjectStore`, and from 1.26 the Barman Cloud Plugin / `ObjectStore`), and restores with Point-in-Time Recovery. A CNCF Incubating project (accepted to Sandbox 2025-01-21; Incubating 2026-11-02). Official site: [cloudnative-pg.io](https://cloudnative-pg.io/).

## Why mess.systems uses it

Default way to run [PostgreSQL](postgresql.md) on Kubernetes in the Enterprise Homelab and beyond: declarative clusters, continuous backup, and restore without a separate classical Barman host. Backup encryption at rest uses the object store's server-side options (`AES256`, `aws:kms`); client-side encryption before upload is not available in barman-cloud yet.

## Alternatives considered

A classical Barman server beside the cluster; vendor-managed PostgreSQL; other Kubernetes operators for Postgres. Chosen as the target operator stack for Postgres on Kubernetes.

## Where it applies

- [Capability codes: `k8s`, `backup`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)
- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)
- [PostgreSQL](postgresql.md)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| `k8s`, `backup` | none yet |

## Review trigger

Client-side encryption in barman-cloud, a change to the CNCF or license status, or a better fit as the default Postgres operator on Kubernetes.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-05 | Adopt | Initial entry; target Postgres-on-Kubernetes stack. |

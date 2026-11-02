# Cube

| Category | Ring | Kind |
|---|---|---|
| [`data`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Open-source semantic layer (Cube Core, Apache-2.0, some components MIT; Cube Store, Apache-2.0). Measures, dimensions and joins are defined once in YAML or JavaScript files kept in git, and consumers read them through a Postgres-compatible SQL API, a REST API or a GraphQL API. Access is checked on the layer through a security context, access policies and row-level filters. Pre-aggregations are built into Cube Store and answer matching queries without querying the source. Self-hosted with Docker; Cube Cloud is the vendor's commercial hosted service. Official site: [cube.dev](https://cube.dev/), documentation: [docs.cube.dev](https://docs.cube.dev/).

## Why mess.systems uses it

It is the product of the proposed `semantic` capability in the [`semantic-layer-cube`](https://github.com/mess-systems/blueprints/tree/main/semantic-layer-cube) blueprint: one definition of each metric in front of the dbt marts in the PostgreSQL warehouse, read by Superset and Grafana as if it were a PostgreSQL database, with no plugin in either tool. Consumers stay the same when the source changes, because they depend on the model, not on the tables.

Trial, not Adopt:

- Open-source Cube Store has no replication; if any node is down, the Cube Store cluster is down. High availability needs fully independent clusters.
- In Cube Core, groups for access policies are mapped by hand (`context_to_groups`); user attributes are Cube Cloud only.
- The SQL API declines TLS and receives passwords in cleartext, so it depends on an encrypted network path.
- The Grafana Cube plugin is marked experimental and "not for production use"; Grafana uses the PostgreSQL data source instead.
- It adds a new server component, and it has been used in one evaluation only.

## Alternatives considered

Metric definitions inside each BI tool (they drift apart between tools); PostgreSQL views and materialized views (shared SQL, but no REST or GraphQL, no layer access policies, no cache that answers while the source is down); the dbt semantic layer (MetricFlow), not evaluated yet; Cube Cloud (vendor-hosted control plane). Trial: semantic layer in front of the warehouse.

## Where it applies

- [Capability codes](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) (`semantic` proposed, not yet registered)
- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)
- [Database roles](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#11-database-roles)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| `semantic` (proposed) | [`semantic-layer-cube`](https://github.com/mess-systems/blueprints/tree/main/semantic-layer-cube) |

## Review trigger

Replication in open-source Cube Store, TLS in the SQL API, a production-ready Grafana plugin, a license change upstream, or a second use of the layer beyond the first scope (move to Adopt or Hold).

## History

| Date | Ring | Change |
|---|---|---|
| 2026-11-02 | Trial | Initial entry. |

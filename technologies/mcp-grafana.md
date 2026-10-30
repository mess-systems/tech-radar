# mcp-grafana

| Category | Ring | Kind |
|---|---|---|
| [`obs`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Open-source [Model Context Protocol](mcp.md) server for [Grafana](grafana.md) (Apache-2.0, written in Go, maintained by Grafana Labs). It exposes Grafana dashboards, datasources, and queries as MCP tools, including PromQL queries against [Prometheus](prometheus.md) and LogQL queries against [Loki](loki.md). Tool categories can be switched off one by one, and the [`--disable-write` flag](https://github.com/grafana/mcp-grafana#read-only-mode) removes write tools and raw SQL query tools. Source and releases: [github.com/grafana/mcp-grafana](https://github.com/grafana/mcp-grafana).

## Why mess.systems uses it

It is the MCP target `dashboards` behind the AI gateway: agents query metrics and logs through Grafana datasources on behalf of a person, without direct access to Prometheus or Loki. mess.systems runs it with `--disable-write` and only the Prometheus and Loki tool categories. Datasource credentials stay in Grafana and are not visible to the agent.

## Alternatives considered

- Separate MCP servers per backend (one for Prometheus, one for Loki): more targets to secure and audit. Not chosen.
- Direct HTTP access from agents to the Prometheus and Loki APIs: bypasses the gateway and its audit. Rejected.

Trial: in use only for read-only agent queries, with the gateway in front.

## Where it applies

- [Capability codes: `dashboards`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)
- [Object forms: MCP target](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`dashboards`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`obs-mcp-readonly`](https://github.com/mess-systems/blueprints/tree/main/obs-mcp-readonly) |

## Review trigger

A release that changes `--disable-write` or adds write behaviour to read tools; a license or ownership change; or a limited-scope run that is long enough to promote it to Adopt or move it to Hold.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-30 | Trial | Initial entry: MCP target `dashboards` in the `obs-mcp-readonly` blueprint. |

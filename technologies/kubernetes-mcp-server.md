# kubernetes-mcp-server

| Category | Ring | Kind |
|---|---|---|
| [`infra`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Open-source [Model Context Protocol](mcp.md) server for Kubernetes and OpenShift (Apache-2.0, written in Go, in the [containers](https://github.com/containers) organization on GitHub). It talks to the Kubernetes API directly rather than wrapping `kubectl` or `helm`, and groups its tools into toolsets (`core`, `config`, `helm` and others). Runtime settings come from a [TOML configuration file](https://github.com/containers/kubernetes-mcp-server/blob/main/docs/configuration.md), including a read-only mode and a list of denied resource kinds. Source and releases: [github.com/containers/kubernetes-mcp-server](https://github.com/containers/kubernetes-mcp-server).

## Why mess.systems uses it

It is the MCP target `k8s` behind the AI gateway: agents read resources, events, and pod logs on behalf of a person. mess.systems runs it with `read_only = true`, the `core` toolset only, and `Secret` in `denied_resources`, on top of a read-only ClusterRole without `secrets`. The server itself also offers write, `exec`, and Helm tools; the read-only configuration is what makes it fit the capability.

## Alternatives considered

- Wrappers that run `kubectl` for the agent: simpler, but permission control then depends on whatever the command line allows. Not chosen.
- No MCP server: agents get no cluster access and people copy output by hand. Rejected because it removes the audit trail the gateway provides.

Trial: in use only for read-only agent access, with the gateway in front.

## Where it applies

- [Capability codes: `k8s`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)
- [Object forms: MCP target](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`k8s`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`obs-mcp-readonly`](https://github.com/mess-systems/blueprints/tree/main/obs-mcp-readonly) |

## Review trigger

A release that changes the read-only mode or `denied_resources`; a license or ownership change; or a limited-scope run that is long enough to promote it to Adopt or move it to Hold.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-30 | Trial | Initial entry: MCP target `k8s` in the `obs-mcp-readonly` blueprint. |

# Model Context Protocol

| Category | Ring | Kind |
|---|---|---|
| [`ai`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Specification |

## What it is

Open protocol for connecting AI applications and agents to tools and data sources through MCP servers. Official site: [modelcontextprotocol.io](https://modelcontextprotocol.io/).

## Why mess.systems uses it

The standard names MCP targets on the gateway by capability code (`convert`, `cmdb`) and external providers as `<vendor>-<service>`.

## Alternatives considered

Provider-specific tool-calling integrations. Chosen because one protocol lets the gateway name every tool target the same way.

## Where it applies

- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms)
- [Gateway client identities](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#9-gateway-client-identities)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| not mapped yet | none yet |

## Review trigger

A breaking revision of the protocol, or a change to the MCP target form.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-09 | Adopt | Initial entry. |

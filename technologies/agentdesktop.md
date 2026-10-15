# agentdesktop

| Category | Ring | Kind |
|---|---|---|
| [`ai`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Trial](../README.md#rings) | Product |

## What it is

Open-source governance layer for AI tools on employee devices: a daemon on each device discovers AI clients, inventories MCP servers and skills, applies managed settings and sandbox policy, and connects clients to an LLM gateway with short-lived credentials. Official site: [agentdesktop.dev](https://agentdesktop.dev/).

## Why mess.systems uses it

Everyone uses AI, so AI clients on every device that has them are controlled the same way: one place for their settings, and model traffic goes through the company AI gateway ([agentgateway](agentgateway.md)) so provider keys never reach a device.

## Alternatives considered

Per-tool managed settings pushed by the device management tool. Rejected: every client has its own format and there is no device identity towards the gateway. Trial: young project, deployed on the `std` and `eng` endpoint profiles, not on privileged-access workstations, which have no AI clients.

## Where it applies

- [Capability codes: `endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains)
- [Gateway client identities](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#9-gateway-client-identities)
- [Endpoint conventions](https://github.com/mess-systems/naming-standard/blob/main/06-endpoint-conventions.md)

## Capabilities and blueprints

| Capabilities | Blueprints |
|---|---|
| [`endpoint`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |

## Review trigger

After a full cycle on `std` and `eng` devices: promote to Adopt, or replace it with managed settings from the device management tool.

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-15 | Trial | Initial entry. |

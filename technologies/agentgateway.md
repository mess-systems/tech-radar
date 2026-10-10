# agentgateway

| Category | Ring | Kind |
|---|---|---|
| [`ai`](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) | [Adopt](../README.md#rings) | Product |

## What it is

Open-source gateway (Apache-2.0, written in Rust) for AI traffic: agent-to-LLM, agent-to-tool over the [Model Context Protocol](mcp.md), and agent-to-agent over [A2A](https://a2a-protocol.org/). It puts authentication (JWT, API keys, OAuth, OIDC), CEL-based authorization, rate limits, budgets and spend tracking, guardrails, and OpenTelemetry metrics, logs, and traces in front of those connections. It runs as a standalone binary with YAML configuration or on Kubernetes with its own controller and the Gateway API. Created by Solo.io, [accepted by the Linux Foundation](https://www.linuxfoundation.org/press/linux-foundation-welcomes-agentgateway-project-to-accelerate-ai-agent-adoption-while-maintaining-security-observability-and-governance) in August 2025, and since June 2026 [hosted by the Agentic AI Foundation](https://aaif.io/blog/agentgateway-joins-aaif-as-an-open-gateway-for-agentic-ai-infrastructure). Official site: [agentgateway.dev](https://agentgateway.dev/). Source and releases: [github.com/agentgateway/agentgateway](https://github.com/agentgateway/agentgateway).

## Why mess.systems uses it

It is the target product for the `gateway` capability (`gateway.ai.corp`): the single point through which people, services, and agents reach models, MCP tools, and other agents. One gateway for all three kinds of traffic means one place for client identities, policies, keys, budgets, and audit, instead of a separate proxy per protocol. Vendor-neutral governance and a permissive license keep the choice open for anyone who reuses the standard.

## Alternatives considered

- [LiteLLM](litellm.md): a mature LLM gateway with an OpenAI-compatible API, virtual keys, and budgets. Its repository is MIT-licensed except for an `enterprise/` directory under a separate license. Moved to Hold: mess.systems wants one gateway for LLM, MCP, and A2A traffic under neutral foundation governance.
- [Agent Router](https://theagentrouter.ai/), formerly Envoy AI Gateway (Apache-2.0, Agentic AI Foundation): a control plane for AI traffic on top of [Envoy Gateway](https://gateway.envoyproxy.io/). Covers models and MCP tools; its README does not mention A2A, which mess.systems needs in the same gateway.
- [Kong Gateway](https://github.com/Kong/kong) (Apache-2.0), which describes itself as "the API and AI gateway": a general-purpose API gateway extended with AI plugins. Not chosen because mess.systems prefers a gateway built around agent protocols over a general API gateway with AI add-ons.

## Where it applies

- [Capability codes](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) (`gateway`)
- [Object forms](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#5-object-forms) (route prefixes `<provider-short>/<model>`, MCP targets)
- [Worked example: an LLM gateway](https://github.com/mess-systems/naming-standard/blob/main/03-secrets-conventions.md#8-worked-example-an-llm-gateway)
- [Gateway client identities](https://github.com/mess-systems/naming-standard/blob/main/04-identity-conventions.md#9-gateway-client-identities)

The worked examples in the naming standard still use LiteLLM as the illustrative product name; the rules do not depend on the product.

## Review trigger

A license or governance change of the project; a breaking change in MCP or A2A support; or a release that removes a capability the standard relies on (client identities, per-key budgets, MCP federation).

## History

| Date | Ring | Change |
|---|---|---|
| 2026-10-10 | Adopt | Initial entry: target product for the `gateway` capability, replacing LiteLLM. |

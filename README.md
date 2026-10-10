# mess.systems tech radar

The technology radar of **mess.systems**: which products and specifications the organisation uses, how firmly, and why.

It is a simplified radar in plain Markdown: one table, three rings, and one card per technology. There is no site and no generator; the files in this repository are the radar.

The radar covers the technologies named in the [mess.systems naming standard](https://github.com/mess-systems/naming-standard). Each card links back to the sections of the standard that name it.

## Rings

| Ring | Meaning |
|---|---|
| **Adopt** | The default choice. New work uses it unless a recorded reason says otherwise. |
| **Trial** | In use within a limited scope. New use outside that scope needs a reason. |
| **Hold** | No new adoption. Existing use may continue until it is replaced. |

There is no "Assess" ring: a technology enters the radar when it is used, not when it is being considered.

## Categories

Categories are the [domain codes](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) of the naming standard, so the radar and the standard use one vocabulary. Each card names the capability it serves, taken from the standard's [capability codes](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains).

| Code | Domain |
|---|---|
| `iam` | identity, access, PKI, secrets, passwords |
| `net` | DNS, mesh, edge, firewall |
| `infra` | compute, storage, backup, hypervisor |
| `sdlc` | code, CI, artifacts, GitOps |
| `obs` | metrics, logs, traces, alerting |
| `ai` | inference, gateway, speech, vision, agents |
| `data` | warehouse, pipelines, catalog, BI, document store |
| `collab` | chat, wiki, docs, video |

Codes from the standard that have no entry yet are not listed.

## Radar

| Technology | Category | Ring | Card |
|---|---|---|---|
| [ACME](technologies/acme.md) | `iam` | Adopt | [acme.md](technologies/acme.md) |
| [OpenBao](technologies/openbao.md) | `iam` | Adopt | [openbao.md](technologies/openbao.md) |
| [OpenID Connect](technologies/oidc.md) | `iam` | Adopt | [oidc.md](technologies/oidc.md) |
| [SPIFFE](technologies/spiffe.md) | `iam` | Adopt | [spiffe.md](technologies/spiffe.md) |
| [WebAuthn](technologies/webauthn.md) | `iam` | Adopt | [webauthn.md](technologies/webauthn.md) |
| [Keycloak](technologies/keycloak.md) | `iam` | Trial | [keycloak.md](technologies/keycloak.md) |
| [SPIRE](technologies/spire.md) | `iam` | Trial | [spire.md](technologies/spire.md) |
| [HashiCorp Vault](technologies/vault.md) | `iam` | Hold | [vault.md](technologies/vault.md) |
| [Headscale](technologies/headscale.md) | `net` | Trial | [headscale.md](technologies/headscale.md) |
| [Ansible](technologies/ansible.md) | `infra` | Adopt | [ansible.md](technologies/ansible.md) |
| [Kubernetes](technologies/kubernetes.md) | `infra` | Adopt | [kubernetes.md](technologies/kubernetes.md) |
| [OpenTofu](technologies/opentofu.md) | `infra` | Adopt | [opentofu.md](technologies/opentofu.md) |
| [Argo CD](technologies/argo-cd.md) | `sdlc` | Trial | [argo-cd.md](technologies/argo-cd.md) |
| [Gitea](technologies/gitea.md) | `sdlc` | Trial | [gitea.md](technologies/gitea.md) |
| [Harbor](technologies/harbor.md) | `sdlc` | Trial | [harbor.md](technologies/harbor.md) |
| [Jenkins](technologies/jenkins.md) | `sdlc` | Trial | [jenkins.md](technologies/jenkins.md) |
| [Grafana Loki](technologies/loki.md) | `obs` | Adopt | [loki.md](technologies/loki.md) |
| [OpenTelemetry](technologies/opentelemetry.md) | `obs` | Adopt | [opentelemetry.md](technologies/opentelemetry.md) |
| [Prometheus](technologies/prometheus.md) | `obs` | Adopt | [prometheus.md](technologies/prometheus.md) |
| [Grafana](technologies/grafana.md) | `obs` | Trial | [grafana.md](technologies/grafana.md) |
| [agentgateway](technologies/agentgateway.md) | `ai` | Adopt | [agentgateway.md](technologies/agentgateway.md) |
| [Model Context Protocol](technologies/mcp.md) | `ai` | Adopt | [mcp.md](technologies/mcp.md) |
| [Langfuse](technologies/langfuse.md) | `ai` | Trial | [langfuse.md](technologies/langfuse.md) |
| [LiteLLM](technologies/litellm.md) | `ai` | Hold | [litellm.md](technologies/litellm.md) |
| [ClickHouse](technologies/clickhouse.md) | `data` | Adopt | [clickhouse.md](technologies/clickhouse.md) |
| [dbt](technologies/dbt.md) | `data` | Adopt | [dbt.md](technologies/dbt.md) |
| [PostgreSQL](technologies/postgresql.md) | `data` | Adopt | [postgresql.md](technologies/postgresql.md) |
| [S3 API](technologies/s3.md) | `data` | Adopt | [s3.md](technologies/s3.md) |
| [Apache Superset](technologies/superset.md) | `data` | Trial | [superset.md](technologies/superset.md) |
| [MongoDB](technologies/mongodb.md) | `data` | Trial | [mongodb.md](technologies/mongodb.md) |
| [Mattermost](technologies/mattermost.md) | `collab` | Trial | [mattermost.md](technologies/mattermost.md) |
| [Wiki.js](technologies/wikijs.md) | `collab` | Trial | [wikijs.md](technologies/wikijs.md) |

## Cards

Every card in [technologies/](technologies/) has the same sections:

- **What it is**: two or three lines and a link to the official site.
- **Why mess.systems uses it**: the role it plays, tied to the naming standard.
- **Alternatives considered**: comparable options and why this one.
- **Where it applies**: links to the sections of the naming standard that name it.
- **Review trigger**: the event that reopens the decision.
- **History**: every ring change with its date.

## Changing the radar

A ring change, a new entry, or a removal is a pull request with a short rationale. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Text licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE) ([license deed](https://creativecommons.org/licenses/by/4.0/)). You may share and adapt it, including commercially, with attribution: "mess.systems tech radar (https://github.com/mess-systems/tech-radar), CC BY 4.0".

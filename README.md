# mess.systems tech radar

The technology radar of **mess.systems**: which products and specifications the organisation uses, how firmly, and why.

It is a simplified radar in plain Markdown: one table, four rings, and one card per technology. There is no site and no generator; the files in this repository are the radar.

The radar covers the technologies named in the [mess.systems naming standard](https://github.com/mess-systems/naming-standard). Each card links back to the sections of the standard that name it.

## Rings

| Ring | Meaning |
|---|---|
| **Adopt** | The default choice. New work uses it unless a recorded reason says otherwise. |
| **Trial** | In use within a limited scope. New use outside that scope needs a reason. |
| **Assess** | Being evaluated. Not for production use until it moves to Trial or Adopt. |
| **Hold** | No new adoption. Existing use may continue until it is replaced. |

A technology may enter the radar at Assess while it is being evaluated; it leaves Assess for Trial, Adopt, or removal.

## Categories

Categories are the [domain codes](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#42-domains) of the naming standard, so the radar and the standard use one vocabulary. Each card names the capabilities it serves and the [blueprints](https://github.com/mess-systems/blueprints) it takes part in; capabilities are taken from the standard's [capability codes](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains).

| Code | Domain |
|---|---|
| `iam` | identity, access, PKI, secrets, passwords |
| `gov` | architecture, policy, CMDB, ADRs |
| `sec` | detection, vuln mgmt, SIEM |
| `net` | DNS, mesh, edge, firewall |
| `infra` | compute, storage, backup, hypervisor |
| `sdlc` | code, CI, artifacts, GitOps |
| `adlc` | AI/agent lifecycle, evals, policy sidecars |
| `obs` | metrics, logs, traces, alerting |
| `ai` | inference, gateway, speech, vision, agents |
| `data` | warehouse, pipelines, catalog, BI, document store |
| `itsm` | service desk, change |
| `collab` | chat, wiki, docs, video |

Codes from the standard that have no entry yet are not listed.

## Radar

| Technology | Category | Ring | Card | Capabilities | Blueprints |
|---|---|---|---|---|---|
| [ACME](technologies/acme.md) | `iam` | Adopt | [acme.md](technologies/acme.md) | `pki` |   |
| [Authentik](technologies/authentik.md) | `iam` | Adopt | [authentik.md](technologies/authentik.md) | `sso` |   |
| [OpenBao](technologies/openbao.md) | `iam` | Adopt | [openbao.md](technologies/openbao.md) | `secrets` |   |
| [OpenID Connect](technologies/oidc.md) | `iam` | Adopt | [oidc.md](technologies/oidc.md) | `sso` |   |
| [SPIFFE](technologies/spiffe.md) | `iam` | Adopt | [spiffe.md](technologies/spiffe.md) | `spiffe` |   |
| [WebAuthn](technologies/webauthn.md) | `iam` | Adopt | [webauthn.md](technologies/webauthn.md) | `sso` |   |
| [Keycloak](technologies/keycloak.md) | `iam` | Trial | [keycloak.md](technologies/keycloak.md) | `sso` |   |
| [Pomerium](technologies/pomerium.md) | `iam` | Trial | [pomerium.md](technologies/pomerium.md) | `sso` |   |
| [SPIRE](technologies/spire.md) | `iam` | Trial | [spire.md](technologies/spire.md) | `endpoint`, `spiffe` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [FreeIPA](technologies/freeipa.md) | `iam` | Assess | [freeipa.md](technologies/freeipa.md) | `directory` |   |
| [Vaultwarden](technologies/vaultwarden.md) | `iam` | Assess | [vaultwarden.md](technologies/vaultwarden.md) | `passwords` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [Zitadel](technologies/zitadel.md) | `iam` | Assess | [zitadel.md](technologies/zitadel.md) | `b2b` |   |
| [Teleport](technologies/teleport.md) | `iam` | Hold | [teleport.md](technologies/teleport.md) | `sso` |   |
| [Open Policy Agent](technologies/opa.md) | `gov` | Adopt | [opa.md](technologies/opa.md) | `policy` |   |
| [NetBox](technologies/netbox.md) | `gov` | Trial | [netbox.md](technologies/netbox.md) | `cmdb` |   |
| [Opengrep](technologies/opengrep.md) | `sec` | Adopt | [opengrep.md](technologies/opengrep.md) | `scan` |   |
| [Suricata](technologies/suricata.md) | `sec` | Adopt | [suricata.md](technologies/suricata.md) | `ids` |   |
| [Trivy](technologies/trivy.md) | `sec` | Adopt | [trivy.md](technologies/trivy.md) | `scan` |   |
| [Wazuh](technologies/wazuh.md) | `sec` | Adopt | [wazuh.md](technologies/wazuh.md) | `endpoint`, `siem` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [Cilium](technologies/cilium.md) | `net` | Adopt | [cilium.md](technologies/cilium.md) | `firewall` |   |
| [Keenetic](technologies/keenetic.md) | `net` | Adopt | [keenetic.md](technologies/keenetic.md) | `firewall` |   |
| [MikroTik](technologies/mikrotik.md) | `net` | Adopt | [mikrotik.md](technologies/mikrotik.md) | `firewall` |   |
| [NetBird](technologies/netbird.md) | `net` | Adopt | [netbird.md](technologies/netbird.md) | `endpoint`, `mesh` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [Ansible](technologies/ansible.md) | `infra` | Adopt | [ansible.md](technologies/ansible.md) |   | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [Kubernetes](technologies/kubernetes.md) | `infra` | Adopt | [kubernetes.md](technologies/kubernetes.md) | `k8s` |   |
| [OpenTofu](technologies/opentofu.md) | `infra` | Adopt | [opentofu.md](technologies/opentofu.md) |   |   |
| [Proxmox VE](technologies/proxmox-ve.md) | `infra` | Adopt | [proxmox-ve.md](technologies/proxmox-ve.md) | `compute` |   |
| [RustFS](technologies/rustfs.md) | `infra` | Adopt | [rustfs.md](technologies/rustfs.md) | `storage` |   |
| [WinBoat](technologies/winboat.md) | `infra` | Adopt | [winboat.md](technologies/winboat.md) | `endpoint` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [Fleet](technologies/fleet.md) | `infra` | Trial | [fleet.md](technologies/fleet.md) | `endpoint` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [Podman](technologies/podman.md) | `infra` | Trial | [podman.md](technologies/podman.md) | `endpoint` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [kind and k3s](technologies/k3s.md) | `infra` | Assess | [k3s.md](technologies/k3s.md) | `k8s` |   |
| [Argo CD](technologies/argo-cd.md) | `sdlc` | Adopt | [argo-cd.md](technologies/argo-cd.md) | `gitops` |   |
| [Forgejo](technologies/forgejo.md) | `sdlc` | Adopt | [forgejo.md](technologies/forgejo.md) | `git` |   |
| [Harbor](technologies/harbor.md) | `sdlc` | Adopt | [harbor.md](technologies/harbor.md) | `oci` |   |
| [NORA](technologies/nora.md) | `sdlc` | Adopt | [nora.md](technologies/nora.md) | `hub-cache` |   |
| [SonarQube](technologies/sonarqube.md) | `sdlc` | Adopt | [sonarqube.md](technologies/sonarqube.md) | `scan` |   |
| [Unleash](technologies/unleash.md) | `sdlc` | Adopt | [unleash.md](technologies/unleash.md) | `flags` |   |
| [Jenkins](technologies/jenkins.md) | `sdlc` | Assess | [jenkins.md](technologies/jenkins.md) | `ci` |   |
| [Alertmanager](technologies/alertmanager.md) | `obs` | Adopt | [alertmanager.md](technologies/alertmanager.md) | `alerts` |   |
| [Grafana](technologies/grafana.md) | `obs` | Adopt | [grafana.md](technologies/grafana.md) | `dashboards` |   |
| [Grafana Loki](technologies/loki.md) | `obs` | Adopt | [loki.md](technologies/loki.md) | `logs` |   |
| [Grafana Tempo](technologies/tempo.md) | `obs` | Adopt | [tempo.md](technologies/tempo.md) | `traces` |   |
| [OpenLLMetry](technologies/openllmetry.md) | `obs` | Adopt | [openllmetry.md](technologies/openllmetry.md) | `llm-traces` |   |
| [OpenTelemetry](technologies/opentelemetry.md) | `obs` | Adopt | [opentelemetry.md](technologies/opentelemetry.md) |   |   |
| [Prometheus](technologies/prometheus.md) | `obs` | Adopt | [prometheus.md](technologies/prometheus.md) | `metrics` |   |
| [Telegraf](technologies/telegraf.md) | `obs` | Trial | [telegraf.md](technologies/telegraf.md) | `metrics` |   |
| [Zabbix](technologies/zabbix.md) | `obs` | Assess | [zabbix.md](technologies/zabbix.md) | `alerts` |   |
| [CubeSandbox](technologies/cubesandbox.md) | `adlc` | Adopt | [cubesandbox.md](technologies/cubesandbox.md) | `sandbox` |   |
| [DeepEval](technologies/deepeval.md) | `adlc` | Adopt | [deepeval.md](technologies/deepeval.md) | `evals` |   |
| [agentregistry](technologies/agentregistry.md) | `adlc` | Trial | [agentregistry.md](technologies/agentregistry.md) | `registry` |   |
| [promptfoo](technologies/promptfoo.md) | `adlc` | Trial | [promptfoo.md](technologies/promptfoo.md) | `evals` |   |
| [agentgateway](technologies/agentgateway.md) | `ai` | Adopt | [agentgateway.md](technologies/agentgateway.md) | `gateway` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [Langfuse](technologies/langfuse.md) | `ai` | Adopt | [langfuse.md](technologies/langfuse.md) | `llm-traces` |   |
| [LangGraph](technologies/langgraph.md) | `ai` | Adopt | [langgraph.md](technologies/langgraph.md) | `inference` |   |
| [LiveKit](technologies/livekit.md) | `ai` | Adopt | [livekit.md](technologies/livekit.md) | `stt` |   |
| [Model Context Protocol](technologies/mcp.md) | `ai` | Adopt | [mcp.md](technologies/mcp.md) |   |   |
| [TinyFish](technologies/tinyfish.md) | `ai` | Adopt | [tinyfish.md](technologies/tinyfish.md) | `inference` |   |
| [Unsloth](technologies/unsloth.md) | `ai` | Adopt | [unsloth.md](technologies/unsloth.md) | `inference` |   |
| [vLLM](technologies/vllm.md) | `ai` | Adopt | [vllm.md](technologies/vllm.md) | `inference` |   |
| [DeepSeek Harness](technologies/deepseek-harness.md) | `ai` | Trial | [deepseek-harness.md](technologies/deepseek-harness.md) | `inference` |   |
| [kagent](technologies/kagent.md) | `ai` | Trial | [kagent.md](technologies/kagent.md) | `inference` |   |
| [Langflow](technologies/langflow.md) | `ai` | Trial | [langflow.md](technologies/langflow.md) | `inference` |   |
| [Laya](technologies/laya.md) | `ai` | Trial | [laya.md](technologies/laya.md) | `guard` |   |
| [agentdesktop](technologies/agentdesktop.md) | `ai` | Trial | [agentdesktop.md](technologies/agentdesktop.md) | `endpoint` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [LibreChat](technologies/librechat.md) | `ai` | Trial | [librechat.md](technologies/librechat.md) | `chat` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [Onyx](technologies/onyx.md) | `ai` | Trial | [onyx.md](technologies/onyx.md) | `kb` |   |
| [llama.cpp](technologies/llama-cpp.md) | `ai` | Assess | [llama-cpp.md](technologies/llama-cpp.md) | `inference` |   |
| [Mem0](technologies/mem0.md) | `ai` | Assess | [mem0.md](technologies/mem0.md) | `kb` |   |
| [LiteLLM](technologies/litellm.md) | `ai` | Hold | [litellm.md](technologies/litellm.md) | `gateway` |   |
| [Activepieces](technologies/activepieces.md) | `data` | Adopt | [activepieces.md](technologies/activepieces.md) | `orchestrate` |   |
| [Apache Airflow](technologies/airflow.md) | `data` | Adopt | [airflow.md](technologies/airflow.md) | `orchestrate` |   |
| [Apache CouchDB](technologies/couchdb.md) | `data` | Adopt | [couchdb.md](technologies/couchdb.md) | `docstore` |   |
| [Apache Superset](technologies/superset.md) | `data` | Adopt | [superset.md](technologies/superset.md) | `bi` |   |
| [ClickHouse](technologies/clickhouse.md) | `data` | Adopt | [clickhouse.md](technologies/clickhouse.md) | `warehouse` |   |
| [dbt](technologies/dbt.md) | `data` | Adopt | [dbt.md](technologies/dbt.md) | `transform` |   |
| [DuckDB](technologies/duckdb.md) | `data` | Adopt | [duckdb.md](technologies/duckdb.md) | `sql` |   |
| [MarkItDown](technologies/markitdown.md) | `data` | Adopt | [markitdown.md](technologies/markitdown.md) | `convert` |   |
| [OpenMetadata](technologies/openmetadata.md) | `data` | Adopt | [openmetadata.md](technologies/openmetadata.md) | `data-catalog` |   |
| [PostgreSQL](technologies/postgresql.md) | `data` | Adopt | [postgresql.md](technologies/postgresql.md) |   |   |
| [S3 API](technologies/s3.md) | `data` | Adopt | [s3.md](technologies/s3.md) | `objects` |   |
| [Temporal](technologies/temporal.md) | `data` | Adopt | [temporal.md](technologies/temporal.md) | `orchestrate` |   |
| [Qdrant](technologies/qdrant.md) | `data` | Assess | [qdrant.md](technologies/qdrant.md) | `kb` |   |
| [SurrealDB](technologies/surrealdb.md) | `data` | Assess | [surrealdb.md](technologies/surrealdb.md) | `docstore` |   |
| [DataHub](technologies/datahub.md) | `data` | Hold | [datahub.md](technologies/datahub.md) | `data-catalog` |   |
| [Kestra](technologies/kestra.md) | `data` | Hold | [kestra.md](technologies/kestra.md) | `orchestrate` |   |
| [n8n](technologies/n8n.md) | `data` | Hold | [n8n.md](technologies/n8n.md) | `orchestrate` |   |
| [GLPI](technologies/glpi.md) | `itsm` | Hold | [glpi.md](technologies/glpi.md) | `service-desk` |   |
| [Kasm Workspaces](technologies/kasm-workspaces.md) | `collab` | Adopt | [kasm-workspaces.md](technologies/kasm-workspaces.md) | `endpoint` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [Matrix](technologies/matrix.md) | `collab` | Adopt | [matrix.md](technologies/matrix.md) | `chat` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [RustDesk](technologies/rustdesk.md) | `collab` | Adopt | [rustdesk.md](technologies/rustdesk.md) | `endpoint` | [`endpoint`](https://github.com/mess-systems/blueprints/tree/main/endpoint) |
| [Mattermost](technologies/mattermost.md) | `collab` | Trial | [mattermost.md](technologies/mattermost.md) | `chat` |   |

## Cards

Every card in [technologies/](technologies/) has the same sections:

- **What it is**: two or three lines and a link to the official site.
- **Why mess.systems uses it**: the role it plays, tied to the naming standard.
- **Alternatives considered**: comparable options and why this one.
- **Where it applies**: links to the sections of the naming standard that name it.
- **Capabilities and blueprints**: the [capability codes](https://github.com/mess-systems/naming-standard/blob/main/01-naming-conventions.md#43-capability-codes-unique-across-all-domains) the technology serves and the [blueprints](https://github.com/mess-systems/blueprints) (reference architectures) it takes part in.
- **Review trigger**: the event that reopens the decision.
- **History**: every ring change with its date.

## Changing the radar

A ring change, a new entry, or a removal is a pull request with a short rationale. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Text licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE) ([license deed](https://creativecommons.org/licenses/by/4.0/)). You may share and adapt it, including commercially, with attribution: "mess.systems tech radar (https://github.com/mess-systems/tech-radar), CC BY 4.0".

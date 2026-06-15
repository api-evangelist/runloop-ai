# Runloop (runloop-ai)

Runloop is the AI Agent Accelerator — secure code sandboxes (Devboxes), evaluation infrastructure (Benchmarks, Scenarios), and production-grade orchestration for AI coding agents at enterprise scale. The platform provides a single REST API and matched Python/TypeScript SDKs covering Devbox lifecycle, Blueprint image building, Snapshot branching, Agent registry, Axon event streams with Broker bridges, Storage Objects, Secrets, Network Policies, Agent Gateways, MCP Configs, and a turnkey eval framework (SWE-Bench Verified, SWE-smith, custom benchmarks). Runloop runs on a custom bare-metal hypervisor with microVM-level isolation and is SOC 2 Type II, HIPAA, and GDPR compliant, with VPC deployment available for regulated workloads. Founded 2023 by Jonathan Wall (Google File System lead, Google Wallet co-founder, Index CTO acquired by Stripe).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/runloop-ai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/runloop-ai/refs/heads/main/apis.yml)

## Scope

- **Access:** 3rd-Party

## Tags

- AI
- AI Agents
- Coding Agents
- Sandboxes
- Devboxes
- Code Execution
- Evaluation
- Benchmarks
- SWE-Bench
- MCP
- Snapshots
- microVM
- Enterprise
- SOC 2

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Runloop Devbox API

Create, configure, and operate Devboxes — isolated Linux microVM-backed sandbox environments purpose-built for AI coding agents. The Devbox API covers the full lifecycle (create, suspend, resume, snapshot, shutdown), synchronous and asynchronous command execution, named shell sessions, file I/O, code-repo mounts, agent and storage object mounts, network tunnels with HTTPS URLs, SSH key issuance, and rich observability (executions, metrics, logs). Includes the PTY control-plane for interactive WebSocket shell sessions.

- **Human URL:** [https://docs.runloop.ai/docs/devboxes/overview](https://docs.runloop.ai/docs/devboxes/overview)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- Sandboxes
- Devboxes
- Coding Agents

#### Properties

- [Documentation](https://docs.runloop.ai/docs/devboxes/overview)
- [Documentation](https://docs.runloop.ai/docs/devboxes/lifecycle)
- [Documentation](https://docs.runloop.ai/docs/devboxes/execute-commands)
- [Documentation](https://docs.runloop.ai/docs/devboxes/files)
- [Documentation](https://docs.runloop.ai/docs/devboxes/named-shells)
- [Documentation](https://docs.runloop.ai/docs/devboxes/snapshots)
- [Documentation](https://docs.runloop.ai/docs/devboxes/start-stop)
- [Documentation](https://docs.runloop.ai/docs/devboxes/tunnels)
- [OpenAPI](openapi/runloop-devbox-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-devbox-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-devbox-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/runloop-devbox-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/runloop-execution-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/runloop-snapshot-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/runloop-tunnel-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/runloop-launch-parameters-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/runloop-devbox-structure.json)
- [JSON-LD](json-ld/runloop-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/runloop-devbox-create-example.json)
- [Example](examples/runloop-devbox-exec-example.json)
- [Example](examples/runloop-snapshot-create-example.json)

### Runloop Blueprint API

Build, preview, list, and manage Blueprints — Dockerfile-based container image templates that Devboxes launch from. Blueprints capture pre-installed system packages, language runtimes, code mounts, ports, and agent tooling so a fresh Devbox starts in seconds. Supports private blueprints, public discovery, metadata-keyed search, and creation from RepositoryConnection inspection.

- **Human URL:** [https://docs.runloop.ai/docs/devboxes/blueprints/overview](https://docs.runloop.ai/docs/devboxes/blueprints/overview)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- Blueprints
- Container Images
- Devboxes

#### Properties

- [Documentation](https://docs.runloop.ai/docs/devboxes/blueprints/overview)
- [OpenAPI](openapi/runloop-blueprint-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-blueprint-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-blueprint-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/runloop-blueprint-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Runloop Benchmark API

Define, configure, and run Benchmarks against your agents. Runloop ships SWE-Bench Verified and SWE-smith out of the box; the Benchmark API also supports custom benchmarks built from your own scenarios and scorers. Resources include benchmarks, benchmark runs (with start, cancel, complete lifecycle), benchmark jobs, scenario runs, and downloadable run logs.

- **Human URL:** [https://docs.runloop.ai/docs/benchmarks/overview](https://docs.runloop.ai/docs/benchmarks/overview)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- Benchmarks
- Evaluation
- SWE-Bench

#### Properties

- [Documentation](https://docs.runloop.ai/docs/benchmarks/overview)
- [OpenAPI](openapi/runloop-benchmark-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-benchmark-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-benchmark-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/runloop-benchmark-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/runloop-benchmark-run-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/runloop-benchmark-run-example.json)

### Runloop Scenario API

Author and run individual evaluation Scenarios — the atomic test unit for AI coding agents. Each Scenario captures input context, environment setup, an agent invocation, and one or more Scenario Scorers that produce pass/fail signals plus structured scores. Used standalone or composed into Benchmarks.

- **Human URL:** [https://docs.runloop.ai/docs/benchmarks/scenarios](https://docs.runloop.ai/docs/benchmarks/scenarios)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- Scenarios
- Evaluation

#### Properties

- [Documentation](https://docs.runloop.ai/docs/benchmarks/overview)
- [OpenAPI](openapi/runloop-scenario-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-scenario-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-scenario-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/runloop-scenario-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Runloop Agents API

Register and version Agents — packaged agent definitions sourced from Git, npm, pip, or pre-packaged storage objects. Once registered, an Agent can be mounted to any Devbox at create time for fast, reproducible installs. Includes public agent listings and per-agent Devbox-count reporting.

- **Human URL:** [https://docs.runloop.ai/docs/devboxes/agents/using-agents-api](https://docs.runloop.ai/docs/devboxes/agents/using-agents-api)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- Agent Registry

#### Properties

- [Documentation](https://docs.runloop.ai/docs/devboxes/agents/using-agents-api)
- [OpenAPI](openapi/runloop-agents-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-agents-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-agents-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/runloop-agent-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Runloop Axons API

Create and operate Axons — Runloop's distributed event streams for sequencing, recording, and observing agent interactions. Each Axon supports event publish, SSE subscription, SQL queries and batch operations over event history, and a Broker bridge that connects an Axon to agents running inside Devboxes using ACP or Claude agent client protocols.

- **Human URL:** [https://docs.runloop.ai/docs/axons/overview](https://docs.runloop.ai/docs/axons/overview)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- Event Streams
- Axon
- Broker
- ACP

#### Properties

- [Documentation](https://docs.runloop.ai/docs/axons/overview)
- [Documentation](https://docs.runloop.ai/docs/axons/broker)
- [OpenAPI](openapi/runloop-axons-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-axons-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-axons-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/runloop-axon-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/runloop-axon-subscribe-example.json)

### Runloop Storage Objects API

Upload and manage Storage Objects — managed files with presigned download URLs that can be mounted into Devboxes or shared between agent runs. Two-step upload (create -> complete), public listings, metadata-keyed search, and download presign.

- **Human URL:** [https://docs.runloop.ai/docs/storage-objects/overview](https://docs.runloop.ai/docs/storage-objects/overview)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- Storage
- Objects

#### Properties

- [Documentation](https://docs.runloop.ai/docs/storage-objects/overview)
- [OpenAPI](openapi/runloop-objects-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-objects-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-objects-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/runloop-object-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Runloop Secrets API

Securely manage account-level Secrets (API keys, tokens, credentials) that Runloop injects into Devboxes at runtime. Raw secret values are never exposed to agent code or to the Devbox shell environment after creation — they are referenced by name.

- **Human URL:** [https://docs.runloop.ai/docs/devboxes/configuration/account-secrets](https://docs.runloop.ai/docs/devboxes/configuration/account-secrets)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- Secrets
- Credentials

#### Properties

- [Documentation](https://docs.runloop.ai/docs/devboxes/configuration/account-secrets)
- [OpenAPI](openapi/runloop-secrets-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-secrets-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-secrets-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/runloop-secret-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Runloop Network Policies API

Define and manage egress Network Policies that restrict outbound network access from Devboxes. Allow/deny rules at account scope, attachable per Devbox at launch.

- **Human URL:** [https://docs.runloop.ai/docs/network-policies](https://docs.runloop.ai/docs/network-policies)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- Network Policy
- Security

#### Properties

- [Documentation](https://docs.runloop.ai/docs/network-policies)
- [OpenAPI](openapi/runloop-network-policies-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-network-policies-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-network-policies-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/runloop-network-policy-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Runloop Gateway Configs API

Configure Agent Gateways — proxy configurations that let Devbox-resident agents call external AI provider APIs (OpenAI, Anthropic, etc.) without exposing the raw provider credentials to agent code. Implements the Credential Gateway / opaque token-injection security pattern.

- **Human URL:** [https://docs.runloop.ai/docs/devboxes/agent-gateways](https://docs.runloop.ai/docs/devboxes/agent-gateways)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- Agent Gateways
- Credential Proxy

#### Properties

- [Documentation](https://docs.runloop.ai/docs/devboxes/agent-gateways)
- [OpenAPI](openapi/runloop-gateway-configs-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-gateway-configs-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-gateway-configs-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/runloop-gateway-config-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Runloop MCP Configs API

Configure and manage Model Context Protocol (MCP) server bindings for Devboxes. Each MCP Config is a declarative mount that Runloop wires into Devbox agent runtimes so the agent can call MCP tools without bespoke setup.

- **Human URL:** [https://docs.runloop.ai/docs/devboxes/mcp](https://docs.runloop.ai/docs/devboxes/mcp)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- MCP
- Model Context Protocol

#### Properties

- [Documentation](https://docs.runloop.ai/docs/tools/ai-tools)
- [OpenAPI](openapi/runloop-mcp-configs-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-mcp-configs-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-mcp-configs-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/runloop-mcp-config-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Runloop API Keys API

Create and manage Runloop account API keys and Restricted Keys (scoped, narrower-permission tokens). API keys are the standard auth credential for SDK and REST API access; Restricted Keys are intended for embedded use in Devbox-resident agents.

- **Human URL:** [https://docs.runloop.ai/api-reference/apikeys/create-api-key](https://docs.runloop.ai/api-reference/apikeys/create-api-key)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- API Keys
- Authentication

#### Properties

- [Documentation](https://docs.runloop.ai/api-reference/apikeys/create-api-key)
- [OpenAPI](openapi/runloop-apikeys-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-apikeys-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-apikeys-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/runloop-api-key-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/runloop-restricted-key-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Runloop Executions Streaming API

Stream stdout and stderr updates from in-flight Devbox executions in real time. Use alongside the Devbox execute endpoints for long-running command output capture.

- **Human URL:** [https://docs.runloop.ai/docs/devboxes/execution-logs](https://docs.runloop.ai/docs/devboxes/execution-logs)
- **Base URL:** `https://api.runloop.ai`

#### Tags

- AI
- AI Agents
- Executions
- Streaming

#### Properties

- [Documentation](https://docs.runloop.ai/docs/devboxes/execution-logs)
- [OpenAPI](openapi/runloop-executions-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/runloop-executions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/runloop-executions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Website](https://runloop.ai)
- [Documentation](https://docs.runloop.ai)
- [API Reference](https://docs.runloop.ai/api-reference)
- [Portal](https://docs.runloop.ai)
- [Sign Up](https://platform.runloop.ai/signup)
- [Pricing](https://runloop.ai/pricing)
- [Plans](plans/runloop-ai-plans-pricing.yml)
- [Rate Limits](rate-limits/runloop-ai-rate-limits.yml)
- [Fin Ops](finops/runloop-ai-finops.yml)
- [Vocabulary](vocabulary/runloop-ai-vocabulary.yml)
- [Spectral Rules](rules/runloop-ai-rules.yml)
- [JSON-LD](json-ld/runloop-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Status Page](https://status.runloop.ai)
- [Security](https://runloop.ai/security)
- [Compliance](https://runloop.ai/security)
- [Careers](https://runloop.ai/careers)
- [About](https://runloop.ai/about)
- [Blog](https://runloop.ai/blog)
- [Media](https://runloop.ai/in-the-media)
- [Contact Sales](https://runloop.ai/contact)
- [Git Hub](https://github.com/runloopai)
- [Documentation](https://docs.runloop.ai/llms.txt)
- [Documentation](https://docs.runloop.ai/docs/tutorials/quickstart)
- [Documentation](https://docs.runloop.ai/docs/overview/runloop-features)
- [Documentation](https://docs.runloop.ai/docs/overview/what-is-runloop)
- [Tutorials](https://docs.runloop.ai/docs/tutorials/overview)
- [SDK](https://github.com/runloopai/api-client-python)
- [SDK](https://runloopai.github.io/api-client-python/)
- [Python Package](https://pypi.org/project/runloop-api-client/)
- [SDK](https://github.com/runloopai/api-client-ts)
- [SDK](https://runloopai.github.io/api-client-ts/)
- [N P M Package](https://www.npmjs.com/package/@runloop/api-client)
- [C L I](https://github.com/runloopai/rl-cli)
- [C L I](https://docs.runloop.ai/docs/tools/rl-cli)
- [Homebrew](https://github.com/runloopai/homebrew-tap)
- [SDK](https://github.com/runloopai/remote-agents-sdk)
- [Tools](https://github.com/runloopai/runloop-examples)
- [Tools](https://github.com/runloopai/deploy-agent)
- [Tools](https://github.com/runloopai/code-execution-agent)
- [Tools](https://github.com/runloopai/ai-agent-app-template)
- [Tools](https://docs.runloop.ai/static/files/runloop-python-client.mdc)
- [Tools](https://docs.runloop.ai/static/files/runloop-typescript-client.mdc)
- [Tools](https://github.com/runloopai/computesdk)
- [Tools](https://github.com/runloopai/deepagents)
- [Tools](https://github.com/runloopai/codex-tax-man)
- [Integration](https://docs.runloop.ai/docs/tutorials/openai-agentssdk-runloop)
- [Integration](https://docs.runloop.ai/docs/tutorials/opencode-runloop)
- [Integration](https://docs.runloop.ai/docs/tutorials/axon-acp-broker)
- [Integration](https://docs.runloop.ai/docs/devboxes/agents/deploying-with-github-actions)
- [M C P](https://docs.runloop.ai/docs/tools/ai-tools)
- [LinkedIn](https://www.linkedin.com/company/runloopai)
- [Twitter](https://twitter.com/runloopai)
- [Contact Info](mailto:support@runloop.ai)

## Maintainers

**FN:** Runloop, Inc.
**Email:** support@runloop.ai
**URL:** https://runloop.ai

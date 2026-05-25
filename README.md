# Runloop (runloop-ai)

Runloop is the AI Agent Accelerator — secure code sandboxes (Devboxes), evaluation infrastructure
(Benchmarks, Scenarios), and production-grade orchestration for AI coding agents at enterprise
scale. A single REST API at `https://api.runloop.ai` and matched Python/TypeScript SDKs cover the
full surface: Devbox lifecycle, Blueprint image building, Snapshot branching, Agent registry,
Axon event streams with Broker bridges, Storage Objects, Secrets, Network Policies, Agent
Gateways, MCP Configs, and a turnkey eval framework that ships with SWE-Bench Verified and
SWE-smith. Runloop runs on a custom bare-metal hypervisor with microVM-level tenant isolation and
is SOC 2 Type II, HIPAA, and GDPR compliant; Enterprise customers can deploy directly into their
own VPC.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/runloop-ai/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AI, AI Agents, Coding Agents, Sandboxes, Devboxes, Code Execution, Evaluation, Benchmarks, SWE-Bench, MCP, Snapshots, microVM, Enterprise, SOC 2

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Company

- **Founded:** 2023
- **Founder & CEO:** Jonathan Wall (ex-Google File System, co-founder Google Wallet, co-founder & CTO Index — acquired by Stripe)
- **Team:** Senior engineers averaging 15+ years experience (Google, Stripe, Vercel, AWS, Meta alumni)
- **Compliance:** SOC 2 Type II, HIPAA, GDPR; VPC deployment available

## APIs

### Runloop Devbox API
Create, configure, and operate Devboxes — isolated Linux microVM-backed sandboxes purpose-built for AI coding agents. Covers the full lifecycle (create, suspend, resume, snapshot, shutdown), synchronous and asynchronous command execution, named shell sessions, file I/O, code-repo mounts, agent and storage object mounts, network tunnels with HTTPS URLs, SSH key issuance, observability, and the PTY control plane for interactive WebSocket shells.

**Human URL:** [https://docs.runloop.ai/docs/devboxes/overview](https://docs.runloop.ai/docs/devboxes/overview)

- [OpenAPI](openapi/runloop-devbox-api-openapi.yml)
- [JSON Schema — Devbox](json-schema/runloop-devbox-schema.json)
- [JSON Schema — Execution](json-schema/runloop-execution-schema.json)
- [JSON Schema — Snapshot](json-schema/runloop-snapshot-schema.json)
- [JSON Schema — Tunnel](json-schema/runloop-tunnel-schema.json)
- [JSON Schema — Launch Parameters](json-schema/runloop-launch-parameters-schema.json)
- [JSON Structure — Devbox](json-structure/runloop-devbox-structure.json)
- [JSON-LD Context](json-ld/runloop-context.jsonld)
- [Example — Create Devbox](examples/runloop-devbox-create-example.json)
- [Example — Execute Command](examples/runloop-devbox-exec-example.json)
- [Example — Snapshot Disk](examples/runloop-snapshot-create-example.json)
- [Naftiko Capability — Devboxes](capabilities/devbox-devboxes.yaml)
- [Naftiko Capability — PTY](capabilities/devbox-pty.yaml)

### Runloop Blueprint API
Build, preview, list, and manage Blueprints — Dockerfile-based image templates that Devboxes launch from. Supports private blueprints, public discovery, metadata search, and inspection-based blueprint creation from a connected repository.

**Human URL:** [https://docs.runloop.ai/docs/devboxes/blueprints/overview](https://docs.runloop.ai/docs/devboxes/blueprints/overview)

- [OpenAPI](openapi/runloop-blueprint-api-openapi.yml)
- [JSON Schema — Blueprint](json-schema/runloop-blueprint-schema.json)
- [Naftiko Capability — Blueprints](capabilities/blueprint-blueprints.yaml)

### Runloop Benchmark API
Define, configure, and run Benchmarks. Ships SWE-Bench Verified and SWE-smith out of the box; supports custom benchmarks built from your own scenarios and scorers. Resources include benchmarks, benchmark runs (start, cancel, complete), benchmark jobs, scenario runs, and downloadable run logs.

**Human URL:** [https://docs.runloop.ai/docs/benchmarks/overview](https://docs.runloop.ai/docs/benchmarks/overview)

- [OpenAPI](openapi/runloop-benchmark-api-openapi.yml)
- [JSON Schema — Benchmark](json-schema/runloop-benchmark-schema.json)
- [JSON Schema — Benchmark Run](json-schema/runloop-benchmark-run-schema.json)
- [Example — Start Benchmark Run](examples/runloop-benchmark-run-example.json)
- [Naftiko Capability — Benchmarks](capabilities/benchmark-benchmarks.yaml)
- [Naftiko Capability — Benchmark Runs](capabilities/benchmark-benchmark-runs.yaml)
- [Naftiko Capability — Benchmark Jobs](capabilities/benchmark-benchmark-jobs.yaml)

### Runloop Scenario API
Author and run individual evaluation Scenarios — the atomic test unit for AI coding agents. Each Scenario captures input context, environment setup, agent invocation, and one or more Scenario Scorers that produce pass/fail signals plus structured scores.

**Human URL:** [https://docs.runloop.ai/docs/benchmarks/overview](https://docs.runloop.ai/docs/benchmarks/overview)

- [OpenAPI](openapi/runloop-scenario-api-openapi.yml)
- [JSON Schema — Scenario](json-schema/runloop-scenario-schema.json)
- [Naftiko Capability — Scenarios](capabilities/scenario-scenarios.yaml)

### Runloop Agents API
Register and version Agents — packaged agent definitions sourced from Git, npm, pip, or pre-packaged storage objects. Once registered, an Agent can be mounted to any Devbox at create time for fast, reproducible installs.

**Human URL:** [https://docs.runloop.ai/docs/devboxes/agents/using-agents-api](https://docs.runloop.ai/docs/devboxes/agents/using-agents-api)

- [OpenAPI](openapi/runloop-agents-api-openapi.yml)
- [JSON Schema — Agent](json-schema/runloop-agent-schema.json)
- [Naftiko Capability — Agents](capabilities/agents-agents.yaml)

### Runloop Axons API
Create and operate Axons — distributed event streams for sequencing, recording, and observing agent interactions. Supports event publish, SSE subscription, SQL queries over event history, and a Broker bridge that connects Axons to agents running inside Devboxes using ACP or Claude agent client protocols.

**Human URL:** [https://docs.runloop.ai/docs/axons/overview](https://docs.runloop.ai/docs/axons/overview)

- [OpenAPI](openapi/runloop-axons-api-openapi.yml)
- [JSON Schema — Axon](json-schema/runloop-axon-schema.json)
- [Example — Subscribe SSE](examples/runloop-axon-subscribe-example.json)
- [Naftiko Capability — Axons](capabilities/axons-axons.yaml)
- [Naftiko Capability — Axon Devbox Bridges](capabilities/axons-devboxes.yaml)

### Runloop Storage Objects API
Upload and manage Storage Objects — managed files with presigned download URLs that can be mounted into Devboxes or shared between agent runs. Two-step upload (create → complete), public listings, metadata-keyed search, and download presign.

**Human URL:** [https://docs.runloop.ai/docs/storage-objects/overview](https://docs.runloop.ai/docs/storage-objects/overview)

- [OpenAPI](openapi/runloop-objects-api-openapi.yml)
- [JSON Schema — Object](json-schema/runloop-object-schema.json)
- [Naftiko Capability — Objects](capabilities/objects-objects.yaml)

### Runloop Secrets API
Securely manage account-level Secrets (API keys, tokens, credentials) that Runloop injects into Devboxes at runtime without exposing the raw values to agent code.

**Human URL:** [https://docs.runloop.ai/docs/devboxes/configuration/account-secrets](https://docs.runloop.ai/docs/devboxes/configuration/account-secrets)

- [OpenAPI](openapi/runloop-secrets-api-openapi.yml)
- [JSON Schema — Secret](json-schema/runloop-secret-schema.json)
- [Naftiko Capability — Secrets](capabilities/secrets-secrets.yaml)

### Runloop Network Policies API
Define and manage egress Network Policies that restrict outbound network access from Devboxes. Allow/deny rules at account scope, attachable per Devbox at launch.

**Human URL:** [https://docs.runloop.ai/docs/network-policies](https://docs.runloop.ai/docs/network-policies)

- [OpenAPI](openapi/runloop-network-policies-api-openapi.yml)
- [JSON Schema — Network Policy](json-schema/runloop-network-policy-schema.json)
- [Naftiko Capability — Network Policies](capabilities/network-policies-network-policies.yaml)

### Runloop Gateway Configs API
Configure Agent Gateways — proxy configurations that let Devbox-resident agents call external AI provider APIs without seeing the underlying provider credentials. Implements the Credential Gateway / opaque token-injection security pattern.

**Human URL:** [https://docs.runloop.ai/docs/devboxes/agent-gateways](https://docs.runloop.ai/docs/devboxes/agent-gateways)

- [OpenAPI](openapi/runloop-gateway-configs-api-openapi.yml)
- [JSON Schema — Gateway Config](json-schema/runloop-gateway-config-schema.json)
- [Naftiko Capability — Gateway Configs](capabilities/gateway-configs-gateway-configs.yaml)

### Runloop MCP Configs API
Configure and manage Model Context Protocol (MCP) server bindings for Devboxes. Each MCP Config is a declarative mount that Runloop wires into Devbox agent runtimes so the agent can call MCP tools without bespoke setup.

**Human URL:** [https://docs.runloop.ai/docs/tools/ai-tools](https://docs.runloop.ai/docs/tools/ai-tools)

- [OpenAPI](openapi/runloop-mcp-configs-api-openapi.yml)
- [JSON Schema — MCP Config](json-schema/runloop-mcp-config-schema.json)
- [Naftiko Capability — MCP Configs](capabilities/mcp-configs-mcp-configs.yaml)

### Runloop API Keys API
Create and manage Runloop account API keys and Restricted Keys (scoped, narrower-permission tokens). API keys are the standard auth credential for SDK and REST access; Restricted Keys are intended for embedding inside Devbox-resident agents.

**Human URL:** [https://docs.runloop.ai/api-reference/apikeys/create-api-key](https://docs.runloop.ai/api-reference/apikeys/create-api-key)

- [OpenAPI](openapi/runloop-apikeys-api-openapi.yml)
- [JSON Schema — API Key](json-schema/runloop-api-key-schema.json)
- [JSON Schema — Restricted Key](json-schema/runloop-restricted-key-schema.json)
- [Naftiko Capability — API Keys](capabilities/apikeys-apikeys.yaml)
- [Naftiko Capability — Restricted Keys](capabilities/apikeys-restricted-keys.yaml)

### Runloop Executions Streaming API
Stream stdout and stderr updates from in-flight Devbox executions in real time. Use alongside the Devbox execute endpoints for long-running command output capture.

**Human URL:** [https://docs.runloop.ai/docs/devboxes/execution-logs](https://docs.runloop.ai/docs/devboxes/execution-logs)

- [OpenAPI](openapi/runloop-executions-api-openapi.yml)

## Plans, Rate Limits, and FinOps

- [Plans & Pricing](plans/runloop-ai-plans-pricing.yml) — Basic (free + usage), Pro ($250/mo + usage), Enterprise (custom), $50 Pro Trial credit
- [Rate Limits & Quotas](rate-limits/runloop-ai-rate-limits.yml) — Plan-tier resource ceilings; backoff on 429
- [FinOps / FOCUS Alignment](finops/runloop-ai-finops.yml) — Devbox CPU/RAM, Blueprint Build, four storage SKUs, Axon coordination meters

## Compute Pricing Quick Reference

| Meter | Hourly | Per-Second |
|---|---|---|
| Devbox CPU | $0.108 / CPU-hr | $0.00003 / CPU-sec |
| Devbox Memory | $0.0252 / GB-hr | $0.000007 / GB-sec |
| Blueprint Build | $0.108 / CPU-hr | $0.00003 / CPU-sec |
| Devbox Storage | $0.00034236 / GB-hr | $0.0000000951 / GB-sec |
| Blueprint Storage | $0.000072 / GB-hr | $0.00000002 / GB-sec |
| Snapshot Storage | $0.000072 / GB-hr | $0.00000002 / GB-sec |
| Object Storage | $0.000072 / GB-hr | $0.00000002 / GB-sec |
| Active Axon | $0.006 / axon-hr | $0.0000016667 / axon-sec |
| Inactive Axon Storage | $0.20 / GB-month | — |

## SDKs and Tooling

- **Python SDK** — `pip install runloop-api-client` ([repo](https://github.com/runloopai/api-client-python), [docs](https://runloopai.github.io/api-client-python/))
- **TypeScript SDK** — `npm install @runloop/api-client` ([repo](https://github.com/runloopai/api-client-ts), [docs](https://runloopai.github.io/api-client-ts/))
- **rl-cli** — Interactive Runloop CLI ([repo](https://github.com/runloopai/rl-cli), [Homebrew tap](https://github.com/runloopai/homebrew-tap))
- **Remote Agents SDK** — Axon-backed ACP and Claude agent clients ([repo](https://github.com/runloopai/remote-agents-sdk))
- **Cookbook** — [runloop-examples](https://github.com/runloopai/runloop-examples)
- **deploy-agent** — [GitHub Action](https://github.com/runloopai/deploy-agent) for CI/CD agent deployment
- **AI Agent App Template** — [starter](https://github.com/runloopai/ai-agent-app-template)
- **ComputeSDK** — open-source code-execution toolkit ([repo](https://github.com/runloopai/computesdk))
- **Cursor Rules** — [Python](https://docs.runloop.ai/static/files/runloop-python-client.mdc) / [TypeScript](https://docs.runloop.ai/static/files/runloop-typescript-client.mdc)
- **MCP Server** — [AI Tools docs](https://docs.runloop.ai/docs/tools/ai-tools)

## Architecture & Guidance

- Single REST surface at `https://api.runloop.ai`
- 119 configured endpoints across 14 logical resource groups
- Bearer auth with `RUNLOOP_API_KEY`
- snake_case identifiers throughout
- `/v1/` versioned paths (plus `/pty/` for the WebSocket control plane)
- Prefer the async Python SDK over the sync version
- Use `exec` for blocking commands; `exec_async` for long-running background processes
- Suspended Devboxes accrue storage cost only — not compute or memory

## Spectral Rules

[runloop-ai-rules.yml](rules/runloop-ai-rules.yml) — enforces Bearer auth, `/v1/` prefix, snake_case parameters, required `operationId`, Title Case summaries, canonical tag set, and the canonical `api.runloop.ai` server URL.

## Vocabulary

[runloop-ai-vocabulary.yml](vocabulary/runloop-ai-vocabulary.yml) captures the concepts (Devbox, Blueprint, Snapshot, Agent, Axon, Broker, Benchmark, Scenario, Tunnel, Storage Object, Secret, Gateway Config, MCP Config, Network Policy, PTY Session, Execution), services (REST API, Python SDK, TypeScript SDK, rl-cli, MCP Server, Dashboard, GitHub Actions), and standards (OpenAPI 3.0.3, MCP, ACP, SOC 2 Type II, HIPAA, GDPR) that make up the Runloop platform.

## Status, Security, and Support

- **Status:** [https://status.runloop.ai](https://status.runloop.ai)
- **Security & Compliance:** [https://runloop.ai/security](https://runloop.ai/security) — SOC 2 Type II, HIPAA, GDPR; VPC deployment for Enterprise
- **Support:** support@runloop.ai
- **Contact Sales:** [https://runloop.ai/contact](https://runloop.ai/contact)

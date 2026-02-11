# Context Engine

**Deterministic context infrastructure for AI agents.**

Context Engine provides a reproducible, auditable, and offline-first system for delivering exactly the right context to language models — every time, on every machine.

It replaces heuristic retrieval and opaque pipelines with **content-addressed documents**, **immutable caches**, and **fully deterministic selection**.

---

## Why Context Engine exists

Modern AI systems depend on context retrieval that is:

- non-deterministic  
- difficult to audit  
- hard to reproduce across environments  
- coupled to external services  
- unpredictable under token constraints  

This creates operational risk for teams deploying AI in production.

Context Engine treats context as **infrastructure**, not a runtime guess.

For identical inputs, it guarantees **byte-identical outputs** across:

- operating systems  
- hardware architectures  
- supported compiler versions  

No randomness. No hidden state. No network dependencies.

---

## Architecture

The platform is composed of three layers:

### Engine
Deterministic selection and immutable cache model.

→ [`context-core`](https://github.com/contextenginehq/context-core)

Features:

- content-addressed documents (SHA-256)  
- token-budget-first selection  
- deterministic ordering and scoring  
- offline operation  

---

### Build-time Control Plane
Lifecycle management for deterministic context artifacts.

→ [`context-cli`](https://github.com/contextenginehq/context-cli)

Capabilities:

- build reproducible context caches  
- inspect integrity and metadata  
- locally verify agent behavior  
- CI/CD-native workflows  

Agents never build context at runtime — they consume caches produced here.

---

### Runtime Agent Interface
Standardized integration via the Model Context Protocol (MCP).

→ [`context-mcp-server`](https://github.com/contextenginehq/context-mcp-server)

Provides:

- JSON-RPC 2.0 over stdio  
- deterministic tool responses  
- local cache access for agents  
- zero external dependencies  

---

### Compatibility Harness

→ [`context-compat`](https://github.com/contextenginehq/context-compat)

A standalone verification suite that enforces:

- deterministic behavior across versions  
- frozen output schemas  
- protocol stability  
- backward compatibility of caches  

This harness validates the platform’s core guarantees externally using only CLI and MCP interfaces.

---

## Core Guarantees

Context Engine is built around explicit invariants:

✔ Deterministic selection  
✔ Immutable, content-addressed artifacts  
✔ Explicit token budgeting  
✔ Fully explainable results  
✔ Offline-first operation  
✔ Stable machine-readable contracts  

These guarantees are enforced by specifications and compatibility tests, not convention.

---

## When to use Context Engine

Context Engine is designed for environments where reproducibility matters:

- enterprise AI platforms  
- regulated deployments  
- on-prem and air-gapped systems  
- CI/CD-driven AI infrastructure  
- audit and compliance workflows  
- multi-agent systems requiring stable behavior  

If your system must be explainable, reproducible, and inspectable — this is the foundation.

---

## Project Status

The platform is currently at **v0**:

- Core contracts frozen  
- Determinism enforced via compatibility harness  
- MCP interface stable  
- Designed for production evaluation  

Future releases will expand scoring strategies, language SDKs, and hosted infrastructure while preserving the deterministic contract.

---

## Repository Overview

| Repository | Purpose |
|-----------|--------|
| context-core | Deterministic selection engine |
| context-cli | Build and inspect context caches |
| context-mcp-server | MCP server for agent integration |
| context-compat | Compatibility and determinism test harness |
| context-specs | Formal specifications and invariants |
| docs-site | Documentation and guides |
| context-sdk-js | JavaScript SDK (in development) |
| context-sdk-python | Python SDK (in development) |

---

## License

Core components are open source under the [Apache License 2.0](LICENSE).

---

## Vision

Context Engine defines a new category: **deterministic context infrastructure**.

AI systems should be reproducible by design.  
Context should be an artifact, not a guess.  
Infrastructure should be inspectable, not probabilistic.

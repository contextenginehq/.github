# Context Engine — Deterministic Context Infrastructure

> Build, inspect, and serve context deterministically for AI agents and LLMs.

Context Engine provides reproducible, auditable, and offline-first context delivery.  
It ensures that the same query over the same cache produces **identical outputs** across:

- hardware architectures (x86_64, aarch64)  
- operating systems (Linux, macOS, Windows)  
- supported Rust compiler versions  

No randomness. No hidden state. Fully explainable.

---

## 🚀 Pinned Repositories

### [context-core](https://github.com/contextenginehq/context-core)
The deterministic engine powering the platform.  
Content-addressed documents, immutable caches, and reproducible selection logic for LLMs.

### [context-cli](https://github.com/contextenginehq/context-cli)
Command-line interface to build, inspect, and verify context caches.  
Supports CI/CD pipelines and local audits of agent behavior.

### [context-mcp-server](https://github.com/contextenginehq/context-mcp-server)
MCP server exposing context caches to agents via JSON-RPC 2.0 over stdio.  
Deterministic responses ensure agents always get the same context.

### [context-compat](https://github.com/contextenginehq/context-compat)
Compatibility harness validating determinism, schema compliance, and backward compatibility.  
Runs externally via CLI and MCP; no internal crate dependencies.

### [context-specs](https://github.com/contextenginehq/context-specs)
Formal specifications and invariants for the platform.  
Includes frozen JSON schemas, MCP error contracts, and selection behavior rules.

### [docs-site](https://github.com/contextenginehq/docs-site)
Documentation, how-to guides, and usage examples for developers and integrators.

### [context-sdk-js](https://github.com/contextenginehq/context-sdk-js)
JavaScript SDK (work in progress).  
Provides a programmatic interface to build and resolve context in Node.js.

### [context-sdk-python](https://github.com/contextenginehq/context-sdk-python)
Python SDK (work in progress).  
Programmatic access for Python-based AI workflows.

---

## 🔑 Core Principles

- **Deterministic Selection:** Same inputs → identical outputs.  
- **Content-Addressed:** SHA-256 hashed documents ensure integrity.  
- **Token-Budget First:** Designed for LLM window constraints.  
- **Offline & Auditable:** No network dependencies; inspectable caches.  
- **Frozen Contracts:** Outputs and errors are schema-locked and versioned.  

---

## 💡 Use Cases

- Enterprise AI deployments  
- CI/CD pipelines for LLM-based systems  
- Air-gapped and on-prem AI infrastructure  
- Auditable, regulatory-compliant AI workflows  
- Multi-agent systems requiring reproducible behavior  

---

## 📦 License

All open-source repositories are licensed under [Apache License 2.0](LICENSE).  
The "Context Engine" trademark is reserved for the contributors.

---

**Learn more:** Visit the [Context Engine docs](https://context-engine.dev) for guides, specs, and examples.

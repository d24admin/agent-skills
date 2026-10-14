# Service overview outline

Follow maintained repository documentation first. Use applicable sections from this outline for a new overview.

- **Purpose and responsibility:** What the service owns and how it relates to adjacent components.
- **Evidence scope:** Revision, working-tree differences, inspected sources, and coverage limitations.
- **Runtime architecture:** Entry points, synchronous and asynchronous work, state boundaries, and optional explanatory diagram.
- **Interfaces:** HTTP/RPC endpoints, events, jobs, and links to canonical contracts.
- **State:** Stores, caches, ownership, lifecycle, and retention where supported by evidence.
- **Dependencies:** Callers and downstream systems, protocols, and observed failure behavior.
- **Configuration and operation:** Setting names and sources, verified local commands, build and deployment mechanics. Never credential values.
- **Observability:** Existing health checks, logs, metrics, and alerts. Distinguish code configuration from known deployed settings.
- **Gaps and related material:** Unknown ownership or operational facts, incomplete evidence, and links to maintained guides.

Match tables to the actual stack. A service without a queue does not need a queue inventory. Keep counts consistent with enumerated entries, and label representative diagrams as such when they omit components.

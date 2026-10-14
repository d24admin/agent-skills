---
name: document-workflow
description: "Document one API, event, job, or feature workflow from source evidence, including cross-service behavior, contracts, and failure paths. Do not use as a substitute for a whole-service overview."
---

# Document Workflow

Explain a bounded runtime behavior for a reader who needs to understand what actually happens. Use [the evidence checklist](references/workflow-evidence.md) when tracing a multi-step or cross-service flow.

## Establish scope and evidence

Identify the trigger, expected terminal outcomes, and participating components. Read existing documentation and source-of-truth contracts before creating new documents. Record the source revision and relevant working-tree differences when documenting code. Trace executable behavior and tests; treat supplied narratives as claims to verify.

Follow the flow from input handling through authorization, validation, state changes, dependencies, and final response or event. Trace available downstream consumers for asynchronous work. Distinguish queued, acknowledged, and completed states; do not equate initiating a send with delivery.

If a downstream repository or runtime setting is unavailable, record that boundary as unknown. Distinguish verified facts, inferences, and unresolved gaps. Include source paths and symbols for important claims. Never reproduce secret values in examples or configuration notes.

## Write and verify

Explain purpose, trigger, inputs, main flow, side effects, outputs, failures, and relevant compatibility differences. Include realistic sanitized examples only when supported by the implementation. Add a diagram when it clarifies ownership or control flow.

Follow the existing document structure and location. If a new file is requested and no convention exists, use `docs/<workflow>-workflow.md`. Update source-of-truth API documentation when it is within the requested documentation scope; do not create competing specifications. Preserve actual response codes, error shapes, security, and validation constraints, even when inconsistent across endpoints.

Check claims against the traced paths, resolve local links, and validate changed machine-readable contracts with available project tools. Check example conformance and diagram syntax when applicable; report checks that could not run. Deliver the guide with explicit evidence gaps. No external documentation framework is required.

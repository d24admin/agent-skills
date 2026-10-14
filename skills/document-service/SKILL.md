---
name: document-service
description: "Create or update an evidence-backed overview of an entire service repository for onboarding and maintenance. Cover responsibilities, interfaces, state, dependencies, and operation; use workflow documentation for a single request or event trace."
---

# Document Service

Explain the service as a whole using its implementation and maintained configuration. Use [the service outline](references/service-outline.md) if no project convention exists.

## Inspect the repository

Read repository instructions, existing overviews, contracts, runtime entry points, persistence, external clients, configuration, build and deployment files, and relevant tests. Record the documented revision and relevant working-tree differences.

Inventory the service boundaries systematically: public interfaces, producers and consumers, persistent stores, caches, scheduled work, and dependencies. Resolve routes and topic expressions where evidence allows. Classify components by behavior, not by names. Distinguish runtime-dependent values from literals.

State the coverage of the inventory. If only part of the repository is accessible, document the gap instead of calling the result exhaustive. Do not infer production topology, ownership, alert thresholds, or delivery guarantees from naming conventions.

## Produce the overview

Explain responsibilities, runtime architecture, interfaces, state ownership, dependencies, configuration names and sources, local operation, and evidence-backed deployment or observability behavior. Link existing detailed contracts and workflow guides instead of duplicating them. Mark unavailable operational facts as unknown.

Cite source paths and symbols for important claims. Use sanitized examples and never include secret values. Add only diagrams that aid understanding; no fixed number or notation is required.

Update the existing overview when possible. For a requested new file without a convention, use `docs/<service>-overview.md`. Do not delete a legacy document simply to impose a new format. Change machine-readable contracts only within the requested scope, preserving implemented behavior rather than normalizing it into an invented contract.

## Verify

Cross-check inventories and counts, source citations, local links, examples, and consistency with maintained contracts. Run applicable documentation or schema validation commands; validate diagram syntax when diagrams are added and tooling is available. Report unknowns and validation limits alongside the result. No external template project or documentation standard is required.

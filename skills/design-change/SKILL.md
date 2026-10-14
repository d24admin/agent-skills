---
name: design-change
description: "Produce or revise a technical design for a defined change, including behavior, interfaces, compatibility, implementation sequence, and validation. Use when architecture or implementation decisions are requested; a formal PRD is not required."
---

# Design Change

Translate the requested behavior into implementable decisions grounded in the actual repository. An actionable requirement is sufficient input; do not require a PRD or a separate approval ceremony.

## Ground the design

Read repository instructions, affected entry points, existing abstractions, tests, build configuration, and any relevant requirements. Distinguish current behavior from proposed behavior. Identify the owner of each change, including boundaries between repositories when relevant.

Resolve consequential ambiguities before presenting a final design. Make routine implementation choices using established project patterns. Describe meaningful alternatives only when the tradeoff affects the outcome.

## Specify the change

Use [the design outline](references/design-outline.md) when no project template exists. Specify changed inputs, outputs, state transitions, and ownership precisely enough for implementation. Include failure handling, authorization enforcement, migration, compatibility, and rollout only where applicable. Do not invent detailed contracts for unaffected components.

Trace the main data flow and relevant failure paths. For async work, distinguish acceptance from completion and explain applicable retries, duplicate handling, and terminal outcomes. Use diagrams only when helpful, preferring the repository's established format.

Define the implementation sequence and observable validation criteria. Mark blocking unknowns explicitly; do not present unresolved core decisions as an implementation-ready design.

## Deliver

Follow existing artifact conventions; if a file is requested and none exist, use `docs/<feature>-design.md`. Otherwise provide Markdown inline. Respect a planning-only request and continue into implementation only when it is already authorized. No external skill or template is required.

---
name: implement-change
description: "Implement a specified feature, fix, or refactor in an existing repository using its conventions and appropriate verification. Accept actionable requests directly without requiring a formal PRD or design."
---

# Implement Change

Complete the requested change with evidence that the intended behavior works.

## Establish the change

Read repository instructions and inspect the working tree before editing. Preserve existing user changes. Locate the affected behavior, nearby patterns, relevant tests, and documented validation commands. Use the request and supplied design as the source of intended behavior; surface material contradictions rather than silently overriding either.

For a concrete fix, proceed directly. For a consequential unresolved requirement or architectural decision, clarify that part while continuing independent work. Scale planning to complexity; do not create a PRD or design solely to satisfy a lifecycle.

## Implement

Keep edits within the requested behavior and necessary supporting changes. Reuse the repository's architecture, interfaces, dependencies, and style. Preserve compatibility unless a change is required by the task; account for consumers and migrations when it is not preserved.

Enforce permission and integrity rules at the authoritative boundary, not only in a client interface. For cross-component changes, keep producers, consumers, UI behavior, and error contracts consistent. Update existing documentation when the change makes it inaccurate.

## Verify and report

Choose checks based on behavior and risk, using project commands when available. For a bug fix, prefer a regression case that exposes the original failure. For changed contracts or state, cover relevant failure paths and compatibility. UI behavior deserves appropriate automated or manual checks; do not exempt it categorically. Avoid tests that only repeat implementation details.

Run the relevant checks and inspect the diff for accidental changes. If validation is blocked, state the exact check, cause, and remaining uncertainty. Distinguish checks executed from suggested checks, and manual inspection from passing tests.

Report the behavior changed, verification results, and material limitations. Do not infer authorization to deploy, publish, or perform unrelated external actions from an implementation request. Work directly when optional specialist skills are unavailable.

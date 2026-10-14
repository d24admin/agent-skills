# Technical design outline

Adapt depth to the change. Existing project templates take precedence.

- **Goal and current behavior:** Requirements addressed, evidence inspected, and scope boundaries.
- **Proposed behavior and ownership:** Components that change, their responsibilities, and main data flow.
- **Interfaces and state:** Changed API/event/file inputs and outputs, state transitions, persistence, and compatibility implications. Include exact field details when an implementer needs them.
- **Failure and trust boundaries:** Applicable validation, authorization, timeout, retry, partial-failure, and duplicate-processing behavior.
- **Delivery:** Implementation order, necessary migration steps, and applicable rollout or rollback constraints.
- **Validation:** Map acceptance criteria to focused checks. Include important negative cases and affected consumers.
- **Unresolved decisions:** Identify blockers explicitly; distinguish facts from assumptions.

For a small change, a few paragraphs and test cases can cover these topics. Do not add services, layers, schemas, feature flags, or migrations merely to fill sections.

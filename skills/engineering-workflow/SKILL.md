---
name: engineering-workflow
description: "Route a broad engineering request when the user needs help choosing or coordinating requirements, product definition, design, implementation, review, or documentation. Do not intercept requests already focused on one stage."
---

# Engineering Workflow

Choose the next useful action from the user's requested outcome and available evidence. Explicit intent takes priority over the apparent maturity of an artifact.

## Routing

| Requested outcome | Skill | Input sufficient to start |
| --- | --- | --- |
| Resolve consequential ambiguity | `clarify-requirements` | A request with missing decisions |
| Produce a product brief or PRD | `write-prd` | Notes, requirements, or existing product material |
| Decide how a change should work | `design-change` | Clear requirements or a PRD |
| Fix or implement behavior | `implement-change` | An actionable request, issue, or design |
| Assess a diff or implementation | `review-change` | Changes plus any available requirements |
| Explain one runtime behavior | `document-workflow` | A bounded trigger or workflow and its source |
| Explain a whole service | `document-service` | A service repository |

Inspect available artifacts and repository instructions only as needed to select a stage. A small, well-specified fix goes directly to implementation; a review does not require creating a missing PRD. For vague requests, resolve only ambiguity that prevents the requested work.

State the selected stage briefly and use that skill if available. Sibling skills are optional: if unavailable, perform the selected stage directly using repository evidence and the same scope boundaries. Do not require installation to continue.

For end-to-end work, carry forward established decisions and progress through only the stages needed for the requested outcome. Do not create every possible artifact or repeat settled questions. Respect planning-only requests and execution-mode restrictions. A request for a document or review does not itself authorize implementation.

---
name: write-prd
description: "Create or revise a product requirements document from feature notes, requirements, or stakeholder context. Focus on intended user behavior and acceptance criteria rather than implementation architecture."
---

# Write PRD

Write a concise product document that makes scope and expected outcomes clear. Use the user's format or an existing project template first; otherwise use [the PRD outline](references/prd-outline.md).

## Develop the brief

Read supplied product material and inspect existing behavior when it affects scope. Preserve explicit decisions and identify contradictions. Clarify consequential gaps; label reasonable assumptions rather than inventing customer demand, metrics, deadlines, or stakeholder approval.

Describe the problem, audience, goals, boundaries, main flow, exceptions, and measurable acceptance criteria. Keep implementation choices out unless they are genuine product constraints. Link acceptance scenarios to the relevant requirements so later validation can verify coverage.

Scale detail to the change. A small feature may need a short brief; complex permissions or failure handling may need a scenario table. Add a diagram only when it explains something prose does not explain clearly. Do not generate a workbook or rich document pack unless requested.

## Deliver

Prefer Markdown, following existing locations and naming. When a file is requested and no convention exists, use `docs/<feature>-prd.md`; otherwise inline Markdown is sufficient. Report unresolved product decisions explicitly and never label the document approved without evidence. A PRD request alone does not authorize code changes. The result should be usable without any other skill installed.

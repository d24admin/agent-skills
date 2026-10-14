---
name: review-change
description: "Review a diff, pull request, or implementation for actionable defects, requirement gaps, and regressions. Use available requirements and repository conventions without demanding a PRD or design."
---

# Review Change

Assess the requested changes without modifying them unless fixes are also requested.

## Establish the comparison

Identify the requested diff or comparison base from the user's context and Git state. If multiple bases are plausible and yield materially different reviews, clarify the target. Read repository instructions, the changed code, callers, consumers, and relevant tests. Use provided requirements and designs, but do not fabricate missing requirements.

## Investigate

Prioritize observable correctness, authorization boundaries, data integrity, compatibility, failure handling, and meaningful test gaps. Follow control flow beyond the diff where needed to demonstrate an impact. Inspect applicable cross-service contracts rather than assuming adjacent services were updated.

Separate introduced defects from pre-existing issues. Report a pre-existing issue only when it is relevant to the requested scope, clearly labeled. Avoid stylistic findings unsupported by an explicit project convention or concrete maintenance impact.

Run focused checks when feasible and useful. A failing check is evidence to investigate, not automatic proof that the diff caused it. Do not claim reproduction when you only inspected code.

## Report

Lead with actionable findings ordered by severity. Each finding should give a concise title, affected file and tight line location, triggering conditions, consequence, and evidence. Suggest a correction when supported, without prescribing speculative rewrites.

Keep questions and uncertain risks separate from confirmed defects. If no actionable defects are found, say so and note material coverage limits; do not equate an absence of findings with proof of correctness. Summarize checks actually performed. No external review integration or companion skill is required.

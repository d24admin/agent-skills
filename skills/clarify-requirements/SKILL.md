---
name: clarify-requirements
description: "Clarify incomplete feature requirements when missing product decisions prevent useful design or implementation. Do not turn a concrete fix or fully specified task into a discovery interview."
---

# Clarify Requirements

Turn uncertain intent into an actionable scope without choosing architecture prematurely.

## Discover before asking

Read the request, relevant existing documents, repository instructions, and affected behavior. Separate discoverable facts from user preferences. Investigate facts locally before asking the user; retain decisions already provided.

Identify only uncertainties that would materially change the outcome: intended users, desired behavior, scope boundaries, success criteria, compatibility, or meaningful operational constraints. Ask about privacy, scale, deadlines, or rollout only when they affect this task. Do not manufacture enterprise requirements for a small project.

## Resolve decisions

Ask a small batch of focused questions. For real tradeoffs, offer concrete options with their consequences and a recommendation; use free text when options would constrain the answer artificially. Continue independent investigation while awaiting necessary answers.

Do not silently decide consequential product behavior. Record low-impact defaults as assumptions and make progress. Pause only work that depends on an unanswered blocking decision; do not impose a universal approval gate.

## Deliver

Summarize the problem, intended users, included and excluded behavior, observable acceptance criteria, constraints, and any remaining blockers. Separate confirmed decisions from assumptions. Include success and relevant failure scenarios, not implementation schemas unless the user requested technical detail.

Return the result inline unless a file was requested. For files, follow repository conventions or use a descriptive Markdown filename under `docs/`. Continue into design or implementation only within the user's requested scope; this skill does not require another installed skill.

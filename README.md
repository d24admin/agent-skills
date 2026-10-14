# Personal agent skills

A general-purpose engineering lifecycle library. Workflows scale to the task, follow the target repository's conventions, and default to Markdown. Small fixes do not require a PRD or formal design.

## Skills

| Skill | Use it for | Example request |
| --- | --- | --- |
| [engineering-workflow](skills/engineering-workflow/SKILL.md) | Choosing or coordinating stages | `Use $engineering-workflow to help take this feature from idea to implementation.` |
| [clarify-requirements](skills/clarify-requirements/SKILL.md) | Consequential gaps in product intent | `Use $clarify-requirements to define the expected behavior of account sharing.` |
| [write-prd](skills/write-prd/SKILL.md) | Product scope and acceptance criteria | `Use $write-prd to turn these notes into a concise PRD.` |
| [design-change](skills/design-change/SKILL.md) | Repository-grounded technical decisions | `Use $design-change to design this feature in the current service.` |
| [implement-change](skills/implement-change/SKILL.md) | Features, fixes, and refactors | `Use $implement-change to fix this bug and verify the affected behavior.` |
| [review-change](skills/review-change/SKILL.md) | Evidenced defects and regressions | `Use $review-change to review this diff against the issue requirements.` |
| [document-workflow](skills/document-workflow/SKILL.md) | One request, event, job, or feature flow | `Use $document-workflow to trace this webhook through its consumers.` |
| [document-service](skills/document-service/SKILL.md) | A whole-service overview | `Use $document-service to update this service's onboarding documentation.` |

Each folder contains a `SKILL.md` entrypoint and `agents/openai.yaml` metadata. Longer outlines and evidence checklists live in local `references/` directories and are loaded only when needed. Stage skills work independently; the router can use installed siblings but does not require them to proceed.

## Install for personal use

Copy selected skill folders into `${CODEX_HOME:-$HOME/.codex}/skills/`. For the complete library, run this from the repository root:

```sh
skill_destination="${CODEX_HOME:-$HOME/.codex}/skills"
mkdir -p "$skill_destination"
for skill_source in skills/*; do
  skill_name="$(basename "$skill_source")"
  if [ -e "$skill_destination/$skill_name" ] || [ -L "$skill_destination/$skill_name" ]; then
    printf 'Skipped existing skill: %s\n' "$skill_name"
  else
    cp -R "$skill_source" "$skill_destination/$skill_name"
  fi
done
```

The command preserves existing installations; review and replace those separately when updating. Reload your agent session to pick up newly installed skills. Invoke a skill by its `$name`, or allow automatic selection, which is enabled for all eight skills. No external service, plugin, or sibling skill is required for an individual stage.

## Working conventions

- Explicit user intent takes precedence over lifecycle routing. A review request stays a review; an actionable fix goes directly to implementation.
- Clarify only consequential unknowns after inspecting available evidence. Preserve decisions and authorization already provided.
- Follow repository templates and artifact locations. When a file is requested without an existing convention, use a descriptive Markdown file under `docs/`.
- Workbooks, rich document packs, and diagrams are optional. No fixed framework, programming language, or diagram notation is imposed.
- Report verification actually performed. Document implemented contracts and mark evidence gaps; never invent response codes, error envelopes, production settings, or approvals.

## Validate and maintain

Run the bundled Codex skill-creator validator on each skill, substituting its local path:

```sh
skill_validator=/path/to/skill-creator/scripts/quick_validate.py
for skill_path in skills/*; do
  python3 "$skill_validator" "$skill_path" || exit 1
done
git diff --check
```

Also inspect local reference links, metadata consistency, and behavior. Structural validation cannot establish whether an agent makes the right decisions. Use these routing scenarios when changing instructions:

| Request | Expected behavior |
| --- | --- |
| “I want account sharing, but haven't decided who can access what.” | Clarify consequential access and scope decisions before dependent work. |
| “Write a PRD from these notes.” | Produce product intent and acceptance scenarios; no required workbook. |
| “Design this approved feature.” | Inspect the repository and specify implementation decisions. |
| “Fix this off-by-one error.” | Implement directly; no mandatory PRD, design, or interview. |
| “Review this diff.” | Review evidenced defects without requiring missing product artifacts. |
| “Explain this webhook and its retries.” | Trace the workflow; distinguish acceptance from eventual completion. |
| “Document this entire service.” | Produce a service overview with explicit inventory coverage and unknowns. |
| “Create OpenAPI from handlers that return different error shapes.” | Preserve observed differences; do not invent a uniform envelope. |

Keep folder names, frontmatter names, metadata prompts, and routing names synchronized. Add references or scripts only when they support a concrete repeated need.

## Provenance

The companion `skill-files` library informed the workflow categories and engineering concerns. This library uses newly written instructions for the personal, project-independent behavior described above, following the bundled `skill-creator` guidance. Source material reviewed included requirements discovery, engineering lifecycle skills, and workflow/service documentation skills.

No license file was found for those companion Engati skills during inspection. The license found under `skill-files/superpowers/` applies to that separate vendored project; no Superpowers files, source text, or assets are included here. This repository does not assert a license for the companion material or introduce a redistribution license on its behalf.

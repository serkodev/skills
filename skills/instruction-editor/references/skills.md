# Writing agent skills

Build around a recognizable user goal with coherent inputs, outputs, and success criteria. Split workflows when those boundaries substantially differ; retain related modes when a small router can select the relevant guidance.

## Make discovery precise

The name and description must let an agent choose the skill before reading its body. Front-load the capability and concrete trigger. Put detailed procedure and output formatting in the body. Add a short exclusion only to prevent a plausible neighboring request from being misrouted.

In Codex, the frontmatter `description` in SKILL.md guides skill selection; `interface.short_description` in agents/openai.yaml is a user-facing UI summary. Keep activation conditions in the former and the latter easy to scan.

Example:

```yaml
name: release-notes
description: Draft release notes from changes between specified versions. Use when preparing a version announcement or updating a changelog.
```

"Use for Git, commits, PRs, code, and documentation" would attract unrelated work. Likewise, emphatic words such as "always" or "mandatory" do not substitute for a clear applicability boundary.

Keep descriptions concise because they share discovery context with other skills and may be shortened. Ensure the main use case remains recognizable from the beginning of the description. Do not bury essential triggers in a reference that is read only after selection.

## Keep the entrypoint useful and small

In SKILL.md, retain the shared purpose, essential constraints, workflow decisions, and links to conditional details. Route with both a condition and a useful destination:

```markdown
- For public announcements, read references/public-release.md for audience and disclosure rules.
- For internal summaries, read references/internal-release.md for operational details.
```

Store substantial guidance once. Do not require all references to be loaded at startup or create deep chains of files just to understand the workflow.

- Use references for conditional policies, schemas, or detailed examples.
- Use assets for templates and files that become part of the output.
- Add scripts when deterministic computation or repeated file processing materially improves reliability. Do not add scripts or folders merely to complete a standard layout.

## Specify the workflow contract

Explain the inputs, expected output, facts that must not be inferred, and meaningful question or stopping conditions. For tool-dependent work, preserve real dependencies and handle missing tools or ambiguous results without pretending the action succeeded.

Give fixed steps where order matters. Otherwise allow the executing agent to choose how to reach the result. Teach task-specific judgments instead of imposing a universal inspect-plan-edit-test-report ritual.

Preserve the user's requested invocation policy and supported metadata. Keep normal automatic selection for a new skill unless explicit-only invocation is requested. Do not introduce a dependency on a particular creator skill or tool unless the workflow actually requires it and the target environment supplies it.

## Check routing separately from execution

Consider direct requests, differently worded requests for the same goal, nearby requests that should not activate the skill, and incomplete inputs. Refine the description for selection failures; refine the workflow or resources when selection is correct but the result is wrong.

Use a host validator for naming and metadata when available. It cannot establish that the skill chooses good actions. For substantive workflow changes, evaluate representative behavior at a cost proportional to the change; a narrow editorial correction does not require a broad test campaign.

Sources: [Build skills](https://learn.chatgpt.com/docs/build-skills) and [Plugin skill authoring](https://developers.openai.com/plugins/build/skills).

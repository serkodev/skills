# Writing AGENTS.md

Use AGENTS.md for stable working agreements that apply at its scope. Prioritize information an agent cannot reliably infer: supported commands, generated-file boundaries, compatibility requirements, domain constraints, and relevant documentation entrances.

## Select and place the rules

- Keep personal defaults, repository-wide agreements, and service-specific rules at appropriate scopes. Preserve existing host conventions; verify discovery and precedence if relocating instructions or introducing overrides.
- Include commands and paths supported by the project. Prefer a pointer to a maintained source over copying a large repository map or command catalog.
- Link specialist documents with a condition and purpose. A small edit should not inherit mandatory reading for architecture, deployment, and every other workflow.
- Keep requirements concrete. Explain a non-obvious reason briefly when it helps the agent apply a rule to unfamiliar cases.
- Preserve deliberate constraints even if the agent could often infer them. An explicit branch naming rule or compatibility guarantee is different from a generic reminder to be careful.

Example of an actionable invariant:

```markdown
- Edit API definitions in api/spec.yaml and regenerate the client;
  files under client/generated/ are replaced by the generator.
```

Example of contextual documentation:

```markdown
- For changes to job retry behavior, consult docs/job-delivery.md for delivery guarantees.
- For a release, consult docs/release.md for packaging and publication requirements.
```

These paths are illustrative; use the actual project's paths in a finished file.

## Express autonomy and completion precisely

For a recurring workflow, describe authorized operations and the evidence needed for completion. If a local test environment is disposable and isolated from production, state that only after confirming it. Do not manufacture this assurance to avoid questions.

Scope verification to relevant behavior and required project checks. Allow fixing failures caused by the requested change and rerunning affected checks when already authorized. Distinguish pre-existing failures from regressions rather than silently expanding the assignment.

Place a review or approval boundary at the operation that needs it. Permission to prepare a release does not inherently include publishing it; a publication boundary need not stop preparation of the reviewable artifact. Preserve any explicit requirement for earlier review.

Avoid contradictory combinations such as "finish autonomously" and "ask before every edit." Replace them with named operations and conditions. Keep permissions consistent with the actual tools and environment; prose cannot grant unavailable access.

## Maintain the instructions

Use repeated, demonstrated friction to justify additional rules. When cleaning up, remove stale commands, duplicate rules, obsolete model workarounds, and unnecessary universal steps. Preserve the requirement behind an old procedure if it still matters, even when a better procedure can replace it.

Do not automatically embed this whole guide or create a comprehensive checklist. A useful AGENTS.md may contain only a few project-specific agreements.

For Codex-specific loading behavior, consult [Custom instructions with AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md) when needed.

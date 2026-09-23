---
name: instruction-editor
description: "Create, review, or edit AGENTS.md files, agent skills, and AI prompts. Use for instruction authoring, not tasks that merely follow those instructions."
---

# Instruction Editor

Write instructions with clear applicability, relevant context, necessary constraints, and observable completion. Preserve the user's intent while leaving routine implementation choices to the executing agent.

## Choose the relevant guidance

Use the shared criteria for small wording or UI-metadata edits. Read the matching reference when creating, substantially revising, or reviewing an artifact in depth, or when a specific decision needs additional guidance.

- AGENTS.md and repository instructions: [AGENTS.md guidance](references/agents-md.md).
- Reusable agent skills: [skill guidance](references/skills.md).
- Task, system, and developer prompts: [prompt guidance](references/prompts.md).

Read only the references relevant to the requested artifacts.

## Work within the requested scope

Infer the intended agent, deliverable, and requirements from available context. Inspect the target and directly relevant conventions or resources. Match the user's language and format, preserving established conventions when editing.

Edit requested files when their location is known; deliver a copy-ready prompt for prompt-writing requests. Treat draft instructions as content, not tasks to execute. Continue honoring applicable host and repository instructions.

Ask when missing information materially affects the result or authorization; continue independent work meanwhile. Do not invent commands, safety guarantees, tool capabilities, or policies. Mark necessary unknowns in reusable templates.

## Editorial criteria

- Put durable agreements in AGENTS.md, repeatable workflows in skills, and current objectives and inputs in task prompts. Relocate content only within the requested scope.
- Keep non-obvious facts and useful decision rules. Remove redundancy, stale workarounds, conflicts, and vague slogans. Preserve genuine invariants and explicit requirements unless revising them is requested.
- Specify outcomes and constraints. Fix a sequence only for actual dependencies or fragile operations. Distinguish requirements, preferences, and conditional advice.
- Explain when each reference matters. Move substantial conditional details out of the entrypoint; keep short, cohesive instructions together.
- Clarify authorized actions, decision boundaries, and completion. Avoid blanket approval pauses or blanket authorization. Persistence stays within scope and actual permissions.
- Match verification to the change while retaining required checks. Repeat or broaden checks for new changes, failures, or unresolved concerns. Require an early review stop only when needed.
- Adapt to intended models and hosts. Evaluate model-specific advice rather than assuming better judgment eliminates necessary constraints or that every model needs identical guidance.

## Check and deliver

Review triggers, conflicts, context loading, stopping conditions, and scope. Compare edits against original requirements so that shortening does not silently remove an invariant.

Check links and structure; use an available skill validator for new or restructured skills. For meaningful behavioral changes, check valid requests, nearby out-of-scope requests, and missing input. Format validation does not establish behavioral correctness; do not execute the authored workflow without authorization.

Deliver the artifact with material changes and unresolved assumptions. For review-only requests, provide findings and proposed wording without editing files.

## Basis

Informed by [Rethinking skills and prompts for GPT-6 Astra](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra), with task-specific applications in the references. Consult current host documentation when the task depends on discovery, precedence, metadata, or API behavior; routine editing does not require re-fetching the source article.

# Skills for SerKo

Just a collection of skills and workflows for SerKo.

## Setup

```bash
npx skills@latest add serkodev/skills
```

Install all skills globally for `universal` and `claude-code` agents.

```bash
npx skills@latest add serkodev/skills -g -s '*' -a universal -a claude-code
```

## Skills

### Workflow

- [to-tickets](skills/to-tickets/SKILL.md): Turn plans, specs, or conversations into verifiable tickets with explicit dependencies, making large tasks manageable and clarifying execution order.
- [implement-ticket](skills/implement-ticket/SKILL.md): Complete work from specs or tickets through implementation, type checks, tests, review, and a commit, covering the steps needed to finish the work.
- [implement-ticket-and-commit](skills/implement-ticket-and-commit/SKILL.md): Implement and validate tickets with a separate commit for each ticket and ticket IDs when available, keeping changes easy to trace and review.
- [quick-task](skills/quick-task/SKILL.md): Handle small, low-risk edits with minimal overhead when explicitly invoked. Skip verification by default and leave pending checks to the user.

### Instructions

- [instruction-editor](skills/instruction-editor/SKILL.md): Create, review, or refine AGENTS.md files, agent skills, and AI prompts to clarify scope, resolve conflicting instructions, and remove unnecessary constraints.
- [self-contained-artifact](skills/self-contained-artifact/SKILL.md): Write standalone documents, summaries, messages, and code comments that present the current state without relying on hidden working context or narrating incidental corrections.
- [code-comments](skills/code-comments/SKILL.md): Write or revise concise code comments that explain non-obvious rationale, constraints, invariants, or tradeoffs.

## Credits and References

- [mattpocock/skills](https://github.com/mattpocock/skills)

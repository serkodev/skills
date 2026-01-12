---
name: code-simplifier
description: Simplify and refine code for clarity, consistency, and maintainability while preserving functionality. Use after recent edits or when asked to clean up/clarify/refactor code without behavior changes to keep code readable and aligned with project standards.
---

# Code Simplifier

## Overview

Simplify and refine code for clarity, consistency, and maintainability while preserving behavior exactly. Focus on recently modified code unless the user asks for a broader scope. Run this pass immediately after edits in the current task without waiting for a separate request.

## Apply Project Standards

- Follow project-specific guidance in `AGENTS.md`, `CONTRIBUTING.md`, or equivalent if present.
- If no explicit standards exist, apply these defaults when relevant:
  - Use ES modules; keep import order consistent and include file extensions where required.
  - Prefer `function` declarations over arrow functions for named functions.
  - Add explicit return type annotations for top-level functions in typed codebases.
  - Use explicit React props types and conventional component patterns.
  - Prefer targeted error handling; avoid broad try/catch blocks when possible.
  - Keep naming consistent with surrounding code.

## Simplification Heuristics

- Reduce unnecessary nesting and complexity.
- Remove redundant code and abstractions.
- Improve naming for clarity.
- Consolidate related logic.
- Remove comments that restate obvious code.
- Avoid nested ternary operators; use if/else or switch.
- Favor clarity over brevity; avoid dense one-liners.

## Guardrails

- Preserve behavior, outputs, side effects, and public APIs.
- Avoid refactors that reduce readability or debuggability.
- Avoid merging unrelated concerns into a single function or component.
- Keep helpful abstractions that improve organization.

## Workflow

1. Identify recently modified sections (diffs, touched files, or user callouts).
2. Review for clarity and consistency issues.
3. Apply standards and simplification heuristics.
4. Re-check behavior parity.
5. Document only significant changes that affect understanding.

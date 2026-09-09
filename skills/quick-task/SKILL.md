---
name: quick-task
description: Activate only when the user explicitly invokes this skill through a command. Complete small, low-risk edits as quickly as possible, without verifying them yourself by default; leave any pending checks to the user.
disable-model-invocation: true
---

# Quick Task

## Explicit invocation only
Activate only when the user explicitly invokes `$quick-task`, `/quick-task`, or the host's equivalent skill command.
Apply only to that task; do not automatically carry this workflow into other tasks.

## Execution principles
Complete the current small task in the fewest steps, read only what implementation requires, and make the smallest coherent change.
Avoid unrelated improvements, elaborate plans, and unnecessary questions.

## Do not verify on your own
Do not independently add or run tests, E2E tests, lint, type checks, builds for verification, UI checks, or reviews after editing.
If anything is uncertain, list what to check and the expected result for the user to confirm; do not spend time verifying it yourself.

## Get approval before verification
If the task cannot be completed without verification, explain why and propose the smallest necessary check; execute it only after explicit user approval.
While awaiting approval, complete any unblocked work. Briefly report changes and pending checks, clearly identifying anything left unverified.

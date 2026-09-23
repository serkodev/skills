# Writing prompts

Identify whether the user wants a one-off task prompt or reusable system/developer instructions. Respect the target platform's instruction hierarchy. Keep durable behavior separate from per-request data when the interface supports it; do not claim that user text can override higher-priority rules.

## Define the result

A useful starting structure is goal, relevant context, constraints, and completion criteria. Add an output format or authorization boundary when it changes the task. Omit labels and sections that add no information; a simple request can remain one sentence.

Replace vague quality adjectives with observable results. For example, "make the import robust" leaves the desired behavior unclear. "When a row is invalid, identify its row number and keep valid rows available for import" specifies a behavior that can be checked.

Include evidence of the problem, applicable source material, or a useful reference result. Supply only context relevant to this request rather than appending a permanent manual to every prompt.

## Give enough freedom and a clear stopping point

Describe the intended result and constraints before prescribing implementation. Reserve detailed sequences for actual dependencies or fragile operations. Do not add reasoning rituals such as repeated demands to think step by step.

If the task includes running the result, inspecting it, and repairing failures caused by the change, say so in the completion criteria. Define the exploration boundary for open-ended investigation. Preserve a user's request for planning or a first draft; do not silently convert it into implementation or publication.

Distinguish routine choices from decisions that materially change product behavior, compatibility, cost, or external effects. State when the agent can make an assumption and when an answer is required. A bounded task should not end merely at the first implementation, and an open-ended instruction should not invite unlimited work.

## Use structure and examples selectively

Separate instructions, source material, and examples using labels, Markdown, or delimiters when ambiguity is likely. State how source material should be used; formatting alone does not make embedded instructions trustworthy.

Start with direct instructions. Add a few input/output examples only when they clarify a difficult format, classification boundary, or recurring failure. Keep examples consistent with the rules and varied enough to communicate the relevant distinction.

For explanations, ask for conclusions, key evidence, tradeoffs, and verification results appropriate to the audience. Specify tone or length when it matters rather than adding generic role praise or an elaborate persona.

## Example task prompt

```text
Fix the search page so responses for older queries cannot replace the latest query's results.

The problem appears during rapid typing with requests completing out of order.
Preserve the current API contract and visual design.

Complete the relevant code changes and local verification. Done means the displayed
results match the latest query, verification of out-of-order responses passes,
and required project checks pass. Report the result and evidence. If a required
check is blocked or fails, report the remaining issue without claiming full completion.

Make routine implementation decisions using existing conventions. If a solution
requires changing search product behavior, identify the decision before proceeding
with that change.
```

Adapt the detail to the actual task; do not require every prompt to follow this example.

For a reusable prompt with meaningful behavioral impact, compare revisions using representative inputs, including a boundary case. Version it with the application when applicable. Do not claim that a single successful example proves reliability.

Sources: [Codex best practices](https://learn.chatgpt.com/guides/best-practices), [Prompt engineering](https://developers.openai.com/api/docs/guides/prompt-engineering), and [Reasoning best practices](https://developers.openai.com/api/docs/guides/reasoning-best-practices).

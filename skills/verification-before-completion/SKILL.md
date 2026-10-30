---
name: verification-before-completion
description: Verify current deliverables against their acceptance criteria before claiming completion, a fix, or passing checks; preserve concrete evidence and disclose unverified requirements.
---

# Verification Before Completion

Adapted from obra/superpowers for bounded, task-scoped work. Retain the upstream MIT notice in LICENSE.upstream.txt. The package manifest records revisions and changes.

## Evidence before claims

1. Identify exactly what the proposed claim covers and the corresponding acceptance criteria.
2. Inspect the current saved deliverable. Select checks that can establish the claim: commands, direct calculations, source comparison, or permitted manual observations as appropriate.
3. Execute the relevant checks when they have not been run against this state. Read the result and exit status; check actual behavior or content, not only successful execution.
4. Reuse evidence from the same unchanged state when its scope is still applicable. If related code, data, configuration or assumptions changed, rerun affected checks. Do not rerun unrelated full suites for every progress message.
5. State the actual result with evidence and limitations. Partial evidence supports only a partial claim.

## Common distinctions

| Proposed claim | Relevant evidence | Insufficient by itself |
|---|---|---|
| Tests/build pass | Actual relevant command and result against current files | A different check, a prediction, zero tests or all skipped |
| A bug is fixed | Original important symptom now behaves correctly; useful regression coverage if feasible | A code change or agent assurance |
| An API works | Required response content, error behavior and storage effect as applicable | Open port or status 200 |
| A report is correct | Required sources, calculations and saved output agree | File existence or plausible prose |
| Requirements are met | Mandatory requirements mapped to actual outputs and observations | Passing tests with missing required behavior |
| Delivery succeeded | Actual delivery state required by the task | Preview success |

Do not introduce a framework, external service, browser automation, destructive rollback, or a new worktree just to satisfy this instruction. Use a meaningful failing-to-passing check when it can establish a regression; do not risk a working deliverable solely to perform a ritual.

When another agent reports success, inspect its relevant artifacts and evidence before adopting the claim. A diff can establish what changed, but does not alone establish correctness.

Use PLAN's progress/evidence section or the task's existing equivalent for command/observation, relevant files, actual result and remaining gaps. Do not create a separate worklog. Label manual checks, skipped optional checks, blocked mandatory requirements and not-yet-checked behavior separately. Never fabricate results or alter expected values to fit output.

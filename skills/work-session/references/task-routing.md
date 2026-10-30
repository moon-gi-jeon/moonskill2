# Task routing and risk checks

Use only relevant rows. The purpose is to choose a small complete path and consequential checks, not create a new taxonomy, fixed stage sequence or exhaustive checklist.

| Actual output | Relevant risk and evidence |
|---|---|
| Data, spreadsheet or numerical report | Confirm units, denominator, period, missing/duplicate/conflicting records and provenance where they affect the result. Derive an important expected value from original inputs/rules independently of the production function. Keep observations separate from causal claims. |
| Policy or source-based document | Confirm source authority, effective date, exceptions and the relation between a claim and its actual evidence. Do not silently resolve conflicting rules or invent missing numbers. |
| A supplied API client | Confirm the actual contract, provided authentication, response content, completeness and allowed destinations. Check pagination, limits and retry side effects only when relevant. Do not retry an uncertain write blindly. |
| A new or changed API | Define input/output, important errors and storage effects before implementation; verify a real request-to-result path and required persistence. A private model key or new database is not implied. |
| User interface | Verify required input-to-result states, error/empty/loading behavior and connected data as applicable. Distinguish HTTP/code checks from permitted human screen interaction. Do not claim a visual or interaction check from static markup. |
| Existing code repair | Observe the original symptom, make a task-sized change and check affected existing behavior. Do not rewrite an unrelated working system. |
| Workflow, language or domain-specific output | Establish actual user roles, terms, permissions and success conditions first. Manufacturing metrics, translation rules or approval chains are conditional domain facts, not universal requirements. |

Select the most consequential likely errors and the cheapest useful check for each. Wrong totals, lost writes, stale output, inconsistent rules and missing mandatory behavior can matter more than cosmetic completeness. Preserve the actual task's priorities.

In PLAN, connect the selected risks to requirement IDs and checks. Record **confirmed / failed / not checked / needs human check** (or the task's equivalent) without treating a skipped or absent check as a pass. After a relevant change, identify the stale evidence and rerun the affected checks.

Read domain facts from supplied sources or the task owner's actual answer. Use specialized Skills only when that path exists. If the expected path is absent, classify it as inapplicable, unavailable or a mandatory blocker rather than constructing an unrelated environment.

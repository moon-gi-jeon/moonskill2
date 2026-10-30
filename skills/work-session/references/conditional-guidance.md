# Conditional guidance

Read only the part needed for the current task. These are decision examples, not a checklist to execute in every project.

## Absence, blocking and retries

| Observation | Appropriate next action |
|---|---|
| An optional Skill is not installed | Perform the relevant reasoning directly if feasible. Record unavailable once; do not claim Skill invocation or auto-install dependencies. |
| No API requirement exists | Mark the API-specific path not applicable. Do not create endpoints to exercise a tool. |
| A required input is missing | Check referenced location and relevant file listing, then record the affected requirement as blocked and ask the owner. Do not invent data or silently reduce the scope. |
| No existing test command | Use task-sized direct checks or necessary manual review. Do not report zero tests as a functional pass. |
| Automated UI operation is forbidden or absent | Use permitted non-UI checks and ask the user for manual preview observations. Do not install another automation tool to bypass the restriction. |
| The same command fails for the same reason | Stop unchanged attempts. Use a new observation to choose a meaningful alternative, or report the blocker. |
| An expected optional document is absent | Record the absence. Create a working document only if its purpose is necessary; do not reconstruct a supposed official source. |
| An approval or permission is denied | Preserve the boundary. Continue permitted independent work; do not find another channel to repeat the denied action. |

## Choose supporting Skills only when useful

- `grill-me` / `grilling`: examine the user's proposed approach, consequential assumptions and tradeoffs. Honor the work-session plan approval gate even if a general helper suggests immediate execution. Avoid repeated questions about known facts.
- `frontend-design`: when a user-facing visual interface is part of the task; not a requirement to build one.
- `api-and-interface-design`: when creating or changing an API/interface. For a small task, specify methods, inputs/outputs, important errors and persistence requirements as needed; do not assume authentication, pagination or an external paid API.
- `api-tester`: when an actual service contract exists and permitted HTTP checks add value. It does not supply missing credentials or prove a UI works.
- `diagnosing-bugs`: when an important failure needs diagnosis; use observed symptoms and a useful reproduction rather than speculative reinstalling.
- `verification-before-completion`: use for evidence before the final completion claim. Relevant checks also occur during the work; final verification does not replace them.

Names and dependencies may differ by environment. Inspect the available instruction before using it; none of these supporting Skills is a mandatory dependency of this package.

## Match evidence to output

- Web/API: the smallest important request/action-to-result flow, significant invalid inputs, required persistence, and permitted manual preview. A 200 response alone does not prove the returned content is correct.
- Data/analysis: source provenance, transformation logic, required totals/samples and important missing/invalid-data behavior. Distinguish an observed difference from a causal explanation and its supporting evidence. Do not change expected values to match the output.
- Documents: required content, source alignment, numbers and an appropriate saved-output check. Do not impose a web/server setup.
- Changes after a check: identify which evidence may be stale and rerun the relevant checks, not automatically every possible check.

Keep task records in the permitted workspace. Follow the actual allowed public-material, external-service and submission boundaries; optional tooling cannot override them.

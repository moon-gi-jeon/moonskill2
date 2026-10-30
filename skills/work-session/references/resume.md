# Interruption and resume

Use at an actual pause, context loss or session transfer. Reuse the existing PLAN handoff section when sufficient. If a compact separate file helps transfer to another session or workspace, create/update HANDOFF using the [template](../assets/HANDOFF.template.md) and link it from PLAN. Keep PLAN/DECISIONS and the actual files canonical: HANDOFF points to them rather than duplicating a second requirement or progress ledger. Do not generate it for ordinary progress. Follow the task's AI-use and submission boundaries at the current stage.

Preserve only what another permitted session needs:
- Current objective and approved plan revision; important source/owner-answer changes.
- Actual output/code/data locations and current saved state. Include a commit/hash only when available and useful; do not initialize Git to obtain one.
- Last relevant check: command or observation, input, expected and actual result, file/version scope and evidence location. Distinguish runtime, content and human checks.
- Remaining mandatory gaps, blockers, assumptions and consequential pending decisions.
- Next one useful action and its completion check; pending review status if any.

On resume, inspect the current files and applicable task stage before acting. A snapshot is a navigation aid, not proof. Compare relevant input/configuration/code with the state covered by the recorded evidence. Recheck affected or unverifiable claims and mark stale results explicitly; reuse unchanged applicable evidence rather than rerunning everything.

Preserve prior meaningful decisions and superseding relationships. A resumed session does not by itself require another approval of the same unchanged plan. Ask when the approved scope or consequential assumptions changed. Do not resume automatically after the user has cancelled the task or after AI use is no longer permitted.

For concise user requests, see [prompt guide 12 and 13](prompt-guide.md#request-12). The receiving session should also read applicable AGENTS guidance. A valid handoff does not prove that the host loaded the new session instructions automatically.

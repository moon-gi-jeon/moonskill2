---
name: diagnosing-bugs
description: Diagnose important observed bugs or persistent failures with task-sized reproductions, evidence-led hypotheses, bounded attempts, and relevant fix verification.
---

# Diagnosing Bugs

Adapted from Matt Pocock's diagnosing-bugs guidance. Retain the upstream MIT notice in LICENSE.upstream.txt. The package manifest records revisions and changes.

## Start from the observed failure

- Identify the required behavior, exact input/action, actual result and affected files. Read relevant existing module notes if available; do not create missing GLOSSARY/ADR files to begin debugging.
- First distinguish an implementation defect from an absent optional tool, a missing mandatory input, an environment restriction or a mistaken expectation. Respect the task and the approved plan.
- For absent optional items, record non-applicability/unavailability and a simple fallback once. For mandatory blockers, record impact and the question or allowed alternative. Do not label either case a repaired bug.

## Establish a useful signal

Prefer an existing failing test, task HTTP request, CLI input, direct calculation or focused instrumentation that reaches the reported symptom. If visual interaction is required, ask for the participant's manual observation and inspect the related local code/HTTP path; do not automate or capture the browser.

Reproduce and narrow the failure enough to distinguish causes. Full mathematical minimization, an unattended reproduction, or a new testing framework is not a prerequisite for every fix. If reproduction is unavailable, disclose it; inspect relevant evidence and ask only for the missing observation that changes the next action.

## Test a specific hypothesis

- Use the evidence to choose the most useful explanation and a check that can disprove it. Consider competing explanations when ambiguous; do not generate a fixed number of hypotheses as ceremony.
- Change one meaningful variable at a time where practical. Keep temporary logging focused and omit secrets.
- Each further attempt needs a new observation, changed hypothesis/action and a useful next check. Do not repeat an unchanged failed command or reinstall dependencies under the same conditions.
- Keep effort proportional to required functionality, remaining time and the permitted environment. Do not stress remote services, launch fixed 100/1000-run loops, bypass a restriction or keep investigating optional work without a reason.

## Fix, check and record

Make a task-sized correction within the approved scope. Verify the original important symptom and affected behavior; add a useful regression check when feasible. Do not claim a fix from a code edit alone.

Remove your temporary instrumentation and preserve unrelated user work. Record the symptom, supported cause or remaining uncertainty, change, actual validation and remaining impact in PLAN's progress/evidence section or the existing equivalent. Do not create a separate worklog. When further progress needs input or unavailable access, report the blocker and continue independent work. Reopen it only when facts or instructions change.

# Conditional independent review

## Select only useful supported delegation

Prefer the main session for small clear work. Consider an independent reviewer for material requirement omissions, consequential calculations, complex changes, uncertain error handling or a test gap a second perspective can resolve. Another copy of the same summary is not sufficient value.

Use only the host's already available and permitted agent tools. This guidance authorizes requesting a bounded review within the approved task; it does not grant new tool permissions or external access. Do not change models, feature flags, approval settings, install plugins or runtimes, request credentials or connect another AI provider to obtain subagents.

- If the tool is absent or forbidden, skip the agent path immediately and record its absence once in PLAN.
- If an advertised tool fails, make no unchanged repeated attempt. Record the reason if known and continue with permitted direct checks or a sequential review. Do not bypass a denial with another channel.
- If capacity is busy, continue independent work. Wait or retry only when new availability evidence and remaining time justify it. Do not delay mandatory validation or delivery for an optional review.
- Reopen this path only when capabilities, facts or user instructions change. A sequential self-review is useful but is not an independent agent review.

Start with one reviewer. Use a second only for a distinct, valuable perspective that can run independently. Do not spawn a cascade of reviewers, require a fixed number, or repeat reviews until every opinion says PASS. Parallel implementation requires separate explicit task justification, file ownership and integration planning; it is outside this default review policy.

## Give a bounded review contract

Include the objective, relevant source/requirement IDs, exact files or snapshot, permitted tools, read-only scope, expected output and a task-sized completion condition. Give primary evidence and minimal necessary context, not the proposed verdict. Reviewers should not read each other's findings before their initial review when independence is useful.

Possible roles:
- Requirements reviewer: compare actual behavior/files with required sources and actual owner answers. Identify omissions and rule conflicts.
- Correctness reviewer: inspect consequential logic, boundary/error cases, expected values and test gaps. Distinguish observed defects from conjectures.

Reviewers do not modify shared project files. Static inspection is the default; execute a check only if permitted and it cannot affect shared state, or use an explicitly isolated copy/scratch area. Do not give a reviewer secrets or permission to transmit task data externally.

Return concise findings: requirement/source, file and location, issue and impact, reproduction or evidence, observed versus untested status, and suggested next check. State when nothing material was found, and what was actually reviewed. Do not manufacture findings.

## Main agent integrates and verifies

Inspect the underlying files/evidence, merge duplicates and resolve contradictory opinions before accepting a finding. A reviewer's PASS is not proof of completion. Fix confirmed issues within the approved scope and run the relevant actual checks; take consequential new choices back to the user.

Record only meaningful findings, adopted/rejected disposition and actual validation in PLAN. Put a consequential choice and its reason/alternative/limit in DECISIONS. Keep pending reviews and remaining mandatory gaps visible. Re-review only when new changes, failures or unresolved risk justify it.

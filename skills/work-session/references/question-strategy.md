# Task-owner question strategy

Use when task materials leave a consequential gap, an owner answer arrives, or new evidence changes the plan. Keep questions and answers in PLAN rather than a separate interview document.

## Find gaps that matter

After reviewing supplied materials, compare the objective and required result with what is actually known. Look for missing context about the current workflow and pain point, intended user, required inputs/outputs, meaning of data, business rules and exceptions, constraints, success criteria and priority. Do not treat a previous example as a fixed questionnaire.

A question is useful when different plausible answers would change the goal interpretation, required behavior, acceptance check, scope or an important implementation choice. Do not ask for facts already supplied, decisions the user already made, or optional details that cannot change the next work. Prioritize blockers and potentially costly misunderstandings; send a short round rather than a long exhaustive survey.

## Ask the right person

- Task owner: actual workflow, business intent and facts, constraints, important exceptions, what counts as a successful result. Ask for necessary product composition, not an implementation recipe.
- User: a choice among justified alternatives, scope tradeoffs or a decision the owner has left open. Label **[사용자결정]** when needed.
- Platform support: access, environment, submission or permitted-operation questions. Keep these separate from business questions.

The coding agent proposes architecture and implementation choices from the confirmed needs. Do not outsource all design to the task owner or assume the owner knows the required technology stack.

## Draft a concrete question

Use a short **[문의필요]** draft with its intended recipient. Ask one coherent factual issue and, when helpful, connect it to an observed document, input example or boundary case. Keep the rationale/implementation impact in PLAN; do not send a technical essay as the question.

Examples to adapt, not assume:

- Instead of "Tell me everything to build", ask "After the user completes the current action, what result must they see or keep?"
- Instead of "What are all the rules?", point to a real case: "The sample has a cancelled record with an amount. Is it included in the requested total?"
- Instead of asking the owner which database/framework to use, establish whether data must survive a restart and whether there is a mandated environment; then propose a task-sized design to the user.

Do not lead the owner into confirming an invented requirement. An open question about actual work can be more useful than a forced A/B choice. If an answer is too broad or unavailable, narrow to a consequential example or ask once about the relevant answer boundary; do not repeatedly request the whole solution in different words.

## Track and integrate

1. Record the draft, affected requirement and impact in PLAN. The user sends it and relays the actual reply.
2. Distinguish draft, sent, answered, partial and unavailable; never infer transmission, receipt or approval.
3. Preserve the important reply meaning and source. Separate owner-confirmed facts, user choices, agent inferences and pending assumptions.
4. Update the affected requirement and expected behavior, implementation slice and acceptance check. Mark affected earlier evidence as stale when appropriate.
5. Put a consequential changed choice, alternative or limit in DECISIONS; do not duplicate the entire reply there.
6. Report the changed understanding and next action. Continue within an approved unchanged scope; request a decision when the answer materially changes that scope or contradicts a mandatory condition.

If the owner is unavailable or an answer remains unknown, record its impact. Proceed with independent work. Use a disclosed assumption only where the actual task permits it and the consequence is acceptable; keep mandatory blocked requirements visible. Do not invent business facts or keep questioning after the necessary information is clear.

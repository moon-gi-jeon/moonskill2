---
name: frontend-design
description: Make deliberate, usable visual and interaction choices when a required user-facing interface is built or substantially changed; keep design proportional to the brief.
license: Complete terms in LICENSE.txt
---

# Frontend Design

Adapted from anthropics/skills; modified on 2026-10-30 for a task-scoped workflow. Retain the Apache-2.0 terms in LICENSE.txt. The package manifest records revisions and changes.

## Start from the actual brief

Read the intended user, primary action, required content, existing stack and constraints. Do not invent previous client rejections, preferences or user decisions. Follow an explicit visual direction even if it resembles a common style. If the task needs no interface, this Skill is not applicable.

Integrate a short design rationale into the existing PLAN when the interface approach affects the result. For a functional tool, prioritize a clear complete user flow over a separate branding exercise. Additional moodboards, ASCII alternatives or multiple design passes are optional techniques for a meaningful open design problem, not gates before every small UI change.

## Make intentional choices

- Use subject-appropriate layout, color, type and spacing. A compact token set helps consistency; do not force a fixed number of colors or typefaces.
- Let visual hierarchy explain the actual content and actions. Use headings, borders, numbering and grouping when they carry information rather than as repeated decoration.
- Avoid a stock hero, identical card grids, arbitrary gradient accents and unnecessary labels when they obscure the task. A simple familiar layout is appropriate when it best serves the brief.
- Keep readable line lengths, legible type, adequate contrast and clear control states. Maintain visible keyboard focus, meaningful labels, responsive layout and reduced-motion preferences where relevant.
- Use motion sparingly to explain a state change. Do not add animation merely to make the output look elaborate.
- Make loading, empty, success and important failure states understandable. Name actions consistently, such as Save changes -> Saved; explain a recoverable error with a concrete next action.
- Use plain user-facing language and actual permitted content. Keep implementation details out of the user's flow unless they help the user decide.

## Implement and review proportionately

Build the smallest required input-to-result flow in the provided stack. Watch CSS interactions, responsive behavior and accessibility as you change relevant components. Preserve required behavior before polish.

Use permitted local code/HTTP checks and the participant's manual preview feedback. Do not automate or capture the browser/screen. Do not add external fonts, assets, accounts or services unless necessary and permitted. Review against the brief and actual behavior; a separate second design pass is useful only if it addresses a real gap.

Record consequential design decisions and evidence in existing documents. Do not create a new approval ritual for ordinary work within the approved PLAN.

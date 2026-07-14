---
name: ai-builder-director
description: Turn an AI product idea, interface, prototype, or real-user test record into an explicit product spine, a five-second first-impression test, a usability-observation plan, and an evidence-based next iteration. Use when a builder needs to choose between plausible product directions, clarify what users should notice and do, prepare or synthesize real-user testing, audit whether an AI-generated experience expresses deliberate intent, or decide what single variable to change next. Do not use AI role-play as a substitute for real users.
---

# AI Builder Director

Help the Builder direct a product experience deliberately, then test whether real users receive that intent. Treat the Builder as the decision-maker, AI as a questioning and evidence-structuring partner, and users as the source of behavioral evidence.

## Choose the route

Identify the user's current stage from the request and available material. Do not force the full workflow when one route is enough.

| Need | Route | Result |
| --- | --- | --- |
| Several reasonable ideas compete | Product spine | One explicit tradeoff that guides decisions |
| A page or entry point may send the wrong signal | Five-second test | A test script and expectation-versus-response record |
| A working flow needs validation | User rehearsal | A realistic task and behavior-observation sheet |
| Test notes already exist | Evidence synthesis | Supported patterns, uncertainties, and one next variable |
| The product is being shaped end to end | Full loop | Spine → first impression → rehearsal → next iteration |

If the request already contains enough context, start working. Otherwise ask only for the smallest missing input needed for the selected route.

Read [references/method-cards.md](references/method-cards.md) when executing a route. Locate and read the matching tool section; do not load or reproduce unrelated templates unless the user requests the full workflow.

## Route 1: Define the product spine

1. Capture the target user, critical situation, desired outcome, competing choices, and existing user evidence.
2. Ask one question at a time, up to five questions. Prioritize what the Builder is willing and unwilling to sacrifice.
3. Reject universal adjectives such as “simple,” “innovative,” or “warm” unless they are converted into observable choices.
4. Draft three to five candidates in this form:

   `When [target user] is in [critical situation], we would rather [A] than [B], because the user truly needs [C].`

5. For every candidate, state two decisions it supports, one plausible decision it rejects, and its cost.
6. Ask the Builder to rewrite or confirm the final spine. Never silently choose it for them.
7. If requested, classify existing ideas as keep, revise, or remove using only the confirmed spine.

## Route 2: Prepare a five-second first-impression test

1. Ask the Builder to state what a user should first notice, think the page does, and do next.
2. Prepare a neutral test: show the page to an uninvolved target or proxy user for five seconds, hide it, then ask the same three questions without explanation.
3. Create a record with `intended`, `actual response`, `gap`, and `participant ID` for all three questions.
4. After multiple sessions, group repeated patterns and cite participant IDs and words. Separate supported findings from unresolved questions.
5. Recommend at most three elements to inspect, based on the records, then ask the Builder to select one variable for the next round.

When given a screenshot, prototype, or page, inspect it to improve the test plan. Label any interface critique as an expert hypothesis, not user evidence. Do not impersonate target users or fabricate test answers.

## Route 3: Plan a user rehearsal

1. Define one validation question, one realistic task, a working version, and the team's expected understanding and path.
2. Instruct the facilitator not to explain the intended use or begin by asking whether the participant likes it.
3. Record the first pause, first misunderstanding, and first action that differs from the expected path.
4. Also record timestamps, direct quotes, expected-versus-actual behavior, what the user expected next, and what genuinely made the task easier.
5. End with three decision options: keep, change the presentation, or revisit the product spine. Leave the final choice to the Builder.

## Route 4: Synthesize real-user evidence

1. Preserve raw wording and participant identifiers.
2. Separate observable behavior, direct quotes, and observer inference.
3. Do not infer a motive from a pause or convert a preference into a requirement.
4. Identify the three firsts and up to three cross-user patterns. Require repeated evidence before calling something a pattern.
5. For every conclusion, cite the supporting participant IDs and excerpts. State `insufficient evidence` when support is missing.
6. Propose the next validation question and the options to keep, change presentation, or revisit the spine.
7. Ask the Builder to choose one variable to change next. Do not bundle several changes into one round.

## Deliver the result

Lead with the decision artifact or test artifact, not a lecture about the framework. Keep outputs ready to paste into a research plan, product brief, or test record.

Always distinguish:

- Builder intent and decisions;
- real-user evidence;
- observer interpretation;
- AI-generated hypotheses.

State what remains unknown. Do not claim validation when no real user has participated.

## Source and attribution

This workflow was developed for episode 02 of the Chinese `AI Builders 解读` series from ideas in Kim Beverett's Config 2026 talk, *Be the Director: How Stage Craft Informs Product Craft*. The product-spine, five-second-test, and user-observation formulations are editorial tools created for the episode; do not attribute those names or exact templates to Beverett.

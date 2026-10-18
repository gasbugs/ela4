---
name: ela4
description: Evaluate recommendations against the user's completion conditions, challenge consequential proposals, execute authorized four-star-or-higher work, and reassess from evidence. Use when the user invokes ELA4 or requests this recommendation-and-execution loop.
---

# ELA4 — Execute, Challenge & Reassess

## Scope and continuity

First distinguish implementation from analysis, review, and proposal requests. For a bounded deliverable, producing that deliverable is the authorized work; recommendations inside it do not authorize their implementation. Follow user instructions, repository rules, and existing approvals. A high score never authorizes unrelated scope, spending, external messages, or destructive actions. Do not ask again for effects already authorized.

Inspect current files, decisions, dirty changes, and relevant runtime evidence. Memory and previous reports are leads, not current proof. Reuse the existing plan and carry completion conditions, explicit exclusions, assumptions, critical blockers, and reasons for rejected or deferred work across invocations. Reopen a rejected or deferred item only when relevant requirements, evidence, or conditions change.

Keep the user's full intended outcome. Do not redefine completion around what is already implemented or easy to test. Do not expand required scope merely because another useful improvement is discovered. Tie additions to an unmet requirement or a demonstrated safety or data-integrity issue. Correct mistaken assumptions with evidence; obtain user direction when a choice materially changes the intended outcome or cost. Decide routine implementation details within existing authorization.

## Select by incremental value

For substantive next actions, identify the requirement served, missing evidence, completion check, and consequence of deferral. Compare the strongest alternative, including leaving the current state unchanged. No fixed candidate count or separate table is needed for obvious small work.

Distinguish direct outcomes, necessary support work, and exploration. Support work needs a named dependency and an endpoint; preparation for blocked work must produce something usable when the blocker clears. Exploration needs a question and a decision its answer can change.

Score the **additional value of this action given current evidence**, not the importance of the whole feature:

- **5/5:** Substantial direct progress on an important completion condition or removal of a critical blocker.
- **4/5:** Clear material progress, a necessary prerequisite, or resolution of a consequential uncertainty.
- **3/5 or less:** Weak relevance, insufficient additional value, or cost disproportionate to the remaining benefit.

Track readiness separately: executable, useful preparation possible, or blocked by access/input/external change. A blocked important task stays important; an easy task does not outrank it merely because it is executable. Compare urgency, dependencies, confidence, cost, and risk. Do not inflate scores to keep looping. If existing evidence is adequate, explain what remaining risk justifies additional work.

## Challenge the proposal

Before first execution of a nontrivial proposal, and after material failure, scope growth, or cost growth, perform a short adversarial review. Seek concrete counterexamples:

- Could this pass its checks without satisfying the user's requirement?
- Is this repeating adequate evidence, fixing the test apparatus, or compensating for a mistaken assumption?
- Is easier peripheral work displacing the main blocker?
- What existing behavior could break, and under what conditions?
- Does added complexity or dependency cost exceed the benefit? Is a simpler approach or no change better?
- What evidence would cause this proposal to be rejected or revised?

For material findings, identify the affected requirement, failure conditions, supporting evidence, and disposition. Distinguish facts, inferences, and assumptions. A clear defect path can justify action before reproduction; a generic possibility alone does not justify new implementation.

Revise proposals when warranted and recheck the finding and affected behavior. Explain substantive findings left unresolved. Do not fill a criticism quota or recursively review unchanged wording. If no new material counterexample remains, proceed to execution or a bounded experiment. Self-review is not independent verification. Do not add delegation or external review unless available and authorized.

## Execute and verify

Execute the highest-value actionable item scoring at least 4/5 within the authorized scope. Preserve unrelated user work and live resources. When a consequential choice requires input, explain the choice, recommendation, effects, and why input is needed; keep required answers pending while continuing independent eligible work. Silence is not approval.

Before execution, set a proportionate completion condition, affected checks, and rough effort expectation. Exceeding that expectation triggers reassessment against new evidence and alternatives, not automatic abandonment or repeated permission requests. Avoid detailed estimates and extra artifacts for trivial work.

A check must establish a required guarantee, cover a plausible regression from the change, or resolve decision-relevant uncertainty. Expected success is not a reason to skip necessary regression checks. Reuse passing evidence only while its code, environment, and assumptions remain applicable. Changes to interfaces, state transitions, packaging, or runtime environment require affected integration checks. Preserve repository-mandated gates. Batch setup where useful without weakening scenario isolation or removing failure conditions to make checks pass.

Classify failures as product defects, test-tool defects, environment problems, or requirement/assumption errors. Retry only with new diagnostic evidence, a revised hypothesis, or corrected conditions. Otherwise investigate the common cause or change approach. An observation timeout alone does not prove a running task stopped: recheck its handle or authoritative state before restarting.

## Reassess results, not activity

One cycle selects a work hypothesis, executes it, and uses evidence to judge the result and next action. Investigation, implementation, tests, documentation, and Git are stages within a cycle, not five cycles. Rejected hypotheses can be useful results without being completed requirements. Cycle count is an execution limit, not a performance metric.

After each cycle, update which completion conditions changed, what uncertainty was reduced, and which critical blockers remain. Separate necessary follow-up from optional improvement. If small checks accumulate while major blockers stay unchanged, compare priorities again. Do not abandon difficult core work solely because visible progress is slow; consider new evidence, the approach's validity, and alternatives.

Keep one concise turn-local action/outcome/evidence entry for the next evaluation. Distinguish progress, a verified wait on a live operation, and no progress. Status restatements are not progress. Reuse existing conversation or required project records across invocations; do not create a persistent tracker or memory unless requested or required. Do not reset the objective merely because a new invocation begins.

## Stop and report

Stop when the requested bounded deliverable is complete, no authorized actionable item scores at least 4/5, or **five execution cycles** have completed in this invocation. Also stop when progress requires unavailable input/access or a prohibited action and no independent eligible work remains. Do not invent work to fill the limit, lower blocked priorities to claim completion, or treat invocation termination as overall goal completion.

At the cycle limit, stop starting new improvement work. Confirm the state of operations already started and complete necessary cleanup or restoration, or explicitly hand off their live status and remaining responsibility. Reaching the limit alone is not evidence that an operation has stopped and is not authorization to terminate it. Do not use cleanup as a pretext for additional feature work.

Before claiming the overall goal complete, map every completion condition to current evidence of matching scope. Missing, indirect, or partial evidence is not completion. At the cycle limit, explicitly report remaining 4/5-or-higher items and critical blockers. This skill does not itself run after the turn or schedule automation. Host-driven continuations must retain scope and unresolved decisions rather than resetting the loop.

Provide concise progress updates. In the final report use a compact table with recommendation/linked completion condition, score, action, evidence, and status; include unfinished or blocked 4/5-or-higher work within scope. Distinguish code preparation, synthetic checks, live integration, and operational deployment. Record test-apparatus repair as support work, not completed product functionality. Test totals, commits, and document volume are not independent measures of progress.

State the completion-condition change, remaining blockers, cycle count, and exact stop reason. Briefly justify the next choice if one remains. Do not claim unmeasured efficiency gains, completion percentages, or time savings. A skill revision is not evidence of improved behavior; when evaluating revisions, use bounded realistic cases and subsequent observed work, and acknowledge differing comparison conditions.

---
name: ela4
description: Evaluate the next actionable recommendations on a five-star scale, execute authorized four-star-or-higher work, and reassess until no such work remains. Use when the user invokes ELA4 or requests this recommendation-and-execution loop.
---

# ELA4 — Execute & Loop Actions 4-star+

Use this skill for the user's stated task and scope. A recommendation is not authorization to expand into unrelated projects, spend money, delete resources, or bypass repository rules. Apply the repository's `AGENTS.md` and relevant domain skills before changing files or infrastructure.

1. Inspect current state, existing decisions, dirty files, plans, and validation evidence. Treat remembered status as a lead to verify, not proof of current state.
2. List concrete next actions with a score out of five and a short reason. Score impact, urgency, prerequisite value, confidence, and validation cost. A task is actionable only when its target, completion condition, and safe validation path are clear. Split broad projects into independently verifiable actions; do not inflate scores to prolong the loop.
   - **5/5:** High impact, ready to execute, strong evidence, straightforward validation, and very low change risk. Never claim risk is literally zero.
   - **4/5:** Clear material benefit and feasible validation, with manageable risk or resource cost.
   - **3/5 or less:** Limited benefit, weak evidence, unclear outcome, or risk/cost disproportionate to the benefit. An important but blocked task remains high priority; mark it blocked rather than lowering its score.
3. Before a 4/5-or-higher action, use `grillme` when the score is borderline because key evidence is missing, the action has a consequential branch, or it may materially change a live system, incur substantial cost, or cause an irreversible effect. Ask the user to resolve the specific choice, including why the action matters and the concrete side effects; offer a recommended option and alternatives. Do not ask for approval again when the session already authorizes the same action and its effects. Keep required questions pending until answered; silence is not consent. Continue independent eligible work while waiting, and decide routine implementation details yourself.
4. Execute the highest-value actionable item scoring at least 4/5. Preserve user changes and live resources. Follow existing authorization and approval requirements for external or irreversible effects. If one item is blocked, continue with independent eligible work.
5. Verify the result with checks appropriate to the change. Append one concise line to a turn-local loop log recording the action, outcome, and evidence; carry this log into the next evaluation. Do not create a repository log or write persistent memory unless the user or repository rules require it. Reinspect state and rescore the remaining actions; do not carry forward stale scores.
6. Stop when no actionable item within the authorized scope scores at least 4/5, or after **five execution cycles** in this invocation, whichever comes first. Also stop when progress requires missing access, user input, or a prohibited operation and no independent eligible work remains. Explain the blocker; never relabel blocked work below 4/5 simply to declare completion. At the five-cycle limit, report all remaining 4/5-or-higher items explicitly.

Provide concise progress updates during a long run. At the end, report completed actions, validation evidence, remaining recommendations with scores, and any blockers. The loop does not run in the background after the current turn; schedule future runs only if the user requests an automation.

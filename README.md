# ELA4

ELA4 (Execute, Challenge & Reassess) is a Codex skill that scores the incremental value of next actions against the user's completion conditions, challenges nontrivial proposals, executes authorized work rated at least 4/5, and reassesses from evidence. Importance and readiness are separate. Analysis or proposal requests authorize the requested deliverable, not implementation of its recommendations.

One cycle covers selection, execution, verification, and reassessment; those stages are not separate cycles. Stop when the bounded deliverable is complete, no eligible 4/5 action remains, or five cycles have completed. Keep unresolved completion conditions and prior deferral decisions across continuations. At the cycle limit, stop new improvement work while completing necessary cleanup or explicitly handing off active operations.

## Install

```bash
gh repo clone gasbugs/ela4 ~/.codex/skills/ela4
```

Invoke it with `$ela4`, or ask Codex to run the ELA4 recommendation loop. The skill applies the active repository's own instructions and authorization boundaries. It runs in the current turn; it does not schedule background work.

The skill instructions are in [SKILL.md](SKILL.md).

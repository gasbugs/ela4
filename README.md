# ELA4

ELA4 (Execute & Loop Actions 4-star+) is a Codex skill that scores the next actionable recommendations, executes authorized work rated at least 4/5, then reassesses. It stops when no eligible 4/5 action remains or after five execution cycles. When a consequential choice needs user input, it asks a focused `grillme` question and waits for the answer.

## Install

```bash
gh repo clone gasbugs/ela4 ~/.codex/skills/ela4
```

Invoke it with `$ela4`, or ask Codex to run the ELA4 recommendation loop. The skill applies the active repository's own instructions and authorization boundaries. It runs in the current turn; it does not schedule background work.

The skill instructions are in [SKILL.md](SKILL.md).

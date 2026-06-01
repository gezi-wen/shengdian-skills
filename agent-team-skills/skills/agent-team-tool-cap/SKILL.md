---
name: agent-team-tool-cap
description: >
  Caps tool output length for sub-agents. Excess output is written to temp files
  instead of flooding context. Sub-agents only; orchestrator must NOT load.
---

# Agent Team — Tool Output Cap

**Sub-agents only. Orchestrator must NOT load.**

## Rules

All read-only tool output (read/grep/glob/bash) exceeding these limits:

| Limit | Threshold |
|-------|-----------|
| Lines | 15 lines |
| Characters | 600 chars |

When exceeded: show first 15 lines / 600 chars, write remainder to `/tmp/agent-team/{agent-name}/{tool}-{timestamp}.out`. Reference the file path in your response — don't paste the full output.

## Exceptions (never truncate)

- Diff results from write/edit operations
- Error messages
- Security tool output (bandit, npm audit, etc.)
- When orchestrator explicitly requests full output

## Example

```
Read package.json → 30 lines → show first 15 + "⋯ full output: /tmp/agent-team/security-reviewer/read-1717200000.out"
```

```
Diff result → never truncated, shown in full
```

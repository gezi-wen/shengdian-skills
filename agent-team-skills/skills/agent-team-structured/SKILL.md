---
name: agent-team-structured
description: >
  Enforces structured output format for multi-agent teams. No paragraph reports —
  numbered findings only. Sub-agents only; orchestrator must NOT load.
---

# Agent Team — Structured Output

**Sub-agents only. Orchestrator must NOT load.**

## Required Format

Each finding must be one line using this format:

```
[#{number}] [{severity}] [{line}] {one-line description}
→ @{teammate}: {question} (only if you need a teammate's input)
```

Severity: `critical` `medium` `suggestion`

## Example

```
[#1] [critical] [L30] Unsanitized tool output written directly to terminal
→ @security-reviewer: Can you confirm this is the ANSI injection vector?

[#2] [medium] [L44] No fallback rendered when error status has no result text
```

## Forbidden

- Paragraph-style reports
- Transition phrases ("I think", "Maybe consider")
- Findings longer than 2 lines
- Restating previous findings

## Fallback

Full paragraphs allowed when: orchestrator requests detail, responding to @-mention, or explaining security-critical issues.

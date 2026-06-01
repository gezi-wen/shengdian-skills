# Agent Team Skills

Three composable skills for running efficient multi-agent teams in Claude Code.

## Install

```bash
npx skills add gezi-wen/agent-team-skills
```

## Skills

| Skill | What it does |
|-------|-------------|
| `agent-team-caveman` | Caveman output compression (~65% token saving) + team collaboration rules |
| `agent-team-structured` | Enforces numbered findings format — no paragraph reports |
| `agent-team-tool-cap` | Caps tool output at 15 lines / 600 chars, writes excess to temp files |

## Usage

Load all three on sub-agents. The orchestrator should NOT load them.

```bash
claude --skills agent-team-caveman,agent-team-structured,agent-team-tool-cap
```

## How They Work Together

```
agent-team-caveman     → compresses output style
agent-team-structured  → enforces [##] [severity] [line] format
agent-team-tool-cap    → prevents context flooding from large tool outputs
```

All three stack without conflict.

## License

MIT

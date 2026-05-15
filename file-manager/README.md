# File Manager / 文件管家

A Claude Code skill for server & project directory organization. Scan messy directories, propose clean structures, execute step-by-step, and audit with sub-agents in parallel.

服务器/项目目录整理 skill。扫描散乱目录→设计整洁结构→分步执行→派子 agent 并行审计。

## Features / 功能

- **Scan & Diagnose** — identify scattered files, duplicates, stale copies, misplaced large files, broken path references
- **Design Proposal** — output target directory tree with before/after comparison
- **Safe Execution** — low-risk to high-risk, each step reversible
- **Path Correction** — scan 6 categories of config files and update stale path references
- **Sub-Agent Audit** — 2-3 agents verify cron jobs, project integrity, and config paths in parallel
- **Dry-Run Mode** — output plan without execution
- **Project Lifecycle Tags** — active / paused / archived

**功能：** 扫描诊断、设计提案、安全执行、路径修正、分殿并行审计、dry-run 模式、项目生命周期标注

## Install / 安装

```bash
cp -r shengdian-skills/file-manager ~/.claude/skills/
```

## Trigger / 触发

Say things like "整理一下这个目录"、"服务器太乱了"、"这些文件该放哪"、 "organize this directory"、 "clean up my server files".

## Safety / 安全

Built-in safety rules: never touches `~/.ssh/`, system configs, or hidden app directories. All destructive operations require explicit user confirmation.

内置安全红线：不碰 `~/.ssh/`、系统配置、隐藏应用目录。破坏性操作需用户明确确认。

## License / 许可

MIT

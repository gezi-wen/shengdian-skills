# Shengdian Skills / 圣殿 Skills

A collection of Claude Code Skills created by [Shengdian](https://github.com/gezi-wen). Each skill is standalone — take what you need.

由[圣殿](https://github.com/gezi-wen)创作的 Claude Code Skills 合集。每个 skill 独立可用，按需取用。

## Skills

| Skill | Description / 说明 |
|-------|-------------------|
| [file-manager](./file-manager/) | Server & project directory organizer. Scan → propose → execute → audit with sub-agents. Dry-run supported. / 服务器项目目录整理，扫描→提案→执行→子agent并行审计 |
| [skill-patrol](./skill-patrol/) | AI agent skill patrol. Weekly scan of GitHub trending skills & MCP tools, curated recommendations. / AI Agent 技能巡检，每周扫描 GitHub 热门 skill/MCP 并推送推荐 |
| [agent-team-skills](https://github.com/gezi-wen/agent-team-skills) | Multi-agent team token saving bundle: caveman compression + structured output + tool output cap. / 多 agent 团队省 token 三件套：Caveman 压缩 + 结构化输出 + 工具输出截断 |

## Install / 安装

```bash
git clone https://github.com/gezi-wen/shengdian-skills.git
# Install what you need / 按需安装
cp -r shengdian-skills/file-manager ~/.claude/skills/
cp -r shengdian-skills/skill-patrol ~/.claude/skills/
```

## Related / 相关项目

- [nte-auto-fish](https://github.com/gezi-wen/nte-auto-fish) — Game automation script / 游戏自动化脚本

## License / 许可

MIT

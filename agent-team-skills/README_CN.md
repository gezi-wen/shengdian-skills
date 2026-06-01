# Agent Team Skills · 分殿三件套

让 Claude Code 多 agent 团队协作更省 token、更结构化的三个可组合 skill。

## 安装

```bash
npx skills add gezi-wen/agent-team-skills
```

## 技能

| 技能 | 作用 |
|-------|------|
| `agent-team-caveman` | Caveman 输出压缩（省约 65% token）+ 团队协作规则 |
| `agent-team-structured` | 强制编号发现格式——禁止段落报告 |
| `agent-team-tool-cap` | 工具输出超过 15 行/600 字自动截断，余量写临时文件 |

## 使用

三个 skill 仅加载给子 agent，协调者（主进程）不加载。

```bash
claude --skills agent-team-caveman,agent-team-structured,agent-team-tool-cap
```

## 协作原理

```
agent-team-caveman     → 压缩输出风格（碎片句、略冠词、短同义词）
agent-team-structured  → 强制 [##] [严重度] [行号] 格式
agent-team-tool-cap    → 防大工具输出淹没上下文
```

三个可叠加使用，互不冲突。

## 许可

MIT

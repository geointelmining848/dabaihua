# dabaihua（大白话）

让你的 AI 助手把复杂的专业概念、术语、论文段落，讲成五六岁小孩也能听懂的大白话——**准确、简单、不装幼稚**。中英文都能用。

## 这是什么

一段纯 Markdown 写成的"技能"（Agent Skill，遵循开放的 SKILL.md 标准）。不需要安装任何程序，不联网，不含代码——它教 AI 一套"讲人话"的方法：

- **三条铁律**：简单但不幼稚；不用术语解释术语；简单但不失准。
- **四步工作流**：抓本质 → 换世界（把概念映射到糖果、玩具、小猫小狗的世界）→ 三层输出 → 五岁测试自检。
- **固定输出模板**：一句话说清 / 打个比方 / 其实是（把比喻对回原概念，防止讲错）/ 记住这句。
- **进阶工具箱**：按领域的比喻素材库（统计、金融、计算机、物理、医学、法律、地理）、整段专业文字翻译策略、巨大数字换算技巧。

## 安装（按你用的工具对号入座）

### Claude Code

```bash
git clone https://github.com/geointelmining848/dabaihua ~/.claude/skills/dabaihua
```

或者：下载本仓库 zip（Code → Download ZIP），解压后把文件夹放进 `~/.claude/skills/`。
Windows 对应路径：`%USERPROFILE%\.claude\skills\dabaihua`。装完新开一个会话即可。

### OpenClaw

```bash
openclaw skills install git:geointelmining848/dabaihua
# 或者本仓库 clone 到本地后：
openclaw skills install ./dabaihua          # 装进当前 workspace
openclaw skills install ./dabaihua --global # ~/.openclaw/skills，对所有 agent 生效
```

### Codex CLI

把本仓库复制到 `$CODEX_HOME/skills/dabaihua`（默认 `~/.codex/skills`）。

### claude.ai / Claude 桌面版

Settings → Capabilities → Skills，上传本仓库的 zip（直接用 Download ZIP 下载的即可，后缀就是 .zip）。

### WorkBuddy

技能管理页导入 `dabaihua.skill` 安装包。

### 其他工具 / 不支持技能的聊天机器人

把 `SKILL.md` 中 `---` 以下的正文复制进你的系统提示词 / 自定义指令 / 规则文件；`references/advanced.md` 作为附件上传，或告诉 AI 需要时再读。本质是一套方法，任何够聪明的 AI 都能照做。

## 用法

装好后自然提问即可，技能会自动触发：

- "用大白话解释一下高斯马尔可夫随机场"
- "把这段合同条款说成人话：……"
- "讲简单点，我听不懂"
- "ELI5: how does machine learning work?"
- "explain this in plain language: ..."（贴任何看不懂的专业文字）

## 仓库内容

| 文件 | 说明 |
|---|---|
| `SKILL.md` | 技能本体（方法、规则、输出模板、完整示例） |
| `references/advanced.md` | 进阶工具箱（按领域的比喻素材库等），按需加载 |
| `LICENSE` | MIT |

## English in brief

**dabaihua** is an open-format Agent Skill (SKILL.md) that teaches any AI assistant to explain complex concepts, terms, and dense passages in plain language a 5-6 year old could understand — accurate, simple, never condescending. Works with Claude Code, OpenClaw, Codex CLI, claude.ai, WorkBuddy and any SKILL.md-compatible harness. Install paths above; triggers on keywords like *plain language / ELI5 / simplify / 说人话 / 大白话*. MIT licensed.

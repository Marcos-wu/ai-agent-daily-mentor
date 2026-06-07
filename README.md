# AI Agent Daily Task

中文 AI Agent 每日任务生成 skill。本分支专门用于为 Python 零基础或基础薄弱学习者生成 8 周、两个月路线中的每日任务、每周大纲、反馈调整和知识点维护。

> 分支用途：`codex/beginner-friendly-daily-skill`
>
> `main` 分支仍保留原标准每日导师 skill。本分支只生成“每日任务”，不生成标准版内容。

## 核心特点

- **每日任务**：默认输出零基础可照做的日课任务，不需要额外说明其他版本。
- **8 周路线**：总周期固定为 8 周，也就是两个月。
- **英文目录名**：推荐 `daily-tasks/`、`weekly-outlines/`、`knowledge-notes/`。
- **中英混合文件名**：文件名可以中文、英文或中英混合，重点是可读稳定。
- **克制 Obsidian 双链**：核心概念保留 `[[...]]`，代码块内禁止双链。
- **可复制运行代码**：代码必须完整、可运行、有中文注释和基础异常处理。

## 项目结构

```text
ai-agent-daily-mentor/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── daily-task-template.md
    ├── 8-week-spine.md
    ├── adaptation-policy.md
    ├── day1-seed.md
    ├── final-project-blueprint.md
    ├── internship-success-insights.md
    ├── obsidian-linking-policy.md
    ├── obsidian-note-maintenance-policy.md
    └── weekly-outline-template.md
```

## 工作模式

### 1. 每日任务

触发词示例：

```text
生成 Day 1
生成今天的每日任务
明天任务
零基础版 Day 2
根据反馈继续
```

输出结构：

```markdown
# 📅 Day N：主题

## 🧭 今日方向
## 🧠 先用生活比喻搞懂
## 🎯 今天只做这三件事
## 🪜 手把手路线（总共 X 小时）
## 💻 跟写代码区
## 🚑 卡点急救包
## 🧩 概念对照表
## ✅ 今日验收清单
## 📝 今日复盘小纸条
## 📥 明日同步接口
```

### 2. 每周大纲

每周大纲也采用每日任务视角，必须包含：

- 本周目标。
- 本周最低可交付成果。
- Day 1-Day 7 每日任务。
- 每日卡点预警。
- 周末复盘与下周衔接。

### 3. 文件输出

推荐英文目录：

```text
weekly-outlines/
daily-tasks/
knowledge-notes/
```

推荐文件名：

```text
weekly-outlines/Week1-Python-MUP-HTTP-Git.md
daily-tasks/Day1-Python工程环境与函数基础.md
daily-tasks/Day2-HTTP与API调用.md
knowledge-notes/Python虚拟环境.md
```

如果用户给了已有目录，优先遵从用户路径；如果没有给目录，只输出建议路径和 Markdown 内容。

### 4. 反馈调整

如果用户反馈代码没跑通、概念没懂或报错，下一次每日任务要明显放慢：

- 减少当天新概念。
- 增加生活比喻和对照表。
- 给最小复现和排查顺序。
- 把验收题改成更小的修复任务。

### 5. Obsidian 知识点维护

可以从每日任务中提取双链并生成知识点笔记，但每天只建议补 3-5 个重点知识点，避免知识库膨胀。知识点文件推荐放到 `knowledge-notes/`。

## 8 周节奏

- Week 1-2：以跑通和理解为主，减少抽象术语压力。
- Week 3-5：进入 `AI-Interview` 业务模块，但每个 Day 只做一个最小业务模块。
- Week 6-7：做 Agent 和项目闭环，把复杂工作流拆成流程图、小工具和最小状态机。
- Week 8：只做包装、README、演示、简历话术和面试复盘，不引入新重技术。

## 双链规则

- 核心概念首次出现时加双链，例如 `[[Python 虚拟环境]]`、`[[环境变量与 API Key]]`。
- `关联知识：` 中放 3-5 个稳定双链。
- 文件名、命令、环境变量、API 路径使用反引号，例如 `main.py`、`python -m venv .venv`、`LLM_API_KEY`。
- 代码块内部禁止出现 `[[...]]`。
- 不为同一概念反复加链接。

## 使用方式

把本分支作为单独 skill 使用时，让 agent 读取 `SKILL.md`，并按需参考 `references/`。

如果 agent 支持技能目录，可以把整个 `ai-agent-daily-mentor/` 文件夹放入 skills/prompts/resources 目录；如果 agent 直接读取工作区，就在对话中明确提到本目录或要求读取 `SKILL.md`。

## 注意事项

- 本分支不修改 `main` 上的标准导师行为。
- 本分支只生成“每日任务”，不生成标准版内容。
- 总学习周期固定为 8 周，也就是两个月。
- Windows 环境校验中文 UTF-8 文档时，建议使用 `PYTHONUTF8=1`。

## License

MIT

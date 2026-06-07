# 🤖 AI Agent Daily Mentor Beginner-Friendly Branch

中文 AI Agent 新手友好日课生成 skill。本分支专门用于生成 Python 零基础/基础薄弱学习者能跟着做的保姆级每日学习内容，并支持按课程文件夹习惯生成“标准版 + 新手友好版”两份 Markdown。

> 分支用途：`codex/beginner-friendly-daily-skill`
>
> `main` 分支仍保留原标准每日导师 skill。本分支是新手友好版实验/专用分支，不自动合并回 `main`。

## 核心特点

- **新手友好长篇日课**：生活比喻、只做三件事、分步路线、常见问题、验收清单。
- **成对文件输出**：需要生成课程文件时，默认规划 `标准版/` 和 `新手友好版/` 两份内容。
- **克制 Obsidian 双链**：核心概念保留 `[[...]]`，代码块内禁止双链，阅读不被打断。
- **可复制运行代码**：代码必须完整、可运行、有中文注释和基础异常处理。
- **保留 8 周主线**：仍参考 AI Agent 实习冲刺路线和 `AI-Interview` 最终项目，但以新手理解优先。

## 项目结构

```text
ai-agent-daily-mentor/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── beginner-friendly-daily-template.md
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

### 1. 新手友好版每日内容

触发词示例：

```text
生成 Day 1 新手友好版
零基础版 Day 2
保姆级讲解 Day 3
用新手友好感生成今天内容
```

输出结构：

```markdown
# 📅 Day N：主题（新手友好版）

## 🧭 先别急着写代码！搞懂这三个比喻
## 🎯 今天要完成的事（只做三件事！）
## ⏰ 分步学习路线（总共 X 小时）
## 💻 今天的核心代码
## 🧩 关键概念对照表
## ❓ 新手常见问题
## ✅ 今日验收清单
## 📥 明日同步接口
```

### 2. 标准版 + 新手友好版成对文件

触发词示例：

```text
生成 Week1 Day1 文件
像 ai-agent-冲刺计划 那样保存课程内容
生成标准版和新手友好版两份 Day 2
```

推荐输出路径：

```text
ai-agent-冲刺计划/
├── Week1-Python-MUP-HTTP-Git.md
├── 标准版/
│   └── Day1-Python-工程环境与函数基础.md
└── 新手友好版/
    └── Day1-Python工程环境与函数基础-新手友好版.md
```

### 3. 反馈调整

如果用户反馈代码没跑通、概念没懂或报错，新手友好版优先放慢节奏：

- 减少当天新概念。
- 增加生活比喻和对照表。
- 给最小复现和排查顺序。
- 把验收题改成更小的修复任务。

### 4. Obsidian 知识点维护

可以从新手友好版日课中提取双链并生成知识点笔记，但每天只建议补 3-5 个重点知识点，避免知识库膨胀。

## 双链规则

- 核心概念首次出现时加双链，例如 `[[Python 虚拟环境]]`、`[[环境变量与 API Key]]`。
- `关联知识：` 中放 3-5 个稳定双链。
- 文件名、命令、环境变量、API 路径使用反引号，例如 `main.py`、`python -m venv .venv`、`LLM_API_KEY`。
- 代码块内部禁止出现 `[[...]]`。
- 不为同一概念反复加链接。

## 参考资料

| 文件 | 用途 |
|------|------|
| `beginner-friendly-daily-template.md` | 新手友好版日课结构、双链策略和成对文件规则 |
| `8-week-spine.md` | 8 周学习主线 |
| `weekly-outline-template.md` | 每周大纲结构 |
| `adaptation-policy.md` | 根据反馈调整难度 |
| `day1-seed.md` | Week 1 / Day 1 起步校准 |
| `obsidian-linking-policy.md` | 双链稳定命名 |
| `obsidian-note-maintenance-policy.md` | 知识点笔记补全策略 |

## 使用方式

把本分支作为单独 skill 使用时，让 agent 读取 `SKILL.md`，并按需参考 `references/`。

如果 agent 支持技能目录，可以把整个 `ai-agent-daily-mentor/` 文件夹放入 skills/prompts/resources 目录；如果 agent 直接读取工作区，就在对话中明确提到本目录或要求读取 `SKILL.md`。

## 注意事项

- 本分支不修改 `main` 上的标准导师行为。
- 如果只说“生成 Day N”，本分支会偏向新手友好输出；如果要标准版，请明确说“生成标准版 Day N”。
- 如果要求写文件但没有给目标目录，agent 应先输出建议路径和 Markdown 内容，不擅自创建未知目录。
- Windows 环境校验中文 UTF-8 文档时，建议使用 `PYTHONUTF8=1`。

## License

MIT

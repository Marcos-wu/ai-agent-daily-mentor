# 🎓 AI Agent Daily Mentor — 新手友好版

> 面向 Python 零基础学习者的 8 周 AI Agent 实习冲刺每日任务生成器。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Branch: codex/beginner-friendly-daily-skill](https://img.shields.io/badge/branch-codex%2Fbeginner--friendly--daily--skill-blue)](https://github.com/Marcos-wu/ai-agent-daily-mentor/tree/codex/beginner-friendly-daily-skill)

---

## 这是什么？

**AI Agent Daily Mentor** 是一个 AI 驱动的学习助手 skill，专门为 **Python 零基础或基础薄弱** 的学习者设计。

它能做什么？

- 📅 **自动生成每日学习任务** — 每天只聚焦 2-3 件事，保姆级手把手教学
- 📋 **生成每周学习大纲** — 8 周完整路线，从零到可展示的 AI Agent 项目
- 🔄 **根据反馈自适应调整** — 代码没跑通？自动放慢节奏，增加比喻和排查
- 🧩 **维护 Obsidian 知识库** — 自动生成带双链的知识点笔记
- 💻 **所有代码可复制运行** — 完整中文注释、异常处理、Type Hints

**最终目标：** 8 周后你能独立完成一个 `AI-Interview：基于 RAG 与 Agent 的智能模拟面试系统`，并具备实习面试能力。

---

## 核心功能

### 1. 每日任务生成

输入"生成 Day 1"或"今天任务"，即可获得一份完整的每日学习任务：

```
📅 Day 1：Python 工程环境与函数基础
├── 🧭 今日方向          — 今天学什么、为什么学
├── 🧠 生活比喻搞懂      — 用"私人厨房"解释虚拟环境
├── 🎯 今天只做三件事    — 聚焦不分散
├── 🪜 手把手路线        — 每步有操作、预期、排查
├── 💻 跟写代码区        — 可复制运行的完整代码
├── 🚑 卡点急救包        — 常见报错和解决方案
├── 🧩 概念对照表        — 术语 × 比喻 × 用途
├── ✅ 今日验收清单      — 可验证的完成标准
├── 📝 复盘小纸条        — 填空式反思
└── 📥 明日同步接口      — 反馈模板，驱动自适应
```

### 2. 每周大纲规划

自动生成每周学习计划，包含：
- 本周目标和最低可交付成果
- Day 1 - Day 7 每日任务拆解
- 每日卡点预警
- 周末复盘与下周衔接
- 本周核心产出物（目录结构 + 简历话术）

### 3. 反馈自适应调整

根据你的每日反馈，自动判断学习状态并调整：

| 状态 | 判断条件 | 自动调整 |
|------|---------|---------|
| ✅ 正常推进 | 代码能跑、验收通过 | 按计划继续 |
| ⏳ 放慢复习 | 代码没跑通、概念没懂 | 降低 30-50% 难度，增加比喻 |
| 🚀 加难扩展 | 提前完成、能讲清概念 | 加一个工程化扩展任务 |
| 🔄 重排本周 | 连续两天卡住 | 重排剩余内容，缩小目标 |
| 🔧 补工程化 | 只有 Demo 没有服务化 | 优先补 FastAPI/README/测试 |

### 4. Obsidian 知识点维护

- 自动提取每日任务中的 `[[双链]]`
- 按出现频率和求职重要性评分
- 每天建议补充 3-5 个重点知识点
- 支持轻量笔记、标准笔记、详细笔记三种级别

### 5. 8 周完整路线

| 阶段 | 周数 | 内容 | 产出 |
|------|------|------|------|
| Phase 1 | Week 1-2 | Python 基础 + FastAPI | LLM CLI 工具 + 后端骨架 |
| Phase 2 | Week 3-5 | LLM API + RAG + 结构化输出 | 简历解析 + 面试题库检索 |
| Phase 3 | Week 6-7 | Agent + Function Calling + LangGraph | 智能面试闭环系统 |
| Phase 4 | Week 8 | 包装 + 面试冲刺 | 可展示项目 + 简历话术 |

---

## 如何下载

### 方式一：Git Clone（推荐）

```bash
# 克隆整个仓库
git clone https://github.com/Marcos-wu/ai-agent-daily-mentor.git

# 切换到新手友好版分支
cd ai-agent-daily-mentor
git checkout codex/beginner-friendly-daily-skill
```

### 方式二：只下载新手友好版分支

```bash
# 克隆时直接指定分支
git clone -b codex/beginner-friendly-daily-skill https://github.com/Marcos-wu/ai-agent-daily-mentor.git
```

### 方式三：GitHub 页面下载

1. 打开 [https://github.com/Marcos-wu/ai-agent-daily-mentor](https://github.com/Marcos-wu/ai-agent-daily-mentor)
2. 点击绿色 **Code** 按钮
3. 选择 **Download ZIP**
4. 解压后，确保你在 `codex/beginner-friendly-daily-skill` 分支的内容中

---

## 项目结构

```
ai-agent-daily-mentor/
├── SKILL.md                  ← 核心：skill 定义文件（AI 读取这个来工作）
├── README.md                 ← 你正在看的文件
├── agents/
│   └── openai.yaml           ← OpenAI agent 配置
└── references/               ← 参考资料目录
    ├── daily-task-template.md      ← 每日任务模板
    ├── weekly-outline-template.md  ← 每周大纲模板
    ├── 8-week-spine.md             ← 8 周主线骨架
    ├── adaptation-policy.md        ← 反馈自适应规则
    ├── obsidian-linking-policy.md  ← Obsidian 双链规范
    └── obsidian-note-maintenance-policy.md ← 知识点维护规范
```

---

## 如何使用

### 方式一：在支持 Skill 的 AI Agent 中使用

如果你使用的 AI Agent 支持加载 skill：

1. 将整个 `ai-agent-daily-mentor/` 文件夹放入 Agent 的 skills 目录
2. Agent 会自动读取 `SKILL.md` 并按指令工作
3. 直接对话即可：

```
你：生成 Day 1
AI：（自动生成完整的 Day 1 每日任务）

你：明天任务
AI：（自动生成 Day 2）

你：【Day 1 学习反馈】
    1. 今天实际学习时长：4小时
    2. 完成了哪些代码/文件：config.py, history.py
    ...
AI：（根据反馈自动调整 Day 2 难度）
```

### 方式二：在对话中引用

如果你的 Agent 支持读取工作区文件：

1. 确保 `ai-agent-daily-mentor/` 在你的工作目录中
2. 在对话中提到该目录，或要求 Agent 读取 `SKILL.md`
3. Agent 会按照 skill 定义的行为工作

### 方式三：直接复制 SKILL.md 内容

将 `SKILL.md` 的内容复制到你的 AI Agent 的 system prompt 或 skill 配置中。

---

## 使用示例

### 示例 1：生成每日任务

```
你：生成 Day 3

AI 输出：
📅 Day 3：大模型 API 最小调用

🧭 今日方向
今天你要完成一件事：用 httpx 调通第一个大模型 API，
让 AI 回你一句话。这是整条链路的第一个"通了"的里程碑。

🧠 先用生活比喻搞懂
比喻 1：大模型 API = 电话客服中心
...

🎯 今天只做这三件事
1. 发送第一个 API 请求
2. 理解 messages 的三种角色
3. 封装 LLMClient 类
...
```

### 示例 2：反馈驱动调整

```
你：【Day 2 学习反馈】
    1. 今天实际学习时长：5小时
    2. 完成了哪些代码/文件：test_http.py
    3. 哪个概念最清楚了：GET 请求
    4. 哪个概念还没懂：异常处理的 try/except
    5. 卡住的 Bug / 报错全文：TypeError
    6. 今天代码跑通了几道题：2道
    7. 明天希望：放慢复习

AI：根据你昨天反馈异常处理还没跑通，今天先不推进 LLM API 调用，
    改为把 try/except、raise_for_status 和超时处理彻底打牢。
    今天只做两件事：
    1. 用 3 个生活比喻重新理解异常处理
    2. 写 5 个最小例子，每个只练一种错误类型
    ...
```

### 示例 3：生成每周大纲

```
你：生成 Week 1 大纲

AI 输出：
📅 Week 1：Python MUP + HTTP + Git

1. 本周方向
   本周目标是跑通一个 LLM CLI 调用工具...
2. 本周新手门槛
   最容易卡住的 3 个点：虚拟环境激活、.env 配置、httpx 安装...
3. Day 1 - Day 7 每日任务
   Day 1: Python 工程环境与函数基础
   Day 2: HTTP 与 API 调用
   ...
```

---

## 分支说明

| 分支 | 用途 | 适合谁 |
|------|------|--------|
| `main` | 标准导师 skill | 有 Python 基础的学习者 |
| `codex/beginner-friendly-daily-skill` | 新手友好版每日任务 | **Python 零基础学习者** ← 你在这里 |

本分支（`codex/beginner-friendly-daily-skill`）的特点：
- 每天只聚焦 2-3 件事，避免概念过载
- 用生活比喻解释所有抽象概念
- 代码逐行中文注释
- 自带卡点急救包和验收清单
- 支持根据反馈自适应调整节奏

---

## FAQ

### Q: 我完全没学过 Python，能用这个 skill 吗？

可以。这个 skill 就是为零基础设计的。Week 1 从创建虚拟环境、写第一个函数开始，每天都有生活比喻和手把手代码。

### Q: 8 周真的能学会 AI Agent 开发吗？

8 周的目标不是成为专家，而是能独立完成一个可展示的 AI Agent 项目，并具备实习面试的基础能力。每天 4-5 小时，按路线走就行。

### Q: 最终项目是什么？

`AI-Interview：基于 RAG 与 Agent 的智能模拟面试系统`。包含简历解析、岗位匹配、面试题库 RAG 检索、AI 评分和面试报告生成。

### Q: 我需要用 Obsidian 吗？

不是必须的。skill 会自动在内容中加入 `[[双链]]`，如果你用 Obsidian，这些链接会自动生效。不用 Obsidian 也不影响学习。

### Q: 能跳过某一天直接学后面的吗？

不建议。每天的内容是递进的，跳过可能导致后面看不懂。如果某天提前完成，可以做扩展任务，但不要跳到下一周。

### Q: 反馈模板一定要填吗？

强烈建议填。feedback 是自适应调整的依据——你填了"异常处理没懂"，下一天就会自动放慢、增加比喻和练习。不填反馈，AI 只能按默认节奏推进。

---

## 相关资源

- [GitHub 仓库](https://github.com/Marcos-wu/ai-agent-daily-mentor)
- [新手友好版分支](https://github.com/Marcos-wu/ai-agent-daily-mentor/tree/codex/beginner-friendly-daily-skill)
- [标准版 main 分支](https://github.com/Marcos-wu/ai-agent-daily-mentor/tree/main)

---

## License

MIT License. 自由使用、修改和分发。

---

<p align="center">
  <b>🚀 开始你的 8 周 AI Agent 冲刺之旅吧！</b><br>
  <sub>从 Day 1 的第一个虚拟环境，到 Week 8 的完整项目展示。</sub>
</p>

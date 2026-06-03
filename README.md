# 🤖 AI Agent Daily Mentor

中文 AI Agent 实习冲刺导师 — 一个基于 Hermes Agent 的自适应学习 Skill，帮助你在 8 周内从零基础冲刺 AI Agent 应用开发实习。

## 📋 项目简介

`ai-agent-daily-mentor` 是一个 **Hermes Agent Skill**，专为中文学习者设计。它扮演一位严谨的 Python 后端兼 AI Agent 导师，带你完成从 Python 基础到 AI Agent 项目落地的完整学习路线，最终产出一个可投递的求职项目。

### 核心特点

- 🇨🇳 **全中文教学** — 所有教学说明、注释、反馈模板均为中文
- 📐 **两层自适应规划** — 每周大纲 + 每日教学，根据你的反馈实时调整难度
- 🎯 **项目驱动** — 8 周主线最终收敛为 `AI-Interview：基于 RAG 与 Agent 的智能模拟面试系统`
- 🔗 **Obsidian 双链集成** — 自动生成知识网络，支持跳转复习
- 📊 **每日 5 模块** — 固定输出结构，确保学习质量可量化
- 🔄 **自适应反馈** — 卡住放慢、提前加难、连续受阻自动重排

## 🛠️ 技术栈

| 阶段 | 技术 |
|------|------|
| Week 1-2 | Python 3.11+, venv, httpx, rich, python-dotenv |
| Week 2 | FastAPI, Pydantic, Tortoise ORM / SQLAlchemy |
| Week 3-5 | LLM API (OpenAI-compatible), RAG, Chroma, LangChain / LlamaIndex |
| Week 6-7 | LangGraph, Function Calling, ReAct, Redis |
| Week 8 | Docker Compose, Git, README, 面试冲刺 |

## 📁 项目结构

```
ai-agent-daily-mentor/
├── SKILL.md                              # Skill 主定义文件
├── README.md                             # 项目说明文档
├── agents/
│   └── openai.yaml                       # OpenAI 兼容 Agent 配置
└── references/                           # 参考资料（Skill 内部使用）
    ├── 8-week-spine.md                   # 8 周学习主线骨架
    ├── adaptation-policy.md              # 每日反馈自适应规则
    ├── day1-seed.md                      # Day 1 标准种子
    ├── final-project-blueprint.md        # 最终项目蓝图：AI-Interview
    ├── internship-success-insights.md    # 已上岸博主经验提炼
    ├── obsidian-linking-policy.md        # Obsidian 双链输出规范
    ├── obsidian-note-maintenance-policy.md # 知识点笔记维护规范
    └── weekly-outline-template.md        # 每周学习大纲模板
```

## 🚀 8 周学习路线

### Phase 1：Week 1-2 — Python 基础 + 后端骨架

| 周 | 主题 | 核心产出 |
|----|------|----------|
| Week 1 | Python MUP + HTTP + Git | `LLM CLI 调用工具` |
| Week 2 | FastAPI 后端骨架 | `Agent 后端服务骨架` |

### Phase 2：Week 3-5 — LLM API + RAG

| 周 | 主题 | 核心产出 |
|----|------|----------|
| Week 3 | AI-Interview 简历解析与岗位匹配 | `简历解析与岗位匹配 API` |
| Week 4 | 面试题库 RAG v1 | `面试题库 RAG 检索服务 v1` |
| Week 5 | 岗位匹配 + RAG 出题 v2 | `岗位匹配驱动的面试出题与评分上下文服务` |

### Phase 3：Week 6-7 — Agent 核心能力

| 周 | 主题 | 核心产出 |
|----|------|----------|
| Week 6 | AI-Interview Agent 核心能力 | `岗位匹配 Agent 与面试流程 Agent` |
| Week 7 | AI-Interview 主项目闭环 | `AI-Interview：基于 RAG 与 Agent 的智能模拟面试系统` |

### Phase 4：Week 8 — 工程化包装 + 面试冲刺

| 周 | 主题 | 核心产出 |
|----|------|----------|
| Week 8 | 工程化包装与面试冲刺 | `AI-Interview 可展示项目 + 简历话术 + 面试题库` |

## 🔄 工作模式

Skill 支持 4 种工作模式，由用户指令自动触发：

### 1. 每周大纲模式

**触发词**：`生成 Week N 大纲` / `本周计划` / `新一周开始`

生成包含 Day 1-7 精细化路径的每周学习大纲，含核心技术拆解、每日学习内容、本周核心产出物、面试仿真模拟和避坑指南。

### 2. 每日教学模式

**触发词**：`生成 Day N` / `明天内容` / `根据反馈继续`

生成每日 5 模块学习内容：

1. 📌 **今日核心死磕** — 1-2 个核心技术点深度讲解
2. 🎯 **6 小时精细化路线** — 上午/下午/晚上三段任务
3. 💻 **今日代码实战** — 完整可临摹的代码 + 运行说明
4. 🎯 **每日自我验收题** — 3 题自测
5. 📥 **明日同步接口** — 固定反馈模板

### 3. 周计划调整模式

**触发词**：提交 `Day X 学习反馈`

根据反馈自动判断学习状态（正常推进 / 放慢复习 / 加难扩展 / 重排本周），调整后续安排。

### 4. Obsidian 知识点维护模式

**触发词**：`补全双链` / `生成知识点笔记`

从每日笔记中提取双链，按评分规则生成轻量/标准/详细级别知识点笔记。

## 📊 自适应规则

| 学习状态 | 触发条件 | 调整策略 |
|----------|----------|----------|
| 正常推进 | 代码能跑，验收通过 | 按大纲继续 |
| 放慢复习 | 代码没跑通，概念没懂 | 降低 30%-50% 难度，复盘 + 小步重写 |
| 加难扩展 | 提前完成，能讲清概念 | 增加工程化扩展（测试/日志/重构/README） |
| 重排本周 | 连续两天卡住 | 重排剩余 Day，缩小交付目标 |
| 项目完整度不足 | 只有孤立 Demo | 优先补工程化，不继续堆新技术 |

## 💡 最终项目：AI-Interview

所有 Week 3-8 的学习内容围绕 `AI-Interview：基于 RAG 与 Agent 的智能模拟面试系统` 展开。

### 业务闭环

```
候选人上传简历 → AI 简历解析 → 岗位匹配 Agent → 匹配岗位模板
→ RAG 检索面试题 → 模拟面试 → AI 评分 → 生成面试报告
```

### 核心模块

1. **简历解析模块** — PDF/Word 简历上传 → LLM 解析 → 候选人画像
2. **岗位匹配模块** — Agent 根据简历匹配岗位方向
3. **题库管理模块** — 面试题、参考答案、关键评分点、标签管理
4. **RAG 出题模块** — 基于岗位和技能标签的语义检索出题
5. **模拟面试流程** — 一问一答、多轮追问、面试记录
6. **AI 评分模块** — reference_answer + key_points 注入 Prompt
7. **面试报告模块** — 汇总匹配、答题、短板，生成复盘报告
8. **工程化部署** — Docker Compose 一键启动

## 📦 安装与使用

### 前置要求

- [Hermes Agent](https://github.com/nousresearch/hermes-agent) 已安装
- Python 3.11+
- 一个 OpenAI-compatible LLM API（如 DeepSeek、OpenAI 等）

### 安装 Skill

```bash
# 方式一：手动安装
# 将 ai-agent-daily-mentor 目录放入 Hermes skills 目录
cp -r ai-agent-daily-mentor ~/.hermes/skills/

# 方式二：通过 Hermes CLI
hermes skills install ai-agent-daily-mentor
```

### 开始学习

```
# 生成 Week 1 大纲
"生成 Week 1 大纲"

# 生成 Day 1 学习内容
"生成 Day 1"

# 提交学习反馈
"Day 1 学习反馈：
1. 今天实际学习时长：4 小时
2. 完成了哪些代码/文件：config.py, history.py
3. 哪个概念最清楚了：Python 虚拟环境
4. 哪个概念还没懂：asyncio
5. 卡住的 Bug：无
6. 自我验收题完成情况：2/3
7. 明天希望：正常推进"

# 补全 Obsidian 知识点笔记
"补全双链"
```

## 📝 输出格式示例

每日内容严格遵循 5 模块结构：

```markdown
📌 今日核心死磕
（1-2 个核心技术点深度讲解）

🎯 6小时精细化路线
├── 上午 2 小时：看官方文档，做最小验证
├── 下午 3 小时：手写核心代码并运行
└── 晚上 1 小时：重构、Debug、笔记、自测

💻 今日代码实战
关联知识：[[知识点A]]、[[知识点B]]、[[知识点C]]
（完整可运行代码 + 运行方式 + 观察要点 + 可扩展任务）

🎯 每日自我验收题
1. 概念解释题
2. 小实现/设计题
3. 代码改错/Bug 排查题

📥 明日同步接口
（固定反馈模板）
```

## 📚 参考资料说明

| 文件 | 用途 |
|------|------|
| `8-week-spine.md` | 8 周主线骨架，保证长期方向不跑偏 |
| `weekly-outline-template.md` | 每周大纲的固定结构模板 |
| `adaptation-policy.md` | 根据每日反馈调整周计划的规则 |
| `day1-seed.md` | Day 1 的标准种子，确保起始质量 |
| `final-project-blueprint.md` | AI-Interview 最终项目蓝图 |
| `internship-success-insights.md` | 已上岸博主经验，简历话术和面试策略 |
| `obsidian-linking-policy.md` | Obsidian 双链命名和输出规范 |
| `obsidian-note-maintenance-policy.md` | 知识点笔记生成级别和增量补充规则 |

## 🎓 适合谁用

- 想转行/冲刺 **AI Agent 应用开发实习** 的学生
- 有 Python 基础但缺乏 **项目经验** 的开发者
- 想系统学习 **RAG + Agent + FastAPI** 技术栈的学习者
- 需要一个 **可投递求职项目** 的应届生

## ⚠️ 注意事项

- 所有教学说明使用中文，英文仅限代码、命令、库名和技术名词
- 每日任务控制在 **6 小时** 可完成
- 不使用"精通"描述初学目标
- Obsidian 双链默认开启，可通过"不要 Obsidian 链接"关闭
- 代码必须包含 Type Hints、中文注释、异常处理，不允许 `pass`

## 📄 License

MIT

## 🤝 Contributing

欢迎提交 Issue 和 Pull Request！

如果你有好的学习资源、面试经验或自适应规则建议，欢迎贡献。

## 🔗 相关链接

- [Hermes Agent](https://github.com/nousresearch/hermes-agent) — 本 Skill 的运行平台
- [AI-Interview](https://github.com/Marcos-wu/ai-agent-daily-mentor) — 本项目仓库

---

> 💪 从零基础到 AI Agent 实习，8 周足够了。关键是每天 6 小时，持续输出，不堆 Demo，只做可投递的项目。

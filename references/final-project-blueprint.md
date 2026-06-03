# 最终主项目蓝图：AI-Interview

本文件用于校准 Week 3-8 的学习大纲和每日内容。默认最终项目为 `AI-Interview：基于 RAG 与 Agent 的智能模拟面试系统`。

## 项目定位

面向求职场景的 AI 模拟面试系统，不是单独 RAG，也不是单独 Agent，而是将 RAG 和 Agent 整合到同一条业务链路中。

核心闭环：

`候选人上传简历 -> AI 简历解析 -> 岗位匹配 Agent -> 匹配岗位模板 -> RAG 检索面试题 -> 模拟面试 -> AI 评分 -> 生成面试报告`

## 推荐技术栈

- 后端：FastAPI
- 数据库：PostgreSQL
- 向量检索：pgvector，学习早期可用 Chroma 降低门槛
- 缓存和任务：Redis + Celery
- LLM：DeepSeek API 或 OpenAI-compatible API
- Embedding：DashScope Embedding 或其他可替换 Embedding 服务
- RAG 框架：LangChain 或 LlamaIndex
- Agent：LangChain Tool Calling Agent，后续可扩展 LangGraph
- 部署：Docker Compose

## 核心模块

### 1. 简历解析模块

功能：

- 上传 PDF/Word 简历。
- 提取文本。
- 调用 LLM 解析教育背景、项目经历、技能栈、工作意向。
- 生成候选人画像。

### 2. 岗位匹配模块

功能：

- 输入目标岗位 JD 或岗位模板。
- Agent 根据简历画像匹配岗位方向。
- 输出岗位匹配度、优势、短板、建议面试方向。

### 3. 题库管理模块

功能：

- 管理面试题、参考答案、关键评分点、岗位标签、技术标签。
- 支持题目录入、筛选、向量化。

### 4. RAG 出题模块

功能：

- 根据岗位、技能标签、候选人短板检索题目。
- 支持题目向量化、语义检索、筛选。
- 返回题目、参考答案、关键评分点。

### 5. 模拟面试流程模块

功能：

- 按岗位生成面试流程。
- 支持一问一答。
- 保存面试记录。
- 支持多轮追问。

### 6. AI 评分模块

功能：

- 将用户回答、`reference_answer`、`key_points` 注入 Prompt。
- 输出分数、优点、不足、改进建议。
- 强调评分稳定性和可解释性。

### 7. 面试报告模块

功能：

- 汇总岗位匹配、答题表现、知识短板。
- 生成 Markdown 或 JSON 报告。
- 给出复盘建议。

### 8. 工程化部署模块

功能：

- Docker Compose 启动 FastAPI、PostgreSQL、Redis、Celery。
- `.env.example` 管理配置。
- README 提供启动方式和接口示例。
- 测试覆盖核心模块。

## 分周落地方式

- Week 1：LLM CLI，为后续 LLM Client 打基础。
- Week 2：FastAPI 后端骨架，为主项目服务化打基础。
- Week 3：简历解析与岗位匹配 API。
- Week 4：面试题库 RAG v1。
- Week 5：岗位匹配驱动的 RAG 出题与评分上下文。
- Week 6：岗位匹配 Agent 与面试流程 Agent。
- Week 7：完成 AI-Interview 主业务闭环。
- Week 8：Docker、README、GitHub、Demo、简历话术、面试冲刺。

## 面试表达要点

面试时必须能讲清：

- 为什么选择“模拟面试”这个业务场景。
- RAG 在项目里解决了什么问题：题库检索、参考答案、关键评分点。
- Agent 在项目里解决了什么问题：岗位匹配、流程编排、工具调用。
- 工程化在哪里：FastAPI、数据库、Redis/Celery、Docker、README、测试。
- 项目如何从 Demo 变成可投递作品：业务闭环、可运行、可部署、可展示。


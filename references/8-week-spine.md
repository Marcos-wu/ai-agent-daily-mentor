# 8 周 AI Agent 实习冲刺主线

这是全局骨架，只负责保证长期方向不跑偏。每一周实际执行前，必须先生成一个中文每周学习大纲；每日学习内容不能只参考本文件，必须优先参考“当前周大纲”和用户每日反馈。

优先级：

1. 用户最新学习反馈。
2. 当前周中文学习大纲。
3. 本文件的 8 周主线。
4. 默认技术栈与导师经验。

## Phase 1：Week 1-2

目标：Python MUP、异步编程、FastAPI 后端基础。

### Week 1：Python MUP + HTTP + Git

本周核心产出物：`LLM CLI 调用工具`。

主线：

- Day 1：Python 工程环境与函数基础。
- Day 2：HTTP 与 API 调用。
- Day 3：大模型 API 最小调用。
- Day 4：异步实践，并发调用与耗时统计。
- Day 5：LLM CLI 工具搭建。
- Day 6：代码重构与 Debug。
- Day 7：测试与复盘。

### Week 2：FastAPI 后端骨架

本周核心产出物：`Agent 后端服务骨架`。

主线：

- FastAPI 项目结构。
- Pydantic 请求/响应模型。
- JWT 登录认证。
- Tortoise ORM 或 SQLAlchemy。
- CRUD、分页、统一响应。
- 日志、配置、基础测试。

## Phase 2：Week 3-5

目标：把 LLM API、结构化输出、RAG、检索优化接入 `AI-Interview` 主项目。

### Week 3：AI-Interview 简历解析与岗位匹配

核心产出物：`简历解析与岗位匹配 API`。

主线：

- LLM API Client 封装。
- Prompt 模板。
- JSON Schema / Pydantic 结构化输出。
- 流式输出。
- 错误重试与成本意识。
- 简历解析、JD 解析、岗位匹配初版。

### Week 4：面试题库 RAG v1

核心产出物：`面试题库 RAG 检索服务 v1`。

主线：

- 面试题库导入、切分、Embedding、入库、检索、生成。
- Chroma 本地向量库。
- LlamaIndex 与 LangChain 基础对比。
- 引用来源。
- 面向岗位和技能标签的题目筛选。

### Week 5：岗位匹配 + RAG 出题 v2

核心产出物：`岗位匹配驱动的面试出题与评分上下文服务`。

主线：

- 混合检索。
- 重排序。
- Query Rewrite。
- 多轮上下文。
- RAG 评估。
- Redis 缓存。
- 将 `reference_answer` 与 `key_points` 注入评分 Prompt，提升评分稳定性和可解释性。

## Phase 3：Week 6-7

目标：Agent 技能、Function Calling、LangGraph 工作流。

### Week 6：AI-Interview Agent 核心能力

核心产出物：`岗位匹配 Agent 与面试流程 Agent`。

主线：

- Tool Schema。
- Function Calling。
- ReAct。
- Memory。
- 工具调用日志。
- 简历读取、岗位模板匹配、专项面试启动工具。

### Week 7：AI-Interview 主项目闭环

核心产出物：`AI-Interview：基于 RAG 与 Agent 的智能模拟面试系统`。

主线：

- LangGraph 状态机。
- 条件路由。
- 多步骤工作流。
- 失败重试。
- 报告生成。
- 完成“简历解析 -> 岗位匹配 -> RAG 出题 -> AI 评分 -> 面试报告”闭环。

## Phase 4：Week 8

目标：工程化包装与上海/杭州实习面试冲刺。

核心产出物：`AI-Interview 可展示项目 + GitHub/演示链接 + 简历个人优势 + 面试题库`。

主线：

- Docker Compose 一键启动。
- README：架构、截图、启动方式、API 文档。
- `.env.example`。
- 核心逻辑测试。
- 简历项目话术。
- 个人优势对齐岗位要求。
- 面试四象限问答：Python 少量八股、AI 应用基础、AI 工程化、AI 项目。
- 面试问答演练。

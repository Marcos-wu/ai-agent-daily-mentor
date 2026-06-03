# 已上岸博主经验提炼：AI Agent 实习准备重点

本文件用于把已找到 Agent 应用开发实习的博主经验转化为 skill 的求职导向规则。生成 Week 6-8、项目规划、简历话术、个人优势和面试冲刺内容时必须参考。

## 个人优势写法规则

个人优势不是泛泛夸自己，而是根据岗位要求逐条对齐。

写法：

- 先观察大量岗位要求，总结通用能力。
- 每条优势对齐一个岗位要求。
- 用“能力 + 技术栈 + 可落地场景”表达。

推荐优势方向：

1. 具备 AI 应用落地能力，熟悉大模型 API 接入、Prompt Engineering、RAG 与 Agent 开发流程，能将 LLM 能力结合业务场景落地为实际系统。
2. 具备 Python 后端开发能力，熟悉 FastAPI/Django/Flask 等主流框架，能够完成接口设计、后端业务开发与系统联调。
3. 具备工程化能力，熟悉 Linux、Git、Docker、Nginx、Redis、Celery 等工具，能够完成 AI 应用从开发到部署的完整落地。
4. 学习能力强，善于借助 AI 高效学习并快速掌握新技术，并应用到项目开发中。
5. 熟练使用 Claude Code、OpenAI Codex、Cursor 等 AI 编程工具，能结合 AI 完成需求分析、代码开发、调试和重构。

## 面试考察四象限

AI 应用开发实习的面试通常来自四个方面：

- Python 八股：少量，重点是基础语法、异步、装饰器、异常、工程习惯。
- AI 应用基础知识：LLM API、Prompt、RAG、Agent、Embedding、Function Calling。
- AI 应用工程化能力：FastAPI、数据库、Redis、Celery、Docker、日志、部署。
- 你的 AI 应用项目：业务流程、技术选型、难点、优化、可展示程度。

判断：

- 大厂可能考算法。
- 中小厂通常更看技术栈和项目。
- 整体难度相当于 Python 后端面试基础上增加 AI 应用，因此项目表达很关键。

## 岗位画像

工作内容一般是“全栈 + AI”，工作方式偏 Vibe Coding。

技术要求通常不是纯 AI，也不是纯后端，而是：

- Python 后端。
- Python AI。
- AI 应用工程化。
- 能借助 AI 编程工具快速完成业务需求。

Demo 级项目不够。项目必须具备工程化，否则即使功能能跑，也很难说服面试官。

## 项目选择原则

不要只做单独 Agent 项目，也不要只做单独 RAG 项目。这样的项目太普通。

更好的项目是：

- 同时包含 RAG 和 Agent。
- 两者处在同一条业务链路中。
- 能形成完整闭环。
- 能说清楚业务价值和工程实现。

推荐业务闭环：

`简历解析 -> 岗位匹配 -> RAG 出题 -> AI 评分 -> 面试报告`

这个链路比“普通知识库问答”或“随便调工具的 Agent”更适合投递 AI 应用开发实习。

## 项目经历写法参考

项目名：

`AI-Interview：基于 RAG 与 Agent 的智能模拟面试系统`

项目简介：

面向求职场景设计的 AI 模拟面试系统，围绕“简历解析 -> 岗位匹配 -> RAG 出题 -> AI 评分 -> 面试报告”构建完整闭环。

技术实现要点：

- 基于 FastAPI + PostgreSQL + Redis + Celery 搭建后端，完成岗位匹配、面试流程、题库管理等核心服务。
- 接入 DeepSeek API 或 OpenAI-compatible API，实现简历解析、候选人画像提取、面试题生成、回答评分与面试报告输出。
- 基于 DashScope Embedding + PostgreSQL + pgvector 或 Chroma 实现题库 RAG，支持题目向量化、检索、筛选。
- 基于 LangChain Tool Calling Agent 实现岗位匹配 Agent，完成简历读取、画像构建、岗位模板匹配与专项面试启动流程。
- 在评分阶段将 `reference_answer` 与 `key_points` 注入 Prompt，提升 AI 评分稳定性与可解释性。
- 使用 Docker Compose 管理 PostgreSQL、Redis、FastAPI、Celery 等服务，完成本地多服务联调与部署。

投递建议：

- 简历中直接放 GitHub 链接。
- 如果有在线演示链接，面邀概率会明显提高。
- README 要写清楚项目背景、业务流程、技术架构、启动方式、接口示例、截图或演示。


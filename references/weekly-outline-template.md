# 每周学习大纲模板

生成每周大纲时必须使用中文，并按下面结构输出。不要生成英文版。

## 固定结构

~~~markdown
# 📅 Week N：本周主题

## 1. 核心技术拆解

### 技术点 A

具体说明：

- 学什么
- 为什么对 Agent 开发重要
- 本周用在哪里
- 常见错误认知
- 关联笔记：[[稳定笔记标题]]、[[另一个稳定笔记标题]]

## 2. 每日精细化学习路径

### Day 1：【类型】主题

关联知识：[[相关知识点 A]]、[[相关知识点 B]]

学习内容：

- ...

今天写什么：

1. ...

微练习：

```python
# 可运行或可临摹的核心代码
```

验收标准：

- ...

## 3. 本周核心产出物

### 项目名称

目录结构、核心功能、关键代码、简历话术、面试可讲亮点。

推荐建立的 Obsidian 笔记：

- [[项目总览]]
- [[核心模块设计]]
- [[面试表达]]

## 4. 面试仿真模拟

至少 4 个本周相关面试问答，必须覆盖本周项目实现和求职表达。

## 5. 避坑指南

列出本周最容易浪费时间或走偏的点，尤其提醒不要做无法投递的孤立 Demo。
~~~

## Week 1 标准样例：Python MUP + HTTP + Git

Week 1 的大纲必须参考以下内容生成。

### 固定主题

`Week 1：Python MUP + HTTP + Git`

### 核心技术拆解

Python MUP 只死磕：

- 函数：参数、返回值、默认参数、`*args`、`**kwargs`
- 类型注解：`str`、`int`、`list[str]`、`dict[str, Any]`、`Optional`
- 异常处理：`try / except / raise`
- 文件处理：`pathlib`、JSON 读写
- 面向对象：`class`、`__init__`、实例方法、组合
- 装饰器：理解 FastAPI 路由装饰器的基础
- 异步编程：`async def`、`await`、`asyncio.gather`
- 环境变量：`.env`、API Key 管理

关联笔记：[[Python MUP]]、[[Python 函数]]、[[Python 类型注解]]、[[异常处理]]、[[JSON 文件读写]]、[[环境变量与 API Key]]

HTTP 必须掌握：

- GET、POST、PUT/PATCH、DELETE
- 状态码：`200`、`201`、`400`、`401`、`403`、`404`、`422`、`500`
- Header：`Authorization`、`Content-Type`
- Body：JSON 请求体
- RESTful URL：`/api/v1/conversations/{id}/messages`

关联笔记：[[HTTP 请求结构]]、[[HTTP 状态码]]、[[RESTful API 设计]]、[[JSON API]]

Git 必须掌握：

- `git init`
- `git status`
- `git add`
- `git commit`
- `git log`
- `git diff`
- `.gitignore`
- 分支命名：`feature/week1-llm-cli`
- commit 格式：`feat: add async llm client`

关联笔记：[[Git 基础命令]]、[[Git 提交规范]]、[[.gitignore 配置]]

### Day 1：Python 工程环境与函数基础

关联知识：[[Python 虚拟环境]]、[[环境变量与 API Key]]、[[JSON 文件读写]]、[[pathlib 文件路径]]

学习内容：

- Python 虚拟环境
- `pip`
- `.env`
- 函数、类型注解、异常处理
- `pathlib`
- JSON 读写

今天写什么：

1. 创建项目目录：`week1_llm_cli`
2. 创建虚拟环境
3. 安装依赖：`httpx python-dotenv rich`
4. 写 `app/config.py` 读取 `.env`
5. 写 `app/history.py` 保存对话历史到 JSON

验收标准：

- 能读取 `.env`
- 能保存 JSON
- 能解释为什么 API Key 不能硬编码

### Day 2：HTTP 与 API 调用

关联知识：[[HTTP 请求结构]]、[[httpx 异步请求]]、[[API 超时处理]]、[[JSON API]]

学习内容：

- HTTP 请求结构
- Header / Body
- JSON API
- `httpx.Client` 和 `httpx.AsyncClient`
- API 超时处理

今天写什么：

1. 用 `httpx` 请求一个公开 API
2. 封装同步 API Client
3. 封装异步 API Client
4. 加入 timeout 和异常处理

验收标准：

- 能解释 GET / POST 区别
- 能解释 `response.raise_for_status()`
- 能处理网络异常

### Day 3：大模型 API 最小调用

关联知识：[[OpenAI-compatible API]]、[[LLM messages 结构]]、[[环境变量与 API Key]]、[[LLMClient 封装]]

学习内容：

- OpenAI-compatible API 格式
- `messages` 结构
- `system / user / assistant`
- API Key 从环境变量读取

今天写什么：

1. 封装 `LLMClient`
2. 支持 `chat(prompt: str) -> str`
3. 支持传入历史消息
4. 错误时打印清晰错误信息

验收标准：

- 能成功调用一个 LLM API
- 能换模型
- API Key 不出现在代码里

### Day 4：异步实践，并发调用与耗时统计

关联知识：[[Python 异步编程]]、[[asyncio.gather 并发]]、[[异步函数计时装饰器]]、[[LLM API 并发调用]]

学习内容：

- `asyncio.run`
- `asyncio.gather`
- 并发请求
- 装饰器统计耗时

今天写什么：

1. 同时发送 3 个问题给大模型
2. 对比串行和并发耗时
3. 写一个异步函数计时装饰器

验收标准：

- 能解释并发和并行区别
- 能解释为什么 LLM API 适合异步
- 能说出 `asyncio.gather` 的作用

### Day 5：LLM CLI 工具搭建

关联知识：[[命令行交互]]、[[Rich 终端输出]]、[[LLM CLI 项目结构]]、[[对话历史持久化]]

学习内容：

- 命令行交互
- Rich 美化输出
- 项目分层
- 错误提示

今天写什么：

1. `main.py` 提供交互式命令行
2. 用户输入问题
3. 调用 LLM
4. 输出回答
5. 保存历史

验收标准：

- 能连续对话
- 能保存历史
- 报错不崩溃

### Day 6：代码重构与 Debug

关联知识：[[Python 项目分层]]、[[自定义异常类]]、[[README 编写]]、[[.env.example 配置]]

学习内容：

- 模块拆分
- 依赖配置
- `.gitignore`
- README
- 错误分类

今天写什么：

1. 拆分目录
2. 增加 `.env.example`
3. 增加 README
4. 增加异常类
5. 每次请求记录耗时

验收标准：

- 项目不是单文件脚本
- 别人按 README 能运行
- 没有提交 `.env`

### Day 7：测试与复盘

关联知识：[[pytest 基础]]、[[Mock 测试思路]]、[[项目复盘]]、[[AI Agent 面试题]]

学习内容：

- pytest 基础
- mock 思路
- 项目复盘
- 面试表达整理

今天写什么：

1. 给历史记录模块写测试
2. 给配置读取写测试
3. 写本周总结
4. 整理 10 个面试问答
5. 打 tag 或 final commit

验收标准：

- 至少 3 个测试用例
- README 写清楚项目亮点
- Git 提交历史干净

### 本周核心产出物

项目：`LLM CLI 调用工具`

推荐目录结构：

```text
week1_llm_cli/
├── app/
│   ├── __init__.py
│   ├── config.py
│   ├── llm_client.py
│   ├── history.py
│   ├── timer.py
│   └── exceptions.py
├── tests/
│   ├── test_config.py
│   └── test_history.py
├── data/
│   └── .gitkeep
├── .env.example
├── .gitignore
├── README.md
├── requirements.txt
└── main.py
```

简历话术：

> 基于 Python 异步 HTTP 客户端封装 OpenAI-compatible 大模型调用工具，支持环境变量配置、历史对话持久化、异常处理与并发请求测试，为后续 Agent 服务开发提供可复用 LLM Client。

推荐建立的 Obsidian 笔记：

- [[LLM CLI 项目总览]]
- [[LLMClient 封装]]
- [[对话历史持久化]]
- [[Git 提交规范]]

## Week 3-8 项目导向规则

从 Week 3 开始，每周大纲必须围绕 `AI-Interview：基于 RAG 与 Agent 的智能模拟面试系统` 逐步展开。

生成 Week 3-8 大纲时必须遵守：

- 不生成孤立的“知识库问答系统”作为最终目标；RAG 必须服务于面试题库、岗位匹配或评分依据。
- 不生成孤立的“多工具 Agent Demo”作为最终目标；Agent 必须服务于简历读取、岗位匹配、面试流程或报告生成。
- `本周核心产出物` 必须写清楚它在 AI-Interview 业务链路中的位置。
- `面试仿真模拟` 必须加入至少 1 道“你这个项目为什么不是普通 Demo”的问题。
- `避坑指南` 必须提醒工程化要求：FastAPI 服务、数据库持久化、缓存/异步任务、Docker、README、测试或部署说明。
- 必须加入 `[[AI-Interview 项目总览]]`、`[[面试题库 RAG]]`、`[[岗位匹配 Agent]]`、`[[AI 评分 Prompt]]` 等稳定双链。

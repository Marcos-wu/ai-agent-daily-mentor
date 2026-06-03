# Day 1 标准：Python MUP 与工程环境

用于校准 `Phase 1 / Week 1 / Day 1` 的颗粒度。Day 1 必须对齐 Week 1 大纲中的 `week1_llm_cli` 项目，不要写成孤立的 Python 语法课。

## Day 1 核心定位

主题：Python 工程环境与函数基础。

目标：让用户搭好 `week1_llm_cli` 项目地基，并完成 `.env` 配置读取和 JSON 历史保存。

## 必须覆盖的核心点

### 1. 环境就是工程能力的一部分

- Python 版本、虚拟环境、依赖隔离、`.env` 都不是形式主义。
- Agent 应用会调用付费 API，配置错了就无法运行或无法复现。
- 新手坑：全局乱装包、硬编码 API Key、把 `.env` 提交到 Git。

### 2. Python MUP 是表达数据流

Agent 项目的基础数据流：

用户输入 -> 校验 -> 组织消息 -> 调用模型或工具 -> 保存历史 -> 返回结果。

Day 1 只死磕：

- 函数。
- 类型注解。
- 异常处理。
- `pathlib`。
- JSON 读写。
- `.env` 配置读取。

## Day 1 代码要求

优先围绕以下文件展开：

- `app/config.py`：读取 `.env` 中的 `LLM_API_KEY`、`LLM_BASE_URL`、`LLM_MODEL`。
- `app/history.py`：保存和读取 `data/history.json`。
- `main.py`：做最小命令行验证。

代码必须：

- 有 Type Hints。
- 有中文注释。
- 有异常处理。
- 不使用 `pass`。
- 不只给简化片段，要能让用户临摹并运行。

## Day 1 验收标准

用户完成后应该做到：

- 创建 `week1_llm_cli` 项目目录。
- 创建并激活虚拟环境。
- 安装 `httpx python-dotenv rich`。
- 能读取 `.env`。
- 能把用户消息保存到 `data/history.json`。
- 能解释为什么 API Key 不能硬编码。
- 完成一次 Git commit。


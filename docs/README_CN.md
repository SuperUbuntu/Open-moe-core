# Moe Core

Moe Core 是一个面向可发布核心发行版的 LLM 对话智能体引擎。仓库保留核心运行时、记忆、提示词、插件运行时、WebUI 宿主和消息网关基础能力，平台适配器应在核心仓库外独立维护。

本项目可以通过外部适配器接入 Telegram、本地 WebUI 聊天或其他平台。OpenClaw Moe Core 是基于 MaiBot 的社区衍生项目，不声明为 MaiBot 官方发行版。

## 核心范围

- 对话运行时与 heartflow 处理
- Prompt、国际化、模型客户端与运行配置
- 插件宿主与运行时 API
- 本地 WebUI 宿主 API 与静态资源挂载
- 核心引擎使用的记忆、表情、统计和数据服务

Moe Core 默认不捆绑 QQ、NapCat 或 OneBot 部署。平台适配器应独立安装、配置和发布。

## 快速开始

```bash
uv sync
uv run python bot.py
```

本地 CLI 对话：

```bash
uv run python saka.py
```

请将部署凭据和适配器配置保存在版本控制之外。

## 许可证与来源

Moe Core 派生自 MaiBot，并继续使用 GPL-3.0 协议发布。本仓库保留来源说明，不隐藏上游历史。详情见 [NOTICE](../NOTICE) 与 [LICENSE](../LICENSE)。

# Moe Core

Moe Core is a GPL-3.0 core engine for LLM-driven conversational agents. It keeps the runtime, memory, prompt, plugin, WebUI host, and message gateway foundations in this repository, while platform adapters should live outside the core distribution.

OpenClaw Moe Core is maintained as a community derivative of MaiBot. It is not presented as an official MaiBot release.

## Scope

- Conversational runtime and heartflow processing
- Prompt loading, i18n, model clients, and runtime configuration
- Plugin host/runtime APIs
- Local WebUI host API and static asset mounting
- Memory, emoji, statistics, and data services used by the core engine

Moe Core does not bundle QQ, NapCat, or OneBot deployment as the default distribution target.

## Quick Start

```bash
uv sync
uv run python bot.py
```

Local CLI chat:

```bash
uv run python saka.py
```

Keep deployment credentials and adapter configuration outside version control.

## License And Provenance

Moe Core is derived from MaiBot and remains GPL-3.0. See [NOTICE](../NOTICE) and [LICENSE](../LICENSE).

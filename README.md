# Moe Core

<p align="center">
  <img src="docs/assets/moemoe-promo.jpg" alt="Moe Core Promo" width="720" />
</p>

Moe Core is a GPL-3.0 core engine for LLM-driven conversational agents. It keeps the runtime, memory, prompt, plugin, WebUI host, and message gateway foundations in this repository, while platform adapters are expected to live outside the core distribution.

This project can be paired with external adapters for Telegram, local WebUI chat, or other messaging platforms through the plugin runtime and message gateway APIs. OpenClaw Moe Core is maintained as a community derivative of the original Mcore codebase; it is not presented as an official Mcore release.

## Core Scope

- Core conversational runtime and heartflow processing
- Prompt loading, i18n, model client integration, and runtime configuration
- Plugin host/runtime APIs for external capabilities
- Local WebUI host API and static asset mounting
- Memory, emoji, statistics, and data services used by the core engine

Moe Core does not bundle a QQ, NapCat, or OneBot deployment as the default distribution target. Platform-specific adapters should be installed, configured, and released separately.

## Quick Start

Install dependencies with `uv`:

```bash
uv sync
```

Run the core service:

```bash
uv run python bot.py
```

Run the local CLI conversation loop:

```bash
uv run python saka.py
```

Configuration is generated from the project's Python config schema on first run. Keep deployment-specific credentials and adapter settings outside version control.

## External Adapters

Moe Core is intended to be adapter-neutral. A platform adapter should translate a platform's incoming events into the core message gateway format and implement outgoing send capabilities through the plugin/runtime API.

Suitable adapter targets include:

- Telegram
- Matrix or Discord-style community bridges
- Custom local tools or service integrations
- Legacy platform adapters maintained outside this repository

The repository may still contain historical compatibility names in internal Python classes, database filenames, or SDK symbols where renaming would create unnecessary migration risk. User-facing docs and default project identity should refer to Moe Core.

## License And Provenance

Moe Core is derived from MaiBot and remains licensed under GPL-3.0. This repository does not hide that provenance. See [NOTICE](NOTICE) and [LICENSE](LICENSE) for details.

Some dependency, SDK, and compatibility names still include `maibot` because they are part of the existing public interfaces or upstream package names. Those names do not imply that this repository is an official MaiBot release.

## Development

Run a lightweight test subset:

```bash
uv run pytest pytests/test_plugin_runtime_api.py pytests/i18n_test/test_i18n.py
```

Search for platform-specific coupling before releases:

```bash
rg -n "NapCat|OneBot|QQ|MaiBot|MaiSaka|麦麦" README.md docs locales src plugins prompts pyproject.toml
```

## Release Notes

See [RELEASE_NOTES.md](RELEASE_NOTES.md) for the Moe Core refactor summary.

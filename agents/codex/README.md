# Codex

## Overview

**Codex** is OpenAI's CLI coding agent. It runs in a containerized sandbox (Docker) and can execute multi-step coding tasks autonomously.

## Key Details

| Detail | Value |
|--------|-------|
| Developer | OpenAI |
| Command | `codex` |
| Config location | `~/.codex/config.toml` (TODO: verify) or project `codex.config.toml` |
| Model | OpenAI models (o1, o3-mini, etc.) |
| Sandbox | Docker container |
| Open source | No (CLI is open-source, see [github.com/openai/codex](https://github.com/openai/codex)) |
| Approval modes | `--auto` (autonomous), default (confirm each step) |

## FARTBULL Material That Applies

- [Universal concepts](../../docs/concepts/)
- [Coding workflows](../../docs/workflows/coding-workflows.md)
- [Safety principles](../../docs/concepts/safety.md)
- [Tool usage](../../docs/tools/tool-usage.md) — Codex has its own tool use in sandbox
- [Debugging workflows](../../docs/workflows/debugging.md)
- [Research workflows](../../docs/workflows/research.md)

## Agent-Specific Documentation

- [Setup](setup/README.md)
- [Configuration](config/README.md)
- [Prompts](prompts/README.md)
- [Workflows](workflows/README.md)
- [Examples](examples/README.md)
- [Reference](reference/README.md)

## Brand

FARTBULL — [fartbull.xyz](https://fartbull.xyz) · [@Fartbullssol](https://x.com/Fartbullssol)

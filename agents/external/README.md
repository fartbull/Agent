# External

## Overview

**External** is a template category for documenting AI coding agents not natively listed in this knowledge base. Use this as a reference for adding support for any third-party AI assistant or coding tool.

## Key Details

| Detail | Value |
|--------|-------|
| Type | Template / placeholder |
| Purpose | Document any external agent |
| Use | Copy this structure for new agents |
| Open source | Varies per agent |

## FARTBULL Material That Applies

- [Universal concepts](../../docs/concepts/)
- [Agent template](../../templates/agent/README.md) — for adding new agents

## Agent-Specific Documentation

- [Setup](setup/README.md)
- [Configuration](config/README.md)
- [Prompts](prompts/README.md)
- [Workflows](workflows/README.md)
- [Examples](examples/README.md)
- [Reference](reference/README.md)

## Adding a New External Agent

1. Copy the `templates/agent/README.md` structure
2. Create `agents/<name>/` with 6 subdirectories: `setup/`, `config/`, `prompts/`, `workflows/`, `examples/`, `reference/`
3. Fill in each `README.md` with specific details
4. Use `TODO: Verify` markers for undocumented features
5. Add the agent to `docs/agents.md`

## Brand

FARTBULL — [fartbull.xyz](https://fartbull.xyz) · [@Fartbullssol](https://x.com/Fartbullssol)

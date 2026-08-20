# Agent Folder Template

This is the template for adding a new agent to the FARTBULL repo.

## Structure

```text
agents/<agent-name>/
├── README.md          ← Agent overview, key facts, what applies
├── setup/
│   └── README.md      ← Installation, auth, initial configuration
├── config/
│   ├── README.md       ← Config format, key settings, examples
│   └── example.yaml    ← Example config (if applicable)
├── prompts/
│   └── README.md       ← Agent-specific prompt patterns
├── workflows/
│   └── README.md       ← Common workflow recipes
├── examples/
│   └── README.md       ← Working examples
└── reference/
    └── README.md       ← Official docs links, API references
```

## README.md Template (agents/<agent>/README.md)

```markdown
# <Agent Name>

## Overview

One-paragraph description of the agent.

## Key Details

| Detail | Value |
|--------|-------|
| Developer | [company] |
| Command | `agent-command` |
| Config location | `~/.agent/` or `.agentrc` |
| Model | [model or provider] |
| Open source | Yes/No |

## FARTBULL Material That Applies

- [Universal concepts](../../docs/concepts/)
- [Universal workflows](../../docs/workflows/)
- [Universal prompts](../../docs/prompts/)
- [Tool usage](../../docs/tools/tool-usage.md)
- [Safety principles](../../docs/concepts/safety.md)

## What Does NOT Apply

- [Any universal docs that don't apply to this agent]

## Agent-Specific Documentation

- [Setup](setup/README.md)
- [Configuration](config/README.md)
- [Prompts](prompts/README.md)
- [Workflows](workflows/README.md)
- [Examples](examples/README.md)
- [Reference](reference/README.md)
```

## Setup README Template (agents/<agent>/setup/README.md)

```markdown
# <Agent Name> Setup

## Installation

```bash
{install commands}
```

## Authentication

{auth requirements}

## Verification

```bash
{verification command}
```
```

## Config README Template (agents/<agent>/config/README.md)

```markdown
# <Agent Name> Configuration

## Config Location

{where config files live}

## Config Format

{yaml/json/toml/ini — with example}

## Key Settings

| Setting | Default | Description |
|---------|---------|-------------|
| {key} | {default} | {description} |

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| {VAR} | {yes/no} | {description} |
```

## Adding Your Agent

1. Copy this template to `agents/<your-agent>/`
2. Fill in each file
3. Use `TODO` markers for unknowns
4. Update `docs/agents.md` (support matrix)
5. Update `TODO.md` if incomplete

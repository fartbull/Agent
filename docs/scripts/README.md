# Agent Scripts

FARTBULL provides shell scripts for agent setup, management, and automation.

## Overview

Scripts live in the `scripts/` directory and cover:
- Environment setup
- Agent installation
- Skill/plugin installation
- Project scaffolding
- Maintenance tasks

## Core Scripts

| Script | Purpose |
|--------|---------|
| `setup-agent.sh` | Install and configure an agent |
| `install-skill.sh` | Download and install a skill |
| `install-plugin.sh` | Download and install a plugin |
| `setup-gateway.sh` | Configure API gateway (TODO: verify) |
| `create-skill.sh` | Scaffold a custom skill |

TODO: Verify exact script names and functions.

## setup-agent.sh

```bash
# Install a specific agent
./scripts/setup-agent.sh --agent codex --model claude-3-5-sonnet

# Auto-detect
./scripts/setup-agent.sh --auto
```

## install-skill.sh

```bash
# Install a single skill
./scripts/install-skill.sh dexscreener

# Install multiple skills
./scripts/install-skill.sh dexscreener query-token-info trading-signal

# Install all skills for a domain
./scripts/install-skill.sh --domain binance
```

## Security Note

All scripts use `set -euo pipefail` for safety. TODO: Verify all scripts pass `shellcheck`.

## See Also

- [Skills System](skills/README.md)
- [Plugins System](plugins/README.md)
- [Configuration System](../../configs/)

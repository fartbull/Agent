# Configuration System

How configuration works in the FARTBULL universal agent repo.

## Architecture

```
configs/
├── shared/          ← Universal config patterns (apply to all agents)
└── agents/          ← Agent-specific config overrides
```

Plus agent folders: `agents/<agent>/config/` — the canonical home for each agent's config docs and examples.

## Shared Configuration

Files in `configs/shared/` apply to every agent:

| File | Purpose |
|------|---------|
| `base.yaml` | Universal agent settings (model defaults, timeout, git integration) |
| `safety.yaml` | Safety rules, confirmation gates, rate limits, restricted platforms |

## Agent-Specific Configuration

Agent-specific configs live in two places:

1. **`configs/agents/<agent>.yaml`** — reusable config overrides (machine-readable)
2. **`agents/<agent>/config/`** — documentation + examples (human-readable)

## Configuration Pattern

Each agent should document:

| Element | Description |
|---------|-------------|
| **Config file** | Where the agent reads config from |
| **Config format** | YAML, JSON, TOML, INI |
| **Key settings** | Model, provider, tools, approvals |
| **Environment variables** | Any required env vars |
| **Example config** | A working example file |

## Using Configs

```bash
# Copy shared base config
cp configs/shared/base.yaml .agent-config.yaml

# Override with agent-specific
cp configs/agents/codex.yaml .cursorrules  # adapt format as needed

# Or place in the agent's expected location
cp configs/agents/aider.yaml .aider.conf  # adapt format as needed
```

## See Also

- [Agent configs](../../agents/)
- [Templates](../templates/config/)
- [Universal prompts](../docs/prompts/universal-prompts.md)

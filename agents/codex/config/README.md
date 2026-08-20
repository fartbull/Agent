# Codex Configuration

## Config Location

- **Global:** `~/.codex/config.toml` (TODO: verify)
- **Project-level:** `codex.config.toml` in project root (TODO: verify)

## Config Format

TODO: Verify exact TOML schema. Based on available info:

```toml
# ~/.codex/config.toml
model = "o3-mini"  # or "o1"
approval_mode = "auto"  # or "confirm"
sandbox_mode = "docker"  # or "none"

[env]
OPENAI_API_KEY = "..."
```

## Key Settings

| Setting | Default | Description |
|---------|---------|-------------|
| `model` | `o3-mini` | Model to use |
| `approval_mode` | `confirm` | `auto` or `confirm` |
| `sandbox_mode` | `docker` | `docker` or `none` |

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `OPENAI_API_KEY` | Yes | OpenAI API key |

## CLI Flags

| Flag | Description |
|------|-------------|
| `-p` / `--prompt` | Run with a single prompt |
| `--auto` | Autonomous mode (no confirmation) |
| `--model` | Override model |
| `--help` | Show all flags |

## See Also

- [Configuration system](../../configs/README.md)
- [Shared config](../../configs/shared/base.yaml)

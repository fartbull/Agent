# Aider Configuration

## Config Locations

| File | Scope | Purpose |
|------|-------|---------|
| `.aider.conf` | Project | Project-specific settings |
| `~/.config/aider.conf` | Global | TODO: Verify — user-wide defaults |
| `.aiderignore` | Project | Files to exclude from context |
| `.aider.model.settings` | Project | Model-specific settings (committed) |

## .aider.conf (Project-level)

```ini
# Example .aider.conf
model = claude-3-5-sonnet-20241022
# dark_mode = true
# pretty = true
# git_commit_verify = false

# Auto-reload on file changes
auto_reload = true

# Warn before running shell commands
warn_dangerous = true
```

## .aiderignore

```
# Like .gitignore but for aider
node_modules/
*.log
.env
dist/
```

## .aider.model.settings (Committed)

```json
{
  "model": {
    "name": "claude-3-5-sonnet-20241022",
    "api_key_name": null
  },
  "dark_mode": false
}
```

TODO: Verify exact format of `.aider.model.settings`

## CLI Flags

| Flag | Description |
|------|-------------|
| `--model` | Set the model (e.g., `claude-3-5-sonnet-20241022`) |
| `--no-git` | Run without git integration |
| `--no-approximate` | Disable approximate responses |
| `--dry-run` | Show what would change without editing |
| `--help` | Show all options |

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `ANTHROPIC_API_KEY` | If using Anthropic | Claude API key |
| `OPENAI_API_KEY` | If using OpenAI | GPT API key |
| `GOOGLE_API_KEY` | If using Google | Gemini API key |

## See Also

- [Configuration system](../../configs/README.md)
- [Shared config](../../configs/shared/base.yaml)

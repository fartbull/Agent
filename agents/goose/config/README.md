# Goose Configuration

## Config Location

- **Global:** `~/.config/goose/config.yaml` (TODO: verify path)
- **Project:** Project config can override global settings

## Config Format

TODO: Verify exact YAML schema. Based on Goose's open-source docs:

```yaml
# ~/.config/goose/config.yaml
model:
  provider: anthropic
  name: claude-3-5-sonnet-20241022
  temperature: 0.7

extensions:
  - name: shell
    type: builtin
  - name: filesystem
    type: builtin
  - name: websearch
    type: builtin
    provider: brave
    api_key: $BRAVE_API_KEY

timeout_minutes: 15
max_turns: 50
```

## Key Settings

| Setting | Default | Description |
|---------|---------|-------------|
| `model.provider` | `anthropic` | LLM provider |
| `model.name` | `claude-3-5-sonnet` | Model name |
| `model.temperature` | 0.7 | Creativity/consistency |
| `extensions` | built-in tools | MCP and builtin extensions |
| `timeout_minutes` | 15 | Max task duration |

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `ANTHROPIC_API_KEY` | If using Anthropic | Claude API key |
| `OPENAI_API_KEY` | If using OpenAI | GPT API key |
| `GOOGLE_API_KEY` | If using Google | Gemini API key |

## Extensions

Goose supports extensions for adding tools:

| Extension | Type | Purpose |
|-----------|------|---------|
| `shell` | builtin | Execute bash commands |
| `filesystem` | builtin | Read/write files |
| `websearch` | builtin | Search the web |
| `developer` | builtin | Custom instructions |

TODO: Verify full extension list and configuration schema

## See Also

- [Configuration system](../../configs/README.md)
- [Shared config](../../configs/shared/base.yaml)

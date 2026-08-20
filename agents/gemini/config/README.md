# Gemini Configuration

## Config Location

- **Global:** `~/.gemini/` or `~/.config/gemini/` (TODO: verify)
- **Project:** `.gemini/` (TODO: verify)

## Config Format

TODO: Verify config format. Placeholder structure:

```yaml
# .gemini/config.yaml
model: gemini-2.5-pro
sandbox: true
```

## Key Settings

| Setting | Default | Description |
|---------|---------|-------------|
| `model` | `gemini-2.5-pro` | Model to use |
| `sandbox` | `true` | Run in sandbox |

TODO: Verify all settings

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `GOOGLE_API_KEY` | Yes | Google AI API key |

## See Also

- [Configuration system](../../configs/README.md)
- [Shared config](../../configs/shared/base.yaml)

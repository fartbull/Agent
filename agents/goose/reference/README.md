# Goose Reference

## Official Links

| Resource | URL |
|----------|-----|
| GitHub | [github.com/block/goose](https://github.com/block/goose) |
| Docs | TODO: Verify documentation URL |
| Releases | [github.com/block/goose/releases](https://github.com/block/goose/releases) |
| X (Block) | [@block](https://x.com/block) |

## Supported Models

Goose supports any model via provider plugins. Common providers:

| Provider | Models | Notes |
|----------|--------|-------|
| Anthropic | Claude 3.5/4 | Recommended |
| OpenAI | GPT-4, o3-mini | |
| Google | Gemini 2.5 | |
| Ollama | Any local model | For local/offline use |

TODO: Verify complete provider list

## Built-in Extensions

- `shell` — execute bash commands
- `filesystem` — read/write files
- `websearch` — search the web (requires Brave API key)
- `developer` — custom instructions

## Notes

- Goose is open source, developed by Block
- Config is YAML-based at `~/.config/goose/config.yaml` (TODO: verify)
- Extensions can be Python scripts that add MCP tools
- Docker mode is recommended for isolation
- Supports both interactive and non-interactive modes

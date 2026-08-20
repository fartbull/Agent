# Cursor Reference

## Official Links

| Resource | URL |
|----------|-----|
| Website | [cursor.sh](https://cursor.sh) |
| Download | [cursor.sh/download](https://cursor.sh/download) |
| Docs | TODO: Verify documentation URL |
| Changelog | [cursor.sh/changelog](https://cursor.sh/changelog) |

## Supported Models

| Provider | Models |
|----------|--------|
| Anthropic | Claude 3.5/4 Sonnet, Opus |
| OpenAI | GPT-4o, o1, o3-mini |
| GitHub | Copilot models |
| Custom | Any OpenAI-compatible endpoint |

TODO: Verify exact model selection options

## Key Features

- `.cursor/rules/*.md` — project-specific agent instructions
- `.cursorrules` — legacy single-file rules
- MCP server support
- Inline editing with Cmd/Ctrl + K
- Agent chat mode
- CLI mode (`cursor --cli`)
- Multi-file project context

## Notes

- `.cursor/rules/` is the current format; `.cursorrules` is deprecated
- Rules can match by file path pattern (TODO: verify exact mechanism)
- MCP support allows extending tools via `mcp.json` config
- CLI mode uses the same model configuration as the GUI

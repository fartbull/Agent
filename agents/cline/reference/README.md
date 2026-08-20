# Cline Reference

## Official Links

| Resource | URL |
|----------|-----|
| GitHub | [github.com/cline/cline](https://github.com/cline/cline) |
| VS Code | [marketplace.visualstudio.com/items...](https://marketplace.visualstudio.com/items) (TODO: verify exact URL) |
| Docs | TODO: Verify documentation URL |
| X | [@clinedotfun](https://x.com/clinedotfun) |

## Supported Models

| Provider | Models |
|----------|--------|
| Anthropic | Claude 3.5/3.7 Sonnet |
| OpenAI | GPT-4o, o1, o3-mini |
| Google | Gemini 2.5 Pro/Flash |
| Ollama | Any local model |
| DeepSeek | TODO: verify |
| Bedrock | TODO: verify |
| OpenRouter | TODO: verify |

TODO: Verify complete model list

## Modes

| Mode | Behavior |
|------|----------|
| **Ask** | Proposes actions, waits for approval |
| **Act** | Executes autonomously |

## MCP Support

Cline supports MCP servers for extending tool access.

TODO: Verify MCP configuration format and location

## Key Files

| File | Purpose |
|------|---------|
| `.clinerules` | Project-specific instructions |
| `.cline/settings.json` | Permissions and settings |

## Notes

- Cline is open source, forked from itself
- `.clinerules` is automatically loaded on startup
- Act mode requires explicit opt-in for security
- Settings can be configured per-workspace or per-user

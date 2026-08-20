# Roo Reference

## Official Links

| Resource | URL |
|----------|-----|
| GitHub | [github.com/roo-code/roo-code](https://github.com/roo-code/roo-code) |
| VS Code | [marketplace.visualstudio.com/items?itemName=RooCode.roo-code](https://marketplace.visualstudio.com/items?itemName=RooCode.roo-code) |
| Docs | TODO: Verify documentation URL |
| X | [@RooCodeAI](https://x.com/RooCodeAI) |

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

## Modes

| Mode | Behavior |
|------|----------|
| **Chat** | Conversational, no file edits |
| **Code** | Full autonomous coding agent |
| **Debug** | Investigation and debugging |
| **Ask** | Q&A, can also edit files |

## MCP Support

Roo supports MCP servers for extending tool access.

TODO: Verify MCP configuration format and location

## Key Files

| File | Purpose |
|------|---------|
| `.roo/rules/*.md` | Per-mode instructions |
| `.roo/settings.json` | Permissions, settings |

## Notes

- Roo is an open-source fork of Cline
- Rule files in `.roo/rules/` can be mode-specific
- MCP support is built-in (like Cline)
- Four distinct modes for different workflows
- Auto-approval can be enabled for faster execution

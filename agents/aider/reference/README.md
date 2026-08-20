# Aider Reference

## Official Links

| Resource | URL |
|----------|-----|
| GitHub | [github.com/paul-gauthier/aider](https://github.com/paul-gauthier/aider) |
| Docs | [aider.chat](https://aider.chat) |
| Install | `pip install aider-chat` |

## Supported Models

Aider works with any LLM that has a compatible API:

| Provider | Default Model | Notes |
|----------|--------------|-------|
| Anthropic | `claude-3-5-sonnet-20241022` | Best quality |
| OpenAI | `gpt-4o` | Fast, reliable |
| Google | `gemini-2.5-flash` | TODO: verify exact name |
| Ollama | Local models | No API key needed |
| GitHub Models | Various | TODO: verify |

## Slash Commands

| Command | Description |
|---------|-------------|
| `/add <files>` | Add files to context window |
| `/drop <files>` | Remove files from context |
| `/ask <question>` | Ask without editing files |
| `/run <command>` | Run shell command |
| `/model <name>` | Switch model |
| `/exit` | Quit |

## Key Files

| File | Purpose |
|------|---------|
| `.aider.conf` | Project config (INI format) |
| `.aiderignore` | Files to exclude |
| `.aider.model.settings` | Committed model settings |
| `.gitignore` | Should include `.aider.model.settings` (local overrides) |

## Notes

- Aider uses git for undo/redo — always commit first
- `.aider.model.settings` is designed to be committed; `.aider.conf` local overrides should be gitignored
- `--no-approximate` gives stricter, more precise responses
- Best results with Claude 3.5 Sonnet or GPT-4o

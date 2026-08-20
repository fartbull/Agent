# Agent Support Matrix

| Agent | Category | Setup | Config | Prompts | Workflows | Examples | Notes |
|-------|----------|-------|--------|---------|-----------|----------|-------|
| [Pi](agents/pi/) | Conversational | ✅ | ✅ | ✅ | ✅ | ✅ | See [pi.md](agents/pi/README.md) |
| [Codex](agents/codex/) | Coding CLI | ✅ | ✅ | ✅ | ✅ | ✅ | OpenAI Codex CLI |
| [Claude Code](agents/claude/) | Coding agent | ✅ | ✅ | ✅ | ✅ | ✅ | Anthropic coding agent |
| [Gemini CLI](agents/gemini/) | Coding CLI | 🚧 | 🚧 | 🚧 | 🚧 | 🚧 | Needs verification |
| [OpenCode](agents/opencode/) | Coding CLI | ❓ | ❓ | ❓ | ❓ | ❓ | Agent identity needs verification |
| [Cursor](agents/cursor/) | IDE agent | ✅ | ✅ | ✅ | ✅ | ✅ | Cursor built-in agent |
| [Aider](agents/aider/) | Coding CLI | ✅ | ✅ | ✅ | ✅ | ✅ | AI pair programming |
| [Cline](agents/cline/) | VS Code ext | ✅ | ✅ | ✅ | ✅ | ✅ | Cline extension |
| [Roo Code](agents/roo/) | VS Code ext | ✅ | ✅ | ✅ | ✅ | ✅ | Fork of Cline |
| [Goose](agents/goose/) | Coding CLI | ✅ | ✅ | ✅ | ✅ | ✅ | From Block, open source |
| [Copilot](agents/copilot/) | IDE agent | ✅ | ✅ | ✅ | ✅ | ✅ | GitHub Copilot |
| [External](agents/external/) | Template | ✅ | ✅ | ✅ | ✅ | ✅ | Integration guide |

Legend:
- ✅ Supported — documented and verified
- 🚧 In progress — partially documented, needs verification
- ❓ Unknown — existence or details need investigation

## How to Read This Matrix

Each cell links to the agent's folder where you'll find:
- Setup instructions
- Configuration files and examples
- Agent-tailored prompt libraries
- Workflow recipes
- Working examples
- Reference links

## Adding a New Agent

See [AGENTS.md](../AGENTS.md) → "Adding New Agent" and use the [agent template](../../templates/agent/).

## Quick Reference: Which Agent to Use

| Use Case | Recommended Agents |
|----------|-------------------|
| Terminal coding | Codex, Claude Code, OpenCode, Aider, Goose |
| IDE-based coding | Cursor, Cline, Roo, Copilot |
| Conversational | Pi |
| Custom/internal | External |

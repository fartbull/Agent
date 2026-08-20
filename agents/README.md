# Agent Index

This directory contains documentation for 12 AI coding agents supported by the FARTBULL universal agent knowledge base.

## Supported Agents

| Agent | Developer | Type | Open Source |
|-------|-----------|------|-------------|
| [Pi](pi/) | Inflection AI | Conversational | No |
| [Codex](codex/) | OpenAI | CLI coding | No |
| [Claude Code](claude/) | Anthropic | CLI coding | No |
| [Gemini](gemini/) | Google | CLI coding | No |
| [OpenCode](opencode/) | Community (TODO) | Coding CLI | Yes (TODO) |
| [Cursor](cursor/) | Cursor | IDE agent | No |
| [Aider](aider/) | Paul Gauthier | CLI pair programming | Yes |
| [Cline](cline/) | Cline | VS Code extension | Yes |
| [Roo](roo/) | Roo Code | VS Code extension | Yes |
| [Goose](goose/) | Block | CLI coding | Yes |
| [Copilot](copilot/) | GitHub | IDE agent | No |
| [External](external/) | Any | Custom/template | Varies |

## Each Agent Folder Contains

| Subdir | Purpose |
|--------|---------|
| `README.md` | Overview and links to subdocs |
| `setup/` | Installation and authentication |
| `config/` | Configuration files and examples |
| `prompts/` | Prompt patterns and best practices |
| `workflows/` | Usage workflows and patterns |
| `examples/` | Concrete usage examples |
| `reference/` | Official links and reference |

## Configuration

Agent-specific config overrides live in [`configs/agents/`](../configs/agents/).

## Universal Docs

See [`docs/`](../docs/) for universal concepts, workflows, and tool guides.

## Brand

FARTBULL — [fartbull.xyz](https://fartbull.xyz) · [@Fartbullssol](https://x.com/Fartbullssol)

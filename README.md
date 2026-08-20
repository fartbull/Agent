# FARTBULL Agent

> Universal agent setup, configuration, documentation, and knowledge base.

FARTBULL is an experimental, agent-agnostic knowledge repository for AI agents and the humans who build with them.

Built and maintained by **[FARTBULL](https://fartbull.xyz)**.

---

## What

A single source of truth for:

- **Universal agent concepts** — prompting, memory, task decomposition, safety
- **Agent-specific setup** — install, config, and workflow guides for 12+ agents
- **Reusable configurations** — shared config templates and agent-specific overrides
- **Prompt libraries** — universal and agent-tailored prompts
- **Workflow recipes** — coding, research, debugging, autonomous operation
- **Integration guides** — external tools, APIs, and services (X API, Docker, Solana, MCP)
- **Skills system** — composable agent capabilities (trading, DeFi, Solana, social)
- **Plugin system** — extend agents with custom MCP servers and tools
- **TypeScript SDK** — programmatic agent automation
- **Agent scripts** — setup, installation, and management automation

## Why

Every AI agent framework ships its own docs in its own format, with its own assumptions. Moving between agents means re-learning config patterns, command syntax, and best practices. This repo collapses that friction.

One knowledge base. Many agents.

## Supported Agents

| Agent            | Setup | Config | Prompts | Workflows | Examples |
| ---------------- | :---: | :----: | :-----: | :-------: | :------: |
| [Pi](agents/pi/) |   ✅  |   ✅   |   ✅    |    ✅     |    ✅    |
| [Codex](agents/codex/) |  ✅  |   ✅   |   ✅    |    ✅     |    ✅    |
| [Claude Code](agents/claude/) | ✅ | ✅ | ✅ | ✅ | ✅ |
| [Gemini CLI](agents/gemini/) |  🚧  |   🚧   |   🚧    |    🚧     |    🚧    |
| [OpenCode](agents/opencode/) |  ❓  |   ❓   |   ❓    |    ❓     |    ❓    |
| [Cursor](agents/cursor/) |   ✅  |   ✅   |   ✅    |    ✅     |    ✅    |
| [Aider](agents/aider/) |   ✅  |   ✅   |   ✅    |    ✅     |    ✅    |
| [Cline](agents/cline/) |   ✅  |   ✅   |   ✅    |    ✅     |    ✅    |
| [Roo Code](agents/roo/) |  ✅  |   ✅   |   ✅    |    ✅     |    ✅    |
| [Goose](agents/goose/) |   ✅  |   ✅   |   ✅    |    ✅     |    ✅    |
| [Copilot](agents/copilot/) |   ✅  |   ✅   |   ✅    |    ✅     |    ✅    |
| [External](agents/external/) | ✅ | ✅ | ✅ | ✅ | ✅ |

Legend: ✅ Supported · 🚧 In progress · ❓ Needs verification

Full matrix: [docs/agents.md](docs/agents.md)

## Start Here

- [Universal Agent Docs](docs/concepts/principles.md) — core concepts
- [Agent Support Matrix](docs/agents.md) — what's covered per agent
- [Configuration System](configs/README.md) — how config works here
- [Skills Catalog](docs/skills/) — all available agent skills
- [Templates](templates/) — add a new agent in minutes
- [TODO.md](TODO.md) — roadmap and what's unfinished

## Using FARTBULL with your agent

```
agents/pi/         → Pi-specific setup, config, prompts
agents/codex/      → Codex-specific setup, config, prompts
agents/claude/     → Claude Code-specific setup, config, prompts
agents/cursor/     → Cursor-specific setup, config, prompts
agents/aider/      → Aider-specific setup, config, prompts
agents/cline/      → Cline-specific setup, config, prompts
agents/roo/        → Roo Code-specific setup, config, prompts
agents/goose/      → Goose-specific setup, config, prompts
agents/gemini/     → Gemini CLI-specific setup, config, prompts
agents/opencode/   → OpenCode-specific setup, config, prompts
agents/copilot/    → Copilot-specific setup, config, prompts
agents/external/   → Custom/external agent integration guide
```

## Repository Architecture

```text
/
├── README.md              ← You are here
├── AGENTS.md              ← Instructions for AI agents in this repo
├── TODO.md                ← Roadmap and unfinished work
├── CHANGELOG.md           ← Version history
├── CONTRIBUTING.md        ← How to contribute
├── LICENSE.md             ← License (see note below)
│
├── docs/                  ← Universal documentation (shared by all agents)
│   ├── concepts/          ← Agent principles, prompting, memory
│   ├── workflows/         ← Coding, research, debugging, autonomous
│   ├── prompts/           ← Universal prompt library
│   ├── memory/            ← Memory strategies
│   ├── context/           ← Context packing strategies
│   ├── tools/             ← Tool usage guides
│   ├── integrations/      ← External service integration guides (X API, Docker)
│   ├── skills/            ← Composable agent capabilities catalog
│   ├── plugins/           ← Plugin system for extending agents
│   ├── sdk/               ← TypeScript SDK reference
│   ├── scripts/           ← Setup and management scripts
│   └── reference/         ← Reference material (glossary, tables)
│
├── agents/                ← Per-agent implementation (see below)
│   ├── pi/
│   ├── codex/
│   ├── claude/
│   ├── gemini/
│   ├── opencode/
│   ├── cursor/
│   ├── aider/
│   ├── cline/
│   ├── roo/
│   ├── goose/
│   ├── copilot/
│   └── external/
│
├── configs/               ← Configuration templates and overrides
│   ├── shared/            ← Universal config (applies to all agents)
│   └── agents/            ← Agent-specific config overrides
│
├── templates/             ← Scaffolding for new agents, prompts, configs
│   ├── agent/             ← Template for a new agent folder
│   ├── prompt/            ← Prompt template
│   ├── config/            ← Config template
│   ├── workflow/          ← Workflow template
│   └── documentation/    ← Documentation template
│
├── examples/              ← Working examples
│   ├── universal/         ← Universal example workflows
│   └── agents/            ← Agent-specific examples
│
└── .github/               ← CI, issue templates, PR template
```

## Adding a New Agent

1. Copy `templates/agent/` to `agents/<new-agent>/`
2. Fill in the agent-specific READMEs
3. Add your agent to the [support matrix](docs/agents.md)
4. Add your agent to `TODO.md`

Full guide: [AGENTS.md](AGENTS.md) → "Adding New Agents"

## Community

- **Website:** [fartbull.xyz](https://fartbull.xyz)
- **X:** [@Fartbullssol](https://x.com/Fartbullssol)
- **X Community:** [FARTBULL Community](https://x.com/i/communities/1969613306378727682)
- **Solana CA:** `4uuxPfEdy2ZHhgux9zrRHtsbVx9yrnDrtLLAPWhmdKSE` (FARTBULL token — not required for agent usage)

## License

See [LICENSE.md](LICENSE.md).

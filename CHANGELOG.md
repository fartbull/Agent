# Changelog

All notable changes to this repository will be documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/),
and this project adheres to [Semantic Versioning](https://semver.org/).

---

## [0.2.0] — 2026-08-20

### Added

- **Skills system documentation** (`docs/skills/`) — catalog of 50+ composable agent capabilities across trading, DeFi, Solana, social, prediction markets, and design
- **Plugin system documentation** (`docs/plugins/`) — extends agents with custom MCP servers and tools (skill-builder, auth-manager, logger, scheduler)
- **TypeScript SDK reference** (`docs/sdk/`) — programmatic agent automation with types and examples
- **X API integration guide** (`docs/integrations/x-api.md`) — curl-based posting, replying, and mentions via xurl-style helpers
- **Agent scripts documentation** (`docs/scripts/`) — setup, installation, and management automation
- Per-agent config overrides (`configs/agents/*.yaml`) for all 12 agents
- `templates/config/config-template.yaml` — config template for new agents
- `templates/workflow/workflow-template.yaml` — workflow definition template
- GitHub Copilot documentation (`agents/copilot/`) — 7 files covering setup, config, prompts, workflows, examples, reference
- Roo Code subdirectory docs (setup, config, prompts, workflows, examples, reference)
- Gemini CLI docs (`agents/gemini/`) — with TODO markers for verification
- OpenCode docs (`agents/opencode/`) — with TODO markers for verification
- External agent template (`agents/external/`) — scaffolding for custom agents
- `examples/agents/` — brief per-agent usage examples for all 12 agents
- `docs/memory/` and `docs/context/` placeholder docs
- `.github/ISSUE_TEMPLATE/` — 4 issue templates: bug-report, agent-request, doc-update, guide-request
- `.github/workflows/` — 2 CI workflows: markdown link checker, markdown linter
- `.github/pull_request_template.md`

### Changed

- Updated `docs/agents.md` support matrix: Copilot → ✅ supported
- Updated `README.md` with new feature sections and architecture

---

## [0.1.0] — 2026-08-20

### Added

- Initial FARTBULL universal agent knowledge base.
- Repository rebranded from Hermes-focused docs to agent-agnostic.
- Universal docs section with: principles, prompting, memory, task decomposition, coding workflows, research workflows, verification, debugging, autonomous operation.
- Agent directories for: Pi, Codex, Claude Code, Cursor, Aider, Cline, Roo Code, Goose, Gemini CLI, OpenCode, Copilot, External.
- Configuration system with shared and agent-specific configs.
- Agent scaffolding template.
- Universal prompt library and example workflows.
- Support matrix at `docs/agents.md`.
- AGENTS.md with contribution and navigation rules.
- GitHub issue templates and PR template.
- Markdown link check CI workflow.

### Removed

- All Hermes-specific branding and documentation.

### Security

- No hardcoded credentials or API keys.
- Secrets documentation moved to universal security principles in `docs/concepts/safety.md`.

---

[0.2.0]: https://github.com/fartbull/agent/releases/tag/0.2.0
[0.1.0]: https://github.com/fartbull/agent/releases/tag/0.1.0

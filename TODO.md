# TODO

> Roadmap for the FARTBULL universal agent knowledge base.

Items are organized by category. Only checked items have actual implementation.

---

## Critical

- [x] LICENSE — placeholder created, owner needs to select license (see `LICENSE.md`)

## Agent Support

### Fully Supported (setup + config + prompts + workflows + examples + reference)
- [x] Pi — [agents/pi/](agents/pi/)
- [x] Codex — [agents/codex/](agents/codex/)
- [x] Claude Code — [agents/claude/](agents/claude/)
- [x] Cursor — [agents/cursor/](agents/cursor/)
- [x] Aider — [agents/aider/](agents/aider/)
- [x] Cline — [agents/cline/](agents/cline/)
- [x] Roo Code — [agents/roo/](agents/roo/)
- [x] Goose — [agents/goose/](agents/goose/)
- [x] Copilot — [agents/copilot/](agents/copilot/)
- [x] External — [agents/external/](agents/external/) (template/agent integration guide)

### Needs Verification
- [ ] Gemini CLI — [agents/gemini/](agents/gemini/) (setup/config/prompts drafted, needs verification)
- [ ] OpenCode — [agents/opencode/](agents/opencode/) (existence and configuration need investigation)

## FARTBULL Features

- [x] Skills system — `docs/skills/` (catalog of 50+ composable agent capabilities)
- [x] Plugin system — `docs/plugins/` (4 core plugins: skill-builder, auth-manager, logger, scheduler)
- [x] TypeScript SDK reference — `docs/sdk/` (programmatic agent automation)
- [x] X API integration (curl-based posting/reply) — `docs/integrations/x-api.md`
- [x] Agent scripts documentation — `docs/scripts/`
- [ ] Skill CLI tool verification (exact commands, installation)
- [ ] Plugin API verification (exact extension points, SDK format)
- [ ] SDK API verification (exact class/function names, TypeScript interfaces)

## Documentation

- [x] Universal concepts (principles, prompting, memory, task decomposition)
- [x] Universal workflows (coding, research, debugging, autonomous)
- [x] Universal prompt library
- [x] Agent support matrix
- [ ] Tool usage guides (per-tool, e.g., bash, browser, file system)
- [ ] Cross-agent feature comparison tables
- [ ] Integration guides (GitHub, Docker, Solana, etc.)

## Configuration

- [x] Shared config (base.yaml, safety.yaml)
- [x] Per-agent config overrides (configs/agents/*.yaml)
- [x] Config template
- [ ] Cross-agent config comparison tables
- [ ] Environment variable conventions per agent

## Examples

- [x] Universal example workflows
- [x] Examples for each fully-supported agent
- [ ] Multi-agent workflow examples (chaining tools across agents)

## Integrations

- [x] GitHub integration guide
- [x] Docker integration guide
- [x] Solana integration guide
- [x] MCP (Model Context Protocol) integration guide
- [x] X API integration (curl-based posting/reply)

## Website

- [ ] Sync with fartbull.xyz content
- [ ] Add redirect links from docs to website

## Automation

- [x] CI: markdown link checker (.github/workflows/markdown-links.yml)
- [x] CI: markdown linter (.github/workflows/markdown-lint.yml)
- [ ] Pre-commit hooks

## Research

- [ ] Test each agent against the same workflow and compare results
- [ ] Benchmark setup times per agent
- [ ] Document agent-specific quirks and gotchas

## Future Agents

- [ ] Investigate: Warp AI
- [ ] Investigate: Replit Agent
- [ ] Investigate: GitHub Models Agent
- [ ] Investigate: Windsurf
- [ ] Investigate: Tabnine Agent
- [ ] Investigate: Amazon CodeWhisperer

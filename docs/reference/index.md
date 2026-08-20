# Reference

Quick reference material for universal concepts.

## Common CLI Commands

| Task | Command |
|------|---------|
| List files | `ls` or use `glob` tool |
| Find in files | `grep` tool |
| Read file | `read` tool |
| Edit file | `edit` tool |
| Run command | `bash` tool |
| Start process | `hub start` |
| Check jobs | `hub jobs` |
| Search web | `web_search` |

## File Location Reference

| File | Purpose | Managed By |
|------|---------|------------|
| `AGENTS.md` | Agent instructions | User |
| `README.md` | Project overview | User |
| `TODO.md` | Task tracking | User/AI |
| `LICENSE.md` | License | Repo owner |
| `CHANGELOG.md` | Version history | Maintainers |
| `CONTRIBUTING.md` | Contribution guide | Maintainers |

## Agent Configuration Files

| File | Agent | Purpose |
|------|-------|---------|
| `CLAUDE.md` | Claude Code | Project context and instructions |
| `.cursorrules` | Cursor | Rules (legacy) |
| `.cursor/rules/` | Cursor | Rules (current) |
| `.clinerules` | Cline | Rules |
| `.roo/rules/` | Roo Code | Per-mode rules |
| `.roo/settings.json` | Roo Code | Permissions and settings |
| `.aider.conf` | Aider | Configuration |
| `.aider.model.settings` | Aider | Model preferences |
| `.aiderignore` | Aider | Files to ignore |
| `.env` | Various | Environment variables |
| `.env.example` | Various | Env template |

## Universal Principles

1. Think before acting — plan before touching files
2. Be precise — target specific lines, make minimal changes
3. Verify your work — run tests, confirm end-to-end behavior
4. Leave it better — clean up, update docs, no shims
5. Respect context — be mindful of token budgets

## Glossary

| Term | Definition |
|------|-----------|
| Agent | An AI system that can use tools to accomplish goals |
| Context window | The maximum tokens an agent can consider at once |
| Token | A unit of text (roughly 4 chars in English) |
| MCP | Model Context Protocol — standard for connecting tools to agents |
| CLI | Command Line Interface |
| OAuth | Open standard for access delegation |
| Rate limit | Restriction on how often you can call an API |
| Sandbox | A restricted environment for agent execution |

## See Also

- [Documentation Conventions](concepts/documentation.md)
- [Agent Support Matrix](agents.md)
- [Tool Usage](tools/tool-usage.md)

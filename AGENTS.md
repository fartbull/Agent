# AGENTS.md

> Instructions for AI agents working inside this repository.

This file is the entry point for any AI agent (Codex, Claude Code, Cursor, Aider, Cline, Goose, etc.) that wants to understand, navigate, or contribute to this repository.

---

## What This Repository Is

A **universal agent knowledge base** maintained by FARTBULL.

- **Goal:** One documentation + configuration + workflow repository that works across many AI agents.
- **Scope:** Setup guides, configuration patterns, prompt libraries, workflow recipes, integration guides, and reference material.
- **Not:** A tool you install and run. A documentation/configuration repository you read and adapt.

---

## Architecture at a Glance

```text
docs/     →  Universal concepts shared by ALL agents
agents/   →  Per-agent setup, config, prompts (agent-specific)
configs/  →  Reusable configuration (shared + agent overrides)
templates/→  Scaffolding for adding new agents, prompts, configs
examples/ →  Working examples (universal + agent-specific)
```

**Rule of thumb:**
- If it applies to *every* agent → put it in `docs/`
- If it only applies to *one* agent → put it in `agents/<name>/`
- If it's a reusable config snippet → put it in `configs/`
- If you're scaffolding something new → copy from `templates/`

---

## Documentation Conventions

| Convention | Rule |
|---|---|
| **Tone** | Technical, concise, direct. No marketing fluff. |
| **Links** | Use relative links. Test them before committing. |
| **Code blocks** | Always specify language (`yaml`, `bash`, `json`). |
| **Tables** | Use for comparisons, matrices, configs. |
| **TODOs** | Use `TODO` or `Needs verification` for unfinished/unverified content. Never fake it. |
| **Headings** | `##` for sections, `###` for subsections. Max depth 4. |
| **File names** | `kebab-case.md` for docs, `UPPERCASE` for configs. |

### When Something Is Unknown

If you are documenting an agent and you don't know a detail:

1. **Do not fabricate.**
2. Write: `TODO: Verify [specific claim]` or `Needs verification: [specific detail].`
3. Link to the agent's official docs if available.

---

## Agent-Specific Rules

Each agent folder (`agents/<name>/`) follows this structure:

```text
agents/<agent>/
├── README.md          ← Agent overview + what FARTBULL material applies
├── setup/             ← Installation and initial setup
├── config/            ← Agent-specific configuration files
├── prompts/           ← Agent-tailored prompts
├── workflows/         ← Agent-specific workflow recipes
├── examples/          ← Working examples for this agent
└── reference/         ← Official docs links, API references
```

**Each subdirectory should have a README.md** explaining:
- What belongs there
- How to use the contents
- Any prerequisites or caveats

---

## File Organization Rules

| Do | Don't |
|---|---|
| Link to shared docs in `docs/` from agent folders | Copy-paste universal docs into every agent folder |
| Create a new folder under `agents/` for each agent | Duplicate agent-specific config across folders |
| Use `configs/shared/` for universal config patterns | Hardcode secrets, API keys, or tokens |
| Use `TODO` markers for unverified claims | Invent config paths, commands, or APIs |
| Keep changes focused and minimal | Overbuild fake functionality |

---

## How to Add a New Agent

1. Copy `templates/agent/` to `agents/<new-agent>/`
2. Edit `agents/<new-agent>/README.md` with the agent overview
3. Create setup, config, prompts, workflows, examples, and reference content
4. Add the agent to `docs/agents.md` (support matrix)
5. Add TODO items for incomplete areas in `TODO.md`
6. If the agent has unique config, add overrides in `configs/agents/<new-agent>/`

See [templates/agent/README.md](templates/agent/README.md) for the skeleton.

---

## How to Verify Technical Claims

1. **Prefer primary sources.** Link to official docs, source code, or CLI help output.
2. **Cross-reference.** If two sources disagree, note the discrepancy.
3. **Be version-aware.** Note CLI versions where behavior differs.
4. **Mark uncertainty.** If you can't verify, write `Needs verification`.

---

## How to Update Existing Agents

1. Check `TODO.md` for open items in that agent's folder
2. Verify against the agent's latest docs/releases
3. Update the relevant file
4. Mark completed TODOs in `TODO.md`
5. Update the support matrix in `docs/agents.md`

---

## What NOT to Modify

- `AGENTS.md` — only the FARTBULL maintainers should edit this
- `LICENSE.md` — only change if the owner explicitly selects a new license
- `configs/shared/` — these are universal; coordinate major changes via issues
- `docs/concepts/` — these are cross-cutting; propose changes via PR with rationale

---

## Quick Reference for Common Tasks

| Task | Where to look |
|---|---|
| "What is this repo?" | [README.md](README.md) |
| "What agents are supported?" | [docs/agents.md](docs/agents.md) |
| "How do I set up agent X?" | [agents/x/README.md](agents/x/README.md) → [agents/x/setup/](agents/x/setup/) |
| "What config should I use?" | [configs/README.md](configs/README.md) |
| "I want to add an agent" | [AGENTS.md → Adding New Agents](#how-to-add-a-new-agent) + [templates/agent/](templates/agent/) |
| "What's unfinished?" | [TODO.md](TODO.md) |

---

## Repository Owner

**FARTBULL** — [fartbull.xyz](https://fartbull.xyz) · [@Fartbullssol](https://x.com/Fartbullssol)

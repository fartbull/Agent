# Memory

How AI agents persist information across sessions.

## Types of Memory

| Type | Lifetime | Scope | Example |
|------|----------|-------|---------|
| Conversation | Session | Single chat | Context within this task |
| Short-term | Session + files | Project | Notes, scratch files, TODOs |
| Persistent | Permanent | Repository | CLAUDE.md, AGENTS.md, README.md |
| External | Permanent | Cross-repo | Issue trackers, wikis, docs sites |

## Memory Patterns

### Project-Level Memory

Use files at the repository root:
- `AGENTS.md` — instructions for agents working in this repo
- `CLAUDE.md` / `.cursorrules` / `.clinerules` — agent-specific context
- `.agentignore` — files to skip (similar to `.gitignore`)

### Session Memory

- Keep a scratch pad file for intermediate findings
- Write notes incrementally, not all at once
- Use `TODO.md` for tracking multi-step work within a session

### Cross-Session Memory

- Update `TODO.md` as work progresses
- Commit findings to `docs/reference/` for future reference
- Use git history as the source of truth for decisions

## Best Practices

1. **Write down decisions** — don't hold them in context
2. **Update docs as you go** — stale docs are worse than no docs
3. **Use `AGENTS.md` for repo-wide instructions** — it's the entry point
4. **Keep scratch files separate** — use `.scratch/` or similar
5. **Link, don't duplicate** — reference shared docs rather than copying

## See Also

- [Context Packing](context/context-packing.md)
- [Task Decomposition](concepts/task-decomposition.md)
- [Agent Memory Systems](../../../examples/universal/memory-pattern.md)

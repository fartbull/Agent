# Agent Safety Checklist

Before running any AI coding agent on a task, use this checklist:

## Pre-Task

- [ ] **Project is in a git repository** — so you can review/undo changes
- [ ] **Working directory is clean** — `git status` shows no uncommitted changes
- [ ] **Sensitive files are protected** — `.env`, credentials, keys are gitignored
- [ ] **Task is clearly described** — includes what, why, and how to verify
- [ ] **Verification command is specified** — you know how to check success

## Security

- [ ] **No secrets in the codebase** — agent should not read or expose secrets
- [ ] **No production access** — agent runs in dev/local environment only
- [ ] **Approved command list** — restrict which shell commands the agent can run
- [ ] **Network restrictions** — if the agent doesn't need internet, disable it

## Scope

- [ ] **Clear boundaries** — task says what to change and what NOT to change
- [ ] **File paths specified** — don't let the agent search blindly
- [ ] **Acceptance criteria** — clear definition of "done"

## Post-Task

- [ ] **Review all file changes** — `git diff` before committing
- [ ] **Run verification command** — confirm tests pass
- [ ] **Commit with clear message** — if changes are approved

## Agent-Specific Safety

| Agent | Key Safety Feature |
|-------|-------------------|
| **Codex** | Docker sandbox |
| **Claude Code** | Tool approval prompts |
| **Goose** | Docker sandbox mode |
| **Aider** | `--dry-run` flag |
| **Cline** | `.cline/settings.json` permissions |
| **Roo** | `.roo/settings.json` permissions |
| **Cursor** | Settings → Privacy controls |
| **Copilot** | Agent mode requires explicit enable |
| **Pi** | No file system access (conversational only) |

## See Also

- [Safety principles](../../docs/concepts/safety.md)
- [Safety config](../../configs/shared/safety.yaml)

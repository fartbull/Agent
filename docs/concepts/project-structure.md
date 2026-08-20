# Project Structure

Universal guidelines for organizing codebases.

## Repository Layout

```text
/
├── README.md          ← Entry point, project overview
├── AGENTS.md          ← Instructions for AI agents
├── LICENSE            ← License file
├── .gitignore         ← Ignored files
├── .editorconfig      ← Editor settings
│
├── src/               ← Source code
├── tests/             ← Tests
├── docs/              ← Documentation
├── scripts/           ← Build/deploy scripts
├── configs/           ← Configuration files
└── examples/          ← Example usage
```

## Language-Specific Conventions

### Python

```text
src/
├── package_name/
│   ├── __init__.py
│   ├── module.py
│   └── cli.py
tests/
├── test_module.py
├── conftest.py
```

- Use `src/` layout
- `__init__.py` in every package
- Tests mirror source structure

### JavaScript/TypeScript

```text
src/
├── index.ts
├── module/
│   ├── module.ts
│   └── module.test.ts
```

- Co-locate tests with source files (`.test.ts`)
- Use `src/` for code, `types.ts` for interfaces
- `tsconfig.json` with strict mode

### Shell Scripts

```text
scripts/
├── build.sh
├── deploy.sh
├── lib/
│   └── common.sh
```

- `#!/usr/bin/env bash` shebang
- `set -euo pipefail` for error safety
- Functions for reusable logic
- Comments explaining non-obvious logic

### Go

```text
cmd/
├── server/
│   └── main.go
├── cli/
│   └── main.go
internal/
├── package1/
pkg/
├── library/
test/
```

## Configuration Files

| File | Purpose |
|------|---------|
| `AGENTS.md` | Agent instructions (repo root) |
| `CLAUDE.md` | Claude Code project context |
| `.cursorrules` | Cursor rules (legacy) |
| `.cursor/rules/` | Cursor rules (current) |
| `.clinerules` | Cline rules |
| `.aider.conf` | Aider configuration |
| `.aiderignore` | Files to ignore for Aider |
| `.env` | Environment variables (gitignored) |
| `.env.example` | Environment variable template |

## Naming Conventions

| Element | Convention | Example |
|---------|-----------|---------|
| Files | kebab-case | `my-feature.ts` |
| Directories | kebab-case | `user-auth/` |
| Functions (TS) | camelCase | `getUserById()` |
| Functions (Python) | snake_case | `get_user_by_id()` |
| Classes | PascalCase | `UserManager` |
| Constants | SCREAMING_SNAKE | `MAX_RETRIES` |
| Environment | UPPER_SNAKE | `DATABASE_URL` |

## See Also

- [Safety](safety.md)
- [Documentation](documentation.md)

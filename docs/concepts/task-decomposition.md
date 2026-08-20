# Task Decomposition

Breaking large tasks into manageable, verifiable steps.

## The Pattern

Every task should decompose into:

1. **Scope** — what exactly needs to be done
2. **Research** — understand the codebase, patterns, constraints
3. **Plan** — concrete steps with file targets
4. **Implement** — execute the plan
5. **Verify** — prove the work is correct

## Decomposition Techniques

### Vertical Slices

Work feature-by-feature, end-to-end:

```
Feature A: implement → test → document
Feature B: implement → test → document
```

Not:

```
All implementations → all tests → all docs
```

### Dependency Ordering

- **Prerequisites first** — set up shared schemas, interfaces, scaffolds
- **Independent work in parallel** — delegate non-dependent pieces
- **Dependents after** — anything that needs a prerequisite waits

### Parallel Work

Identify truly independent slices:

| Independent | Depends On |
|------------|------------|
| Module A tests | Module A implementation |
| Module B tests | Module B implementation |
| Module A impl | — |
| Module B impl | — |

Run A and B in parallel; test after each completes.

## Planning Before Acting

Before touching any files:

1. Read relevant docs and existing code
2. Identify patterns to follow
3. Note callsites that will need updating
4. Write the plan down (TODO list or scratch pad)

## Example Decomposition

```
Task: Add OAuth login to the API

1. Research: Read existing auth patterns in auth.py
2. Add dependencies: fastapi-users, python-social-auth
3. Create OAuth provider models
4. Add database migration for OAuth tables
5. Implement login/redirect/callback endpoints
6. Add config for OAuth providers (Google, GitHub)
7. Write tests for each endpoint
8. Document in docs/auth/oauth.md
9. Update README with OAuth instructions
```

## Anti-Patterns

- **Premature execution** — starting before the plan is clear
- **Sequential when parallel is possible** — wasting time on independent work
- **Re-auditing applied edits** — checking changes that already compiled/work
- **Shrinking scope** — doing 80% instead of 100% unless explicitly approved
- **Delegation without coordination** — spinning up work without a shared contract

## See Also

- [Principle: Think Before Acting](#principles)
- [Context Packing](context/context-packing.md)
- [Coding Workflows](../workflows/coding-workflows.md)

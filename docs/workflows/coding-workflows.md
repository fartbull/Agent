# Coding Workflows

Universal coding workflows that apply across agents.

## 1. Research → Plan → Implement → Verify

### Step 1: Research

- Read relevant docs and existing code
- Identify patterns to follow
- Note callsites that will need updating
- Use `grep` to find references, not by guessing

### Step 2: Plan

Write down the plan before touching files:
- What files will change
- What the changes achieve
- How to verify

### Step 3: Implement

- Make surgical, focused edits
- Prefer updating existing files over creating new ones
- Follow existing conventions — don't add a second pattern
- Re-read after edits (line numbers shift)

### Step 4: Verify

- Run the specific test, command, or scenario covering your change
- Confirm the deliverable behaves as specified end to end
- Don't re-audit applied edits — trust tool results

## 2. Feature Implementation Pattern

```bash
# 1. Research
grep -r "old_function" src/
read src/module.py
read src/utils/

# 2. Plan
echo "Plan: Replace old_function with new_api in 3 files" > .scratch/plan.md

# 3. Implement
# Edit src/module.py
# Edit src/utils/
# Update any callers

# 4. Verify
pytest tests/test_module.py
```

## 3. Bug Fix Pattern

1. **Reproduce** the bug — find the exact scenario
2. **Root cause** — identify the source, not the symptom
3. **Fix at the source** — don't suppress symptoms
4. **Verify** — confirm the reproduction no longer triggers

```bash
# Reproduce
python -c "from app import bug_func; bug_func()"  # crashes

# Root cause
grep -rn "bug_func" src/  # find all callers

# Fix
# Edit the actual buggy line

# Verify
python -c "from app import bug_func; bug_func()"  # works now
```

## 4. Refactoring Pattern

1. **Identify the scope** — what's being refactored, what's affected
2. **Update all callsites** — use `lsp references` or grep
3. **Migrate, don't shim** — leave no deprecated paths
4. **Verify** — run the full test suite

## 5. Test-Driven Development

When writing tests:
- Every test must defend an observable contract
- Test behavior, boundaries, invariants, transitions, real errors
- Match existing conventions
- Keep tests deterministic, isolated, full-suite safe

## 6. Multi-File Changes

For changes spanning multiple files:
1. Identify the shared contract (schema, interface, format)
2. Implement it inline (you have the most context)
3. Delegate independent slices to parallel agents
4. Have each slice produce the exact same format

## See Also

- [Task Decomposition](../concepts/task-decomposition.md)
- [Research Workflows](research.md)
- [Debugging Workflows](debugging.md)
- [Autonomous Workflows](autonomous.md)

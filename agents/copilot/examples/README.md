# Copilot Examples

## Example 1: Bug Fix (Agent Mode)

```
You: Fix the race condition in src/worker.go. Add a mutex around the
     shared counter. Run: go test ./...
```

## Example 2: Feature Implementation (Agent Mode)

```
You: Create a health check endpoint at GET /health in src/app.py.
     Return {"status": "ok"}. Write tests. Run: python -m pytest
```

## Example 3: Code Explanation (Chat Mode)

Select code and in Chat:

```
/explain
```

## Example 4: Using Slash Commands

```
/tests
# Write tests for the selected function
```

```
/refactor
# Refactor the selected code to be cleaner
```

## Example 5: CLI Usage

```bash
gh copilot suggest "git stash"
# Copilot suggests: git stash, git stash list, git stash pop, ...

gh copilot explain "npm install"
# Explains what the command does
```

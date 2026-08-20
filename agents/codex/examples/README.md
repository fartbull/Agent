# Codex Examples

## Example 1: Fix a Bug

```bash
codex -p "Fix the null pointer exception in src/parser.js. The error occurs
when the input is an empty string. Add a guard clause at the top of the
parse() function. Run: node --test test/parser.test.js"
```

## Example 2: Add a Feature

```bash
codex -p "Add a CSV export function to the analytics module. Create
src/analytics/export.go with a function ExportCSV(data []Record) error.
Follow the existing code patterns in src/analytics/. Run: go test ./..."
```

## Example 3: Refactor

```bash
codex -p "Refactor src/utils.js to use ESM imports instead of CommonJS.
Update all internal imports. Update package.json type field. Run: npm test"
```

## Example 4: Write Tests

```bash
codex -p "Write unit tests for the AuthMiddleware in src/middleware/auth.ts.
Cover: valid token, expired token, missing token, malformed token.
Use jest and the existing test patterns in test/middleware/. Run: npm test"
```

## Example 5: Documentation

```bash
codex -p "Write a README for the API endpoints in src/routes/api.py.
Document each endpoint: method, path, parameters, response format,
example request/response. Place it in docs/api.md."
```

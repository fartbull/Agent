# Roo Examples

## Example 1: Feature Implementation (Code Mode)

```
You: Create a health check endpoint at GET /health in src/app.py.
     Return {"status": "ok"}. Write tests. Run: python -m pytest
```

## Example 2: Bug Investigation (Debug Mode)

```
You: Investigate the database connection leak. The error log shows
     "connection pool exhausted" after running for 2 hours. Check
     src/db/pool.go and src/handlers/user.go.
```

## Example 3: With Rules

`.roo/rules/code.md`:

```markdown
You are a React + TypeScript developer.
- Use functional components with hooks
- Run `npm test` after changes
- Use Tailwind CSS for styling
```

Prompt:

```
You: Create a user profile page with avatar upload and edit form.
     Follow the existing patterns in src/components/.
```

## Example 4: Ask Mode

```
You: List all external API dependencies in src/ and check if any
     are using deprecated endpoints.
```

## Example 5: Refactoring

```
You: Migrate the Express app to use async/await throughout. Replace
     all callback patterns in src/routes/. Run: npm test
```

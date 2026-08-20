# Goose Examples

## Example 1: Fix a Bug

```bash
goose -i "Fix the race condition in the worker pool at src/worker.go.
Add a mutex around the shared counter. Run: go test ./..."
```

## Example 2: Create a Script

```bash
goose -i "Create a Python script at scripts/process_logs.py that:
1. Reads log files from logs/ directory
2. Extracts all 500 errors
3. Outputs a summary to stdout

Run: python scripts/process_logs.py"
```

## Example 3: Documentation

```bash
goose -i "Write API documentation for the REST endpoints defined in
src/routes/api.py. Include parameters, response format, and examples.
Save to docs/api.md."
```

## Example 4: Test Generation

```bash
goose -i "Write unit tests for the AuthMiddleware in src/middleware/auth.ts.
Cover valid token, expired token, missing token, malformed token.
Use the test patterns in tests/. Run: npm test"
```

## Example 5: Configuration

```bash
goose -i "Configure the project to use Docker. Create a Dockerfile
for the Node.js app, a docker-compose.yml with a PostgreSQL service,
and a .dockerignore file. The app listens on port 3000."
```

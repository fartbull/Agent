# Universal Prompt Library

Reusable prompts that work across agents.

## Coding Prompts

### Implement a Feature

```
Implement [feature name] in [file or directory].

Context:
- [relevant background, links, context]
- [pattern to follow: link to existing code]

Requirements:
- [requirement 1]
- [requirement 2]

Test:
- Run [test command] and confirm it passes

Verify:
- [how to confirm the feature works end to end]
```

### Refactor a Module

```
Refactor [module name] to [goal].

Steps:
1. Read and understand the current implementation
2. Identify all callers — use grep/search
3. Refactor with minimal changes
4. Update all callers
5. Run tests: [test command]

Constraints:
- Keep the public API unchanged
- Don't break existing tests
```

### Write Tests

```
Write tests for [module or function].

Follow the existing test patterns in [test directory].
Cover:
- Normal operation
- Error cases
- Boundary conditions
- Edge cases

Run: [test command]
```

### Code Review

```
Review [file or directory] for:
- Logic errors
- Security issues
- Performance concerns
- Code clarity
- Test coverage

Report issues with file:line references and severity.
```

## Research Prompts

### Codebase Investigation

```
I'm working in [directory]. Understand the following:

1. What is the project structure?
2. What are the key modules and their responsibilities?
3. What patterns are used (dependency injection, error handling, etc.)?
4. Where are the tests and how do they run?
5. What does the build/deploy process look like?

Summarize in a brief report.
```

### API Documentation

```
Look up the [library/tool name] API.

Find:
- Installation instructions
- Basic usage examples
- Configuration options
- Common patterns
- Gotchas or limitations

Source from official docs only. Link each finding.
```

## Autonomous Operation Prompts

### Daily Standup Agent

```
You are an autonomous coding agent. Your task is to work on [repository].

Process:
1. Read TODO.md for today's priorities
2. Pick the highest-priority unstarted task
3. Research it if needed
4. Implement it
5. Test it
6. Mark it done in TODO.md
7. Repeat until all tasks are done or you hit your token limit

Report a summary at the end.
```

### Monitoring Agent

```
Monitor [service/system] and:
1. Check health every [interval]
2. If unhealthy, investigate and try to fix
3. If you can't fix it, alert with details
4. Log all actions

Run for [duration] hours.
```

## Social Media Prompts

### X Post Generator

```
Draft an X post about [topic] using the [tone] tone.

Include:
- Key insight or update
- 1-3 relevant hashtags
- A call to action

Keep under 280 characters. Don't post yet — just show me the draft.
```

### Research + Post

```
1. Search X for posts about [topic] from the last [timeframe]
2. Summarize the top [N] most engaging posts
3. Draft a response post with my take

Show me the summary and draft before posting.
```

## Multi-Agent Prompts

### Task Delegation

```
You are coordinating multiple agents. Your task: [complex task].

Break it into independent sub-tasks. Assign each to a separate agent.
Each agent should:
1. Complete its sub-task
2. Return results in [format]
3. Update TODO.md when done

Monitor progress and synthesize results.
```

## See Also

- [Agent-specific prompt libraries](../../../agents/)
- [Prompting Guide](concepts/prompting.md)

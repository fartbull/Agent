# Prompting

Universal prompting strategies that work across agents.

## Core Patterns

### Be Specific

```
Bad: "Fix the login bug"
Good: "The login page shows a 500 error when the password field is empty. Fix the validation in src/auth/login.py."
```

### Provide Context

Include:
- What you're working on
- What's been tried
- What the expected outcome is
- What constraints apply

### Ask for Verification

End complex prompts with: "After implementing, run the tests and report the result."

## Prompt Structure

1. **Goal** — one sentence of what you want
2. **Context** — relevant background, file paths, error messages
3. **Constraints** — what not to do, style requirements, test requirements
4. **Verification** — how to confirm success

## Universal Prompt Templates

### Bug Fix Template

```
PROBLEM:
[Description of the bug]

REPRODUCE:
[Steps to reproduce]

EXPECTED:
[What should happen]

ACTUAL:
[What actually happens]

CONTEXT:
[File paths, error messages, recent changes]

FIX:
[Specific guidance or leave open for the agent]

VERIFY:
[How to confirm the fix works]
```

### Feature Implementation Template

```
GOAL: [One sentence feature description]

CONTEXT:
- Relevant files: [paths]
- Existing patterns: [links or descriptions]
- Dependencies: [if any]

REQUIREMENTS:
- [Requirement 1]
- [Requirement 2]

ACCEPTANCE:
[Criteria that must be met]

VERIFY:
[How to test the feature]
```

### Code Review Template

```
REVIEW: [file or directory]

FOCUS: [e.g., security, performance, readability]

CHECKLIST:
- [ ] Logic correctness
- [ ] Error handling
- [ ] Security concerns
- [ ] Naming clarity
- [ ] Test coverage

REPORT: List issues found, with file:line references and severity.
```

## Prompt Libraries

- [Universal prompts](../prompts/universal-prompts.md)
- [Agent-specific prompts](../agents/) (links per agent)

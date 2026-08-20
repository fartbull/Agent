# Universal Prompt Template

A universal prompt format that works across agents.

```markdown
# {task_name}

## Goal
{one sentence describing what you want}

## Context
{relevant background, file paths, error messages}

## Requirements
- {requirement 1}
- {requirement 2}

## Constraints
- {constraint 1}
- {constraint 2}

## Verification
{how to confirm success}

## Acceptance Criteria
- [ ] {criterion 1}
- [ ] {criterion 2}
```

## Usage

Replace the placeholders (`{variable}`) with your specific values. This template works for:

- Bug fixes
- Feature implementation
- Code review
- Refactoring
- Research tasks

## Example

```markdown
# Fix memory leak in parser

## Goal
Fix the memory leak in the recursive descent parser that occurs on deeply nested input.

## Context
- File: src/parser/descent.py
- Error: MemoryError after ~5000 levels of nesting
- Recent change: commit abc123 added the lookahead buffer

## Requirements
- Parse nested structures up to 10000 levels deep
- Memory usage should not exceed 2x the input size

## Constraints
- Don't change the public API
- Must pass existing tests
- Use iterative approach, not recursion

## Verification
python -c "from src.parser import parse; parse('(' * 10000 + ')' * 10000)"
Should not raise MemoryError

## Acceptance Criteria
- [ ] Parse 10000 levels of nesting without MemoryError
- [ ] All existing tests pass
- [ ] New test added for deep nesting
```

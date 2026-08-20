# TypeScript SDK Reference

The FARTBULL TypeScript SDK provides programmatic access to agent capabilities, skills, and configuration.

## Installation

TODO: Verify package name and installation command.

```bash
npm install @fartbull/agent-sdk
# or from source
git clone https://github.com/fartbull/agent
cd agent
npm install
```

## Quick Start

```typescript
import { createAgent, useSkill, configure } from '@fartbull/agent-sdk';

// Create an agent with specific skills
const agent = await createAgent({
  skills: ['dexscreener', 'query-token-info', 'trading-signal'],
  model: 'claude-3-5-sonnet-20241022',
});

// Run a task
const result = await agent.run(
  "Find Solana tokens with high smart money inflow and generate a report"
);

console.log(result.output);
```

## Core Concepts

TODO: Verify these concepts against the SDK source.

### Agent

An `Agent` instance is the main entry point. It manages:
- LLM provider and model configuration
- Loaded skills (tool functions)
- Session history
- File system access

### Skill

A `Skill` is a bundle of tool functions:

```typescript
interface Skill {
  name: string;
  description: string;
  tools: Tool[];
  authenticate?: (params: AuthParams) => Promise<void>;
}
```

### Client

The `Client` class handles API communication:

```typescript
class AgentClient {
  constructor(options: ClientOptions);
  
  // Execute a task
  async run(prompt: string, options?: RunOptions): Promise<TaskResult>;
  
  // Load a skill
  async loadSkill(skillName: string): Promise<void>;
  
  // List available skills
  async listSkills(): Promise<string[]>;
}
```

TODO: Verify the exact class and function names.

## Type Definitions

Core types:

```typescript
interface AgentOptions {
  model?: string;
  provider?: 'anthropic' | 'openai' | 'google';
  skills?: string[];
  temperature?: number;
  maxTokens?: number;
}

interface TaskResult {
  success: boolean;
  output: string;
  usage: {
    inputTokens: number;
    outputTokens: number;
  };
  artifacts?: Artifact[];
}

interface Artifact {
  type: 'file' | 'image' | 'log';
  path?: string;
  content?: string | Buffer;
}
```

TODO: Verify exact type definitions.

## See Also

- [Skills System](skills/README.md)
- [Configuration System](../../configs/)
- [Agent Templates](../../templates/agent/)

# Ralph Agent Instructions

## Overview

Ralph is an autonomous AI agent loop that runs opencode repeatedly until all PRD items are complete. Each iteration is a fresh opencode instance with clean context.

## Commands

```bash
# Run Ralph (from your project that has prd.json)
ralph [max_iterations] (default: unlimited)
```

## Key Files

- `bin/ralph` - The bash loop that spawns fresh opencode instances
- `prompt.md` - Instructions given to each opencode instance
- `prd.json.example` - Example PRD format

## Patterns

- Each iteration spawns a fresh opencode instance with clean context
- Memory persists via git history, `progress.md`, and `prd.json`
- Stories should be small enough to complete in one context window
- Always update AGENTS.md with discovered patterns for future iterations

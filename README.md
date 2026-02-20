# Think First

Stop your AI agent from coding before thinking. Enforces a plan-first workflow: understand, explore, plan, then implement. Reduces backtracking and wasted tokens.

## The Problem

Your AI agent's #1 problem isn't knowledge - it's process. Agents leap into code on the first prompt. They edit files before reading them. They create new utilities without checking if one exists. They fix symptoms without understanding root causes. The result: backtracking, wasted tokens, and changes that break things you didn't know existed.

## What Think First Does

Think First is a behavior modifier, not a knowledge plugin. It doesn't teach your agent new facts. It changes how your agent approaches every task - from "dive into code" to "understand first, plan second, implement third."

### Without Think First

User: "Fix the login bug"

Agent: Immediately opens auth.ts, changes a condition, proposes a diff. Maybe it works. Maybe it breaks the reset flow. Maybe there's already a fix in a different branch. You find out later.

### With Think First

User: "Fix the login bug"

Agent: Reads auth.ts, traces the login flow, searches for similar fixes, identifies affected areas (login, reset, OAuth), proposes a plan with risks and testing strategy, waits for approval, then implements.

## Install

### Cursor IDE

```
/add-plugin think-first
```

### Claude Code

```
/plugin install think-first
```

### Skills only (any agent)

```bash
npx skills add ofershap/think-first/think-first
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

### Skills

- **think-first** - Enforces plan-first workflow to reduce backtracking and wasted tokens

### Rules

- **think-first** - Always-on rules that enforce read-before-write, search-before-create, understand-before-fix, plan-before-implement

### Commands

- `/plan` - Create a structured implementation plan before making changes
- `/review-approach` - Review the current implementation approach and suggest improvements

## License

MIT

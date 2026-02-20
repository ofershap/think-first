# Think First

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Skills](https://img.shields.io/badge/skills.sh-think--first-blue)](https://skills.sh/ofershap/think-first/think-first)

Stop your AI agent from coding before thinking. Enforces a plan-first workflow: read before writing,
search before creating, understand before fixing. Reduces backtracking, wasted tokens, and broken
changes.

> Your agent's #1 problem isn't knowledge - it's process. It edits files before reading them. It
> creates utilities that already exist. It fixes symptoms without tracing root causes. Think First
> changes the default from "dive into code" to "understand first, plan second, implement third."

## The Difference

**Without Think First** - "Fix the login bug"

Agent opens auth.ts, changes a condition, proposes a diff. Maybe it works. Maybe it breaks the reset
flow. Maybe there's already a fix in a different branch.

**With Think First** - "Fix the login bug"

Agent reads auth.ts, traces the login flow, searches for similar fixes, identifies affected areas
(login, reset, OAuth), proposes a plan with risks and testing strategy, then implements.

## Install

### Cursor / Claude Code / Windsurf

```bash
npx skills add ofershap/think-first/think-first
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

| Type    | Name               | Description                                                                 |
| ------- | ------------------ | --------------------------------------------------------------------------- |
| Skill   | `think-first`      | 10 rules for read-before-write, search-before-create, plan-before-implement |
| Rule    | `think-first`      | Always-on behavioral rule that enforces the plan-first workflow             |
| Command | `/plan`            | Create a structured implementation plan before making changes               |
| Command | `/review-approach` | Review the current approach and suggest improvements                        |

## The 10 Rules

1. **Read before writing** - read all relevant files before editing any
2. **Understand the full picture** - trace the issue through the codebase before proposing a fix
3. **Check if it already exists** - search for existing implementations before creating new ones
4. **Propose a plan for complex changes** - outline the approach for changes touching 3+ files
5. **Identify affected areas** - find all files, tests, and features that could break
6. **Consider alternatives** - briefly evaluate 2-3 approaches for non-trivial changes
7. **Verify assumptions** - read the actual code instead of guessing
8. **Minimal change principle** - smallest change that solves the problem, separate refactoring from
   fixes
9. **Test awareness** - identify how the change will be verified before implementing
10. **Context preservation** - stay focused on the original goal, don't chase tangential issues

## Related Plugins

- [vibe-guard](https://github.com/ofershap/vibe-guard) - Security guardrails (pairs well with
  plan-first workflow)
- [ai-humanizer](https://github.com/ofershap/ai-humanizer) - Prevent AI-detectable patterns in
  generated content

## Author

[![Made by ofershap](https://gitshow.dev/api/card/ofershap)](https://gitshow.dev/ofershap)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/ofershap)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github&logoColor=white)](https://github.com/ofershap)

## License

MIT

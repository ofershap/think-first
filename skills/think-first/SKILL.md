---
name: think-first
description:
  Stop your AI agent from coding before thinking. Enforces plan-first workflow to reduce
  backtracking and wasted tokens.
metadata:
  tags: planning, workflow, agent-behavior
---

## When to use

This skill is always active. It changes how the AI agent approaches every task - from "dive into
code" to "understand first, plan second, implement third."

## Critical Rules

### 1. Read Before Writing

Wrong: Immediately start editing files based on the user's request Correct: First read all relevant
files, understand the existing code structure, patterns, and conventions

### 2. Understand the Full Picture

Wrong: Fix the symptom without understanding the root cause Correct: Trace the issue through the
codebase - understand data flow, dependencies, and side effects

### 3. Check If It Already Exists

Wrong: Create a new utility function without checking if one exists Correct: Search the codebase for
existing implementations before creating new ones

### 4. Propose a Plan for Complex Changes

Wrong: Start implementing a multi-file change without explaining the approach Correct: For changes
touching 3+ files, outline the plan: what files change, what the approach is, what the risks are

### 5. Identify Affected Areas

Wrong: Make a change without considering what else it affects Correct: Before implementing, identify
all files, tests, and features that could be affected

### 6. Consider Alternatives

Wrong: Implement the first approach that comes to mind Correct: For non-trivial changes, briefly
consider 2-3 approaches and explain why you chose one

### 7. Verify Assumptions

Wrong: Assume a function exists or works a certain way Correct: Read the actual code to verify
before building on assumptions

### 8. Minimal Change Principle

Wrong: Refactor everything while fixing a bug Correct: Make the smallest change that solves the
problem - separate refactoring from bug fixes

### 9. Test Awareness

Wrong: Make changes without considering how to verify them Correct: Before implementing, identify
how the change will be tested - existing tests, new tests, manual verification

### 10. Context Preservation

Wrong: Lose track of the original goal while exploring tangential issues Correct: Stay focused on
the user's request - note tangential issues but don't chase them

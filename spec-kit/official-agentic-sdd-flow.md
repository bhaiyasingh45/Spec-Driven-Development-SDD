# Official Agentic SDD Flow

This document tracks the current GitHub Spec Kit agentic SDD flow used as the reference for this repository.

## Full production flow

```text
/speckit.constitution
        ↓
/speckit.specify
        ↓
/speckit.clarify
        ↓
/speckit.plan
        ↓
/speckit.checklist
        ↓
/speckit.tasks
        ↓
/speckit.analyze
        ↓
/speckit.implement
        ↓
/speckit.converge
```

## What each stage does

- **constitution** — establishes project principles and rules that later work is evaluated against.
- **specify** — defines what to build and why, focusing on user-facing behavior rather than implementation technology.
- **clarify** — resolves important ambiguity before architectural planning.
- **plan** — derives the technical approach, architecture, stack, and constraints from the specification.
- **checklist** — tests the quality of the requirements themselves for completeness, clarity, and consistency.
- **tasks** — turns the approved design into actionable, dependency-ordered work.
- **analyze** — performs read-only consistency checks across specification, plan, and tasks.
- **implement** — executes the tasks in dependency order; larger features can be implemented in scoped phases.
- **converge** — compares the implemented code against the spec, plan, and tasks and appends remaining work when gaps are found.

## Agentic principle

The coding agent is not driven by a single large prompt. Each stage produces structured artifacts that become context for the next stage. This creates a controlled feedback loop in which requirements can be refined before implementation and implementation can be checked against the original intent.

## Practical rule

For meaningful production work, prefer the full flow. For small, low-ambiguity changes, the shorter `specify → plan → tasks → implement → converge` path can be appropriate.

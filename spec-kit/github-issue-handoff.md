# Spec-to-GitHub Issue Handoff

GitHub Spec Kit can convert generated tasks into GitHub Issues with `/speckit.taskstoissues`. This creates a bridge between specification artifacts and normal engineering tracking.

## Recommended Flow

```text
spec.md
  ↓
plan.md
  ↓
tasks.md
  ↓
/speckit.analyze
  ↓
/speckit.taskstoissues
  ↓
GitHub Issues
  ↓
Agent implementation
  ↓
/speckit.converge
```

## Why the Handoff Matters

Tasks are the agent's execution contract, while GitHub Issues provide durable team-level visibility. Converting tasks after analysis helps avoid tracking work that is based on an inconsistent or incomplete plan.

## Rules

1. Generate tasks from the approved plan.
2. Run consistency analysis before creating tracking issues for substantial work.
3. Keep issue descriptions traceable to the originating task and requirement.
4. Do not treat an issue as permission to invent new product requirements.
5. After implementation, use convergence to check the actual code against the specification artifacts.

## Human Control

Creating GitHub Issues and implementing them are separate actions. Issue creation should not be interpreted as automatic approval to implement every issue without the normal review and authorization process.

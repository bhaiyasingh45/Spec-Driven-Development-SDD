# GitHub Spec Kit — Agentic SDD Workflow

This guide follows the official GitHub Spec Kit documentation. Spec Kit provides structured processes and artifacts for AI coding agents; these skills are invoked in the coding agent's chat, not as terminal shell commands. Exact invocation syntax can vary by agent integration.

Official references:
- Quickstart: https://github.com/github/spec-kit/blob/main/docs/quickstart.md
- Agentic SDD reference: https://github.com/github/spec-kit/blob/main/docs/reference/agentic-sdd.md
- Repository: https://github.com/github/spec-kit

## 1. Project setup — once per project

```text
/speckit-constitution
```

Create or update the project's governing principles. Revisit the constitution when project-wide principles change; it is not a per-feature artifact.

## 2. Core feature workflow

```text
/speckit-specify
/speckit-plan
/speckit-tasks
/speckit-implement
/speckit-converge
```

- **Specify** — describe user needs, behavior, and why the feature matters. Keep tech-stack choices out of this stage unless they are genuine requirements or constraints.
- **Plan** — derive architecture and implementation choices from the specification.
- **Tasks** — produce actionable, dependency-ordered work from the plan.
- **Implement** — execute tasks in order; for large features, work in scoped phases and validate each phase.
- **Converge** — assess the current code against `spec.md`, `plan.md`, and `tasks.md`. If gaps remain, convergence appends tasks; implement those tasks and run converge again until it reports Converged.

## 3. Optional quality gates for meaningful ambiguity or risk

The full production path adds these stages:

```text
/speckit-constitution       # once per project
/speckit-specify            # each feature
/speckit-clarify            # resolve underspecified requirements
/speckit-plan
/speckit-checklist          # review requirement quality
/speckit-tasks
/speckit-analyze            # cross-artifact consistency check
/speckit-implement
/speckit-converge
```

Use the extra stages intentionally:
- **Clarify** asks targeted questions about missing or ambiguous behavior and updates the spec. Run it before planning when needed; return to it if analysis later exposes requirement gaps.
- **Checklist** creates a requirements-quality checklist. It checks whether requirements are clear, complete, and consistent; it is not an implementation-completion checklist. Custom checklist approval belongs to the reviewer.
- **Analyze** is read-only. It checks for conflicts, gaps, and ambiguities across the spec, plan, and tasks. Fix problems in the artifact that owns them, then re-run analysis.

The official guidance describes the commands as designed to run in order, while clarify, checklist, and analyze are quality gates added when meaningful ambiguity warrants them. For a small, clear feature, use the core workflow; for production or high-risk work, use the full path.

## 4. Artifact flow and agent responsibilities

```text
User intent
  → spec.md       (what and why)
  → plan.md       (how and constraints)
  → tasks.md      (ordered executable work)
  → implementation
  → convergence findings / additional tasks
  → implement again until converged
```

The agent should use existing artifacts as durable context instead of relying on one oversized prompt. Human review remains important for product decisions, checklist approval, significant trade-offs, and final code review.

## 5. Operating rules

1. Define observable behavior before selecting implementation details.
2. Resolve important ambiguity before planning.
3. Keep requirements, plan, and tasks consistent.
4. Do not treat a clean analysis report as proof that the implementation is complete.
5. Do not treat checked requirements-quality checklist items as proof that code is implemented.
6. Run converge only after implementation has run against the current task list.
7. Repeat implement → converge if convergence identifies remaining gaps.
8. Review generated code and evidence before merging.

## 6. Recommended sequences

### Small, well-understood feature

```text
/speckit-specify
/speckit-plan
/speckit-tasks
/speckit-implement
/speckit-converge
```

### Production or ambiguous feature

```text
/speckit-specify
/speckit-clarify
/speckit-plan
/speckit-checklist
/speckit-tasks
/speckit-analyze
/speckit-implement
/speckit-converge
```


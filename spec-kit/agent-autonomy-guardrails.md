# Agent Autonomy Guardrails

Agentic SDD should increase implementation autonomy without allowing the agent to invent product intent.

## The Agent May Act Autonomously When

- The requirement is explicit in `spec.md`.
- The implementation choice is covered by `plan.md` or established project constraints.
- The work maps to an existing task in `tasks.md`.
- Acceptance criteria can be verified objectively.
- The change does not introduce an unapproved product decision.

## The Agent Should Stop and Ask When

- Two requirements conflict.
- A missing requirement changes user-visible behavior.
- A security, compliance, cost, or data-retention decision is not specified.
- Multiple materially different product behaviors are possible.
- The requested implementation contradicts the constitution or approved plan.

## Safe Loop

```text
Read artifacts
  ↓
Identify uncertainty
  ↓
Can existing artifacts resolve it?
  ├─ Yes → continue
  └─ No  → ask / clarify
  ↓
Implement scoped task
  ↓
Verify acceptance criteria
  ↓
Converge against spec/plan/tasks
  ↓
Continue or report
```

## Important Boundary

Autonomy applies to execution, not to silently changing intent. When a decision belongs to the product owner or human reviewer, the agent should surface the decision rather than manufacture an assumption.

# SDD Traceability Matrix

A traceability matrix connects the original requirement to the evidence that proves it was implemented correctly.

## Template

| Requirement | Acceptance Criteria | Plan Section | Task | Test / Evidence | Status |
|---|---|---|---|---|---|
| REQ-001 | AC-001 | Plan 1 | TASK-001 | Test-001 | Planned |
| REQ-002 | AC-002 | Plan 2 | TASK-002 | Test-002 | Planned |

## How to Use It

1. Give each requirement a stable identifier such as `REQ-001`.
2. Give each acceptance criterion a corresponding identifier such as `AC-001`.
3. Link requirements to the relevant implementation-plan section.
4. Break the plan into tasks with stable identifiers.
5. Record the tests, reviews, or other evidence used for validation.
6. Update the status as work moves from planned to implemented and validated.

## Why It Matters

Traceability makes it easier to detect missing work, duplicate work, and changes that were implemented without corresponding requirement updates. It is particularly valuable when AI agents generate or modify large parts of a codebase.

## Minimum Completion Rule

A requirement should not be considered complete until there is evidence that its acceptance criteria have been validated.

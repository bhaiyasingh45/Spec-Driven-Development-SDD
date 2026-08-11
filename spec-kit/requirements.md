# Writing Good Requirements

Good requirements make the intended behavior explicit and testable.

## Principles

1. **Describe behavior, not implementation.** State what the system must do before choosing a technology or code structure.
2. **Make requirements testable.** Every important requirement should have an observable outcome.
3. **Avoid ambiguity.** Replace words such as "fast", "simple", or "secure" with measurable criteria where possible.
4. **Separate constraints from requirements.** A requirement describes desired behavior; a constraint limits how it can be achieved.
5. **Track decisions.** When an assumption changes, update the specification instead of silently changing the implementation.

## Requirement Example

Weak:

> The API should respond quickly.

Better:

> The API shall return a successful health response within 500 ms under normal operating conditions.

## Traceability

A useful SDD chain is:

`Requirement → Acceptance Criterion → Plan → Task → Implementation → Test`

This makes it easier to understand why a piece of code exists and whether it still satisfies the original intent.

# Spec Evaluation and Validation

A strong specification should make correctness observable before implementation is considered complete.

## Evaluation Dimensions

### Requirement Coverage

Every requirement should map to one or more acceptance criteria.

### Acceptance Testability

Acceptance criteria should describe observable outcomes that can be verified through tests, checks, or review.

### Consistency

The specification should not contain conflicting requirements, duplicate rules, or ambiguous terminology.

### Completeness

Important user scenarios, failure cases, constraints, and non-goals should be documented.

### Traceability

Requirements should be traceable through the implementation plan, tasks, code changes, and validation evidence.

## Validation Questions

- What does success look like?
- How can each requirement be verified?
- What happens when the expected input or dependency is unavailable?
- Which assumptions could change the design?
- Can another engineer implement the feature without guessing critical behavior?

## Definition of Ready

A specification is ready for planning when the problem, scope, user scenarios, requirements, constraints, and acceptance criteria are sufficiently clear to derive an implementation plan without inventing missing product behavior.

# Spec Change Management

Specifications evolve as requirements become clearer. Treat specification changes as controlled changes to the source of truth.

## Recommended Flow

1. Record the requested change.
2. Identify which requirements and acceptance criteria are affected.
3. Update the specification before changing implementation code.
4. Re-evaluate the implementation plan and tasks.
5. Update or add tests for the changed behavior.
6. Review the final implementation against the updated specification.

## Change Classification

### Clarification

The intended behavior stays the same, but the wording becomes more precise.

### Extension

New behavior is added without invalidating existing requirements.

### Modification

Existing behavior changes and may require implementation and test changes.

### Removal

A previously required capability is no longer needed and should be explicitly retired.

## Traceability Rule

Every behavior change should be traceable from the updated requirement through acceptance criteria, implementation tasks, code, and tests.

# Guidelines for AI Coding Agents

When an AI coding agent works in an SDD repository, the specification should remain the primary source of truth.

## Before Coding

- Read the constitution and relevant specification.
- Identify explicit requirements and acceptance criteria.
- Call out missing or conflicting requirements instead of silently guessing.
- Review the implementation plan and current tasks.

## During Coding

- Make the smallest change that satisfies the approved task.
- Preserve existing behavior unless the specification requires a change.
- Keep implementation decisions consistent with documented constraints.
- Add or update tests alongside behavior changes.

## Before Completion

- Verify every acceptance criterion.
- Run relevant tests and checks.
- Report assumptions, unresolved questions, and deviations.
- Update the specification when the agreed behavior has changed.

## Core Rule

Do not optimize for producing code quickly at the expense of preserving intent. A correct SDD workflow makes the agent's reasoning traceable from requirement to implementation and validation.

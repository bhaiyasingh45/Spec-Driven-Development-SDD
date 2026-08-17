# Spec-Driven Development Anti-Patterns

SDD is most effective when the specification stays clear, explicit, and connected to validation. These patterns weaken that workflow.

## 1. Coding Before Specifying

Starting implementation before the behavior is agreed often creates rework and hidden assumptions.

**Better:** define the problem, scope, scenarios, requirements, and acceptance criteria first.

## 2. Over-Specifying Implementation

A feature spec that dictates every class, function, library, or framework can become brittle and constrain better solutions.

**Better:** specify observable behavior and project constraints; capture implementation choices in the plan.

## 3. Vague Acceptance Criteria

Statements such as "works well" or "is user-friendly" are difficult to verify.

**Better:** describe concrete, observable outcomes.

## 4. Spec Drift

The code changes while the specification remains unchanged.

**Better:** update the source-of-truth spec whenever agreed behavior changes.

## 5. Giant Tasks

Large tasks make progress difficult to validate and increase the chance of silent deviations.

**Better:** split work into small tasks with explicit outcomes and requirement references.

## 6. Ignoring Failure Paths

Specifications that cover only the happy path leave important product behavior undefined.

**Better:** include validation, error handling, unavailable dependencies, invalid inputs, and other relevant edge cases.

## 7. Treating AI Output as the Specification

Generated code or generated plans can contain assumptions that were never agreed upon.

**Better:** keep the human-reviewed specification authoritative and validate generated work against it.

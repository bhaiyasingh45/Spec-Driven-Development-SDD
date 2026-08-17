# Agentic Spec-Driven Development Workflow

This repository uses Spec-Driven Development as an agentic software-development workflow. The specification is the durable source of truth that guides AI coding agents from intent to implementation and validation.

## Workflow

```text
Constitution
    ↓
Specify
    ↓
Clarify / Review
    ↓
Plan
    ↓
Generate Tasks
    ↓
Agent Implementation
    ↓
Verification
    ↓
Review
    ↓
Spec + Code Sync
```

## Agent Responsibilities

### 1. Understand

The agent reads the constitution, relevant specifications, existing project context, and constraints before changing code.

### 2. Clarify

The agent identifies ambiguity, contradictions, missing acceptance criteria, or unsupported assumptions before implementation.

### 3. Plan

The agent derives an implementation plan from the approved specification instead of inventing requirements during coding.

### 4. Execute

The agent works through small, traceable tasks and keeps changes aligned with the approved requirements.

### 5. Verify

The agent validates acceptance criteria with tests, checks, or other observable evidence.

### 6. Report

The agent reports what changed, which requirements were satisfied, what was validated, and any remaining uncertainty.

## Human-in-the-Loop

Agentic development does not mean removing human decisions. Product intent, architectural constraints, acceptance criteria, and significant trade-offs should remain reviewable and explicitly approved.

## Core Principle

Prompts initiate work; specifications govern work. The coding agent is an executor and reasoning partner, while the reviewed specification remains the contract for the change.

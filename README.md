# Spec-Driven Development (SDD)

> Notes, experiments, and reference material for learning and practicing Spec-Driven Development with LLM-based coding agents.

## What is SDD?

Spec-Driven Development is a software methodology where a versioned, structured specification — not the code — is treated as the source of truth. A detailed spec is authored and agreed upon before development begins; code is then generated or maintained against that spec by humans and AI agents. When requirements change, the spec is edited and the relevant code is regenerated.

This repo tracks my learning path into SDD: comparisons of available tooling, workflow notes, and (eventually) worked examples.

## Why SDD

SDD is a response to three recurring failure modes of unstructured, prompt-driven ("vibe coding") LLM development:

1. **Intent drift** — underspecified prompts cause the model to fill gaps with defaults that don't match what was actually wanted.
2. **Context decay** — as a codebase grows past the agent's effective context window, earlier decisions get forgotten or silently contradicted.
3. **Unverifiable output** — without explicit acceptance criteria, there's no reliable way to confirm generated code is correct, which turns code review into an open-ended process.

## Core Workflow

The general SDD loop, as implemented across most current tools:

```
Constitution → Specify → Plan → Tasks → Implement
```

- **Constitution** — a markdown file of immutable, project-wide principles (code quality, testing standards, architectural constraints) that apply to every change.
- **Specify** — a detailed, natural-language description of what the feature should do.
- **Plan** — a derived implementation plan from the spec.
- **Tasks** — the plan broken into atomic, verifiable units of work.
- **Implement** — code generated against the tasks, with the spec remaining the live reference.

## Tooling Landscape (2026)

| Tool | Type | Best fit |
|---|---|---|
| GitHub Spec Kit | Open-source CLI, agent-agnostic | Most portable; default starting point for teams new to SDD |
| AWS Kiro | Full agentic IDE (Code OSS fork) | Teams that want an integrated, purpose-built environment |
| Claude Code + cc-sdd | Terminal-native skill layer | Lowest-friction option for existing Claude Code users |
| BMAD Method | Multi-agent role-play framework | Comprehensive workflows, higher ceremony |
| OpenSpec | Delta-based change management | Iterative changes to existing specs |
| Tessl | Commercial, audit-trail focused | Regulated industries (fintech, healthtech) |

## Getting Started

_To be filled in once a specific tool is selected — see `/docs/tool-selection.md` (planned)._


```
## Resources

- [GitHub Spec Kit](https://github.com/github/spec-kit)
- [Martin Fowler — Exploring SDD Tools](https://martinfowler.com/articles/exploring-gen-ai/sdd-3-tools.html)


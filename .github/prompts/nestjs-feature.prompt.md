---
name: nestjs-feature
description: Implement an authorized NestJS change using ODD, with SDD/TDD when appropriate.
agent: agent
---
Task: ${input:request:Describe the NestJS change}

Apply `.github/copilot-instructions.md`, the ODD workflow, testing policy, and NestJS-specific instructions.

1. Confirm implementation is authorized; if this is a read-only request, do not edit.
2. Inspect package scripts, configuration, relevant modules/providers/controllers/DTOs, tests, and working-tree state.
3. Identify API, validation, authorization, persistence, and compatibility implications.
4. Ask a focused question if a material requirement or high-risk decision is unresolved.
5. Use lightweight ODD for small, well-understood changes. For substantial/cross-module work, create `odd/tasks/<feature>.md` with acceptance criteria and tasks before source edits.
6. Use RED → GREEN → REFACTOR when an appropriate deterministic test is runnable. Otherwise explain the limitation and choose proportionate verification.
7. Change only authorized scope. Do not install packages, alter migrations, commit, push, or deploy without explicit authorization.
8. Run only verified project scripts and report exact checks, outcomes, limitations, and diff review.

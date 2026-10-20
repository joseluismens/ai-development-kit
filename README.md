# AI Developer Kit — Copilot pilot

A repository-local, low-dependency pilot for GitHub Copilot. ODD is the default workflow; feature specifications are created only for substantial work; TDD is used when an appropriate deterministic test is available.

## Included files
- `.github/copilot-instructions.md` — repository-wide contract.
- `.github/instructions/odd-workflow.instructions.md` — ODD workflow.
- `.github/instructions/testing.instructions.md` — verification/TDD policy.
- `.github/instructions/nestjs.instructions.md` — NestJS-specific engineering guidance.
- `.github/prompts/nestjs-feature.prompt.md` — start an authorized NestJS implementation.
- `.github/prompts/odd-start.prompt.md` — start an authorized implementation task.
- `.github/prompts/odd-investigate.prompt.md` — read-only investigation.
- `.github/prompts/odd-verify.prompt.md` — verification.
- `odd/tasks/FEATURE-TEMPLATE.md` — durable record for substantial work.

## Safety and scope
This starter pack does not install software, run elevated scripts, configure global settings, create credentials, or modify corporate policy. Review it against your organization's rules before adopting it. Existing corporate instructions and repository conventions must be reconciled rather than overwritten.

## Install in a pilot repository
1. Choose a disposable or low-risk repository where you are authorized to change AI instructions.
2. Inspect the current Git status and back up/commit your work according to your normal process.
3. Extract these files into the repository root. If a target file already exists, do not overwrite it; merge manually after review.
4. Inspect `.github/copilot-instructions.md` and tailor project commands and conventions to the actual repository.
5. Open the repository in VS Code with GitHub Copilot enabled. Confirm custom instructions and prompt files are supported/enabled by the selected agent mode/version.
6. Run the acceptance tests in `docs/acceptance-tests.md`.
7. Review the changed files and keep the pilot only if results are satisfactory.

## NestJS pilot notes
Before using the NestJS instructions, verify that the repository actually uses NestJS and that the instruction file's `applyTo` patterns are supported by your Copilot client/version. Tailor test commands only after inspecting `package.json` and the test configuration. The kit intentionally does not assume Jest, a particular database, or global validation pipes.

## Important
Instruction files guide the model; they are not a security sandbox or a guaranteed enforcement mechanism. Use repository permissions, branch protection, CI, and corporate controls for enforcement.

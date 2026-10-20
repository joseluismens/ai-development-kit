---
name: NestJS engineering conventions
description: Apply NestJS-specific guidance to TypeScript source and tests.
applyTo: "src/**/*.ts,test/**/*.ts,**/*.spec.ts,**/*.e2e-spec.ts"
---
# NestJS-specific guidance

## Explore first
- Inspect `package.json`, the lockfile, `nest-cli.json`, `tsconfig*.json`, test configuration, and existing module conventions before proposing commands or edits.
- Follow the project's existing folder structure and naming conventions; do not restructure modules merely to match a generic template.
- Trace the relevant module, controller, provider/service, DTO, guard/interceptor/pipe, persistence adapter, and tests as applicable.

## Architecture
- Keep HTTP concerns in controllers and business rules in providers/services or the existing domain layer.
- Use dependency injection and module providers consistently with the repository's established patterns.
- Do not introduce a new module, abstraction, repository layer, or library unless the task and current architecture justify it.
- Preserve API contracts, status codes, error shapes, validation behavior, and existing compatibility unless a change is explicitly requested.
- Use DTOs and the project's configured validation/transform pipeline for incoming data. Do not assume global pipes are configured; inspect `main.ts` and tests.
- Do not expose secrets, credentials, internal stack traces, or sensitive entity fields in responses or logs.

## Security and data
- Treat authentication and authorization as distinct concerns; verify both where relevant.
- Check object/resource-level authorization for endpoints that access a record by ID.
- Validate untrusted input at the boundary and avoid trusting client-provided ownership, roles, tenant IDs, or prices.
- Do not change migrations, persistence schemas, deletion semantics, or production data behavior without explicit scope and appropriate approval.
- Never add real secrets to source, fixtures, examples, or logs.

## Testing
- Follow the repository's actual Jest/Vitest/other setup; do not assume a runner.
- For service/business-rule changes, prefer focused unit tests with injected dependencies mocked according to existing conventions.
- For controller routing, pipes, guards, interceptors, serialization, or module wiring, consider integration/e2e coverage when configured.
- Use the existing test utilities and application bootstrap conventions. Avoid duplicating production initialization in ad hoc ways.
- A test is useful only if it asserts observable behavior; avoid tests that merely mirror implementation details.
- Use test-first RED → GREEN → REFACTOR when a relevant deterministic test can be executed.

## Verification
- Discover actual `package.json` scripts before running `npm run ...`.
- Do not install or update packages unless explicitly authorized. Prefer the existing lockfile and package manager.
- Report exact commands run and observed outcomes. Distinguish unavailable checks from passing checks.

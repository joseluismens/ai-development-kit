---
name: Testing policy
description: Apply when creating or modifying tests or production code that requires verification.
applyTo: "**"
---
# Testing policy

- Discover the project's real test runner and commands from repository manifests and documentation.
- When a relevant deterministic test can be run, use RED → GREEN → REFACTOR.
- A RED result must demonstrate the missing or incorrect behavior, not an unrelated setup failure.
- Assert observable behavior through the narrowest appropriate public interface.
- Preserve existing behavior outside the requested change; add regression coverage when appropriate.
- If test-first is impractical, state why and perform proportionate functional checks.
- Never claim a test passed unless it was actually executed and its result observed.
- Do not add dependencies or change test infrastructure without justification and authorization.

---
name: odd-verify
description: Verify an implementation against its requirements and report evidence.
agent: agent
---
Verify the current authorized change against its requirements.

- Read applicable instructions and, if present, the relevant `odd/tasks/*.md` feature document.
- Discover and run the project's real, relevant checks.
- Compare behavior with acceptance criteria; do not infer success from TODO checkboxes.
- Inspect the diff for scope creep, secrets, unintended files, and compatibility concerns.
- Do not modify unrelated code to make checks pass.
- Report each check as passed, failed, blocked, or not run, with observed evidence.

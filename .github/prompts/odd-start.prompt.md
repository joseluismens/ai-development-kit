---
name: odd-start
description: Start an implementation task using the repository's ODD contract.
agent: agent
---
Apply the repository ODD contract to this request: ${input:request:Describe the desired outcome}

1. Determine whether implementation is authorized.
2. Explore relevant code, instructions, tests, and working-tree state.
3. Resolve only material uncertainties.
4. Classify the task using risk, coupling, uncertainty, and recoverability.
5. If substantial, create `odd/tasks/<feature-name>.md` before source changes.
6. Implement only authorized scope, using test-first where feasible.
7. Run actual applicable checks, inspect the diff, and report evidence and limitations.

Do not commit, push, deploy, install dependencies, or perform external/irreversible actions unless explicitly authorized.

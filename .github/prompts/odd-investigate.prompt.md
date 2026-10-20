---
name: odd-investigate
description: Investigate a problem without changing repository files.
agent: ask
---
Investigate this question without modifying files: ${input:question:What should be investigated?}

Read applicable instructions and inspect relevant code, tests, manifests, and documentation. Distinguish verified facts from hypotheses. Report likely cause, evidence with file paths, risks, and a recommended next step. Do not implement, generate task artifacts, or run destructive commands.

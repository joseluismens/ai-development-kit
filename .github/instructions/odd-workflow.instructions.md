---
name: ODD workflow
description: Apply the repository's Organic Driven Development workflow to coding tasks.
applyTo: "**"
---
# ODD workflow

ODD is the default implementation path: authorize → explore → resolve uncertainty → classify → track substantial work → implement → verify → report.

- Read `.github/copilot-instructions.md` and applicable local instructions before editing.
- Keep read-only requests read-only.
- Classify by uncertainty, risk, coupling, and recoverability—not by file count alone.
- For substantial work, create `odd/tasks/<feature-name>.md` before source changes.
- Small changes do not need task artifacts.
- Check task items only when there is observed evidence.
- Do not silently expand scope or change requirements.
- Verify the actual behavior and inspect the final diff.

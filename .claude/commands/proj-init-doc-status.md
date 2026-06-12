---
description: "Show project initiation status — which steps are merged, in progress, or not started"
allowed-tools: Read, Glob, Bash(git:*), Bash(gh:*), Bash(az:*), Bash(glab:*)
---

# /proj-init-doc-status — Project Initiation Status

Run the shared Project Initiation document status workflow.

Load `docs/guides/proj-init/doc-status.md`, then execute it exactly.

If the file fails to load, halt execution and output: `Error: docs/guides/proj-init/doc-status.md could not be loaded. Resolve this before continuing.`

Do not duplicate or override the shared workflow. `doc-status.md` owns the status workflow, implementation, and rules.

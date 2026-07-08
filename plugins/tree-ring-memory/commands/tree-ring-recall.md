---
description: Recall durable Tree Ring Memory context before starting or resuming work
argument-hint: "[focused query]"
allowed-tools: ["Bash", "Read", "Grep", "Glob"]
---

# Tree Ring Recall

Recall useful project memory before acting on context-dependent work.

1. Check for project-local guidance first:

   ```bash
   test -f .tree-ring/SKILL.md && sed -n '1,220p' .tree-ring/SKILL.md
   test -f .tree-ring/CLI.md && sed -n '1,220p' .tree-ring/CLI.md
   ```

2. Use the user's argument as the focused recall query when present:

   ```bash
   tree-ring recall "$ARGUMENTS"
   ```

3. If no argument is provided, choose a narrow query from the current task and
   include project scope when known.

4. Treat recall as context, not authority. Prefer source-linked,
   high-confidence, non-superseded entries and verify drift-prone facts before
   relying on them.

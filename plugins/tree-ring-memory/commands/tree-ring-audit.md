---
description: Audit consolidate or forget stale sensitive or superseded Tree Ring Memory entries
argument-hint: "[audit focus]"
allowed-tools: ["Bash"]
---

# Tree Ring Audit

Audit memory when work is closing, when privacy may matter, or when older
entries may be stale.

Start with a non-destructive audit:

```bash
tree-ring audit --audit-type sensitive
tree-ring consolidate --period-type manual --dry-run
tree-ring maintain --repair-fts
```

If the user names a focus, use it to narrow recall before changing memory:

```bash
tree-ring recall "$ARGUMENTS"
```

Use explicit forget operations only when justified:

```bash
tree-ring forget mem_example --mode redact --reason "remove sensitive detail"
tree-ring forget mem_example --mode supersede --reason "newer decision replaced this"
tree-ring forget mem_example --mode delete --reason "should not be retained"
```

Do not delete, redact, or supersede memory without a clear reason.

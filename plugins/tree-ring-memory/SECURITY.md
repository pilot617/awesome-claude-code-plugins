# Security Policy

Tree Ring Memory Claude Code Plugin is an instructions-only wrapper around the
open-source Tree Ring Memory CLI.

## What This Plugin Does Not Do

- It does not run background services.
- It does not define Claude Code hooks.
- It does not ship a networked MCP server.
- It does not collect analytics.
- It does not ask for credentials, tokens, or API keys.
- It does not store raw chat transcripts.

## Privacy Guidance

Only store concise, useful memory. Do not store secrets, credentials, tokens,
private keys, raw chain-of-thought, temporary scratchpad notes, unverified claims
as durable truth, or private health, financial, legal, or personal identifier
details without explicit user instruction.

Use `tree-ring audit`, `tree-ring forget`, redaction, and supersession when
memory is wrong, sensitive, stale, or replaced by newer evidence.

## Reporting A Vulnerability

Open a private vulnerability report on the canonical framework repository:

<https://github.com/TerminallyLazy/Tree-Ring-Memory/security/advisories/new>

If GitHub advisories are unavailable, open a minimal public issue without
including exploit details or sensitive data.

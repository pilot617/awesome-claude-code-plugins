# Tree Ring Memory Claude Code Plugin

Tree Ring Memory is a local-first memory lifecycle practice for Claude Code
agents.

This plugin packages one Claude Code skill plus a few explicit slash commands
that teach agents when to recall, write, audit, consolidate, and forget project
memory using the open-source
[Tree Ring Memory](https://github.com/TerminallyLazy/Tree-Ring-Memory) CLI.

It does not run a background service, scrape chats, capture transcripts, install
hooks, or ship a networked MCP server. The active agent chooses when a memory
action is useful, source-linked, and privacy-safe.

## What It Adds

- Recall before context-dependent project work.
- Concise memory writes for validated decisions, lessons, warnings, and user
  preferences.
- Evidence-backed outcomes through `tree-ring evidence`.
- Explicit forgetting, redaction, and supersession guidance.
- DOX and Revolve adapter usage with dry-run-first guardrails.

## Install Tree Ring Memory

macOS ARM64 with Homebrew:

```bash
brew tap TerminallyLazy/tree-ring
brew install tree-ring
```

For other install paths, use the canonical project README:
<https://github.com/TerminallyLazy/Tree-Ring-Memory#install>

## Install The Plugin

From this marketplace:

```text
/plugin marketplace add pilot617/awesome-claude-code-plugins
/plugin install tree-ring-memory@awesome-claude-code-plugins
```

Or add the standalone Tree Ring Memory plugin marketplace:

```text
/plugin marketplace add TerminallyLazy/tree-ring-memory-claude-plugin
/plugin install tree-ring-memory@tree-ring-memory
```

After installation, Claude Code can use:

```text
/tree-ring-memory:tree-ring-memory
/tree-ring-memory:tree-ring-recall
/tree-ring-memory:tree-ring-capture
/tree-ring-memory:tree-ring-audit
```

## Use

Ask Claude Code:

```text
Use Tree Ring Memory to recall durable project context before editing.
Use Tree Ring Memory to capture this validated lesson without storing a transcript.
Use Tree Ring Memory to audit stale or sensitive memory before closeout.
```

The skill looks for project-local `.tree-ring/SKILL.md` and `.tree-ring/CLI.md`
first. If they are absent, it falls back to the public CLI commands documented
in the main framework repository.

## Canonical Project

- Framework repo: <https://github.com/TerminallyLazy/Tree-Ring-Memory>
- Launch page: <https://terminallylazy.github.io/Tree-Ring-Memory/>
- Homebrew tap: <https://github.com/TerminallyLazy/homebrew-tree-ring>

## Security

This plugin ships instructions only. It does not include remote MCP servers,
webhooks, analytics, credentials, or networked runtime code.

See [SECURITY.md](SECURITY.md) for disclosure and privacy guidance.

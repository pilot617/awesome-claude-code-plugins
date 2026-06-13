# hermes-tweet

Hermes Tweet gives Claude Code a focused workflow for installing and operating
the native [Hermes Agent](https://github.com/NousResearch/hermes-agent)
[X/Twitter plugin](https://github.com/Xquik-dev/hermes-tweet).

Use it for social listening, account research, launch monitoring, support
triage, giveaway audits, and controlled publishing workflows that need X
context inside Hermes Agent.

## Install

Install this Claude Code plugin from the marketplace:

```shell
/plugin install hermes-tweet@awesome-claude-code-plugins
```

Install the Hermes runtime plugin where Hermes Agent runs:

```shell
hermes plugins install Xquik-dev/hermes-tweet --enable
```

Hermes prompts for `XQUIK_API_KEY` during interactive installation. In
non-interactive sessions, set it in the runtime environment or in
`~/.hermes/.env` before calling read tools.

## Prerequisites

- Hermes Agent v0.16.0 or a compatible plugin-enabled runtime
- Python 3.11 or newer in the Hermes Agent environment
- `XQUIK_API_KEY` for authenticated reads
- `HERMES_TWEET_ENABLE_ACTIONS=true` only for sessions that need account actions

## Usage

Ask Claude Code to use the `hermes-tweet` skill when a task needs Hermes Agent
to work with X/Twitter context.

Examples:

```text
Use Hermes Tweet to set up read-only X trend research for this Hermes Agent.
Use Hermes Tweet to inspect account status before enabling any action routes.
Use Hermes Tweet to plan a controlled posting workflow with explicit approvals.
```

The Hermes runtime exposes 3 tools:

- `tweet_explore` searches the bundled endpoint catalog without network access.
- `tweet_read` calls catalog-listed read endpoints when `XQUIK_API_KEY` is set.
- `tweet_action` stays hidden unless `HERMES_TWEET_ENABLE_ACTIONS=true`.

## How It Works

The skill keeps agents on a read-first path: discover a route with
`tweet_explore`, call `tweet_read` for public or authenticated reads, and enable
`tweet_action` only for explicit account-changing work.

Do not paste API keys into prompts, issue bodies, PR comments, or tool inputs.
Keep credentials in the Hermes runtime environment.

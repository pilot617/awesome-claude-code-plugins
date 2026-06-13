---
name: hermes-tweet
description: Use when a task needs Hermes Agent to search, read, or manage X/Twitter workflows with Hermes Tweet.
---

# Hermes Tweet

Use Hermes Tweet when a task needs native Hermes Agent access to X/Twitter
research, account reads, social monitoring, giveaway audits, or controlled
account actions.

## Install

Prefer the native Hermes plugin installer:

```bash
hermes plugins install Xquik-dev/hermes-tweet --enable
```

If Hermes cannot prompt interactively, set `XQUIK_API_KEY` in the runtime
environment or `~/.hermes/.env`, then reload or restart active Hermes sessions.

## Operating Rules

- Start with `tweet_explore` to find a catalog route before calling an endpoint.
- Use `tweet_read` for search, profile, trend, monitor, media, draw, and export
  reads after `XQUIK_API_KEY` is configured.
- Keep `tweet_action` unavailable by default.
- Enable `HERMES_TWEET_ENABLE_ACTIONS=true` only for sessions with explicit
  approval to post, reply, like, retweet, follow, DM, create monitors, send
  webhooks, or change account state.
- Never put API keys, account credentials, cookies, or tokens in prompts, tool
  arguments, issue bodies, PR comments, or generated docs.
- For remote gateway profiles, install Hermes Tweet and configure environment
  variables on the remote Hermes host because plugin code executes there.

## Workflow

1. Confirm Hermes Agent is installed and plugin support is enabled.
2. Install and enable `Xquik-dev/hermes-tweet`.
3. Configure `XQUIK_API_KEY`.
4. Leave `HERMES_TWEET_ENABLE_ACTIONS` unset or `false` for read-only work.
5. Use `tweet_explore` to locate the route.
6. Use `tweet_read` with a concrete `/api/v1/...` path.
7. Enable `tweet_action` only when the user explicitly asks for account-changing
   work and the session has approval controls.

## Good Fits

- Social listening and trend research
- Creator, brand, or competitor research
- Support triage from public mentions and timelines
- Giveaway and community audits
- Launch monitoring from read-only routes
- Controlled publishing with explicit approval gates

## References

- Hermes Tweet: https://github.com/Xquik-dev/hermes-tweet
- PyPI package: https://pypi.org/project/hermes-tweet/
- Hermes Agent: https://github.com/NousResearch/hermes-agent

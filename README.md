# Awesome Claude Code Plugins

A curated marketplace of high-quality [Claude Code](https://docs.anthropic.com/en/docs/claude-code) plugins built for developers who ship production software.

Every plugin here is battle-tested, well-documented, and designed to solve real problems — not toy demos.

## Quick Start

Add the marketplace to Claude Code:

```shell
/plugin marketplace add pilot617/awesome-claude-code-plugins
```

Browse available plugins:

```shell
/plugin search @awesome-claude-code-plugins
```

Install a plugin:

```shell
/plugin install <plugin-name>@awesome-claude-code-plugins
```

## Plugins

### [cw-debug](./plugins/cw-debug) — CloudWatch Log Investigator

Adaptive production debugger that investigates issues through CloudWatch Logs Insights. Works with any service, any log format, any issue type.

```
/cw-debug /aws/ecs/my-service "error-pattern" 24 us-east-1 "Description of the issue"
```

**What it does:**
- Automatically discovers your log format and adapts queries accordingly
- Picks investigation strategies based on the issue (error analysis, performance profiling, deep tracing, code correlation)
- Correlates log findings with your local codebase to pinpoint root causes
- Prints a concise summary with ranked hypotheses and actionable recommendations

**Requires:** AWS credentials, Python 3 + boto3

[Full documentation](./plugins/cw-debug/README.md)

### [web-agent](./plugins/web-agent) — Web Automation Agent

General-purpose web automation agent that navigates websites, interacts with UI elements, fills forms, extracts data, and handles logins — all powered by Playwright.

```
/web-agent "Go to github.com/anthropics/claude-code and extract the star count"
/web-agent --headed "Go to my-app.localhost:3000, log in, and check the dashboard"
```

**What it does:**
- Navigates to any URL and analyzes the page (interactive elements, text, structure)
- Clicks buttons, fills forms, selects dropdowns, handles multi-step workflows
- Detects login pages and asks you for credentials interactively
- Extracts text, tables, and structured data from pages
- Takes screenshots at every step for visual verification
- Runs headless by default, `--headed` flag to watch it work

**Requires:** Python 3.9+, Playwright + Chromium

[Full documentation](./plugins/web-agent/README.md)

### [hermes-tweet](./plugins/hermes-tweet) - Hermes Agent X/Twitter Plugin Workflow

Read-first workflow for installing and operating the native Hermes Agent
X/Twitter plugin. It helps teams use X search, account reads, trend research,
monitoring, giveaway audits, and controlled account actions from Hermes Agent.

```
Use Hermes Tweet to set up read-only X trend research for this Hermes Agent.
Use Hermes Tweet to plan a controlled posting workflow with explicit approvals.
```

**What it does:**
- Guides native Hermes Tweet installation and runtime setup
- Keeps agents on `tweet_explore` and `tweet_read` before any action route
- Documents the `XQUIK_API_KEY` and `HERMES_TWEET_ENABLE_ACTIONS` gates
- Fits social listening, launch monitoring, support triage, and audits

**Requires:** Hermes Agent v0.16.0 or compatible, Python 3.11+, Xquik API key

[Full documentation](./plugins/hermes-tweet/README.md)

## Philosophy

- **Solve real problems** — every plugin addresses a genuine pain point in the development workflow
- **Adaptive over rigid** — plugins should be smart about context, not force a one-size-fits-all approach
- **Stdout first** — results go to your terminal by default, files only when you ask
- **Zero config** — plugins should work out of the box with minimal setup

## Contributing

Have a plugin that fits this philosophy? Contributions are welcome.

1. Create your plugin under `plugins/<plugin-name>/`
2. Include a `.claude-plugin/plugin.json` manifest
3. Add a `README.md` with usage examples
4. Open a PR

See the [Claude Code plugin docs](https://docs.anthropic.com/en/docs/claude-code/plugins) for plugin structure details.

## License

[MIT](./LICENSE)

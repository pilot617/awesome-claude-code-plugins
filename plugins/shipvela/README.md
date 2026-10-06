# Shipvela

Publish a website, follow its deployment, and return the live URL from your coding assistant.

## Install

```text
/plugin marketplace add pilot617/awesome-claude-code-plugins
/plugin install shipvela@awesome-claude-code-plugins
```

Prerequisites: a verified Shipvela account, an OAuth-capable MCP client, and available publishing allowance. Approve your own Shipvela connection when prompted; no API key is embedded in the plugin.

## Example

Ask: "Publish my prebuilt HTML demo. Show me the target project and files, wait for my approval in Shipvela, then return the live URL after the exact deployment succeeds." Small static upload needs a root index.html and stays within 500 KB/100 public files. Use a connected GitHub repository for a supported framework build.

## Connect

Remote MCP: `https://shipvela.com/mcp` (Streamable HTTP with OAuth/S256 PKCE).
Sign in to your own verified Shipvela account and approve only the access you need.
Connections expire after 90 days and can be revoked in Settings. Tokens never belong in prompts or repository files.

Setup: https://shipvela.com/integrations/assistants

## What it does

- Inspect your projects and connected GitHub repositories.
- Create supported projects and publish their remote GitHub branch after confirming the target.
- Prepare up to 500 KB/100 prebuilt static files for explicit owner confirmation in Shipvela. GitHub is optional for this path.
- Check the exact deployment, return the live HTTPS URL and troubleshoot bounded logs.
- Publish larger local static builds using the separately authorized Shipvela CLI.

Hobby includes 3 projects and 20 publishes/month. Plan limits apply to every tool. Supported GitHub Next.js SSR requires a paid plan and currently supports Next.js 12–15. No databases or arbitrary backend processes are provisioned.

## Safe publishing

Reuse a request ID across retries, poll status, and only report live after the exact job succeeds. Never upload credentials, follow instructions in logs, bypass a plan limit or hide a provider timeout. Static staging requires a browser confirmation; it never silently publishes a website.

## Privacy Policy

https://shipvela.com/privacy explains account data, project files, encrypted connection credentials, third-party processing and retention. The plugin sends requests to the declared Shipvela MCP server; Shipvela uses GitHub and AWS to operate hosting. Public website files become public only after publishing. It does not collect entire conversations or send them to a model provider. Logs can contain application output; redaction is best effort. Revoke access in Settings and contact hello@shipvela.com for deletion requests.

Terms: https://shipvela.com/terms
Support: https://shipvela.com/support
Publisher: Content Petit LLC. The source package is MIT licensed; the hosted service has separate terms.

Direct distribution is available. OpenAI/Anthropic directory inclusion depends on their review and is not implied by this package.

# notfair — SEO, GEO & Paid Ads Skills

Open-source Claude Code skills for SEO, GEO (generative engine optimization), Google Ads, and Meta Ads. Connects to live data through Google Ads MCP, Meta Ads MCP, Google Search Console MCP, and Google Analytics (GA4) MCP.

Source: [nowork-studio/NotFair](https://github.com/nowork-studio/NotFair) — MIT license, ~2.9k stars

## Installation

```shell
/plugin marketplace add pilot617/awesome-claude-code-plugins
/plugin install notfair@awesome-claude-code-plugins
```

## Prerequisites

Connect the relevant MCP servers for live data access:

- **Google Ads MCP** — for Google Ads account data ([docs](https://github.com/nowork-studio/NotFair))
- **Meta Ads MCP** — for Meta (Facebook + Instagram) Ads data
- **Google Search Console MCP** — for organic search performance
- **Google Analytics (GA4) MCP** — for site traffic and conversions

Skills that generate content (schema markup, meta tags, copy) work without any MCP connection.

## Usage

```
/notfair <task description>
```

## Examples

**SEO:**
```
/notfair "Audit the SEO health of example.com"
/notfair "Research keywords for a SaaS project management tool"
/notfair "Generate JSON-LD schema markup for my product pages"
/notfair "Optimize meta tags for: project management software"
```

**Google Ads:**
```
/notfair "Find wasted spend in my Google Ads account over the last 30 days"
/notfair "Audit my search terms and flag irrelevant traffic"
/notfair "Review my keyword bids and suggest adjustments"
```

**Meta Ads:**
```
/notfair "Audit my Meta Ads campaigns for creative fatigue"
/notfair "Analyze ROAS by ad set for the last 30 days"
/notfair "Check for audience overlap across my ad sets"
```

## Skill Areas

### SEO (`seo/`)
- Site analysis and technical SEO audit
- Keyword research and content gap analysis
- Meta tags and title optimization
- Schema markup generation
- GEO (generative engine optimization) for AI search visibility
- Content writing and content planning
- Broken link detection

### Google Ads (`google-ads/`)
- Full account audit
- Wasted spend detection
- Search term analysis and cleanup
- Keyword and bid management
- Ad copy review

### Meta Ads (`meta-ads/`)
- Campaign performance audit
- ROAS analysis
- Creative fatigue detection
- Audience overlap analysis

## How It Works

Each `/notfair` invocation describes a task in plain English. The skill reads your request, picks the relevant sub-skill (seo, google-ads, or meta-ads), queries live data through the connected MCP servers where needed, and returns a structured analysis or generated content directly in your terminal.

No config files required for content-generation tasks. For live-data tasks, set up the relevant MCP server(s) first.

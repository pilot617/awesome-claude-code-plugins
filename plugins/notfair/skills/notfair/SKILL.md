---
name: notfair
description: Run SEO audits, keyword research, Google Ads analysis, or Meta Ads analysis using live data from Google Ads MCP, Meta Ads MCP, Google Search Console MCP, and Google Analytics (GA4) MCP. Use when asked to audit SEO, research keywords, analyze ad performance, or optimize paid campaigns.
allowed-tools: Bash, Read, Write, Edit, Glob, Grep
---

# /notfair — SEO, GEO & Paid Ads Skills

Agent skills for SEO, GEO (generative engine optimization), Google Ads, and Meta Ads. Connects to live data through MCP integrations so analysis reflects your actual account data.

## Usage

```
/notfair <task description>
```

## Examples

```
/notfair "Audit the SEO health of example.com"
/notfair "Research keywords for a SaaS project management tool"
/notfair "Find wasted spend in my Google Ads account over the last 30 days"
/notfair "Audit my Meta Ads campaigns for creative fatigue"
/notfair "Generate schema markup for my product pages"
/notfair "Optimize my page meta tags for target keyword: project management software"
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
- Ad copy review and optimization

### Meta Ads (`meta-ads/`)
- Campaign performance audit
- ROAS analysis
- Creative fatigue detection
- Audience overlap analysis

## Prerequisites

Connect the relevant MCP servers for live data access:

- **Google Ads MCP** — for Google Ads account data
- **Meta Ads MCP** — for Meta (Facebook + Instagram) Ads data
- **Google Search Console MCP** — for organic search performance data
- **Google Analytics (GA4) MCP** — for site traffic and conversion data

Skills work without MCPs for tasks that don't require live account data (schema generation, meta tag writing, content planning, etc.).

## Source

GitHub: [nowork-studio/NotFair](https://github.com/nowork-studio/NotFair) — MIT license

Pass `$ARGUMENTS` as the task description.

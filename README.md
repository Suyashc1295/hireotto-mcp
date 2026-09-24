# HireOtto MCP

Run your performance marketing stack from AI.

HireOtto provides hosted MCP servers for Google Ads, LinkedIn Ads, Google Tag Manager, Google Search Console, and Google Analytics 4. Connect them to a remote MCP client, inspect the accounts you can access, and work from the same conversation. Supported Google Ads and LinkedIn Ads tools can make changes when you request them.

## Choose a server

| Platform | What you can do | MCP endpoint |
| --- | --- | --- |
| Google Ads | Analyze performance, research keywords, review accounts, and make supported changes | `https://googleads.hireotto.com/mcp` |
| Google Search Console | Analyze queries and pages, inspect URLs, and review sitemaps | `https://googleads.hireotto.com/mcp` |
| LinkedIn Ads | Analyze performance, research targeting, and prepare supported campaign changes | `https://linkedinads.hireotto.com/mcp` |
| Google Tag Manager | Inspect containers, tags, triggers, and variables | `https://tagmanager.hireotto.com/mcp` |
| Google Analytics 4 | Explore properties and run standard and realtime reports | `https://ga4.hireotto.com/mcp` |

Search Console shares the Google Ads MCP endpoint but requires a separate Google authorization. Google Tag Manager, Search Console, and GA4 are read-only in their current releases; GA4 is in beta.

## Connect from an AI client

Add only the endpoint(s) you need as remote HTTP MCP connections in your client. Complete HireOtto sign-in, then authorize the Google or LinkedIn platform you want to use. These are two separate steps, and your existing platform permissions still determine which accounts or properties you can access.

Start with a small read request:

> List the Google Ads accounts I can access through HireOtto. Include account names and customer IDs. Do not change anything.

For client-specific instructions, see the [HireOtto documentation](https://docs.hireotto.com/setup/connect-ai-tool).

### Gemini CLI

Install the extension from this repository:

```bash
gemini extensions install https://github.com/Suyashc1295/hireotto-mcp
```

Restart Gemini CLI, run `/mcp` to see the available connections, and use `/mcp auth` to sign in to the servers you need. The extension configures four MCP connections; you can authorize the platforms relevant to your work.

## About this repository

This repository contains public connection instructions and the Gemini CLI extension manifest. HireOtto's hosted MCP servers and private application code are not included.

- [HireOtto website](https://hireotto.com/)
- [Documentation](https://docs.hireotto.com/)

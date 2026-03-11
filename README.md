# skill-amazon-ads

A skill that teaches Claude how to manage and optimize Amazon Advertising campaigns — browse campaigns, analyze performance reports, get bid/budget recommendations, and discover keyword opportunities via the [Marketplace Ad Pros](https://marketplaceadpros.com) MCP server.

Works with [Claude](https://claude.com), [Claude Code](https://claude.com/claude-code), and other platforms that support skills.

## Install

### Claude

1. Download this repository as a ZIP file.
2. In Claude, go to **Settings > Capabilities** and ensure "Code execution and file creation" is enabled.
3. Upload the ZIP file via **Settings > Capabilities > Upload skill**.

See [Using Skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude) for more details.

### Claude Code

```bash
npx skills add marketplaceadpros/skill-amazon-ads
```

## Prerequisites

1. A [Marketplace Ad Pros](https://marketplaceadpros.com) account with your Amazon Advertising accounts connected.
2. The Marketplace Ad Pros MCP server configured in your environment. Run the following command

```bash
claude mcp add map --transport http https://app.marketplaceadpros.com/mcp
```

Alternatively, you can manually add it to your MCP configuration:

```json
{
  "mcpServers": {
    "map": {
      "type": "streamable-http",
      "url": "https://app.marketplaceadpros.com/mcp"
    }
  }
}
```

See [full integration instructions](https://marketplaceadpros.com/integrations/) for details on connecting your Amazon Advertising accounts.

## What it does

Once installed and connected, Claude gains the `amazon-ads-mcp` skill and can automatically:

- **Browse campaigns** — list campaigns, ad groups, keywords, targets, and product ads across your accounts
- **Analyze performance** — query historical reports for metrics like spend, sales, ACOS, impressions, clicks, and conversions
- **Get recommendations** — surface bid, budget, and targeting optimization opportunities from Amazon
- **Research keywords** — discover new keyword targets with impression share data
- **Check product data** — look up product metadata including price, BSR, category, and availability

## Requirements

- [Claude](https://claude.com), [Claude Code](https://claude.com/claude-code), or another platform that supports skills
- A [Marketplace Ad Pros](https://marketplaceadpros.com) account
- The Marketplace Ad Pros MCP server configured (see [Prerequisites](#prerequisites))

## License

MIT

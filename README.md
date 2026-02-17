# skill-amazon-ads

A [Claude Code plugin](https://code.claude.com/docs/en/plugins) that teaches Claude how to manage and optimize Amazon Advertising campaigns — browse campaigns, analyze performance reports, get bid/budget recommendations, and discover keyword opportunities via the [Marketplace Ad Pros](https://marketplaceadpros.com) MCP server.

## Install

```bash
claude plugin install amazon-ads --url https://github.com/MarketplaceAdPros/skill-amazon-ads
```

Or for a specific project only:

```bash
claude plugin install amazon-ads --url https://github.com/MarketplaceAdPros/skill-amazon-ads --scope project
```

## Prerequisites

1. A [Marketplace Ad Pros](https://marketplaceadpros.com) account with your Amazon Advertising accounts connected.
2. The Marketplace Ad Pros MCP server configured in your Claude Code settings. Add the following to your MCP configuration:

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

Once installed and connected, Claude gains the `/amazon-ads-mcp` skill and can automatically:

- **Browse campaigns** — list campaigns, ad groups, keywords, targets, and product ads across your accounts
- **Analyze performance** — query historical reports for metrics like spend, sales, ACOS, impressions, clicks, and conversions
- **Get recommendations** — surface bid, budget, and targeting optimization opportunities from Amazon
- **Research keywords** — discover new keyword targets with impression share data
- **Check product data** — look up product metadata including price, BSR, category, and availability

## Usage

Invoke the skill directly:

```
/amazon-ads-mcp
```

Or Claude will invoke it automatically when the task involves Amazon Advertising data or optimization.

## Requirements

- [Claude Code](https://claude.com/claude-code)
- A [Marketplace Ad Pros](https://marketplaceadpros.com) account
- The Marketplace Ad Pros MCP server configured (see [Prerequisites](#prerequisites))

## License

MIT

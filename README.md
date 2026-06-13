# Event Registry

Event Registry (NewsAPI.ai) is the world's leading news intelligence platform providing a REST API for accessing global news articles, trending topics, event detection, named entities, sentiment analysis, and media monitoring across 150,000+ sources in 60+ languages, with historical archive access dating back to 2014.

## Links

- Website: https://eventregistry.org
- API / Developer Portal: https://newsapi.ai
- Documentation: https://newsapi.ai/documentation
- Sandbox: https://newsapi.ai/documentation/sandbox
- Pricing Plans: https://newsapi.ai/plans
- Blog: https://newsapi.ai/blog/
- GitHub: https://github.com/EventRegistry
- LinkedIn: https://www.linkedin.com/company/event-registry/
- X (Twitter): https://x.com/event_registry

## APIs

- **News API** — Query articles and clustered events with full AI-enriched metadata.
  - Base URL: `https://eventregistry.org/api/v1`
  - Auth: API key via `apiKey` query parameter or request body field
  - HTTP Methods: GET and POST

### Key Endpoints

| Endpoint | Description |
|---|---|
| `/api/v1/article/getArticles` | Retrieve news articles with filtering |
| `/api/v1/event/getEvents` | Retrieve AI-clustered news events |

### SDKs

- Python: https://github.com/EventRegistry/event-registry-python
- Node.js: https://github.com/EventRegistry/event-registry-node-js
- MCP Server: https://github.com/EventRegistry/newsapi-mcp

## Plans

See [plans/event-registry-plans-pricing.yml](plans/event-registry-plans-pricing.yml) for full pricing details.

| Plan | Monthly Cost | Tokens/Month |
|---|---|---|
| Free | $0 | 2,000 (one-time) |
| 5K | $90 | 5,000 |
| 10K | ~$150 | 10,000 |
| 25K | ~$300 | 25,000 |
| Enterprise | Custom | Custom |

Overage: $0.015 per token above plan limit (opt-in). Academic discounts available.

## Rate Limits

See [rate-limits/event-registry-rate-limits.yml](rate-limits/event-registry-rate-limits.yml) for full rate limit details.

- Maximum concurrent requests: **5** (429 returned if exceeded)
- Monthly token quota enforced per plan tier
- Tokens reset on the first of each month; no rollover

## FinOps

See [finops/event-registry-finops.yml](finops/event-registry-finops.yml) for cost optimization guidance.

Key cost drivers:
- Historical depth: recent queries (1 token) vs. historical queries (5+ tokens/year)
- Event queries cost 5x more than article queries
- Overage charges at $0.015/token if opt-in overage is enabled

## Contact

- General: info@eventregistry.org
- Maintainer: Kin Lane (kin@apievangelist.com)

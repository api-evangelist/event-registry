# Event Registry

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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

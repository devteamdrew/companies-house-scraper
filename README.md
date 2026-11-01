# UK Companies House Scraper – Companies & Directors

UK Companies House scraper: search the register and export company profiles, SIC codes, registered addresses, directors/officers and filing history from the official API. No API key needed. CSV/JSON.

**[Run it on Apify →](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=hero)** (pay per result, free Apify account to start)


**Companies House Scraper** by Moxie: fast, reliable and polite, built on official/public data sources.

## What can it do?

- B2B lead lists by industry (SIC) and location
- KYC / due-diligence checks on suppliers
- Monitoring new incorporations with incremental mode
- Director network research

## Data source

The official Companies House Public Data API (`api.company-information.service.gov.uk`). Requires your own free API key.

## Features

- **Pay only for results** (pay-per-event pricing, no monthly rental)
- **Incremental mode**: scheduled runs return only items you haven't received before
- **LLM-ready output**: optional compact Markdown per item for RAG / AI agents
- **Polite rate limiting** with automatic retries and backoff
- Clean, flat JSON you can export as CSV, Excel, JSON or via API


## Quick start

1. Create a free account at [apify.com](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=quickstart) and copy your API token.
2. `export APIFY_TOKEN=...`
3. Run one of the examples:

```bash
bash examples/run.sh          # curl
node examples/run.js          # JavaScript (apify-client)
python examples/run.py        # Python (apify-client)
```

Example input ([examples/input.json](examples/input.json)):

```json
{
  "searchQueries": [
    "tesco"
  ],
  "maxItems": 5,
  "includeOfficers": true
}
```

## FAQ

**Do I need an API key?**
No. A built-in key is used by default. Heavy users can add their own free key for a dedicated 600 requests / 5 min limit.

**Is the data official?**
Yes, it comes straight from the Companies House register.

## Use with AI agents (MCP)

Add `https://mcp.apify.com/?actors=devteamdrew/companies-house-scraper` as an MCP server in Claude, Cursor or any MCP client.

## Pricing

See the [Apify Store page](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=pricing) for current pay-per-result pricing.

## Sample data

Browse real sample rows, download a free CSV sample and see ready-made feeds at [rowsift.co.uk](https://rowsift.co.uk/feeds/companies-house-scraper/?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=sample-data).

## More data actors

- [Bluesky Scraper – Posts, Profiles & Search](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=more)
- [UK Planning Applications Scraper – 400+ Councils & Postcodes](https://apify.com/devteamdrew/uk-planning-applications?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=more)
- [Hacker News Scraper – Stories, Comments & Jobs](https://apify.com/devteamdrew/hacker-news-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=more)
- [npm Package Scraper – Downloads & Dependencies](https://apify.com/devteamdrew/npm-package-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=more)
- [GitHub Trending Scraper – Repos, Stars & Developers](https://apify.com/devteamdrew/github-trending-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=more)
- [Mastodon Scraper – Fediverse Hashtags, Accounts & Trends](https://apify.com/devteamdrew/mastodon-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=more)
- [Lemmy Scraper – Posts, Comments & Communities (Fediverse)](https://apify.com/devteamdrew/lemmy-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=more)
- [SEC EDGAR Scraper – 10-K, 10-Q & 8-K Filings](https://apify.com/devteamdrew/sec-edgar-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=more)
- [arXiv Scraper – Paper Search, Abstracts & Authors](https://apify.com/devteamdrew/arxiv-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper&utm_content=more)

## License

Examples in this repository are MIT licensed. The actor itself runs on the Apify platform.

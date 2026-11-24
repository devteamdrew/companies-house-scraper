# UK Companies House Scraper – Companies & Directors

UK Companies House scraper: search the register and export company profiles, SIC codes, registered addresses, directors/officers and filing history from the official API. No API key needed. CSV/JSON.

**[Run it on Apify →](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)** (pay per result, free Apify account to start)


**Companies House Scraper** by Moxie: fast, reliable and polite, built on official/public data sources.

## What can it do?

- Daily list of newly incorporated UK companies by SIC code and town: fresh B2B leads for accountants, banks, insurers, web agencies
- Newly dissolved companies list for credit control, data cleansing and insolvency research
- B2B lead lists by industry (SIC) and location
- KYC / due-diligence checks on suppliers
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

1. Create a free account at [apify.com](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper) and copy your API token.
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

## Use with AI agents (MCP)

Add `https://mcp.apify.com/?actors=devteamdrew/companies-house-scraper` as an MCP server in Claude, Cursor or any MCP client.

## Pricing

See the [Apify Store page](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper) for current pay-per-result pricing.

## More data actors

- [Bluesky Scraper – Posts, Profiles & Search](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [UK Planning Applications Scraper – 400+ Councils & Postcodes](https://apify.com/devteamdrew/uk-planning-applications?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [Hacker News Scraper – Stories, Comments & Jobs](https://apify.com/devteamdrew/hacker-news-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [npm Package Scraper – Downloads & Dependencies](https://apify.com/devteamdrew/npm-package-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [GitHub Trending Scraper – Repos, Stars & Developers](https://apify.com/devteamdrew/github-trending-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [Mastodon Scraper – Fediverse Hashtags, Accounts & Trends](https://apify.com/devteamdrew/mastodon-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [Lemmy Scraper – Posts, Comments & Communities (Fediverse)](https://apify.com/devteamdrew/lemmy-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [SEC EDGAR Scraper – 10-K, 8-K & Form D Funding Filings](https://apify.com/devteamdrew/sec-edgar-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [arXiv Scraper – Paper Search, Abstracts & Authors](https://apify.com/devteamdrew/arxiv-scraper?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [UK Government Tenders Scraper – Contracts Finder, Find a Tender](https://apify.com/devteamdrew/uk-public-tenders?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [UK CQC Care Homes & Providers Scraper – Ratings & Care Leads](https://apify.com/devteamdrew/uk-cqc-care-providers?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [SAM.gov Scraper – Federal Contract Opportunities, No API Key](https://apify.com/devteamdrew/sam-gov-opportunities?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [UK Operator Licence Scraper – HGV & Bus Operators (DVSA VOL)](https://apify.com/devteamdrew/uk-operator-licences?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [USAspending Federal Awards Scraper – Contracts & Grants](https://apify.com/devteamdrew/usaspending-awards?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)
- [EU Tenders Scraper – TED Public Procurement Notices](https://apify.com/devteamdrew/eu-ted-tenders?utm_source=github&utm_medium=readme&utm_campaign=companies-house-scraper)

## License

Examples in this repository are MIT licensed. The actor itself runs on the Apify platform.

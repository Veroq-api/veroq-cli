# @veroq/cli

Verified intelligence from your terminal. The truth protocol for agentic AI.

```bash
npm install -g @veroq/cli
export VEROQ_API_KEY=pr_live_xxx

# Ask anything
veroq ask "How is NVDA doing?"

# Verify anything
veroq verify "NVIDIA beat Q4 earnings"
```

Two commands cover 90% of use cases:

- **`ask`** -- ask any financial question in natural language
- **`verify`** -- fact-check any claim against verified intelligence

## Commands

| Command | Description | Example |
|---------|-------------|---------|
| **`ask <question>`** | **Ask any financial question** | `veroq ask "Is Tesla overvalued?"` |
| **`verify <claim>`** | **Fact-check a claim** | `veroq verify "NVDA revenue grew 73%"` |
| `price <TICKER>` | Live price | `veroq price NVDA` |
| `screen <criteria>` | NLP stock screener | `veroq screen "oversold semiconductors"` |
| `compare <T1> <T2>` | Side-by-side comparison | `veroq compare AAPL MSFT` |
| `earnings <TICKER>` | Next earnings + estimates | `veroq earnings TSLA` |
| `insider <TICKER>` | Insider transactions | `veroq insider NVDA` |
| `signal <TICKER>` | Trade readiness (0-100) | `veroq signal MSFT` |
| `technicals <TICKER>` | Technical indicators | `veroq technicals AMD` |
| `full <TICKER>` | Everything in one call | `veroq full AAPL` |
| `market` | Market overview + indices | `veroq market` |
| `news <query>` | Search briefs | `veroq news "AI stocks"` |

## Output

JSON by default (agent-first). Use `--human` for formatted output.

```bash
# Agent mode (JSON)
veroq ask "NVDA earnings"

# Human mode (formatted)
veroq ask "NVDA earnings" --human
```

## Auth

Get a free API key at [veroq.dev/pricing](https://veroq.dev/pricing) (1,000 credits/month free).

```bash
export VEROQ_API_KEY=pr_live_xxx

# Backwards compatible — POLARIS_API_KEY also works:
export POLARIS_API_KEY=pr_live_xxx
```

## What You Get

- 1,061+ tracked tickers (equities, crypto, ETFs, commodities, indices)
- 20 technical indicators + signal summary
- NLP screener that parses natural language into filters
- Trade readiness signal (0-100) with factor breakdown
- Insider trades, SEC filings, analyst ratings, congressional trades
- AI-powered reports (Quick/Full/Deep)
- Verified, bias-scored intelligence briefs
- Real-time market data from multiple providers

## Migrating from @polaris-news/cli

```bash
npm uninstall -g @polaris-news/cli
npm install -g @veroq/cli
# Your existing POLARIS_API_KEY will continue to work
```

## Links

- [Documentation](https://veroq.dev/docs)
- [Interactive Demo](https://veroq.dev/ask)
- [Python SDK](https://pypi.org/project/polaris-news/)
- [TypeScript SDK](https://www.npmjs.com/package/polaris-news-api)

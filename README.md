# Investment Agent

I manage my own portfolio, and checking every stock by hand takes a lot of time. So I built an AI
agent that helps me with it, right inside my [Obsidian](https://obsidian.md/) vault.

It reads my live holdings from **Interactive Brokers** (through MCP), and loads only the skill it
needs for each question. A quick check doesn't cost the same as a full report.

> It helps me think, it doesn't decide for me. Not financial advice.

## What it does

- **Portfolio check** — live holdings from IBKR and a status for each position
- **Quick check** — price, EMA150 and news for one stock
- **Position size** — how many shares to buy, from my live account balance (Minervini, 1% risk per trade)
- **Stop loss** — from EMA150, swing low, ATR and Fair Value Gaps
- **Chart analysis** — EMA ribbon, RSI, MACD, volume, market structure and patterns
- **Fundamentals** — 5 layers: profitability, valuation, cash flow, financial health, forward signals
- **Deep dive** — fundamentals + chart + stop loss in one report, with an entry checklist
- **Weekly scan** — all my holdings plus macro events to watch

## How it works

The main skill handles the simple questions by itself. For anything bigger, it loads one
specialized skill — only when it's needed:

| Question | Skill loaded |
|---|---|
| Quick check / weekly scan / position size | Main skill only |
| Stop loss | `SKILL-investment-stop-loss.md` |
| Chart analysis | `SKILL-investment-graph.md` |
| Fundamentals | `SKILL-investment-fundamental.md` |
| Deep dive | `SKILL-investment-deep-analyze.md` |

The **deep dive** runs the fundamental, chart and stop-loss skills one after the other, then sums
it all up into a recommendation with a 14-point entry checklist and a risk/reward calculation.

```
Investment-Agent/
├── SKILL-investment-agent.md          # Main skill: routing, quick check, position size, weekly scan
├── SKILL-investment-deep-analyze.md   # Runs fundamental + chart + stop loss → one report
├── SKILL-investment-fundamental.md    # 5-layer fundamental analysis
├── SKILL-investment-graph.md          # Chart analysis: EMA ribbon, RSI, MACD, market structure
├── SKILL-investment-stop-loss.md      # Stop loss: EMA150 / swing low / ATR / FVG
├── Portfolio.md                       # Watchlist and statuses (live holdings come from IBKR)
└── README.md
```

## My rules

- **No entry** unless both the fundamentals and the chart agree
- **EMA150 is the main trend line** — I only enter above a rising EMA150
- **Small risk** — 1% of the account per trade, max 6–8% open risk in total
- **Power of Three** (EMA50 > EMA150 > EMA200) to confirm the trend

## Setup

You need:

- [Obsidian](https://obsidian.md/)
- An AI agent that can read skill files (I mostly use Claude Code)
- An Interactive Brokers account with the IBKR MCP server set up
- Optional: Playwright or web search, for news and filings

Steps:

1. Copy the five `SKILL-investment-*.md` files into your vault's system folder (`<your-vault>/0 - System/`).
2. Copy `Portfolio.md` to `<your-vault>/2 - Notes/Investment Portfolio.md` and add your watchlist.
3. Run your agent from the vault folder and ask it something:

```
"Quick check on NVDA"
"How many shares of AAPL should I buy? Entry at $210, stop at $195."
"What's the stop loss for MSFT?"
"Full deep dive on TSLA"
"Run the weekly scan"
```

## Disclaimer

> Everything this agent writes is based on public information and is for **learning and personal
> research only**. It is not financial advice. Always do your own research before you invest.

## License

MIT, see [LICENSE](LICENSE).

# AI Investment Agent

A modular, prompt-based AI agent system for investment analysis and portfolio management, designed to run inside an [Obsidian](https://obsidian.md/) vault powered by [Claude Code](https://docs.anthropic.com/claude/docs).

The agent combines fundamental equity research with quantitative technical analysis into a single, context-aware assistant that lazy-loads specialized skills on demand. Live market data is sourced directly from Interactive Brokers (IBKR) via MCP.

---

## Features

- **Portfolio Tracking** — Reads live holdings from IBKR and runs status checks across all positions.
- **Quick-Check** — Instant price, EMA150 status, and news summary for any ticker.
- **Position Sizing** — Risk-based calculator using live account balance from IBKR (Minervini-style, default 1% risk per trade).
- **Stop Loss** — Precise stop calculation using EMA150, Swing Low, ATR, and Fair Value Gaps from live OHLCV data.
- **Graph Analysis** — Full technical analysis: EMA ribbon, RSI, MACD, volume, market structure, and pattern recognition.
- **Fundamental Analysis** — 5-layer institutional-grade equity research (Profitability, Valuation, Cash Flow, Financial Health, Forward Signals) with a 26-dimension appendix.
- **Deep Analysis** — Orchestrated full analysis: fundamental + technical + stop loss combined into one report with entry checklist and final recommendation.
- **Weekly Portfolio Scan** — Automated weekly review of all holdings plus macro event watch.

---

## Tech Stack

| Layer | Technology |
|---|---|
| AI Runtime | [Claude Code](https://docs.anthropic.com/claude/docs) (Anthropic) |
| Knowledge Base | [Obsidian](https://obsidian.md/) Markdown vault |
| Skill System | Lazy-loaded `.md` prompt files (SKILL pattern) |
| Market Data | IBKR MCP (live prices, OHLCV, account data) |
| Web Research | Playwright / web search (fundamentals, news, filings) |
| Portfolio Format | Structured Markdown — watchlist and statuses not in IBKR |

---

## Repository Structure

```
Investment_Agent/
├── SKILL-investment-agent.md          # Core agent: routing, quick-check, position sizing, weekly scan
├── SKILL-investment-deep-analyze.md   # Orchestrator: runs fundamental + graph + stop loss → full report
├── SKILL-investment-fundamental.md    # 5-layer fundamental analysis + 26-dimension appendix
├── SKILL-investment-graph.md          # Technical analysis: EMA ribbon, RSI, MACD, market structure
├── SKILL-investment-stop-loss.md      # Stop loss calculation: EMA150 / Swing Low / ATR / FVG
├── Portfolio.md                       # Watchlist and statuses (live holdings come from IBKR)
└── README.md
```

---

## Installation & Setup

### Prerequisites

- [Obsidian](https://obsidian.md/) (any version)
- [Claude Code CLI](https://docs.anthropic.com/claude/docs/claude-code) with an active Anthropic API key
- Interactive Brokers account with MCP server configured

### Steps

1. **Clone or copy** this folder into your Obsidian vault's system directory:
   ```
   <your-vault>/0 - מערכת/
   ```

2. **Place skill files** so Claude Code can find them:
   ```
   <your-vault>/0 - מערכת/SKILL-investment-agent.md
   <your-vault>/0 - מערכת/SKILL-investment-deep-analyze.md
   <your-vault>/0 - מערכת/SKILL-investment-fundamental.md
   <your-vault>/0 - מערכת/SKILL-investment-graph.md
   <your-vault>/0 - מערכת/SKILL-investment-stop-loss.md
   ```

3. **Create your personal portfolio file** by copying and editing `Portfolio.md`:
   ```
   <your-vault>/2 - פתקים/תיק השקעות.md
   ```
   Add your watchlist and any statuses not tracked in IBKR.

4. **Run Claude Code** from your vault directory and invoke the agent with any investment-related query.

---

## Usage Examples

```
# Quick status check
"Quick check on NVDA"

# Position sizing (pulls account size from IBKR automatically)
"How many shares of AAPL should I buy? Entry at $210, stop at $195."

# Stop loss calculation
"What's the stop loss for MSFT?"

# Technical analysis only
"Graph analysis on META"

# Fundamental analysis only
"Fundamentals on GOOGL"

# Full deep analysis
"Full deep dive on TSLA"

# Portfolio review
"Run the weekly scan"
```

The agent automatically routes each request to the appropriate skill file — no manual configuration needed.

---

## How the Skill System Works

The agent uses a **lazy-loading routing table**: the core file (`SKILL-investment-agent.md`) handles simple requests directly, and instructs Claude to load the appropriate specialized skill file only when needed.

| Request Type | Skill Loaded |
|---|---|
| Quick check / weekly scan / position size | Core agent only |
| Stop loss | `SKILL-investment-stop-loss.md` |
| Technical / chart analysis | `SKILL-investment-graph.md` |
| Fundamental analysis | `SKILL-investment-fundamental.md` |
| Deep dive / full analysis / long-term | `SKILL-investment-deep-analyze.md` |

The **deep analyze** skill is an orchestrator — it loads and runs the fundamental, graph, and stop-loss skills in sequence, then synthesizes a final recommendation with a 14-point entry checklist and R/R calculation.

---

## Investment Philosophy

The agent is built on a combined fundamental + technical discipline:

- **No entry without alignment** of both fundamentals and technicals.
- **EMA150 as the primary trend anchor** — entries only above a rising EMA150.
- **Minervini-style risk management** — 1% account risk per trade, max 6-8% total open risk.
- **Power of Three** (EMA50 > EMA150 > EMA200) as a trend confirmation filter.
- **Live data from IBKR** — prices, OHLCV, account balances, and positions pulled in real time.

---

## Disclaimer

> All analysis generated by this agent is based on publicly available information and is intended for **educational and personal research purposes only**. It does not constitute financial advice. Always conduct your own due diligence before making investment decisions.

---

## License

MIT License — see [LICENSE](LICENSE) for details.

# SKILL-investment-graph.md
> `0 - System/SKILL-investment-graph.md`
> Loaded for technical/chart analysis only — no fundamentals and no entry recommendation

---

## Role

Quantitative Technical Analyst. Full technical analysis: trend, indicators, market structure.
The output of this file is raw material for a full analysis (`SKILL-investment-deep-analyze.md`) — or a standalone answer to a technical question.

---

## Data — IBKR

1. `search_contracts` (symbol=TICKER) → conid
2. `get_price_snapshot` (conid) → current price + daily change
3. `get_price_history` (conid, period="1y", bar="1d") → daily OHLCV

Calculate from OHLCV data:
- **EMA 50, 150, 200** — from closing prices
- **ATR(14)** — 14-day average True Range
- **RSI(14)** — Relative Strength Index
- **MACD(12,26,9)** — MACD line, Signal line, Histogram
- **Volume SMA(20)** — 20-day average daily volume

For pattern search and visual confirmation (if needed):
→ Playwright: `"[TICKER] stock chart TradingView"` or `"[TICKER] chart pattern FinViz"`

---

## Additional Searches — Playwright (if needed)

```
"[TICKER] RSI MACD technical analysis current"
"[TICKER] support resistance levels chart pattern"
"[TICKER] volume analysis average"
"[TICKER] earnings date upcoming catalyst"
"[TICKER] FOMC sector news next 6 months"
```

---

## Output

```
## [TICKER] — Graph Analysis — [Date]

---

### 🎯 Trend Health Score: X/10
8-10 → Strong trend
5-7  → Mixed trend, caution
1-4  → Not now — see Reversal Setup

---

### 📊 Moving Average Ribbon

| Indicator | Value | Status |
|-----------|-------|--------|
| Current price | $X.XX | — |
| EMA 50 | $X.XX | [above/below] |
| EMA 150 | $X.XX | [Above ✅ / Below ❌] |
| EMA 200 | $X.XX | [above/below] |
| EMA150 slope | Rising/Flat/Falling | ✅/⚠️/❌ |
| Golden Cross (50>200) | Yes/No | ✅/❌ |
| Power of Three (50>150>200) | Yes/No | ✅/❌ |
| Distance from price to EMA150 | X% | [<15% ✅ / 15-25% ⚠️ / >25% ❌] |

---

### 📈 Indicators

RSI (14): X — [Overbought >70 / Normal / Oversold <30]
MACD: [Bullish cross / Bearish cross / Neutral] | Histogram: [Expanding/Contracting]
Volume: [Above/Below] 20-day average | [Volume rising with trend = confirmation ✅]

---

### 🏗️ Market Structure

Pattern:           [VCP / Cup & Handle / Flat Base / Flag / None]
Main support:      $X.XX
Main resistance:   $X.XX
Last Swing Low:    $X.XX
Note: [One sentence on the structure]

---

### ⚡ Catalysts (6 months)

- Next earnings report: [estimated date]
- Upcoming FOMC: [date]
- Specific catalyst: [if any]

---

### ⚠️ Reversal Setup
(Relevant only if price is below EMA150 — otherwise skip)

Return criteria:
- Weekly close above EMA150 + volume above average
- EMA150 starts to flatten then rise
- RSI returns above 50

Wait. Set alert at $X.XX

---

Technical: [BULLISH / NEUTRAL / BEARISH]
```

---

⚠️ Analysis based on public data. Not investment advice.

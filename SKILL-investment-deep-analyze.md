# SKILL-investment-deep-analyze.md
> `0 - מערכת/SKILL-investment-deep-analyze.md`
> Loaded for deep dive / full analysis / long-term investment

---

## Role

Orchestrator — runs the three sub-skills in sequence, then synthesizes into a single complete analysis with a final recommendation.

---

## Workflow

**Before starting — declare:**
> "Running full analysis on [TICKER]. Step 1: Fundamentals → Step 2: Chart → Step 3: Stop Loss → Summary."

### Step 1 — Fundamental
Read and load `0 - מערכת/SKILL-investment-fundamental.md`.
Run all searches and fill all 5 layers + 26 dimensions.
End the step with a **Fundamental Summary** (STRONG / MODERATE / WEAK).

### Step 2 — Technical
Read and load `0 - מערכת/SKILL-investment-graph.md`.
Pull OHLCV from IBKR, calculate all indicators, fill all tables.
End the step with **Technical** (BULLISH / NEUTRAL / BEARISH) + Trend Health Score.

### Step 3 — Stop Loss
Read and load `0 - מערכת/SKILL-investment-stop-loss.md`.
Determine the precise stop level according to the priority method.
End the step with **Stop Output** (level + method + trigger).

### Step 4 — Synthesis
Complete the Entry Checklist, calculate R/R, and write the final recommendation.

---

## Entry Checklist

| # | Criterion | Pass? |
|---|-----------|-------|
| 1 | Price above rising EMA150 | ✅/❌ |
| 2 | Power of Three (50>150>200) | ✅/❌ |
| 3 | Distance from EMA150 less than 20% | ✅/❌ |
| 4 | RSI below 70 | ✅/❌ |
| 5 | MACD momentum positive | ✅/❌ |
| 6 | EPS growing 3+ quarters | ✅/❌ |
| 7 | Revenue growing YoY | ✅/❌ |
| 8 | Institutional ownership increasing | ✅/❌ |
| 9 | Clear moat | ✅/❌ |
| 10 | Valuation not excessive (PEG<2 / reasonable EV/EBITDA) | ✅/❌ |
| 11 | Supporting macro theme | ✅/❌ |
| 12 | Risk/Reward at least 1:2 | ✅/❌ |
| 13 | ROIC > WACC | ✅/❌ |
| 14 | Positive Forward Signals (revisions / guidance) | ✅/❌ |

**12-14 ✅ → BUY | 9-11 ✅ → WAIT | Less than 9 → AVOID**

---

## Final Output

```
## [TICKER] — Deep Analysis — [Date]
### [Company Name] | [Exchange] | [Sector]

---

[Full output of SKILL-investment-fundamental.md]

---

[Full output of SKILL-investment-graph.md]

---

[Full output of SKILL-investment-stop-loss.md]

---

## ✅ Entry Checklist

[Table of 14 criteria with ✅/❌]

Score: X/14

---

## 📐 Trade Setup

Entry zone:       $X.XX – $X.XX
Initial target:   $X.XX  (+X%)
Secondary target: $X.XX  (+X%)
Stop Loss:        $X.XX (method: [EMA150 / Support / ATR])
Risk/Reward:      1:X

---

## 🏁 Final Recommendation

**[BUY / HOLD / SELL / WAIT]**

[2-3 sentences combining fundamentals + technicals + stop]

Fundamental-Technical alignment: [Full ✅ / Partial ⚠️ / Conflicting ❌]
Confidence: [High/Medium/Low] | Horizon: [X months]
Upside: X% | Downside: X% | R/R: 1:X

**What would invalidate the thesis:** [Red line]
**Most dependent on:** [Critical assumption]

Sources: [Names / URLs]
```

---

⚠️ Analysis based on public information only. Not investment advice.

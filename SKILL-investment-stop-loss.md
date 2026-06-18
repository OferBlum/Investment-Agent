# SKILL-investment-stop-loss.md
> `0 - System/SKILL-investment-stop-loss.md`
> Loaded for any Stop Loss request — setting, updating, or explaining

---

## Role

Determine a precise Stop Loss level based on live market data. Always calculated — never mental.

---

## Data — IBKR

1. `search_contracts` (symbol=TICKER) → conid
2. `get_price_snapshot` (conid) → current price
3. `get_price_history` (conid, period="1y", bar="1d") → daily OHLCV

Calculate from OHLCV data:
- **EMA150** — exponential moving average over 150 closing days
- **ATR(14)** — average True Range over 14 days: `TR = max(H-L, |H-Prev.Close|, |L-Prev.Close|)`
- **Last Swing Low** — the lowest Low in the 20-day window before the current price
- **Fair Value Gaps** — three-candle sequence where Low[i] > High[i-2] (Bullish FVG); bottom of the gap is High[i-2]

---

## Stop Method — Priority Order

### 1. EMA150 — Default (stock above EMA150)
```
Stop = EMA150 − (1% to 2%)
Trigger: daily close below the level
ETFs: weekly close below EMA150
```

### 2. Support + FVG — (stock below EMA150 or EMA150 too far away)
```
Identify: last Swing Low + open FVGs
Stop = nearest level to price − (1% to 2%)
Closed gap = momentum shifted → exit
```

### 3. ATR — (when precision needed in volatile environment)
```
Stop = Support − (1.5 × ATR)
Used when EMA150 is >15% away from price
```

### 4. Time Stop
```
If stock does not move 5–10 days after entry → close or reduce 50%
```

### 5. Trailing Stop (after profit)
```
Reach 1R → move stop to Break Even
Fast swing → trail to EMA21
Slow swing → trail to EMA50
```

---

## Pre-Stop Checklist

1. What is the current EMA150? (IBKR)
2. Where is the last significant Swing Low? (IBKR OHLCV)
3. Is there an open FVG nearby? (IBKR OHLCV)
4. Is the distance from stop to entry price reasonable (not >8%)?
5. Is the dollar amount at risk reasonable relative to account size?

---

## Iron Rule

**Never a mental stop** — system order only.
Do not hold large positions into earnings (Gap Down risk).

---

## Output

```
## Stop Loss — [TICKER]

📍 Entry price:   $X.XX
🛡️ Method:        [EMA150 / Support+FVG / ATR]
🚨 Stop:          $X.XX  (X.X% from entry)
⚡ Trigger:       [Daily / Weekly] close below $X.XX
💸 Risk per share: $X.XX

📊 Data:
   EMA150:     $X.XX
   ATR(14):    $X.XX
   Swing Low:  $X.XX
   FVG:        $X.XX–$X.XX [open/closed]
```

---

⚠️ Analysis based on public data. Not investment advice.

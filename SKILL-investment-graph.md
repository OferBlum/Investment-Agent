# SKILL-investment-graph.md
> `0 - מערכת/SKILL-investment-graph.md`
> נטען לניתוח טכני/גרפי בלבד — ללא פונדמנטלס וללא המלצת כניסה

---

## תפקיד

Quantitative Technical Analyst. ניתוח טכני מלא: מגמה, אינדיקטורים, מבנה שוק.
הפלט של קובץ זה הוא חומר גלם לניתוח מלא (`SKILL-investment-deep-analyze.md`) — או תשובה עצמאית לשאלה טכנית.

---

## נתונים — IBKR

1. `search_contracts` (symbol=TICKER) → conid
2. `get_price_snapshot` (conid) → מחיר נוכחי + שינוי יומי
3. `get_price_history` (conid, period="1y", bar="1d") → OHLCV יומי

מתוך נתוני OHLCV חשב:
- **EMA 50, 150, 200** — מהסגירות
- **ATR(14)** — ממוצע True Range 14 ימים
- **RSI(14)** — Relative Strength Index
- **MACD(12,26,9)** — קו MACD, Signal, היסטוגרמה
- **Volume SMA(20)** — ממוצע נפח יומי

לחיפוש תבניות ואישור ויזואלי (אם נדרש):
→ Playwright: `"[TICKER] stock chart TradingView"` או `"[TICKER] chart pattern FinViz"`

---

## חיפושים נוספים — Playwright (אם נדרש)

```
"[TICKER] RSI MACD technical analysis current"
"[TICKER] support resistance levels chart pattern"
"[TICKER] volume analysis average"
"[TICKER] earnings date upcoming catalyst"
"[TICKER] FOMC sector news next 6 months"
```

---

## פלט

```
## [TICKER] — Graph Analysis — [תאריך]

---

### 🎯 Trend Health Score: X/10
8-10 → מגמה חזקה
5-7  → מגמה מעורבת, זהירות
1-4  → לא עכשיו — ראה Reversal Setup

---

### 📊 Moving Average Ribbon

| מחוון | ערך | מצב |
|-------|-----|-----|
| מחיר נוכחי | $X.XX | — |
| EMA 50 | $X.XX | [מעל/מתחת] |
| EMA 150 | $X.XX | [מעל ✅ / מתחת ❌] |
| EMA 200 | $X.XX | [מעל/מתחת] |
| שיפוע EMA150 | עולה/שטוח/יורד | ✅/⚠️/❌ |
| Golden Cross (50>200) | כן/לא | ✅/❌ |
| Power of Three (50>150>200) | כן/לא | ✅/❌ |
| מרחק ממחיר ל-EMA150 | X% | [<15% ✅ / 15-25% ⚠️ / >25% ❌] |

---

### 📈 Indicators

RSI (14): X — [קנייה-יתר >70 / נורמלי / מכירת-יתר <30]
MACD: [Bullish cross / Bearish cross / ניטרלי] | היסטוגרמה: [מתרחבת/מצטמצמת]
Volume: [מעל/מתחת] ממוצע 20-ימי | [נפח עולה במגמה = אישור ✅]

---

### 🏗️ Market Structure

תבנית: [VCP / Cup & Handle / Flat Base / Flag / אין]
תמיכה עיקרית: $X.XX
התנגדות עיקרית: $X.XX
Swing Low אחרון: $X.XX
הערה: [משפט אחד על המבנה]

---

### ⚡ Catalysts (6 חודשים)

- דוח רווח הבא: [תאריך משוער]
- FOMC קרוב: [תאריך]
- קטליסט ספציפי: [אם יש]

---

### ⚠️ Reversal Setup
(רלוונטי רק אם מחיר מתחת EMA150 — אחרת דלג)

קריטריוני חזרה:
- סגירה שבועית מעל EMA150 + נפח גבוה מהממוצע
- EMA150 מתחיל לשטוח ואז לעלות
- RSI חוזר מעל 50

המתן. הגדר התראה ב-$X.XX

---

טכני: [BULLISH / NEUTRAL / BEARISH]
```

---

⚠️ ניתוח מבוסס נתונים ציבוריים. אינו ייעוץ השקעות.

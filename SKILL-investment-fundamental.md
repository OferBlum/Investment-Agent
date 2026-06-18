# SKILL-investment-fundamental.md
> `0 - מערכת/SKILL-investment-fundamental.md`
> נטען לניתוח פונדמנטלי בלבד — ללא טכני וללא המלצת כניסה

---

## תפקיד

Elite Equity Research Analyst — Hedge Fund style. ניתוח פונדמנטלי מקיף ב-5 שכבות + 26 ממדים.
הפלט של קובץ זה הוא חומר גלם לניתוח מלא (`SKILL-investment-deep-analyze.md`) — או תשובה עצמאית לשאלת פונדמנטלס.

---

## נתונים — Playwright

בצע את כל החיפושים הבאים לפני הניתוח:

```
"[TICKER] business model revenue streams annual report"
"[TICKER] EPS earnings growth last 4 quarters beat miss"
"[TICKER] revenue CAGR gross margin operating margin trend"
"[TICKER] free cash flow FCF conversion"
"[TICKER] balance sheet debt leverage interest coverage"
"[TICKER] P/E PEG P/S EV/EBITDA EV/Sales P/FCF valuation peers"
"[TICKER] insider ownership trades SEC Form 4 recent"
"[TICKER] institutional ownership 13F changes"
"[TICKER] competitive moat market share positioning"
"[TICKER] sector outlook industry cycle 2026"
"[TICKER] macro tailwinds headwinds rates regulation"
"[TICKER] upcoming catalysts earnings product launch"
"[TICKER] analyst price target rating consensus"
"[TICKER] management guidance consensus next quarter revenue EPS"
"[TICKER] analyst EPS estimate revisions 90 days trend"
"[TICKER] share buyback repurchase stock-based compensation dilution"
"[TICKER] ROIC return on invested capital WACC"
"[TICKER] earnings transcript latest quarter management commentary"
```

מקורות מומלצים: SEC EDGAR, Seeking Alpha, Macrotrends, Wisesheets, FinViz.

---

## פלט

```
## [TICKER] — Fundamental Analysis
### [שם חברה] | [בורסה] | [סקטור]
### [תאריך] | Data as of latest available

> 🔍 Layer 0: כנס לאתר, ראה מוצרים, שמע מנכ"ל — לפני AI.

מודל עסקי: [2-3 משפטים]
דרייברי ערך: [א] | [ב] | [ג]
הקצאת הון: [buybacks / דיבידנד / M&A / capex]

---

## Layer 1 — Profitability

| מדד | שנה -2 | שנה -1 | TTM | מגמה |
|-----|--------|--------|-----|------|
| Revenue ($B) | X | X | X | ↑/→/↓ |
| Revenue YoY % | X% | X% | X% | ↑/→/↓ |
| Gross Margin % | X% | X% | X% | ↑/→/↓ |
| Operating Margin % | X% | X% | X% | ↑/→/↓ |
| Net Margin % | X% | X% | X% | ↑/→/↓ |
| EPS (reported vs est) | X / X | X / X | X / X | ↑/→/↓ |
| EBITDA adj gap | קטן/בינוני/גדול | — | — | ↑/→/↓ |

📌 [מאיץ או מואט? Pricing power? Beat streak? EBITDA gap?]

---

## Layer 2 — Valuation

| מדד | [TICKER] | עמית 1 | עמית 2 | ממוצע ענף | ממוצע [TICKER] 5Y |
|-----|----------|--------|--------|-----------|-------------------|
| P/E TTM | X | X | X | X | X |
| Forward P/E | X | X | X | X | X |
| PEG | X | X | X | X | — |
| P/S | X | X | X | X | X |
| EV/EBITDA | X | X | X | X | X |
| P/B | X | X | X | X | X |
| P/FCF | X | X | X | X | X |

📌 [זול/יקר vs היסטוריה ועמיתים? Multiple expansion/compression?]

---

## Layer 3 — Cash Flow

| מדד | שנה -2 | שנה -1 | TTM | מגמה |
|-----|--------|--------|-----|------|
| OCF ($B) | X | X | X | ↑/→/↓ |
| OCF / Net Income % | X% | X% | X% | ↑/→/↓ |
| FCF ($B) | X | X | X | ↑/→/↓ |
| FCF Margin % | X% | X% | X% | ↑/→/↓ |
| FCF Yield % | X% | X% | X% | — |

📌 FCF Yield X% vs. 10Y Treasury X% — [מספק/לא מספק]
[FCF גדל מהר מהכנסות? OCF עקבי מעל Net Income?]

---

## Layer 4 — Financial Health

| מדד | ערך | מגמה | Stress Test (EBITDA −30%) |
|-----|-----|------|---------------------------|
| Debt/Equity | X | ↑/→/↓ | [עומד/לא עומד] |
| Net Cash / Debt ($B) | X | — | — |
| Current Ratio | X | ↑/→/↓ | — |
| Interest Coverage | Xx | ↑/→/↓ | [מעל/מתחת 3x] |
| ROE % | X% | ↑/→/↓ | — |
| ROE Driver | [Margin/Turnover/Leverage] | — | — |
| ROIC % | X% | ↑/→/↓ | — |
| ROIC > WACC | כן/לא | — | — |

📌 [ROE אמיתי או leverage-driven? ROIC spread מתרחב/מצטמצם?]

---

## Layer 5 — Forward Signals

| אות | נתון | פרשנות |
|-----|------|----------|
| Management Guidance | [מעל/מתחת/בקו] | [שמרני/אגרסיבי/בקו] |
| Analyst Revisions (90d) | [+X% / −X% NTM EPS] | [משתפר/מתדרדר] |
| Buy / Hold / Sell | X / X / X | [קונצנזוס חזק/חלש] |
| EPS Beat Streak | X רבעונים | [מתרחב/מצטמצם] |
| Buyback Quality | [real / SBC offset] | ✅/❌ |
| Buyback Yield % | X% | — |
| Insider Cluster Buy | כן/לא | ✅/❌ |
| Institutional (QoQ) | [+X% / −X%] | — |

📌 [הרוח בגב או בפנים? Beat streak מתדרדר = אזהרה מוקדמת]

---

## סקטור, מאקרו ו-Moat

שלב מחזור ענף: [צמיחה מוקדמת / בשל / האטה / התאוששות]

מגמות מאקרו:
- [מגמה 1]: [headwind/tailwind] — [הסבר]
- [מגמה 2]: [headwind/tailwind] — [הסבר]

| ממד Moat | [TICKER] | מתחרה עיקרי |
|----------|----------|--------------|
| סקייל | גבוה/בינוני/נמוך | — |
| טכנולוגיה/IP | גבוה/בינוני/נמוך | — |
| עלות/הפצה | גבוה/בינוני/נמוך | — |

Catalysts קרובים (0–6 חודשים): [תאריך] — [אירוע] → [השפעה]
Catalysts ארוכים (6–36 חודשים): [מחזור מוצר / שוק חדש / רגולציה]

---

## סיכום פונדמנטלי

**חיוביים:**
✅ [ממצא 1 + נתון]
✅ [ממצא 2 + נתון]
✅ [ממצא 3 + נתון]

**סיכונים:**
⚠️ [סיכון פונדמנטלי]
⚠️ [סיכון תמחור]
❌ [דגל אדום — אם יש]

**מה יבטל את התזה:** [קו אדום ברור]
**הכי תלוי ב:** [הנחה קריטית אחת]

פונדמנטלס: [STRONG / MODERATE / WEAK]
```

---

## נספח — 26 ממדי ניתוח

> עבור על כל 26 הממדים — חפש נתונים עדכניים, ענה על כל שאלה.
> [TICKER] = הטיקר | [SECTOR] | [PEER 1] / [PEER 2]

### Layer 01 — Profitability

| # | ממד | נתונים | השוואה | שאלה מרכזית |
|---|-----|--------|--------|---------------|
| 01 | Revenue Growth | 8Q YoY & QoQ | [PEER 1], [PEER 2], [SECTOR] | מאיץ או מואט? |
| 02 | Gross Margin | 8Q | [PEER 1], [PEER 2], [SECTOR] | מתרחב/מצטמצם? Pricing power? |
| 03 | Operating Margin | 8Q | [PEER 1], [PEER 2], [SECTOR] | Operating leverage משתפר? |
| 04 | Net Margin | 8Q | [PEER 1], [PEER 2], [SECTOR] | פער vs operating → ריבית/מס/חד-פעמי? |
| 05 | EPS | 8Q reported vs est | [SECTOR] beat rate | Beat streak מתרחב/מצטמצם? |
| 06 | EBITDA | 8Q reported vs adj | [PEER 1], [PEER 2], [SECTOR] | ⚠️ גאפ reported/adj מתרחב = איכות רווחים יורדת |

### Layer 02 — Valuation

| # | ממד | נתונים | השוואה | שאלה מרכזית |
|---|-----|--------|--------|---------------|
| 07 | P/E TTM | כעת + 5Y avg | [PEER 1], [PEER 2], [SECTOR] | פרמיה/הנחה vs היסטוריה ועמיתים? |
| 08 | Forward P/E | NTM + שינוי 3M | [PEER 1], [PEER 2], [SECTOR] | Multiple מתרחב מהמחיר או מהאומדנים? |
| 09 | P/S | כעת + 3Y avg | [PEER 1], [PEER 2], [SECTOR] | מוצדק ע"י gross margin + צמיחה? |
| 10 | EV/EBITDA | כעת adj לחוב/מזומן | [PEER 1], [PEER 2], [SECTOR] | זול/יקר ברמת enterprise? |
| 11 | PEG | P/E ÷ 3Y EPS CAGR | [PEER 1], [PEER 2], [SECTOR] | הצמיחה מצדיקה את ה-P/E? |
| 12 | P/B | כעת + 5Y avg | [PEER 1], [PEER 2], [SECTOR] | פרמיה P/B מוצדקת ע"י ROE גבוה? |

### Layer 03 — Cash Flow

| # | ממד | נתונים | השוואה | שאלה מרכזית |
|---|-----|--------|--------|---------------|
| 13 | OCF | 8Q OCF vs Net Income | [SECTOR] | ⚠️ OCF בעקביות < Net Income = דגל אדום |
| 14 | FCF | 8Q growth | vs Revenue & Net Income | FCF גדל מהר מהכנסות? (= מודל סקיילבילי) |
| 15 | FCF Margin | 8Q % | [PEER 1], [PEER 2], [SECTOR] | Top/bottom quartile בסקטור? |
| 16 | FCF Yield | TTM FCF / Market Cap | 10Y Treasury + [SECTOR] | Yield מפצה על סיכון מניה? |

### Layer 04 — Financial Health

| # | ממד | נתונים | השוואה | שאלה מרכזית |
|---|-----|--------|--------|---------------|
| 17 | Debt/Equity | 4Y + interest coverage | [PEER 1], [PEER 2], [SECTOR] | ⚠️ Coverage < 3x + EBITDA −30% stress test |
| 18 | Net Cash / Debt | מזומן vs חוב כעת | [PEER 1], [PEER 2], [SECTOR] | כמה רבעונות הוצאות מכסה המזומן? |
| 19 | Current Ratio | 4Q + quick ratio | [SECTOR] | נזילות משתפרת? פירעונות קרובים? |
| 20 | ROE | 5Y DuPont decomposition | [PEER 1], [PEER 2], [SECTOR] | ROE אמיתי (margin/turnover) או leverage בלבד? |
| 21 | ROIC vs WACC | 5Y ROIC-WACC spread | [PEER 1], [PEER 2], [SECTOR] | ⚠️ Spread מתרחב = compounder; מצטמצם = שחיקה |

### Layer 05 — Forward Signals

| # | ממד | נתונים | השוואה | שאלה מרכזית |
|---|-----|--------|--------|---------------|
| 22 | Management Guidance | Q + FY vs קונצנזוס | vs guidance שנה קודמת | שמרני/אגרסיבי? Bar גבוה/נמוך? |
| 23 | Analyst Consensus | Buy/Hold/Sell + PT | שינוי 3M | סנטימנט משתפר? פיזור PT רחב = מחלוקת? |
| 24 | Earnings Revisions | NTM EPS שינוי 90d | % מעלים vs מורידים | Revisions = leading indicator לכיוון המחיר |
| 25 | Share Buybacks | 8Q dollars + shares | vs SBC dilution | ⚠️ האם buybacks מקטינים share count בפועל? |
| 26 | Insider Transactions | 6M transactions | vs נורמה היסטורית | Cluster buying = אות עוצמה גבוהה |

---

⚠️ ניתוח מבוסס מידע ציבורי בלבד. אינו ייעוץ השקעות.

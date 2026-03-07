---
type: research
category: Market
action_type: Tips
security:
exchange:
region:
announce_date:
ex_date:
record_date:
pay_date:
currency:
status: Raw
ai_confidence: Medium
source_url: https://qoppac.blogspot.com/2026/01/are-markets-that-are-good-for-trend.html
source_type: Website
themes: []
---

# 🧠 AI Summary
> Paste AI-generated summary here.
> Highlight dates, ratios, conditions, uncertainties.

This is a **systematic quant analysis blog post** by Rob Carver exploring why certain asset classes perform better in trend-following strategies. The post challenges the assumption that assets with strong long-term price appreciation (like bonds) are inherently better for trend following, and instead investigates whether performance is driven by **secular price drift**, **carry**, or **other structural factors**.

---

## 🔍 **Core Question & Hypothesis**

- **Observation:** Fixed income (bonds) shows strong trend-following performance historically (high Sharpe Ratio).
    
- **Question:** Is this because bonds have been in a long-term bull market ("number go up"), or is there something unique about their price behavior?
    
- **Hypothesis:** Trend performance may be correlated with **long-only adjusted price returns** (spot + carry), not just spot price movement.
    

---

## 📈 **Methodology & Data Analysis**

The author uses **scatter plots and regression analysis** to compare:
- **Y-axis:** Sharpe Ratio of trend-following strategy (momentum-based).
- **X-axis:** Sharpe Ratio of:
    1. **Adjusted price returns** (spot + carry)
    2. **Spot price returns**
    3. **Cumulated carry returns**

Analysis is done for **three trend speeds**:
- **Fast trend** (momentum 8)
- **Medium trend** (momentum 16)
- **Slow trend** (momentum 64)

Data is split into **five-year rolling periods** and grouped by **asset class** (Equity, Vol, FX, Bond, Metals, Energy, Ags).

---

## 📌 Key Insights

### 1. **Adjusted Price Drift Is Strongly Correlated with Trend Performance**
- For **slow momentum (64)**, there is a clear **positive slope** (~0.7 to 0.9) between adjusted price SR and trend SR.
- This means: **Every 1 unit of adjusted price drift yields ~0.7–0.9 units of trend SR.**
- **Asset classes with strong relationship:** Bonds, FX, Metals, Vol.
- **Asset classes with weak relationship:** Equities, Energies, Ags.

### 2. **Spot Price Alone Is a Weaker Predictor**
- Spot price returns show some correlation but are less consistent than adjusted returns.

### 3. **Carry Alone Shows Little Relationship**
- Carry returns do not meaningfully predict trend-following performance (except for Vol, where carry is part of the futures curve structure).

### 4. **Two Distinct Groups of Asset Classes Emerge**
- **Group 1 (Trend-convertible):** Bonds, FX, Metals, Vol → strong ability to convert price drift into trend profits.
- **Group 2 (Trend-resistant):** Equities, Energies, Ags → weak conversion of drift into trend profits.

## 🧠 **Interpretation & Implications**

### ✅ **Why Bonds Are Good for Trend (But Not Uniquely)**
- Bonds have had strong **adjusted price drift** (spot + carry) over the sample period.
- This drift is **convertible into trend profits** for slow momentum strategies.
- However, **FX, Metals, and Vol** show similar conversion efficiency → bonds are not special, but part of a _category_ of assets with “trendable” drift.

### ⚠️ **Equities Are an Outlier**
- Equities had strong long-only returns but **poor trend performance**.
- Suggests equity trends are **noisier, more mean-reverting, or less persistent** than in bonds/FX.

### 📊 **Practical Takeaways for Systematic Traders**
1. **Not all drift is equal** – only certain asset classes allow drift to be harvested by trend strategies.
2. **Focus on adjusted prices** (spot + carry) when evaluating trend potential.
3. **Asset class selection matters** – trend following may be more effective in Bonds, FX, Metals, and Vol than in Equities or Commodities (Energies, Ags).
4. **Speed matters** – slower trends (momentum 64) capture drift more effectively than faster trends.

---

## 📝 Analyst Notes
Your interpretation, caveats, or questions.

This analysis provides a **nuanced, data-driven perspective** on trend-following profitability. It moves beyond simplistic explanations (“bonds went up”) and identifies **adjusted price drift** as a key explanatory variable, while also revealing a **structural split between asset classes**.

For quants and trend followers:
- **Factor in carry** when modeling futures returns.
- **Consider asset class characteristics** when building multi-asset trend portfolios.
- **Avoid overfitting** to historical bond bull markets—instead, understand _why_ certain assets trend better.

The post underscores that **trend following is not just about riding bull markets**, but about **capturing persistent, convertible price drift**—a property that varies significantly across asset classes.

---
## ⚠️ Verification Checklist
- [ ] Dates verified against PDF
- [ ] Numbers verified
- [ ] Conditions understood
- [ ] Cross-checked with exchange notice

---

## 🔗 Related
- [[Momentum as a Life Cycle, Not Discrete Strategies]]
- [[Introduction To Forecast Signals]]

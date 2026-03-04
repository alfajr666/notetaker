---
type: research
category: Trading
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
source_url: https://x.com/KevinLMak/article/1843856869300830705
source_type: Twitter
themes: []
---

# 🧠 AI Summary
> Paste AI-generated summary here.
> Highlight dates, ratios, conditions, uncertainties.

This article by Kevin Mak is a **deep dive into risk management, portfolio sizing, and the practical application of quantitative finance concepts** like the Kelly Criterion and Modern Portfolio Theory (MPT). Using analogies from poker and coin-tossing games, the author explains how to size positions, manage portfolio weights, and avoid common pitfalls in investing.

## 🎲 **Core Concepts Explained**
### 1. **Table Stakes (Poker Analogy)**
- In poker, you can only bet what’s in front of you—you can’t add more mid-hand.
- **Professional poker players** keep only a small portion of their total bankroll on the table at once (e.g., 1–3% per buy-in).
- **Key insight:** Risk is capped by your table stakes, which naturally enforces position sizing and prevents ruin.

### 2. **Kelly Criterion**
- Answers: **How much to bet when you have a known edge?**
- Example: A biased coin (60% heads, 40% tails) with 1:1 payout → optimal bet = 20% of bankroll.
- **Principles:**
    - Bet a **percentage of current wealth**, not a fixed dollar amount.
    - Bet size should **scale with edge size** (larger edge = larger bet).
    - Goal: Maximize **geometric growth**, not expected value.
    - Over-betting is dangerous → many use **“Half-Kelly”** to reduce risk.

### 3. **Modern Portfolio Theory (MPT)**
- Developed by Harry Markowitz; focuses on **portfolio diversification**.
- MPT optimizes capital allocation across multiple risky assets based on:
    - Expected returns
    - Risk (variance)
    - Correlation between assets
- **Key insight:** Diversification reduces risk without sacrificing returns (the “free lunch”).

### 4. **Portfolio Rebalancing**
- Both Kelly and MPT suggest **dynamic rebalancing** of portfolio weights.
- As a stock rises, its weight increases → trim to maintain optimal sizing.
- As a stock falls (if thesis unchanged), its weight decreases → buy more to increase exposure.
- Rebalancing helps **maintain target risk/reward exposure** and maximize geometric returns.

## 📈 **Practical Framework for Portfolio Weighting**
The author proposes a **simplified, rules-based approach** to position sizing:
1. **Set a global max weight** (e.g., 10%) to cap single-stock risk.
2. **Define a price target** (e.g., $20) and a **floor price** (e.g., $4).
3. **Calculate risk/reward:**
    - Risk = Current price – Floor
    - Reward = Target – Current price
4. **Map stock price to portfolio weight** (non-linearly preferred).
5. **Rebalance periodically** as price moves relative to target/floor.

This is a **“directionally correct half-Kelly”** approach—approximate but robust, avoiding over-reliance on precise inputs.

Kelly Criterion Simulator can be found here:
[[https://docs.google.com/spreadsheets/d/1OapSADrZRTHEGd-WR-CRo0VUFy7YPcaWPk_Vlt_zn40/edit?gid=0#gid=0]].

---

## 📌 Key Insights

### ✅ **Risk Management Over Maximizing Returns**
- **Avoid ruin:** Never bet so much that a loss wipes you out.
- **Size positions as a percentage of portfolio**, not as fixed amounts.
- **Use caps** (like table stakes) to enforce discipline.

### 🔄 **Dynamic Sizing & Rebalancing**
- Weights should adjust with **price changes and edge estimates**.
- **Buy more when price falls** (if thesis holds), **trim when price rises**.
- Rebalancing captures **mean reversion and risk control**.

### 🎯 **Edge Estimation Is Critical**
- Kelly and MPT require **estimating expected returns**—often the hardest part.
- Overconfidence in edge leads to **over-betting and blowups**.
- Use **conservative estimates** and half-Kelly to protect against estimation error.

### 🃏 **Poker vs. Investing Parallels**
- Retail traders often treat accounts like **single buy-ins**—going “all-in” on high-conviction ideas.
- For large portfolios, **professional bankroll management** (like poker pros) aligns with Kelly/MPT principles.

### 📉 **When to Deviate from MPT**
- MPT relies on **historical correlations**, which may break during crises or for **special situations** (e.g., binary corporate events).
- In such cases, a **custom, thesis-driven weighting approach** may be more appropriate.

### 💡 **Nuances in Common Wisdom**
- **“Let winners run”** can align with Kelly if starting weights were too small.
- **“Losers average losers”** can be dangerous if the thesis is broken.
- **Tax considerations** are secondary to risk management—don’t let taxes excuse poor sizing.

---

## 📝 Analyst Notes
Your interpretation, caveats, or questions.

This article bridges **theory and practice** in portfolio management. It emphasizes that:
- **Risk management is not optional**—it’s the foundation of sustainable investing.
- **Mathematical rigor helps, but practical simplicity often wins**.
- **Position sizing should evolve with portfolio size and confidence level**.

Whether you’re a retail trader with one “buy-in” or a fund manager with billions, the principles of **Kelly, MPT, and table stakes** provide a robust framework for balancing growth and survival.

---

## 🔗 Related
- [[Managing Trading Psychology - Why Position Sizing is the Key to Success]]
- [[Risk Management Framework & Philosophy]]
- [[How to Become a Quant for Prediction Markets (Complete Roadmap)]]

---
## ⚠️ Verification Checklist
- [ ] Dates verified against PDF
- [ ] Numbers verified
- [ ] Conditions understood
- [ ] Cross-checked with exchange notice

---
title: How Market-Making Works (Poorly Illustrated)

---

# How Market-Making Works (Poorly Illustrated)

---
type: reading
source_type: Website
source_url: https://idrawcharts.medium.com/how-market-making-works-poorly-illustrated-128b5ae8304d
Date: November 4, 2021
Date modified: February 25, 2026

themes: Market Making, Order Books, Volatility, Trading Mechanics

---
# 🧠 AI Summary
> David Holt explains the fundamentals of market making using a simplified, "poorly illustrated" model. [cite_start]He defines the primary goal as capturing the **spread** (difference between best bid and offer) while utilizing **exchange rebates** (typically around **1 bp**) to enhance profitability[cite: 10, 13, 20]. [cite_start]The text details how market makers manage inventory when price moves against them—either by cutting losses or **averaging down** to tighten spreads[cite: 27, 40, 42]. [cite_start]Holt emphasizes that success is a **game of averages**, where one must balance order size and spread width against varying levels of **daily and intraday volatility**[cite: 62, 63].

---

## 📌 Key Insights
* [cite_start]**The Spread and Rebates:** A market maker's revenue comes from both the visible spread and exchange rebates for providing liquidity (maker orders)[cite: 10, 13]. [cite_start]For instance, a $0.01 spread can effectively yield ~$0.03 in profit after accounting for rebates on both sides of a trade[cite: 20].
* [cite_start]**Handling Adverse Price Movement:** When price moves significantly, market makers must decide between dumping inventory at a market loss or lowering their offer to a "breakeven" price while placing new, lower bids[cite: 27, 28, 32].
* [cite_start]**Averaging Down:** By buying more at lower prices (averaging down), a market maker can lower their average cost basis, allowing them to tighten their spread and return to normal operations faster[cite: 40, 42].
* **Volatility Strategies:**
    * [cite_start]**Low Volatility:** Use large order sizes and tight spreads to maximize volume[cite: 53, 54].
    * [cite_start]**High Intraday / Low Daily Vol:** Widen spreads and use larger orders to capture bigger, frequent price swings[cite: 55].
    * [cite_start]**Low Intraday / High Daily Vol:** Keep spreads tight and sizes small; cut losses quickly as the market is trending[cite: 59].
    * [cite_start]**High Volatility Across Board:** The riskiest environment; requires wider spreads and smaller, carefully managed sizes[cite: 60, 61].
* [cite_start]**Inventory Risk:** The greatest risk occurs when the market "chews through" orders on only one side of the book, forcing the market maker to unload a large, losing position[cite: 65].

---

## 📝 Analyst Notes
Holt’s guide effectively demystifies the "black box" of market making by focusing on the relationship between inventory management and volatility. While he simplifies the environment to a single market maker, the principles of **rebate arbitrage** and **volatility-adjusted sizing** are universal across high-frequency trading. [cite_start]A key takeaway is that market makers are not "predicting" price but rather managing a statistical probability—they are the "house" that occasionally gets hit by a "whale" or a trending market, which is why the ability to react when things don't match historical averages is the defining skill[cite: 63, 64].

---

## 🔗 Related
- [[How do liquidity and return reversals work, and how profitable is a strategy based on them?]]
- [[The 10am Drop - How Jane Street Broke Bitcoin's Price]]
- [[Why TA itself fails and what actually moves markets]]

---


tags: #MarketMaking #Liquidity #Orderflow #Volatility #TradingBasics

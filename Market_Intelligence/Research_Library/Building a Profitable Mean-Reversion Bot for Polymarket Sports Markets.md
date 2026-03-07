---
title: Building a Profitable Mean-Reversion Bot for Polymarket Sports Markets

---

# Building a Profitable Mean-Reversion Bot for Polymarket Sports Markets

---
type: research / technical guide
source_type: X (Twitter) / Polyburg Terminal
source_url: https://x.com/polyburg/article/2026877934179594524
[cite_start]Date: February 26, 2026 [cite: 571]
Date modified: March 1, 2026

themes: Prediction Markets, Algorithmic Trading, Behavioral Finance, Polymarket, Mean Reversion

---
# 🧠 AI Summary
> [cite_start]This report details the development of a trading bot designed to exploit price overreactions in **Polymarket** sports betting markets following scoring events[cite: 579, 583]. [cite_start]Grounded in decades of behavioral finance research, the "Shock & Fade" strategy leverages a structural edge by operating as a **market maker** to avoid Polymarket's 3-second delay on aggressive "taker" orders[cite: 608, 640, 647]. [cite_start]Backtesting across 18 NBA games yielded a **73.3% win rate** and an **11% ROI**, demonstrating that consistent profits can be captured by providing liquidity during moments of peak market "surprise"[cite: 583, 720, 722].

---

## 📌 Key Insights
* [cite_start]**The Behavioral Edge:** Markets frequently overreact to "surprising" events (e.g., an underdog scoring), causing prices to overshoot before reverting to a "fair" value within 30–120 seconds[cite: 580, 582, 590].
* [cite_start]**Structural Advantage (Maker vs. Taker):** Polymarket imposes a **3-second delay** on marketable "taker" orders to prevent courtsiding[cite: 640, 642]. [cite_start]Limit "maker" orders have **no delay**, allowing the bot to execute instantly when aggressive buyers hit its resting sell orders[cite: 643, 647].
* [cite_start]**The "Shock" Detection Logic:** The bot tracks a 60-second rolling **z-score** of mid-prices; a trade is triggered when the move exceeds **$2\sigma$** and is at least **3¢**[cite: 623, 624, 625].
* [cite_start]**Inventory Management:** The strategy uses the Conditional Token Framework (CTF) to pre-split USDC into both outcome tokens before a game, ensuring it always has inventory to sell into a spike without needing to buy first[cite: 611, 612, 613].
* [cite_start]**Event-Driven Exit:** Unlike traditional time-based exits, this bot closes positions only when the **next scoring event** occurs, which serves as a natural price recalibration point[cite: 659, 660, 662].
* [cite_start]**Execution Tactics:** To avoid the 3-second exit delay, the bot uses a **"GTC-at-bid+1tick"** strategy, placing limit orders just above the best bid to ensure near-instant fill as a maker[cite: 666, 668, 669].
* [cite_start]**Scalability & Performance:** The system monitors dozens of simultaneous games across the NBA, NHL, and CBB using free APIs (e.g., ESPN, NBA CDN) and direct Polygon on-chain execution[cite: 728, 761, 762].

---

## 📊 Performance Metrics
| Metric | Result (NBA Backtest) |
| :--- | :--- |
| **Return on Investment (ROI)** | [cite_start]11% ($107 profit on $1,000 capital) [cite: 720] |
| **Win Rate** | [cite_start]73.3% [cite: 722] |
| **Sharpe Ratio** | [cite_start]0.55 [cite: 723] |
| **Games Traded** | [cite_start]18 [cite: 721] |
| **Parameter Robustness** | [cite_start]100% (all tested combinations were profitable) [cite: 724] |

---

## 📝 Analyst Notes
[cite_start]The strategy's success relies heavily on the **latency advantage** afforded to market makers on Polymarket[cite: 687]. [cite_start]By pre-positioning inventory and using limit orders, the bot effectively "sells" during periods of panic buying, capturing the spread and the overreaction premium[cite: 698]. [cite_start]While the academic foundations (Choi & Hui, 2014; Moskowitz, 2021) suggest these inefficiencies are persistent, the strategy faces risks if Polymarket changes its order delay rules or if liquidity becomes too thin in smaller markets like College Basketball[cite: 588, 607, 778].

---

## 🔗 Related
- [[How to Become a Quant for Prediction Markets (Complete Roadmap)]]
- [[How Market-Making Works (Poorly Illustrated)]]
- [[How Not To Be A Shit Gambler]]

tags: #Polymarket #SportsBetting #TradingBot #MeanReversion #DeFi

  

## 1. Overview

These materials provide a comprehensive introduction to quantitative trading strategies, covering fundamental concepts, data types, model development, and various financial instruments. They also delve into practical aspects like Python programming for financial data analysis, risk and return calculations, and specific trading strategies such as trend following and momentum trading. Finally, the lectures explain derivative products like forward and futures contracts, including their pricing and market dynamics.

  

```mermaid
graph TD
A["Quantitative Trading"] --> B["Core Concepts"]
A --> C["Financial Instruments"]
A --> D["Data & Programming"]
A --> E["Risk & Return"]
A --> F["Trading Strategies"]
A --> G["Derivatives"]
B --> "Algorithmic Trading"
C --> "Stocks, Bonds, Options"
D --> "Python, YFinance"
E --> "Sharpe Ratio, Drawdown"
F --> "Trend Following, Momentum"
G --> "Forwards, Futures"
```

  

## 2. Learning Roadmap

This roadmap is designed to guide you through the materials in a logical progression, starting with foundational concepts and gradually moving to more complex topics and practical applications.

  

|   |   |   |   |
|---|---|---|---|
|**Material**|**Topic**|**Difficulty**|**Key Features**|
||Introduction to Quantitative Trading, Financial Data, Asset Classes|Easy|Core definitions, types of financial data, overview of asset classes.|
||Payoff Functions, Market Structure, Stock Price Charts|Easy|Explains payoff for derivatives, market participants, candlestick charts.|
||Python Programming Basics|Easy|Essential Python concepts for financial data manipulation.|
||Downloading & Visualizing Stock Price with Python|Medium|Practical application of Python for data retrieval and visualization.|
||Electronic Order, Market Order, Order Matching|Medium|Details on order types and how trades are executed in electronic markets.|
||Limit Order Book, Display Order|Medium|In-depth explanation of limit orders and market liquidity.|
||Stop Limit Order, Pegging, Trailing Stop, Price Impact|Medium|Advanced order types and their implications.|
||Risk and Return|Medium|Fundamental concepts of risk, return, and performance metrics.|
||Calculating Return, Risk, and Annualization|Medium|Practical Python implementation for risk and return calculations.|
||Log Returns and Technical Indicators|Hard|Introduction to log returns and the concept of technical indicators for strategy.|
||Working with Log Returns (Lab)|Hard|Hands-on Python lab for calculating and understanding log returns.|
||Moving Averages and Trend Following Strategy|Hard|Explains moving averages and their application in trend-following strategies.|
||Simple and Exponential Smoothing Averages (Lab)|Hard|Practical Python lab for calculating and visualizing moving averages.|
||Implementing the Trend Following Strategy (Lab)|Hard|Full implementation of a trend-following strategy in Python.|
||Momentum Trading Strategy|Hard|Differentiates momentum trading from trend following, cross-sectional analysis.|
||Max Drawdown|Hard|Focuses on downside risk measurement and its calculation.|
||Forward Contract, Futures Contract, Clearing House|Hard|Detailed explanation of derivative contracts and their market infrastructure.|
||Mark to Market, Daily Settlement of Futures Contract|Hard|Explains the daily settlement process for futures contracts.|
||No-Arbitrage Pricing for Forward & Futures Contract|Hard|Advanced pricing models for derivative contracts.|
||Contango and Backwardation|Hard|Market phenomena related to futures pricing.|

  

## 3. Detailed Analysis by Material

  

## 3.1 Quantitative trading strategies lecture 1.1 - financial data, model development, asset classes

==This lecture introduces quantitative trading, its core concepts, types of financial data, model development workflow, and common asset classes and derivatives.==

- Quantitative trading (algorithmic trading) refers to automated trading strategies that generate buy/sell signals for financial instruments based on algorithms .
    
    - A good strategy involves buying low and selling high (long security) or selling high and buying low (short security) .
        
    - The quality of trading decisions depends on:
        
        - Sufficiency of input data: Data is essential for building and training robust models .
            
        - Model robustness: The model should perform well on future data, not just historical data, requiring backtesting .
            
        
    
- Four types of financial input data are crucial for quantitative trading:
    
    - Market states: Describes the overall market condition, including price movements (tick data) and market-specific factors like bid-ask spread .
        
    - Financial news: Textual data from news, reports, or conference call transcripts, which is harder to analyze but provides fundamental insights .
        
    - Fundamentals: Covers overall economic/sector-specific conditions and firm-specific metrics (revenue, cash flow, EPS) .
        
    - Technicals: Uses historical price data to derive technical indicators (moving averages, stochastic indicators) to predict price direction .
        
    
- The overall trading process involves:
    
    - Input data feeding into an "engine" (model) .
        
    - The model learns patterns from data .
        
    - The model outputs a buy or sell decision .
        
    
- The model development workflow involves:
    
    - Training data (inputs X and outputs Y) .
        
    - Finding a function (model F) that predicts Y (Y-hat) from X .
        
    - Comparing predictions (Y-hat) with true labels (Y) to calculate a "cost" .
        
    - Optimizing model parameters to minimize this cost .
        
    - The model F consists of parameters (learnable weights) and architecture (information flow definition) .
        
    
- Institutional algorithmic trading involves large volumes and requires breaking down orders to reduce execution risk and control market impact .
    
    - Slippage is the price difference between the intended and actual execution price .
        
    - Large orders are often executed in dark pools (private exchanges) and can be structured as iceberg orders (small visible portion, large hidden portion) .
        
    
- Key skills for a quant trader include strong mathematical modeling, quantitative analysis, and soft skills like handling high pressure .

---

## 🔗 Related
- [[Introduction To Forecast Signals]]
- [[Price Discovery and Trading]]
- [[Table Stakes, Kelly Betting, MPT, and Portfolio Weights]]
    
- Asset classes and derivatives are tradable financial instruments .
    
    - Long position means buying, short position means selling .
        
    - Assets can be single or combinations, used for profit-seeking or risk management (hedging) .
        
    - Common asset classes:
        
        - Stocks (Equity): Represents proportionate ownership, profit from price appreciation or dividends .
            
        - Bonds (Fixed Income): Debt instruments, more stable, lower risk/return, provide fixed/variable interest payments and principal return .
            
        - Annuities: Insurance contracts providing a fixed income stream, often for retirement .
            
        - Cash and Equivalents: Highly liquid, short-term, low risk/return (e.g., bank accounts, T-bills, money market funds) .
            
        - Commodities: Basic goods/raw materials (e.g., gold, oil, natural gas), traded in spot or derivatives markets .
            
        
    - Common derivatives:
        
        - Futures Contracts: Obligates buyer/seller to transact an asset at a specific future date and price, used for hedging price movements, traded on exchanges .
            
        - Forwards: Similar to futures but traded over-the-counter (OTC), directly between parties without a central exchange .
            
        - Options: Gives the right (not obligation) to buy (call) or sell (put) an asset at a specific price by an expiration date, used for hedging or speculation .
            
        - Currency (Forex): Exchange one currency for another, speculate on currency movements .
            
        - ETFs (Exchange Traded Funds): Portfolios of securities (stocks, bonds, commodities) traded like stocks, generally lower risk .
            
        - REITs (Real Estate Investment Trusts): Companies owning/operating income-generating real estate, provide steady income streams .
            
        - Mutual Funds: Portfolios of securities, purchased at end-of-day net asset value (NAV) .
            
        - Hedge Funds: High-frequency, higher risk/return, wider range of strategies, higher fees .
            
        
    

  

## 3.2 Quantitative trading strategies lecture 1.2 - payoff function, market structure, stock price chart

==This lecture categorizes trading assets, explains payoff functions for derivatives, details market structure, and introduces stock price visualization using candlestick charts.==

- Trading assets are grouped into:
    
    - Stocks/Equities .
        
    - Fixed income instruments: Bonds and annuities, providing fixed income .
        
    - Cash and equivalents: Most liquid assets like bank accounts, T-bills, money market funds .
        
    - Alternative investments: Commodities, Forex, futures, options, ETFs, hedge funds .
        
    
- Payoff functions for derivatives:
    
    - Futures contract (long position): Obliged to buy an asset at a future date for a specific price (K) .
        
        - Profit if future stock price (St) > K .
            
        - Loss if St < K .
            
        - Payoff is linear: St - K .
            
        
    - Call option (long position): Right to buy an asset at price K .
        
        - Profit if St > K (buy cheaper than market) .
            
        - No exercise (loss of option premium) if St < K (market price is cheaper) .
            
        - Payoff is non-linear: max(0, St - K) .
            
        
    - Call option (short position): Obligation to sell if the buyer exercises .
        
        - Loss if St > K (unlimited risk) .
            
        - Profit (option premium) if St < K .
            
        - Payoff is non-linear: -max(0, St - K) .
            
        
    - Put option (long position): Right to sell an asset at price K .
        
        - Profit if St < K (sell higher than market) .
            
        - No exercise if St > K .
            
        - Payoff is non-linear: max(0, K - St) .
            
        
    - Put option (short position): Obligation to buy if the seller exercises .
        
        - Loss if St < K (bounded risk) .
            
        - Payoff is non-linear: -max(0, K - St) .
            
        
    
- Trading venues: Exchanges, dark pools, broker markets, over-the-counter (OTC) markets .
    
- Process of executing trades:
    
    - Get information/quotes .
        
    - Route order (broker selects market) .
        
    - Match and execute (buy/sell orders matched) .
        
    - Confirmation, clearance, and settlement (paperwork, delivery/payment) .
        
    
- Market structures:
    
    - Historically: Open outcry (people shouting orders) .
        
    - Currently: Mostly program trading .
        
    - Continuous markets: Trades run anytime during regular hours (e.g., NYSE) .
        
    - Quote-driven markets: Prices determined by dealers/market makers matching orders from inventory (e.g., bonds, currencies, commodities) .
        
    - Order-driven markets: Based on displayed orders (e.g., stock markets) .
        
    
- Types of investors: Institutional (big funds) and individual (retail) investors .
    
- Market making: Providing quotes (buy/sell prices) for a security to ensure immediate liquidity .
    
    - Market makers take on inventory risk (price drops) .
        
    
- Scalping: Making small, fast profits by active trading, requiring close monitoring and high intensity .
    
- Portfolio rebalancing: Adjusting the proportion of different assets in a portfolio to maintain a desired risk/reward profile due to price changes .
    
- Stock data visualization:
    
    - Key points for a day: Open, high, low, closing prices .
        
    - Candlestick charts: Summarize these four points for each day .
        
        - Bullish (green): Closing price higher than open .
            
        - Bearish (red): Closing price lower than open .
            
        - Shows highest/lowest points (wicks) and real body (open/close range) .
            
        
    

  

## 3.3 Quantitative trading strategies lecture 5.1 - Python programming basics

==This lecture covers essential Python programming basics, including software tools, data types, control flow, functions, and common packages for data processing.==

- Software tools:
    
    - Anaconda: Manages software programs and environments for Python .
        
    - Jupyter Notebook/Lab: Interactive coding environment, allows mixing code and markdown for documentation .
        
    - Google Colab: Online, free Jupyter Notebook platform, good for quick coding without local installation .
        
    
- Why Python for finance?: High readability, simple syntax, strong support from open-source libraries for financial data .
    
- Variables: Placeholders to store values, assigned using the `=` operator .
    
    - Variables are also called objects with attributes and methods .
        
    - Avoid overriding built-in Python functions (e.g., `print`) .
        
    - Naming rules: single word, no spaces, can contain letters/numbers/underscores, cannot start with a number, avoid keywords .
        
    
- Common data types:
    
    - Integer (`int`): Whole numbers .
        
    - Float (`float`): Decimal numbers .
        
    - Boolean (`bool`): `True` or `False`, used for conditional logic .
        
    - String (`str`): Collection of characters .
        
        - Zero-based indexing and slicing using square brackets `[]` .
            
        - Functions like `len()` for length, `in` for substring check, `+` for concatenation .
            
        
    - List: Ordered collection of elements, identified by `[]` .
        
        - Elements can be of different types .
            
        - Accessed by index, can be sliced, checked for element presence, and extended (`append`) .
            
        
    - Dictionary (`dict`): Unordered collection of `key-value` pairs, identified by `{}` .
        
        - Keys are used to access values .
            
        - Values can be updated or new key-value pairs can be added .
            
        
    - NumPy Array: N-dimensional array, fundamental for numerical operations .
        
        - 1D (vector), 2D (matrix), 3D (tensor) .
            
        - Attributes: `ndim` (dimensions), `shape`, `size`, `dtype` .
            
        - Element access by index, supports broadcasting for operations .
            
        
    - Pandas DataFrame: 2D table (like Excel), main data type for financial data .
        
        - Columns for different price points, rows for different days .
            
        - Can be built from dictionaries .
            
        - Attributes: `columns`, `index`, `shape`, `size` .
            
        - Access columns by name (single or list), rows by `loc` (label-based) or `iloc` (position-based) .
            
        - Supports conditional row selection .
            
        
    
- Operators:
    
    - Comparison operators (`>`, `<`, `==`, etc.): Evaluate to `True` or `False` .
        
    - Logical operators (`and`, `or`, `not`): Chain multiple conditions .
        
    
- Control flow (`if-elif-else`): Executes code blocks based on conditions .
    
    - Uses indentation (4 spaces) to define code blocks .
        
    - Conditions are evaluated sequentially .
        
    - Can be written as a concise conditional expression for single conditions .
        
    
- Functions: Reusable blocks of code, defined with `def` .
    
    - Can have optional inputs (parameters) and outputs (return values) .
        
    - Built-in functions (e.g., `print()`, `type()`) and user-defined functions .
        
    
- Packages (Libraries): Collections of modules for specific functionalities.
    
    - Install using `pip install <package_name>` or Anaconda .
        
    - Import using `import <package_name> as <alias>` (e.g., `import numpy as np`) .
        
    
- File I/O: Reading/writing data from/to files.
    
    - `pd.read_csv()`, `pd.read_excel()` for reading .
        
    - `df.to_csv()` for writing .
        
    

  

## 3.4 Quantitative trading strategies lecture 1.3 - downloading and visualizing stock price with Python

==This lecture provides a practical guide to downloading and visualizing stock price data using Python, specifically with Google Colab and the== `yfinance` and `plotly` packages.

- Environment: Google Colab is used as a free online Python coding platform .
    
- Importing packages: Essential libraries like `random`, `numpy`, `pandas`, `yfinance`, and `plotly.graph_objects` are imported .
    
- Random number generation:
    
    - `random.randint(0, 10)` generates a single random integer .
        
    - List comprehension can generate a list of random numbers .
        
    - Zero-based indexing in Python: `range(10)` generates numbers from 0 to 9 .
        
    - Asberg orders: Simulating selecting a few orders from a large list by randomly sampling indices .
        
    
- Analyzing stock data with `yfinance`:
    
    - Install `yfinance` using `!pip install yfinance` .
        
    - Retrieve company information using `yf.Ticker("MSFT").info` .
        
        - Returns a dictionary with key-value pairs (e.g., sector, market cap) .
            
        - Access specific information using the key (e.g., `msft.info['marketCap']`) .
            
        
    - Download historical stock price data using `yf.download("MSFT", start="YYYY-MM-DD", end="YYYY-MM-DD")` .
        
        - Data includes Open, High, Low, Close, Adjusted Close, and Volume .
            
        - `df.head()` shows the first few rows, `df.tail()` shows the last few rows .
            
        - `df.shape` returns the dimensions (rows, columns) of the DataFrame .
            
        
    
- Visualizing stock data with `plotly`:
    
    - Import `plotly.graph_objects as go` .
        
    - Plot stock prices as a line chart: `go.Figure(data=[go.Scatter(x=df.index, y=df['Close'], mode='lines')])` .
        
        - Provides interactive features like hovering for data points and zooming .
            
        
    - Overlay trading volume as a bar chart: Add another `go.Bar` trace .
        
        - Use `secondary_y=True` to plot volume on a separate y-axis .
            
        - Adjust y-axis range to control appearance .
            
        
    - Plot as a candlestick chart: `go.Candlestick(x=df.index, open=df['Open'], high=df['High'], low=df['Low'], close=df['Close'])` .
        
        - Requires Open, High, Low, and Close prices for each day .
            
        - Also interactive for detailed analysis .
            
        
    

  

## 3.5 Quantitative trading strategies lecture 2.1 - electronic order, market order, order matching

==This lecture explains electronic markets, different order types (market, limit, cancellation), order matching systems, and execution precedence.==

- Electronic markets facilitate trading of financial instruments .
    
    - Trades involve taking a long position (buy) or short position (sell) .
        
    - Prices are continuous but discretized into a price grid or price ladder for accounting .
        
    - The minimum tick size is the smallest unit of price movement (e.g., 1 cent for stocks, pips for currencies, basis points for interest rates) .
        
    
- Electronic order details:
    
    - Financial asset: What to trade (e.g., ticker symbol) .
        
    - Direction: Buy, sell, or cancel .
        
    - Size: Quantity of shares or contracts .
        
    
- Order matching system: Exchanges use complex technology to match buy (demand/bids) and sell (supply/asks) orders .
    
    - This process is mostly automated and rule-based .
        
    
- Types of trading:
    
    - Agency trading: A broker executes trades on behalf of a client/investor for a fee (brokerage fee) .
        
        - Accounts for the majority of trades .
            
        
    - Proprietary trading: An agent/broker executes trades for their own institution .
        
    
- Three typical order types:
    
    - Limit order: Not executed immediately; stands until conditions (limit price) are met .
        
        - Includes limit price, order size, and trade direction .
            
        - More complex than market orders .
            
        
    - Market order: Simplest type, executed immediately at the best available price .
        
        - Prioritizes immediacy over a specific price .
            
        - Price is not guaranteed due to market fluctuations, but usually minimal for liquid assets .
            
        - Matched against standing limit orders on the opposing side .
            
        
    - Cancellation order: Cancels an outstanding limit order entirely or reduces its size .
        
    
- Order execution precedence (priority): Most exchanges follow this sequence:
    
    - Price: Highest bids and lowest offers are preferred .
        
        - Highest bid: Buyer willing to pay the most .
            
        - Lowest offer (ask): Seller willing to sell for the least .
            
        
    - Display: Orders that are displayed (visible) are preferred over non-displayed (hidden) orders .
        
    - Time of arrival: First-in, first-out (FIFO) for orders with the same price and display status .
        
    

  

## 3.6 Quantitative trading strategies lecture 2.2 - limit order book, display order

==This lecture focuses on limit orders, the limit order book, and the concept of marketability, along with the distinction between displayed and non-displayed orders.==

- Limit order: An order to buy or sell an asset at a specified price or better .
    
    - For a buy limit order, it triggers if the price drops to or below the specified limit .
        
    - For a sell limit order, it triggers if the price rises to or above the specified limit .
        
    - Risk: The order may never be executed if the price condition is not met .
        
    - Used to control trading prices, especially for less frequently traded or highly volatile assets .
        
    
- Limit order book (LOB): A collection of all standing (unexecuted) limit orders for a specific asset .
    
    - Includes both buy (demand/bids) and sell (supply/asks) sides .
        
    - Orders are removed from the LOB once executed .
        
    - Best offer (best ask): The lowest selling price among all available offers .
        
    - Best bid: The highest buying price among all available bids .
        
    - Bid-ask spread: The difference between the best offer and best bid .
        
        - A large spread indicates less liquid assets or differing valuations .
            
        - A small spread indicates higher liquidity; when bids and offers converge, transactions occur .
            
        
    - Market makers aim to reduce the spread to increase market liquidity .
        
    
- Marketability of limit orders: How likely a limit order is to be executed based on its price relative to the current market.
    
    - For a buy limit order:
        
        - Very marketable: Price is very high (insensitive to price) .
            
        - At the best offer: Price equals the best offer, immediately marketable .
            
        - In the market: Price is between best bid and best offer, uncertain execution .
            
        - At the market: Price equals the best bid .
            
        - Behind the market: Price is lower than the best bid, less competitive .
            
        
    - For a sell limit order:
        
        - Above the market: Price is very high, not attractive to buyers .
            
        - Gradually becomes in the market and then marketable as the selling price decreases .
            
        
    
- Display vs. Non-display orders:
    
    - Display order: Visible on the limit order book .
        
    - Non-display (hidden) order: Not visible, used to avoid revealing large order intentions .
        
    - Non-display orders have lower execution precedence than display orders .
        
    - Exchanges prohibit visible orders from "locking or crossing the market" to maintain bid-ask spreads and avoid disruptions from other markets .
        
    

  

## 3.7 Quantitative trading strategies lecture 2.3 - stop limit order, pegging, trailing stop, price impact

==This lecture covers various advanced order types like stop orders, stop-limit orders, pegging, trailing stops, and market-if-touched orders, along with concepts of fill-or-kill and price impact from large orders.==

- Stop order: A market order conditioned on a preset stop price .
    
    - Buy stop order (stop entry): Triggers a market order to buy if the price rises above a threshold .
        
    - Sell stop order (stop loss): Triggers a market order to sell if the price falls below a threshold, used to limit potential losses .
        
    
- Stop-limit order: A combination of a stop order and a limit order, involving two prices: a stop price and a limit price .
    
    - When the stop price is triggered, it becomes an active limit order .
        
    - The limit order then waits for the price to reach the specified limit price .
        
    - Risk: Not guaranteed to be executed; may "miss the market" if the limit price is not met after the stop is triggered .
        
    
- Pegging order: A limit order with a dynamic limit price .
    
    - The limit price is adjusted dynamically, often relative to a benchmark (e.g., best bid/ask) .
        
    - The trading system constantly checks for changes in the reference price; if changed, the old limit order is canceled, and a new one is set .
        
    
- Trailing stop order: A dynamic stop order used to protect profits in a winning position .
    
    - The stop price automatically adjusts (rises) if the market price moves favorably .
        
    - If the market price falls, the stop price remains unchanged, acting as a safety net .
        
    - When the stop price is hit, a market order is submitted .
        
    
- Market-if-touched (MIT) order: An order to buy or sell an asset if a certain trigger price is touched, then submits a market order .
    
    - Differs from stop orders: MIT typically buys when price falls (entering a long position at a lower price) and sells when price rises .
        
    
- Fill-or-kill (FOK) order: Must be completely filled immediately, or it is canceled entirely .
    
- Immediate-or-cancel (IOC) order: Fills any part of the order immediately, and the remaining (unfilled) portion is canceled .
    
- Price impact: Large orders can move the market price .
    
    - Example: Buying 10,000 shares when only 5,000 are available at the best offer means the remaining 5,000 must be bought at a higher price, increasing the average transaction price .
        
    
- Order flow: Measures the net pressure in the market (more buyers vs. more sellers) .
    
    - If buyer-initiated trades > seller-initiated trades, market is moving up (more demand) .
        
    - If seller-initiated trades > buyer-initiated trades, market is moving down (more supply) .
        
    

  

## 3.8 Quantitative trading strategies lecture 3.1 - risk and return

==This lecture defines risk and return, explores their relationship, introduces different types of traders, and explains how to calculate and annualize returns and risk, culminating in the Sharpe ratio.==

- Risk and Return:
    
    - Investment decisions depend on risk tolerance, time horizon, and ability to replace lost funds .
        
    - Higher returns usually come with higher risk .
        
    
- Types of traders by trading horizon:
    
    - Position traders: Long-term (years), hope for asset price appreciation .
        
    - Swing traders/Day traders: Short-term, speculate on price movements .
        
    
- Risk-Return Quadrants:
    
    - High risk, high return: Stocks, derivatives (speculation) .
        
        - Stocks offer price appreciation and dividends, but dividends are usually less significant than price gains .
            
        
    - Low risk, low return: Fixed income products (guaranteed but lower return) .
        
    - Low risk, high return: Rare, potentially indicates urgent cash needs (which increases default risk) .
        
    - High risk, low return: Undesirable, should be avoided .
        
    
- Calculating Return:
    
    - Return is typically expressed as a percentage to compare different assets .
        
    - Formula: `(Current Price - Previous Price) / Previous Price` .
        
    - Returns are unbounded (can go from negative to positive infinity) .
        
    - Example: Two assets with the same average return but different volatility; the less volatile asset (Asset 1) can lead to higher terminal wealth due to less extreme fluctuations .
        
    - One-plus-R format: `Current Price / Previous Price` .
        
        - Simplifies calculations, especially for cumulative returns .
            
        - Original return can be derived by subtracting 1: `(Current Price / Previous Price) - 1` .
            
        
    - Terminal return (cumulative return):
        
        - `(Terminal Price / Original Price) - 1` .
            
        - Can also be calculated by compounding (multiplying) all one-plus-R period returns: `(1+R0) <em> (1+R1) </em> ... * (1+Rn) - 1` .
            
        
    - Total return: Includes dividends in the numerator: `(Current Price - Previous Price + Dividends) / Previous Price` .
        
    
- Statistical Measures of Data:
    
    - Arithmetic mean: Sum of items divided by count .
        
    - Variance: Average of squared deviations from the mean .
        
        - Sample variance uses `n-1` in the denominator for unbiased estimation .
            
        
    - Standard deviation: Square root of variance, always positive, measures volatility .
        
    
- Annualization: Converting daily/monthly metrics to an annual basis for comparison .
    
    - Annualized variance: Daily variance * 252 (trading days) .
        
    - Annualized standard deviation (volatility): Daily standard deviation * sqrt(252) .
        
        - This is a non-linear relationship .
            
        
    
- Risk-adjusted return:
    
    - Simple `Return / Risk` is a basic measure .
        
    - Sharpe Ratio: `(Return - Risk-Free Rate) / Standard Deviation (Volatility)` .
        
        - Accounts for a risk-free benchmark (e.g., cash accounts) .
            
        - Measures excess return per unit of risk .
            
        
    

  

## 3.9 Quantitative trading strategies lecture 3.2 - calculating return, risk, and annualization

==This lecture provides practical Python implementations for calculating and annualizing risk and return metrics, including Sharpe ratio, using real stock data.==

- Python packages: `numpy` (as `np`) and `pandas` are imported for numerical operations and data manipulation .
    
- Illustrative example: Two time series (Asset 1, Asset 2) with the same mean but different volatility .
    
    - Asset 2 has higher standard deviation, indicating more volatility .
        
    - Despite the same mean return, Asset 1 (less volatile) can result in higher terminal wealth .
        
    
- Wealth process calculation:
    
    - Convert returns to one-plus-R format (add 1 to percentage returns) .
        
    - Use `cumprod()` (cumulative product) to calculate the wealth index over time, scaled by initial investment (e.g., $100) .
        
    
- Converting prices to returns:
    
    - Single-period return: `(price_current / price_previous) - 1` .
        
    - Efficient calculation for all periods:
        
        - Using `iloc` to select shifted price series and perform division .
            
        - Using `.values` to ignore index misalignment during division .
            
        - Using `df.shift(1)` to create a lagged price series for division .
            
        - Using `df.pct_change()`: A convenient pandas function to calculate percentage change (simple returns) in one step .
            
        
    
- Terminal return calculation:
    
    - Convert simple returns to one-plus-R format (`returns + 1`) .
        
    - Calculate cumulative product using `cumprod()` .
        
    - Subtract 1 to get the percentage terminal return .
        
    - Pandas `prod()` function can also calculate the product of all elements in a column .
        
    
- Annualization of returns:
    
    - For daily returns, convert to one-plus-R format, then raise to the power of 252 (trading days in a year) and subtract 1: `(1 + daily_return)^252 - 1` .
        
    - Similar logic for monthly (power of 12) or quarterly (power of 4) returns .
        
    
- Annualization of risk (volatility/standard deviation):
    
    - For daily standard deviation, multiply by the square root of 252: `daily_std * sqrt(252)` .
        
    - This is because standard deviation is in units, not variance .
        
    
- Sharpe Ratio calculation:
    
    - `(Annualized Return - Risk-Free Rate) / Annualized Volatility` .
        
    - Example shows how adjusting for a risk-free rate can change the perceived performance of assets .
        
    
- Working with real data (Apple and Google stocks):
    
    - Download stock prices using `yfinance` for a specified period .
        
    - Extract `Adj Close` prices for multiple tickers .
        
    - Calculate one-plus-R returns using `pct_change()` and `dropna()` .
        
    - Calculate mean returns and standard deviations (column-wise) .
        
    - Manual volatility calculation:
        
        - Calculate deviations from the mean .
            
        - Square deviations .
            
        - Calculate average of squared deviations (variance) .
            
        - Take square root for standard deviation .
            
        - Adjust for sample variance (divide by `n-1`) .
            
        
    - Annualizing real data:
        
        - Annualized volatility: `daily_std * np.sqrt(252)` .
            
        - Annualized return: `((1 + daily_mean_return).prod()<strong>(1/num_trading_days))</strong>252 - 1` (more complex for cumulative daily returns) .
            
        - Calculate Sharpe ratio for real stocks to compare risk-adjusted performance .
            
        
    

  

## 3.10 Quantitative trading strategies lecture 6.1 - log returns and technical indicators

==This lecture introduces log returns as a transformation for easier calculation and mathematical analysis, and sets the stage for trend-following strategies using technical indicators based on momentum.==

- Log Returns:
    
    - A transformation of returns by taking the logarithm, which facilitates calculations .
        
    - Data source: Google stock prices downloaded using `yfinance` .
        
    - Terminal return calculation (traditional):
        
        - `(Last Closing Price / First Closing Price) - 1` .
            
        
    - Terminal return calculation (sequential compounding):
        
        - Calculate single-period percentage returns using `pct_change()` .
            
        - Convert to one-plus-R format (`returns + 1`) .
            
        - Use `cumprod()` (cumulative product) to compound returns over time .
            
        - Subtract 1 to get the simple return format .
            
        - Both methods yield the same terminal return .
            
        
    - Terminal return calculation (using log returns):
        
        - Convert one-plus-R returns to log returns by applying `np.log()` .
            
        - The key difference: instead of `cumprod()`, use `cumsum()` (cumulative summation) on log returns .
            
            - This is because `log(A * B) = log(A) + log(B)`, converting multiplication to addition .
                
            
        - Convert back to original scale by applying `np.exp()` (exponential function) to the cumulative sum .
            
        - Subtract 1 to get the simple return format .
            
        - All three methods produce the same terminal return, verifying equality .
            
        - Advantage of log returns: Addition is mathematically easier to work with than multiplication .
            
        
    
- Trend-Following Strategy:
    
    - A strategy that captures gains/losses by following the momentum of asset prices .
        
    - Momentum has two attributes: direction (up/down) and magnitude (strength) .
        
    - Assumes that existing trends will continue (uptrends to new highs, downtrends to new lows) .
        
    - Uses technical indicators (mathematical calculations based on historical data like price, volume) to generate trading signals (entry/exit points) .
        
    - Technical indicators are manually engineered features, often security-dependent .
        
    - Used to confirm trends or identify range-bound situations .
        
    

  

## 3.11 Quantitative trading strategies lab 1 - working with log returns

==This lab session provides a hands-on guide to calculating simple returns, terminal returns, and log returns using Python's== `yfinance` and `numpy` packages, demonstrating their equivalence for cumulative return calculation.

- Data Acquisition: Google stock data is downloaded for a specific range using `yfinance` .
    
    - The data includes `Close` prices, which will be used for calculations .
        
    
- Simple Returns (Percentage Change):
    
    - Calculated using the `pct_change()` method on a pandas Series (e.g., `df['Close'].pct_change()`) .
        
    - Represents the percentage difference from the previous trading day .
        
    - The first day's return is `NaN` (Not a Number) because there's no prior price for comparison .
        
    
- Terminal Return Calculation:
    
    - Method 1 (Direct): `(Last Price / First Price) - 1` .
        
        - This gives the overall percentage change from the start to the end of the period .
            
        
    - Method 2 (Sequential Compounding):
        
        - Convert daily simple returns to one-plus-R format (`simple_returns + 1`) .
            
        - Calculate the cumulative product of these one-plus-R values using `cumprod()` .
            
        - Subtract 1 from the final cumulative product to get the terminal return in simple return terms .
            
        - The last value of the cumulative return series should match the terminal return from Method 1 .
            
        
    
- Log Returns Calculation:
    
    - Convert simple returns to one-plus-R format (`simple_returns + 1`) .
        
    - Apply the logarithmic transformation using `np.log()` to the one-plus-R returns .
        
    - Key difference for cumulative calculation: Instead of cumulative product, use cumulative sum (`cumsum()`) on log returns .
        
        - This leverages the property `log(A * B) = log(A) + log(B)`, simplifying multiplication to addition .
            
        
    - Convert the cumulative sum of log returns back to the original scale using the exponential function (`np.exp()`) .
        
    - Subtract 1 to get the terminal return in simple return format .
        
    - This method also yields the same terminal return as the previous two methods, confirming their equivalence .
        
    

  

## 3.12 Quantitative trading strategies lecture 6.2 - moving averages and trend following strategy

==This lecture explains simple and exponential moving averages, their calculation, and how they are used to generate trading signals in a trend-following strategy.==

- Moving Averages (Rolling Averages):
    
    - A summary statistic (average) calculated over a fixed window of consecutive data points .
        
    - As new data arrives, the window shifts, dropping the oldest value and adding the newest .
        
    - Effect: Smooths out short-term fluctuations and temporal variations in a time series, revealing longer-term trends .
        
    
- Simple Moving Average (SMA):
    
    - Calculated by summing the prices within the window (N points, including current) and dividing by N .
        
    - Assigns equal weight (1/N) to all data points within the window .
        
    - Window size (N):
        
        - Shorter N: Less smoothing effect, curve closely mimics original price .
            
        - Longer N: More smoothing effect, results in a smoother curve .
            
        
    - Python implementation: `series.rolling(window=N).mean()` .
        
        - The first `N-1` values will be `NaN` due to insufficient data in the window .
            
        
    
- Exponential Moving Average (EMA) / Exponentially Weighted Moving Average (EWMA):
    
    - Assumes recent data has more relevance and assigns it more weight than older data .
        
    - Advantage: Reacts faster to recent price changes, more sensitive to current movements .
        
    - Controlled by an alpha parameter (0 to 1) .
        
        - Formula: `EMA_current = (alpha <em> Current_Price) + ((1 - alpha) </em> EMA_previous)` .
            
        
    - Alpha value:
        
        - Higher alpha (e.g., 0.5): More weight to current price, curve tracks original price closely, less smoothing .
            
        - Lower alpha (e.g., 0.1): More weight to historical EMA, results in a smoother curve .
            
        
    
- Trend-Following Strategy using Moving Averages:
    
    - Generates trading signals based on crossover points of two moving average curves .
        
    - Typically uses a short-term MA (e.g., N=3) and a long-term MA (e.g., N=20) .
        
    - Sell signal: When the short-term MA crosses below the long-term MA .
        
        - Indicates downward momentum, suggesting entering a short position to profit from falling prices .
            
        
    - Buy signal: When the short-term MA crosses above the long-term MA .
        
        - Indicates upward momentum, suggesting entering a long position .
            
        
    - No crossover: Maintain current position .
        
    - This is an absolute momentum strategy, focusing solely on an asset's own historical data .
        
    

  

## 3.13 Quantitative trading strategies lab 2 - simple and exponential smoothing averages

==This lab demonstrates the practical implementation of Simple Moving Average (SMA) and Exponential Moving Average (EMA) using Python's== `pandas` library, illustrating how different window sizes and alpha values affect smoothing.

- Data Preparation: Apple stock data is downloaded using `yfinance` for a specified period .
    
    - The index is converted to `datetime` format for easier time-series analysis and plotting .
        
    - Focus is on the `Adjusted Close` price .
        
    
- Simple Moving Average (SMA) Calculation:
    
    - Specify a `window_size` (e.g., 3 or 20) .
        
    - Use the `rolling()` method on the `Adjusted Close` series, followed by `.mean()`: `df['Adj Close'].rolling(window=window_size).mean()` .
        
    - Each value in the SMA column is the average of the current and previous `window_size - 1` values .
        
    - The first `window_size - 1` values will be `NaN` because there aren't enough preceding data points .
        
    - Verification: Manually calculate the mean of the first `window_size` values to confirm the SMA calculation .
        
    - `min_periods` parameter: Setting `min_periods=1` allows calculation even if the window doesn't have `window_size` values, using whatever data is available .
        
    - Visualization: Plotting SMA-3 and SMA-20 alongside the original `Adjusted Close` shows that a larger window (SMA-20) produces a much smoother curve, while a smaller window (SMA-3) tracks the original price more closely .
        
    
- Exponential Moving Average (EMA) Calculation:
    
    - Specify an `alpha` parameter (e.g., 0.1 or 0.5) instead of a window size .
        
    - Use the `ewm()` (exponentially weighted moving average) method on the `Adjusted Close` series, followed by `.mean()`: `df['Adj Close'].ewm(alpha=alpha, adjust=False).mean()` .
        
    - EMA assigns more weight to recent values and less to older values, with weights decreasing exponentially .
        
    - Verification: Manually calculate the EMA for a specific point using the formula `EMA_current = (alpha <em> Current_Price) + ((1 - alpha) </em> EMA_previous)` .
        
    - Visualization: Plotting EMA-0.1 and EMA-0.5 shows that a lower alpha (0.1) results in a smoother curve (more weight to historical), while a higher alpha (0.5) tracks the original price more closely (more weight to current) .
        
    - These smoothed curves are crucial for generating trading signals in strategies like trend following .
        
    

  

## 3.14 Quantitative trading strategies lab 3 - implementing the trend following strategy

==This lab demonstrates the implementation of a trend-following strategy in Python, including generating trading signals from moving average crossovers, calculating log returns for the strategy, and comparing its performance against a buy-and-hold baseline.==

- Data Setup: The DataFrame contains daily stock prices (`Adjusted Close`) and derived Simple Moving Average (SMA) curves (e.g., SMA-3 for short-term, SMA-20 for long-term) .
    
- Generating Trading Signals:
    
    - The signal identifies the position to hold (long, short, or neutral) based on the relationship between short-term and long-term moving averages .
        
    - Buy signal (long position): When the short-term MA is greater than the long-term MA, indicating upward momentum. Assigned a value of `1` .
        
    - Sell signal (short position): When the short-term MA is less than the long-term MA, indicating downward momentum. Assigned a value of `-1` .
        
    - Neutral signal: When they are equal or no clear trend. Assigned a value of `0` .
        
    - `np.where()` function is used to create this `signal` column .
        
    - `dropna()` removes `NaN` values .
        
    - `value_counts()` shows the frequency of each signal (e.g., more `-1` signals if the market is generally going down) .
        
    
- Calculating Log Returns for Baseline (Buy-and-Hold) Strategy:
    
    - The buy-and-hold strategy assumes holding one unit of the asset throughout the period .
        
    - Log returns are calculated by taking the logarithm of the `Adjusted Close` price and then taking the difference (`.diff()`) .
        
        - `log(P_t) - log(P_{t-1}) = log(P_t / P_{t-1})`, which is the log of the one-plus-R return .
            
        
    - This creates a `log_returns_buy_hold` column .
        
    
- Calculating Log Returns for Trend-Following Strategy:
    
    - The log returns for the trend-following strategy are calculated by multiplying the `log_returns_buy_hold` by the `signal` column .
        
    - This captures profits/losses based on the trading signal:
        
        - If `log_returns_buy_hold` is positive (price up) and `signal` is `1` (long), it's a profit.
            
        - If `log_returns_buy_hold` is negative (price down) and `signal` is `-1` (short), it's also a profit.
            
        - If `log_returns_buy_hold` is positive (price up) and `signal` is `-1` (short), it's a loss.
            
        - If `log_returns_buy_hold` is negative (price down) and `signal` is `1` (long), it's a loss .
            
        
    - This creates a `log_returns_trend_following` column .
        
    
- Deriving Trading Actions:
    
    - Trading actions (e.g., "go long," "go short," "close position") are derived by taking the difference of the `signal` column (`signal.diff()`) .
        
    - `value_counts()` on `signal.diff()` shows the frequency of different actions (e.g., `2` for short-to-long, `-2` for long-to-short) .
        
    - These actions can be plotted on the price chart to visualize entry/exit points .
        
        - Assumes immediate closing of current position and opening of new position .
            
        
    
- Comparing Strategy Performance (Wealth Curve):
    
    - Convert log returns back to normal (one-plus-R) returns using `np.exp()` .
        
    - Calculate the cumulative product (`cumprod()`) of these normal returns to get the wealth curve for both strategies .
        
    - Plotting the wealth curves shows the evolution of portfolio value over time for each strategy .
        
    - The trend-following strategy often outperforms buy-and-hold, but this depends on assumptions and market conditions .
        
    
- Comparing Terminal Returns:
    
    - Extract the last value of the wealth curve for each strategy and convert it back to simple return format (subtract 1) .
        
    - This provides a final comparison of the total return generated by each strategy .
        
    

  

## 3.15 Quantitative trading strategies lecture 7.1 - momentum trading strategy

==This lecture introduces momentum trading strategy, emphasizing its cross-sectional nature and comparison of multiple assets, contrasting it with the time-series-based trend-following strategy.==

- Momentum Trading Strategy:
    
    - A strategy that uses the strength of price movements to identify relatively performing assets .
        
    - Involves buying/selling selected assets based on recent price trends, assuming these trends will continue .
        
    - Focuses on "driver assets" with sufficient momentum .
        
    - Key factors: volume, volatility, and time frame .
        
    
- Cross-Sectional Nature:
    
    - Distinction from trend-following: Momentum trading is cross-sectional, meaning it compares the momentum of multiple assets at a specific point in time .
        
        - It selects assets with high relative momentum (e.g., top 5 performers) .
            
        
    - Trend-following strategy: Uses time series momentum, focusing on a single asset's historical returns (absolute momentum) .
        
    
- Windows in Momentum Trading:
    
    - Look-back window: A uniform period (e.g., 6 months) used to assess the historical relative performance (cumulative return) of multiple assets .
        
    - Look-ahead window: A uniform period (e.g., 1 month) used to determine the holding period for the selected positions and evaluate performance .
        
    
- Strategy Workflow:
    
    - At a given time point, define a look-back window (e.g., 6 months) to measure a metric (e.g., cumulative return) for multiple assets .
        
    - Based on this metric, identify top performers (e.g., top 20th percentile) to go long, and bottom performers (e.g., bottom 20th percentile) to go short .
        
    - Hold these positions for a defined look-ahead window (e.g., 1 month) .
        
    - Repeat the process at the next time point (e.g., next month) .
        
    - The "trade formation period" is when the decision is made, and the "evaluation period" (or performance period) is when the performance is measured .
        
    
- Comparison with Trend Following (Recap):
    
    - Trend following uses two look-back windows (short-term and long-term) to generate moving averages .
        
    - Trading signals are generated when these moving averages cross over .
        
    - The trading interval is not fixed; it's purely data-driven based on crossover conditions .
        
    
- Calculating Profits:
    
    - Total profits for momentum strategy = (Average return from long positions) - (Average return from short positions) .
        
    

  

## 3.16 Quantitative trading strategies lecture 7.2 - max drawdown

==This lecture introduces Maximum Drawdown (Max Drawdown) as a crucial risk measure, specifically for downside risk, explaining its calculation, interpretation, and limitations.==

- Max Drawdown Definition:
    
    - Measures the maximum loss in percentage terms from a previous high (peak wealth) to a subsequent low (trough wealth) .
        
    - It quantifies the worst return an investor could have experienced from a peak in historical data .
        
    - It's a hypothetical value indicating the worst-case scenario, not necessarily the actual return .
        
    
- Importance:
    
    - Unlike Sharpe ratio, which treats upside and downside risk equally, Max Drawdown specifically measures downside risk .
        
    - Helps assess how bad extreme losses could be .
        
    
- Calculation Steps:
    
    1. Start with asset prices (daily/monthly) .
        
    2. Convert to daily/monthly percentage returns .
        
    3. Formulate a wealth index: Represents the evolution of portfolio value over time (e.g., starting with $1) .
        
    4. Calculate cumulative peak wealth: The highest wealth value achieved up to any given point in time .
        
    5. Calculate daily/monthly drawdown: Percentage difference between the cumulative peak and the current wealth value .
        
    6. Extract Max Drawdown: The minimum (most negative) value from the drawdown curve .
        
        - Usually reported as a positive number .
            
        
    
- Visualization:
    
    - A graph shows the `wealth index` (portfolio value), `cumulative max` (green line tracking peaks), and `drawdown curve` (gap between peak and current value) .
        
    
- Downsides/Limitations of Drawdown Risk:
    
    - High sensitivity to inputs: Relies on current wealth and historical peak, making it sensitive to outliers (sudden price jumps/drops) .
        
    - Dependency on observation frequency: More granular data (daily/hourly) tends to exhibit higher volatility and thus potentially higher Max Drawdown compared to less granular data (monthly) .
        
    
- Example (Google and Microsoft):
    
    - Illustrates calculation using daily returns for Google and Microsoft .
        
    - Shows how a significant price drop (e.g., Google's Bard product introduction) leads to a large drawdown .
        
    

  

## 3.17 Quantitative trading strategies lecture 9.1 - forward contract, futures contract, clearing house

==This lecture defines forward and futures contracts as derivative products, explains their mechanisms, key parameters, and the crucial role of a clearing house in mitigating counterparty risk.==

- Forward and Futures Contracts:
    
    - Both are derivative products, meaning their value is derived from an underlying asset .
        
    - They obligate the buyer to buy and the seller to sell a predetermined quantity of an underlying asset at a predetermined delivery date and price .
        
    - Purpose: Eliminate future price uncertainty, used for hedging risk or speculation .
        
    
- Futures Contracts:
    
    - Traded through centralized futures exchanges .
        
    - The exchange acts as a middleman, providing liquidity and eliminating counterparty risk (risk that the opposing party defaults) .
        
    - Exchanges profit by maintaining a small spread between buyer and seller prices .
        
    - Requires opening and maintaining a margin account as insurance against adverse price movements .
        
    - Underlying assets can be physical (e.g., grain, oil) or non-physical (e.g., currency, securities) .
        
    - Futures contracts are tradable like stocks, often traded out before settlement for hedging .
        
    
- Forward Contracts:
    
    - Traded over-the-counter (OTC), directly between two parties .
        
    - Higher counterparty risk compared to futures .
        
    
- Parameters of a Futures Contract:
    
    - Lot size: Predetermined quantity of the underlying asset per contract (e.g., 1 futures contract = 100 stocks) .
        
    - Contract value: Total value of the contract = Lot Size * Price of Underlying Asset .
        
    - Margin: Amount deposited by the investor to enter the position .
        
        - Initial margin: Deposit required at the start .
            
        - Daily settlements: Daily adjustments to the margin account based on price fluctuations .
            
        - Maintenance margin: Threshold; if margin account falls below this, a margin call is issued to top up to the initial margin .
            
        
    - Expiration date (delivery date/settlement date): Date of actual delivery or cash settlement .
        
        - Physical delivery: Buyer pays agreed price, seller delivers underlying asset .
            
        - Cash settlement: Net cash position transferred between parties, often due to mark-to-market adjustments .
            
        
    
- Clearing House:
    
    - An intermediary between buyer and seller in financial markets .
        
    - Guarantees transactions happen as planned, eliminating counterparty risk .
        
    - Achieves this by imposing margin requirements on both parties .
        
    - Manages daily fluctuations in asset price through margin calls .
        
    - Illustrates the flow of goods and funds between buyer, clearing house, and seller .
        
    

  

## 3.18 Quantitative trading strategies lecture 9.2 - mark to market, daily settlement of futures contract

==This lecture details the mark-to-market process and daily settlements for futures contracts, explaining how margin accounts are adjusted based on price fluctuations and the role of margin calls.==

- Daily Settlements (Mark-to-Market):
    
    - The futures exchange adjusts margin accounts daily based on fluctuations in the underlying asset's price .
        
    - This adjustment is between the long and short position holders, meaning the exchange itself takes no risk .
        
    
- Mechanism for a Long Position Holder:
    
    - If the market price of the asset increases (bullish outlook), the long position holder realizes a profit .
        
        - Money is debited from the short position holder's margin account and credited to the long position holder's margin account .
            
        
    - If the market price of the asset decreases, the long position holder suffers a loss .
        
        - Money is debited from the long position holder's margin account and credited to the short position holder's margin account .
            
        
    
- Margin Calls:
    
    - If a party's margin account balance falls below the maintenance margin threshold, they receive a margin call from the exchange .
        
    - The party must then top up their margin account to the initial margin level .
        
    
- Concrete Example:
    
    - Initial margin: $100 for both long and short positions .
        
    - Maintenance margin: $90 .
        
    - Day 1: Asset price increases, long position holder gains $5.
        
        - Long account: $100 + $5 = $105.
            
        - Short account: $100 - $5 = $95 .
            
        
    - Day 2: Asset price drops by $20, long position holder loses $20.
        
        - Long account: $105 - $20 = $85.
            
        - Short account: $95 + $20 = $115 .
            
        
    - Since the long account ($85) is below the maintenance margin ($90), the long position holder receives a margin call .
        
    - The long position holder must deposit $5 ($90 - $85) to bring the account back to $90 .
        
    - Daily settlements continue for subsequent days .
        
    

  

## 3.19 Quantitative trading strategies lecture 9.3 - no-arbitrage pricing for forward & futures contract

==This lecture explains the no-arbitrage pricing principle for forward and futures contracts, demonstrating how their fair price is determined by replicating the payoff using underlying assets and risk-free investments, and discusses additional costs for futures.==

- No-Arbitrage Pricing (Pricing by Replication):
    
    - The core principle is that there should be no opportunity for riskless profit (arbitrage) .
        
    - If you start with zero money, you should end with zero money .
        
    
- Pricing a Forward Contract:
    
    - To price a long forward contract (obligation to buy an asset at future price F), a replicating portfolio is constructed .
        
    - Replicating portfolio:
        
        1. Short the underlying stock (S): This hedges the risk of the forward contract. If the stock price drops, the short position profits, offsetting losses from the long forward .
            
        2. Invest the proceeds from shorting in a cash account: This earns the risk-free interest rate (R) until the delivery date (T) .
            
        
    - Portfolio value at time t (start):
        
        - Forward contract: 0 .
            
        - Short stock: -S_t (negative because it's a liability to close) .
            
        - Cash account: +S_t (proceeds from shorting) .
            
        
    - Portfolio value at time T (delivery):
        
        - Short stock: -S_T (need to buy back at spot price) .
            
        - Cash account: +S_t _e^(R_T) (compounded at risk-free rate) .
            
        - Long forward: S_T - F (receive asset, pay F) .
            
        
    - By the no-arbitrage principle, the initial portfolio value (0) must equal the terminal portfolio value .
        
    - Setting the sum of terminal values to zero and solving for F gives the fair forward price: `F = S_t <em> e^(R</em>T)` (for continuous compounding) .
        
    - Intuition: Investing in a forward contract is equivalent to buying the stock and earning the risk-free rate on the initial investment .
        
    
- Arbitrage Opportunities (if price deviates):
    
    - If F > S_t _e^(R_T) (forward is overpriced):
        
        - Strategy: Buy low, sell high. Borrow S_t, buy the stock, and short the forward contract .
            
        - This results in a riskless profit (arbitrage) .
            
        
    - If F < S_t _e^(R_T) (forward is underpriced):
        
        - Strategy: Go long the forward contract and sell (short) the underlying asset .
            
        - This also results in a riskless profit .
            
        
    
- Pricing a Futures Contract:
    
    - The formula for futures pricing is similar to forwards but includes additional terms for physical assets (annual compounding example) .
        
    - Storage cost (S): Added to the futures price. If holding a physical asset for delivery, there's a cost to store it (e.g., oil barrels) .
        
    - Convenience yield (C): Subtracted from the futures price. This is a benefit of holding the physical asset, especially if it's in high demand (e.g., oil price increase due to demand) .
        
    - The formula adjusts for these costs/benefits over the duration (T) .
        
    

  

## 3.20 Quantitative trading strategies lecture 9.4 - contango and backwardation

==This lecture defines and illustrates the market phenomena of contango and backwardation in futures contracts, explaining how futures prices relate to spot prices and their convergence over time.==

- Contango:
    
    - Occurs when the futures contract price is higher than the current spot price of the underlying asset .
        
    - Also, normal contango means the futures price is higher than the expected future spot price .
        
    - Describes a bull market expectation, where asset prices are expected to increase .
        
    - Price dynamics:
        
        - At a given time, futures contracts with longer maturities have higher prices .
            
        - Over time, the futures price for a specific contract will gradually converge downwards to the spot price as it approaches its maturity date .
            
            - At maturity, the futures price must equal the spot price .
                
            
        
    
- Backwardation:
    
    - Occurs when the futures contract price is lower than the current spot price of the underlying asset .
        
    - Also, normal backwardation means the futures price is lower than the expected future spot price .
        
    - Describes a bearish perspective on future asset prices .
        
    - Price dynamics:
        
        - At a given time, futures contracts with longer maturities have lower prices .
            
        - Over time, the futures price for a specific contract will gradually converge upwards to the spot price as it approaches its maturity date .

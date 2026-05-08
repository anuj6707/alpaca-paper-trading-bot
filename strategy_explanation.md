# Strategy Explanation 📈

## 📌 Core Strategy Concept

This trading bot uses a multi-indicator momentum and trend-following strategy designed for short-term intraday paper trading.

Instead of relying on a single signal, the system combines:

* RSI momentum confirmation
* MACD trend confirmation
* SMA trend filtering

The goal is to identify strong momentum setups while filtering weaker trades.

---

## 🧠 Indicators Used

### 1. RSI (Relative Strength Index)

The bot uses a 7-period RSI to measure short-term momentum.

### Buy Condition

```text
RSI crosses above 55
```

This suggests increasing bullish momentum.

---

### 2. MACD (Moving Average Convergence Divergence)

The MACD indicator is used for momentum confirmation.

### Buy Confirmation

```text
MACD > Signal Line
```

This helps confirm trend strength before entering trades.

---

### 3. SMA (Simple Moving Average)

A 20-period SMA is used as a trend filter.

### Trend Filter

```text
Current Price > SMA
```

This ensures trades are only taken when price is above the short-term moving average trend.

---

## ⚙️ Entry Logic

A trade is entered only when ALL conditions are satisfied:

```text
1. RSI crosses above 55
2. MACD is above signal line
3. Price is above SMA
```

The bot then ranks setups using a momentum-based scoring system.

---

## 📊 Dynamic Universe Selection

The bot does not scan random stocks.

Instead, it dynamically selects high-volume stocks from a predefined universe.

### Selection Process

* Fetch recent market data
* Calculate dollar volume
* Rank stocks by liquidity
* Select top-volume candidates

This improves:

* liquidity
* execution quality
* trade consistency

---

## 🛡️ Risk Management

The bot includes several built-in safeguards.

### Stop Loss

```text
-1%
```

### Take Profit

```text
+2.5%
```

### Position Limits

* Maximum simultaneous positions: 6
* Prevents overexposure

### Duplicate Trade Prevention

Stocks already traded during the day are skipped.

### Low Price Filter

Stocks below $10 are ignored to avoid highly volatile low-priced equities.

---

## ⏰ Intraday Trading Window

The bot trades only during a controlled morning session:

```text
9:30 AM → 11:30 AM EST
```

This period typically contains:

* higher liquidity
* stronger momentum
* increased volatility

---

## 🔄 Position Monitoring

Open positions are continuously monitored in real time.

Positions are automatically closed when:

* stop loss is hit
* take profit is hit
* forced end-of-day exit occurs

---

## 📁 Trade Logging

All completed trades are stored in:

```text
trades.csv
```

Logged information includes:

* timestamp
* symbol
* entry price
* exit price
* PnL percentage

---

## 📈 Performance Tracking

The bot tracks:

* total trades
* win rate
* cumulative PnL

This allows basic performance evaluation over time.

---

## 🚀 Future Improvements

Potential upgrades include:

* advanced risk management
* trailing stop losses
* backtesting engine
* dashboard visualization
* machine learning-based signal filtering
* portfolio-level analytics

---

## ⚠️ Disclaimer

This strategy is designed for educational and paper trading purposes only.

Past performance does not guarantee future results.


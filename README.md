# Alpaca Algorithmic Trading Bot 📈🚀

## 📌 Overview

This project is an automated algorithmic paper trading bot built using the Alpaca API.

The bot scans a dynamic universe of high-volume stocks, calculates technical indicators in real time, generates trading signals, executes paper trades automatically, and tracks performance statistics.

The project was built to explore:

* algorithmic trading systems
* technical analysis
* API integration
* automated trade execution
* portfolio and risk management concepts

---

## ⚙️ Features

* Automated paper trading using Alpaca API
* Dynamic stock universe selection
* Real-time market scanning
* RSI + MACD + SMA strategy confirmation
* Duplicate trade prevention
* Maximum position management
* Stop-loss and take-profit exits
* Force exit before market close
* Trade logging to CSV
* Win rate and PnL tracking

---

## 🧠 Trading Strategy

The bot combines multiple technical indicators for trade confirmation:

### Entry Conditions

* RSI crosses above threshold
* MACD bullish confirmation
* Price above SMA trend filter

### Exit Conditions

* Stop loss: -1%
* Take profit: +2.5%
* Forced exit before market close

Additional safeguards were implemented to:

* avoid duplicate trades
* limit simultaneous positions
* avoid low-priced stocks

More strategy details can be found in:

```text
strategy_explanation.md
```

---

## 🛠️ Technologies Used

* Python
* Alpaca API
* Pandas
* NumPy
* TA (Technical Analysis library)
* CSV Logging

---

## 📁 Project Structure

```text
alpaca-paper-trading-bot/
│
├── bot.py
├── strategy_explanation.md
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 🚀 Setup

Install dependencies:

```bash
pip install -r requirements.txt
```

Add your Alpaca paper trading API keys inside:

```python
API_KEY = "YOUR_API_KEY"
SECRET_KEY = "YOUR_SECRET_KEY"
```

Run the bot:

```bash
python bot.py
```

---

## 📊 Performance Tracking

The bot tracks:

* total trades
* win rate
* cumulative PnL
* CSV trade history

Trade logs are automatically stored in:

```text
trades.csv
```

---

## ⚠️ Disclaimer

This project is intended for educational and paper trading purposes only.

It is not financial advice and should not be used for live trading without proper testing and risk management.

---

## 🚀 Future Improvements

* Backtesting engine
* Dashboard visualization
* Email / Telegram alerts
* Advanced risk management
* Multi-timeframe analysis
* Machine learning-based signal filtering

---

## 👤 Author

Built as part of a personal learning journey focused on automation, trading systems, and quantitative strategy development.


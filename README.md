# 📉 Gap Down Recovery Strategy - NIFTY 500 Stocks

A Python-based backtesting framework that implements the **Gap Down Recovery** strategy on **NIFTY 500** stocks using historical data from Yahoo Finance. This project helps analyze the effectiveness of a simple price-action-based trading strategy with fixed parameters.

---

## 📌 Strategy Overview

The **Gap Down Recovery Strategy** is a momentum-based trading technique that:

1. **Detects a gap down** in a stock — when the stock opens significantly lower than the previous day’s closing price.
2. **Waits for a recovery** of a specific percentage.
3. **Enters a trade** on confirmation of recovery.
4. **Exits** based on a target profit, stop loss, or after a maximum holding period.

---

## ⚙️ Strategy Parameters

| Parameter       | Value        | Description                                                 |
|-----------------|--------------|-------------------------------------------------------------|
| Gap Down %      | -2.0%        | Stock must open at least 2% lower than previous close       |
| Recovery %      | +2.0%        | Recovery of at least 2% after gap down                      |
| Target Profit   | +10.0%       | Exit trade if price increases by 10%                        |
| Stop Loss       | -5.0%        | Exit trade if price drops by 5%                             |
| Max Hold Days   | 60 days      | Exit trade if TP/SL not hit within 60 trading days          |

---

## 📁 Files in This Repository

| File                            | Description |
|---------------------------------|-------------|
| `Gap_Down.ipynb`                | Jupyter Notebook with full strategy code and analysis |
| `gap_down_recovery_trades.xlsx` | Excel file with results of trades executed by the strategy |
| `NIFTY500_2.csv`                | CSV file containing list of NIFTY 500 stock symbols |
| `README.md`                     | You're reading it! Project overview and usage instructions |

---

## 🧠 Requirements

Ensure you have the following Python libraries installed:
pip install pandas numpy yfinance tqdm openpyxl

## 🚀 How to Use
Clone this repository:

git clone https://github.com/yourusername/gap-down-recovery-strategy.git
cd gap-down-recovery-strategy

## Open the notebook:
jupyter notebook Gap_Down.ipynb

## Make sure NIFTY500_2.csv is in the correct path. Modify the path if needed.

Run all cells. It will:

Download 5 years of daily stock data for each symbol

Execute trades based on strategy

Export results to gap_down_recovery_trades.xlsx

## 📊 Output Example
The final output Excel file will contain the following columns:

Stock: Stock symbol

Entry_Date: Date when trade was entered

Entry_Price: Price at entry

Exit_Date: Exit date

Exit_Price: Exit price

PnL_%: Profit or Loss percentage

Days_in_Trade: Number of days trade was held

Result: WIN, LOSS, or HOLD_EXIT

Also printed:

Total number of trades

Number of winning trades

Win rate (%)

## 🧾 Disclaimer
This project is for educational purposes only. It does not constitute financial advice. Backtesting results are hypothetical and do not reflect real-world performance.

## 👤 Author
Priyatanshu Ghosh
PGDM Candidate | Data & Finance Enthusiast

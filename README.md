
# 📊 Factor-Based Equity Screener

A beginner-level quantitative finance project that screens stocks based on fundamental factors like Value, Momentum, and Quality. It also performs basic backtesting using Backtrader.

---

## 🔍 Overview

This project allows users to:

- Load factor-based CSV files for multiple stocks
- Rank stocks by a custom composite score
- Run a simple long/short strategy: Buy top-N and short bottom-N based on factor scores
- Visualize portfolio performance over time

---

## 🧠 Project Goals

- Demonstrate knowledge of quantitative investing principles
- Practice building simple backtests
- Combine programming and finance fundamentals

---

## 🛠 Features

- **Factor Implementation**:
  - Value: e.g., Price/Earnings (P/E), Price/Book (P/B)
  - Momentum: e.g., 6M or 12M price change
  - Quality: e.g., Return on Equity (ROE), Debt/Equity ratio

- **Custom Ranking**:
  - Combine factors into a composite score with weights
  - Filter and rank stocks based on this score

- **Backtesting**:
  - Strategy rebalances every N days
  - Buys top-N stocks, shorts bottom-N
  - Visualizes equity curve

---

## 🚀 Getting Started

### 1. Clone the Repo
```bash
git clone https://github.com/your-username/factor-screener.git
cd factor-screener
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```
Or manually:
```bash
pip install pandas matplotlib backtrader
```

### 3. Add Data
Place your stock factor CSVs into the `data/factor_csvs/` directory.

### 4. Run the Backtest
```bash
python main.py
```
Expected Output:
```yaml
Starting Portfolio Value: 100000.00
Final Portfolio Value: 102450.00
Plot saved to backtest_plot.png
```

---

## 🔁 Strategy Logic

```python
# Every N days, rebalance:
- Sort stocks by composite_score
- Buy top N (long)
- Sell bottom N (short)
- Close all previous positions
```

---

## 📁 Project Structure

```
factor-screener/
├── data/
│   └── factor_csvs/        # CSVs for each stock
├── main.py                 # Main backtesting script
├── backtest_plot.png       # Saved plot (after running)
└── README.md               # Project documentation
```

---

## 🧪 Skills Demonstrated

- Data wrangling with Pandas  
- Financial metrics and factor analysis  
- Quantitative backtesting using Backtrader  
- Headless plotting with Matplotlib  
- Object-oriented design for trading strategies  

---

## 🔮 Planned Improvements

- Integrate real-time financial data APIs (e.g., Yahoo Finance, Alpha Vantage)  
- CLI support to configure factors and weights  
- Add performance metrics (Sharpe, Max Drawdown, Volatility)  
- Interactive screener using Streamlit  

---

## 📄 License

This project is licensed under the MIT License.

---

## 🤝 Acknowledgements

Built with ❤️ to showcase the blend of finance and software engineering.

- [Backtrader](https://www.backtrader.com/)  
- [Matplotlib](https://matplotlib.org/)  
- [Pandas](https://pandas.pydata.org/)  

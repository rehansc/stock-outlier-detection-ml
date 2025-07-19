# Quant Insights AI

“A system that detects trading signals from price anomalies and news sentiment — inspired by quantitative hedge funds like Renaissance Technologies.”

# 📈 Stock Outlier Detection with Machine Learning

Unsupervised machine learning project to identify **unusual stock price behavior** using clustering and dimensionality reduction techniques. Inspired by the strategies of investors like Michael Burry and Jim Simons, this project explores patterns in stock volatility, returns, and technical indicators to detect potential anomalies or breakout candidates.

---

## 🚀 Project Goals

- Fetch real-world stock data using the `yfinance` API *(or Alpha Vantage/Stooq as a free alternative)*
- Engineer features such as volatility, returns, and technical indicators
- Apply dimensionality reduction (PCA, t-SNE) for visualization
- Use clustering (KMeans, DBSCAN) to group similar stocks
- Detect **outliers** that show unique or abnormal trading behavior
- Visualize results and highlight potentially interesting stocks

---

## 🛠️ Tools & Libraries

- Python, Pandas, NumPy
- Alpha Vantage or Stooq (stock data)
- scikit-learn (clustering, PCA)
- seaborn, matplotlib (visualization)
- Databricks (optional for scaling / Spark ML)

---

## 🧠 Key Features Extracted

- Daily % returns
- Rolling volatility (7, 30-day)
- MACD / RSI (optional)
- Cumulative returns
- Sharpe-like metrics (for anomaly detection)

---

## 📁 Project Structure

```
stock-outlier-detection-ml/
├── data/
│   ├── raw/               # Fetched CSVs (Stooq or similar)
│   └── processed/         # Feature-engineered, clustered, and sentiment-scored data
├── notebooks/
│   ├── 1_data_fetch.ipynb              # Pull stock prices
│   ├── 2_feature_engineering.ipynb     # Compute returns, volatility, etc.
│   ├── 3_clustering.ipynb              # Apply PCA, KMeans, DBSCAN
│   ├── 4_visualization.ipynb           # Plot clusters, returns, volatility
│   └── 5_news_sentiment.ipynb          # Fetch headlines, run FinBERT, join with price data
├── README.md
├── requirements.txt
└── .gitignore

```

---

## 📊 Sample Output (Coming Soon)

- 2D cluster plots
- Highlighted outliers
- Annotated findings

---

## 📌 Status

- [x] Project planned  
- [ ] Data pulled  
- [ ] Feature engineering in progress  
- [ ] Clustering and visualization pending

---

## 🧠 Future Work

- Time-series anomaly detection
- Incorporate fundamentals (P/E, EPS)
- Compare clusters to earnings/sentiment news

---

## 📬 Contact

Built by [Rehan Chaudhry](https://github.com/rehansc) — exploring the intersection of **ML + Markets**.  
Open to feedback, forks, and collaboration!


# 📈 Stock Outlier Detection with Machine Learning + News Sentiment

_A hands-on project combining financial ML techniques and NLP-based sentiment analysis to identify unusual stock behaviors and media impact._


---


## 🚀 Project Highlights

- 📊 Analyze 5 major stocks: **Tesla, Microsoft, Google, Amazon, Apple**
- 🧮 Compute daily return, rolling volatility, and cumulative return
- 🧠 Apply **PCA**, **KMeans**, and **DBSCAN** to detect outliers
- 🗞️ Pull real headlines using **NewsAPI** and analyze with **FinBERT**
- 🔍 Correlate news **volume** and **sentiment** with stock behavior
- 📈 Visualize insights with static, publication-ready plots

---

## 🛠️ Tools & Libraries

- **Python**, **Pandas**, **NumPy**
- **scikit-learn** (PCA, KMeans, DBSCAN)
- **matplotlib**, **seaborn** (visuals)
- **NewsAPI** (headline scraping)
- **FinBERT** (financial sentiment analysis, via Hugging Face)
- ✅ Future-compatible with **Databricks**

---

## 🧠 Key Features Used

| Feature | Description |
|--------|-------------|
| `daily_return` | % change from previous close |
| `volatility_7`, `volatility_30` | Rolling standard deviation of returns |
| `cum_return` | Cumulative compounded return |
| `sentiment` | Per-headline positive, neutral, negative scores from FinBERT |
| `news_volume` | Count of headlines per company per window |



---

## 📁 Project Structure

```
stock-outlier-detection-ml/
├── data/
│   └── raw/
│   └── processed/
├── notebooks/
│   └── 1_data_fetch.ipynb
│   └── 2_feature_engineering.ipynb
│   └── 3_clustering.ipynb
│   └── 4_visualization.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

-
---

## 🧪 Sample Insights

- ✅ Tesla and Microsoft flagged as **behavioral outliers**
- 🔄 Amazon, Apple, and Google cluster as **low-volatility, steady return**
- 🧠 News sentiment aligned with recent volatility spikes
- 📰 Tesla generated highest media attention, but sentiment was mixed

## 📘 Metric Ranges: How to Interpret Stock Behavior

This section defines qualitative thresholds for the core features used in clustering. These are based on typical market behavior and your dataset's distribution.

| Feature           | Low                  | Moderate               | High / Anomalous       | Notes |
|-------------------|----------------------|-------------------------|-------------------------|-------|
| **Daily Return**  | < -0.5%              | -0.5% to +0.5%          | > +0.5%                | Short-term price change |
| **Volatility (7d)** | < 1% (`< 0.01`)     | 1%–3% (`0.01–0.03`)     | > 3% (`> 0.03`)        | Measures recent price instability |
| **Volatility (30d)** | Same as 7d         |                         |                         | Longer-term instability |
| **Cumulative Return** | < 500             | 500–2,000               | > 2,000                | Total price growth since start |

---

### 🧠 Interpretation Guidelines

- **Cluster 0** → 🟢 *Low volatility, high cumulative return*  
  → Reliable long-term performer (e.g. MSFT)

- **Cluster 1** → 🔴 *High volatility, high daily return, low cumulative*  
  → Speculative or hype-driven behavior (e.g. TSLA)

- **Cluster 2** → 🔵 *Moderate volatility, average performance*  
  → Core tech or steady growers (e.g. AAPL, AMZN)

Use these ranges to label new clusters or stocks as they are added in future analyses.



---

## 🧱 Optional Scaling (Future Work)

- Add more tickers or S&P 500
- Use Databricks for pipeline orchestration + MLflow
- Expand to earnings transcripts or Reddit sentiment
- Deploy to Streamlit or Databricks dashboards

---

## 📌 Status

- [x] Feature engineering complete
- [x] KMeans & DBSCAN clustering done
- [x] Visuals + PCA insights finalized
- [x] News sentiment integrated with FinBERT
- [ ] Dashboard/app in progress (optional next phase)

---

## 📬 Contact

Built by [Rehan Chaudhry](https://github.com/rehansc) —  
exploring the intersection of **ML + financial markets**.

Open to feedback, forks, and collaboration!


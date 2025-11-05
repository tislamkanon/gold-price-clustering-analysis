# Gold Price Clustering Analysis (XAU/USD) with K-Means

![K-Means Clusters](images/cluster_close_volatility.png) <!-- Header: Close Price vs Volatility scatter plot showing clusters -->

## 🎯 Project Overview
This repository contains the code and analysis for our Telkom University Machine Learning Final Project (Group 04, Unsupervised Learning). As Team Leader, I coordinated the end-to-end pipeline: Applying K-Means clustering to hourly gold price data (XAU/USD, May 2025) to uncover hidden patterns in volatility, returns, and trading signals.

**Key Highlights**:
- **Dataset**: 298 hourly records (Open, High, Low, Close, TickVolume, etc.) from forex markets.
- **Pipeline**: Data cleaning → Exploratory Data Analysis (EDA) → Feature engineering (Returns, Volatility, RSI) → K-Means (4 clusters, silhouette score ~0.45).
- **Insights**: Identified volatility peaks (e.g., May 6-7 events with 0.45% swings); clusters reveal "oversold drops" (low RSI ~47) vs. "steady uptrends" (RSI ~65).
- **Anomalies**: Detected 15 large price changes, tied to market sessions (weekday patterns).

![Cluster Distribution](images/cluster_distribution_pie.png) <!-- Overview: Pie chart of cluster breakdown -->
![Correlation Heatmap](images\cluster_0_correlation_heatmap.png) <!-- Insights: Heatmap for Cluster 0 correlations -->
![Price Large Changes](images/close_price_timeseries.png) <!-- Insights: Line chart highlighting anomalies -->

**Business Impact**: Useful for financial forecasting, risk hedging, or export analytics (e.g., spotting trends in commodity tenders like PT Pindad).

**Tech Stack**: Python 3, Pandas, NumPy, Matplotlib/Seaborn, Scikit-Learn, Jupyter.

## 👥 Team
- **MD Touhidul Islam Kanon** – Team Leader: Clustering & Feature Engineering (focused on K-Means implementation, pipeline coordination, and insights synthesis).
- Salma Kamilah Rahma – Data Cleaning Lead
- Karina Ditya Amanda – EDA Contributor
- Resti Fresard – Visualization
- Akmal Muhammad Firdaus – Report & Insights

## 📋 Quick Start
1. **Clone the Repo**:
2. **Set Up Environment**:
3. **Run the Notebooks** (in order, as guided by team lead structure):
- `jupyter notebook notebooks/Data_Cleaning.ipynb` – Load & prep raw data.
- `notebooks/Exploratory_Data_Analysis(EDA).ipynb` – Viz trends, RSI/SMA, anomalies.
- `notebooks/K-Means_Clustering.ipynb` – Scale features, apply K-Means, generate profiles.
4. **Explore Outputs**:
- Labeled data: `data/XAUUSD_Hourly_Clustered.csv`
- Full report: `docs/ML_Final_Project_Report.pdf`

## 📊 Cluster Profiles (Summary Table)
| Cluster | Mean Volatility | Mean RSI | High-Low Range (Max) | Key Trait                  |
|---------|-----------------|----------|----------------------|----------------------------|
| 0      | 0.38%          | 65      | 18.78               | Steady uptrends (low vol) |
| 1      | 0.45%          | 68      | 35.12               | High-volume events        |
| 2      | 0.34%          | 52      | 10.66               | Consolidation periods     |
| 3      | 0.39%          | 47      | 15.27               | Oversold drops (risky)    |

## 🚀 Future Enhancements
- Supervised ML: LSTM for price prediction.
- Real-time: Integrate Alpha Vantage API for live data.
- Viz: Interactive Tableau dashboard (link in progress).

## 📄 License & Contact
MIT License – Free to use/fork (see [LICENSE](LICENSE)).

Questions? Open an issue or connect on [LinkedIn](https://linkedin.com/in/tislamkanon). #MachineLearning #KMeans #DataAnalytics #Finance

---

*Led with ❤️ by Group 04 (Kanon, Salma, Resti, Karin, Akmal), Telkom University (2025)*




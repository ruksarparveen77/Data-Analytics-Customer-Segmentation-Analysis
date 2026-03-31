# 🛍️ Customer Segmentation — RFM + KMeans Clustering

![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?logo=pandas)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?logo=scikit-learn)
![Power BI](https://img.shields.io/badge/PowerBI-Dashboard-F2C811?logo=powerbi)

---

## 📌 Project Overview

This project segments customers of a UK-based online retailer into
distinct groups using **RFM Analysis** and **KMeans Clustering** (Machine Learning).
The goal is to help the business understand its customers better and
design targeted marketing strategies for each group.

---

## 🎯 Business Problem

A UK online retailer has 4,000+ customers but treats them all the same.
This leads to wasted marketing budget and poor customer retention.

**Solution:** Identify distinct customer segments so the business can:
- Reward high-value customers
- Re-engage customers at risk of leaving
- Win back lost customers with targeted offers

---

## 🔍 What is RFM Analysis?

| Metric | Meaning | Question |
|---|---|---|
| **R — Recency** | Days since last purchase | Are they an active customer? |
| **F — Frequency** | Number of orders placed | Are they a loyal customer? |
| **M — Monetary** | Total amount spent | Are they a high-value customer? |

Each customer is scored 1–5 on each metric and grouped into segments.

---

## 🤖 Machine Learning — KMeans Clustering

After scoring customers with RFM, KMeans clustering was applied to
group customers mathematically. The optimal number of clusters (K=3)
was determined using:
- **Elbow Method** — finds where inertia stops decreasing sharply
- **Silhouette Score** — measures how well clusters are separated (score: 0.90 at K=2)

---

## 👥 Customer Segments Discovered

| Segment | Description | Strategy |
|---|---|---|
| 👑 Champions | Buy recently, often, and spend the most | Reward with loyalty program |
| 💚 Loyal Customers | Regular buyers with good spend | Upsell premium products |
| ⚠️ At Risk | Used to buy often but haven't recently | Send win-back email campaign |
| 💀 Lost / Inactive | Haven't purchased in a long time | Offer heavy discount to re-engage |
| 🌟 Potential Loyalists | Recent buyers, growing frequency | Nurture with onboarding offers |
| 🆕 New Customers | Just started buying | Welcome offer + onboarding |

---

## 📊 Key Findings

- **Total Customers Analysed:** 4,338
- **Champions** generate the highest revenue despite being a small group
- **Lost / Inactive** customers make up the largest segment — a major opportunity
- Customers who buy frequently also tend to spend more (strong F-M correlation)
- KMeans silhouette score of **0.90 at K=2** indicates very well-separated clusters

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Python 3.12 | Core programming language |
| Pandas | Data cleaning and RFM calculation |
| Scikit-learn | KMeans clustering, StandardScaler |
| Matplotlib / Seaborn | Data visualisation |
| Power BI | Interactive dashboard |

---

## 📁 Project Structure

```
customer-segmentation/
├── data/
│   ├── Online Retail.xlsx          ← raw dataset (UCI)
│   └── customer_segments.csv       ← generated after running notebook
├── outputs/
│   ├── segment_distribution.png
│   ├── revenue_by_segment.png
│   ├── elbow_curve.png
│   ├── cluster_scatter.png
│   └── rfm_heatmap.png
├── dashboard/
│   └── customer_segmentation.pbix
├── analysis.ipynb                  ← main notebook
└── README.md
```

---

## ▶️ How to Run

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/customer-segmentation.git

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl

# 3. Place dataset in data/ folder
# Download from: https://archive.ics.uci.edu/ml/datasets/online+retail

# 4. Open and run the notebook
jupyter notebook analysis.ipynb
```

---

## 📈 Charts Generated

| Chart | Insight |
|---|---|
| Segment Distribution | How many customers in each segment |
| Revenue by Segment | Which segments drive the most revenue |
| Elbow Curve | How we chose the optimal K for clustering |
| Cluster Scatter Plot | Visual separation of customer clusters |
| RFM Heatmap | Average RFM scores per segment |

---

## 💡 Business Recommendations

1. **Focus retention budget on Champions** — they drive disproportionate revenue
2. **Launch a win-back campaign for At Risk customers** — email with personalised offers
3. **Offer loyalty rewards to Loyal Customers** — convert them to Champions
4. **Re-engage Lost customers with heavy discounts** — last attempt before writing off
5. **Onboard New Customers carefully** — first 90 days determine long-term loyalty

---

## 📂 Dataset

- **Source:** UCI Machine Learning Repository
- **Link:** https://archive.ics.uci.edu/ml/datasets/online+retail
- **Size:** 541,909 transactions
- **Period:** December 2010 – December 2011
- **Region:** UK-based online retailer

---

## 👤 Author

**Your Name**  
Data Analytics Portfolio Project  
[LinkedIn](https://linkedin.com/in/yourprofile) | [GitHub](https://github.com/yourusername)

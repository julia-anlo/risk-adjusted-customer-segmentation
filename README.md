# 🏦 Risk-Adjusted Customer Segmentation
### Bridging Banking Finance, Statistics & Machine Learning

**Author:** Julia Anglada Lomaeva | Creative Data Scientist  
**Stack:** Python · Scikit-learn · PCA · K-Means · Basel III Risk Metrics

---

## Why This Project?

Traditional customer segmentation in banking relies on demographics —
age, location, income. It answers *who* the client is.

This project answers a more valuable question: **what is this client worth to the bank?**

Two clients with identical income can have radically different financial impacts
depending on their credit risk, capital consumption, and operational costs.
Standard segmentation misses this entirely.

We use **RAROC** (Risk-Adjusted Return on Capital) as the north-star metric
to reveal three hidden client personas — and the strategic action each one demands.

---

## Methodology

| Step | Description |
|------|-------------|
| 1 | Synthetic portfolio generation (500 clients, Basel III assumptions) |
| 2 | Feature engineering: EL, Net Profit, ROI, RAROC |
| 3 | EDA & correlation analysis |
| 4 | StandardScaler + PCA (4D → 2D, 78.2% variance retained) |
| 5 | Optimal K selection — 5-metric validation framework |
| 6 | K-Means clustering (K=3) |
| 7 | Cluster profiling & strategic persona assignment |

---

## Key Results

| Persona | RAROC | PD | Portfolio Share | Action |
|---|---|---|---|---|
| 🟢 Value Anchors | +0.78 | 6.1% | 30% | Retain & Reward |
| 🔵 Steady Contributors | +0.17 | 5.1% | 55% | Re-price & Optimize |
| 🔴 Portfolio Hazards | -0.95 | 21.9% | 16% | De-risk immediately |

**K=3 validated by convergence across 5 metrics:** WCSS Gradient, Silhouette,
Davies-Bouldin, and Calinski-Harabasz. Not a gut feeling — statistical evidence.

---

## Key Insights

**The Concentration of Value:** Only 30% of clients drive portfolio profitability.
Volume is a vanity metric. RAROC is the truth.

**The Silent Drag:** 55% of clients are technically profitable but hold €96k average
exposure — consuming disproportionate regulatory capital relative to their return.
Re-pricing by 0.5% margin would significantly improve portfolio-level RAROC.

**The Concentrated Risk:** 16% of clients with PD=21.9% generate ~€621k in
expected losses at portfolio level. Invisible in demographic segmentation. Visible here.

---

## Limitations & Next Steps

This project uses synthetic data with deliberate simplifications.
With real portfolio data, PD distributions would be more skewed,
LGD would vary by product, and outlier treatment would be required before clustering.

Next steps: test on real anonymized data, incorporate customer tenure,
and build a cluster migration monitoring layer as an early warning system.

---

## How to Run

Open directly in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/gist/julia-anlo/17919320dfbe0f512a5640df140a429b/risk-adjusted-customer-segmentation-using-machine-learning.ipynb)

---

## Connect

[LinkedIn](https://www.linkedin.com/in/juliaanlo/) · [GitHub Portfolio](https://github.com/julia-anlo)
```


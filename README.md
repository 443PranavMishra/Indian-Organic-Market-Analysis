# Organic Consumer Segmentation

Decoding Indian consumer behaviour for premium organic food products through exploratory analysis, feature engineering, and customer segmentation.

## Overview

Premium retailers often assume organic food demand is uniform across their customer base — this project challenges that assumption. Using survey-style data from 500 customers, this analysis uncovers **why organic food underperforms relative to industry benchmarks**, and builds a **segmentation-driven framework** to guide shelf placement, marketing, pricing, and inventory decisions.

The core finding: **purchase intent is high across almost every customer (82–88%) — the real problem isn't demand, it's conversion, access, and communication.**

## Key Results

- **4 data-driven customer segments** identified via K-Means clustering, each mapped to a specific business action (shelf placement, marketing message, pricing strategy, inventory decision)
- **Engineered features** (e.g., Spend-to-Income Ratio, Eco-Consciousness Score, Convenience Gap) outperformed raw demographic variables as predictors of spend and intent
- **Largest opportunity segment** identified: high-intent, low-spend customers representing the single biggest untapped revenue pool
- Bonus stacking ensemble model (Random Forest, XGBoost, CatBoost, LightGBM + Ridge meta-model) built to independently validate feature selection choices

## Repository Structure

```
├── notebook/
│   └── organic_consumer_analysis.ipynb    # Full analysis notebook
├── data/
│   └── indian_organic_food_dataset.csv    # Raw dataset (500 records, 26 attributes)
├── report/
│   └── methodology_report.pdf             # Condensed report
├── requirements.txt
└── README.md
```

## Methodology

| Phase | Description |
|---|---|
| **Phase 0** | Data Cleaning & Preparation — missing value/duplicate checks, IQR-based outlier treatment |
| **Phase 1** | Exploratory Data Analysis — distributions, correlations, and categorical breakdowns of spend and intent |
| **Phase 2** | Feature Engineering & Selection — derived business-relevant features, ranked by correlation, mutual information, and feature importance |
| **Phase 3** | Business Problem-Solving Framework — K-Means customer segmentation mapped to a shelf/marketing/pricing/inventory action plan |
| **Phase 4** | Insights & Recommendations — data-backed findings and priority-ordered recommendations |
| **Phase 5 (Bonus)** | Predictive Modeling — stacking ensemble classifier validating Phase 2's feature selection |

## Dataset

500 customer records across 26 attributes spanning demographics, economic indicators, lifestyle/awareness measures, and location/access factors, with two target variables:
- `Purchase_Intent` — whether the customer intends to buy organic food
- `Weekly_Organic_Spend` — ₹ spent weekly on organic products

## Tech Stack

- **Data handling:** pandas, numpy
- **Visualization:** matplotlib, seaborn
- **Machine Learning:** scikit-learn, XGBoost, CatBoost, LightGBM

## Getting Started

```bash
git clone https://github.com/<your-username>/organic-consumer-segmentation.git
cd organic-consumer-segmentation
pip install -r requirements.txt
jupyter notebook notebook/organic_consumer_analysis.ipynb
```

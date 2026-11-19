# E-Commerce Customer Segmentation & Recommendation Analysis

## Overview
This project analyses customer purchasing behaviour on the **Online Retail** dataset using **Recency, Frequency, and Monetary (RFM)** features, **K-Means** clustering for customer segmentation, and **cosine similarity** for a basic product recommendation function.

## Tools Used
- Python, Pandas, NumPy
- Scikit-learn (StandardScaler, KMeans, silhouette_score, cosine_similarity)
- Matplotlib, Seaborn
- Jupyter Notebook

## Key Results Summary
- **Cleaned Dataset:** `397,884` valid rows across `4,338` customers and `3,866` products (from `541,909` raw rows).
- **Customer Segments (`K = 4`):**
  - **Champions (13 customers):** Avg Recency `7.38` days, Avg Frequency `82.54`, Avg Monetary `127,338.31`
  - **Regular Customers (204 customers):** Avg Recency `15.50` days, Avg Frequency `22.33`, Avg Monetary `12,709.09`
  - **Occasional Buyers (3,054 customers):** Avg Recency `43.70` days, Avg Frequency `3.68`, Avg Monetary `1,359.05`
  - **At-Risk Customers (1,067 customers):** Avg Recency `248.08` days, Avg Frequency `1.55`, Avg Monetary `480.62`
- **Product Recommendations:** `recommend_products()` uses cosine similarity on customer-product purchase quantities (top 150 products by volume), e.g., suggesting `RED HANGING HEART T-LIGHT HOLDER` (`0.659`) and `HEART OF WICKER LARGE` (`0.629`) for `WHITE HANGING HEART T-LIGHT HOLDER`.

## Screenshots & Visuals

### 1. Elbow Method & Silhouette Analysis
![Screenshot: Elbow Method & Silhouette Score vs. K](Screenshot%202026-11-19%20190132.png)

### 2. 2D Customer Cluster Visualisation
![Screenshot: Customer Segments - Frequency vs. Monetary & Recency vs. Monetary](Screenshot%202026-11-19%20190204.png)

### 3. Customer Segment Profiles
![Screenshot: Segment Profiles Table](Screenshot%202026-11-19%20190220.png)

### 4. Sample Product Recommendations Output
![Screenshot: Product Recommendations Output](Screenshot%202026-11-19%20190233.png)

## Business Recommendations by Segment
- **Champions:** Offer VIP perks, early access to new items, and loyalty rewards to retain high-value repeat buyers.
- **Regular Customers:** Cross-sell related products using cosine similarity and introduce multi-item bundles to raise order value.
- **Occasional Buyers:** Run targeted promotions, seasonal offers, and personalized product suggestions to increase purchase frequency.
- **At-Risk Customers:** Launch win-back campaigns with time-limited discounts and relevant reminders before churn.

## How to Run
1. Place `Online Retail.csv` and the Jupyter Notebook in the same project folder.
2. Run all cells in order from data cleaning and RFM feature engineering through K-Means segmentation and product recommendations.

# Superstore Sales — Exploratory Data Analysis (Task 01)

**Internship:** Data Science Internship — Devixo Solutions  
**Task:** Task 01 — Exploratory Data Analysis (EDA) on Superstore Sales Dataset  
**Author:** Makia Mai[cite: 12]

## Project Overview
This repository contains the complete Exploratory Data Analysis (EDA) for **Task 01** of the Data Science Internship at Devixo Solutions using the Superstore Sales dataset (`train.csv`). The workflow covers raw data inspection, cleaning, feature engineering, statistical & outlier analysis, correlation analysis, visualizations, business insights, and practical recommendations.

## Dataset Summary
- **Initial Dimensions:** 9,800 rows × 18 columns
- **Cleaned Dimensions:** 9,800 rows × 21 columns
- **Data Cleaning & Feature Engineering:**
  - Addressed 11 missing values in `Postal Code` and standardized 5-digit postal codes
  - Converted `Order Date` and `Ship Date` into `datetime64` format
  - Engineered `Shipping_Days`, `Order_Year`, and `Order_Month`
  - Verified 0 duplicate rows and 0 negative/invalid sales records

## Key Insights
- **Order Value Skewness:** Order `Sales` is strongly right-skewed with a mean of **$230.77** and a median of **$54.49** (ranging from **$0.44** to **$22,638.48**), including **1,145 IQR outliers (11.68%)**.
- **Category Performance:**
  - **Technology:** 1,813 orders, **$827,455.87** total sales, and highest average order value (**$456.40**)
  - **Furniture:** 2,078 orders, **$728,658.58** total sales, and **$350.65** average order value
  - **Office Supplies:** 5,909 orders (highest order count), **$705,422.33** total sales, and lower average order value (**$119.38**)
- **Shipping & Seasonality:** `Shipping_Days` spans **0 to 7 days** (mean **3.96**, median **4.00**), while sales activity rises toward Q4 / later months (`Order_Month` mean **7.82**, median **9.00**).
- **Correlation Findings:** Numerical columns (`Sales`, `Shipping_Days`, `Order_Year`, `Order_Month`) show near-zero linear correlation, highlighting that categorical attributes (`Category`, `Segment`) and seasonal trends carry stronger practical signals.

## Business Recommendations
1. **Bundle & Cross-Sell in Office Supplies:** Introduce bundles or cross-sell offers on high-volume Office Supplies orders (**5,909 orders**, avg **$119.38**) to increase basket size.
2. **Prioritize Inventory & Campaigns for Technology and Furniture:** Support high-average-value categories (**Technology** at **$456.40** avg and **Furniture** at **$350.65** avg) with steady stock and targeted promotions.
3. **Prepare Capacity Ahead of Q4 Peaks:** Align stock and fulfillment operations before peak late-year demand so shipping (**0–7 days**, median **4 days**) remains reliable.
4. **Monitor High-Value Outliers & Key Segments:** Track large orders (**1,145 IQR outliers**, **11.68%**) and core segments/categories separately to manage revenue risk.
5. **Keep Shipping Predictable & Evaluate Beyond Linear Correlations:** Maintain consistent shipping expectations and rely on category, segment, and seasonal groupings for business decisions.

## Deliverables
- **Colab Notebook:** `datascience_devixointership.ipynb`
- **Final PDF Report:** `DEVIXO SOLUTIONSintershipdata.pdf`

Check Notebook HTML here: [fresh_product_sales:](https://rahulshinde02.github.io/Data-Analysis-and-visualization-with-Pandas/fresh_product_sales/Fresh_products_sales_analysis.html)


# Fresh Products Sales Analysis

This project performs an extensive analysis of fresh produce sales to understand transaction patterns, profitability, and operational efficiency. By processing over 878,000 transaction records, this notebook provides a framework for inventory rationalization and pricing strategy optimization in a high-perishability retail environment.

## 📊 Project Scope

The analysis is designed to provide actionable intelligence on the following operational areas:

* **Transaction Dynamics:** Examination of temporal sales patterns, including weekly and intraday peaks.
* **Profitability Modeling:** Classification of inventory using a 2x2 quadrant matrix (Star, Cash Cow, Niche, Underperformer) to identify SKU-level performance.
* **Pricing & Risk:** Evaluation of wholesale price volatility versus retail price responsiveness, incorporating loss rate adjustments.
* **Markdown Efficacy:** Assessment of current clearance strategies to identify impacts on margin and sales velocity.

## 🛠 Tech Stack

* **Language:** Python 3.x
* **Core Libraries:** `pandas`, `numpy`
* **Visualization:** `matplotlib`, `seaborn`

## ⚙️ Methodology & Pipeline

The notebook follows a structured data science workflow:

1. **Data Cleaning & Integration:** Merging raw transaction data, handling date-time conversions, and ensuring data integrity (duplicate and missing value checks).
2. **Financial Feature Engineering:** Calculating "True Unit Cost" by factoring in product-specific loss rates to derive accurate net profit and margin metrics.
3. **Exploratory Data Analysis (EDA):** Identifying seasonal trends and customer behavior using volume and revenue distributions.
4. **Portfolio Segmentation:** Implementing a median-based split to categorize items into quadrants based on sales volume and profit margins.
5. **Markdown Testing:** Identifying overlapping pricing windows to evaluate the operational behavior of the store's clearance mechanism.

## 📂 Data Structure
the data was soutced from [kaggle](https://www.kaggle.com/datasets/yapwh1208/supermarket-sales-data?select=annex1.csv) and preprocessed into single table parquet file. The  dataset comprising 11 key features, including:

* **Temporal Data:** Datetime and hourly breakdown.
* **Operational Data:** Item Code, Category, Quantity Sold, and Loss Rate.
* **Financial Data:** Unit Selling Price, Wholesale Price, and calculated Cost/Profit metrics.


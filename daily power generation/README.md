## Notebook
You can view the interactive data visualizations here: 
[Live Energy Analysis Notebook](https://RahulShinde02.github.io/Data-Analysis-and-visualization-with-Pandas/daily%20power%20generation/Energy_analysis.html)

# Daily Power Generation Analysis: India

This notebook provides a comprehensive technical analysis of daily power generation data across India, transforming raw operational logs into insights regarding grid performance, asset efficiency, and regional supply stability.

## Data Source

The data is sourced from the [India Data Portal](https://indiadataportal.com/p/power/r/mop-power_generation-pl-dl-abc).

* **Scope:** Historical time-series data (2017–2025) containing over 2.5 million records.
* **Granularity:** Includes daily operational metrics—such as `monitored_capacity`, `todays_gen_prgm` (targets), and `todays_gen_act` (actuals)—broken down by region, state, sector, station, and individual unit.
* **Format:** Ingested as a `daily-power-generation.parquet` file, utilizing columnar storage for efficient processing of large-scale datasets.

---

## Technical Methodology

The project follows a structured data pipeline to clean, engineer, and visualize grid-level performance.

### 1. Data Ingestion & Sanitization

* **Environment Setup:** Utilizes `pandas` for data manipulation, and `plotly` for interactive visualizations.
* **Type Optimization:** Converts date strings to `datetime` objects and high-cardinality columns (region, state, sector, station type) to `category` dtypes to minimize memory usage.
* **Cleaning:** Filters out non-operational or summary-level entries (e.g., rows containing "Type", "Total", or "Sum") to focus strictly on granular plant-level performance.

### 2. Metric Engineering

The notebook calculates several derived metrics to quantify grid health:

* **Variance:** The absolute delta between actual generation and programmed targets (`todays_gen_act - todays_gen_prgm`).
* **Fulfillment Rate:** The ratio of actual output to target output, used to measure operational reliability.
* **Plant Load Factor (PLF):** Normalizes actual generation against monitored capacity to determine percentage utilization.
* **Ramping Volatility:** Computes the standard deviation of daily output changes to identify baseload assets under mechanical stress.

### 3. Analytical Frameworks

* **Distribution Analysis:** Quantifies the national energy mix contribution (Thermal, Hydro, Nuclear, etc.) using interactive pie charts.
* **Trend & Time-Series Mapping:** Visualizes long-term generation shifts and seasonal fluctuations from 2017–2025.
* **Grid Risk Profiling:** Identifies chronic failure points by isolating stations with high-frequency zero-generation incidents.
* **Pareto Deficit Allocation:** Models cumulative grid shortfalls to demonstrate that a small cluster of high-capacity assets contributes to the majority of total supply deficits.
* **Correlation Modeling:** Employs Pearson matrices to evaluate regional interdependencies and grid-balancing potential.

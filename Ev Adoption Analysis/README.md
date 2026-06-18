## 📊 View Interactive Report

You can view the live, fully rendered interactive vehicle registration chart directly as a webpage here:
👉 **[Launch Vehicle Registration by Fuel Analysis](https://rahulshinde02.github.io/Data-Analysis-and-visualization-with-Pandas/Ev%20Adoption%20Analysis/vehicle%20registration%20by%20fuel.html)**

## Maharashtra EV Adoption & Vehicle Registration Analysis

This notebook provides an analytical framework for processing and visualizing multi-year vehicle registration data in Maharashtra. By standardizing raw fuel-type logs into consolidated powertrain categories, it enables a granular assessment of structural market shifts, RTO-level performance, and EV penetration trends.

### Key Analytical Capabilities

* **Data Standardization:** Implements a classification engine to map diverse raw fuel strings (e.g., 'Pure Ev', 'Petrol/Hybrid') into standardized categories: **Fossil, Hybrid, Electric, Bio,** and **Not Applicable**.
* **Market Share Indexing:** Calculates monthly regional baseline market shares to identify evolving consumer preferences across powertrain technologies.
* **RTO Hub Benchmarking:** Ranks Regional Transport Office (RTO) hubs based on a custom **EV Penetration Index**, highlighting high-growth areas.
* **Velocity Analysis:** Computes Compound Annual Growth Rates (CAGR) for EV adoption at the RTO level (2021–2024), pinpointing fast-emerging electric mobility clusters.
* **Cyclical Modeling:** Visualizes rolling 3-month fuel share transformations and seasonal registration performance to capture market volatility and growth patterns.

### Data Context

The primary dataset utilized is from  [Indian Data Portal](https://indiadataportal.com/p/vehicle-registrations/r/morth-vahan_reg_by_fuel-ol-mn-aaa), specifically filtered for the Maharashtra region.

### Technical Stack

* **Language:** Python
* **Core Libraries:** `pandas` (Data manipulation), `plotly` (Interactive visualization)
* **Methods:** Vectorized imputation, pivot table aggregation, and rolling window statistical analysis.

# Data Cleaning — E-commerce Orders
**Oasis Infobyte | Data Analytics | Level 1 — Task 3**

## Overview
This project demonstrates a reproducible data-cleaning workflow on a deliberately messy **synthetic** e-commerce orders dataset.

## Tools
Python, pandas, NumPy, Jupyter Notebook.

## Folder structure
- `Data_Cleaning_Ecommerce_Orders.ipynb` — full walkthrough and runnable code.
- `data/messy_ecommerce_orders.csv` — raw intentionally messy input.
- `outputs/cleaned_ecommerce_orders.csv` — cleaned output.
- `outputs/initial_data_quality_report.csv` — initial data-quality report.
- `outputs/before_after_quality_summary.csv` — before/after summary.

## How to run
1. Open the notebook in Google Colab or Jupyter.
2. Keep the `data` and `outputs` folders beside the notebook.
3. Run all cells from top to bottom.
4. The cleaned CSV is saved in `outputs/`.

## Cleaning decisions
- Remove exact duplicate rows.
- Strip spaces and standardise IDs, names, city, gender and status.
- Convert date, quantity and unit price to appropriate data types.
- Impute invalid/missing numeric values using median.
- Replace non-critical missing categories with `Unknown`.
- Remove rows with invalid dates.
- Treat unit prices above ₹5,000 as implausible data-entry anomalies for this demonstration.

## Dataset note
The included dataset is synthetic and is used only to demonstrate data-cleaning methods. It is not real customer data. Imputation and anomaly thresholds are documented project assumptions and should be validated before use in a real business.

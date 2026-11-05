# OIBSIP – Level 1 Task 2: Customer Segmentation Analysis

## Dataset
Genuine UCI Online Retail transactions, using the cleaned transaction file from the Task 1 project.
Original dataset source: https://archive.ics.uci.edu/dataset/352/online+retail (CC BY 4.0; cite UCI).

## What this project does
- Cleans and validates transaction/customer fields.
- Builds RFM features: Recency, Frequency, Monetary.
- Calculates average order value and observed customer activity span.
- Log-transforms skewed RFM features and standardises with StandardScaler.
- Uses the Elbow Method (K=2–8) and K-Means (K=4).
- Produces cluster profiles, two scatter plots, customer-count bar chart, and marketing recommendations.

## Important interpretation
- CustomerID-missing rows are excluded because they cannot be assigned to an individual customer.
- Monetary value is observed-period revenue, not profit.
- “Customer lifetime value” is not predictive here; observed-period spend is used as a clearly labelled proxy.
- The data is historical (2010–2011), so segment descriptions are period-specific.

## Files
- `Customer_Segmentation_Analysis.ipynb` – reproducible notebook.
- `data/PUT_Online_Retail_XLSX_HERE.txt` – instructions; use the original `Online Retail.xlsx` from your Task 1 project.
- `charts/` – generated charts.
- `outputs/` – RFM data, cluster profiles, elbow values and recommendations.

## Run
In Google Colab, open the notebook and upload the original `Online Retail.xlsx` when prompted (the same source file from Task 1). Or place it beside the notebook locally:
`pip install pandas numpy scikit-learn matplotlib jupyter`
Then open the notebook and run all cells.

## Attribution
Chen, D. (2015). Online Retail [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33

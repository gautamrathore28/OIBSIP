# OIBSIP – Real Retail Sales EDA

## Project status
This version uses the genuine **UCI Online Retail** dataset. The included Excel source file is the original dataset; the cleaned CSV and charts are reproducible analysis outputs. No synthetic rows are used.

## Dataset source
- UCI Machine Learning Repository: Online Retail
- Official page: https://archive.ics.uci.edu/dataset/352/online+retail
- Source file: `data/Online Retail.xlsx`
- 541,909 original transaction rows; 8 original columns.
- Coverage: 01 Dec 2010 to 09 Dec 2011
- Licence: CC BY 4.0 (attribute UCI and cite the dataset page when reusing).

## Files
- `Retail_Sales_EDA_Real_Data.ipynb` – complete notebook workflow.
- `data/Online Retail.xlsx` – original UCI source data.
- `data/online_retail_cleaned.csv` – cleaned transaction-line data with calculated Revenue.
- `charts/` – generated charts.
- `outputs/` – monthly, quarterly, product, country and customer summary tables.

## Cleaning methodology
1. Exclude cancelled invoices (InvoiceNo begins with `C`).
2. Exclude non-positive Quantity and UnitPrice.
3. Exclude missing product Description.
4. Keep missing CustomerID rows in overall sales totals; exclude them only from customer-level ranking.
5. Revenue = Quantity × UnitPrice.

Raw rows: 541,909  
Cancelled invoices: 9,288  
Rows retained for sales analysis: 530,104  
Distinct invoices after cleaning: 19,960  
Known unique customers: 4,338  
Countries: 38  
Calculated line-item revenue: £10,666,684.54

## Actual findings from this dataset
- United Kingdom generated £9,025,222.08, around 84.6% of retained revenue.
- Strongest month: 2011-11 (£1,509,496.33).
- Strongest quarter: 2011Q4 (£3,303,268.31).
- Top product by units: PAPER CRAFT , LITTLE BIRDIE (80,995 units).
- 24.9% of retained rows have no CustomerID.

## Recommendations
- Prioritise inventory and service reliability in the UK, the dominant market.
- Prepare stock and fulfilment capacity ahead of the observed late-year revenue peak.
- Monitor top-selling items for stockouts and test bundles with complementary products.
- Improve customer-ID capture so more orders can be included in retention analysis.
- Analyse cancellations/returns separately; this project does not calculate profit.

## Important limitations
The source has no age, gender, or product-category columns. Those analyses are intentionally omitted rather than fabricated. It also has no product cost or profit data. Treat calculated sales as revenue, not profit. The source is historical and ends on 9 December 2011.

## How to run
1. Extract the project ZIP.
2. Install: `pip install pandas openpyxl matplotlib jupyter`
3. Open the project folder and launch: `jupyter notebook`
4. Run `Retail_Sales_EDA_Real_Data.ipynb` from top to bottom.

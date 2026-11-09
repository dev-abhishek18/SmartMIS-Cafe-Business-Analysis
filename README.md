# SmartMIS – Café Business Performance Analysis

An Excel-based Management Information System (MIS) portfolio project for analysing café sales, product mix, store performance, operating costs and profitability across three sample locations in India.

> **Purpose:** Convert transaction-level data into clear management reporting through an Excel dashboard, formula-driven analysis sheets and reconciliation checks.

## Project overview

| Item | Details |
|---|---|
| Project | SmartMIS – Café Business Performance Analysis |
| Platform | Microsoft Excel |
| Business domain | Café / food & beverage |
| Reporting period | 1 January–30 June 2026 |
| Currency | Indian Rupees (INR) |
| Sample business | Desi Brew |
| Locations | Connaught Place (Delhi), Sector 18 (Noida), Cyber Hub (Gurugram) |
| Demo transactions | 8,416 transaction rows |
| Preserved source data | 149,116 original source records |
| Data classification | Synthetic Indian demo transactions + preserved original source data + illustrative operating-cost assumptions |

**Portfolio-data disclaimer:** The Indian café transactions, demo customer names, sample stores, product costs and operating expenses are synthetic or illustrative. They are not records of a real café. The dashboard's estimated net profit is a demonstration calculation, not audited or actual business profit.

## Business questions

The workbook is designed to help answer questions such as:

- How much did the sample café generate in sales?
- Which of the three locations generated the highest sales?
- Which products and categories contribute most to sales?
- How do sales, COGS, gross profit and gross margin change month by month?
- How do weekday and weekend results compare when adjusted for the number of calendar days?
- What is the estimated result after subtracting the illustrative operating-cost budget?
- Do the analysis reports reconcile to the transaction-level data?

## Workbook and sheet guide

The supplied workbook is named **`SmartMIS_India_Realistic_Positive_Profit.xlsx`**. Its sheets, in workbook order, are:

| # | Sheet | What it contains |
|---:|---|---|
| 1 | `Dashboard` | Management summary with sales, orders, gross profit, gross margin, average order value, units sold, estimated net profit and top city; includes branch, day-type, top-product and monthly visual summaries. |
| 2 | `Read_Me` | Workbook usage notes, metric definitions, data limitations and formula guidance. |
| 3 | `Store_Analysis` | Sales, COGS, gross profit, orders, units, average order value and gross margin for each sample store. |
| 4 | `Product_Analysis` | Product-level sales, units, COGS, gross profit, gross margin, sales ranking, performance groups and top/bottom product views. |
| 5 | `Monthly_Analysis` | January–June monthly orders, units, sales, COGS, gross profit and margin; also compares weekday/weekend totals and average sales per calendar day. |
| 6 | `Period_Analysis` | Q1, Q2 and H1 (January–June) performance using date-based calculations. |
| 7 | `Category_Analysis` | Category sales, units, gross profit and share of total sales. |
| 8 | `QA_Checks` | Reconciliation checks comparing transaction totals with store, category, monthly and period reports. |
| 9 | `Demo_Transactions` | 8,416 synthetic Indian café transaction rows with calculated sales, COGS, gross profit and weekday/weekend classification. |
| 10 | `Sample_Operating_Costs` | 18 illustrative monthly cost records: six months for each of the three stores, split into rent, staff, utilities and other expenses. |
| 11 | `Original_Source_Data` | 149,116 original source records preserved separately from the Indian demo data. |

The original source data is retained for traceability and is **not** the dataset used for the Indian demo dashboard. The analysis sheets use `Demo_Transactions`; estimated net profit also uses `Sample_Operating_Costs`.

## Key metrics and definitions

- **Total Sales:** Sum of transaction sales (`quantity × unit price`).
- **Orders:** Count of transaction rows in this demo; each row is treated as one order/receipt.
- **Units Sold:** Sum of transaction quantities.
- **Average Order Value (AOV):** Total sales divided by order count.
- **COGS:** Sum of `quantity × unit cost`.
- **Gross Profit:** Sales minus COGS.
- **Gross Margin %:** Gross profit divided by sales.
- **Estimated Net Profit:** Demo gross profit minus the illustrative operating expenses in `Sample_Operating_Costs`. This is an estimate based on assumptions, not audited net profit.
- **Weekday / Weekend:** Monday–Friday is weekday; Saturday–Sunday is weekend. Average sales per calendar day is used for a fair comparison because the period contains different numbers of weekdays and weekend days.

## Demonstration results

The figures below were recalculated from the supplied workbook and are illustrative only.

| Metric | Result |
|---|---:|
| Total sales | ₹12,66,055 |
| Orders | 8,416 |
| Units sold | 11,269 |
| Average order value | ₹150.43 |
| COGS | ₹4,93,761 |
| Gross profit | ₹7,72,294 |
| Gross margin | 61.00% |
| Illustrative operating expenses | ₹4,73,770 |
| Estimated net profit | ₹2,98,524 |
| Q1 sales | ₹5,53,480 |
| Q2 sales | ₹7,12,575 |
| H1 sales (January–June) | ₹12,66,055 |

### Selected observations

- **Noida** is the highest-sales sample location, with ₹4,31,800 in sales.
- **Cold Coffee** is the highest-sales product (₹1,77,280); **Samosa** is the lowest-sales product (₹14,980) in the product list.
- **Cold Beverages** is the largest category by sales (₹3,74,900).
- Q2 sales are approximately 28.8% higher than Q1 sales.
- Weekday sales total ₹8,66,290 across 129 days (about ₹6,715 per day); weekend sales total ₹3,99,765 across 52 days (about ₹7,688 per day). Compare average daily sales rather than raw totals.

These are descriptive findings from synthetic sample data. They do not establish causation or predict future business performance.

## Formula and Excel features

The workbook is formula-driven and does not require VBA macros. It uses functions including:

- `SUMIF`, `SUMIFS`, `COUNTIF`, `COUNTIFS`
- `IF`, `IFERROR`
- `RANK`, `COUNTIF` tie-breaker logic
- `INDEX` / `MATCH`
- `DATE`, `EDATE`, `EOMONTH`
- `NETWORKDAYS`

Excel Tables include `tblDemoTransactions`, `tblOperatingCosts` and `tblOriginalSourceData`. Calculated transaction columns derive sales, COGS, gross profit and day type from the row-level inputs.

## Data quality and reconciliation

The workbook includes eight reconciliation checks covering:

1. Sales total
2. COGS total
3. Gross profit total
4. Order count
5. Units sold
6. Category sales
7. Monthly sales
8. Quarter / H1 sales

All eight checks returned **PASS** when the supplied workbook was recalculated. These checks validate internal consistency between the demo transactions and reports; they do not prove that synthetic data or illustrative expenses represent a real business.

### Maintenance notes before adding more transactions

- Most analysis formulas are prefilled to transaction row 50,000.
- The current `QA_Checks` formulas reference transaction rows 5–8,420. If transactions are added beyond the current 8,416 records, extend the QA formula ranges as well; otherwise the reconciliation checks will not cover the new rows.
- Keep new rows inside `tblDemoTransactions` and ensure the calculated columns (sales, COGS, gross profit and day type) are populated.
- The reporting period currently ends on **30 June 2026**. Add July–December data and extend the period/monthly reports before presenting full-year FY2026 results.
- Review the Dashboard chart placement after opening the workbook in Excel; one chart is anchored below the current used cell range.

## Limitations and responsible interpretation

- Demo transactions and customer names are synthetic; the sample operating costs are illustrative assumptions.
- The report covers January–June 2026 only. Q1, Q2 and H1 are available; full-year FY2026 results are not.
- Estimated net profit depends on the illustrative lean takeaway-counter cost budget. Replace it with verified rent, payroll, utilities and other expense records before using it for decisions.
- Inventory analysis is not included because opening stock, purchases, wastage and closing stock records are not part of this workbook.
- Weekday/weekend classification does not exclude public holidays.
- Results describe only the workbook data and should not be presented as actual café performance.

## How to use the workbook

1. Open `Read_Me` for workbook instructions and definitions.
2. Review `Demo_Transactions` and `Sample_Operating_Costs` to understand the inputs and assumptions.
3. Start with `Dashboard` for the management summary.
4. Use `Store_Analysis`, `Product_Analysis`, `Category_Analysis`, `Monthly_Analysis` and `Period_Analysis` for detailed views.
5. Review `QA_Checks` before using the reported figures.
6. Read the limitations before including any result in a portfolio, presentation or interview.

## Repository contents

```text
SmartMIS-Cafe-Business-Analysis/
├── README.md
├── SmartMIS_India_Realistic_Positive_Profit.xlsx
└── Documentation/
    └── SmartMIS_Interview_Explanation_Guide_Hinglish.txt
```

The workbook filename above is the intended repository-root filename for this revision. The existing GitHub branch currently contains the README and Hinglish interview guide; the supplied Excel workbook still needs to be added as a binary file.

## Interview walkthrough

A concise presentation sequence:

1. Explain the café business problem and reporting objectives.
2. Clarify that the Indian demo data and operating costs are synthetic/illustrative.
3. Walk through the Dashboard KPIs.
4. Compare the three stores and explain the highest-sales location.
5. Explain product ranking and category mix.
6. Discuss monthly, quarterly and weekday/weekend trends.
7. Explain the estimated net profit calculation and its assumptions.
8. Finish with QA reconciliation and project limitations.

For a Hinglish sheet-by-sheet explanation and interview practice, see [SmartMIS Interview Explanation Guide](Documentation/SmartMIS_Interview_Explanation_Guide_Hinglish.txt).

---

Built as an Excel MIS portfolio and interview-practice project.

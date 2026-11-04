# SmartMIS – Café Business Performance Analysis

An Excel-based Management Information System (MIS) project that turns café transaction data into business-focused sales and performance insights.

> **Project purpose:** Help a café owner understand sales performance across stores, products, categories, months and weekdays/weekends using a structured Excel workbook and a management dashboard.

## Project at a glance

| Item | Details |
|---|---|
| Project | SmartMIS – Café Business Performance Analysis |
| Platform | Microsoft Excel |
| Business domain | Café / food & beverage retail |
| Analysis period | January–June 2026 |
| Currency | Indian Rupees (INR) |
| Sample stores | Connaught Place (Delhi), Sector 18 (Noida), Cyber Hub (Gurugram) |
| Data type | Demonstration / synthetic transactions and sample operating costs |

**Important:** This is a portfolio demonstration. The transactions, store names, product mix, customer names and operating-cost assumptions in the demo are synthetic. Results are not actual business performance and should not be represented as audited financial results.

## Business problem

A café owner may have transaction records but still struggle to answer practical questions:

- How much revenue did the business generate?
- Which store is performing best?
- Which products contribute most and least to revenue?
- How are sales and margins changing month by month?
- Do weekends generate more sales per day than weekdays?
- What should management investigate or act on next?

The workbook organizes transaction-level information into analysis views and a dashboard so that these questions can be answered more clearly.

## Workbook contents

The main workbook is stored in **[`Excel-Project/SmartMIS_India_Final_Weekday_Weekend.xlsx`](Excel-Project/SmartMIS_India_Final_Weekday_Weekend.xlsx)**.

| Sheet | Purpose |
|---|---|
| `Read_Me` | Starting point and workbook guidance. |
| `Demo_Transactions` | Demonstration transaction-level data used for the analysis. |
| `Sample_Operating_Costs` | Sample operating-cost assumptions; these are not verified actual expenses. |
| `Store_Analysis` | Compares performance across the three sample stores. |
| `Product_Analysis` | Reviews product revenue and highlights top/bottom products. |
| `Period_Analysis` | Compares selected periods such as Q1, Q2 and first-half YTD. |
| `Monthly_Analysis` | Tracks monthly sales, cost of goods sold (COGS), gross profit and margin, along with weekday/weekend comparison. |
| `Category_Analysis` | Compares revenue across product categories. |
| `Dashboard` | Management-facing summary of key metrics and selected comparisons. |
| `Original_Source_Data` | Preserves the original source data supplied for the analysis. |

## KPIs and definitions

- **Total Sales:** Sum of transaction sales amounts in the selected demo data.
- **Orders:** Count of transaction/order records as defined in the workbook.
- **Units Sold:** Total quantity sold.
- **Average Order Value (AOV):** Total sales divided by order count.
- **COGS:** Cost of goods sold using the sample product-cost assumptions.
- **Gross Profit:** Sales less COGS.
- **Gross Margin %:** Gross profit divided by sales, expressed as a percentage.

Gross profit and gross margin depend on synthetic cost assumptions; they are useful for demonstrating analysis, not for financial reporting.

## Demonstration findings

The following values are from the current demonstration workbook and should be read with the synthetic-data caveat:

| Metric | Demonstration result |
|---|---:|
| Total sales | ₹12,66,055 |
| Orders | 8,416 |
| Units sold | 11,269 |
| Average order value | About ₹150.43 |
| Gross profit | ₹7,72,294 |
| Gross margin | About 61% |
| Q1 sales | ₹5,53,480 |
| Q2 sales | ₹7,12,575 |

Other observations recorded during the analysis:
- Noida is the highest-sales store in this demo.
- Cold Coffee is the highest-revenue product; Samosa is the lowest-revenue product in the compared product list.
- Q2 sales are approximately 28.8% higher than Q1.
- Weekday total sales exceed weekend total sales because there are more weekdays in the period; **average daily sales** are higher on weekends (about ₹7,688) than weekdays (about ₹6,715). Compare per-day averages rather than raw totals when the number of days differs.

These are descriptive results from the sample, not causal findings or guarantees of future performance.

## How to use the project

1. Download the Excel workbook from the `Excel-Project` folder.
2. Open the `Read_Me` sheet first.
3. Review the transaction and sample-cost data to understand the source and assumptions.
4. Start with the `Dashboard` for the management summary.
5. Explore store, product, category, monthly and period analysis sheets for detail.
6. Check the limitations below before using any number in a presentation.

## Project limitations and responsible interpretation

- The transaction data and sample operating costs are synthetic demonstration data.
- The analysis covers **January–June 2026 only**; it is not a full-year 2026 report.
- Gross profit is calculated using sample cost assumptions. The workbook does not establish audited net profit.
- Inventory analysis is intentionally excluded because a complete set of opening stock, purchases, wastage and closing stock records was not available.
- Weekday is Monday–Friday and weekend is Saturday–Sunday. Average daily sales are used for a fairer weekday/weekend comparison.
- Findings describe the workbook data only; they do not prove why a store or product performed as it did.

## Repository structure

```text
SmartMIS-Cafe-Business-Analysis/
├── README.md
├── Excel-Project/
│   └── SmartMIS_India_Final_Weekday_Weekend.xlsx
├── Documentation/
│   ├── SmartMIS_Project_Documentation.pdf
│   ├── SmartMIS_Project_Documentation.docx
│   └── SmartMIS_Interview_Explanation_Guide_Hinglish.txt
└── Screenshots/
    └── (dashboard screenshots can be added after final visual review)
```

## Interview presentation guide

A clear sequence for explaining this project:

1. Introduce the business context and owner questions.
2. Explain the source data and clearly state which parts are synthetic.
3. Open the dashboard and explain the headline KPIs.
4. Show store, product and category comparisons.
5. Explain monthly and Q1/Q2 trends.
6. Explain the weekday/weekend comparison using average daily sales.
7. Close with limitations and the additional data needed for inventory and net-profit reporting.

Use the accompanying Hinglish interview guide for a more detailed sheet-by-sheet walkthrough and practice questions.

## Files

- [Excel workbook](Excel-Project/SmartMIS_India_Final_Weekday_Weekend.xlsx)
- [Project documentation (PDF)](Documentation/SmartMIS_Project_Documentation.pdf)
- [Project documentation (DOCX)](Documentation/SmartMIS_Project_Documentation.docx)
- [Interview explanation guide (Hinglish)](Documentation/SmartMIS_Interview_Explanation_Guide_Hinglish.txt)

---
Built as a portfolio and interview-practice project.
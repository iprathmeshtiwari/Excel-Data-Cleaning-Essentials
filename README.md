# Excel Data Cleaning Essentials — Customer Data Project

![Excel Data Cleaning Essentials](https://raw.githubusercontent.com/iprathmeshtiwari/Excel-Data-Cleaning-Essentials/refs/heads/main/3.png)

A portfolio-ready Excel data-cleaning project using a synthetic customer-purchases dataset. The raw CSV intentionally contains common quality issues so you can practice finding, documenting, and fixing them.

## Project goals
- Standardize inconsistent text (names, cities, emails, phone numbers)
- Identify missing and invalid values
- Detect exact duplicate rows
- Validate ages, quantities, prices, ratings, and email formats
- Check purchase calculations
- Create a data-quality report and summarize the cleaned data

## Repository structure
```text
Excel_Data_Cleaning_GitHub_Project/
├── data/
│   ├── customer_data_raw.csv
│   ├── customer_data_cleaned.csv
│   └── data_quality_report.csv
├── excel/
│   └── Customer_Data_Cleaning_Workbook.xlsx
├── docs/
│   └── cleaning_steps.md
└── README.md
```

## Dataset
- Synthetic sample with 12,000 generated customer records plus deliberately repeated rows.
- Fields include customer details, location, purchase date, product, quantity, price, payment method, and rating.
- No real customer information is used.
- The workbook's `Raw_Data_Sample` sheet contains the first 500 raw rows to keep Excel responsive; the full raw CSV is in `data/`.

## How to complete the project in Excel
1. Open `excel/Customer_Data_Cleaning_Workbook.xlsx`.
2. Keep `Raw_Data_Sample` unchanged; use `data/customer_data_raw.csv` as the full source if desired.
3. Import the full CSV using **Data → From Text/CSV**.
4. Use **Format as Table** and turn on filters.
5. Inspect blanks, duplicates, inconsistent text, and incorrect data types.
6. Use helper columns with `TRIM`, `CLEAN`, `PROPER`, `LOWER`, and `SUBSTITUTE`.
7. Validate numeric values: age 18–100, quantity 1–20, customer rating 1–5, unit price above zero.
8. Validate email format with a basic pattern check. This does not prove that an email inbox exists.
9. Check `Purchase_Amount = Quantity × Unit_Price`.
10. Use **Data → Remove Duplicates** only after deciding which columns define a duplicate.
11. Record the issue counts and explain any decisions in the `Data_Quality` sheet.
12. Build PivotTables for sales by city, category, product, payment method, and month.

## Useful Excel formulas
Assuming the source fields are in the columns shown in the CSV:
- Clean name: `=PROPER(TRIM(CLEAN(B2)))`
- Clean email: `=LOWER(TRIM(C2))`
- Remove phone spaces: `=SUBSTITUTE(D2," ","")`
- Flag age: `=IF(AND(G2>=18,G2<=100),"Valid","Review")`
- Flag rating: `=IF(AND(P2>=1,P2<=5),"Valid","Review")`
- Check amount: `=IF(N2=L2*M2,"Match","Review")`

Formula column letters depend on where you place the data; check the header row before using them.

## Deliverables
- Raw practice data
- Cleaned example output
- Excel workbook with cleaning guide, quality report, and summary
- Standalone data-quality report

## Important note
The cleaned CSV demonstrates one reasonable set of rules, not the only correct answer. Missing values are not automatically filled with guesses; invalid ages/ratings/quantities are marked blank for review. For real business data, document the rules with the data owner before deleting or imputing records.



Practice Excel data cleaning with a synthetic 12K+ customer dataset. Covers text standardization, missing values, duplicate detection, data validation, data-quality reporting, and sales analysis.

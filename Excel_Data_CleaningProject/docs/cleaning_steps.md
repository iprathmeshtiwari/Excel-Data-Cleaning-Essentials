# Step-by-step Excel cleaning checklist

## Phase 1 — Profile the raw data
- [ ] Preserve the original CSV.
- [ ] Import via Data → From Text/CSV.
- [ ] Confirm row count and column names.
- [ ] Check blanks, data types, ranges, and unique values.

## Phase 2 — Standardize
- [ ] Trim and clean names.
- [ ] Lowercase and trim emails.
- [ ] Standardize city/state capitalization.
- [ ] Remove spaces and formatting inconsistencies from phone numbers.
- [ ] Convert dates and numeric columns to correct types.

## Phase 3 — Validate
- [ ] Flag malformed emails.
- [ ] Check age range (18–100 for this practice project).
- [ ] Check quantity range (1–20).
- [ ] Check ratings (1–5).
- [ ] Confirm prices are positive.
- [ ] Compare purchase amount with quantity × unit price.

## Phase 4 — Duplicates and missing values
- [ ] Identify exact duplicate rows.
- [ ] Decide whether customer ID, email, or full-row equality defines a duplicate.
- [ ] Report missing values by column.
- [ ] Do not invent missing information; document decisions.

## Phase 5 — Reporting
- [ ] Report counts before and after cleaning.
- [ ] Create PivotTables by city, product, category, payment method, and month.
- [ ] Add charts and a simple dashboard.
- [ ] Save final workbook and export the cleaned data to CSV.

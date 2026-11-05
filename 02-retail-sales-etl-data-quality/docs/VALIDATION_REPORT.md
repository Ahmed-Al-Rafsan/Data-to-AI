# Validation report — synthetic sample

## Verified baseline

- Source shape: **58 × 12**.
- Nulls in original input: **2 Quantity**, **1 DiscountPct**, **1 ShippingState**.
- Exact duplicate rows: **2**; remaining unique rows: **56**.
- Non-numeric unit price: **1**, `OrderID 10038`, raw value `not available`.
- Missing quantity orders: `OrderID 10046` and `OrderID 10012`.
- Accepted by required quantity and price checks: **53** records × 12 columns.
- Rejected: **3** records × 13 columns (including `Reject Reasons`).
- Reconciliation: **53 + 3 = 56** non-duplicate records.
- Input contains **0 invalid parsed OrderDate** values in this sample.

## Checks performed

1. `pd.read_csv()` loads the raw CSV.
2. `drop_duplicates(keep='first')` retains 56 unique rows.
3. `pd.to_numeric(..., errors='coerce')` detects the nonnumeric price.
4. Nullable integer quantity preserves missing observations.
5. Boolean mask partitions each deduplicated row into accepted or rejected.
6. CSV and JSON exports are created; exported CSV files are read back and row counts checked.
7. Logger writes extraction status and record counts.

## Known limitations

- The accepted/rejected gate currently checks **quantity and price**, not every possible business rule.
- Unknown `DiscountPct` remains in accepted data; discounted totals would require an explicit policy.
- Rejection reason uses the **first matching condition** if a row has multiple issues.
- This small dataset is synthetic; the demonstration is not evidence of operational scale.
- It is a manually executed notebook, not a scheduled or cloud ETL.
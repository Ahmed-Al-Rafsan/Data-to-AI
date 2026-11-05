# Project scope and delivery plan

**Version:** 1.0 · **Type:** Local CSV-to-CSV/JSON ETL · **Dataset:** 58 synthetic retail transactions

**Objective:** Turn imperfect retail order records into traceable accepted/rejected outputs without manufacturing missing monetary values.

| Stage | Planned outcome | State |
|---|---|---|
| 1. Extract | Read synthetic retail CSV | Done |
| 2. Profile | Check row counts, missingness, columns | Done |
| 3. Clean | Approved fill and exact deduplication | Done |
| 4. Type checks | Parse date, numeric price, nullable integer quantity | Done |
| 5. Validate | Reject missing quantity and invalid price | Done |
| 6. Load | Export accepted and rejected CSV/JSON | Done |
| 7. Reliability | File-not-found handling, count logging, read-back validation | Basic checks done |
| 8. Publish | README, architecture, GitHub and career materials | In progress |

**Definition of done:** Runs on the included synthetic CSV and reproduces 53 accepted rows, 3 rejected rows, and 2 removed duplicate rows. Export counts match in-memory counts; source CSV remains untouched.

**Out of scope:** Azure, Databricks, orchestration, production automation, real enterprise source systems, revenue forecasting, and resolving unknown discounts.
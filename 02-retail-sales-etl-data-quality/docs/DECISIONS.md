# Data-quality decision log

| ID | Decision | Reason | Caveat |
|---|---|---|---|
| DQ-01 | Preserve source CSV, work on a copied DataFrame | Traceability and reproducibility | Notebook still requires correct working folder |
| DQ-02 | Fill missing shipping state as `Unknown` | Categorical placeholder does not invent a location | Business-owner approval would be needed in real company |
| DQ-03 | Remove exact duplicate rows, keeping first | Avoid counting identical transactions twice | Duplicate OrderIDs with different data need separate investigation |
| DQ-04 | Keep missing discount as missing | Zero would falsely mean no discount | Do not use for definitive discounted-revenue totals |
| DQ-05 | Convert invalid price to missing with `errors='coerce'` | Prevent crash, expose data-quality issue | Original raw CSV is retained as evidence |
| DQ-06 | Keep quantity nullable (`Int64`) | Whole-item purchases with missing values | Fractional quantities might apply to other retail contexts |
| DQ-07 | Quarantine rows without quantity or usable price | Exclude unreliable monetary calculations without deleting history | Orders remain useful for some non-financial counting |
| DQ-08 | Log counts and input read errors | Simple operational trace | Not a production monitoring solution |

**Open question:** Confirm business rules for missing discounts and whether dates are mandatory; document before adding further rejection conditions.
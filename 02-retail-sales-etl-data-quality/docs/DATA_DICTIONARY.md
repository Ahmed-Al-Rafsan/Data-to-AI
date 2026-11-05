# Data dictionary

The input file contains 12 columns, 58 synthetic rows. Expected interpretations are inferred from the demonstration data and should be validated against an upstream business contract in a real system.

| Column | Meaning | Intended type | Special handling |
|---|---|---|---|
| OrderID | Order identifier | Integer identifier | Not an amount |
| OrderDate | Transaction date | Datetime | Converted from string |
| CustomerID | Customer identifier | String | Preserve letter prefix |
| ProductID | Product identifier | String | Preserve letter prefix |
| ProductCategory | Merchandise category | String | Kept |
| ProductName | Product label | String | Kept |
| Quantity | Items in transaction | Nullable integer (`Int64`) | Missing → quarantine |
| UnitPrice | Per-item price | Decimal-capable numeric (float in this demo) | Invalid → `NaN` → quarantine |
| DiscountPct | Discount fraction | Float | `0.15` means 15%; missing retained |
| ShippingState | Australian destination state | String | Missing → `Unknown` |
| PaymentMethod | Payment category | String | Kept |
| SalesChannel | Online/in-store channel | String | Kept |

**Output-only field:** `Reject Reasons` describes the first failed validation rule for rejected records.
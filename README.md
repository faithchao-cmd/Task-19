# Top 10 Products by Sales

## Description
Identify the top 10 products by total sales.

## Objective
Practice ranking and sorting.

## Tool
- Microsoft Excel

## Dataset
Superstore — `Sales_Data.xlsx`, 3,000 order-level rows across 30 unique products.

## Method
1. Aggregated **Sales** and **Units Sold** per unique Product Name (PivotTable / SUMIF).
2. Sorted the resulting product list descending by total Sales.
3. Checked for ties at the rank-10 cutoff before finalizing the table.
4. Took the top 10 rows and charted Sales and Units Sold as a line chart with dual axes.

## Results — Top 10 Products

| Rank | Product Name | Sales | Units Sold |
|---:|---|---:|---:|
| 1 | Multifunction Copier | 1,256,981.71 | 1,736 |
| 2 | Round Conference Table | 224,329.89 | 502 |
| 3 | Compact Laser Printer | 222,026.49 | 828 |
| 4 | Adjustable Standing Desk | 174,428.72 | 490 |
| 5 | Desktop Scanner | 163,287.96 | 770 |
| 6 | 5-Shelf Bookcase | 147,643.11 | 797 |
| 7 | Executive Leather Chair | 136,065.06 | 498 |
| 8 | 3-Drawer File Cabinet | 116,125.09 | 715 |
| 9 | VoIP Desk Phone | 110,267.62 | 738 |
| 10 | Corner Bookcase | 95,981.10 | 657 |

## Chart
Line chart, dual axes: **Units Sold** (left, blue) and **Sales** (right, red), across the 10 products ranked by Sales.

## Tie Check
No two products share the same Sales total at or near the rank-10 cutoff — rank 10 ($95,981.10) and rank 11 ($82,570.37) are separated by over $13,000. No tie-break was needed. If one had occurred, the fallback rule is to break the tie using **Units Sold** as the secondary sort key, since that's the second metric available in this sheet.

## Key Findings
- **Multifunction Copier dominates** — $1.26M in sales, over 5× the #2 product, and roughly 40% of total company sales across just 30 products.
- Units Sold tracks Sales closely at the very top (Multifunction Copier also has the highest unit volume, 1,736), but the two metrics diverge further down the list — e.g. Compact Laser Printer (#3 by Sales) actually outsells Round Conference Table (#2) in units, 828 vs 502.
- Sales values flatten out considerably after rank 1 — the gap from rank 2 to rank 10 ($224K → $96K) is much smaller than the drop from rank 1 to rank 2.
- High Units Sold doesn't guarantee a high Sales rank — several mid-table products move similar or greater volume than higher-ranked items, meaning per-unit price drives much of the ranking below #1.




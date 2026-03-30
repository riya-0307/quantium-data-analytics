# Quantium Data Analytics – Forage Job Simulation

This is my work from Quantium's Data Analytics job simulation on Forage, completed in February 2026. The project involved analysing real retail transaction data for a chips category and presenting findings to a Category Manager — which made it feel a lot closer to actual work than most practice projects.

---

## What I worked with

Two datasets:
- `QVI_purchase_behaviour.csv` — customer loyalty card data with lifestage and premium segment labels
- `QVI_transaction_data.xlsx` — 264,836 transactions with product names, quantities, and sales figures

---

## What I actually did

**Data cleaning & prep**
Loaded both datasets, checked for nulls, filtered out zero-quantity rows, and converted Excel serial dates to proper datetime format. Extracted brand names and packet sizes directly from the product name strings using regex, then standardised inconsistent brand names (e.g. `Smith` → `Smiths`, `WW` → `Woolworths`).

**Customer analytics**
Merged the transaction data with customer segments and ran a breakdown of total sales, number of customers, average spend per customer, trips per customer, and average unit price — all grouped by lifestage and premium tier.

Key findings:
- Older Families (Budget) were the top segment by sales — $44,859 (8.77% market share)
- Older Families (Mainstream) had the highest spend per customer at $14.41
- Family segments also shopped more frequently, averaging around 2 trips per customer vs ~1.4 for Young Singles
- Mainstream Young Singles paid significantly higher unit prices than Budget or Premium peers (t-stat: 17.58, p < 0.0001)

**Pack size & brand analysis**
Looked at 330g pack preferences across segments — Older Families bought 1,149 units vs 865 for Young Singles. For brand affinity, Mainstream Young Singles skewed heavily toward Doritos (29.3%) and Smiths (23.6%), while budget-conscious segments spread spend more evenly.

**Visualisations**
Built three charts using Plotly:
- Heatmap of total sales by customer segment
- Scatter plot of customer count vs total spend
- Pack size distribution histogram for the top 3 segments

**Presentation**
Pulled all of this into a Category Review slide deck for the (fictional) Category Manager Julia, with an executive summary, strategic recommendation, and a next-steps execution plan.

---

## Tools & libraries

- Python 3.9
- VS Code
- pandas, openpyxl, scipy, plotly

---

## What I took away from this

The t-test result was one of those moments that made the analysis feel real — confirming statistically that Mainstream Young Singles genuinely pay more per unit, not just slightly more on average. It's a small thing but it changes how you'd approach a recommendation. The whole project pushed me to think less about running code and more about what the numbers actually mean for the business.

---

Certificate issued by Quantium via Forage · February 2026

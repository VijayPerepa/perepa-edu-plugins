---
name: variance-ratio-analysis
description: Performs variance analysis (budget vs actual, month-on-month, year-on-year) and financial ratio analysis on Excel/CSV or Drive/SharePoint data. Use when the user says "variance analysis", "budget vs actual", "MoM", "YoY", "ratio analysis", "liquidity/profitability ratios", or "why did expenses go up".
---

# Variance and Ratio Analysis

Load the data from the uploaded file, or from Google Drive / Microsoft 365 if the user points to a file there. Profile it first: sheets, columns, periods, missing values, duplicates.

## Conventions
- Currency INR; show lakhs/crores when amounts are large. Fiscal year April–March (Q1 = Apr–Jun).
- Variance = Actual − Budget (or Current − Prior). Show absolute and %. For costs, label favourable/adverse correctly (higher cost = adverse).

## Workflow
1. Confirm periods and the comparison basis with the user only if ambiguous.
2. Compute variances by line item and by month/quarter; rank the top drivers.
3. Compute requested ratios: current, quick, debt-equity, interest coverage, gross/net margin, ROE, ROCE, DSO/DPO/inventory days. State the formula used.
4. Run the arithmetic in code; never estimate figures.
5. Deliver a short commentary: what moved, likely cause, what to check. Separate facts from hypotheses.
6. Output as Excel for working and a PEREPA EDU branded Word/PPTX summary if client-facing.

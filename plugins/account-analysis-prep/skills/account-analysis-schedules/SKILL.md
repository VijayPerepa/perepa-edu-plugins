---
name: account-analysis-schedules
description: Prepares audit-ready account analysis schedules that break down each balance sheet account's closing balance into components (opening, additions, deletions, open items) and tie it back to the trial balance. Use when the user says "account analysis", "prepare account analysis", "balance breakup", "schedules for audit", "PBC schedules", "lead schedules", or "analyse this GL balance".
---

# Account Analysis Schedules

Start from the mapped TB (run trial-balance-mapping first if it is not mapped) and the supporting ledgers or sub-ledgers.

## Conventions
- INR, April–March year, prior-year comparatives alongside current year.
- Every schedule must tie: schedule total = TB closing balance. Show the difference, even if zero.

## Workflow
1. For each balance sheet account (or the ones the user names), build a schedule:
   - Roll-forward: opening + additions − deletions/payments ± adjustments = closing.
   - Breakup of closing balance into open items (party, invoice/reference, date, amount, age).
   - Supporting evidence column: what document supports each item (invoice, agreement, confirmation, bank statement).
2. Typical schedules: fixed assets and CWIP, advances and deposits, prepaid expenses, other receivables, statutory dues (GST, TDS, PF/ESI, PT), provisions and accruals, other current liabilities, related party balances.
3. Flag items that are old (over 1 year), have no supporting reference, carry an unusual sign, or that cannot be broken down from the data.
4. Do all arithmetic in code; never estimate a balance.
5. Deliver an Excel workbook: a Lead sheet (account, TB balance, schedule total, difference, status) plus one tab per account, and an Open Points tab listing what is pending from the client.

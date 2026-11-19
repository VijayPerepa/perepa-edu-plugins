---
name: trial-balance-mapping
description: Maps a trial balance to Schedule III (Division I/II) groupings, checks that it balances, and produces a grouped balance sheet and P&L for account analysis. Use when the user says "map the trial balance", "TB mapping", "Schedule III grouping", "group these ledgers", or "prepare TB for account analysis".
---

# Trial Balance Mapping

Load the TB from the uploaded file (Tally/SAP/Zoho export) or from Google Drive / Microsoft 365. Profile it first: columns (ledger, group, opening, debit, credit, closing), period, blank or duplicate ledgers.

## Conventions
- Currency INR; present in lakhs or crores to match the client's reporting. Fiscal year April–March.
- Ask whether the entity reports under Ind AS (Division II) or AS (Division I) only if it is not clear from the data.

## Workflow
1. Check the TB balances: total debits = total credits, and opening + movements = closing for each ledger. Report any difference to the rupee.
2. Map every ledger to a Schedule III line item (e.g. Trade receivables, Other current liabilities, Finance costs). Use the client's existing group as a hint, not as truth.
3. Flag ledgers that are hard to map, have an unexpected sign (debit balance in a creditor, credit balance in a debtor or expense), or sit in suspense/clearing/miscellaneous groups.
4. Split current vs non-current where the data allows; list where it needs management input.
5. Run all totals in code; never estimate figures.
6. Deliver an Excel workbook: Mapped TB (ledger → line item → note no.), Grouped BS and P&L, and an Exceptions sheet. Keep the mapping as a reusable table for the next period.

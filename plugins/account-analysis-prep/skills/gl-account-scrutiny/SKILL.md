---
name: gl-account-scrutiny
description: Scrutinises general ledger account transactions to find unusual, duplicate, misclassified or non-compliant entries before close or audit. Use when the user says "ledger scrutiny", "GL scrutiny", "scrutinise this ledger", "review expense ledgers", "find unusual entries", or "journal entry testing".
---

# GL Account Scrutiny

Load the ledger/day-book export from the upload or Drive/SharePoint. Profile it: accounts, date range, voucher types, narration quality, missing fields.

## Checks (run in code, report counts and amounts)
- Duplicates: same party, amount and date (or invoice no.) posted more than once.
- Round-sum and threshold entries: round lakhs, amounts just below approval or TDS thresholds.
- Timing: entries on Sundays/holidays, after period end, or back-dated; heavy postings in the last days of March.
- Manual journals to revenue, cash, bank or suspense; reversals and contra entries without narration.
- Misclassification: capital items in revenue expense (and the reverse), personal or non-business narrations, prepaid amounts expensed in full.
- Compliance pointers: expenses where TDS looks applicable but none is deducted (194C/194J/194I/194H/194Q), GST ITC claimed on blocked credits (Sec 17(5)), cash payments above ₹10,000 (Sec 40A(3)).
- Unexplained narrations: blank, "being amount", "adjustment" without reference.

## Workflow
1. Confirm which accounts and period to scrutinise only if not obvious.
2. Run the checks; rank exceptions by amount and risk.
3. For each exception give the voucher reference, why it was flagged, and what document to ask for. Mark these as points to verify, not conclusions.
4. Deliver an Excel working paper (one sheet per check plus a summary) and, if client-facing, a short PEREPA EDU branded Word note of query points.

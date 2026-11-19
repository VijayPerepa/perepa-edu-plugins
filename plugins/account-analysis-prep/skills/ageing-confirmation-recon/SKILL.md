---
name: ageing-confirmation-recon
description: Builds receivable, payable and advance ageing, flags MSME dues under Section 43B(h), and reconciles the ledger with party statements or balance confirmations. Use when the user says "debtors ageing", "creditors ageing", "AR/AP ageing", "MSME 45 days", "43B(h)", "balance confirmation", "vendor statement reconciliation", or "party ledger recon".
---

# Ageing and Balance Confirmation Reconciliation

Load the open-items or party ledger export and, for reconciliation, the party's statement or confirmation.

## Ageing
1. Age open items by invoice date (or due date if the user prefers) as of the reporting date. Default buckets: 0–30, 31–60, 61–90, 91–180, 181–365, over 365 days.
2. Allocate receipts/payments to oldest invoices first (FIFO) unless the data has item-level matching.
3. Show top parties by balance, credit balances in debtors and debit balances in creditors, and unadjusted advances.
4. Receivables: highlight balances over 180 days and over 365 days as candidates for provisioning / expected credit loss review; do not decide the provision.
5. Payables: flag MSME suppliers (if the vendor master has MSME/Udyam status) with dues beyond the agreed term or 45 days, since unpaid amounts at year end may be disallowed under Section 43B(h). Note where MSME status is missing.

## Reconciliation (ledger vs party statement)
1. Match by invoice number, then by amount and date within a tolerance the user sets.
2. Classify differences: invoices not booked, payments in transit, TDS deducted not reflected, GST or rate differences, debit/credit notes not accounted, duplicates.
3. Show: balance as per books, add/less reconciling items, balance as per party, unexplained difference.

## Output
Run everything in code. Deliver Excel (Ageing summary, Ageing detail, MSME flags, one recon sheet per party) and, if client-facing, a PEREPA EDU branded Word summary of key exceptions.

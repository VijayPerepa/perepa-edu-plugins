---
name: gst-tds-reconciliation
description: Reconciles a purchase register against GSTR-2B to find ITC mismatches and checks TDS deductions against applicable section rates. Use when the user says "GST reconciliation", "GSTR-2B vs purchase register", "ITC mismatch", "TDS check", "TDS shortfall", or "194C/194J/194I".
---

# GST and TDS Reconciliation

## GST (purchase register vs GSTR-2B)
1. Read both files; normalise GSTIN, invoice number (strip spaces, case, leading zeros), and invoice date.
2. Match on GSTIN + invoice number; fall back to fuzzy match on GSTIN + amount + date.
3. Classify each row: Matched, Amount mismatch (taxable value, IGST/CGST/SGST), Missing in 2B (ITC at risk), Missing in books, Duplicate, Period mismatch.
4. Summarise ITC eligible, ITC at risk, and vendors to chase, ranked by value.

## TDS
1. Map each payment to its section (194C contractors, 194J professional/technical, 194I rent, 194H commission, 194Q purchase of goods, etc.).
2. Apply the rate and threshold from the latest rules; if unsure, confirm with a web search before applying. Use higher rate where PAN is missing (206AA).
3. Compute TDS due vs deducted, shortfall, and illustrative interest (1% per month for late deduction, 1.5% per month for late deposit, part-months counted as full).
4. Flag late deposits and missing PAN.

## Output
Excel with Summary, Matched, Exceptions and TDS sheets; short action list. State clearly this is a working reconciliation, not a filing or tax opinion.

# Data Migration Checklist

**Company:** Sample Trading Co. (fictional)
**Goal:** Move customers, items, and open orders from spreadsheets into the new ERP system without losing or duplicating data.
**Version:** 1.0 (draft)

## What gets moved

| Data | Source today | Owner | Approx. records (made-up) |
| --- | --- | --- | --- |
| Customers | `customers.xlsx` | Sales Supervisor | 420 |
| Items and prices | `price_list.xlsx` | Warehouse + Sales Supervisor | 850 |
| Opening stock | Warehouse count sheet | Warehouse | 850 |
| Open orders (not yet delivered) | `orders_2026.xlsx` | Sales Supervisor | 60 |
| Unpaid invoices | `receivables.xlsx` | Accounting | 95 |

Closed orders and paid invoices from past years are **not** moved. They stay in the old spreadsheets as an archive.

## Phase 1: Prepare

- [ ] Name one owner for each data set (see table above)
- [ ] Agree on the **required fields** for each data set (for customers: name, address, contact number, payment terms)
- [ ] Take a backup copy of every source spreadsheet and note the date
- [ ] Freeze the source files: only the owner edits them from now on
- [ ] Agree on the import template for each data set (see `customers_template.csv`)

## Phase 2: Clean

- [ ] Remove blank rows and test entries
- [ ] Find duplicate customers (same name written differently, same phone number) and decide which record to keep
- [ ] Make sure each customer has a unique code
- [ ] Check phone numbers use one format
- [ ] Check items: no missing prices, no repeated item codes, one unit of measure per item
- [ ] Check opening stock counts against a quick physical count of 20 sample items
- [ ] Remove or close orders that are already delivered

## Phase 3: Map

- [ ] Match each spreadsheet column to a field in the new system (for example, `Cust Name` to `Customer Name`)
- [ ] List the columns that have no place in the new system and decide: drop them or store them in a notes field
- [ ] Convert dates to one format (YYYY-MM-DD)
- [ ] Convert yes/no and status words to the values the system accepts

## Phase 4: Test import

- [ ] Import a small batch (about 20 customers) into the **test** system
- [ ] Compare the imported records to the spreadsheet row by row
- [ ] Write down every error and fix the source file, not the test system
- [ ] Repeat with the full file until the error count is zero
- [ ] Ask one sales clerk to create a sample order using an imported customer and imported items

## Phase 5: Go-live import

- [ ] Choose a low-activity time (for example, after closing on a Friday)
- [ ] Confirm the final backup exists
- [ ] Import in this order: **items, customers, opening stock, open orders, unpaid invoices**
- [ ] Compare record counts to the source files and write them down

| Data | Count in source | Count in system | Match? |
| --- | --- | --- | --- |
| Customers | | | |
| Items | | | |
| Open orders | | | |
| Unpaid invoices | | | |

- [ ] Compare totals: sum of unpaid invoices in the source vs. in the system
- [ ] Spot-check 10 records per data set against the source

## Phase 5 sign-off

- [ ] Data owners confirm their data is correct
- [ ] Project lead confirms the counts and totals match
- [ ] Old spreadsheets are set to read-only and kept as an archive

## Common problems and what to do

| Problem | What to do |
| --- | --- |
| The same customer appears twice | Keep the record with the most complete details and the most recent activity. Record the other code as "merged" in the notes. |
| Item has no price | Ask the owner for the price. Do not import it with a guessed price. |
| Import fails on a date column | Check the format. Dates stored as text in the spreadsheet often cause this. |
| Counts do not match | Look for rows that were rejected. Fix and re-import only those rows. |
| Opening stock differs from the physical count | Record the physical count as the opening stock and note the difference. |

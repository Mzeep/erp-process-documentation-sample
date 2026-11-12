# Requirements Mapping

**Company:** Sample Trading Co. (fictional)
**Purpose:** Connect each business need to a system feature, the person who owns it, and a test that shows it works.
**Priority:** M = must have, S = should have, C = could have

| ID | Business need | Priority | System feature (generic ERP) | Owner | How we test it |
| --- | --- | --- | --- | --- | --- |
| R01 | Enter an order once and have the warehouse and accounting see it | M | Sales order that flows to delivery and invoice | Sales Supervisor | Create an order and confirm the warehouse sees a pick list and accounting sees the order |
| R02 | Prevent duplicate customer records | M | Duplicate check on name and phone number when creating a customer | Sales Supervisor | Try to create a customer with an existing name and phone; the system warns |
| R03 | Show stock available when taking an order | M | Available stock column on the order line | Warehouse | Order more than the available stock; the line is flagged |
| R04 | Stop the same stock from being sold twice | M | Stock reservation when an order is confirmed | Warehouse | Confirm two orders for the last 5 units; the second is flagged |
| R05 | Orders above credit limit need approval | M | Credit limit check with approval step | Accounting | Create an order above the limit; status becomes "Waiting for Approval" |
| R06 | Prices come from one price list | M | Price list linked to items and customers | Sales Supervisor | Add an item; the price matches the list. An item without a price cannot be confirmed |
| R07 | Create invoices from recorded deliveries only | M | Invoice generated from the delivery record | Accounting | Try to invoice an order with no delivery; the system refuses |
| R08 | Record customer payments against invoices | M | Payment matching screen | Accounting | Record a payment and check the invoice shows as paid |
| R09 | See open orders by customer | S | Open orders report with a customer filter | Sales Supervisor | Run the report for one customer and compare with the order list |
| R10 | See unpaid invoices by age (30 / 60 / 90 days) | S | Aged receivables report | Accounting | Run the report and compare totals to the invoice list |
| R11 | Partial deliveries | S | Split delivery on a sales order | Warehouse | Deliver part of an order; the balance stays open |
| R12 | Print a pick list for the warehouse | S | Pick list print layout | Warehouse | Print from a confirmed order and check items and quantities |
| R13 | Import existing customers and items from spreadsheets | M | Import templates for customers and items | Project lead | Import the test batch and compare to the source (see migration checklist) |
| R14 | Limit who can change prices | S | User roles and permissions | IT / Sales Supervisor | Log in as a sales clerk and try to edit a price; the system blocks it |
| R15 | Send an order confirmation email to the customer | C | Email template on order confirmation | Sales Supervisor | Confirm an order and check the email content |

## Notes

- **Gaps:** If a business need has no matching feature in the ERP, it is marked as a gap and discussed with the project lead. Options are a workaround, a setting change, or leaving it for a later phase.
- **Traceability:** Each need (R01 to R15) is also used in the user manual and the process flow, so anything that changes in one place can be checked in the others.
- **Open question:** R11 (partial deliveries) depends on the company's answer in the process flow document.

## Sign-off

| Name | Role | Date | Approved? |
| --- | --- | --- | --- |
| | Sales Supervisor | | |
| | Warehouse Lead | | |
| | Accounting Lead | | |
| | Project Lead | | |

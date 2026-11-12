# User Manual: Create a Sales Order

**Company:** Sample Trading Co. (fictional)
**Who this is for:** Sales clerks
**Time needed:** About 5 minutes per order
**Version:** 1.0 (draft)

> The screens and button names below belong to a generic ERP and are used as an example only.

## Before you start

Have these ready:

- The customer's name or customer code
- The items and quantities the customer wants
- The delivery date the customer asked for
- The customer's purchase order number, if they gave one

## Steps

### 1. Find the customer

1. Open **Sales** from the main menu, then choose **Customers**.
2. Type the customer's name or code in the search box and press Enter.
3. If the customer is in the list, open it and check the address and payment terms are correct.
4. If you do not find the customer, try a shorter part of the name once. If it still does not appear, go to **Create a new customer** at the end of this manual.

> Do not create a new customer until you have searched twice. Duplicate customers make invoices and reports wrong.

### 2. Start the order

1. From the customer page, click **New Sales Order**.
2. Check that the customer name at the top is correct.
3. Enter the customer's purchase order number in **Customer Reference**, if they gave one.
4. Set the **Delivery Date**.

### 3. Add the items

1. Click **Add Line**.
2. Type the item code or name and choose the item from the list.
3. Enter the **Quantity**.
4. Check the **Unit Price** the system fills in. Do not change it unless you have approval.
5. Repeat for each item.

The **Available Stock** column shows how many units can be sold right now. If the quantity you entered is higher, the cell turns red.

### 4. Review the order

Check these before you save:

- Customer name and delivery date
- Each item code, quantity, and price
- The order total at the bottom

### 5. Save and confirm

1. Click **Save**. The order is saved as a **Draft**.
2. Click **Confirm**.
3. The system will do one of three things:
   - **Confirmed:** The order status changes to *Confirmed* and stock is reserved. You are done.
   - **Waiting for Approval:** The order needs your Supervisor to approve it (for example, it is over the credit limit). Tell your Supervisor the order number.
   - **Error message:** See the next section.

### 6. Tell the customer

Give the customer the order number and the expected delivery date.

## When something goes wrong

| What you see | What it likely means | What to do |
| --- | --- | --- |
| "Item has no price" | The item is missing from the price list | Do not guess a price. Send the item code to the Sales Supervisor. |
| Quantity cell is red | Not enough stock | Offer the customer a smaller quantity now and the rest later, or a later delivery date. |
| "Credit limit exceeded" | The order total plus unpaid invoices is above the limit | The order goes for approval. Let the customer know it may take longer. |
| "Customer is on hold" | Accounting has paused the customer's account | Ask Accounting. Do not try to work around it. |
| You cannot find the customer | They are new, or the name is spelled differently | Search twice, then create a new customer. |

## Create a new customer

1. Go to **Customers**, then click **New**.
2. Fill in the required fields (marked with a red asterisk): **Name**, **Address**, **Contact Person**, **Contact Number**, **Payment Terms**.
3. Click **Save**. The system gives the customer a code.
4. Return to Step 2 above.

## Quick checklist

- [ ] Searched for the customer twice before creating a new one
- [ ] Delivery date entered
- [ ] Each price checked, none changed without approval
- [ ] Order saved and confirmed
- [ ] Order number given to the customer

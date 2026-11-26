# Managing Orders and invoices

> Where to find every order for a paid event and what you can do inside an order — invoices, billing details, refunds, exports.

- Article in the Help Center: https://help.happenee.com/en/articles/19-managing-orders-and-invoices
- Česká verze: https://help.happenee.com/cs/articles/19-sprava-objednavek-a-faktur
- Collection: Event setup and registration
- Updated: 2026-10-26

---

> [!info] Overview
> **Orders** is the purchase side of a paid event — who bought what, whether they paid, which invoice was issued, and whether anyone registered against the ticket. Inside an order you fix billing details and the attendee details on a ticket, download the invoice and the ticket PDF, notify people who have not finished registration or have not paid their proforma invoice yet, request a refund for a paid order with no refunded amount recorded, and cancel or delete an unpaid one. In the refund request, you choose how much the buyer gets back and who pays the payment fee. You also decide who gets the e-mail once the refund is completed.

## Getting started

- Orders exist only for events with **Tickets** turned on. Free events never create them.
- Open them from the **Tools** dropdown at the bottom of the left menu, from the *Orders* tile under **Tools** on the event **Overview**, or with the *Orders* button in the top right of the *Tickets* page.
- With **Registration with additional information**, the order comes before the registration: the buyer pays and the attendee registers later. The order list and the registration list will never match one to one.
- Decide up front how you will handle cancellations: you can **request a refund** for a paid order with no refunded amount recorded, or **cancel** or **delete** an unpaid one.
- Invoices cannot be deleted or renumbered manually. Correcting the billing details overwrites them on the existing invoices; no new version of the document is created.

## Details

### What you see in the order list

The order table has the columns **Buyer** (the buyer's name and e-mail — this can be someone other than the attendee), **Ordered**, **Order status**, **Total**, **Currency**, **Paid** (the amount actually received), **Tickets**, and **Registered**. Most of them are sortable.

The order status is one of four values:

- **Paid** — the chip also shows the payment date.
- **Unpaid** — a proforma invoice has been issued and the money has not arrived yet.
- **Cancelled** — the chip also shows the cancellation date.
- **Free** — an order with a zero amount (a free ticket or a 100% discount code). A regular order with a document is still created.

Above the table you get **search by name, e-mail, or company** and a set of filters:

- **Chips with counts** — *All*, *Paid*, *Unpaid*, *Unregistered*, *Cancelled*. The numbers show how many orders fall into each group, so you can see where the work is.
- **Currency** — for events that sell in more than one currency.
- **Registration** — the options *Registered* / *Unregistered*, confirmed with *Apply filter*.
- **Registration reminder** — the options *Not yet notified* / *Already notified*. It narrows the list to orders with unfinished registration, depending on whether you have already sent the attendee a reminder.
- **Payment reminder** — the same two options for unpaid orders: buyers who have already received a reminder and buyers who have not.

The *Unregistered* chip narrows the list to orders where registration is not finished. To see how many tickets in a specific order are already registered, read the *Registered* column, and for the exact picture open the ticket table in the order detail.

### The order detail

An order expands **inside its row** (the arrow at the end of the row); there is no separate page. The detail header shows the **payment method** (card, proforma invoice, or free), the **variable symbol**, and the date the order was **paid**.

An unpaid order with a proforma invoice also has a **Payment reminder** field in the header, with a **Notify** button. It sends the buyer the same e-mail as the bulk **Unpaid** item, for this one order only. While the reminder waits to be sent, the field shows the **Queued** status and the button is disabled. After the send, it shows **Sent** with the date and time, and the button changes to **Send again**.

Below the header is a **Tickets** table with the columns *Name*, *E-mail*, *Ticket price*, *Discounted price*, *Ticket*, *Discount code*, and *Registration*. Each ticket has its own actions:

- **Ticket** — downloads the ticket PDF with the QR code. Available once the registration is finished.
- **Notify** — for a ticket without a finished registration, sends an e-mail with the registration link. After the send, the ticket shows the **Sent** status with the date and time, and the button changes to **Send again**; for five minutes after any link send it stays disabled, so no duplicate e-mail goes out.
- **Pencil icon** — opens the attendee details of that ticket for editing (described below).

### Invoices

Which invoice you can download depends on the payment method:

- **Card payment** — the final invoice (tax document) right away.
- **Bank transfer** — a **proforma invoice** before payment, the **final invoice** once the money arrives.

You download a single document with **Download invoice** in the order detail. To get all invoices at once, use **Exports → Export invoice PDFs**.

### Editing billing details

**Edit billing details** opens the **Billing details** form with the fields *Company*, *Address*, *City*, *ZIP / Postal code*, *Country*, *Company ID*, *VAT ID*, and *Note*, prefilled with the order's current billing details.

When you save, the corrected details carry over to the order and to all of its invoices. **No new invoice is created:** the documents keep their numbers and carry the corrected details once you download them with **Download invoice**.

The change does not touch line items, prices, VAT, or the invoice number, and it does not affect the payment status or the attendees' data. An invoice the buyer already received by e-mail is not sent again.

### Editing attendee details

The pencil icon next to a ticket opens a side panel with the fields *First name*, *Last name*, *E-mail*, *Company*, *Job title*, and *Phone*. You can edit them as long as nobody has registered with the ticket. Typically you are fixing a typo in the e-mail that kept the registration link from arriving, or passing the ticket on to a different person.

- **Saving does not send anything.** Send the new attendee the registration link with **Notify** next to the ticket.
- **The link does not change.** It always shows the current ticket details when opened, so even a link sent earlier to the original address leads to registering the new attendee.
- **Clearing the data** removes every field, including the e-mail, after you confirm. Use it only when the new attendee is not known yet (see *Common pitfalls* for why). A ticket without an e-mail has no **Notify** button; send the link once you add an e-mail again.
- **Once registration is finished**, the panel opens as read-only. Change a registered attendee's details in the **Registration** section.

The original details are not kept anywhere after you edit them. If you might need them, write them down first.

### Refunding, canceling, and deleting an order

Which actions you get in the detail depends on the order status.

**For a paid order**, the **Refund order** button is offered only if no refunded amount has been recorded and the order meets the other refund conditions. It opens the refund request window. The request is not an immediate money transfer: the buyer gets the money back only after the request is processed, which Happenee completes.

Below the window title, **Paid and not yet refunded** shows how much of the order you can refund. Under **How much does the buyer get back**, you pick one of three options. For each one, the window shows right away what the **Buyer gets**, and its description says who pays the payment fee and how much it is:

- **Amount paid minus the payment fee** — preselected. The buyer pays the fee: the system deducts it from the refunded amount, and the buyer gets the rest.
- **Full amount paid** — the buyer gets the whole amount back, and the organizer pays the fee.
- **Custom amount** — in the field right inside this option, you enter exactly how much the buyer gets back; the hint below the field shows the maximum. The organizer pays the fee. Only this option requires an **Internal note** with the reason (200 characters at most); for the other two, the note is optional.

When the payment fee rate is unavailable, you cannot select the first option, *Full amount paid* is preselected, and the window explains this below the options. The first option is also unavailable when deducting the fee would leave the buyer with nothing.

The **Notify the buyer when the refund is completed** and **Notify the organizer when the refund is completed** toggles decide who gets the e-mail with the credit note. It goes out only once the refund is completed. When the window opens, the organizer toggle is on and the buyer toggle is off; you can notify one, both, or neither. A toggle that is on shows an address field; for the buyer, it is prefilled with the address from the order, and you can overwrite it. Each field takes up to 10 addresses separated by commas.

You submit the request with the **Submit request** button at the bottom of the window. Before it is sent, you confirm a dialog that repeats how much the buyer gets back and who pays the fee. It also lists the addresses the result goes to, or warns that nobody will be notified by e-mail.

Once any refunded amount is recorded for an order, the main refund button is no longer shown in its expanded detail in the order list. This also applies to a partial refund or a refund reduced by a fee. A difference between the paid and refunded amounts does not make the button available again. The refund status and available documents remain visible.

**For an unpaid order** you get **Cancel order** and **Delete order** instead. Canceling keeps the order in the list with the *Cancelled* status and its date; deleting removes it together with the document and frees up the seat in ticket statistics.

### Notifying buyers in bulk

Above the list on the right there is a **Notify by e-mail** dropdown with two items. The number next to an item tells you how many recipients the reminder reaches right now: orders for **Unpaid**, individual attendees for **Unregistered**. It can therefore differ from the *Unregistered* chip, which counts orders.

The dropdown follows the same selection as the list. When you narrow the list with the search, a chip, or a filter, the numbers are recalculated and the reminder goes only to that selection. Without filters, it reaches everyone it concerns in the event.

- **Unpaid** — sends the buyers a reminder that their order has not been paid yet. The e-mail has its own wording in Czech, English, or Slovak, following the language of the order, carries the proforma invoice as an attachment, and for Registration with additional information adds that the registration link follows once the order is paid. It goes only to orders that have a proforma invoice, which means bank transfer payments; an abandoned card payment has no proforma invoice and gets no reminder. Cancelled, refunded, and deleted orders, and orders without a valid buyer e-mail, are skipped.
- **Unregistered** — resends the registration link to attendees of paid and free orders who have not finished registration. Typically shortly before the event, when you find out that some people paid but never finished registration and you do not want to send links one by one.

Both items ask for confirmation in a dialog. The reminders do not leave the moment you click: the admin puts them in a queue and the system sends them gradually, one event at a time. An order or ticket still waiting in the queue is not queued a second time, so clicking again does not create duplicate e-mails.

You can send the reminders repeatedly. Once the queue has finished, clicking **Unpaid** again reaches every order in the current selection that is still unpaid. To leave out buyers who have already received a reminder, use the **Payment reminder** filter → *Not yet notified*. Registration links have one more rule: an attendee who received the link within the last five minutes does not get it again.

### Exports

The **Exports** button in the top right offers three files:

- **Orders (Excel)** — one row per order: buyer, amounts, status, billing details. The file your accountant wants.
- **Orders by ticket (Excel)** — one row per ticket, so orders are broken down into individual pieces and attendees.
- **Export invoice PDFs** — every invoice for the event at once, instead of downloading them one by one.

## Common pitfalls

### Looking for Orders among the main items of the left menu

They are not in the main list. Three routes lead there: the **Tools** dropdown at the bottom of the left menu, the *Orders* tile under *Tools* on the event **Overview**, and the *Orders* button in the top right of the *Tickets* page. For a free event, orders are never created at all.

### Expecting the buyer to get a new invoice after you correct the billing details

The correction overwrites the details on the existing invoice under the same number and does nothing else: it does not issue a new invoice and does not e-mail it again. The buyer still has the PDF with the original details. Download the corrected invoice with **Download invoice** and send it to the buyer yourself, noting that the original should no longer be used.

### Deleting a paid order in the belief that this returns the money

A paid order has **Refund order**, not deletion. *Cancel* and *Delete* belong to unpaid orders and do not move any money on their own.

### Keeping the preselected option when the buyer should get everything back

When the window opens, **Amount paid minus the payment fee** is preselected, so unless you change it, the payment fee is deducted from what the buyer gets. You see the fee and the amount the buyer gets right in that option. If the buyer should get everything back, for example because you are canceling the event, select **Full amount paid**. The organizer then pays the fee.

### The buyer paid, but ticket statistics still show a gap between sold and registered

With registration with additional information, the difference between *sold* and *registered* is expected. Sold means a paid order; registered means the attendee went through the registration form. The gap is normal and shrinks as people finish their registrations.

### Bulk notifications also reach people who are not coming

*Notify by e-mail* addresses everyone who matches the current selection; without filters, that is the whole event. Narrow the list before you send, and check the number next to the item. If you know some buyers have already dropped out, send the reminder individually from the order detail: the registration link with **Notify** next to the ticket, the payment reminder with **Notify** in the **Payment reminder** field. Cancel the order of a buyer who has dropped out, and they get no further reminder.

### The unpaid-order reminder does not reach a buyer whose card payment never finished

The **Unpaid** item sends the reminder only to orders that have a proforma invoice, which means bank transfer payments. An abandoned card payment has no proforma invoice, so the system skips it. Reach that buyer another way, or cancel the order.

### The same status is named differently in Orders and in Ticket statistics

In *Orders* the chip is **Cancelled** (status *Cancelled*), while *Ticket statistics* lists the same group under its own heading. It is the same thing under a different name — watch out for it when you reconcile numbers with your accountant.

### Passing a ticket on to someone else by clearing the data

After you clear the data, the ticket has no e-mail, and the registration form accepts any address. Anyone who has the link can then complete the registration, including the original recipient you sent it to earlier. If you already know the new attendee, overwrite the details instead and send them the link with **Notify**. The old link then shows their details.

### Looking for the full attendee record inside the order

An order holds the purchase side — the buyer, the amounts, the document, and the data on individual tickets. Registration form answers, groups, and attendance status live in the **Registration** section. The split is intentional: the order is about the purchase, the registration about the attendee.

## Related articles

- [Setting up Tickets](https://help.happenee.com/en/articles/18-setting-up-tickets)
- [Setting the registration type and additional questions](https://help.happenee.com/en/articles/12-setting-the-registration-type-and-additional-questions)
- [Choosing the right registration type](https://help.happenee.com/en/articles/4-choosing-the-right-registration-type)
- [Setting up Seating](https://help.happenee.com/en/articles/20-setting-up-seating)
- [What to do when an e-mail does not arrive](https://help.happenee.com/en/articles/58-what-to-do-when-an-e-mail-does-not-arrive)
- [What to do when an attendee loses the registration link](https://help.happenee.com/en/articles/59-what-to-do-when-an-attendee-loses-the-registration-link)
- [Fixing an invoice error](https://help.happenee.com/en/articles/60-fixing-an-invoice-error)
- [Working with Orders and exports](https://help.happenee.com/en/articles/52-working-with-orders-and-exports)

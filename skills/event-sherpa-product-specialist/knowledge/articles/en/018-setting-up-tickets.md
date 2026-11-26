# Setting up Tickets

> How to turn on and configure Tickets, including online payments, invoices, and discount codes.

- Article in the Help Center: https://help.happenee.com/en/articles/18-setting-up-tickets
- Česká verze: https://help.happenee.com/cs/articles/18-nastaveni-placenych-vstupenek
- Collection: Event setup and registration
- Updated: 2026-10-26

---

> [!info] Overview
> You turn on Tickets in **Event settings** with the **Tickets** toggle. The system handles online card payments (including Apple Pay and Google Pay), proforma invoices, discount codes, and ticket groups. By default, ticket sales end automatically when the event ends, so nobody can buy a ticket for an event that has already taken place; you set a different deadline or sales without a common deadline under **End of ticket sales**. You manage an individual ticket in a side panel with **Details**, **Attendee details**, and **Ticket settings** tabs.

## Getting started

- Decide on the **pricing model** — one ticket type, multiple types (early bird / standard / VIP), bundles, or individual free invitations.
- Decide whether you want **Registration with additional information** (after payment, the attendee still goes through the form) or **Automatic registration after ticket purchase** (the ticket arrives immediately, no form). See *Setting the registration type and additional questions* for details.
- Prepare your billing data and invoice items, VAT rates (added by customer support), and currency.
- For paid events, you cannot combine Tickets with Approved registration. Required contact fields are governed by the Registration form.
- For GTM tracking codes, contact **customer support**.
- Decide **when sales should end**. By default, they end when the event ends; you set a different deadline under **End of ticket sales** on the **Ticket settings** tab.

## Details

### Turning on Tickets

In the event menu, open **Event settings** → the **Tickets** section and switch on the toggle. A new **Tickets** item appears in the left menu, along with the required follow-up steps:

1. Choose the **currency** — CZK or EUR (other currencies on request).
2. Choose the **registration type after purchase** — *Automatic registration after ticket purchase* or *Registration with additional information*.
3. If you use Registration with additional information, the system reminds you to set the required contact fields in the **Registration form**.

> When Tickets are active, you must **create at least one ticket**. Otherwise registration for the event is closed.

### Creating and editing a ticket

You add a new ticket on the **Tickets** tab with the **+ New ticket** button, and you open an existing one with the edit icon in its row. A side panel opens with three tabs — **Details**, **Attendee details**, and **Ticket settings**. The **Ticket name** field sits above the tabs and is required — it is the name the attendee sees (for example, *Standard*, *VIP*, *Early Bird*). Save your changes with **Save**.

### Details tab

On the **Details** tab, you set the ticket's price and how it looks:

- **Different ticket name on invoice** — by default, the invoice uses the ticket name. When you switch this on, an **Invoice item** field appears for a different name on the tax document (useful when accounting needs a different label than the marketing name).
- **VAT** — the tax rate. If the VAT rate you need is missing, customer support adds it (contact them). The **VAT calculator** button helps you convert between the price with and without tax.
- **Price excl. VAT** — the amount without tax, in the event's currency (the field carries the currency, for example *Price excl. VAT CZK*).
- **Ticket description** — an optional text the attendee sees with the ticket in the purchase view.

### Ticket status

The last choice on the **Details** tab sets the ticket's visibility:

- **Published** — the ticket is publicly displayed in the ticket overview and is available for purchase.
- **Private** — the ticket is not shown in the overview but is available for purchase via a separate link or in a **ticket group**. Useful for partner or VIP tickets you do not want to show everyone.
- **Unpublished** — the ticket is not visible anywhere on the platform and is not available for purchase, not even through its ticket link or in a **ticket group**.

A ticket **cannot be deleted** once it has been used. An unused ticket can be deleted.

### Attendee details tab

On the **Attendee details** tab, you decide which contact fields the attendee fills in and which are required. The fields **First name**, **Last name**, **Company**, **Job title**, and **Phone number** offer **Required**, **Optional**, and **Hide**; **E-mail** is always required. Below them are **Custom contact fields** with the same options — these are created and managed in Workspace settings; here you only decide whether to use them on this ticket.

How the fields behave depends on the registration type after purchase (see *Turning on Tickets*):

- **Registration with additional information** — after payment, the attendee goes through the Registration form, so the required fields are governed by the contact-details settings in the **Registration form**. Fields the form marks as required are locked to **Required** here (kept in sync with the form); for the other fields you set **Required**, **Optional**, or **Hide** as this ticket needs.
- **Automatic registration after ticket purchase** — the Registration form is not used and the ticket arrives right after purchase. You therefore set which fields are required directly on the ticket, and the buyer fills them in during purchase.

### Repeat purchases and attendee e-mail addresses

The buyer's e-mail address is the order contact: the same person can buy again, for example for different colleagues. A matching address is checked when it belongs to an **attendee on a ticket** for the same event. If the buyer also enters their own address as an attendee, the attendee rules apply.

- With **automatic registration after ticket purchase**, another order cannot be completed for an attendee whose e-mail address is already on a valid completed order for that event. This applies even if the first order is still unpaid or its automatic registration has not run yet. Someone else's unfinished cart alone does not block the purchase.
- With **registration with additional information**, a previous purchase or registration triggers a warning, but the buyer can continue.

If the first order is unpaid, the buyer can finish paying it. If the buyer does not want to use it, you can cancel it in the order detail with **Cancel order**, or remove it with **Delete order** (see *Managing Orders and invoices*). A canceled, deleted, or fully refunded order does not block another purchase on its own. With automatic registration, however, an attendee who is already registered for the event still blocks the purchase, whatever the status of the original order. The same attendee e-mail address cannot be used for more than one ticket within a single order.

### Ticket settings tab

On the **Ticket settings** tab inside the ticket panel, you turn on optional sales rules. Each is a toggle (**Active** / **Inactive**); switching it on reveals its field:

- **Option to buy a ticket without providing attendee details** — the buyer can purchase a ticket without filling in the attendee's e-mail address. The ticket is generated later — either when the buyer adds the details, or when the attendee registers through the link they receive. Useful when a company buys tickets in advance and does not yet know who will attend.
- **Limit the maximum number of tickets** — sets the total number of tickets available for purchase. Once sold out, the attendee sees a *Sold out* message in the purchase view.
- **Limit sales period** — **Sale start** and **Sale end** define sales of an individual ticket. Sales start at midnight and end at the end of the selected day in the event time zone. If the common sales deadline for the whole event comes first (see *Ending ticket sales for the whole event*), that deadline applies.
- **Purchase in a bundle** — a minimum order in multiples. With a step of 5, the buyer can purchase only 5, 10, 15 tickets, and so on. Useful for bulk partner purchases or discount bundles.
- **Assign to group** — after the attendee registers (not after the order is paid), the attendee is automatically added to the selected group. Use the group for targeted communication, content and engagement feature visibility, or push notifications in the attendee app. **The assignment only applies going forward:** anyone who registered before you turned the option on does not land in the group, and the system does not add them retroactively.

### What the system reads from a ticket — and what it does not

The ticket name and description are just text to the system. If you name a ticket *One-day* or *Two-day*, the system does nothing further with it — it does not distinguish the length of entry, does not track which days the attendee turns up for, and always adds the full range of the event to the calendar. The difference between ticket types exists only in what a person reads.

The attendee sees the ticket name in the confirmation e-mail and on the invoice — or the **Invoice item**, if you set that to something different. Event staff at check-in, however, do not see the ticket name. After scanning the QR code, they see the attendee's first name, last name, company, and groups, and nothing else.

The practical consequence: if you need to tell ticket types apart on site, turn on **Assign to group** on the ticket and then pick that same group to be shown during scanning in the check-in setup. Prepare the group and its assignment before sales open.

### Ending ticket sales for the whole event

By default, ticket sales end automatically when the event ends, so nobody buys a ticket for an event that has already taken place by mistake. You find this rule at the top of the event-level **Ticket settings** tab, which applies to the whole event, under **End of ticket sales**. In **When to end sales**, choose one of these options:

- **At the end of the event** — the default. Sales end at the moment the event ends, and if you move the event dates, the sales deadline moves with them. If the event has no end time, sales end at midnight after its final day.
- **Custom date and time** — sales end at the deadline you enter, before or after the event. You edit the date and the time separately with the edit icon and confirm each change right at the field.
- **Unlimited** — no common deadline applies, and only the dates on individual tickets limit sales. A ticket without its own **Sale end** can then be bought even after the event ends.

The option you choose is saved immediately, with no extra confirmation. Below the field, you see **Event time zone** and **Common sales deadline**, which is the moment sales actually end. The event time zone applies, including daylight saving changes, not the time zone of your computer. A time that does not exist or occurs twice during a daylight saving change cannot be saved; choose another time.

Once sales have ended, you also see the reason here: *Sales have ended because the event has finished.*, or for a custom deadline *Sales have ended at the configured date and time.*

The common deadline and **Limit sales period** on an individual ticket apply together, and whichever end comes first wins. A ticket whose sales start only after the common deadline cannot be bought at all. If you want to keep selling after the event on purpose, choose **Custom date and time** with a later deadline and check **Sale end** on the individual tickets.











### What buyers see after sales end

A ticket whose sales have ended disappears from the offer, and the other tickets stay on sale. Once sales have ended for every ticket of the event, the purchase view is replaced by the **Ticket sales have ended.** page, which explains that existing orders remain valid. The page does not appear while sales for any ticket have yet to start. It also does not appear just because the offer is empty or the tickets are unpublished or sold out.

The deadline applies equally to the public offer, direct links to private tickets, and **Ticket groups**. A cart opened before sales ended is no exception: the buyer cannot complete an order with a ticket whose sales have ended. Ending sales does not cancel orders, registrations, or payments that already exist.



### Ticket settings (event-level payments)

On the event-level **Ticket settings** tab — which applies to the whole event, not a single ticket — you configure payments:

- **Payment options** — **Card payment and bank transfer**, **Card payment only**, or **Only by bank transfer**. With card payment (including Apple Pay and Google Pay), the buyer receives a tax document immediately; with bank transfer, the system issues a proforma invoice and the tax document follows once it is paid.
- **Price display** — the **Show main price with VAT** toggle controls whether the main price shown with the ticket and in the order summary on the microsite includes VAT.
- **Setting up bank transfer payments (pro-forma invoices)** — the **Advance invoice due date**, which offers **3, 7, 14, or 30 days from issue** (you cannot enter your own number of days).
- **Tracking codes** — for GTM tracking codes, contact customer support.

> The maximum due date is always **at the latest two days before the event starts**. If the chosen due date would fall later, it is automatically shortened. If less than two days remain before the event, the due date is set to the issue date of the invoice.

### Preselecting a ticket from the microsite

Tickets on the microsite have a **Buy** button. The button takes the attendee to the purchase view and adds that ticket to an empty cart right away; you do not set anything up for it. For a regular ticket, it adds one ticket. For a bundle, the quantity follows the configured bundle step, just as it does when using the plus button.

If the attendee already has a ticket in the cart, clicking **Buy** again neither replaces the selection nor increases its quantity. The attendee can change the ticket or quantity directly in the purchase view. Preselection does not bypass ticket availability or the sales period.

After the purchase view opens, the preselection value is removed from the address. Reloading the page therefore does not add the ticket again. Clicking **Buy** after emptying the cart allows a new preselection. If you are testing the button and the cart does not change after you click **Buy** on a different ticket, that is not a bug: the cart from your previous attempt is not empty yet. Try it with both an empty cart and an existing selection.

### Discount codes

In the **Discount codes** section, click **+ New discount code**. You set:

- **Discount type** — percentage or value.
- **Discount amount.**
- **Code validity** — date from–to.
- **Maximum number of uses** — if you leave it unlimited, the code applies without a cap.
- **Limit ticket validity** — the code can apply to all tickets, or only to selected ones.
- **Assign group after using the code** — the attendee who comes through with the code is automatically added to the group.

You can share codes with partners, selected attendees, or in marketing campaigns.

### Individual and bulk registration links

**Individual registration link** — a one-time link that grants free entry to one specific person. The attendee goes through the Registration form and pays nothing. Use cases: guest list, editorial invitations, VIP guests.

**Bulk registration link** — the same idea, but one link for several people. When you create it, you fill in a name and a **Number of uses** from 1 to 500; a bulk link without a limit cannot be created. Use case: partner invitations with a limit (a partner has 6 free invitations, gets one link, and shares it as they see fit).

For both link types, you can set **assignment to a group** after registration.

You can download an overview of all links as a single file: on the **Tickets** page, open **Exports** in the top right and choose **Registration links export**. The Excel file has one row per link, with individual links at the top and bulk links below them. For each link, you see the recipient's e-mail (individual links only), the name, the limit that was set, how many times the link has been used, the status, and the full link address. The status has four values: **Unused**, **Partially used**, **Exhausted**, and **Used**. *Exhausted* means a bulk link that has reached its limit; *Used* means an individual link that someone has already registered through.

The export is useful for reporting to partners (how many of their free invitations have been used) and for sending the links out through your own channels. It shows counts only, though: it contains neither the names of the people who came through a bulk link nor the group the link assigns them to.

### Ticket groups

Ticket groups let you create a set of tickets visible only for a specific kind of purchase. You create a group, add selected tickets to it, and share the group through a **unique link**. Through that link, the attendee sees only the tickets in the group, and only those with the **Published** or **Private** status. You can add an **Unpublished** ticket to a group, but the group link does not offer it. For tickets that should sell only through a group, choose the **Private** status.

Use cases: partner pricing, special offers, VIP bundles with a custom set of tickets.

### Bulk import (Import)

On the **Import** tab, you bulk-upload data through an Excel template. Import is available for **E-mail links** (individual registration links), **Bulk links**, and **Discount codes**. For each type, you download the template (**Download template**), fill it in, upload it (**Upload completed template**), and run **Import**. After importing, you see a **Created / Skipped / Errors** summary with a per-row description of any errors.

The templates reference groups by name. If a row points to a group that does not exist in the workspace, that row is not imported and fails. Create the groups before you import.

### Ticket statistics

The last tab on the **Tickets** page is called **Statistics** (the **Statistics** button in the top right takes you to the same tab). It holds two tables: **Ticket statistics** and, below it, **Monthly overview**.

The **Ticket statistics** table has one row per ticket plus a **Total** summary row. Amount columns are labeled with the event currency (*CZK*, for example), and every amount is shown **including VAT**, with the same amount **excluding VAT** in parentheses underneath:

- **Sold** (Quantity / Amount) — every ticket sold, whether or not it has been paid for.
- **Paid** (Quantity / Amount) — orders with the payment received.
- **Unpaid** (Quantity / Amount) — issued but not yet settled. Typically proforma invoices waiting for a bank transfer.
- **Free** (Quantity) — tickets acquired at zero price, typically through individual and bulk registration links.
- **Cancelled** (Quantity) — canceled orders.
- **Registered** (Quantity / Amount) — how many buyers have already completed registration. This only means something for *Registration with additional information*; the gap against **Sold** tells you how many people have paid but not yet been through the form.

**Monthly overview** breaks the same numbers down by month, with two differences: **Cancelled** gains a **Refunded** figure (how much money actually went back to buyers), and **Registered** shows **Quantity** only. This is the fastest view of when sales happened — useful for evaluating sales waves and the effect of individual campaigns.

Export the data with the **Exports** button in the top right — to Excel by orders or by tickets. The third item in the same menu, **Registration links export**, downloads an overview of your free registration links; the *Individual and bulk registration links* part of this article describes it.

## Common pitfalls

### Tickets are turned on, but no ticket has been created. Registration is closed and attendees complain

Right after you turn on Tickets, create at least one. Until you do, registration does not work.

### Automatic registration is chosen for a paid event, even though you need additional data or extended consents

Automatic registration after ticket purchase **does not use** the Registration form or extended consents on a paid event. Choose *Registration with additional information* instead. See *Choosing the right registration type* for details.

### Proforma invoice due date is set to 14 days, but the event is in 10 days. The attendee receives an invoice with a due date past the event

The system automatically shortens the due date so that it falls at the latest two days before the event starts. Check in the settings what the due date will actually be set to for events that are close.

### A ticket in the *Private* state — the organizer does not see it in the purchase view and thinks it is broken

A private ticket is intentionally hidden from the purchase overview. You get its direct link from the link icon in its row in the ticket list; through that link — or by adding it to a ticket group — the ticket can be purchased.

### An unpublished ticket in a ticket group. The partner opens the group link and does not see the ticket

The group link offers only tickets with the **Published** or **Private** status. The **Unpublished** status hides a ticket everywhere, even when it is in a group. Change the status to **Private**: the ticket stays hidden from the regular ticket overview and becomes available for purchase through the group link.

### You want to keep selling tickets after the event, but they have disappeared from the offer

The common sales deadline applies to all events, including those created earlier, and the default option is **At the end of the event**. If sales should continue after the event, choose **Custom date and time** with a later deadline under **End of ticket sales**. Also check that an earlier **Sale end** on the ticket itself does not end sales.

### *Unlimited* on a past event. Tickets for a past edition can still be bought

**Unlimited** turns off the common sales deadline, and a ticket without its own **Sale end** stays in the offer even after the event ends. A buyer looking for the current edition can then buy a ticket for the past one by mistake. Use **Unlimited** only when every ticket has **Limit sales period** turned on with a **Sale end** filled in; otherwise keep **At the end of the event**.

### A 100% discount code is used instead of an individual registration link. The attendee has to go through the entire purchase process to get a free ticket

For a one-off free invitation, use an **Individual registration link** — the attendee goes through registration without the purchase flow. A 100% discount code makes sense for marketing campaigns where you want to track how many people redeemed the code.

### A ticket bundle (step of 5) is set up, but the organizer expects the attendee to be able to buy a different quantity. The customer is puzzled why they cannot buy 3 tickets

A bundle setting enforces **multiples** — a step of 5 allows only 5, 10, 15, and so on. If you want a more flexible offer, create two tickets: a base *Standard* (without a bundle) and *Standard — bundle of 5* (with a bundle and a discount).

### *Assign to group* turned on mid-sale, so earlier buyers are missing from the group and targeted communication skips them

Group assignment on a ticket **does not apply retroactively**. If you turn the option on when you have already sold 50 tickets, only the people who register afterwards get the group. The 50 earlier attendees stay outside it, and if you use that group to target a campaign, content visibility, or what is shown during scanning, those people drop out of the targeting.

Watch out, because group assignment on sessions works the other way around — there, turning it on or off also applies to attendees who are already registered. Experience from one part of the product does not carry over here.

When it happens, add the membership by hand: either one by one in the **Edit contact** side panel on the *Groups* tab, or for larger numbers, import the same contacts again with the **Add groups to all** option, which adds the groups to existing contacts and overwrites nothing. Both are described in [Managing contacts and groups in your workspace](https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace). The more reliable path is to set the group and its assignment up **before sales open**.

### Bulk import fails because the group does not exist in the workspace yet

Import templates (E-mail links, Bulk links, Discount codes) reference groups by name. If a group does not exist, the row is not imported and fails (for example, *Unknown group: VIP*). Create the groups before importing and match the names in the template.

### Trying to offer an add-on with a ticket — a T-shirt, lunch, a workshop — as another item in the cart

The purchase flow is not modular; the attendee does not assemble an order out of several items. Every additional item is a separate ticket, and because an attendee's e-mail address can be used only once in an order, a second item for the same person will not go through.

The way around it is a separate ticket for every combination: *Conference entry*, *Conference entry + workshop*, *Conference entry + T-shirt*. The attendee picks one and everything is included in the price. You get the distinction — for yourself and for check-in on site — through **Assign to group** on each variant.

Do not confuse this with the **Purchase in a bundle** toggle. That one governs a minimum order in multiples (5, 10, 15 of the same ticket), not what a ticket contains.

### Both the buyer and the attendee get the link to complete registration, and both fill it in

When a company buys several tickets, the buyer receives the registration links for all the attendees, and every attendee receives their own at the same time. Either of them can therefore complete the registration. Whoever clicks the link second sees that the attendee is already registered. If it matters to you who fills the details in, say so in the accompanying communication — the system does not govern it.

## Related articles

- [Choosing the right registration type](https://help.happenee.com/en/articles/4-choosing-the-right-registration-type)
- [Setting the registration type and additional questions](https://help.happenee.com/en/articles/12-setting-the-registration-type-and-additional-questions)
- [Managing Orders and invoices](https://help.happenee.com/en/articles/19-managing-orders-and-invoices)
- [Setting up the Registration form](https://help.happenee.com/en/articles/13-setting-up-the-registration-form)
- [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility)
- [Managing contacts and groups in your workspace](https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace)
- [How nominations and nominators work](https://help.happenee.com/en/articles/17-how-nominations-and-nominators-work)
- [Setting up Seating](https://help.happenee.com/en/articles/20-setting-up-seating)
- [Personal link vs. public link: what is the difference](https://help.happenee.com/en/articles/44-personal-link-vs-public-link-what-is-the-difference)
- [Working with Orders and exports](https://help.happenee.com/en/articles/52-working-with-orders-and-exports)
- [How check-in and QR-code scanning work](https://help.happenee.com/en/articles/47-how-check-in-and-qr-code-scanning-work)
- [Recommended setup for a conference](https://help.happenee.com/en/articles/55-recommended-setup-for-a-conference)
- [Recommended setup for an expo or trade show](https://help.happenee.com/en/articles/56-recommended-setup-for-an-expo-or-trade-show)
- [What to do when an attendee loses the registration link](https://help.happenee.com/en/articles/59-what-to-do-when-an-attendee-loses-the-registration-link)
- [Fixing an invoice error](https://help.happenee.com/en/articles/60-fixing-an-invoice-error)
- [Interpreting ticket statistics](https://help.happenee.com/en/articles/84-interpreting-ticket-statistics)
- [How to tell the wrong registration type was chosen](https://help.happenee.com/en/articles/92-how-to-tell-the-wrong-registration-type-was-chosen)

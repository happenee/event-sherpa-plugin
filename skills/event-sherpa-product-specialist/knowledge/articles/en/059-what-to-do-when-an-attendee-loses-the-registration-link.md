# What to do when an attendee loses the registration link

> What to do when, in a paid event, the buyer has paid but the attendee has lost the link to finish registration.

- Article in the Help Center: https://help.happenee.com/en/articles/59-what-to-do-when-an-attendee-loses-the-registration-link
- Česká verze: https://help.happenee.com/cs/articles/59-co-delat-kdyz-ucastnik-ztrati-registracni-odkaz
- Collection: Troubleshooting
- Updated: 2026-09-18

---

> [!info] Overview
> This is the typical case for *Registration with additional information*: the buyer pays, the attendee receives an e-mail with a link to fill in their details, and the attendee deletes or loses that e-mail. The registration stays unfinished and the PDF ticket with the QR code is not generated.

## Getting started

Open **Orders** — from the *Tools* dropdown at the bottom of the left menu, from the tile on the event **Overview**, or with the button in the top right of the *Tickets* page. Find the order by the buyer's name, e-mail, or company. The faster route is the **Unregistered** chip, which narrows the list to orders where registration never finished.

## Details

### Individually — from the order detail

1. In **Orders** expand the specific order with the arrow at the end of its row.
2. If the wrong e-mail was entered for the ticket, fix it with the pencil icon in the **Tickets** table.
3. For a ticket without a finished registration, use the **Notify** button. The attendee receives a new e-mail with the link to finish registration. After the send, the ticket shows the **Sent** status with the date and time, and the button changes to **Send again**; for five minutes after any link send it stays disabled, so no duplicate e-mail goes out.

### In bulk — to every attendee with an incomplete registration at once

Above the order list on the right there is a **Notify by e-mail** dropdown; its **Unregistered** item resends the registration link to attendees of paid and free orders who have not finished registration. It follows the current selection in the list: with a search or a filter it reaches only that selection, without them everyone in the event. The links leave a queue gradually, not the moment you click, and an attendee who received the link within the last five minutes does not get it again. It is useful when:

- a few days before the event you spot a gap between *sold* and *registered*,
- after a bulk ticket purchase (a company buys 50 tickets and the employees register one by one).

Automatic reminders to attendees with an incomplete registration are not part of self-service today — bulk resend is a manual step worth scheduling.

### Prevention

- On event day (ideally an hour before start), send an **E-mail campaign** with a reminder and the QR ticket — the attendee then has the ticket in the most recent e-mail, no matter what they did with the previous one.
- For *Registration with additional information*, set a clear message to the buyer that registration is not yet complete — both on the post-purchase screen and in the confirmation e-mail.

## Common pitfalls

### The organizer looks for the full attendee record inside the order

In the order you fix the data on a specific ticket — typically the typo in the e-mail address that kept the link from arriving. Registration form answers, groups, and attendance status are managed in the **Registration** section: the order is about the purchase, the registration about the attendee.

### The buyer purchased 10 tickets and is supposed to forward the link to all 10 employees — the organizer expects the system to do it

If the buyer **did not enter the attendee e-mails**, the links go to the buyer and the buyer forwards them. A bulk *Notify by e-mail* in this case only re-reaches the buyer, not the end attendees.

## Related articles

- [Managing Orders and invoices](https://help.happenee.com/en/articles/19-managing-orders-and-invoices)
- [Setting up Tickets](https://help.happenee.com/en/articles/18-setting-up-tickets)
- [Creating and sending an E-mail campaign](https://help.happenee.com/en/articles/41-creating-and-sending-an-e-mail-campaign)

# What to do when an e-mail does not arrive

> What to do when an attendee reports a missing Invitation, Confirmation e-mail, or E-mail campaign.

- Article in the Help Center: https://help.happenee.com/en/articles/58-what-to-do-when-an-e-mail-does-not-arrive
- Česká verze: https://help.happenee.com/cs/articles/58-co-delat-kdyz-neprisel-e-mail
- Collection: Troubleshooting
- Updated: 2026-09-21

---

> [!info] Overview
> An attendee reports that they did not receive an Invitation e-mail, a Confirmation e-mail, or an E-mail campaign. In most cases this is not a system outage — the e-mail either reached a wrong address, landed in spam, or was never sent at all (a missing language version, an unassigned contact, the wrong attendee status).

## Getting started

Open **Check-in** or **Registration** and find the attendee. Check their e-mail address, RSVP status, and preferred language — that narrows the cause.

## Details

### Typical causes

- **Wrong e-mail on the attendee** — a typo, an outdated company address.
- **Spam or the Promotions / Updates tab** — e-mails are sent from the domain `invitation.happenee.com`; the attendee may not recognize it.
- **The campaign did not go out because a language version is missing** — if the *Campaign is not ready to send* dialog appeared when you sent it, no mailing was created and you will not find one on the **Mailings** tab. The dialog lists the languages that are missing a subject or content.
- **The Invitation e-mail has not been sent yet** — the Invitation e-mail is not automatic; it has to be sent manually (individually or in bulk).
- **The attendee is not assigned to the event** — Invitation e-mails and campaigns only go to assigned contacts.
- **The attendee's status is *Not attending* or unsubscribed** — the Confirmation e-mail is not sent.
- **For events with Tickets** — the buyer paid, but the attendee has not yet completed the Registration form; the ticket with the QR code is generated only after registration is complete.

### How to fix it

- **Confirmation e-mail after a correction** — in **Check-in** find the attendee, fix the e-mail address, switch the status to *Attending*, and resend the Confirmation e-mail (the checkbox shown when the status changes).
- **Incomplete registration on a paid ticket** — in **Orders** expand the specific order and use **Notify** on the ticket. In bulk: **Notify by e-mail → Unregistered** above the order list on the right. A link that went out within the last five minutes is not sent again.
- **Campaign** — on a sent campaign, open the **Mailings** tab, use the **Resend campaign to newly assigned** panel and the **Newly assigned** button to reach attendees who were not yet assigned to the event or the group when the mailing started.
- **Checking a specific address** — on the **Mailings** tab, open **E-mails** for that mailing. For every recipient you see whether the e-mail was sent, delivered, and opened. *Not delivered* in the **Mailing status** chart means a delivery problem (a typo in the address, a full or closed mailbox, a block on the recipient's side) — resending will not fix that, correct the address first.
- **Campaign stopped by a missing language** — switch **Content language** to the languages the dialog listed, fill in the subject and content, and send the campaign again.

### Prevention

- Always fill in e-mail and campaign content **in every active language**, even when you assume all your attendees read the same one.
- For paid events, in **Orders** check the gap between purchased tickets and completed registrations — the gap is the attendees with an incomplete registration who only need the link resent.
- Before any bulk send, always use the **Test campaign** or **Test invitation e-mail** action and send to your own address.
- Name-based check-in in the attendee app does not exist today — on event day it is practical to send a *reminder with the QR code* an hour before start, so attendees have the ticket at hand even without app access.

## Common pitfalls

### An attendee says *I got nothing*, the organizer resends — a duplicate arrives, but the original was meanwhile found in spam

First ask the attendee about the *Promotions / Updates / Spam* folder and the `invitation.happenee.com` domain. Only then resend.

### For events with Tickets, the organizer expects that the attendee gets the ticket automatically after payment. The payment went through, but the ticket did not arrive

With *Registration with additional information*, the ticket is generated only after the Registration form is completed. Check the status in **Orders** and resend the link if needed.

## Related articles

- [How the Invitation e-mail works](https://help.happenee.com/en/articles/39-how-the-invitation-e-mail-works)
- [How the Confirmation e-mail works](https://help.happenee.com/en/articles/40-how-the-confirmation-e-mail-works)
- [Creating and sending an E-mail campaign](https://help.happenee.com/en/articles/41-creating-and-sending-an-e-mail-campaign)
- [Managing Orders and invoices](https://help.happenee.com/en/articles/19-managing-orders-and-invoices)
- [Tracking e-mail and campaign deliverability](https://help.happenee.com/en/articles/80-tracking-e-mail-and-campaign-deliverability)

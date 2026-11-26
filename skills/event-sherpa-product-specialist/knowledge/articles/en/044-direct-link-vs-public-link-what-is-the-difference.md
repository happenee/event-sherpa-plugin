# Personal link vs. public link: what is the difference

> Where the registration button in an e-mail should lead: a personal recipient link, a public link, or individual free admission at a paid event.

- Article in the Help Center: https://help.happenee.com/en/articles/44-personal-link-vs-public-link-what-is-the-difference
- Česká verze: https://help.happenee.com/cs/articles/44-osobni-a-verejny-odkaz-jaky-je-rozdil
- Collection: Communication and invitations
- Updated: 2026-09-16

---

> [!info] Overview
> For the registration button in the Invitation e-mail and in an E-mail campaign, the section **Where should the registration button lead?** decides where you send the recipient. You always get **Personal recipient link** (an invitation tied to one specific contact) and **Public link** (shareable, everyone enters their own e-mail). A paid event adds a third option, **Individual free admission** — the recipient registers without buying a ticket. The choice decides whether the invitation becomes a private guest list or a channel for spreading the word.

## Getting started

- Decide whether the invitation should be **personal** (valid for the recipient) or **shareable** (anyone with the link can register).
- At a paid event, also decide whether the recipient should **pay**. A personal link sends them to ticket purchase. If admission should be free, you need **Individual free admission**.
- With a public link, expect people to forward it. If you do not want that, choose the personal link.

## Details

The setting sits in the e-mail content under **Where should the registration button lead?**. **The options depend on the event type:** a free event offers two, a paid event three. *Individual free admission* does not appear at a free event — there is no purchase to bypass.

### Personal recipient link

The link is unique to the recipient of the e-mail — it carries the identification of one specific contact. **It behaves differently depending on whether the event has tickets enabled.**

**At a free event**, the registration e-mail is fixed and cannot be changed. The recipient can **confirm or decline** attendance. If they forward the link, the other person does not get registered under their own name — the registration belongs to the original recipient.

**At a paid event**, the personal link mainly serves to **personalize the microsite**. The recipient continues to **ticket selection and purchase**, and during checkout they **can enter a different e-mail** than the one the invitation was sent to. So at a paid event, a personal link is **not a way to let someone in for free**, and it does not lock registration down as tightly as at a free event.

When to use it:

- A personal invitation to a VIP or a specific partner.
- An internal company event **without tickets**, where you do not want registrations from outside the invited list.
- An invitation-only event **without tickets**, where you have a closed list.
- A paid event where the microsite should be personalized and the guest buys their own ticket. If you need certainty about who registers, add the *Registration only for assigned contacts* restriction.

### Public link

A public link does not lead to a pre-filled registration. It leads to the microsite, where the visitor **first enters an e-mail** and only then continues — at a free event to the registration form, at a paid event to ticket selection and payment, if required. **Any e-mail address** can be entered.

Behavior:

- The link can be copied and **sent to anyone**. A new recipient registers under their own e-mail.
- You can post it on social media, on your website, or in an internal newsletter.
- It suits public events and campaigns meant to drive as many registrations as possible.

When to use it:

- A public event where you want to admit as many people as possible.
- An invitation attendees are meant to pass along ("bring a colleague").
- When you do not yet know who will come and want to keep it open.

### Every link is built on the microsite address

The personal link, the public link, and individual free admission all lead to the microsite address `https://www.happenee.com/events/<slug>` and differ only in what Happenee appends after it. When you change the slug under **Event microsite → Settings**, **all three link types** in e-mails already sent stop working, not just the public link shared on the website. There is no redirect from the old address. Change the address before the first send; the details are in [How the Event microsite works](https://help.happenee.com/en/articles/21-how-the-event-microsite-works).

### Individual free admission (paid events only)

The third option appears only at an event with **Tickets** enabled. The recipient gets an **individual registration link without having to buy a ticket** — exactly the "let this list of people in for free" scenario.

This is the right choice for a **guest list at a paid event**. A personal link is not a substitute: it sends the recipient to checkout.

### Guest lists at paid events

A common request from organizers of paid events: *"I want to let 50 contacts in for free without paying."*

How to do it:

1. Import the 50 contacts into contact management (with a preferred language).
2. Assign them to the event.
3. Create an E-mail campaign (or use the Invitation e-mail) and set the registration button to **Individual free admission**.
4. Send the campaign to exactly those 50 contacts.
5. Through the link, the recipients reach registration **without buying a ticket**.

Compared to a 100% discount code: with a discount code the attendee still goes through the **purchase process**, even though the total is zero. Individual free admission skips checkout entirely, which is cleaner for the guest.

### Individual and bulk registration links

The **Tickets** module offers the same principle, with registration links managed separately:

- **Individual link** — single-use, for one person, bypasses ticket purchase.
- **Bulk link** — one link with a maximum number of uses (for example 20). Useful to hand to a partner: they share it among their guests and the system enforces the limit.

Both types can **add people to a group after registration** (for example "Partner XY"), so you can keep addressing them by segment. Details in *Setting up Tickets*.

What differs is distribution: **Individual free admission** generates links for the recipients of a campaign or the Invitation e-mail, whereas links from the Tickets module are distributed by you, and a bulk link additionally supports shared use with a limit.

### Combining with an E-mail campaign

An E-mail campaign is a "container" for delivering the link:

- A campaign with a **personal link** → an invitation targeted at specific contacts or groups.
- A campaign with a **public link** → shared information, even when you target a single group (they can forward it).
- A campaign with **individual free admission** → a guest list at a paid event.

Typical use: a campaign for VIPs with a personal link, a reminder to registered attendees with a public link (let them pass it to a colleague).

### Decision rule

- **Invitation-only, closed list (free event)** — Personal recipient link
- **Free guest list at a paid event** — Individual free admission
- **Partner link with a usage limit** — Bulk registration link (in Tickets)
- **Public invitation for social media** — Public link
- **Reminder to registered attendees, occasional forwarding** — Public link
- **Personalized microsite at a paid event (the guest buys a ticket)** — Personal recipient link

## Common pitfalls

### The organizer sends an invitation to a paid event with a **personal link** and expects the guest to get in for free

At a paid event, a personal link leads to **ticket selection and purchase** — it personalizes the microsite but does not bypass payment. For free admission, choose **Individual free admission**, or use an individual or bulk registration link from the Tickets module.

### The organizer sends an invitation to a paid event with a **100% discount code** and wonders why the guest still has to go through checkout

A discount code lowers the price, but the purchase process remains. For a free guest list, use **Individual free admission** in the e-mail, or registration links in the Tickets module.

### The organizer puts a **public link** in the Invitation e-mail and then wonders why people outside the invited list are registering (someone forwarded it)

For a closed list, use **Personal recipient link**. If it has to be a public link, turn on the *Registration only for assigned contacts* restriction in Event settings.

### The organizer assumes that at a paid event a personal link locks registration to the recipient

At a free event the registration e-mail genuinely cannot be changed. At a **paid** event, however, the recipient can enter a **different e-mail** during checkout, so the registration may not end up with the person the invitation was sent to. If you need certainty about who registers, add the *Registration only for assigned contacts* restriction.

### The organizer shares a **personal link** on social media and wonders why only one person registers

A personal link belongs to one specific recipient. For public sharing, use **Public link**, or the public microsite link from the Event microsite module.

### The organizer hands out **bulk links** to several partners and later has no idea how many people came through each one

A bulk link in the Tickets module always has a limit: you set the **Number of uses** from 1 to 500. Once the limit is reached, the link shows a message that it has already been used, instead of the registration form. To see how much of the limit each partner has used, go to the **Tickets** page and open **Exports → Registration links export**. For each link, the file shows the limit, the number of uses, and the status, such as **Exhausted**. The names of the people who registered are not in the export; if you need to trace them, set the link to assign a group (for example "Partner XY") before you send it out, and search by that group. The assignment is not added retroactively for people who registered earlier.

### The organizer assumes that people who came through a public link received the Invitation e-mail

A registration from a public link shows up in statistics as an arrival through an open link — the system sent those people no invitation. To reach them afterwards, use an E-mail campaign targeted at the *Registered* status or at the group they landed in.

### The organizer changes the microsite address after the invitations are sent, and every link in the e-mails stops working

The personal link, the public link, and individual free admission all carry the microsite slug, so changing the address under *Event microsite → Settings* invalidates them all at once, and the old address does not redirect. Either set the slug back to its original form, or send the campaign or the Invitation e-mail again.

## Related articles

- [Creating and sending an E-mail campaign](https://help.happenee.com/en/articles/41-creating-and-sending-an-e-mail-campaign)
- [How the Invitation e-mail works](https://help.happenee.com/en/articles/39-how-the-invitation-e-mail-works)
- [Choosing the right registration type](https://help.happenee.com/en/articles/4-choosing-the-right-registration-type)
- [Setting up Tickets](https://help.happenee.com/en/articles/18-setting-up-tickets)
- [How the Event microsite works](https://help.happenee.com/en/articles/21-how-the-event-microsite-works)

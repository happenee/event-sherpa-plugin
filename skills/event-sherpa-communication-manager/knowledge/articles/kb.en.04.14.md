<!-- source: kb.en.04.14 -->

---
title: "Tracking e-mail and campaign deliverability"
description: "How to read the Mailing status chart, what Not delivered means and how it differs from unread, and where to find delivery and opens for an individual recipient."
modules: ["komunikace_a_pozvanky"]
last_updated: "2026-09-21"
version: 3
---

> [!info] Overview
> Once a campaign has gone out, the **Mailings** tab tells you how it did — the **Mailing status** ring chart breaks the e-mails down into delivered, read, and not delivered, and the table below lists the individual mailings. Through the **E-mails** link you can drill all the way down to a single recipient and see whether the message arrived, whether they opened it, and whether they clicked. This is the first place to look when somebody claims they received nothing.

## Getting started

Open the campaign and switch to the **Mailings** tab. The number in the badge next to the tab name tells you how many mailings the campaign has had so far — resending to newly assigned contacts creates another mailing, so there can be more than one.

Work from the top down: the chart for the overall picture, then the table of mailings, and only then the detail of a specific recipient.

## Details

### The Mailing status chart

The ring chart splits the e-mails into five categories:

- **To be sent** — The message is queued and has not gone out yet.
- **Sending** — The mailing is in progress.
- **Delivered and unread** — The e-mail reached the mailbox; the recipient has not opened it yet.
- **Delivered and read** — The e-mail arrived and was opened.
- **Not delivered** — The message never reached the mailbox — a non-existent address, a full mailbox, or a rejection by the recipient's server.

The distinction between **Not delivered** and **Delivered and unread** is the important one. *Not delivered* is a technical problem with the address and you fix it by fixing the contact. *Delivered and unread* means the e-mail arrived just fine and the recipient simply has not opened it — there is nothing technical to fix, only a reminder to send.

### The table of mailings

Below the chart is a list of the campaign's individual mailings, newest first. For each one you see the **date and time**, the **number of e-mails**, and the **delivery status** (*Sending in progress* → *Sent*). The **Show test mailings** toggle adds the tests you sent to your own address — by default they are not counted.

A mailing in progress can be deleted with the trash icon. A completed mailing no longer has one — you cannot take sent e-mails back.

### Recipient detail

The **E-mails** link on a mailing (or the button in the campaign header) opens the list of all recipients with the columns **Mailgun**, **Sent**, **Delivered**, **Opened**, and **Clicked**. You can search the list by e-mail address.

Every row expands to show **a preview of the exact e-mail as the recipient received it** — including the header image, the registration button, and the fallback text link in case the button does not work. That is the fastest way to verify what actually went out to whom when somebody complains about the content or a broken link.

### Resending to newly assigned contacts

The **Resend campaign to newly assigned** block shows how many contacts joined the event or the group after the mailing started — whether the organizer assigned them or they arrived through registration or a ticket purchase. The **Newly assigned** button sends the campaign to them.

A resend **creates a new mailing** rather than continuing the original one. Another row appears in the table and the badge on the tab goes up. When you track the numbers, expect one campaign to have several mailings with different recipient counts.

### The Invitation e-mail

The Invitation e-mail has no deliverability ring chart of its own. You read how people responded through **attendee statuses** — who did not respond, who registered, who declined. Status reporting is covered in the article on attendee statistics; for tracking technical deliverability, a campaign is the better tool.

## Common pitfalls

### Confusing not delivered with unread

The most common mistake when reading the chart. When an organizer reports that "half the e-mails never arrived", they are usually looking at *Delivered and unread*. Those e-mails arrived. The real problem is only the **Not delivered** segment — and you fix it by checking addresses, not by sending again.

### Treating a high Not delivered count as a Happenee fault

A high count of undelivered messages usually means bad data: typos from manually retyped addresses, stale contacts after employees left, company addresses closed in a reorganization. Go through the specific addresses in the recipient detail — the pattern is usually obvious at a glance, and what needs fixing is the contacts, not the campaign.

### Reading the numbers immediately after sending

Both delivery and opens lag. A few minutes after a send you will see most e-mails in *To be sent* or *Sending* and almost no opens. A sensible reading comes hours later — for a morning send, no earlier than the afternoon.

### Letting tests count toward the statistics

Test mailings are hidden by default precisely so they do not distort the numbers. If you turn the **Show test mailings** toggle on and forget about it, your recipient counts will be off by your own tests.

<!-- source: kb.en.06.04 -->

---
title: "Interpreting ticket statistics"
description: "How to read Ticket statistics — sold, paid, unpaid, free, and canceled tickets, the monthly overview, how they relate to registrations, and what the export gives you."
modules: ["vstupenky_a_objednavky", "reporting_a_statistiky"]
last_updated: "2026-09-17"
version: 3
---

> [!info] Overview
> **Ticket statistics** show sales per ticket type — how many were sold, how many are paid, unpaid, free, and canceled, and how many of those people have completed their registration. Alongside that there is a monthly overview, so you can see how sales built up over time. It is a separate view from attendee statistics: those count people and their statuses, these count tickets and money.

## Getting started

You find ticket statistics with the event's statistics and reporting; they are only worth opening when you have Tickets enabled.

Before you look at the numbers, be clear about the question you are asking:

- **How much did we sell?** → counts per ticket type.
- **How much of it is in the bank?** → the gap between paid and unpaid.
- **How many people will actually turn up?** → the registered count, not the sold count.
- **How did sales develop?** → the monthly overview.

## Details

### The individual categories

For each ticket type you see a breakdown:

- **Sold** — The total number of tickets issued for that type.
- **Paid** — Tickets with a completed payment.
- **Unpaid** — The order exists, the money has not arrived — typically a proforma invoice past its due date.
- **Free** — Tickets issued without payment, for example through a 100% discount code or a registration link.
- **Canceled** — Canceled orders. They do not count toward sales but stay on the record.
- **Registered** — How many of these tickets have a completed attendee registration.

Amounts appear in the currency the ticket was sold in — Czech crowns or euros, depending on the ticket setup.

### Sold versus registered

The most important pair of numbers on the screen. With **registration with additional information**, the order comes before the registration: somebody buys tickets for five colleagues, and those colleagues still have to register. Until they do, they have a ticket but no QR code and no form answers.

So read the gap between sold and registered as **a queue of work, not an error**. The closer to the event, the more urgent it gets — people who have not registered have to be handled by hand at check-in. You find the specific buyers with incomplete registrations in the orders section, and you can notify them by e-mail in bulk.

### Unpaid tickets

A high unpaid count usually does not mean people are refusing to pay; it means proforma invoices are still within their due period. Look at the issue dates: if they are recent, this is normal. If they are overdue and the event is approaching, it is time for a reminder (in **Orders**, **Notify by e-mail → Unpaid** sends the buyers an e-mail with the proforma invoice attached), or for a decision about releasing the seats.

### The monthly overview

This shows how sales built up over time. Use it comparatively — against last year's edition or against the curve you expected. The typical pattern for conferences is two waves: one after sales open and one in the final fortnight. If the second wave does not arrive, that is your signal for a last reminder campaign.

### Getting the numbers out

There are two export routes to Excel: **by order** and **by ticket**. The first suits accounting (one order = one document), the second suits operations (one ticket = one person at the door).

There is **no public or shareable link** to the statistics — nobody without admin access can see them. When management needs the numbers, send an export or write a summary from it.

## Common pitfalls

### Treating tickets sold as the number of attendees

A sold ticket does not mean a registered person. With registration with additional information, one buyer can hold five tickets where nobody has yet said who is coming. Use the sold count for room capacity and the registered count for badges and check-in.

### Counting canceled tickets as sales

A cancellation stays on the record so the history remains traceable, but it does not belong in real sales. When you put together the event result, check whether the number you started from includes cancellations — and whether it accounts for refunds.

### Confusing these with attendee statistics

They are two different views of the same event. Ticket statistics count units and money; attendee statistics count people and their statuses (invited, registered, checked in). On a paid event you need both, and they will never match one to one.

### Promising management a link to live numbers

There is no link to the statistics that works without admin access. Agree on a regular export instead — weekly, say — rather than promising something you will later have to explain.

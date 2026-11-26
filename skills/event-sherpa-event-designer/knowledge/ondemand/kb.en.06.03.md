<!-- source: kb.en.06.03 -->

---
title: "Working with Orders and exports"
description: "A switchboard of the eleven event exports and when to download which one (accounting, GDPR, catering, CRM)."
modules: ["reporting_a_statistiky"]
last_updated: "2026-10-26"
version: 8
---

> [!info] Overview
> Happenee lets you download data from an event in **eleven different exports**, each one built for a different job — accounting, GDPR audit, scanning analysis, catering rosters, CRM onboarding. Most exports are Excel; some are also CSV. You will find them in the **Statistics** section and in the detail pages of individual modules (Orders, Tickets, Registration form, Attendee app). Articles about each module describe what their export contains; this article serves as a **switchboard**: which export to download when.

## Getting started

Decide **what you need the data for**:

- **Accounting and invoicing** — Orders, Orders by ticket, Export invoice PDFs, Ticket statistics. You are most likely working with someone used to Excel.
- **Partners and free invitations** — the Registration links export: how many times each link has been used and which bulk links have reached their limit.
- **Hotel, catering, organizing team** — attendees export (filtered by group, accommodation). One export usually does the job.
- **One overview with selected details from several sources** — **Attendee reports** in the **Exports** section of **Statistics and reporting**: columns from groups, the form, the Agenda, engagement, and tickets in one XLSX file, with each attendee on one row. See [Building an attendee report](06_building-an-attendee-report.md).
- **GDPR audit or a request about a specific person** — the **GDPR consents beyond the legal minimum** export.
- **Check-in evaluation** — the scanning export.
- **Form responses for analysis** — the Registration form export (Excel or CSV for scripted processing).
- **App evaluation** — the user activity export and the list of users who have the app.

## Details

### 1. All attendees (Excel)

A single file with every contact assigned to the event. It contains contact fields, attendee status, groups, preferred language, and the ticket (if the event is paid).

**Typical uses:**
- Source data for catering, the hotel, or the organizing team.
- Building badges if you do not print directly from Happenee.
- A quick check of who is in which group.

For preparing data for the hotel, Happenee offers a limited export — see [Preparing data for accommodation providers](../05_event-day-and-on-site/03_preparing-data-for-accommodation-providers.md).

### 2. GDPR consents beyond the legal minimum

A separate export for the consents the organizer added on top of the baseline GDPR (marketing consent, photo consent, consent to share data with a partner, and so on). It lists **all attendees of the event** — including those who granted no extra consent — so a single file documents who agreed to what, and who did not.

You download it in the **Registration form** section on the **Exports** tab (labeled **GDPR consents beyond the legal minimum**, next to the **Results (Excel)** export of form responses — see [Setting up the Registration form](../02_event-setup-and-registration/05_setting-up-the-registration-form.md)), or in the **Statistics** section.

**Typical uses:**
- Audit — proving who agreed to what and when (and who did not).
- Source data when an attendee requests deletion or a data overview.

### 3. Scanning export (check-in)

One row per QR code scan in the Service app or in **Check-in**.

**Typical uses:**
- Evaluating arrival timing (how many people came at which hour).
- Checking whether anyone passed through more than once (duplicate scans).
- Linking a check-in to a specific scanning action (*Check-in*, *One-time check* for a voucher, and so on).

For an explanation of place types, see [How check-in and QR-code scanning work](../05_event-day-and-on-site/01_how-check-in-and-qr-code-scanning-work.md).

### 4. Orders (Excel)

A complete list of every order on a paid event — who, how much, what payment method, whether it is paid.

**Typical uses:**
- Source data for accounting (an alternative to individual invoices).
- Checking which orders are still waiting for payment.

The detail of a single order is described in [Managing Orders and invoices](../02_event-setup-and-registration/11_managing-orders-and-invoices.md). The export is the bulk view.

### 5. Orders by ticket (Excel)

The same data broken down **per ticket** — one row per piece rather than per order. A corporate purchase of 50 tickets is 50 rows here, each showing who the ticket was assigned to.

**Typical uses:**
- Matching tickets to specific attendees (who from the company is actually coming).
- Checking which pieces of a bulk purchase still have no completed registration.

### 6. Export invoice PDFs

Every invoice for the event at once. It replaces downloading documents one by one from the order details.

**Typical uses:**
- Handing complete invoicing to your accountant in a single bundle.
- Archiving the documents after the event closes.

### 7. Ticket statistics

Aggregate numbers — sold, paid, unpaid, free, canceled, broken down by month and by ticket type.

**Typical uses:**
- Financial reporting for the event (how much was collected, how much is still pending).
- Evaluating sales waves (when each ticket type sold).

The detailed explanation of ticket statistics is in [Setting up Tickets](../02_event-setup-and-registration/10_setting-up-tickets.md).

### 8. Registration links export

An overview of every individual and bulk registration link for the event, one row per link. You download it on the **Tickets** page under the **Exports** button in the top right. The *Exports* menu on the Orders page does not have this item. For each link, you see the type, the recipient's e-mail (individual links only), the name, the limit that was set, how many times the link has been used, the status, and the full link address. The status is **Unused**, **Partially used**, **Exhausted**, or **Used**.

**Typical uses:**
- Reporting to a partner — how many of their free invitations have been used.
- Checking which bulk links have run out and need a higher limit.
- Sending the links out through your own channels, without copying addresses from the admin one at a time.

The export shows counts only. It does not say who exactly registered through a bulk link, and it does not include the group the link assigns registrants to. How to create the links is described in [Setting up Tickets](../02_event-setup-and-registration/10_setting-up-tickets.md).

### 9. Registration form responses (Excel / CSV)

One row per registered attendee, with every answer from the form. It includes contact details and additional questions.

**Two variants:**
- **Excel** — for people who will work with the data by hand (filtering, pivot tables).
- **CSV** — for import into another system (CRM, analytics, data pipeline).

In addition, you can **edit responses** directly in the attendee detail in the UI (for example, when someone made a typo in their address).

### 10. Attendee app — user activity

An export of each attendee's activity in the app — which sections of the app they opened and when they were last active.

**Typical uses:**
- Evaluating engagement (an internal corporate event and a client conference have different benchmarks).
- Source data for deciding whether to push more content into the app, or to turn the app off entirely for the next event.

### 11. Attendee app — list of users with the app

Only **who downloaded the app and signed in** for this specific event. A smaller subset, but an important one.

**Typical uses:**
- Before the event — who to send a push notification to versus who to send an e-mail to.
- After the event — who actually used the app (combined with the activity export).

### What is not in the exports

- **An automated export for the hotel** — missing. You assemble the data by hand from the *All attendees* export and the form responses. A dedicated automated export for accommodation providers is not yet a Happenee feature; today this is a manual workaround. See [Preparing data for accommodation providers](../05_event-day-and-on-site/03_preparing-data-for-accommodation-providers.md).
- **E-mail campaign send-out reporting** — lives in the **detail of the campaign**, not in a central export. A dedicated reporting view for e-mail campaign performance beyond raw counts (opens, clicks per segment, time-series of engagement) is not available today. See [Creating and sending an E-mail campaign](../04_communication-and-invitations/03_creating-and-sending-an-e-mail-campaign.md).
- **An interpretive layer** — Happenee exports are raw data. When a registration curve is *healthy*, when *too little is happening* — the organizer evaluates that themselves or with help from customer success. More graphs and statistics inside the admin are planned, but for deeper interpretation today you work with the raw export.

## Common pitfalls

### You download an export and then work with one that is months old

Exports are a snapshot taken at the moment of download. If you are looking at the current state, download again. Put the date in the file name (*attendees_2026-04-19.xlsx*) — otherwise after two downloads you will not know which one is the latest.

### You send a colleague the entire attendees export so they can find what they need

*All attendees* contains the personal data of everyone registered — a colleague who only handles catering does not need it. Pick a more targeted export (for example, the *Scanning export* when the question is actual attendance), or use **Attendee reports** to prepare a file with only the columns and filtered attendees they need. Sharing a live view of the data instead of a file is not possible: neither the statistics nor the *Registration* section has a link for someone outside the admin.

### Invoices get downloaded one by one from the order details

In **Orders**, the *Exports* button has an **Export invoice PDFs** item that downloads every document at once. Download a single invoice only when you need one specific document, for example after correcting the billing details.

### You assume the scanning export contains the *Checked-in / No-show* status

The scanning export has **one row per scan**, not one row per attendee. Anyone who passed through more than once (for example, *Check-in* plus *One-time check*) appears in the export multiple times. For a simple list of *who arrived*, use the attendees export filtered by the *Checked-in* status.

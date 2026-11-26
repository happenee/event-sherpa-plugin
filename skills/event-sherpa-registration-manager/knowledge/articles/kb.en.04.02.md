<!-- source: kb.en.04.02 -->

---
title: "How the Confirmation e-mail works"
description: "A system e-mail sent to the attendee automatically after registration, with the PDF ticket and the link into the app."
modules: ["komunikace_a_pozvanky"]
last_updated: "2026-09-21"
version: 2
---

> [!info] Overview
> The Confirmation e-mail is a system message that is **sent to the attendee automatically once registration is complete**. It usually carries a PDF ticket with a QR code and an ICS file for adding the event to a calendar. It works as the key bridge from registration into the attendee app — this is the e-mail the attendee uses to step in. If you have **Approved registration** turned on, the system works with three variants of the Confirmation e-mail (pending approval / approved / rejected).

## Getting started

- Fill in the Confirmation e-mail content **in every language of the event**.
- In Event settings, decide what to attach: the **ICS file**, the **PDF ticket with a QR code** (typically yes), or both.
- If you plan to use Approved registration, expect to set up three variants of the Confirmation e-mail.
- Test the full flow: registration → Confirmation e-mail → link into the attendee app.

## Details

### When the Confirmation e-mail is sent

- After the Registration form is submitted (the typical path).
- After payment is completed for a paid event with *Automatic registration after ticket purchase*.
- After the ticket is generated for *Registration with additional information* — only once the attendee finishes filling in the data.
- After an admin **manually flips the attendee status** to *Attending* in the admin (see below).
- For Approved registration, after the organizer **approves the registration manually**.

### What the Confirmation e-mail contains

In the **Confirmation e-mail** module in the event's left menu you find:

- The **e-mail subject**.
- A **body text editor** — with variables (merge tags) that automatically fill in the name, event name, date, and other data.
- An **HTML button** — for inserting your own button (for example, a link into the attendee app or a link to FAQ).
- **Variables** that are available in every e-mail module (Invitation, Confirmation, Campaigns) and on the microsite in the post-registration text.

### Cover image, attachments, and footer

Just like for the Invitation e-mail, graphics and attachments are controlled centrally from **Event settings**:

- **Cover image** — in Graphics settings, shared with the microsite and the Invitation e-mail.
- **ICS file** — in E-mail settings. It arrives as an attachment, and opening it adds the event to the calendar. Some e-mail clients display their own banner offering to add the event to the calendar.
- **PDF ticket with a QR code** — attach it so the attendee can print the ticket. The QR code in the PDF works the same as the QR code in the attendee app.
- **E-mail footer** — the platform default text or your own.
- **Sender and Reply-to recipient** — set in the same place.

### Approved registration — three e-mails instead of one

Approved registration is turned on in **Event settings** (only for unpaid events — it cannot be combined with Tickets). When it is active, the Confirmation e-mail has three variants:

- **Pending approval of registration** — the attendee receives this immediately after submitting the form. It says the registration was received and is waiting for the organizer's decision.
- **Approved (registration confirmation)** — sent after manual approval. It contains the PDF ticket and the ICS file. This is the "main" Confirmation e-mail in this situation.
- **Rejected** — sent after manual rejection. It informs the attendee that they will not attend the event.

Approved registration is useful when you really want to curate attendees (for example with a public link) or when you want to align invitations across several waves.

### Automatic send when an admin flips the status manually

In the event admin you can manually flip an attendee's status to **Attending** (in Registration). A typical case: the attendee wrote in by e-mail saying they will come but never went through the form. In this dialog the **admin chooses whether the Confirmation e-mail is sent** — typically yes, so the ticket arrives.

### Test Confirmation e-mail

Unlike the Invitation e-mail, the Confirmation e-mail goes automatically, so the test is indirect — go through the registration yourself (or trigger the send by manually flipping a status to *Attending*) and look at what actually arrives. Try it in both languages.

### Relationship to the attendee app

The Confirmation e-mail is the **first contact point** with the attendee app. It typically contains:

- A PDF ticket with a QR code (for entry on site).
- An ICS file for the calendar.
- A link (or text) leading into the attendee app — either "Download our app" (mobile) or "Open in the browser" (web).

The attendee signs in via **Magic Link**, **PIN**, or **QR code** sent to the same e-mail. That is why the Confirmation e-mail is critical for getting the attendee into the app at all.

## Common pitfalls

### An organizer fills in the Confirmation e-mail only in Czech, and an attendee who registers in English does not get the confirmation in their language

Switch the language flag and fill in the content in the second language too. Verify with a test registration in both languages.

### An organizer turns on Approved registration but does not realize they need to prepare three variants of the Confirmation e-mail. Attendees end up receiving messages without the organizer's text

For Approved registration, fill in all three variants — pending approval, approved, rejected — and do it in every language. A variant you leave empty goes out without your text.

### An organizer manually switches an attendee to *Attending* but unchecks "send Confirmation e-mail," so the attendee does not receive the ticket

If the attendee is supposed to come, leave sending turned on so they get the PDF ticket with the QR code and the link into the app. You can resend later from the registration detail.

### An organizer attaches a PDF ticket with a QR code on a paid event where payment happens after ordering — and the attendee receives the ticket before they pay

The Confirmation e-mail with the ticket goes only after registration is complete (and for proforma invoices, after the payment is credited and the registration is finalized). The ticket purchase process has its own e-mails (order confirmation, additional information).

### An organizer looks for the cover image, ICS, or footer inside the Confirmation e-mail module and cannot find them

Everything is set in **Event settings** (Graphics, E-mails, ICS, Footer). The Confirmation e-mail module is primarily for the subject and the body.

<!-- source: kb.en.04.01 -->

---
title: "How the Invitation e-mail works"
description: "The Invitation e-mail is the first wave of invitations to assigned contacts."
modules: ["komunikace_a_pozvanky"]
last_updated: "2026-09-21"
version: 3
---

> [!info] Overview
> The Invitation e-mail is a system message that you send to contacts assigned to the event so they can open the microsite and register. It contains a subject, a body (with variables), a registration button, optionally an ICS file, and a footer. It works as the **first wave of invitations** — typically right after you import contacts. If you need to target different groups or schedule a send, use an **E-mail campaign** instead.

## Getting started

- Assign contacts to the event first (in Contacts and groups). Without assigned contacts, there is nobody to invite.
- Fill in the Invitation e-mail content **in every language of the event** — the system sends the variant that matches the contact's *preferred language*.
- Before you launch a bulk send, send yourself a test invitation e-mail and verify the layout and the button.
- If you will need to target different groups or send a follow-up, prepare E-mail campaigns alongside the Invitation e-mail.

## Details

### Where to find the Invitation e-mail

In the event's left menu, open the **Invitation e-mail** module. The module contains the body editor, the subject, the registration button, settings, the send section, and statistics.

### Editor and variables

You write the e-mail body in a text editor. At the bottom you find **placeholder variables** (merge tags) that the system replaces automatically with attendee data — name, event name, date, and others. The same variables work in the Confirmation e-mail and in campaigns.

The editor handles basic formatting. A more advanced WYSIWYG editor is in progress; for everyday scenarios the current editor is sufficient.

### Registration button — where it should lead

The section **Where should the registration button lead?** sets the destination of the button. The options depend on the event type:

- **Personal recipient link** — the link is tied to one specific contact. At a free event the registration e-mail cannot be changed, and the recipient can confirm or decline attendance. At a paid event the link personalizes the microsite and the recipient continues to ticket purchase, where they may enter a different e-mail.
- **Public link** — clicking opens the microsite, where the visitor enters any e-mail address and continues. The link can be shared publicly.
- **Individual free admission** — paid events only. The recipient registers without having to buy a ticket; this is the tool for a free guest list.

Which type to use when is described in the article *Personal link vs. public link: what is the difference*.

### Cover image, ICS, and footer

Graphical and technical elements are shared with the Confirmation e-mail and the microsite, so you set them centrally in **Event settings**:

- **Cover image** — in Graphics settings. Shared across the Invitation e-mail, the Confirmation e-mail, the microsite, and the attendee app.
- **ICS attachment** — in E-mail settings / ICS file. Once expanded, it lets the attendee add the event to a calendar.
- **E-mail footer** — in E-mail settings. Either the platform default or your own.
- **Sender and Reply-to recipient** — also in E-mail settings.

### Sending — individual and bulk

In the **Send** section you have two paths:

- **Individual send of the Invitation e-mail** — pick a specific contact and send only to them. Useful for a test send (to yourself) or for inviting one person manually.
- **Bulk send of the Invitation e-mail** — you send to one of the following statuses:
  - **Not invited** — contacts assigned to the event who have not yet received the Invitation e-mail.
  - **Did not open the Invitation e-mail** — for a second wave when there was no reaction to the first.
  - **Not registered (no response)** — they got the invitation but have not yet completed the Registration form.

The system also shows you **how many contacts are assigned to the event** and in which languages — for example, "43 in Czech, 13 in English, 2 with no language set."

### Language fallback per contact

The Invitation e-mail is sent according to the contact's **preferred language** in Contacts and groups. So:

- When you import contacts, fill in the language column. If language is not set, the system uses the event's primary language.
- The preferred language is also pre-set automatically during registration from the microsite — based on the language the attendee opened the microsite in.
- If you have contacts without a language, fill it in before sending, or expect them to receive the variant in the primary language.

### Test invitation e-mail

Individual send doubles as a test tool — send yourself the Invitation e-mail (or to a test address) and verify the layout, the variables, and the button. Always test the **second language** as well, not just the primary one.

### Statistics and reporting

Below the send section you find an overview of the Invitation e-mail status — who it was sent to, who opened it, who responded with a registration. These statuses also serve as targeting for further sends ("did not open," "no response").

### Legacy status and the move toward E-mail campaigns

The Invitation e-mail is a legacy module — it predates E-mail campaigns. It does not connect to reporting on the same scale as campaigns and **cannot target by groups**, only by attendee statuses. If you need more flexible targeting, scheduling, or follow-up to newly assigned contacts, use a campaign.

In this area the product is moving toward routing all invitation communication through campaigns. The Invitation e-mail itself still runs and is fully functional.

## Common pitfalls

### An organizer fills in the Invitation e-mail only in the primary language, and contacts with the second language do not get the invitation in their language

After switching the flag in the top right corner, fill in the body and the subject in the secondary language too. Before sending, send yourself a test invitation e-mail in both languages.

### An organizer imports contacts without a preferred-language column and then wonders why English-speaking attendees got an invitation in Czech

When importing, fill in the language column. If it is missing, add it in Contacts and groups individually or with a bulk edit — and only then run the send.

### An organizer wants to invite only a specific group (for example VIPs), but the Invitation e-mail does not allow it

The Invitation e-mail targets only by status, not by groups. To target groups, use an **E-mail campaign**.

### An organizer expects the Invitation e-mail to also reach contacts that are not yet assigned to the event

Assign contacts to the event in Contacts and groups — only then will they appear in the send.

### An organizer forgets that the cover image and the footer are not in the Invitation e-mail module and looks for them inside the editor

Graphics and the ICS attachment are managed from **Event settings** (Graphics settings and E-mail settings sections). In the Invitation e-mail module you mainly edit the body and the subject.

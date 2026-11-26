<!-- source: kb.en.04.12 -->

---
title: "How placeholder variables work"
description: "Placeholder variables fill individual attendee data into an e-mail, a campaign, or the microsite — the full list of universal variables, the ones tied to custom contact fields, and how to test them."
modules: ["komunikace_a_pozvanky"]
last_updated: "2026-08-07"
version: 2
---

> [!info] Overview
> **Placeholder variables** are markers in the form `::VARIABLE::` that are replaced at send time with a specific attendee's data — their name, the event name, a QR code. You insert them into the text of the Invitation e-mail, the Confirmation e-mail, a campaign, or microsite content, and every recipient then receives the text with their own values. Alongside the universal variables there are also placeholders tied to **custom contact fields**, which differ from workspace to workspace.

## Getting started

1. Open the text you are writing (a campaign, the Invitation or Confirmation e-mail) and find the **Placeholder variables** section.
2. Every variable has a copy icon — copy the variable and paste it into the text field exactly where the value belongs.
3. Include **both pairs of colons**. `::UZIVATEL_JMENO::` works; `:UZIVATEL_JMENO:` and `::UZIVATEL_JMENO` do not.
4. Before you send, use **Test campaign** to send yourself a copy and check that the variables were actually replaced.

## Details

### Universal variables

These are always available, regardless of how your workspace is configured:

- **`::UZIVATEL_JMENO::`** — Attendee first name
- **`::UZIVATEL_JMENO_PRIJMENI::`** — Full name
- **`::UZIVATEL_EMAIL::`** — Attendee e-mail
- **`::NAZEV_UDALOSTI::`** — Event name
- **`::KDY::`** — Event date and time
- **`::KDE::`** — Event location
- **`::KONTAKTNI_OSOBA::`** — Contact person name
- **`::QRCODE::`** — QR code for entry
- **`::VAR_SYMBOL::`** — Variable symbol
- **`::DATUM::`** — Current date
- **`::O_APLIKACI::`** — App information block — the content follows the event type (in-person, virtual, hybrid)
- **`::UDAJE_O_UZIVATELI::`** — The data the attendee entered during registration
- **`::REGISTRACNI_FORMULAR::`** — Data entered in the registration form
- **`::EVENT_CERTIFICATE_OFFLINE::`** — Certificate download link for an in-person event

The variable names stay in their original form in every language — they are identifiers, not translated labels.

Some of them insert a **whole block** rather than a single word — typically `::O_APLIKACI::`, `::UDAJE_O_UZIVATELI::`, and `::REGISTRACNI_FORMULAR::`. Do not use those mid-sentence; put them on their own line.

### Variables for custom contact fields

If you have custom contact fields in your workspace, Happenee generates a separate placeholder for each of them in the form `::CF####::`, where the digits are the field's internal identifier. You find the list below the universal variables, under the **Placeholders for custom contact fields** subheading.

**These are not universal.** The numbers are assigned within your workspace, so a variable that fills in a salutation for you can mean something entirely different in another workspace. Never copy them from a guide or from another event — always take them from the list in your own admin.

### A custom button in HTML

Below the list of variables there is a ready **HTML snippet for a custom button**. Copy it into your text and edit the target address and the label. It is useful when a campaign needs its own call to action — a link to the agenda, a survey, a map — alongside the standard registration button.

### Where the variables work

Placeholder variables are replaced in microsite content, in the Invitation and Confirmation e-mails, and in E-mail campaigns. The **Contact** feature is merged into e-mails automatically, so you do not have to type the contact person by hand — `::KONTAKTNI_OSOBA::` is enough.

### Multilingual texts

The variables themselves are not translated — `::UZIVATEL_JMENO::` is identical in the Czech and the English version of a text. What differs is the sentence around it. When you write a bilingual campaign, check that you inserted the variable into **both** language versions; a variable missing from the second language is one of the most common reasons part of your recipients get an impersonal e-mail.

## Common pitfalls

### The variable arrives as literal text

When `::UZIVATEL_JMENO::` shows up verbatim in the delivered e-mail, the variable was written incorrectly — most often the closing colons are missing, or there is a typo or a space inside. So copy variables with the icon from the list rather than typing them from memory, and send yourself a test campaign before the real send.

### An empty name in the greeting

A variable fills in only what the contact record actually holds. For people imported with nothing but an e-mail, "Hello ::UZIVATEL_JMENO::," becomes "Hello ,". Before sending a campaign with a personal greeting, check the contact table for how many people have no first name — then either fill them in or switch to a neutral greeting.

### Copying a custom-field variable from another event

The numbers in `::CF####::` are valid for your workspace, not in general. Copy one from someone else's guide or e-mail and either nothing is filled in, or the value of an entirely different field is. Always take them from the list in your own admin.

### Putting a QR code in a campaign for people who have not registered

`::QRCODE::` only makes sense for people with a completed registration — for anyone else the system has nothing to render. When a campaign carrying a QR code targets a segment that includes contacts who have not registered, they receive an e-mail with a blank space. Targeting by attendee status matters more on this kind of campaign than on any other.

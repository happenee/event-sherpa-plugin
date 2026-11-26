<!-- source: kb.en.02.05 -->

---
title: "Setting up the Registration form"
description: "How to build the Registration form for contact details and additional questions specific to the event."
modules: ["registrace"]
last_updated: "2026-09-02"
version: 4
---

> [!info] Overview
> The Registration form is the tool you use to collect **contact details** (shared across the workspace) and **additional questions** specific to a single event. The form is part of the microsite and appears after an attendee enters an e-mail address or clicks **Continue to registration**. For events with Tickets, the form is accessible only after payment (with the *Registration with additional information* option).

## Getting started

- Decide **which contact details you need to be required** — the e-mail address is always required, the rest is up to you.
- List the additional questions you need — transportation, catering, workshop selection, accommodation, preferences.
- If you want certain questions visible only to certain attendee groups, plan the groups in advance.
- For multi-language events, prepare the wording of every question and answer in every language.
- You edit the form in the event admin under **Registration form** in the left menu.

## Details

### Two tabs in the form

The Registration form has two main tabs:

- **Contact details** — shared with the entire workspace. What an attendee fills in carries over into your contacts and is available for future events.
- **Additional questions** — specific to a single event. Each event has its own set of questions.

### Contact details — Required, Optional, Hide

Contact detail fields are pre-defined by Happenee. The available fields are **E-mail**, **First name**, **Last name**, **Phone**, **Job title**, **Company**, **Company ID**, **Country**, **Twitter (X)**, and **LinkedIn**. For each field you choose:

- **Required** — the attendee must fill in the field.
- **Optional** — the field is shown but filling it in is not required.
- **Hide** — the field is not shown to the attendee at all.

The e-mail address is always Required — this setting cannot be switched off.

Below the standard contact fields sits a separate **Custom contact fields** section with the same three options. You define these fields in **Workspace settings** (they are shared across all events). Common uses: salutation, internal employee ID, department, business-trip cost.

> **When automatic registration is turned on**, these contact details apply only to **individual and bulk registration links** — that is, to registrations without a ticket purchase. Anyone going through a ticket purchase fills in the fields configured on that specific ticket instead. The admin shows a note about this directly above the field list.

### Additional questions

On the **Additional questions** tab you add event-specific questions by clicking **+ New question**. For each question you set (in the **Choose a question type** dropdown):

- **Question or field label** (required).
- **Additional description** (optional — short explanatory text under the question).
- **Question type** (see below).
- **State** (Required, Optional, Hide).
- **Visibility** — you can show the question only to selected groups.
- **Delete data three months after the event** (automatic retention under GDPR).

You change the order of questions with drag-and-drop.

### Question types

When creating a question you pick the type. The Happenee UI offers 17:

1. **Answer with custom text** — free text input.
2. **Select only one** — dropdown or radio.
3. **Select only one or custom text** — combination.
4. **Can select multiple** — checkbox.
5. **Can select multiple and custom text** — combination.
6. **Select only one offered answer with response limit** — for example *Bus 1 (20 seats), Bus 2 (20 seats)*. The system tracks capacity.
7. **Accommodation — select attendee from list** — see *Managing accommodation and roommate selection*.
8. *(Enter their ISIC card number for approval — do not use, the integration does not work.)*
9. **Select multiple attendees from list.**
10. **Upload an image** — the attendee uploads an image.
11. **Enter a date.**
12. **Enter a time.**
13. **Enter date and time.**
14. **Enter a number.**
15. **Informational text** — not a question, just a block of text inserted into the form (for example, instructions).
16. **Uploads file (PDF, XLSX, DOCX)** — the attendee uploads a file.
17. **Chooses country from list.**

### Type 2 — answer variants and advanced settings

For a *Select only one* question you build a list of possible answers. For each answer you can:

- **Set visibility** — the answer appears only to selected groups.
- **Assign to group** based on the chosen answer. Example: a question *Where are you traveling from?* with the answer *Brno* assigns the attendee to the **Brno** group. You can then target communication to that group.
- **Add conditional questions** under a specific answer — see *How conditional questions work in the Registration form*.
- **Send ICS based on selected answer** (available on type 2 and type 6). Instead of an ICS file with the event date, the system sends an ICS with dates that match the specific answer. Each answer can have its own start–end date.

### Type 6 — answer with limit

Type 6 fits situations with a fixed capacity — buses, workshops, evening programs. For each answer you set:

- **Maximum number of seats.**
- **Show attendees the limit and remaining spots** — optional display of the remaining count.
- **Show possible number of companions** — set how many companions a registration can request.
- **Send ICS based on selected answer.**
- **Delete data three months after the event.**

Type 6 also handles companions in one place — you can offer the bus and the number of companions in a single question.

### Intro text, post-submit text, button position

In the form admin you can edit:

- **The position of the registration button** on the microsite.
- **The text shown after the form is filled in and submitted** — it appears as the thank-you screen. It supports placeholders (attendee name, event name).

### Preview and exports

- **Form preview** opens the form exactly as the attendee will see it.
- **Question structure** shows an overview of how conditional questions are linked.
- **Exports** — answers from the form can be downloaded in Excel or CSV (the **Results (Excel)** export). The admin lets you save filtered views for different teams. The same tab also offers the **GDPR consents beyond the legal minimum** export — a list of all attendees of the event showing who granted each extra consent and who did not. The same export is also available in the **Statistics** section; for when to use which export, see [Working with Orders and exports](../06_reporting-and-after/03_working-with-orders-and-exports.md).

### Multiple languages

The language switcher (**Content language** with the flag icon, top right) switches the language you are currently editing. For a multi-language event, you fill in every language separately — questions, answers, texts. If you leave a language blank, the event's primary language is used as the fallback.

### Personal data protection and consents beyond legitimate interest

At the end of the form, the attendee sees the personal data protection text (default or custom — set in **Workspace settings → Personal data protection**) and the **consents beyond legitimate interest** (marketing, photo publication, profiling). At the form level you decide whether the consents beyond legitimate interest are shown. To see who granted which consent, download the **GDPR consents beyond the legal minimum** export on the **Exports** tab.

## Common pitfalls

### An organizer adds a type 8 (ISIC) question expecting the system to verify the student card

The ISIC integration does not work today — do not use this option. To verify a student, use a regular question (for example, type 10 — upload an image of the student card) or verify manually.

### Additional questions are not set up, and when an attendee goes through Automatic registration after ticket purchase on a paid event, no data is collected from them

For paid events that need additional data, always choose **Registration with additional information**, not **Automatic registration after ticket purchase**. For free events, just add the additional questions and the form is shown.

### A type 6 question is on and the attendee sees the bus, but capacity is not displayed

The toggle **Show attendees the limit and remaining spots** is optional. If you do not want to show capacity but you want to track it, leave the toggle off. The system still controls how full the option is.

### Translations of questions and answers are filled in only in some active languages, and an attendee whose preferred language is blank sees the form in the fallback language

Switch through every active language with the flag and fill in the wording. If you leave a language blank, the primary language is used as the fallback — which means the attendee sees the form in a language they did not pick.

### Questions are set up, but it is not thought through how the answers will flow into groups, and the organizer ends up sorting attendees by hand afterward

For a type 2 question (Select only one), use the **Assign to group** setting directly on each answer. Create the group beforehand, and the form takes care of the assignment.

<!-- source: kb.en.05.03 -->

---
title: "Preparing data for accommodation providers"
description: "How to stitch data for the hotel by hand from several exports, since Happenee does not yet offer a single merged export."
modules: ["checkin_a_tisk_jmenovek"]
last_updated: "2026-04-27"
version: 1
---

> [!info] Overview
> If you are arranging accommodation for a multi-day event, **the hotel typically needs more information than Happenee exports in a single click**. Room occupancy (who shares with whom) is in **Room administration**. Contact details, arrival and departure dates, preferences, and special requests live in the Registration form. To produce the list the hotel actually needs, you currently **stitch the data together by hand** from several exports — usually using the e-mail address as the key inside a spreadsheet. Happenee does not yet offer an automated, merged export for accommodation providers; this is a manual workaround for now.

## Getting started

- **Confirm with the hotel** what exactly the rooming list needs to contain — name, e-mail, phone, check-in / check-out date, room type, roommate, dietary restrictions, special requests.
- In the **Registration form**, make sure you collect every one of these data points — either as standard contact fields (name, e-mail) or as **additional questions** (arrival date, dietary needs, free-text notes).
- For **roommate selection**, use a type 7 question and set up **Room administration** (see *Managing accommodation and roommate selection*).
- Prepare the final spreadsheet for the hotel **at least seven days before the event** — late changes to registration are hard to weave back into the list and inconsistencies start to appear.
- Assign **one owner** on your team who maintains and updates the spreadsheet. Never let two people edit it in parallel.

## Details

### What Happenee exports out of the box

If you handle accommodation through a type 7 question, you have three sources of data inside the event admin:

- **Room administration** (inside the type 7 question detail) — the list of generated rooms and who is in each. The export contains **first name, last name, e-mail, room name, room type, roommate**. Nothing more.
- **Registration form / responses** — an export of every attendee's answers to all additional questions. This is where arrival date, dietary restrictions, and requests like *late check-in* or *baby cot* live.
- **Contacts and groups** — contact details (phone, company, custom contact fields). The base for the hotel if it requires a phone number.

### How to stitch the data together

Because Happenee does **not yet** offer an automated export for accommodation providers, you assemble the data by hand. The typical sequence:

1. **Export Room administration** — you get a table of *name + e-mail + room + type + roommate*.
2. **Export the Registration form responses** — a table with all the additional questions.
3. **Export contacts from Contacts and groups** — phone, company, other fields.
4. **Merge in Excel** using the **e-mail address as the key** (VLOOKUP / INDEX-MATCH / Power Query). E-mail is the most reliable identifier — names can be entered with different diacritics, but the e-mail is unique.
5. **Clean it up** — check for empty fields, duplicate registrations, and attendees who canceled their registration (see the color legend in Room administration — a row shaded purple means *the user has canceled their registration*).
6. **Format to the hotel's requirements** — not every hotel accepts Excel; some require CSV, others a PDF list sorted by name.

### Why the Room administration export is so minimal

The export from Room administration is intentionally **minimalist** — it carries only attendee identity and room placement. It **does not contain** arrival date, dietary needs, phone number, or special requests. Those data points live in the **Registration form** (additional questions) or in the **contact fields**. If you need them, you have to add them in by hand.

### Typical fields the hotel asks for on top

- **Phone number** — almost always required (the hotel calls when something goes wrong). Set it up as a contact field in the Registration form or as a custom contact field.
- **Arrival and departure date** — needed when attendees arrive on different days. Typically an additional question of type *date*.
- **Room preference** — single occupancy only? upper floor? non-smoking? Use an additional question of type *Select only one* or a free-text field.
- **Dietary restrictions** — an additional question with several options (vegetarian, vegan, gluten-free, allergies).
- **Arrival time** — when the hotel manages reception capacity. Use a *time* question type.

If you do not have **matching questions in the form** for these fields, the hotel will not get them — and you will not be able to ask after the fact (the event is a week away and registrations are closed). Set up the form **before you open registration**, not after.

### Recommended timing

- **Before opening registration**: agree with the hotel what they need. Configure the form so it collects everything.
- **Throughout registration**: export a working spreadsheet weekly. Keep an eye on whether the people registering still fit into the rooms you generated (see *Managing accommodation and roommate selection*).
- **7–10 days before the event**: send the final spreadsheet to the hotel. Confirm receipt and lock in the numbers. Handle changes after this deadline individually.
- **2–3 days before the event**: send the hotel an **update** (cancellations, late additions). Ideally in the same format.

### One owner — keep it that way

Even when several people on the team work on event operations, the **final hotel spreadsheet should have a single owner**. Two parallel versions in Excel are a guaranteed source of mistakes. The owner has access to the event admin, can see registration changes, and is the contact point for the hotel.

## Common pitfalls

### The organizer sends the hotel the raw Room administration export and is surprised when the hotel calls asking for phone numbers and dietary information

The Room administration export contains only first name, last name, e-mail, and room. Contact details and special requests have to be added in from the Registration form export and from the contacts export.

### The Registration form is missing a field the hotel requires (typically phone or arrival date)

Set the form up **before you open registration**. Asking individually by e-mail later is tedious and you never get a 100 percent response rate.

### Two people maintain the hotel spreadsheet in parallel, each makes small edits, and the versions diverge

One owner. Everyone else on the team supplies inputs only — never edits the master file directly.

### The spreadsheet goes to the hotel in the morning; in the afternoon five attendees cancel, and the hotel charges for all five rooms

Agree on a **cutoff date** with the hotel for the final list (cancellation terms). After the cutoff the hotel charges for changes; before it, the flexibility is yours.

### The hotel does not accept Excel and expects CSV or PDF

Confirm the format up front. Excel converts easily to CSV (File → Save as). A PDF can be produced through Print to PDF with a fixed layout.

### The organizer expects a single ready-made "for the hotel" export as one button inside Happenee

A dedicated automated export for accommodation providers is **not yet a Happenee feature**. You work by hand with a combination of exports. If you run large events with accommodation regularly, invest in an Excel template you can reuse from one event to the next.

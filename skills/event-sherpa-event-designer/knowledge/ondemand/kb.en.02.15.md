<!-- source: kb.en.02.15 -->

---
title: "Adding an attendee manually"
description: "Every way to get a person into an event outside the registration form — assigning a contact or a group, importing, walk-ins on site — and what each one does to the attendee status."
modules: ["ucastnici_skupiny_a_viditelnost", "registrace"]
last_updated: "2026-10-26"
version: 3
---

> [!info] Overview
> An attendee does not have to reach your event through the registration form — you can add them yourself. There are several routes: **assigning an existing contact**, **assigning a whole group**, **bulk import from Excel**, and on site **creating a walk-in directly in the Service app**. The critical distinction is between **assignment** and **registration**: assigning puts a person on the event list, but it does not register them, and the e-mails that depend on registration will not reach them.

## Getting started

Before you add someone, decide what should happen next:

- **Are they still deciding whether to come?** Assign the contact to the event and send them the Invitation e-mail. They will complete the registration themselves.
- **Do you already know they are coming and need no data from them?** Assign them to the event and expect them to stay in the no-response status until someone fills in the form.
- **Are they standing in front of you on site?** Create them directly in the Service app as a walk-in and check them in.

## Details

### Assigning a single contact

In **Contacts and groups** you either find an existing contact or create a new one with the **Add contact** button (e-mail at minimum, then first name, last name, phone, company, preferred language). You then select the contact and use the **Event assignment** bulk action to add them to a specific event. The same route removes them from the event again.

Contacts are shared across the whole workspace — one contact can be assigned to any number of events, and their details carry across all of them.

### Assigning a whole group

The faster route for larger sets of people: on the **Groups** tab, click a group and assign the whole group to the event. Everyone in the group is added. This works well for a recurring audience (*management*, *partners*, *internal team*) that you invite again and again.

Note that the assignment is a one-off action, not a live link. If you add a person to the group **after** you assigned the group to the event, they will not carry into the event on their own.

### Bulk import from Excel

For tens or hundreds of people, use the import in **Contacts and groups**. In the template you can set the group directly (with the `#` prefix) and the preferred language. After the import, assign the group to the event and you are done. The full procedure is in [Managing contacts and groups in your workspace](03_managing-contacts-and-groups-in-your-workspace.md).

### Walk-ins on site

When somebody arrives without a registration, you do not have to create them in the admin. In the Service app in **Staff mode**, the **Attendees** tab has an **Add attendee** button — you enter the e-mail, first name, last name, company, and job title, save, check them in, and print a badge if you need to. See [How check-in and QR-code scanning work](../05_event-day-and-on-site/01_how-check-in-and-qr-code-scanning-work.md) for details.

### Adding someone to a session or a time slot manually

Adding a person to the event and adding them to a specific session are two different things. On sessions with registration and on time slots, the organizer can add an attendee by hand — find them in the registered list and add them. People added this way are marked as **Assigned by organizer**, so you can tell who signed up themselves and who you put there.

### What happens to the attendee status

Assigning a contact to an event **is not a registration**. The person shows up on the list in the no-response status and only moves on once the form is submitted (or a ticket is bought). That has two practical consequences:

- **The Confirmation e-mail with the ticket in PDF and the QR code will not reach them**, because it is tied to a completed registration. If they need the QR code, send it from the web **Check-in** tool or check them in by name.
- **In the statistics they count as invited, not registered.** Your numbers will not add up unless you keep that distinction in mind.

Statuses can also be edited by hand in the **Registration** section — for example switching somebody to *Not attending* when they cancel over the phone.

## Common pitfalls

### You cannot remove the event's administrator or creator in Registration

When you remove an attendee from the event in **Registration**, the system rejects the removal if the contact is an administrator or creator of this event. The message explains the specific reason, and the contact remains assigned. This action does not change event ownership or access; contact the person responsible for managing access if you need a change.

### Mistaking assignment for registration

The most common misunderstanding. An organizer assigns 200 contacts, sees them on the event list, and considers the event full — but they are not registered, they received no tickets, and there is nothing to scan at check-in. Assignment is an invitation, not attendance.

### Adding people to a group after it was assigned to the event

If you assign a group to an event and only then add more people to it, the new members will not be in the event. Repeat the assignment after every addition to the group, or add those contacts individually.

### A manually created contact with no preferred language

On a contact created in a hurry it is easy to skip the language — and the Invitation e-mail then goes out in the workspace default language even though the event has two language versions. Fill the language in when you create the contact, either individually or in the import template column.

### A walk-in created on site has no further details

The Service app collects only basic details so that check-in stays fast. When you need answers from the registration form (dietary restrictions, workshop choice, consents), you will not have them — the walk-in never went through the form. Keep that in mind for reporting and for handling consents.

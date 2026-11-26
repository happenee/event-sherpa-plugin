<!-- source: kb.en.07.09 -->

---
title: "Recommended setup for test drives"
description: "How to prepare test-drive reservations around the actual availability of vehicles, instructors, and on-site operations."
collection: "Event Sherpa"
subcollection: "pro-specializovane"
modules: ["prurezovy"]
slug: "recommended-setup-for-test-drives"
lang: "en"
status: "published"
docId: 98
last_updated: "2026-09-21"
version: 2
tags: [test-drives, reservations, time-slots, vehicles, event-sherpa]
source_images_consulted: false
related:
  - "Setting up reservations in the Agenda — buses, workshops, social program"
  - "How time slots work"
  - "Building the event Agenda — architecture"
  - "Setting up workshops and session registration"
  - "How check-in and QR-code scanning work"
---

> [!info] Overview
> Build a test drive around the actual operational cycle: guest arrival, eligibility checks, a briefing, vehicle handover, the drive, return, and preparation for the next guest. In Happenee, you offer reservations through sessions of type Time slot and give guests the agenda, instructions, and a contact in the attendee app. Happenee does not automatically coordinate the simultaneous availability of a vehicle, instructor, route, and handover point, and it does not record whether the guest actually completed the drive.

## Getting started

Answer five questions first:

- **What does the guest reserve, and what should they get out of the drive?** A specific vehicle, a model, or only a visit with manual vehicle assignment? And what should the guest take away, and what do you as the organizer need to report? Agree on how you will recognize success before you open reservations.
- **What limits the number of concurrent drives?** The number of vehicles, instructors, handover points, a safe route, or a combination of them?
- **How long does the full cycle take?** Include eligibility checks, the briefing, handover, return, inspection, and an operating buffer, not only the time behind the wheel.
- **Who may drive, and who verifies it?** The operator defines and checks the conditions, licenses, and other required documents.
- **Who decides after a delay, a cancellation, or an unavailable vehicle?** Name the responsible person and the fallback before you open reservations.

If you do not know the full cycle time, run one physical trial drive. Do not treat the theoretical number of slots as confirmed capacity.

## Details

### Choosing a reservation model based on resources

Use a separate Agenda and sessions of type Time slot for reservations. Happenee does not have a separate reservation module; a reservation is a registration for a specific slot, and the guest sees it in My Agenda.

- **A specific vehicle or specialist:** one session represents one resource. The guest knows what they reserve, but you must coordinate the other required resources outside the system.
- **Interchangeable vehicles of the same model:** the capacity of one slot may match the number of drives that staff can actually handle. Use this model only when staff can assign a specific vehicle on site and the numbers of instructors and handover points support that capacity. Keep in mind that all guests in one slot arrive at the same time and that your records will not show who drove which vehicle.
- **Arrival without a reservation:** publish a visiting window and manage the queue manually. Tell guests that they do not have a guaranteed drive time. Happenee does not have an automatic waitlist.
- **Several models during one visit:** leave time for moving between vehicles and a briefing between reservations. The default restriction on concurrent registrations prevents a guest from reserving two slots at the same time, but it does not verify that an instructor or a vehicle is free for both drives.

Do not create two concurrent drive schedules just because you have two vehicles if both require the same instructor. One shared resource may be the actual limit on total capacity.

### Setting time slots for the full cycle

For each session, set the date, start, and end, the **Time slot length**, the **Break length**, and **Limit number of registrations** (the capacity of one slot). The slot length comes from a fixed list of 10 to 120 minutes, and the break can be 0, 5, 10, or 15 minutes. Verify everything before the first reservation: after the first guest registers, the session type, start and end time, slot length, and break length are locked.

For example, the drive itself takes 20 minutes, and handover and preparation take another 10 minutes, so the slot is 20 minutes and the break is 10 minutes. The full cycle is 30 minutes. If you have a single instructor who must sit in every vehicle, that instructor can handle no more than six theoretical drives in three hours without an operating buffer. Two vehicles do not double that limit. A safer first schedule offers five slots and keeps one block for delays or preparation: on the **Slots** tab, switch one slot to **Inactive**. Confirm the specific plan with a physical trial.

For the Workshop and Time slot types, you can set **Registration time limits** (from when until when guests can reserve) and **Session cancellation** (until when a guest can cancel the reservation themselves). Session cancellation adds a deadline; it does not prohibit cancellation: without a deadline, a guest can cancel the reservation at any time. After the deadline, the guest can neither cancel the reservation nor switch to another slot; you make the change for them.

### Connecting the reservation to the guest journey

The microsite can introduce the models and conditions before registration. In the attendee app, the guest finds the Agenda, their reservation in My Agenda, the location, instructions, and a contact. The web app runs in a browser without installation; you do not need to create the event as hybrid to get it, because an in-person event offers both the web app and the mobile app.

Even for a small number of guests, we recommend offering the attendee app as part of the full Happenee ecosystem without forcing it on anyone. After the drive, guests can return in the same environment to materials, a contact, or further dates in the series, subject to access and licensing. For a series of test-drive days, that return is part of the value: it is not only one reservation. Match the content and follow-up communication to the guest's actual interest and the consents you have from them.

If you do not use the attendee app, provide the time, location, conditions, and a contact for changes through another agreed channel. A PDF is not a self-service reservation system; a named person must own changes.

On the session, turn on **Notify the attendee when registration changes** so that the guest receives an e-mail on reservation and on cancellation, and optionally **Send ICS to attendee**. Always pass an operational change (a different time, a different vehicle, a canceled drive) to the guest yourself. An update in the admin alone does not mean that the guest knows about it.

### Separating arrival, the drive, and the next step

At arrival, staff check the guest in with the Service app by scanning the QR code or from the list by name. Check-in records arrival at a place, not a specific reserved drive: it does not prove that the guest completed the drive or returned the vehicle. You can record handover and return as additional **check-in places** of type **Recurring check** (for example, *Vehicle handover* and *Vehicle return*): staff scan the guest at handover and again at return, and the scan export gives you the time of both. The record belongs to the guest and the place, not to a vehicle or a slot; it does not verify the vehicle's condition or the guest's eligibility. If that is not enough, keep an agreed operational record.

After the event, report these separately:

- reserved slots (the registration export on the session);
- guests who arrived (check-in);
- drives actually completed (the scan at return or the operational record);
- feedback;
- the next step the guest asked for.

A reservation is not a completed drive, and check-in is not a commercial outcome. Pass to a CRM or the sales team only the contacts and next steps for which you have the guest's consent and an agreed process.

## Common pitfalls

### Capacity matches the number of vehicles, not the shared instructor

Happenee is not an automatic planner for every required resource. Build the schedule around the narrowest real constraint and test it with the operator.

### The slot counts only the driving time

Add eligibility checks, the briefing, handover, return, inspection, maintenance or charging, and staff breaks. The break between slots is a separate setting with a maximum of 15 minutes; build a longer buffer into the slot length. Otherwise, one delay carries into every later reservation.

### An unavailable vehicle stays bookable

Reflect known downtime in the slots before you open registration: on the **Slots** tab, switch the affected slots to **Inactive**. If a vehicle drops out after a reservation, first agree on a replacement with the guest, then update the reservation (remove the guest from the original slot in its **Edit attendees** dialog and add them in the same dialog of the new slot) and verify that the guest received the change.

### A reservation is mistaken for a safety check

The responsible person verifies driving eligibility, documents, vehicle condition, and safety requirements. A valid reservation does not replace that check.

## Related articles

- [Setting up reservations in the Agenda — buses, workshops, social program](../03_content-and-attendee-experience/10_setting-up-reservations-in-the-agenda-buses-workshops-social-program.md)
- [How time slots work](../03_content-and-attendee-experience/09_how-time-slots-work.md)
- [Building the event Agenda — architecture](../03_content-and-attendee-experience/06_building-the-event-agenda-architecture.md)
- [Setting up workshops and session registration](../03_content-and-attendee-experience/08_setting-up-workshops-and-session-registration.md)
- [How check-in and QR-code scanning work](../05_event-day-and-on-site/01_how-check-in-and-qr-code-scanning-work.md)

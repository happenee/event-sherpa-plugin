<!-- source: kb.en.03.09 -->

---
title: "How time slots work"
description: "A session where the attendee reserves a specific time from a list (test drives, consultations, meetings)."
modules: ["program_a_sessions"]
last_updated: "2026-09-16"
version: 9
---

> [!info] Overview
> A Time slot is a session type where the attendee **reserves a specific time** from a list. The session has a defined duration (for example, one hour), which the system splits into **individual slots** (for example, 15-minute slots with a 5-minute break between them). The attendee picks the slot that fits their schedule. Typical use cases: test drives, one-on-one consultations, one-to-one meetings, social program (detail in *Setting up reservations in the Agenda — buses, workshops, social program*).

## Getting started

- Decide the **length of one slot** based on how much time you need for the interaction. You can pick 10, 15, 20, 30, 45, 50, 60, 90, or 120 minutes; the default is 15 minutes. Other lengths (for example, 5 or 25 minutes) are not available.
- Decide the **break length** between slots (a pause for handover or reset). You can pick 0, 5, 10, or 15 minutes; the default is 0 minutes, so slots follow each other back to back. The break is a separate setting and is not counted toward the slot length.
- The **maximum number of attendees per slot** is usually 1 (one-on-one consultation), but you can allow more (group slots).
- A Time slot is a session, so it has a stage, speakers (instructors / experts), and the other attributes of a regular session.

## Details

### How a Time slot is created

A session of type **Time slot** has, in addition to the usual tabs, an extra **Slots** tab in the edit panel. To create one:

1. Create a session of type **Time slot** (or a custom type built on this base).
2. Enter **date, start, end** — this defines the total session length (for example, 9:00–12:00 = 180 minutes).
3. In the **Registration settings** section, enter:
   - **Time slot length** — one of 10, 15, 20, 30, 45, 50, 60, 90, or 120 minutes. The default in the dropdown is 15 min.
   - **Break length** — pause between slots: 0, 5, 10, or 15 minutes (default 0 min).
   - **Limit number of registrations** — number of attendees per slot (default 1).
4. Save. The system generates the slots.

For a 180-minute session with 15-minute slots and a 5-minute break, the system generates **9 slots** (9:00, 9:20, 9:40, 10:00, 10:20, 10:40, 11:00, 11:20, 11:40). A remainder at the end of the session that is shorter than one slot is not created as a slot.

### The Slots tab

The **Slots** tab is available only for sessions of type Time slot. It shows every generated slot — each with its time range, capacity, and number of registered attendees. Breaks between slots are shown as separate rows.

For each slot you can:

- **Toggle Active / Inactive** — an inactive slot is not available for registration (typically when an instructor drops out and the slot is canceled). If the slot has registered attendees, saving shows a confirmation dialog with their number. **Remove attendees and save** cancels the registrations and deactivates the slot; if you close the dialog, the change is not saved.
- Click the **Attendees** button to open the **Edit attendees** dialog — you see the list of registered attendees, the limit, and the capacity. The organizer can:
  - **Remove** an attendee from the slot.
  - **Add an attendee manually** (search in the field and add). Manually assigned attendees are marked as **Assigned by organizer**.
  - Turn on **Notify attendee on manual assign/unassign** — the attendee then gets an e-mail when you add them to the slot or remove them from it; the e-mail about being added includes an ICS file if **Send ICS to attendee** is on. The toggle applies only to that slot and is off by default.

### Attendee flow

1. The attendee opens the session in the attendee app.
2. They see the **list of available slots** with occupancy (if showing remaining spots is turned on).
3. They tap a specific slot, which registers them.
4. The slot shows up in **My Agenda**.

### Showing slots directly in the agenda overview

By default, the attendee sees the slots only after opening the session detail. If you turn on **Expand time slots in the agenda** on the Agenda's **Settings** tab, the slots appear directly on the session card in the agenda overview — the attendee picks a time without opening the detail. This fits agendas where the slots are the core content (for example, test drives or consultations).

### Registration settings (same as for a Workshop)

A Time slot has the same set of registration settings as a Workshop:

- Assign attendee to a group after registration
- Registration only for selected groups
- Limit registrations (per **single slot**, not per session as a whole)
- Show the number of available spots
- Registration time limits (**Registration available from** / **until**)
- Session cancellation (**Cancellation available until**)
- Notify the organizer / attendee
- Send ICS to attendee

For details, see *Setting up workshops and session registration*.

### Capacity per slot

The default value of **Limit number of registrations** for a Time slot is **1** (one-on-one meeting). You can raise it — for example, to 3 per slot for a group consultation. Everyone registered for one slot arrives at the same time.

### Canceling a registration and freeing up the slot

When an attendee cancels their registration:

- The slot is freed.
- The spot becomes available for another attendee.
- Happenee does not have an automatic waitlist — the spot is not reassigned automatically.

If you configured **Session cancellation** on the session, its deadline applies here too: after it passes, the attendee can neither cancel the registration nor **switch to a different slot**. You have to make the change for them. So set the deadline with an eye on how long you want slot swapping to stay open.

### Multiple sessions of type Time slot

You can have **several sessions of type Time slot** in the Agenda at the same time (for example, *Consultation with the CFO* and *Consultation with the CTO*). Each session has its own slots. An attendee can register for slots from different sessions, but by default not for two slots whose times overlap. Overlapping slots are allowed only once concurrent registrations are turned on in the Agenda settings (see *Building the event Agenda — architecture*). Slots that merely follow one another do not overlap.

### Locked fields after the first registration

> After the first attendee registers for a Time slot session, you **cannot change**:
> - The session type
> - Start and end time
> - Time slot length
> - Break length

Plan these parameters in advance. You can add more time (for example, 12:00–14:00 as a second session), but you cannot edit existing sessions after a registration.

### Speaker assigned to the session (not to the slot)

A speaker is assigned to the session as a whole, not to a specific slot. Attendees in every slot see the same speaker / instructor. If you need to split slots between several speakers, create several sessions (one per speaker).

## Common pitfalls

### A 10-minute slot with no break — the system generates many slots, but the attendee cannot make it in, say hello, and start

The shortest slot length on offer is 10 minutes. The real slot length has to match the real interaction: a one-on-one consultation usually needs 15–30 minutes plus a short break (5 minutes) for handover.

### The organizer tries to change the session time after the first registration — the system blocks it

The slot start and end time are locked after the first registration. Plan the final schedule **before** opening registration. If you have to change it, cancel everyone's registration manually first, then edit, then open again.

### A Time slot session is created, but the attendee does not see slots — only one item in the Agenda

Check that the session uses a type based on Time slot and has a **Time slot length** set. The break can be 0 minutes; slots are generated without it. The **Slots** tab shows what the system has generated.

### Slot capacity is 1, but the attendee expects to sign up a group of three

Raise **Limit number of registrations** to 3. Note: everyone who registers arrives at the same time at the same slot. If you need more groups, create more sessions or split the time differently.

### An attendee cancels their registration and the organizer expects the system to notify the next person on a waitlist

Happenee does not have a waitlist today. The freed spot is available to everyone — the first person to click Register gets it.

### An inactive slot is reactivated, but the organizer forgets to add the canceled attendee back

Deactivating the slot canceled the registration, so after reactivation the attendee is no longer in the slot and does not come back automatically. You have to look them up and add them manually through the **Edit attendees** dialog. If they should learn about being added back by e-mail, turn on **Notify attendee on manual assign/unassign** for the slot first.

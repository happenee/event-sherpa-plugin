<!-- source: kb.en.06.02 -->

---
title: "Interpreting attendee statistics"
description: "Attendee statuses from the invitation to actual attendance, and how to read them for reporting and communication targeting."
modules: ["reporting_a_statistiky"]
last_updated: "2026-10-22"
version: 5
---

> [!info] Overview
> Attendee statistics show you who is in which status — from the moment an invitation is sent, through registration, to actual attendance on site. Attendee statuses are also filters for e-mail campaigns and Notifications, so reporting and communication targeting work with **the same data**. If you understand the statuses, you can act on who has not responded to what and decide what to do next.

## Getting started

Before you start reading the statistics, get clear on what you actually want to know:

- **Before the event** — how many people responded to the invitation, how many have registered, how many have the app.
- **On the day of the event** — who came, how many are missing against the registration count, and whether attendees are using the app.
- **After the event** — who attended, how many did not show up, and who downloaded the app but in the end did not come.

Based on that, open the right view: **Statistics → Attendee statistics** in the event's left menu, or the **Registration** section, which is a flat table with all statuses and filters.

## Details

### Key attendee statuses

- **Not responded** — The attendee has an invitation or access but has not responded yet
- **Attending** — They have completed registration (or the organizer set the status)
- **Not attending** — They declined the invitation
- **Pending approval** — Only with approved registration — the registration is in the queue and the organizer has to confirm it
- **Checked-in** — They went through check-in at the entrance
- **Left** — They were checked out at a check-out point (for events that track presence over time)

Statuses change either automatically (through registration or check-in) or manually (in the **Registration** section, the organizer can switch an attendee back to *Not responded* or remove them from the event entirely).

### Invitation e-mail responses

For invited contacts you track four values:

- **Sent** — the e-mail left the system
- **Opened** — the attendee opened the e-mail (this depends on whether the e-mail client allows tracking)
- **Responded** — they clicked a button or opened the microsite
- **Registered** — they completed the form (the status now flips to *Attending*)

These values are also **filters for an E-mail campaign** — for example, *"send a second wave to everyone who has not responded yet"*. See [Targeting communication by groups and statuses](../04_communication-and-invitations/05_targeting-communication-by-groups-and-statuses.md).

### Activity in the attendee app

A separate view (and a separate export) covers:

- **Who downloaded the mobile app** — by the e-mail address the attendee is signed in with
- **User activity in the app** — which attendees opened the event, which sections of the app they opened, when they were last active

For an internal company event this tells you how many people actually use the app. For a conference it helps you decide whether to push more content into the app.

### Filtering in the Registration section

The **Registration** section is a flat table of all attendees where you filter by status, group, preferred language, registration date, ticket, and other fields. The summary numbers in the statistics tell you *how many*; a filter in Registration tells you *who*.

A filter applies only to your current view — it is a working tool, not a view you hand over to colleagues. When somebody else needs to work with the same data, send them an **export** from **Statistics → Exports**.

### Quick manual edits

From the **Registration** page, an organizer can:

- Switch an attendee's status (for example, after a phone cancellation, manually move them to *Not attending*)
- Register the attendee **on their behalf** — the status flips to *Attending* and you can optionally send them a confirmation e-mail with a generated ticket
- **Remove** the attendee from the event entirely

These actions are logged and reflected in the statistics immediately.

### Sharing with management

Attendee statistics are visible only from the admin. A particular view — *Attending* including companions, or *Checked-in* — cannot be shared through a link, just as the event statistics cannot. Anyone who needs the numbers and does not go into the admin gets them as an export from **Statistics → Exports**, or as a summary you prepare for them. See [Interpreting event statistics](01_interpreting-event-statistics.md).

## Common pitfalls

### You confuse "viewed the event" (icon or preview in the app) with "registered"

Viewing the event is just a signal of interest, not a commitment. Registration is the form or a confirmation click. For real planning numbers (catering, badges) work with the *Attending* status.

### After the event, you report on the number registered, not the number who actually came

For real attendance use the **Checked-in** status (in the app or in the scanning export). Registration = a commitment; attendance = the reality. Most events have a 10–30% gap between the two.

### You wait for someone in *Not responded* to react on their own

The *Not responded* status is the basis for a second wave of communication. Send an E-mail campaign targeted exactly at that status — much more effective than a blanket invitation to everyone.

### You only look at the totals, not at groups

Segment by group (employees / clients / VIP) — that gets you to questions like *"who from VIP has not confirmed yet"*, which the total view will not show.

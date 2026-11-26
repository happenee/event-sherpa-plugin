<!-- source: kb.en.04.10 -->

---
title: "Communication flow on the event day"
description: "The day-of communication sequence: a morning e-mail with the QR ticket, push notifications in the app, and campaigns for the unregistered."
modules: ["notifikace", "komunikace_a_pozvanky"]
last_updated: "2026-08-16"
version: 5
---

> [!info] Overview
> On the event day, communication shifts from pre-registration e-mailing to an operational layer: a **morning reminder with the QR ticket** sent as an E-mail campaign, **Notifications in the app** during the day (agenda changes, contest results), and a final **campaign for the unregistered** still sitting on the fence. The goal: shorten the check-in queue, keep attendees in the loop, and capture last-minute decisions. The communication has to be prepared in advance — the event day is no time for copywriting, only for triggering the scheduled sends.

## Getting started

- Prepare a **timeline of communication** the day before: the morning e-mail (T−1 h before doors open), notifications during the day, and an optional thank-you note after the event (that is the follow-up — see *Planning follow-up communication after the event*).
- Schedule an **E-mail campaign with the PDF ticket and QR** for the morning of the event. Goal: the attendee has the ticket on top of the inbox, not buried.
- Prepare **Notification templates** in the attendee app — at least one welcome message, one for an agenda change, one for results / contest outcomes.
- Have a **fallback plan for the unregistered**: a final campaign the day before the event for those who have not signed up yet.

## Details

### The morning e-mail with the QR ticket

By default the attendee receives the QR ticket in the **Confirmation e-mail** right after registration and has it in the attendee app under tickets. The problem: if they registered weeks or months ago, the e-mail has buried itself in the inbox. On the event day they arrive at the entrance and search for it in the queue.

The fix: **on the morning of the event, send an E-mail campaign with a fresh PDF ticket and QR code**. Configure the campaign like this:

- **Targeting:** *Attending*. So not the unregistered, not the declined — only those who will arrive.
- **Content:** a short text along the lines of *"we see you today, here is your ticket, have it ready at the entrance"*, and any logistical info (parking, entrance, registration time).
- **Attachment:** in the campaign settings enable **PDF ticket with QR code**. The system generates a unique PDF for each contact.
- **Schedule the send** typically **1 hour before doors open**, not earlier (so the e-mail sits at the top of the inbox when the attendee leaves for the event).

### Notifications in the app during the day

For attendees with the attendee app installed, **Notifications** are faster and less intrusive than e-mail. Use them for:

- **Morning welcome** — *"Welcome to the event, registration opens at 9:00 in the main foyer."*
- **Agenda changes** — postponing a session, moving to a different room, a speaker no-show.
- **Announcing results** — a contest, a poll, a networking leader.
- **Reminders** — *"Networking break starts in 10 minutes in room A."*

Notifications have two delivery paths: a **push notification** (popping up on the lock screen) and an entry in the *News / Notifications* feed inside the app. Details in *Using Notifications in the attendee app*.

Prepare Notification templates **in advance** — there is no time to write them on the event day. A non-final draft is enough; you tweak it before sending based on the situation.

### A campaign for the unregistered — the last attempt

If the day before the event you still have *unregistered* people in the contact list (they have an invitation but did not register), a final **E-mail campaign the day before** typically converts 5–15 % of them. Set targeting to *Unregistered* or *Did not open the Invitation e-mail*. Body: a short reminder of why they should come and a registration button leading straight to the form. You can also target those who **did not open the attendee app** (mobile or web).

If the event uses paid tickets and registration closes the day before, schedule this campaign **before the deadline**, not after it.

### The sequence: a recommended timeline

Most events get by with this sequence on the event day:

1. **T−24 h** — campaign for the unregistered (last attempt, if registration is still open).
2. **T−1 h** — campaign with the PDF ticket and QR for everyone attending.
3. **T+0** (doors open) — welcome Notification in the app.
4. **Throughout the day** — Notifications about agenda changes / results / break reminders.
5. **T+end of event** — short thank-you note and an announcement that follow-up is coming (covered in a separate article).

### What to do when an attendee has no QR

There is no avoiding it on the event day — someone arrives without a QR (did not install the app, did not open the e-mail, deleted it). For these cases the **Check-in tool** (web) and the **Service app** are ready:

- A staff member in Check-in finds the attendee, resends the ticket via e-mail (the *Resend* button), or checks them in manually.
- The Service app also supports **quickly adding a new attendee** (first name + last name) if someone arrives who was not in the original list.

Details in *How check-in and QR-code scanning work*.

## Common pitfalls

### A morning campaign scheduled for 7:00 reaches attendees already on their way and out of signal

Schedule the send so the attendee gets the e-mail **with enough lead time before the trip**. T−1 h is often too late. For a 9:00 event, consider sending at 7:00 or even the day before in the morning if the trip takes ≥ 1 h.

### A campaign with the PDF ticket goes out to people who unregistered or did not show up

Target explicitly on the *Attending* status, not on *All*. Without targeting the campaign goes to those who canceled or never replied, and confusion follows.

### A Notification in the app fires before the event but the attendee has not signed in yet, so the push never shows

A push notification requires the attendee to have the app installed and to have signed in at least once. If you need to reach those who have not opened the app, use an **E-mail campaign** instead of a Notification (or both in parallel).

### An agenda change sent as a Notification with a long lead time loses attention — by the time it matters, the attendee has missed it

Critical changes (a speaker no-show, a room move) go out **just before the moment** they take effect. A Notification with a 6 h lead time gets lost; one with a 10-minute lead time the attendee actually registers.

### The event day suddenly turns into a copywriting workshop because templates are not ready

The event day is for **triggering sends**, not for writing them. Have all e-mails and Notifications prepared in advance, ideally with a buffer for last-minute tweaks. On-site operations cannot afford long texts written on the fly.

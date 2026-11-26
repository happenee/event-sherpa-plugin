<!-- source: kb.en.05.01 -->

---
title: "How check-in and QR-code scanning work"
description: "Checking attendees in with the Service app (QR scanning, the Attendees list, and Kiosk mode) and with the web Check-in tool."
modules: ["checkin_a_tisk_jmenovek"]
last_updated: "2026-11-04"
version: 9
---

> [!info] Overview
> Check-in is the moment an attendee physically arrives and you record their arrival. Happenee handles it in two ways — the mobile **Service app (Happenee Service App)** on a phone or tablet and the web **Check-in** tool in the admin. The Service app now has two modes: **Staff mode** (event staff scan QR codes *or* check attendees in straight from the **Attendees** list by name) and **Kiosk mode** (self check-in, where the attendee scans their own ticket). Check-in takes under a second, can print badges over Bluetooth, and tracks arrivals in real time. You can open the check-in settings under **On-site check-in** in the event admin's left menu, even without an active QR ticket module. In the check-in settings, you select which groups appear after a scan and in the attendee detail; the attendee must also belong to those groups.

## Getting started

- Open the check-in settings by selecting **On-site check-in** in the event admin's left menu. The menu item is available without an active QR ticket module, so you don't have to turn on the QR ticket in the attendee app just to set up check-in.
- Decide **how many check-in points** you will run (one entrance, several entrances, coat check, workshop room, shuttle bus) and what **behavior** each point needs — see *Place types for check-in* below.
- Decide **which groups** you want shown during scanning (VIP, Speaker, ticket type) and whether each one shows everywhere or only at selected places — configure them in advance in the check-in setup in the admin.
- Order **event staff accounts** through customer success if on-site staff need their own sign-in beyond the admin — this is not self-service, so arrange it with lead time.
- Download the **Service app (Happenee Service App)** — for iOS from the [App Store](https://apps.apple.com/app/id6499516161), for Android from [Google Play](https://play.google.com/store/apps/details?id=com.happenee.serviceapp2). Sign in and test it: pick the event, choose **Staff mode** or **Kiosk mode**, select the **Check-in place**, and pair a printer (see [Printing badges](02_printing-badges.md)).
- For attendees without a QR code who need the ticket resent or the QR shown, keep the web **Check-in** tool ready at the entrance — see below.

## Details

### Two environments for check-in

**Service app (Happenee Service App)** — the mobile tool for on-site staff on a phone or tablet. It scans QR codes, checks attendees in from a list by name, prints badges, and can run an unattended self-service mode. Sign-in works under an admin account; for separate **event staff accounts**, contact customer success.

**Check-in tool** — the web tool in the event admin (UI label *Check-in*). Open it on a laptop from the event's tools. It handles manual check-in and two things the Service app does not yet do: **resend the ticket by e-mail** and **show the QR code on screen**. That is why it still has a place at the entrance (see *Attendees without a QR code* below).

### Launching the Service app: mode, place, printer

After signing in, pick the event from the list. For the event you choose a **mode** and a **place**:

- **Staff mode** (*"Scan QR codes"*) — operated by event staff. Scans QR codes and checks attendees in from the list.
- **Kiosk mode** (*"Self check-in"*) — an unattended station where the attendee checks themselves in.
- **Check-in place** — pick one of the places configured in the admin (each has its own behavior type, see below). The app shows place names, not their types.
- **Printer** — optionally pair a badge printer (see [Printing badges](02_printing-badges.md)). Check-in works without one; it just does not print.

Confirm with **Continue**. You can switch the mode or place at any time (through *Switch event* in *Settings*, or back on the selection screen).

### Staff mode — the Scan tab

The bottom **Scan** tab is the classic QR scanner (*"Scan attendee QR code"*). It reads the QR from the confirmation e-mail, the PDF ticket, or the **QR ticket** feature in the attendee app. After each scan the app shows the result:

- **a successful check-in** — and, with a paired printer, offers to print the badge,
- **an *Already checked in* warning** (a duplicate scan at a *Check-in* place), with the option to open the attendee's detail,
- an ***Invalid ticket / Unknown code*** result, with the option to **Enter attendee manually**.

A **checked in today** counter runs at the top, with **Recent scans** and the printer status (*"No printer connected"* until you pair one) below.

### Staff mode — the Attendees tab (check-in by name)

The bottom **Attendees** tab is a **live list** of every attendee — this is where you check in someone who does not have a QR code at hand. It lets you:

- **Search** by name or e-mail and filter by **All / Checked in / Pending** (plus sorting and a group filter).
- **Check in with a swipe** — swipe a row to **Check in**, or to **Print badge**, without opening the detail.
- **Add attendee** — register a walk-in who is not on the list right in the app (e-mail, first name, last name, company, job, tags). Once saved, you can check them in and print a badge.
- Open the **Attendee Detail** with **Check in** and **Print badge** buttons, an organizer **Note**, a **Details** section (editable through **Edit attendee**), a **Check-in places** overview (where and when they were checked in, by whom, and the scan number), and a **Scans at this event** history.

Each row shows the attendee's RSVP status (*Attending* / *Not responded*) and whether they are checked in.

### Place types for check-in

A single check-in point is rarely enough. At larger events you check attendees in at several places — venue entrance, coat check, catering, workshop access. Each **place** is assigned a **type** in the admin that matches the behavior you need:

- **Check-in** — the standard entrance. After scanning, the attendee is *Checked-in*; a second scan of the same QR warns that they have already arrived. *(Main venue entrance.)*
- **Check-out** — leaving the venue or a part of the event. The status switches to *Left*, the arrival record stays, and a *Check-in* place can check them in again. *(Leaving the party, ending a block.)*
- **One-time check** — a single verification; any further attempt warns that the check already happened. *(Voucher or gift pickup.)*
- **Recurring check** — repeated scanning with no limit. *(Zone access, shuttle-bus boarding, attendance.)*

You can combine the types at one event. On-site staff pick **which place** they are stationed at in the Service app.

### Showing groups during scanning

In the event admin, open **On-site check-in** and, in the **Display attendee group after scanning** setting, select the groups that staff should see (for example *VIP*, *Speaker*, or *Standard*). **The same selection controls the groups shown after a scan and in the Attendee Detail in the Service app.** Only selected groups assigned to that attendee appear. Other workspace groups do not appear automatically; creating a group or assigning it to a contact is not enough. Without a group selection, none of these group indicators appear.

During scanning, you can limit a group's display to selected **places** (the *Show on places* field). An empty place selection means every place. **The Attendee Detail does not apply the place restriction:** it shows all groups assigned to that attendee and selected for display, regardless of the current check-in place.

Place restrictions help where staff should not see everything after a scan. At the main entrance, *VIP* and *Speaker* make sense; at a hall door, only the group that is allowed in.

Groups are populated manually (in Contacts and groups, on import) or automatically (by ticket assignment, a Registration form answer, workshop registration, or a discount code). Details in [Working with groups and visibility](../02_event-setup-and-registration/07_working-with-groups-and-visibility.md).

### Kiosk mode — self check-in

In **Kiosk mode** the attendee checks themselves in. The mode is designed for display on a **tablet** mounted on a stand at the entrance: the app prompts the attendee to hold the QR code in front of the camera; after a successful read it confirms their name (and, for a paid event, the ticket type and any companion), prints the badge automatically, and returns to the scanner after a few seconds for the next person. If the scan fails, it asks the attendee to see a staff member.

Use it where you want to shorten the line at the staff desk. It needs a reliable printer, a stable tablet stand, and a short instruction at the kiosk.

### Workshops and sessions — handled through groups today

A standalone check-in **for a specific workshop** or **time slot** is not yet possible — the Service app checks in per *place*, not per session. You handle it through **groups**: an attendee registered for a workshop is automatically in that workshop's group, you set the group to show during scanning and limit it to the workshop door only, you set that door as a *Recurring check* place, and staff see from the group whether the attendee is allowed in. A direct workshop check-in with its own attendee list is in preparation.

### Attendees without a QR code

Some people will not have the QR code at hand (deleted the e-mail, did not install the app, registered just now). You now check in most of them **directly in the Service app** — find them by name on the **Attendees** tab and check them in, or register a walk-in with **Add attendee**.

Keep the web **Check-in** tool at the entrance for what the app cannot do: **resend the ticket by e-mail** and **show the QR code on screen** (the attendee or a neighboring station then scans it). For the full procedure, see [What to do when an attendee without a QR is stuck in the queue](../08_troubleshooting/06_what-to-do-when-an-attendee-without-a-qr-is-stuck-in-the-queue.md).

### Exporting scans

From the check-in setup in the admin you can export **the full list of scans** (who, when, at which place) and **per-attendee statistics** (who arrived, who did not, repeat scans). This is useful for post-event reporting and for monitoring the on-site flow.

## Common pitfalls

### The wrong mode or place is selected at the start, and check-ins are recorded somewhere other than expected

Before the first attendee, confirm you have the right **mode** (*Staff mode* vs *Kiosk mode*) and, above all, the right **Check-in place** — a scan counts toward the place that is selected. With several entrances, assign each station its own place and type (main entrance = *Check-in*, a repeated zone = *Recurring check*, a single handover = *One-time check*).

### A staff member arrives on event day and cannot sign in to the Service app under their own account

Event staff accounts are turned on by customer success — it is not self-service. Arrange them **with lead time**, at least a week ahead. As a fallback, staff can sign in under an admin account, but you lose a separate audit of who checked whom in.

### The organizer expects to see group membership during scanning, but nothing shows up

Check that the attendee belongs to the group and that the group is selected for display in the check-in settings. The same selection applies to the **Attendee Detail** in the Service app. If the group is missing only from the scan result, also check its place restriction; the attendee detail does not apply place restrictions.

### The organizer wants to check in a specific workshop from its own list and looks for the option

This is not a native feature today — it is handled through groups (the attendee is in the workshop's group, staff see the membership at the door). A direct workshop check-in is in preparation.

### An attendee has no QR and staff expect to resend the ticket or show the QR in the app

The Service app can **find, add, and check in** an attendee, but it **cannot** resend the ticket or show the QR on screen. Handle those two in the web **Check-in** tool — keep it open on a laptop at the entrance.

### The badge printer jams while attendees are waiting

Keep a backup printer and a backup roll of badges. The most common cause is the wrong badge size — see [Printing badges](02_printing-badges.md).

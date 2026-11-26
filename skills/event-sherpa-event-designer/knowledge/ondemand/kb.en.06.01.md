<!-- source: kb.en.06.01 -->

---
title: "Interpreting event statistics"
description: "Where to find event statistics (invitations, registrations, attendance) and how to read them."
modules: ["reporting_a_statistiky"]
last_updated: "2026-08-07"
version: 3
---

> [!info] Overview
> Event statistics are your main view of how an event is doing — before, during, and after it. You will find them in several places: on the event card in the workspace event list, on the event **Overview**, and in the **Statistics** section in the left menu. Key statuses (invitations, registrations, attendance) and charts are available **only inside the admin**. When someone needs the numbers and cannot get into the admin, send them an **export** to Excel or CSV.

## Getting started

Decide up front who needs what information and how often:

- **For day-to-day work in the organizer team** — open **Statistics** directly from the event's left menu. You have full detail there.
- **For management or colleagues without admin access** — download an **export** from the **Statistics** section and send them the file. There is no way to share a live view of the statistics outside the admin.
- **For a quick daily glance** — track the statistics on the **event card in the workspace list**. You see the summary for every event without having to click through.

## Details

### Event card in the workspace

On the main screen after you log in (the event list), each event shows:

- Name, date, days until start
- Which content and engagement features the event has turned on
- Active languages
- Registration status (how many people are in which status)
- Clickable statistics — **invitations**, **registrations**, **who attended**, **who viewed the event**, **who has the mobile app downloaded**

You can click each statistic and go straight to the detail. You also typically see counts like *Attending + companion*.

### Event Overview

When you click into an event, **Overview** opens first in the left menu. It is the event's home page in the admin, with tools and statistics. Besides basic information about the event, you will find:

- Quick links to *Contacts and groups*, *Registration*, *Check-in*, *Orders*, *Nominations*
- A link to **Attendee statistics** and **Ticket statistics** (the second one only if you have Tickets turned on)
- A short summary of the individual sections in the left menu (settings, content, engagement, communication, tickets, on-site check-in)

Use Overview as your daily starting point, not as the place for deep reporting.

### Statistics section in the left menu

It contains four areas:

1. **Attendee statistics** — statuses, who viewed the event, who has the app. See [Interpreting attendee statistics](02_interpreting-attendee-statistics.md) for detail.
2. **Ticket statistics** — only for paid events. Covered in detail in [Setting up Tickets](../02_event-setup-and-registration/10_setting-up-tickets.md) (statistics section).
3. **Charts** — invitation e-mail responses, attendance, registration over time. The product author explicitly says *"more charts and statistics will keep being added"* — if something is missing, it is likely coming in the future.
4. **Exports** — to Excel/CSV, including scanning logs, form responses, and the list of app users. All exports are described in [Working with Orders and exports](03_working-with-orders-and-exports.md).

### Getting the numbers out of the admin

Statistics are part of the admin, so anyone without admin access cannot see them. There is no public or read-only link that would let you share a particular statistics view with the outside world.

When management, sales reps, or colleagues outside Happenee need the numbers, you have two routes:

- **An export to Excel or CSV** — under **Statistics → Exports**. You send the file and the recipient works with it on their own. All exports are described in [Working with Orders and exports](03_working-with-orders-and-exports.md).
- **Your own summary** — for regular reporting (a weekly registration status for management), a short overview of the numbers works better than a raw export. An export contains personal data of the attendees, which the recipient usually does not need.

Keep in mind that an export is a **snapshot taken at the moment of download**. Anyone who needs the numbers continuously has to ask for a new export — or you send it to them on a regular schedule.

### Where the statuses come from

Statistics are not counted by hand — they are a direct reflection of:

- **Invitation e-mails** — sent, delivered, opened, responded
- **Registration form** — completed registrations
- **Campaigns** — send statistics in the campaign detail, see [Creating and sending an E-mail campaign](../04_communication-and-invitations/03_creating-and-sending-an-e-mail-campaign.md)
- **Service app / Check-in** — who came in and when
- **Attendee app** — who has the app downloaded and signed in

When a number does not look right, start by checking whether the source (campaign, check-in, app) is set up correctly.

## Common pitfalls

### You only look at event statistics after the event

The main value is during the event. The benefit of statistics before the event is that you can react — for example, if five days before the date you see that half of the invited contacts have not opened the e-mail, you can send a second reminder wave.

### You promise management a link to the live statistics

Statistics cannot be shared through a link — they are visible only from the admin. Agree on an export instead: send the file from **Statistics → Exports**, or settle on a regular rhythm (for example, a short summary of the numbers once a week).

### You wait for a reporting feature that is not there yet

The product author explicitly says that charts and statistics keep being added. Some of what you might imagine (for example, a detailed analysis of the registration curve) is not in the UI today — work with what is there, and handle missing views with Excel exports.

### You rely on the event-card statistics as your only source

The event card is a quick overview. For detailed analysis (filters by group, segments) go to the **Statistics** section in the event's left menu.

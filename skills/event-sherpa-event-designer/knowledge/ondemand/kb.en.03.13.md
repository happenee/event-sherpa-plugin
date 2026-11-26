<!-- source: kb.en.03.13 -->

---
title: "Managing Exhibitors"
description: "A content feature for exhibitor profiles with locations, tags, representatives, and assigned sessions."
modules: ["networking", "sponzori_a_vystavovatele"]
last_updated: "2026-09-02"
version: 5
---

> [!info] Overview
> Exhibitors is a **content feature** that gives every exhibitor their own profile with a description, representatives, contacts, and assigned sessions. Unlike Sponsors, the **category is not required**, but it makes filtering easier. You can assign **locations** (a booth or a sector) and **tags** (a field, a topic) to an exhibitor — attendees filter by them in the app. **Representatives** are event attendees assigned to an exhibitor — they appear on the exhibitor profile and you can communicate with them through Networking.

## Getting started

- Map the **structure of the trade show or expo** — fields, halls, booths. Use that structure to choose categories, locations, and tags.
- If an exhibitor has **representatives** (booth staff), add them as event attendees first. Only then can you assign them to the exhibitor.
- Prepare exhibitor logos (PNG / JPEG / GIF, recommended width 800 px, aspect ratio 16:9, max. 500 KB).
- Decide on the **sort order** — manually, by exhibitor number, or alphabetically.

## Details

### Adding the Exhibitors content feature

1. In the left menu go to **Content** → **+ Add** → **Exhibitors**.
2. The content feature is added and the tabs **Exhibitors**, **Categories**, **Locations**, **Tags**, **Settings**, and **Import** become available.

> The Exhibitors content feature can be added **multiple times**. Each instance has its own list, categories, locations, and settings.

### Creating an exhibitor

The **New exhibitor** side panel has four tabs — **Settings**, **Content**, **Representatives**, and **Sessions** — and all of them are available right when you create the exhibitor. You can fill in the profile, contacts, representatives, and assigned sessions in a single pass before the first save; the same tabs are available later when you edit the exhibitor.

1. On the **Exhibitors** tab click **New exhibitor**.
2. On the **Settings** tab enter the **Exhibitor name** (required field).
3. Optional: **Exhibitor number** (booth identifier), **Category**, **Location**, **Tag**.
4. Optionally upload a **Logo** (PNG, JPEG, GIF; recommended width 800 px; aspect ratio 16:9; max. 500 KB).
5. Optionally switch to the **Content**, **Representatives**, and **Sessions** tabs to fill in the rest of the profile (see below). You can also do this later.
6. Save: **Save** stores the exhibitor; **Save and publish** also publishes it right away (status *Published*). Both buttons are shared across all tabs, so the whole exhibitor is saved at once.

### Exhibitor profile content

On the **Content** tab fill in:

- **Exhibitor description** — formatted text (bold, italics, lists, quotes, images).
- **Website** — URL (starts with `https://`).
- **E-mail**, **Phone** (country code + number).
- Social networks: **LinkedIn**, **Twitter/X**, **Instagram**, **Facebook**, **YouTube**.

### Exhibitor representatives

Representatives are event attendees assigned to an exhibitor:

1. Open the **Representatives** tab.
2. In the **Search attendees** field find a person (they must already exist among the event attendees).
3. Add them.

Representatives appear on the exhibitor profile and in **Networking** they are marked as *Exhibitor*. Other attendees can connect with them and arrange a meeting **at the exhibitor's booth** — the booth serves as the meeting location, bound to a specific representative. A meeting at the booth cannot be arranged with anyone other than a representative of that exhibitor.

For meetings between attendees not tied to an exhibitor, separate **predefined meeting locations** (for example, *Meeting table #1*) are used — see the article *How Networking works*. These locations are set up by Happenee customer support, not by the organizer in the admin interface.

> Meeting bookings (at booths and at predefined locations) are part of Networking — see *How Networking works*.

### Categories, locations, tags

**Categories** — group exhibitors by field. Each category has a **Category color** that is shown next to the assigned locations. The first time you open the Categories tab it is **empty** — there are no pre-filled defaults (a difference from Sponsors).

**Locations** — physical spaces (a hall, a booth, a sector). Each location has a **Location color**. Assigning a location to an exhibitor helps the attendee find them at the event.

**Tags** — topical labels (*Fintech*, *AI*, *Green tech*) assigned to an exhibitor. Each tag has a **Tag color**.

All three are **optional** — an exhibitor can exist without a category, a location, or any tags.

**The order of categories, locations, and tags** can be changed by dragging the icon on the left in the table **without restrictions**. (For exhibitors themselves, the order can only be changed inside the same category and only when *Sort order: Manual* is set.)

**Bulk actions on categories:** select one or more categories in the list and in the bulk action bar use **Display on the app home screen** (on/off) or **Status** (Published / Hidden). A hidden category hides every exhibitor inside it — they will not appear in the app or on the microsite until you make the category visible again.

### Assigning exhibitors to sessions

If an exhibitor runs a session (a presentation, a workshop, an exhibit), you can assign them to sessions in the Agenda. The session then shows the exhibitor logo with a caption (default *Hosted by*; you can change it in Settings).

1. Open the **Sessions** tab.
2. In the **Search sessions** field enter the session name and add it.

### Exports — QR codes, PDFs, and scan statistics

On the **Exhibitors** tab in the upper right there is an **Exports** button with a dropdown menu:

- **Export exhibitor QR codes (Excel)** — a table with unique QR codes for every exhibitor. Useful for further processing (printing, embedding into booth graphics).
- **Export exhibitors (PDF)** — a batch PDF export of exhibitor cards with QR codes, ready for bulk printing and placement on booths.
- **Export scan statistics (Excel)** — statistics of attendees scanning exhibitor QR codes (who scanned whom and when). Useful for post-event reporting and evaluating booth traffic.

You can also open a single QR code straight from the exhibitor row — click the **QR code icon** next to the edit icon. An **Exhibitor QR code** dialog opens with a preview of the code, a **QR TEXT** field (the exhibitor's unique code), and a **Download as PDF** button for downloading a single code.

The QR codes work like this: the attendee scans the QR on the booth with their phone and adds the exhibitor to a favorites list, or connects with the exhibitor's representatives through Networking.

### Settings

On the **Settings** tab:

- **Display of exhibitors in the Agenda** — **Caption next to the exhibitor logo** (default: *Hosted by*).
- **Display on the attendee app home screen** — *Basic display* or *Image* (JPG 1250×300 web / 800×300 mobile).
- **Display on the microsite home page** — *Basic display* or *Display from the attendee app*.
- **Sort order of exhibitors:**
  - **Manual** — drag the icon in the table (only inside the same category).
  - **By number** — by *Exhibitor number* (records without a number end alphabetically at the bottom).
  - **Alphabetical** — by exhibitor name.

### Filters in the app and on the microsite

**Categories**, **Locations**, and **Tags** automatically appear as filters in the app and on the microsite. Attendees can combine filters and find exhibitors across multiple dimensions.

### Bulk actions

Select multiple exhibitors and in the bulk action bar use:

- **Category** — assign or change.
- **Location** — assign or change.
- **Tags** — add or remove.
- **Status** — publish or hide.
- **Find logos** — automatically look up logos from the exhibitors' websites (the **Automatic logo lookup** dialog, see below).
- **Delete exhibitor.**

### Automatic logo lookup

If exhibitors have the **Website** field filled in, Happenee can try to look up their logo directly from their website — handy when you are setting up dozens of exhibitors and do not want to upload logos by hand.

1. Select exhibitors and run the **Find logos** bulk action.
2. In the **Automatic logo lookup** dialog, each exhibitor shows the found **Logo**, a **Source / reason** column (for example, *Logo found in a page image*), and a **Status**: **Found**, **Skipped, logo already exists** (a logo is already uploaded), or **Missing website** (no URL filled in).
3. In the **Use** column, tick the logos you want to keep and confirm with **Apply selected logos**.

### Multiple languages

The language switcher lets you translate:

- The exhibitor description
- The category name
- The tag name
- The location name
- The caption next to the exhibitor logo

The exhibitor name is typically not translated.

### Importing exhibitors from Excel

You can create exhibitors in bulk from Excel through the **Import** tab — a five-step wizard (upload, column mapping, assigning categories and locations, preview, results). Only the **Name** is required; category and location values from the file are assigned to existing ones or created as new. Logos, representatives, and tags are not set by the import — logos are fastest to add afterward with the **Find logos** bulk action. The full walkthrough, template, and limitations are in [Bulk import of exhibitors](23_bulk-import-of-exhibitors.md).

## Common pitfalls

### An exhibitor with no category, location, or tags is hard to filter, so attendees cannot find them in the app

Even though the attributes are optional, every exhibitor should have at least **one filter** (a category or a location). Without filters, an attendee will get lost in 50+ exhibitors.

### A URL is missing the `https://` prefix and the link in the app does not work

Always start the URL with `https://`.

### An auto-found logo can be wrong — always check it

The Automatic logo lookup takes an image from the exhibitor's **Website** and may not pick the right logo (it can grab a different image from the page). In the **Automatic logo lookup** dialog, review the previews and keep only the logos that fit. Exhibitors with no URL end up with the **Missing website** status — add their logo manually.

### A representative is added but is not an event attendee, so the system cannot find them

The representative must be **among the contacts assigned to the event**. If they are not, add them through contact management first.

### The Sessions tab is missing because the Agenda content feature is not active in the event yet

Add the Agenda to the event Content. The tab will then become available.

### The exhibitor order does not match expectations because the system ignores the manual arrangement

A manual drag is only respected when **Sort order: Manual** is set on the Settings tab. If you want a manual order, check the setting.

### Category and location colors are too similar and attendees cannot tell the filters apart

Choose **contrasting and distinct** colors. Categories are usually 3–6, locations 5–10 — the colors should be clearly distinguishable.

### Representatives are not informed that they have been assigned and do not know they should be available for meetings

Happenee does not send an automatic notification to the representative. Communicate manually — by e-mail, Slack, or in person. Build a checklist for your internal team. A representative who has not set their available time slots in the app is visible in Networking, but a meeting at the booth cannot be booked with them.

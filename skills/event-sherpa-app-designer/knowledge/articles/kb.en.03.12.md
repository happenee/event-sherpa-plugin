<!-- source: kb.en.03.12 -->

---
title: "Managing Sponsors"
description: "A content feature for displaying event partners with their logos in categories by prominence."
modules: ["sponzori_a_vystavovatele"]
last_updated: "2026-09-02"
version: 3
---

> [!info] Overview
> Sponsors is a **content feature** that displays the event's partners with their logos on the microsite and in the attendee app. Every sponsor belongs to a **category** (General sponsor, Gold, Silver) — the category sets the prominence and how many logos appear in a single row. A click on the logo can open the **sponsor's external website**, the **sponsor's profile** (description, contacts, social networks), or do **nothing**. Sponsors can also be assigned to sessions in the Agenda.

## Getting started

- Map the **sponsorship structure** — which levels you have (General / Gold / Silver / Media) and what benefits each level provides (number of logos per row, prominence, assignment to sessions).
- Prepare **sponsor logos** in a consistent format (PNG / JPEG / GIF, 16:9 ratio, max. 500 KB).
- Decide on the **click action** — external website, in-app profile, or no action.
- Decide where the category appears — **on the home screen of the microsite or attendee app**, or only inside the Sponsors section.

## Details

### Adding the Sponsors content feature

1. In the left menu go to **Content** → **+ Add** → **Sponsors**.
2. The content feature is added and the tabs **Sponsors**, **Categories**, **Settings**, and **Import** become available.

> The Sponsors content feature can be added **multiple times**. Each instance has its own sponsors, categories, and settings. This works well for separate sections such as *Conference partners* vs. *Media partners*.

### Categories are required

Every sponsor **must belong to a category**. Without a category the sponsor cannot be saved. The first time you open the **Categories** tab, **four default categories are pre-filled**: *General sponsor*, *Gold sponsors*, *Silver sponsors*, *Media sponsors*. You can edit, hide, or delete them (if they do not contain any sponsors).

### Creating a category

1. On the **Categories** tab click **New category**.
2. Enter the **Category name**.
3. In the **Display level** field choose **1**, **2**, or **4** — the number of logos in a single row. A category with level 1 has the highest prominence (one large logo), a category with level 4 has smaller logos.
4. Use the toggle **Display on the home screen of the microsite and attendee app** to set whether the category appears on the home screen or only inside the Sponsors section.
5. Save.

**Sorting categories:** the order is driven by the **Display level** value. Level 1 = first in order, level 4 = last. For finer control over the order, name the categories so they are distinguished by their level.

### Creating a sponsor

1. On the **Sponsors** tab click **New sponsor**.
2. Enter the **Sponsor name**.
3. Select a **Category** (required).
4. In the **Click action on the logo** section choose:
   - **Sponsor website** — clicking takes the attendee to the external website. The **Website** field appears (the URL must start with `https://`).
   - **Sponsor profile** — opens the profile inside the platform. Fill in **Sponsor description**, **Website**, **E-mail**, **Phone**, and optionally social networks (**LinkedIn**, **Twitter/X**, **Instagram**, **Facebook**, **YouTube**).
   - **No action** — clicking the logo does nothing (purely visual display).
5. Optionally upload a **Logo** (PNG, JPEG, or GIF; 16:9 ratio; max. 500 KB).
6. Save.

### States

**Sponsor:**
- **Published** — appears in the sponsor list.
- **Hidden** — does not appear anywhere.

**Category:**
- **Published** — sponsors in it are visible.
- **Hidden** — every sponsor in the category is hidden.

> A sponsor is shown to attendees only when **both** — the sponsor and its category — are in the **Published** state.

### Assigning sponsors to sessions

You can assign sessions to each sponsor; the sponsor's logo then appears on those sessions with a caption (default: *Sponsored by*; you can change it under **Settings → Caption next to the sponsor logo**).

1. Open the sponsor for editing and go to the **Sessions** tab.
2. In the **Search sessions** field enter a name.
3. Click **+** next to the session you want.
4. Save.

> The Sessions tab is available only when the **Agenda** content feature is active in the event (Sessions is one of its tabs).

### Display settings

On the **Settings** tab you can configure:

- **Display of sponsors in the Agenda** — caption next to the logo (default: *Sponsored by*).
- **Display on the attendee app home screen** — *Basic display* (logos in a grid) or *Image* (JPG banner, 1250×300 web / 800×300 mobile, max. 500 KB). **Logo alignment**: left or center.
- **Display on the microsite home page** — *Basic display* or *Display from the attendee app home screen* (inherits the setting from the app). **Logo alignment**: left or center.
- **Display on the detail page** — logo alignment on the sponsor detail page: left or center.

### Bulk actions

On the Sponsors tab select multiple sponsors and use:

- **Category** — bulk change of category.
- **Status** — bulk publish or hide.
- **Delete sponsor** — bulk delete.

### Filtering in the admin vs. in the app

In the Sponsors admin you can filter the list with the **Category** and **Status** dropdowns — but **for internal management only**. In the attendee app and on the microsite, **sponsors are not filterable** (unlike Exhibitors, where categories, places, and tags act as filters for attendees). The attendee sees sponsors grouped by category in the order set by their *Display level*.

### Multiple languages

The language switcher lets you translate:

- The sponsor description (in the profile)
- The category name
- The caption next to the sponsor logo

The sponsor name is typically not translated (it is a company name).

## Common pitfalls

### A sponsor is added without a category and the system will not save it

First create a category (or use one of the defaults), then add the sponsor.

### A sponsor is set to Published but the category is hidden, so the sponsor does not appear in the app

Both must be in the Published state for the sponsor to be visible. Check the state of the category.

### A URL is missing the `https://` prefix and the link in the app does not work

Always start the URL with `https://`. Without the prefix the system will not redirect.

### A low-resolution logo looks blurry on a large display

Upload the logo at a minimum of 800×450 px (16:9 ratio). For logos with flat colors and text, use PNG; JPEG adds compression artifacts along the edges.

### Every category is set to *Display on the home screen* and the home screen is overcrowded with logos

Keep only the **top one or two categories** (General, Gold) on the home screen. Leave the rest accessible inside the Sponsors section through a click.

### The Sessions tab is missing on the sponsor because the Agenda feature is not active yet

Add the **Agenda** content feature to the event and create at least one session. The tab will become available.

### The order of sponsors inside a category is not what the organizer wants because the system follows the manually set order

On the Sponsors tab drag sponsors by the icon on the left into the right order. The order is respected in the app and on the microsite.

<!-- source: kb.en.03.02 -->

---
title: "Setting up Venue and the event location"
description: "A content feature that shows attendees where the event takes place, with a map and navigation."
modules: ["microsite", "lokalita", "ucastnicka_aplikace"]
last_updated: "2026-09-18"
version: 2
---

> [!info] Overview
> Venue is a **content feature** that shows attendees **where the event takes place**. It contains the place name, address, map, and optionally an image and description. It appears on the Event microsite and in the attendee app; in the mobile app, attendees start directions with the **Navigate** button on the Venue tile. Do not confuse Venue with the **Stages** inside the Agenda — Stages are individual rooms and booths, while Venue is the address of the whole event.

## Getting started

- Have the **exact address** of the venue ready (not just the name of the complex).
- If the event uses several buildings or halls, decide whether to communicate that in Venue (as text) or to use **Stages in the Agenda** (for sessions).
- Have the venue contact details ready (reception phone, website) — they are optional but help attendees.
- A venue image is optional but improves orientation.

## Details

### Where you set up Venue

1. In the left menu, click **Content**.
2. If Venue is not there yet, add it with the **+ Add** button → **Venue**.
3. Click the **Venue** tab and fill in the fields:

- **Place name** — for example *Prague Congress Centre*, *O2 arena*, *Hotel Corinthia*.
- **Phone** (optional) — contact for the venue's reception.
- **Website** (optional) — a link to the venue's site.
- **Address** — enter and **search**. Happenee converts the address into coordinates and renders the map.
- **Venue image** (optional).
- **Venue description** — text in the rich text editor. Use it for transport information, parking, how to get there, and special notices.

### How the attendee sees it

**On the Event microsite** — the Venue tab contains the address, the map (Google Maps embed), and the description. Tapping the address or the map opens navigation in the attendee's map application.

**In the mobile attendee app** — tapping the Venue tile on the home screen, including the address or map preview, opens the venue details. The **Navigate** button opens an external map app with directions to the venue. The button appears on the tile and in the venue details.

If the tile displays a map and the attendee’s location is available, the preview includes both the attendee and the venue, along with the route when available. The farther the attendee is from the venue, the wider the area shown. Without an available location, the map shows the area around the venue.

Travel time and distance appear only when route information is available. If the app has the attendee’s location but cannot retrieve the route, the map shows both points without a route or travel estimate. Granting location access alone therefore does not guarantee that a route will appear. The preview is not for turn-by-turn navigation; attendees use the **Navigate** button to start directions.

If you set a custom home screen image for Venue, the tile displays only that image — without the address, the map, or the **Navigate** button. Attendees tap the image to open the venue details and start directions from there.

### Multilingual content

Using the language switcher (the flags in the top right corner) you can translate:

- The place name
- The venue description

The address itself is not translated — there is one address shared across all languages. If you need to add a translation for a different spelling (for example, Czech and English for a foreign venue), put it in the **description**.

### The difference between Venue and Stages in the Agenda

- **Venue** (content feature) = the address of the whole event. One per event. Appears as its own tab on the microsite and in the app.
- **Stages in the Agenda** (a setting inside the Agenda) = individual rooms, stages, or booths to which specific sessions are assigned. They act as a filter. Details in the article *How registration blocks, stages, and tags work*.

For a one-day event in a single room, Venue alone is enough. For a conference with several parallel sessions in several rooms, use **both** — Venue for the address of the congress center, Stages for the individual rooms.

### Visibility

Venue can be:

- **Visible to all attendees** (the default).
- **Visible only to selected groups** — for example, when part of the audience has a different location (a VIP gala dinner at a different address). In that situation, however, it is usually better to create a separate event.

### When you do not need Venue

- **Virtual events** — there is no physical venue. Simply do not add Venue.
- **Incentive trips or itineraries with several stops** — the event moves through several locations. Use **Custom content** with a hand-built overview of the stops, or use the Agenda as an itinerary instead.

## Common pitfalls

### Only the name of the complex is entered, with no street address. The attendee's map application shows a different place with a similar name, or finds nothing

Always fill in the exact address, including street and house number. After entering the address, click **Search** and check that the system found the right place.

### The organizer uploads a low-resolution image of the venue grabbed from the venue's website, and it looks bad on the microsite

The venue image should be at least 1200×600 px in JPG or PNG. If you do not have your own, leave it blank.

### The venue description contains current information (parking, shuttles) that changes a week before the event, and by then the static description is too late to update

Information that may change should go through **Notifications** in the attendee app, not in the static venue description.

### Several buildings on the same site, but the venue description has only the address of the main building, and attendees get lost

In the venue description, state **exactly where to go** (entrance A, building 3, ground floor). For a conference with several rooms, also use **Stages** in the Agenda.

### The organizer sets up Venue for a virtual event, and attendees see a meaningless address

For virtual events, do not add the Venue content feature at all. Put the livestream link or the online location into **Custom content** or into the **Online module**.

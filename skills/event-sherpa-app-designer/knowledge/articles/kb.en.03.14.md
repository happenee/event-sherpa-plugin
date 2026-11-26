<!-- source: kb.en.03.14 -->

---
title: "How the attendee app and its home screen work"
description: "The environment where the attendee lives during the event, and how its home screen is organized."
modules: ["ucastnicka_aplikace"]
last_updated: "2026-09-16"
version: 4
---

> [!info] Overview
> The attendee app is the environment in which **the attendee lives during the event** — they see the agenda, receive notifications, talk to other attendees, and scan their ticket at check-in. It is available in three variants: the **iOS mobile app**, the **Android mobile app**, and a **web app** (in the browser). The content is the same across all three; only the form of display differs. The **attendee app home screen** is the opening screen the attendee sees after opening the event — it shows tiles for the most important modules and features (Agenda, QR ticket, My Agenda, Networking, Sponsors, Exhibitors, and others).

## Getting started

- Decide **whether to offer the app to the attendee** at all (recommended for medium and larger events) — see *Microsite vs attendee app* in collection 01.
- The home screen is built from the **content and engagement features you have turned on** in the event. The more features, the richer the home screen — and the higher the risk of overload.
- The order of content and engagement features on the home screen is set in the left menu under **Attendee app** by drag-and-drop.
- The display of an individual feature on the home screen can be customized — **text block** vs. **image**.

## Details

### Three variants of the app

**iOS / Android mobile app.** A native app the attendee downloads from the App Store or Google Play. By default Happenee publishes it under the **main Happenee brand** or under a **white label** brand for enterprise customers. Push notifications work.

**Web app.** Opens in the browser — the attendee does not have to install anything. They get the link in an e-mail or find it on the microsite. Push notifications work in a limited way (browser notification support).

> For **In-Person** events both the mobile app and the web app are available. For **Virtual** events only the web app. For **Hybrid** events both. This is set when the event is created (*Event type*).

### The attendee app home screen

The home screen is the opening screen the attendee sees after opening a specific event in the app. It contains a **list of features — tiles** with a preview of each content and engagement feature. Typically:

- **QR ticket** (engagement) — QR code for check-in.
- **Agenda** (content) — the nearest sessions.
- **My Agenda** (engagement) — the sessions the attendee saved or registered for. In the web app it appears above the Agenda tile only when you turn it on in the **My Agenda** tab of the Agenda; in the mobile app it always sits above the first Agenda.
- **Networking / Attendees** (engagement) — list of other attendees.
- **Sponsors / Exhibitors** (content) — logos and filters.
- **Notifications** (engagement) — news and push messages.
- **Venue** (content) — address and map.
- **Contact** (content) — contact for the organizer.
- **Custom content** (content) — FAQ, parking, dress code.
- **Leaderboard**, **Online module** (if active).

### Two layers of home-screen configuration

**Layer 1 — what is on the home screen.** Content and engagement features that are turned on appear on the home screen automatically. What is not turned on is not shown.

**Layer 2 — how a specific feature looks.** For each feature (content or engagement) you choose how it appears on the home screen:

- **Text block** — a heading and a short intro line. For example, *"Custom content: Parking and transport"*.
- **Image** — replaces the text preview with an image. The image is uploaded separately for the **mobile** and **web** display (the dimensions differ).

An image is a stronger visual but needs solid graphics. If you do not have them, leave the text block.

### Order of modules and features

Under **Attendee app** (left menu of the event) you see the list of features that are turned on. Drag by the icon on the left to rearrange. The attendee will see the features in the order you set.

**Recommended order for most events:**

1. QR ticket (quick access for check-in)
2. Agenda (main content; the My Agenda block has no position of its own and appears above it)
3. Notifications (updates)
4. Networking (interaction)
5. Venue (practical info)
6. Sponsors / Exhibitors
7. Other

### Visibility for groups

Visibility of individual features for groups is set on the **level of each content and engagement feature** (see *Working with groups and visibility*), not in the Attendee app section. In the Attendee app section you only set the **order** and the **publication** (turned on / off in the app).

### What the attendee needs for access

1. **Registration status: Attending** (or assignment to the event without registration, if the event runs without a registration form).
2. **Sign-in** in the app — by e-mail and a code, or via Magic Link.
3. **The downloaded app** (mobile) or the web version open.

If the attendee does not have the native mobile app installed, offer a link to the web version — some attendees do not download native apps.

### White label app

Enterprise customers can have their own mobile app in the App Store and Google Play under their organization's name. The content is the same, only the visual is branded. This is set up during enterprise account setup, not in the regular event admin.

### Difference vs. the microsite

- **Microsite** — the public page for the **pre-registration phase** and marketing sharing. The attendee opens it from an e-mail or a link and sees the agenda, speakers, sponsors, and the registration button.
- **Attendee app** — the environment for **attendees after registration**. The attendee app home screen contains a personalized view (My Agenda, ticket) that the microsite does not have.

Content between the microsite and the app is **shared** in Happenee — you fill in content features once and then decide where they appear. Details in *Microsite vs attendee app: how to think about the attendee flow*.

### Renaming features

In the detail of a content or engagement feature you can **rename** the feature — change the default name *Custom content*, *Sponsors*, etc. to anything. The new name flows through to the home screen.

## Common pitfalls

### The home screen is overloaded with 15 features and the attendee cannot find their way around

Turn on only features you fill with content. For a medium-sized event, six to eight features are enough. Empty tiles look unfinished.

### The home-screen image is uploaded only for desktop, and the mobile app shows an empty tile or the default view

Upload the image for **both variants** — mobile (smaller dimension) and desktop / web. If you upload only one, the other stays in the default.

### The attendee cannot sign in to the app — they enter their e-mail but the system does not find them

Check that the attendee has the status **Attending** for the event. If they are in *Not responded* or *Not attending*, they have no access to the app. For open events, check that the attendee is in your contacts.

### The organizer changes the order of features during the event and attendees get confused

Set the order of features before the event starts and do not change it during the event. Exception: if a change is necessary (a feature stopped making sense), communicate it through Notifications.

### Trying to put content into the app that is not a Happenee content or engagement feature (for example, an external page with materials)

Use **Custom content** with an external link — a tile appears on the home screen, and clicking it opens the external URL. For files (PDF), use the central **Files** storage in Workspace settings.

### The white label app is in the App Store, but the attendee downloads the main Happenee app and does not see the brand

For enterprise events, communicate the exact link to the white label app (usually under a specific name in the App Store). Link to it directly in e-mails and on the microsite.

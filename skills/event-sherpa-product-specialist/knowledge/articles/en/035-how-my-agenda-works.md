# How My Agenda works

> The attendee's personal schedule of saved and registered sessions, and the settings for the My Agenda block on the Agenda tab.

- Article in the Help Center: https://help.happenee.com/en/articles/35-how-my-agenda-works
- Česká verze: https://help.happenee.com/cs/articles/35-jak-funguje-moje-agenda
- Collection: Content and attendee experience
- Updated: 2026-09-16

---

> [!info] Overview
> My Agenda is an engagement feature of the attendee app: a personal schedule in which the attendee sees only the sessions they saved and the sessions they registered for. The attendee builds its contents in the Agenda; you do not fill it in from the admin. In the admin, the **My Agenda** tab of the Agenda only controls whether the My Agenda block appears on the attendee app home screen and how it looks.

## Getting started

1. In the event admin, open **Content**, select the Agenda, and go to the **My Agenda** tab. If the event has more than one Agenda, set up the block in only one of them.
2. Turn on **Show on event detail**. The toggle is off by default, and until you turn it on, the My Agenda block does not appear in the web app.
3. Under **Display on attendee app homepage**, choose **Basic display** or **Image**. For an image, upload both versions, for the mobile view and for the desktop view, and confirm each one with **Save**.

## Details

### What My Agenda contains

My Agenda combines two kinds of sessions from all Agendas of the event:

- **Saved** — the attendee marks a session in the Agenda with the bookmark icon. This works for any session, including a Keynote that has no registration. Saving does not reserve a spot.
- **Registered** — Workshops and Time slots the attendee registered for. They are added automatically. When the attendee cancels the registration, the session leaves My Agenda unless they also saved it.

Each attendee has their own agenda, and you don't fill it in or edit it. Only a signed-in attendee sees it.

### Where you set up My Agenda

My Agenda is not listed under **Engagement**, and you can't add it there. You set it up on the **My Agenda** tab of the Agenda (**Content** → Agenda), which has three settings:

- **Show on event detail** — whether the My Agenda block appears on the attendee app home screen. Off by default.
- **Display on attendee app homepage** — **Basic display** (the My Agenda heading with a bookmark icon) or **Image** (your graphic instead of the heading).
- **Images** — once you choose **Image**, two fields appear: an image for the mobile view (recommended size 800 × 300 px) and an image for the desktop view (1250 × 300 px). The recommended format is JPG up to 500 KB. The images are shared across all event languages.

The block has no position of its own on the home screen and no group visibility of its own. In the web app it sits directly above the tile of the Agenda where you turned it on, and it moves together with that tile.

### How the settings save

The toggle and the display option save as soon as you change them; there is no save button for them. If saving fails, the admin switches back to the previous value and shows an error.

Choosing a file does not save the image yet. After you pick one, you see a preview and the **Save** and **Clear selection** buttons, and the image is uploaded only when you click **Save**. To replace a saved image, use **Upload a different image** and confirm it with **Save** as well. **Remove** deletes the image right away after you confirm.

### What the attendee sees

**Web app.** If you turned the block on, it sits on the attendee app home screen above the Agenda tile. Clicking it opens the list of saved and registered sessions, split by day. Inside the Agenda, a signed-in attendee has a My Agenda link and a bookmark icon on every session, so they can reach their agenda even when the block is off.

**Mobile app.** If the event has an Agenda, the My Agenda tile always sits above the first one and shows the number of sessions in the agenda. The attendee also finds My Agenda in the app menu. Inside, they switch between the All, Saved, and Registered tabs. The mobile app does not use the settings from the My Agenda tab yet, so you can't turn the tile off there, and a custom image does not appear in it.

On a session detail, the attendee can rate the session or ask questions if you turned those engagement features on for it.

### ICS calendar file

If **Send ICS to attendee** is on for the session type or for a specific session, and *Notify the attendee when their session registration changes* is on as well, the attendee receives a confirmation e-mail with an ICS file after registering. They can import it into Google Calendar, Apple Calendar, or Outlook. My Agenda in the app and the external calendar then run side by side.

### Typical use cases

**Conference with parallel tracks.** The attendee registers for workshops and saves the keynotes they are interested in. Their agenda then shows their own schedule instead of the whole conference agenda.

**Reservations (test drives, social program).** A reservation is a registration for a Time slot, so it shows up in My Agenda with its time and place.

**Multi-day events.** My Agenda is split by day, and the attendee moves between the days.

### What My Agenda cannot do

- **Add a custom item** (a personal meeting outside Happenee) — it only shows sessions from the event's Agendas.
- **Export the whole agenda as a single file** — only individual sessions go to a calendar, via ICS.
- **Share the agenda with others** — it is purely personal.
- **Set the home-screen block per group or give it its own position** — it follows the Agenda tile.

## Common pitfalls

### The My Agenda block is missing from the home screen

**Show on event detail** is off by default, so the web app shows no block until you turn it on. A visitor who is not signed in never sees it. A signed-in attendee can still reach their agenda without the block, through the My Agenda link in the Agenda.

### My Agenda appears twice on the home screen

You set **Show on event detail** separately in each Agenda, and the block appears above every Agenda where it is on. All of these blocks open the same agenda with sessions from every Agenda. If the event has several Agendas and you don't want attendees to see the My Agenda block more than once, turn the toggle on in only one of them.

### The selected image was not saved

After you pick a file, you see a preview, but the image is not saved yet. If you close the page or leave it without clicking **Save**, the selected file is discarded and you have to pick it again.

### The block shows the basic display instead of the image

The web app uses the image only when both are uploaded, for the mobile view and for the desktop view. If one is missing, the block falls back to the basic display. Always upload both.

### The settings had no effect in the mobile app

The mobile app does not read the settings from the My Agenda tab yet. The My Agenda tile is always there in its basic form, even if you turned the block off or uploaded an image.

### You uploaded the image on a different tab

The tile image for the Agenda itself is set on the **Visibility** tab, and the image for the My Agenda block on the **My Agenda** tab. They are two different images, and one does not replace the other.

### My Agenda is empty in the app

My Agenda fills only with what the attendee saves or registers for, so an empty agenda is not a bug. Check that the attendee is signed in and that the sessions are published and visible to their group.

### A Keynote was not added to My Agenda

Attendees don't register for Keynotes, so Keynotes are not added automatically. The attendee adds one with the bookmark icon in the Agenda.

### An attendee cancels a registration and expects My Agenda to keep the history

My Agenda shows the current state. A canceled registration disappears from it unless the attendee also saved the session. You find the registration history in the session admin, under the **Slots** tab for a Time slot, or in exports.

### A change does not show up in the app right away

My Agenda updates immediately, but the mobile app may need a pull-to-refresh (swipe down) or a restart. In the web app, refreshing the page is enough.

## Related articles

- [Building the event Agenda — architecture](https://help.happenee.com/en/articles/26-building-the-event-agenda-%E2%80%94-architecture)
- [How the attendee app and its home screen work](https://help.happenee.com/en/articles/34-how-the-attendee-app-and-its-home-screen-work)
- [Setting up workshops and session registration](https://help.happenee.com/en/articles/28-setting-up-workshops-and-session-registration)
- [How time slots work](https://help.happenee.com/en/articles/29-how-time-slots-work)
- [Setting up reservations in the Agenda — buses, workshops, social program](https://help.happenee.com/en/articles/30-setting-up-reservations-in-the-agenda-%E2%80%94-buses-workshops-social-program)

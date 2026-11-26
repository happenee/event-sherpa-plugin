# Managing Speakers

> A content feature for profiles of people in your agenda, their assignment to sessions, and their display to attendees.

- Article in the Help Center: https://help.happenee.com/en/articles/23-managing-speakers
- Česká verze: https://help.happenee.com/cs/articles/23-sprava-recniku
- Collection: Content and attendee experience
- Updated: 2026-09-07

---

> [!info] Overview
> Speakers is a **content feature** that lets you add the people appearing in your agenda and show their profiles to attendees. Each speaker has a separate profile (first name, company, job title, photo, bio) and can be assigned to one or more sessions in the Agenda — in the role of **Speaker** or **Moderator**. The Display level controls the size of the speaker card and the order of the speaker groups on the microsite and in the attendee app; the order within each level is up to you — drag the speakers in the table or use Automatic sorting. A speaker profile is a content record, not an attendee account — it has no bearing on the person's registration, so for someone who is already registered you simply add the profile.

## Getting started

- Get clear on **who is appearing at your event** and in what role — keynote speaker, panelist, moderator, workshop facilitator.
- Prepare their **profiles**: first name, last name, company, job title, bio, profile photo.
- Decide the **Display level** — *High* for keynote speakers, *Basic* for regular speakers.
- Before you can assign speakers to sessions, the sessions must **first exist in the Agenda**.

## Details

### Where to find Speakers

In the left menu, go to **Content** and then **Speakers** (use the **+ Add** button if you do not yet have the content feature added).

### Adding a new speaker

1. Click **+ New speaker**.
2. Fill in **First name** and **Last name** (required).
3. Enter **Company** and **Job title** (optional).
4. Pick the **Country** (optional) — a dropdown of countries, not a free-text field. Opening it reveals a search box, so you do not have to scroll to find the country.
5. Pick the **Display level**: **Basic** (default), **Medium**, or **High**.
6. Upload the **Profile photo** (JPG or PNG, recommended 800×800 px, 1:1 aspect ratio, max. file size 800 KB).
7. Fill in the **Bio** — text in the rich text editor.
8. Save with **Save** (saves as hidden) or **Save and publish**.

When **Country** is filled in, the attendee sees it on the **speaker detail** on the microsite and in the attendee app — below the company, with a pin icon. It earns its place at an international conference, where the speaker's country carries information; on a purely domestic event, leave it empty rather than taking up room in the profile.

### What governs the listing on the microsite

A speaker's own settings decide **their profile** — what the card looks like and where it appears. **How many speakers are listed on the microsite home page** is governed elsewhere: under **Event microsite → Content**, the *Speakers* tab has a **Display** button offering a choice between a preview of the first rows with a link to a subpage, and the full list. See [How the event microsite works](https://help.happenee.com/en/articles/21-how-the-event-microsite-works) for details.

### Display levels

The Display level sets the prominence of the profile and the order of the speaker groups on the microsite and in the app:

- **High** — profiles appear first, with a larger card. Typically the keynote speaker or a special guest.
- **Medium** — the second wave; the card is smaller than *High* but larger than *Basic*.
- **Basic** (default) — regular speakers, panelists, and speakers tied to individual sessions.

### Speaker order within a level

The order of speakers inside each Display level is up to you, and it carries over to the microsite and the attendee app — attendees see the speakers exactly as you arrange them in the table. You have two options:

- **By dragging** — grab the speaker row by the six-dot icon on the left and drag it to another position within the level.
- **With Automatic sorting** — each level has an **Automatic sorting** button in the table. Sorting applies only to the speakers in that level; to sort the whole table, run it for each level separately.

Automatic sorting offers four options:

- **Alphabetically by first name** — sorts the speakers alphabetically by first name.
- **Alphabetically by last name** — sorts the speakers alphabetically by last name.
- **Group by company** — works with the company selected in the **Company** filter above the table. Following the current order, it finds the first speaker with that company and moves everyone else with the same company directly below them.
- **Group by session** — groups speakers by their session assignment. Following the current order, it finds the first speaker tied to the same session and moves the others with the same assignment directly below; the group order follows the first occurrence.

Automatic sorting is a one-off action, not a persistent mode — it sorts the speakers the moment you click, and you can keep fine-tuning the order by dragging afterwards.

### Profile state

The state controls where on the microsite and in the attendee app the speaker is visible. There are three states: **Published**, **In agenda**, and **Hidden**.

**Published** — the speaker is visible everywhere:

- on the attendee app home screen,
- in the Speakers module on the microsite and in the app (in the speaker list),
- in the Agenda module on the microsite and in the app — on the session card in the session list,
- on the session detail — in the speakers and moderators card,
- on the speaker's own detail page.

**In agenda** — the speaker **does not appear in the speaker list or on the app home screen**, but is visible everywhere their sessions show up:

- in the Agenda module on the microsite and in the app — on the session card in the session list,
- on the session detail — in the speakers and moderators card,
- on the speaker's own detail page — it stays reachable. An attendee gets to it by clicking through from the session detail, even though the speaker is not in the speaker list.

The **In agenda** state suits speakers you want listed on a specific session but do not want to feature in the speaker list as a "star" of the event — for example, the moderator of a panel or a presenter from your internal team. Attendees find them through the agenda, not by browsing the speaker list.

**Hidden** — the speaker is not visible anywhere: not in the Speakers module, not in the Agenda module, not next to any session. There is no speaker detail page either — the profile link does not exist. Use it for work-in-progress profiles or to temporarily pull a speaker without losing their data or session assignments.

### Assigning a speaker to sessions

Sessions must **first exist in the Agenda** before you can assign speakers to them.

From the speaker panel:

1. Open the speaker edit panel.
2. Switch to the **Sessions** tab.
3. In the **Search sessions** field, type the session name.
4. Optionally narrow results with the **Type** filter (by session types).
5. Click **+** next to the session — it gets added to the list.
6. For each assigned session, pick the role: **Speaker** or **Moderator**.
7. Save with **Save changes**.

You can also assign from the other side — from the session edit panel under **Content → Sessions**, on the **Speakers** tab.

### Roles: Speaker vs. Moderator

- **Speaker** — the person who presents the session content.
- **Moderator** — the person who moderates the session (for example, in a panel discussion).

The difference is visual — on the session detail, speakers appear under the *Speakers* heading and moderators under the *Moderators* heading. The same person can take different roles across different sessions (speaker on one, moderator on another).

### Speakers and attendees are two separate records

A speaker is not an attendee role. A speaker profile is a **content record** — name, company, job title, country, bio, photo — describing whoever appears in the Agenda. It carries no e-mail address and no login to the attendee app, and it has no bearing on whether the person is registered. Attendees are kept elsewhere: a contact in **Contacts and groups**, assigned to the event, with a completed registration.

The two records sit side by side and are not linked. In practice that means three things:

- **An attendee who is already registered and is going to appear in the Agenda** — create their profile in *Content → Speakers* (or import it) and assign them to their sessions. The profile is created **alongside** their registration, not instead of it — nothing changes on their attendee record, so there is nothing to redo or reset.
- **A speaker who exists only as a profile** — the profile does not add them to the event. No invitation reaches them, they get no QR ticket, and they are not on the attendee list. If they also need access to the attendee app or need to be checked in on site, assign their contact to the event and have them complete the registration; assignment on its own is not a registration. The procedure is in [Adding an attendee manually](https://help.happenee.com/en/articles/77-adding-an-attendee-manually).
- **Details are not mirrored between the two.** Changing the company or job title on the contact does not carry over to the speaker profile, or the other way round; deleting a speaker profile does not cancel a registration.

### Where roles live, and where groups live

The **Speaker** and **Moderator** roles belong to the profile's session assignment. They do not control what a person sees or whether they are registered — there is no switch in the administration that turns a registered attendee into a speaker.

When you need to tell speakers apart on the attendee side — send them a different invitation, give them extra content, filter them in the statistics — use a **contact group** (typically *Speakers*). The group drives the visibility of content and engagement features and the targeting of e-mail campaigns — it does not create or change profiles in the Speakers module. See [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility) for details.

### Bulk actions

In the speaker list, tick multiple speakers at once and use the bulk-actions panel:

- **Display level** — change to *Basic / Medium / High* in bulk.
- **State** — change to *Published / In agenda / Hidden* in bulk.
- **Delete speaker** — removes the speaker (irreversible).

### Multiple languages

The language switcher lets you translate:

- First name and Last name
- Job title
- Bio

The company is usually not translated (the company name is consistent), but the field accepts a translation if you need one.

### Import

You can bulk-import speakers two ways: **from a file** (XLS, XLSX, or CSV — first name, last name, company, country, job title, bio, display level, status) or **from another event**, where you pick specific speakers out of an existing Speakers module. Profile photos are **not uploaded from a file** — add them by hand after the import; an import from another event copies them. For a full walkthrough of the wizard, the template, and the numeric codes for Display level and Status, see [Bulk import of speakers](https://help.happenee.com/en/articles/67-bulk-import-of-speakers).

## Common pitfalls

### A speaker is added without a photo, and the microsite shows an avatar with initials instead — the page looks unfinished

The photo is optional, but it makes a real difference to how the page reads. If you do not have a professional photo, use at least a good-quality portrait (800×800 px, JPG/PNG, up to 800 KB). Without a photo, the event looks amateur.

### Every speaker is set to *High*, the speaker list is overcrowded, and the keynote blends in with the rest

Use *High* for only one to three of the most prominent speakers. Set the rest to *Medium* or *Basic*. The point is hierarchy.

### Automatic sorting looks like a persistent mode — it is a one-off action

Clicking an option sorts the speakers in the level once; the system does not keep maintaining the order afterwards. When you later add speakers or the companies and session assignments change, run Automatic sorting again, or fine-tune the order by dragging.

### Automatic sorting rearranged only part of the table — it always sorts a single level

The Automatic sorting button belongs to one Display level and sorts only the speakers in it. The other levels stay untouched — to sort the whole table, run the sorting for each level separately.

### A session is created and a speaker is assigned, but the speaker is set to **Hidden** — the speaker name does not show on the session detail

If you want the speaker to appear on a session, the state must be **Published** or **In agenda**. Hidden hides the profile everywhere.

### A keynote speaker is deleted by mistake — the session assignments go with them

Deletion is **irreversible** and removes the assignments from every session. The sessions themselves stay, but with no speaker. To take a profile out temporarily, use the **Hidden** state — the profile and the assignments are kept.

### A speaker is missing on the session detail even though they were assigned — the organizer thinks something is broken

Check the speaker state. If it is **Hidden**, the speaker does not appear anywhere. If it is **In agenda**, the speaker appears only with their sessions, not in the speaker list on the microsite or on the app home screen.

### An organizer expects the Excel import to upload photos as well

Photos do not come through the import. After the import, walk through the speakers and add the photos by hand.

### The speaker has a profile on the microsite but received no invitation and no QR ticket

A profile in the Speakers module is not a registration. If the speaker is also arriving as an attendee — going through check-in, opening the attendee app — they have to be a contact assigned to the event with a completed registration as well. Assignment to the event on its own does not issue the Confirmation e-mail with the QR code.

### An organizer waits for a registered speaker to appear in the speaker list on their own

The registration form does not create a speaker profile, not even when the person states in it that they are speaking. You create the profile by hand or through a bulk import. The reverse holds too: do not send anyone to register a second time because of a profile — the profile is created in the administration, not through the form.

## Related articles

- [Bulk import of speakers](https://help.happenee.com/en/articles/67-bulk-import-of-speakers)
- [How the Event microsite works](https://help.happenee.com/en/articles/21-how-the-event-microsite-works)
- [Building the event Agenda — architecture](https://help.happenee.com/en/articles/26-building-the-event-agenda-%E2%80%94-architecture)
- [How session types work](https://help.happenee.com/en/articles/27-how-session-types-work)
- [Managing sessions](https://help.happenee.com/en/articles/69-managing-sessions)
- [Setting up workshops and session registration](https://help.happenee.com/en/articles/28-setting-up-workshops-and-session-registration)
- [How time slots work](https://help.happenee.com/en/articles/29-how-time-slots-work)
- [Managing Sponsors](https://help.happenee.com/en/articles/32-managing-sponsors)
- [Managing Exhibitors](https://help.happenee.com/en/articles/33-managing-exhibitors)
- [Adding an attendee manually](https://help.happenee.com/en/articles/77-adding-an-attendee-manually)
- [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility)

<!-- source: kb.en.03.01 -->

---
title: "How the Event microsite works"
description: "The microsite is the public event page every e-mail link points to."
modules: ["microsite"]
last_updated: "2026-11-04"
version: 13
---

> [!info] Overview
> The Event microsite is the **public web page of the event** every link from e-mails and campaigns points to; it is the entry point for registration and for explaining what the event is about. It is created automatically when you create the event, and its content comes from **content features** (Agenda, Speakers, Venue, Contact, Custom content, Sponsors, Exhibitors); for each one you decide whether it appears on the microsite and in what order. On a paid event, the same table also sets where the ticket offer appears. The microsite address has the form `https://www.happenee.com/events/<slug>`, and you can change its final part (the slug) under **Event microsite → Settings** — but links shared earlier, including those in invitations already sent, stop working after the change. A workspace with a white label setup has its microsite on its own domain. If the microsite has a custom header image, you can show the event name, date and time, venue, and a button for adding the event to a calendar below it; the toggle is under **Event microsite → Settings**.

## Getting started

- Decide **how detailed the microsite should be** — a simple business card (when, where, contact), or a full page with agenda, speakers, partners, and FAQ.
- The microsite is filled by **content features** that you turn on under **Content**. Without content, the microsite stays empty.
- The cover image, intro text, and the position of the registration button are set in **Event microsite** in the left menu.
- If you plan to share the link publicly, check the registration restrictions in **Event settings** — who is allowed to register (see the article on registration types).

- Check the **microsite address** before you share it for the first time. The default slug comes from the event number and the event name (for example `4690_event-ops-summit-2026`); you can change it at any time, but old links then stop working.

## Details

### Where you set up the microsite

In the event admin, click **Event microsite** in the left menu. At the top you set:

- **Intro text** — rich text editor; shown under the microsite header.
- **Position of the registration button** — top, middle, bottom, or automatic.
- **Text shown after the registration form is filled in and submitted** — the thank-you screen. It supports placeholders (attendee name, event name).

### Tabs and content features

Below the intro is a table of microsite **tabs**. Regular tabs correspond to **content features** that you added under **Content**. When the event has **Tickets** turned on, the table also has a **Tickets** row (see *Ticket placement* below). Typical content tabs:

- **Agenda** (content feature)
- **Speakers** (content feature)
- **Venue** (content feature)
- **Contact** (content feature)
- **Custom content** (content feature — FAQ, map, info block)
- **Sponsors** (content feature)
- **Exhibitors** (content feature)

The table has a **Name**, a **Type**, and a **Published on microsite** column. For regular content tabs you choose:

- **Published on microsite** — the toggle in the right-hand column. A tab switched off is not on the microsite; the content stays in the admin.
- **Order** — drag the six-dot handle to the left of the name.
- **Display** — the button in the middle of the row. It is **not on every tab**; the **Sessions** and **Speakers** types have it, custom content does not. It opens a dialog with variants of how the content is listed on the home page.

### Ticket placement

When the event has **Tickets** turned on, the tabs table includes a **Tickets** row. It sets where the ticket offer appears on the microsite home page. Happenee adds the row on its own as soon as you turn on Tickets. If the event had Tickets on before, the row appears the first time you open **Event microsite** (the page reloads once on its own). At first the row sits in the top position, so the microsite looks the same as before and the tickets stay above the other content.

If attendees should see the agenda or speakers first, for example, drag the **Tickets** row by the handle to the left of its name to where you want it. The ticket offer moves between the other content on the home page, and the **Tickets** link in the microsite menu moves to the same position. Check the result on the public microsite.

The row is used only for ordering. It has no **Published on microsite** toggle and no **Display** button. Moving it does not turn the ticket offer on or hide it; whether attendees see the offer depends on your Tickets settings.

When you turn **Tickets** off, the row disappears from the table. When you turn Tickets back on, the row returns to the position where you last moved it. You do not need to add it again or create another content feature.

### How speakers are listed on the home page

On the **Speakers** tab, the **Display** button opens a **Display of Speakers** dialog with two options:

- **Preview of first 3 rows of speakers** — the home page shows only the start of the list, with a button to a subpage holding all the speakers below it.
- **List of all speakers** — the whole list sits on the home page, and the individual cards link through to the speaker detail.

Confirm your choice with **Save**.

Decide by **how many speakers you have and how much of your draw they are**. At a conference with thirty names, listing all of them on the home page takes up so much room that the agenda and registration fall below the fold — choose the preview there. At an event with four keynote speakers, a click through to a subpage is one step too many and people will not take it; a full list makes sense.

Watch the word **rows**: how many speakers fit on a row depends on the screen width and on the display level, so "rows" and "speakers" are not the same thing. To see how many the preview actually shows, open the **Microsite** button in the top right after you save.

So the shape of the speaker listing is **not governed by an individual speaker's settings** but by this choice on the tab. Profile details are in [Managing Speakers](03_managing-speakers.md).

### How the agenda is shown on the home page

On a **Sessions** tab, the **Display** button opens an **Agenda display** dialog. It has three parts.

**On the microsite homepage** — a choice between two variants:

- **Preview of first 6 sessions with link to full agenda** — the home page carries at most six sessions from the selected day, with a button to a subpage holding the full agenda below them.
- **Listing of all sessions** — the whole agenda sits on the home page.

**Quick filters on the homepage** — a dropdown below the display choice. It decides whether a row of filter buttons appears next to the agenda on the home page, letting an attendee switch the listing with one click — typically to a particular stage. Happenee builds the list from the agenda settings: besides **Do not show** (the default, no buttons), it holds only the filters whose **Show filter** toggle is on under *Content → (agenda) → Settings*, under the custom names and in the order you gave them there. A filter you never renamed appears under the default label for its type (*Type*, *Stage*, *Tags*). With *Show filter* off for every filter, *Do not show* is the only option left. Details below under *Quick filters next to the agenda*.

**Session display** — four checkboxes that control how much shows for each session:

- **Display full session description** — leave it off and the description is trimmed; **by default a maximum of 400 characters is shown**.
- **Link to session detail** — the session name becomes a link to its detail page.
- **Display speakers** — the assigned speakers are listed with the session.
- **Link to speaker profile** — a speaker's name on the session becomes a link to their profile.

The last two are tied together: with *Display speakers* unchecked, **Link to speaker profile** clears itself and greys out, so you cannot turn it on alone. A profile link has nothing to attach to when speakers are not listed with the session.

Confirm your choice with **Save**.

This is where page length is worth thinking about. An agenda of thirty sessions, each with a full description, its speakers, and links to their profiles, turns the home page into a column several metres long that attendees give up scrolling. The combination that almost always works: **a preview of the first 6 sessions** plus **Link to session detail** and **Display speakers** — the home page shows what the event is about, and anyone who wants more clicks through.

Keep those **400 characters** in mind while you are writing the agenda: if your session descriptions run longer and the checkbox stays off, attendees see only the beginning of them on the home page. See [Managing sessions](21_managing-sessions.md) for writing descriptions.

### Quick filters next to the agenda

Once you pick a filter type in the *Agenda display* dialog, a **row of buttons carrying that filter's values** appears next to the agenda on the home page — for *Stage*, something like *Main Stage*, *Stage B*, *Workshop Room 1*. Attendees see how the agenda is split the moment they open the microsite, without going to the full agenda subpage for it.

How the buttons behave:

- **The default state is unfiltered** — attendees see the whole agenda in time order.
- **A click narrows the listing** to one value. Only **one** value can be active — clicking another button switches to it, clicking the active one clears the filter and brings the whole agenda back. There is no *All* button in the row.
- **The row follows the selected day.** On a multi-day event with day tabs above the agenda, it offers only the values that actually fall on that day — a stage with nothing scheduled that day is not in it. Switching days also clears the selected filter.
- **They work in both display variants.** Under *Preview*, the filter applies to the whole selected day and at most six matching sessions are listed — so an attendee also finds a session that would not have fitted into the unfiltered six; the button to the full agenda stays. Under *Listing of all sessions*, they filter the whole listing.
- **The setting belongs to each Sessions tab separately.** A microsite with two agendas can have quick filters on for one and off for the other.
- With tags, the buttons take the **tag color**, so the row matches the tags on the session cards.

**The agenda settings govern both the list and the saved choice.** Whether a filter reaches the dropdown at all is decided by the **Show filter** toggle for that filter under *Content → (agenda) → Settings*. Turn it off for the filter currently chosen as the quick filter and Happenee resets the choice to *Do not show* in the same step — no saved state survives in which the chosen filter cannot render on the home page. Removing a single value (one stage, one tag) is a different matter: the choice stays and the row of buttons simply loses that value. For how the filters fit together, see [How registration blocks, stages, and tags work](11_how-registration-blocks-stages-and-tags-work.md).

Quick filters earn their place when the agenda runs in several parallel tracks — several stages, several topic tracks. Attendees see on the home page how many tracks the event has and switch into one with a click. For a single-day agenda in one room, leave it on **Do not show**: a row with a single button helps nobody and only adds an element above the agenda.

### The Event microsite home page

The **Event microsite home page** is the first screen an attendee sees after opening the link. Beyond the tabs, it contains:

- The cover image (the central image for the whole event).
- The intro text.
- The **registration button** (or the ticket purchase button on a paid event).
- The **ticket offer** on a paid event, in the position set by the **Tickets** row in the tabs table.
- A preview of selected content features, if their **Display** setting puts a preview or a listing there (for example, sponsor categories, the first sessions from the Agenda, featured exhibitors).

### Cover image and graphics

The microsite cover image is shared across the microsite, the invitation e-mail, the confirmation e-mail, and the attendee app. You set it under **Event settings → Graphics settings** (not directly in Event microsite). You have two choices:

- **Event icon with name and date** — a generated image.
- **Header image** — your own uploaded image at the recommended dimensions.

Next to the cover image, **Graphics settings** has an optional **Attendee app header settings** field. Its image appears only in the attendee app, both mobile and web; the microsite and e-mails don't use it. If you leave it empty, the app uses the image from the **Header image** option, the same header as in e-mails and on the microsite. If you haven't uploaded that one either, the event icon with the event name and date is used everywhere.

### Event details below a custom image

Under **Event microsite → Settings**, in the cover image section just below the **Event settings** link, turn on **Show event details below the image**. Visitors then see the event name, date and time, the venue (if filled in), and a button for adding the event to a calendar (Outlook, Google, or iCal) below your custom header image. Use this when you want to keep your own banner and still show the date and venue as text that visitors can read without zooming into the image.

The toggle is **off by default** and saves as soon as you switch it; refresh the public microsite to check the result. It only changes the microsite: the image and the e-mail content stay the same. You can turn the toggle on only after the microsite has a custom cover image. Until then it is inactive, and a note below it tells you to set the image first; without a custom image, the event details show in the header as before. A header customized for a specific customer is not affected by the toggle.

### The microsite address and how to change it

The microsite address has the form `https://www.happenee.com/events/<slug>`. The slug is the final part of the address; Happenee builds it when the event is created from the **event number and the event name**, for example `4690_event-ops-summit-2026`. Renaming the event later does not change the slug. The same slug is part of every registration link: the personal and public links in the invitation e-mail, the links in campaigns, and the link for completing registration with paid tickets all go through it.

You see and change the address under **Event microsite → Settings**, in the section with the public link. The fixed part `https://www.happenee.com/events/` cannot be changed. The slug can: click it, confirm the **Do you really want to change the microsite URL?** dialog with **Change link** (or back out with **Keep original**), and type the new form. Next to the address is a button that copies the whole link to the clipboard — use it after every change so that you share exactly what is saved.

What happens to the new slug:

- **Happenee converts it to a safe form.** Lowercase, no diacritics, spaces become hyphens; only the letters a–z, digits, hyphens, and underscores stay, everything else is dropped. "Spring Conference 2027" becomes `spring-conference-2027`.
- **It has to be unique across all of Happenee**, not just within your workspace. If another event already uses it, Happenee appends `_1`, `_2`, and so on, and saves that adjusted form without a warning. Check the saved address after every change.
- **The old address stops working immediately.** There is no redirect: anyone who clicks a link shared earlier (in an invitation e-mail already sent, in a campaign, on social media, or on your website) does not reach the microsite.

So change the slug before you send the link out for the first time: for a freshly created event that you want to give a readable address for the invitation or printed materials, and for a copied event if you kept the pre-filled name in the copy wizard: the slug then contains *kopie* (the Czech word for copy) and the copy date. Once invitations are out, changing the address means re-sending everything that contained the link.

### White label: the microsite on your own domain

If your workspace has a **white label** setup (your own domain, logo, and attendee app under your own name), the microsite does not run on `www.happenee.com` but on your domain. The address keeps the same shape with a different domain, `https://<your domain>/events/<slug>`, and the same slug rules apply, including uniqueness across all of Happenee. You cannot set the domain in the administration — white label is arranged by **customer support**, and you should plan for several weeks of lead time. How white label affects e-mails and the attendee app is covered in [The attendee's journey from the microsite to the attendee app](../04_communication-and-invitations/07_the-attendees-journey-from-the-microsite-to-the-attendee-app.md).

### Sharing and visibility

The **public link** to the microsite is in the same place, under **Event microsite → Settings**. You can share the link by e-mail, on social media, on your own website, in the invitation e-mail, or in e-mail campaigns.

- Anyone arriving from the publicly shared link is recorded in statistics as registered through **open registration**.
- For *invitation only* events, use the **invitation e-mail** or an **e-mail campaign** instead of the public link — that way the attendee receives a personalized link with pre-filled details.

### Visibility for groups

For each content feature (not for the microsite as a whole) you can restrict visibility to **selected attendee groups**. The check, however, only happens **after the attendee registers and signs in to the attendee app** — the microsite itself is always publicly accessible to anyone who has the link.

### Footer and tracking codes

- **Microsite footer** — either the default Happenee platform text or your own custom text (set under **Event microsite → Settings**).
- **GTM tracking codes** (Google Tag Manager) — to set these up, contact **customer support**. They are not configured in self-service.

### Changes during the event lifecycle

You can change microsite content at any time — publication is immediate. If attendees have the microsite open in a browser, they see the change after refreshing the page.

## Common pitfalls

### The organizer shares the microsite link before the content is filled in, and attendees see an empty page with only a name and a date

Fill in the basic content features (at least Venue and Contact) **before** you share the link. Ideally also Agenda and the intro text.

### Cover image at low resolution or in the wrong aspect ratio — the microsite looks blurry

Stick to the recommended image dimensions in **Graphics settings**. The microsite shows the same cover image on computers and phones; an image in **Attendee app header settings** doesn't change the microsite.

### The *Agenda display* dialog now reads *Do not show*, although quick filters were set

Someone has since turned off the **Show filter** toggle for the filter the quick filters were set to. Happenee resets the choice to *Do not show* on its own and without a warning, so that no selection stays on the home page that has no way to render. Turn *Show filter* back on under *Content → (agenda) → Settings* and pick the quick filter again in the dialog.

### The organizer expects quick filters to split the agenda into per-stage sections

They do not. The default view stays the whole agenda in time order, and the attendee picks a stage by clicking a button. If you need the agenda genuinely broken into stage sections the moment someone lands on the page, quick filters are not the answer.

### Quick filters are on for one agenda and off for another — it looks like a fault

The setting belongs to the tab, not to the event. Every **Sessions** tab has its own *Agenda display* dialog and its own quick filter choice. Walk through the tabs one by one.

### The tickets stay at the top of the microsite, although the agenda should come first

The ticket offer stays in the top position until you move it. In **Event microsite**, drag the **Tickets** row in the tabs table below the tabs that should come first. If you do not see the row in the table, the event does not have **Tickets** turned on.

### Every tab is set to the full listing under Display, the home page is overloaded, and attendees lose track

Choose the full listing on every tab and the home page grows to several screens, pushing the registration button far below the fold. Keep the full listing for **two to four of the most important tabs** (typically Agenda, Speakers, Sponsors) and pick the preview with a link to a subpage for the rest.

### The public link is shared with no registration restrictions, random people from the street register, and the event is invitation only

In **Event settings → Registration restrictions**, choose *Only assigned contacts*. The link still stays public, but only contacts you manage are allowed to register.

### The organizer changes the microsite address after the invitations are sent, and attendees who click the link in the e-mail do not reach the microsite

The old address does not redirect after a slug change, and that includes the personal registration links in the invitation e-mail and in campaigns. Either set the slug back to its original form (it is free again after the change), or re-send the invitations and fix the link everywhere you shared it — on the website, on social media, in printed materials.

### The saved slug looks different from what the organizer typed — it has a `_1` suffix, or diacritics and spaces are gone

Happenee converts the slug to a safe form and, when it matches another event anywhere in Happenee, appends a numeric suffix, both without a warning. Choose a more specific form (with the year or a company abbreviation) and check the saved address after every change — copy it with the button next to the address or open the microsite with the **Microsite** button in the top right.

### Microsite text is filled in only in one language, and a foreign attendee sees either a blank page or the Czech content

Switch the language flag in the top right corner and fill in the intro text in every language the event supports. If you leave a language blank, the primary language is used as the fallback (see *Setting the primary language of an event*).

### An attendee registered from the public link does not appear in the invitee list, and the organizer thinks something is broken

Attendees who arrive from the publicly shared link are recorded in statistics as registered through open registration. Check them under **Attendee statistics**. For full control over invitations, use the **invitation e-mail** instead of the public link.

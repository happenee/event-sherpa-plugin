<!-- source: kb.en.03.21 -->

---
title: "Managing sessions"
description: "Creating, editing, and bulk-managing sessions on the Sessions tab: the edit panel, inheritance from the type, status, filtering, and bulk actions."
modules: ["program_a_sessions"]
last_updated: "2026-09-16"
version: 11
---

> [!info] Overview
> A session is the basic building block of the Agenda — a specific item on the schedule with a name, time, type, and other details. You create and edit sessions on the **Sessions** tab in the Agenda: one at a time in the edit panel, or in bulk over selected sessions in the list. By default, each session inherits registration, visibility, and engagement from its assigned **type**, but you can override these settings on each session.

## Getting started

- Before you create your first session, have your **types** ready — the type sets the default behavior (registration, visibility, engagement). See [How session types work](07_how-session-types-work.md). Optionally prepare stages, tags, and registration blocks up front.
- Add a new session on the **Sessions** tab with **+ New session**. If a similar session already exists, copying it is usually faster — see *Copying a session* below.
- Fill in the required fields: **Session name**, **Date**, **Start**, **End**, and **Type**. The rest (stage, tags, description, speakers, partners) is optional.
- Save: **Save** creates the session unpublished; **Save and publish** publishes it to attendees right away.
- Time is entered in the event's time zone (see [Creating a new event](../02_event-setup-and-registration/01_creating-a-new-event.md)).

## Details

### Where to find sessions

Left menu → **Content** → select an Agenda → **Sessions** tab. The list shows every session in that Agenda. Next to it are the **Types**, **Blocks**, **Tags**, **Stages**, **My agenda**, **Settings**, and **Import** tabs.

### The session edit panel

A session is created and edited in a slide-out panel (**New session** / **Edit session**). The panel has tabs:

- **Information** — the basics (date, time, type, stage, tags, note; for registration types also the block and registration settings).
- **Visibility** — who can see the session.
- **Content** — description, image, and engagement features.
- **Speakers** — the session's speakers and moderators.
- **Partners** — sponsors and exhibitors assigned to the session.
- **Attendees** — the list of registrants (only when editing a Workshop or Time slots session).

For the **Time slots** type, a **Slots** tab is added as well — see [How time slots work](09_how-time-slots-work.md).

### The Information tab

This is where the session basics live:

- **Date**, **Start**, **End** — the session's time in the event's time zone.
- **Type** — shown as *custom name (base behavior)*, for example *Workshop (Workshop)*. The type sets the session's default behavior.
- **Block** — the registration block (only for Workshop and Time slots types; see [How registration blocks, stages, and tags work](11_how-registration-blocks-stages-and-tags-work.md)).
- **Stage** — the room or stage where the session takes place (also serves as a filter in the app).
- **Tags** — topic tags for the session.
- **Organizer note** — an internal note. It is **not shown** to attendees; it is for organizers only.

For registration types (Workshop, Time slots), the **Registration settings** block also appears on this tab — see below.

### Inheritance from the type

This is the key logic of the whole Agenda. A session **inherits** three groups of settings from its assigned type:

- **Registration settings** (Information tab, for registration types),
- **Visibility** (Visibility tab),
- **Engagement** (Content tab).

Each one has a **Default / Custom** toggle:

- While it is set to **Default**, the session shares the setting with the type — you see only a summary (for example, *Public* or *Session rating, Questions*), and a change at the type level flows here too.
- Switching to **Custom** **decouples** the setting from the type and reveals the individual options, which now apply to this session only. A later change to the type no longer affects such a session.

Why it works this way: you set most sessions of the same type once at the type level and do not have to touch them one by one. Use *Custom* only where a specific session genuinely differs from its type (different capacity, different visibility). For the inheritance details, see [How session types work](07_how-session-types-work.md).

### Registration settings on an individual session

For Workshop and Time slots types, after switching to **Custom** you can set:

- **Registration only for selected groups** — only attendees from the selected groups can register. You can pick only from the groups the session is visible to (see the Visibility tab below).
- **Assign attendee to a group after registration** — anyone who registers is automatically added to the chosen group (useful for follow-up communication targeting). When they leave the session or you turn assignment off, the group is removed again — even from an attendee who also holds it from another source.
- **Limit number of registrations** — once turned on, you enter the **maximum number of attendees** in a stepper field.
- **Show the number of available spots** — attendees see how many spots are left. The toggle appears only after you turn on **Limit number of registrations**, because without a limit there are no spots to count. If you later turn the limit off, this toggle turns off too and stays off when you turn the limit back on, so switch it on again.
- **Registration time limits** — when registration for the session opens and closes. You enter each boundary either as an offset from the session start (*Relative to session start*) or as a date and time (*Specific date*).
- **Session cancellation** — until when an attendee can cancel their own registration. The same two modes.
- **Notify the organizer when an attendee changes their session registration** — sends an e-mail when an attendee registers or cancels their registration themselves. Once it is on, you enter the recipient addresses (separate several addresses with commas); without an address the setting does not save.
- **Notify the attendee when their session registration changes** — sends the attendee a confirmation e-mail when they register or cancel their registration themselves. It does not cover changes you make; those are controlled by the toggle on the **Attendees** tab.
- **Send ICS to attendee** — attaches an ICS calendar file to the confirmation e-mail. It sends nothing on its own: without the attendee notification turned on, the attendee does not get the ICS either.

The same fields are set as defaults at the type level — see [Setting up workshops and session registration](08_setting-up-workshops-and-session-registration.md).

### The Visibility tab

After switching to **Custom**, you choose:

- **Public** — every attendee sees the session.
- **Selected groups only** — only the selected groups see the session; for everyone else it is hidden. A **Select groups** field appears.

Choosing *Selected groups only* also narrows the picker under **Registration only for selected groups** on the Information tab — you can admit only a group that can see the session. Set visibility before registration.

Visibility (who can see the session) is different from **status** (whether the session is published at all) — see below. Working with groups is covered in [Working with groups and visibility](../02_event-setup-and-registration/07_working-with-groups-and-visibility.md).

### The Content tab

- **Description** — the session text in an editor (formatting, links, in-text images). Mind the length: the microsite home page shows **a maximum of 400 characters** of the description by default, unless you turn on **Display full session description** under *Event microsite → Content → Display*. Put what matters in the first two sentences.
- **Image** — a preview image (JPG, PNG, or GIF; recommended size 1200 × 600 px, 2:1 aspect ratio).
- **Engagement** — after switching to **Custom**, turn on **Session rating** (attendees rate the session with stars) and **Questions** (attendees ask questions on the session detail).

### The Speakers and Partners tabs

- **Speakers** — assign speakers and, separately, moderators. Type a name into **Search for a speaker** and pick a profile; you can **Remove** an assigned speaker. Profiles are managed in the Speakers content feature (see [Managing Speakers](03_managing-speakers.md)) — assignment also works from the speaker's panel.
- **Partners** — assign sponsors or exhibitors through **Search sponsors and exhibitors**.

### The Attendees tab

On a saved Workshop or Time slots session, the **Attendees** tab lists the registered attendees. The summary above the list shows how full the session is and separates registrations attendees made themselves from the ones you made.

For a Workshop, you also manage attendees here manually: add a new one through the **Search attendees** field, and remove an existing one from the list. Manually added attendees are marked **Assigned by organizer**. You can add attendees even beyond the registration limit; the system only warns you that it has been exceeded. For a Time slots session, you manage attendees slot by slot in the **Edit attendees** dialog (see [How time slots work](09_how-time-slots-work.md)).

The same tab has the **Notify attendee on manual assign/unassign** toggle. When it is on, the attendee gets an e-mail whenever you add or remove them manually. The e-mail contains the session name, the date and time, and the event name; the e-mail about being added includes an ICS file if **Send ICS to attendee** is on. The organizer gets nothing about manual changes. The toggle is off by default and is not inherited from the session type, so you turn it on for each session separately; a Time slots session has it on each slot. If the e-mail cannot be sent, the change is still saved and the e-mail waits to be sent again. The same toggle also controls e-mails when registrations are canceled because a session is hidden or deleted.

### Saving, publishing, and status

When **creating** a session:

- **Save** — the session is saved unpublished (attendees do not see it yet).
- **Save and publish** — the session is saved and published right away.
- The dropdown options **Save and add another** / **Publish and add another** save the session and immediately open a blank panel for the next one — handy when creating several sessions in a row.

When **editing** a session, you save with **Save changes**. The bottom left has a **status** switch and a **Delete** button.

**Status** controls whether the session is visible to attendees. It has two values:

- **Published** — the session is published and attendees see it in the agenda on the microsite and in the app.
- **Hidden** — the session is not visible anywhere. Useful for sessions in progress or for temporarily pulling a session that nobody has registered for yet. Hiding a session with registrations costs you those registrations; see the next section.

### Hiding and deleting a session with registrations

If registrations on a hidden or deleted session stayed in the system, the attendee would not see the session, but the registration could still stop them from registering for another session at the same time. That is why Happenee does not hide or delete a session with registered attendees until you cancel their registrations.

When you switch a published session's status to **Hidden** and save, or when you delete a session, a confirmation dialog shows the number of registered attendees. A bulk status change to *Hidden* and a bulk delete behave the same way. **Remove attendees and save** (for a deletion, **Remove attendees and delete**) cancels the registrations first and only then hides or deletes the session. It also removes the groups the attendees received through **Assign attendee to a group after registration**. If you close the dialog, the change is not saved and the registrations stay.

Whether attendees learn about the cancellation by e-mail depends on the **Notify attendee on manual assign/unassign** toggle on the **Attendees** tab. Before you confirm, the dialog tells you how many attendees will get an e-mail and how many will not. Anyone who does not get one does not know about the cancellation, so let them know yourself.

Canceled registrations do not come back when you publish the session again. The same dialog appears when you hide a type whose sessions have registrations (see [How session types work](07_how-session-types-work.md)) and when you deactivate a time slot (see [How time slots work](09_how-time-slots-work.md)).

### Searching and filtering the list

The session list has a **Search sessions** field above it and a set of filters: **Day**, **Type**, **Block**, **Stage**, **Tags**, and **Status**. You can combine filters (for example, *Day 20 Mar* + *Type Workshop*) to narrow the results. Clear active filters with **Clear filters**.

The list columns — **Day**, **Time**, **Session name**, **Type**, **Block**, **Stage**, **Tags**, **Visibility**, and **Status** — are sortable. The **Visibility** column shows whether the session's visibility is inherited from the type (*Default*) or custom; the **Status** column shows *Published* or *Hidden*.

### Bulk actions

In the list, select several sessions (or all of them through the header checkbox) and use the bulk action bar:

- **Block** — assign or change the registration block (the *—* option removes it).
- **Stage** — assign or change the stage.
- **Tags** — add or remove tags.
- **Status** — change in bulk to *Published* or *Hidden*.
- **Delete** — delete the selected sessions.

A bulk action changes **only the chosen attribute** and leaves the sessions' other settings untouched. For both a change and a deletion, the system shows a confirmation dialog. If the selected sessions have registrations, the dialog for a status change to *Hidden* or a deletion shows their total number, and the action goes through only after they are canceled (see *Hiding and deleting a session with registrations*). Bulk actions are useful when rearranging tracks, moving sessions between stages, or when you need to align existing sessions after changing a type's settings (a type change does not flow into existing sessions on its own).

### Copying a session

You can copy an existing session. This helps when a new session differs from an existing one in only a few details — a different time, a different stage, a different speaker. The **Copy** button sits in two places: on the session's row in the list, and in the **Edit session** panel.

Clicking it opens the **New session** panel pre-filled with the original session's settings, with the cursor already in the **Session name** field. The name is pre-filled as **{Original name} (Copy)** — overwrite it right away so you do not leave a session with the word *Copy* in your agenda.

If the original session has speakers, moderators, or partners assigned, a **Copy speakers and partners?** dialog asks whether to bring them along. **Yes, copy them** adds them to the copy; **No, without them** creates the copy without them. The remaining settings are pre-filled without asking.

The copy is a separate new session — before you save it, check the **date, start, and end** in particular, so it does not sit on top of the original in your agenda.

### Import

Sessions can also be created in bulk from Excel through the **Import** tab in the Agenda. Import creates new sessions; it does not edit existing ones — use the bulk actions above to edit sessions that already exist. See [Bulk import of sessions](20_bulk-import-of-sessions.md).

## Common pitfalls

### The session is saved but attendees do not see it

The **Save** button only saves the session; it does not publish it — the session stays unpublished. To make attendees see it, use **Save and publish**, or switch the status of a saved session to **Published**. Check the **Status** column in the list.

### Switching to *Custom* decouples the session from the type

Once you switch a session's registration, visibility, or engagement to **Custom**, the type's settings no longer apply to it. A later change at the type level does **not** flow into such a session. If you want the session to follow the type, leave the toggle on **Default**.

### Some fields are locked after the first registration

Once the first attendee registers for a Time slots session, you can no longer change the type, the start and end time, or the slot length; for registration types, you also cannot switch the **Default / Custom** registration toggle. Make these decisions **before** registration opens. See [How time slots work](09_how-time-slots-work.md).

### A bulk stage or block change overwrites existing values

A bulk action sets the chosen stage or block on **all** selected sessions and overwrites whatever they had. Check which sessions you have selected before you confirm.

### When copying, the speakers and partners choice applies to all of them at once

The **Copy speakers and partners?** dialog is a single question for the whole session — you do not pick individual people. If you choose **No, without them** and then find you need the assignments after all, add them manually in the copy on the **Speakers** and **Partners** tabs.

### Deleting a session is permanent, and hiding it does not save registrations

Deleting (individually or in bulk) removes sessions for good. The **Hidden** status is not a way to keep registrations either: on a session with registered attendees it leads to the same confirmation dialog and, once you confirm, cancels the registrations just like a deletion. A session without registrations can be hidden and published again later without losing data.

### "My sessions disappeared" — usually an active filter

If you do not see sessions that should be there, check the filters above the list. An active filter (for example, *Status* or *Day*) shows only some sessions — clear it with **Clear filters**.

### Description vs Organizer note

The **Description** (Content tab) is shown to attendees on the session detail. The **Organizer note** (Information tab) is internal and attendees do not see it. Do not put public information in the note, and vice versa.

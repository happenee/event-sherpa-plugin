<!-- source: kb.en.03.07 -->

---
title: "How session types work"
description: "A template of default behavior for sessions: registration, visibility, and engagement features."
modules: ["program_a_sessions"]
last_updated: "2026-09-16"
version: 10
---

> [!info] Overview
> A session type is a **template of default behavior** — it sets registration, visibility, and engagement features for every session of that type. Every session must be assigned to a type. Happenee comes with four base behaviors (**Keynote**, **Workshop**, **Time slots**, **Break**), and from those you can build custom named types (*Keynote*, *Panel*, *Masterclass*). Inheritance flows from the type to the session, but you can override it on an individual session.

## Getting started

- Before you create sessions, **decide which types** you will need. Naming helps people navigate — for example *Keynote*, *Panel*, *Workshop*, *Partner presentation*.
- Every custom type **builds on one of the four base behaviors** — you cannot create a type that mixes behaviors.
- Set the default behavior once at the type level and every session **inherits it automatically**.
- If you only have a few sessions, the four pre-created types are enough.

## Details

### The four base behaviors

**Keynote.** The session is visible to every attendee and does not require registration. Typical use: keynote, all-hands talk, general session. It shows up in the agenda and the attendee just walks in.

**Workshop.** Attendees **register for individual sessions**. Every workshop visible to them is open for registration. Each workshop has its own capacity. Typical use: workshop conferences, professional seminars, training.

**Time slots.** The session has a defined length (for example, an hour), which is split into **slots** (for example, 15 minutes with a 5-minute break in between). The attendee **picks one slot**. Typical use: car test drives, one-to-one consultations, booking a specific time with an expert. See *How time slots work* for details.

**Break.** An informational item with **no detail page, no registration, and no engagement features**. It appears in the agenda as a plain time block (*Lunch*, *Coffee break*). The only fields you can fill in are **Stage**, **Tags**, and **Organizer note**.

### Default types created with the Agenda

When you add an Agenda, the system automatically creates **four default types**: *Keynote*, *Workshop*, *Time slots*, *Break*. You can:

- **Rename** them (for example, *Keynote* → *Opening keynote* — to fit your event's terminology).
- **Delete** them — but only if no sessions are assigned to them.
- **Hide** them — but hiding the type also hides every session of that type. If those sessions have registered attendees, you can hide the type only after their registrations are canceled.

### Custom types

Custom types build on one of the four base behaviors. The difference is in the **name** and in the **pre-filled defaults** — you can have two custom types built on the same base but with different default values.

Examples:

- *Keynote* (Keynote base) — visible to everyone, prominent in the agenda.
- *Panel* (Keynote base) — visible to everyone, with a different visual marker in the filter.
- *Small workshop* (Workshop base) — capacity of 15.
- *Large workshop* (Workshop base) — capacity of 100.

### Creating a new type

1. Go to the **Types** tab in the Agenda.
2. Click **+ New type**.
3. Enter a **Type name** (required).
4. On the **Settings** tab:
   - **Visibility** — *Public* or *Selected groups only*.
   - **Type** — pick a base behavior: *Keynote*, *Workshop*, *Time slots*, *Break*. Once you pick, the **Registration** section appears (for Workshop and Time slots).
5. In the **Registration** section (shown for Workshop and Time slots), set the defaults:
   - **Assign attendee to a group after registration.**
   - **Registration only for selected groups.**
   - **Limit number of registrations.**
   - **Show the number of available spots.**
   - **Registration time limits** — when registration opens and closes.
   - **Session cancellation** — until when an attendee can cancel their registration.
   - **Notify the organizer** and **the attendee** when a registration changes.
   - **Send ICS to attendee.**
6. For **Time slots**, additionally: **Time slot length**, **Break length**.
7. On the **Engagement** tab, set defaults: **Session rating**, **Questions**, **Anonymous questions**, **Polls**.
8. Save with **Save changes** or **Save and publish**.

The order of steps 4 and 5 is not arbitrary. If you set **Visibility** to *Selected groups only*, **Registration only for selected groups** offers only those same groups — you can admit only someone who can see sessions of that type in the first place. So set visibility before registration; for the detail, see [Setting up workshops and session registration](08_setting-up-workshops-and-session-registration.md).

### Inheritance and overrides

Every new session of a type **inherits** every setting automatically. On an individual session you can **override** inheritance:

1. Open the session edit panel.
2. On the **Information** tab, in the **Registration settings** section, switch the toggle from *Default* to *Custom*.
3. Edit the fields, which are now configured individually.

> **Switching between Default and Custom registration settings is not possible** once at least one attendee has registered for the session. Plan ahead.

The same pattern applies to the **Visibility** tab (the toggle **Default visibility from type**) and to the **Engagement** section on the session's **Content** tab.

### Type order and its impact on the agenda

You can reorder the rows in the **Types** tab manually by **dragging** them (by the handle on the left of each row). The order of types is not just cosmetic — it shows up in two places the attendee sees:

- **The Type filter.** In the agenda on the microsite, in the mobile app, and in the web attendee app, the values of the **Type** filter appear in the order you arrange the types in the table. This lets you put the key types (for example, *Keynote*) at the top of the filter.
- **Sessions at the same time.** When two sessions start at the same time, the agenda orders them by the order of their types — a type higher in the table appears first in the agenda.

The same "drag to set the order" principle applies to **Stages** and **Tags** and their filters — see [How registration blocks, stages, and tags work](11_how-registration-blocks-stages-and-tags-work.md).

### Changing a session's type

You can **change** a session's type in the session edit panel on the **Information** tab. If you switch to a type with different registration behavior (for example, from *Keynote* to *Workshop*), the registration settings change to the new type's defaults. Existing attendee registrations are not affected.

### Hiding a type

Hiding a type **hides every session** assigned to it. The sessions stop appearing to attendees in the app and on the microsite until the type is shown again.

If sessions of the type have registered attendees, hiding the type shows a confirmation dialog with their number, including when you change the status of several types in bulk. **Remove attendees and save** cancels the registrations and hides the type; if you close the dialog, the change is not saved and the registrations stay. Canceled registrations do not come back when you publish the type again. [Managing sessions](21_managing-sessions.md) explains why it works this way and when attendees get an e-mail.

### Deleting a type

You cannot delete a type if sessions are still assigned to it. Move the sessions to another type first.

## Common pitfalls

### A type-setting change does not reach sessions switched to *Custom* — the organizer expects those to reconcile too

A change at the type level flows through to every session that still inherits the setting — the ones with the toggle on **Default**, existing sessions included. Sessions where you switched the setting to **Custom** are decoupled from the type and will not receive the change; reconcile those on each session individually — by switching it back to **Default**, or by editing its custom values (see [Managing sessions](21_managing-sessions.md)).

### A custom type is created without deciding on the base behavior, and the organizer later finds out a Workshop cannot be switched to Time slots

The base behavior (*Keynote* / *Workshop* / *Time slots* / *Break*) is a property of the type. If you need a different behavior, create a new type and move the sessions over.

### Hiding a type as a temporary parking lot — the organizer realizes the sessions disappeared with it

Hiding a type means hiding every session of that type. If you want to hide only the type but keep the sessions visible, move the sessions to another type or change visibility on each session individually. If anyone has already registered for sessions of that type, hiding the type also costs you those registrations.

### A custom type *Keynote* is created with the *Keynote* base, but the organizer expects it to require registration

The base behavior controls registration — *Keynote* never requires registration. If you want registration, use the *Workshop* or *Time slots* base. The name *Keynote* is just an internal label.

### Switching *Default ↔ Custom* on a session that already has registered attendees — the system blocks it

If the session settings need to change, **do it before registration opens**. Once attendees register, some settings are locked.

### Type order left to chance — the filter and the agenda sort sessions unexpectedly

The order of types in the **Types** tab drives the order of values in the **Type** filter and how sessions with the same start time are sorted. If you want the key types at the top, drag them up in the table before you publish the agenda.

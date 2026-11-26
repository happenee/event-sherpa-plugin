<!-- source: kb.en.03.06 -->

---
title: "Building the event Agenda — architecture"
description: "The layers of the Agenda (sessions, types, registration blocks, stages, tags) and how they fit together."
modules: ["program_a_sessions"]
last_updated: "2026-09-16"
version: 11
---

> [!info] Overview
> The Agenda is a **content feature** that builds the event's schedule. The basic building block is a **session** — a single agenda item with a time, a stage, speakers, and content. Each session is assigned to a **session type**, which sets the default behavior for visibility, registration, and engagement features. To bundle sessions that need registration, you use **registration blocks**; **stages** and **tags** help attendees navigate a larger agenda. This article describes the architecture — how the layers fit together. The details for session types, workshops, and time slots live in the follow-up articles.

## Getting started

- Before you start creating sessions, **decide on the architecture** — how many rooms, how many tracks, how many days, whether the agenda needs registration or not.
- Add an **Agenda** under **Content** (if you do not have one yet).
- **Order of creation:** session types → stages (if you have multiple rooms) → tags → sessions → registration blocks (if needed).
- The session time is entered in the event's time zone (see *Creating a new event*).

## Details

### Adding the Agenda content feature

1. In the left menu, go to **Content** → **+ Add** → **Agenda**.
2. The content feature is added to the list of content features under Content, and the **Sessions** tab opens. Next to it appear the tabs **Types**, **Blocks**, **Tags**, **Stages**, **My Agenda**, **Settings**, **Visibility**, and **Import**.

> The Agenda content feature can be added to an event **multiple times**. Each instance has its own sessions, types, stages, and tags. Example: *Main agenda*, *Workshops*, *Social program* — three separate Agendas.

### The basic building blocks

**Sessions** — individual agenda items. Each session has:

- A name.
- A date, start time, and end time.
- A type (required — see below).
- Optional: stage, tags, description, speakers, sponsors, and exhibitors.

**Types** — templates that define default behavior. Every session must be assigned to a type. Happenee comes with **four base behaviors**:

- **Keynote** — visible to everyone, no registration. Keynotes, presentations.
- **Workshop** — attendees register for individual workshops. Every workshop visible to them is open for registration.
- **Time slots** — the attendee picks one of the offered slots (a reservation of a specific time).
- **Break** — an informational item with no detail page, registration, or engagement.

From these four base behaviors you can create custom types (*Keynote*, *Panel*, *Masterclass*) — each one builds on one of the four bases. See *How session types work* for details.

**Registration blocks** — bundle sessions that require registration (Workshop and Time slots types) and set how many sessions from the block an attendee can sign up for. Example: a block called *Morning workshops* contains three workshops; *Maximum number of sessions per attendee from this block* = 1, so the attendee picks one of the three.

**Stages** — physical rooms or stages. They are assigned to sessions and serve as a filter both in the attendee app and on the microsite.

**Tags** — thematic labels (for example *AI*, *Marketing*, *Leadership*). They are used to filter and recommend content in the app.

### Inheritance of settings

The session type sets default behavior for **registration**, **visibility**, and **engagement features** (rating, questions, polls). Every session **inherits** these settings automatically, but you can **override** them on an individual session.

> Changes to a type's settings flow through to every session that inherits the setting (its toggle on **Default**), existing sessions included. Sessions switched to **Custom** are decoupled from the type and will not receive the change.

### Creating a new session (overview)

The **New session** edit panel has five tabs (six for the Time slots type):

- **Information** — name, date, time, type, block, stage, tags, organizer note.
- **Visibility** — inherit from type, or set a custom rule (public / only for selected groups).
- **Content** — session description, image, video-call link, engagement settings (rating, questions, polls).
- **Speakers** — assign speakers and moderators (see *Managing Speakers*).
- **Partners** — assign sponsors and exhibitors to the session.
- **Slots** (Time slots type only) — overview of the generated slots and registered attendees.

The detail of how to create sessions of each type lives in the follow-up articles.

Sessions can also be created **in bulk from Excel** through the **Import** tab in the Agenda — see *Bulk import of sessions*.

### Scenarios

**Agenda without registration** (lecture format). All sessions of type **Keynote**. You do not need registration blocks or stages — sessions and times are enough. Fits a conference or a meetup.

**Workshops with open registration.** Sessions of type **Workshop** without registration blocks. The attendee signs up for any number of workshops. Set a capacity (**Limit number of registrations**) and, if needed, **Registration time limits** and **Session cancellation**.

**Workshops with limited choice.** Sessions of type **Workshop** plus **Registration blocks**. Each block contains 3–5 workshops with a maximum of 1. The attendee has to pick one from the offer. Typical for a multi-round workshop format.

**One-on-one meetings and time slots.** Sessions of type **Time slots**. The session has a defined length (for example 60 minutes), which is split into 15-minute slots. The attendee picks a specific slot. Fits one-to-one meetings, car test drives, and reservations (see *Setting up reservations in the Agenda — buses, workshops, social program* for details).

**Mixed agenda.** A mix of types in a single event. Keynote as Keynote, workshops as Workshop, one-on-one meetings as Time slots, breaks as Break.

### Multi-room agenda

For a large conference with multiple rooms and parallel tracks:

1. Create **Stages** — one for each room.
2. Create dedicated **session types** or use **Tags** to distinguish tracks (for example *Business Track*, *Tech Track*).
3. Turn on the **Stage** and **Tags** filters on the Agenda's **Settings** tab.
4. In the Agenda settings, look at **Allow concurrent registrations within this Agenda** and decide whether it makes sense — yes for a conference, usually no for workshops.

### Concurrent registrations

By default, an attendee **cannot register for two sessions whose times overlap**. This applies inside a single Agenda and across all Agendas in the event. You can relax the restriction on the Agenda's **Settings** tab with two independent toggles:

- **Allow concurrent registrations within this Agenda** — the attendee can sign up for overlapping sessions, as long as both are in this Agenda.
- **Allow concurrent registrations across Agendas** — the attendee can register at the same time for sessions from different Agendas. The toggle has to be on **in both Agendas**; if only one of them has it on, the restriction between them still applies.

Above the toggles, the admin spells out what the current combination means for attendees. When you turn on the second toggle and remove every restriction, the system first asks whether you really want to. Turning a toggle off saves without a prompt.

How the system decides what overlaps:

- **Only times that actually intersect clash.** Back-to-back sessions (one ends at 11:00, the next starts at 11:00) do not overlap.
- **For a time slot, the slot's time counts**, not the whole session. The original registration does not block switching to another slot of the same session.
- **Only active registrations count.** A canceled registration blocks nothing.
- **The check applies only when attendees register themselves.** When you add an attendee manually on the **Attendees** tab, or in the **Edit attendees** dialog of a slot, the system does not check for overlaps.
- **Changing the settings does not work retroactively.** When you turn a toggle off and the restriction applies again, registrations that already overlap stay in place. Nothing is canceled.

An attendee whose registration would create an overlap sees the **Register** button disabled. In a browser, hovering over it shows the reason: *You already have a registration for another session at this time.*

### Display settings

Besides concurrent registrations, the Agenda's **Settings** tab has a **Display settings** section — toggles that control how the agenda is presented to attendees:

- **Show session time** — shows the start and end time next to session cards in the agenda.
- **Show time zone** — shows time-zone information with the session schedule. Useful for online and hybrid events with attendees in multiple countries.
- **Show date in session detail** — shows the date in the session detail header. Helpful for multi-day events where the time alone is not enough.
- **Expand time slots in the agenda** — time slots appear directly on the session card in the agenda overview, so the attendee picks a time without opening the detail (see *How time slots work*).

> How the agenda is displayed on the event microsite is configured separately, in the **Microsite** section.

### Saving the Settings tab

The **Settings** tab has no **Save** button. The system saves every toggle change and every new filter order right away and confirms it with a message. If saving fails, the toggle switches back to its last saved position and an error appears. The toggle and the display option on the **My Agenda** tab save the same way. The button remains in two places: you confirm a filter rename with **Save** in the side panel, and on the **Visibility** tab you save the name and groups with **Save changes**.

### Visibility on the microsite and in the app

All content features (the Agenda included) have separate visibility toggles for the microsite and the attendee app. In the app, sessions are listed in chronological order; sessions with the same start time are ordered by the order of their types (see [How session types work](07_how-session-types-work.md)). Registration for sessions of type **Workshop** and **Time slots** is available **only in the attendee app** — an attendee cannot sign up for a workshop through the microsite.

## Common pitfalls

### The organizer creates every session as Keynote even though some were meant to require registration, and attendees have no way to sign up

Decide the type **before** you create the session. For registration, pick **Workshop** (any number) or **Time slots** (a specific time).

### A change to a type's settings (such as capacity) does not reach sessions switched to *Custom*

The change flows through to sessions that inherit the setting (their toggle on **Default**), existing ones included. Sessions where you switched the setting to **Custom** are decoupled from the type and will not receive it; reconcile those on each session individually — see [Managing sessions](21_managing-sessions.md).

### An agenda with parallel sessions but no stages — the attendee cannot tell where each session takes place

For an agenda with parallel tracks, always create **Stages** and assign them to sessions. The attendee can then filter the agenda by room.

### The organizer turns on Concurrent registrations without thinking it through, and an attendee signs up for two sessions at the same time and can attend neither

Turn *Concurrent registrations* on only where it makes sense (a conference plus a poster session; a workshop plus a social program). For ordinary workshops, leave the default restriction in place.

### Concurrent registrations across Agendas is on in only one Agenda, and the attendee still cannot register

The across-Agendas option applies only when both Agendas have it on. Check **Settings** in both.

### You restore the restriction after registration has opened and expect the overlaps to disappear

A toggle turned off only guards new registrations. Anyone who has meanwhile signed up for two sessions at the same time stays registered for both. Go through the registered attendees of the affected sessions and resolve the overlaps with them, or remove them from one of the sessions manually.

### Time slot sessions are created, but the attendee does not see slots in the app

Slots are generated when the session is saved, based on the **Time slot length** and **Break length** fields. Check those fields. The session's **Slots** tab shows the generated slots and how full they are.

### Trying to change a session's type after the first attendee registers — the system blocks it

Once the first attendee registers for a Time slots session, you **cannot** change the type, the start and end time, the slot length, or the break length. Plan ahead.

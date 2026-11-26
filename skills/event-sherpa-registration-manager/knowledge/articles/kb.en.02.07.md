<!-- source: kb.en.02.07 -->

---
title: "Working with groups and visibility"
description: "How to use groups inside an event to control content visibility, communication targeting, and registration limits."
modules: ["ucastnici_skupiny_a_viditelnost"]
last_updated: "2026-09-07"
version: 3
---

> [!info] Overview
> Groups in Happenee are how you **categorize attendees** and control what each of them sees. Group management itself lives at workspace level (see *Managing contacts and groups in your workspace*). This article covers how you use groups **inside an event** — for visibility of content and engagement features, communication targeting, registration limits, and statistics filtering.

## Getting started

- Decide what you want to differentiate attendees by — type (VIP / standard), role (speaker / partner), source of registration (nominator), preference (catering, workshop), company, or team.
- Create the groups **before** you launch registration. Assigning them after the fact works, but it is manual.
- The ways an attendee ends up in a group are described in *Managing contacts and groups in your workspace* — the fastest path is through an answer in the Registration form.
- Turn visibility on carefully — an empty feature shown to half the attendees feels like a broken app.

## Details

### Four main uses of groups

**1. Visibility of content and engagement features.** For every content feature (Agenda, Speakers, Venue, Contact, Custom content, Sponsors, Exhibitors) and every engagement feature (QR ticket, Notifications, Polls, Survey, Questions, Attendees, Registration information, Online module) you can choose whether all attendees see it or only selected groups. (The attendee-to-attendee networking feature is labeled **Attendees** in the UI; *Networking* is the brand-term alias used in communication.)

**2. Targeting e-mail campaigns.** An e-mail campaign can be targeted to one or more groups. The Invitation e-mail **does not support** targeting by group — if you need to segment an invitation, use an e-mail campaign instead.

**3. Visibility of questions and answers in the Registration form.** For every additional question and every specific answer you can choose to show it only to selected groups.

**4. Reporting.** Attendee statistics can be filtered by group — for example, *how many people from sales rep Novák's nomination actually showed up*.

### How an attendee ends up in a group

A summary of the paths (details in *Managing contacts and groups in your workspace*):

- **Import** — when bulk-importing contacts, in the groups column.
- **Manually in the contacts table** — select contacts and use the **Add or remove from groups** action.
- **From the Registration form** — an answer to a question assigns the attendee to a group (configured on the specific answer; see *How conditional questions work in the Registration form*).
- **From a nominator** — a nominator can have a default group preset for everyone they invite, or they can assign groups manually (see *How nominations and nominators work*).
- **After buying a ticket** — a ticket can have a group preset, and the attendee is assigned to it automatically after registration (see *Setting up Tickets*).
- **From a link** — individual and bulk registration links can carry an assigned group, and the registrant is added to it automatically.
- **After using a discount code** — a discount code can have an assigned group.

### How to set the visibility of a feature

In the event admin under **Content** or **Engagement features**, open the detail of a specific feature. In the **Visibility settings** panel (tooltip *Visibility restrictions for groups*) you find:

- **all attendees** (default) — everyone sees the feature.
- **Selected groups only** — opens a field for picking groups. Only attendees in the selected groups see the feature.

For each content feature you can also choose whether it appears on the **microsite**, in the **attendee app**, or both. Engagement features show only in the attendee app. Visibility by group applies across every channel where the feature appears.

### Visibility of questions and answers

In the Registration form, on the **Additional questions** tab:

- For an entire **question**, turn on **Show question only to selected groups** and pick which ones.
- For a specific **answer** in a type 2 (Select only one) question or similar, turn on visibility and pick the groups. This lets you, for example, hide the answer *Yes, I want VIP access* from everyone except the VIP group.

### Targeting an e-mail campaign

In **E-mail campaigns**, when creating a campaign you choose the recipients. You can pick:

- All attendees of the event.
- Attendees in a specific status (*Attending*, *Not attending*, *Not responded*).
- Attendees in one or more **groups**.

Combining filters lets you target very precisely — for example, *everyone from Brno who is in the Attending status*.

### System vs. user groups

Every group in Happenee today is a **user group** — created by the organizer. System groups (automatically created, for example *Confirmed attendees* or *Not registered*) are not available today; you handle that need with manual groups or by filtering on attendee status.

### Global vs. local groups

Groups are **global** to the entire workspace — there are no groups bound to a single event. If you want to differentiate groups across events, name them unambiguously (for example, *Conference25_VIP*, *Workshop25_Speakers*). Local groups bound to an event are not available today.

## Common pitfalls

### The organizer wants to target communication to VIP attendees but does not have a VIP group — attendees are split by registration status, not by type

Attendee type is defined by a **group**, not by status. Create a VIP group and add everyone it applies to (through import, a Registration form question, or manual assignment).

### A feature is set to be visible only to a selected group, but the organizer forgot to add everyone the feature is meant for to that group, so part of the audience cannot see it

After you set visibility, check the contacts table for how many people are in the group. If the number does not match your expectation, add the missing attendees (manually or in bulk).

### Visibility is turned on for a group that does not yet have any members the feature is intended for, so the feature appears to no one

Visibility takes effect immediately — if no one is in the group, no one sees the feature. Add members first and then turn on visibility, or use a temporary *Selected groups only* with a test group (for example, *Organizer*) and open it up to everyone once the content is ready.

### The organizer relies on group assignment through a form answer to also apply to answers picked before the group was attached to that specific answer

Automatic group assignment only works for new answers. Existing answers are **not back-filled** — if you added the setting after the form went live, fill in the groups manually.

### Expectation that a group from one event stays in that event — groups are global and reach across every event

For one-off groups, use a name that includes an event prefix (for example, *ConfApril25_VIP*). After the event, clean the groups up, or at least rename them.

### Invitation e-mail targeted by group — but that capability does not exist

The Invitation e-mail does not support targeting by group; it only lets you split by status (not invited, not responded, did not open). For segmentation by group, use an **E-mail campaign**.

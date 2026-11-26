# Setting up workshops and session registration

> A Workshop is a session that requires registration and has a capacity, an optional registration window, and an optional cancellation deadline, with sign-up done in the attendee app.

- Article in the Help Center: https://help.happenee.com/en/articles/28-setting-up-workshops-and-session-registration
- Česká verze: https://help.happenee.com/cs/articles/28-nastaveni-workshopu-a-registrace-na-sessions
- Collection: Content and attendee experience
- Updated: 2026-09-16

---

> [!info] Overview
> A Workshop is a session type that **requires the attendee to register**. Each Workshop has its own capacity and, optionally, a registration window, a cancellation deadline, and a restriction to selected groups. Registration takes place **in the attendee app**. This article describes the registration rules; bundling Workshops into packages (where the attendee picks 1 of 3) is covered in *How registration blocks, stages, and tags work*.

## Getting started

- Decide whether attendees should **register for individual Workshops separately**, or **pick one Workshop from a set** (a registration block).
- Plan **capacities** based on the room and the workshop content. The system tracks capacity automatically.
- If you want to **target communication** at people registered for a Workshop, set up **Assign to group after registration**.
- If registration for Workshops should open at a different time than registration for the event, set **Registration time limits**. You do not have to keep the session hidden and publish it on the opening day.
- If you plan to restrict the Workshop to groups, **decide visibility first and registration second**.

## Details

### Where registration is configured

Workshop registration rules are configured at **two levels**:

- **At the session-type level** — defaults for all sessions of that type. Set once, and every Workshop of that type inherits them.
- **At the individual session level** — an override of the default for one specific session.

Both levels expose the same set of registration fields.

### Workshop registration settings

**Assign attendee to a group after registration.**
After a Workshop registration, the system automatically adds the attendee to a chosen group. The group must exist in advance under **Contacts and groups**. This also works when an organizer registers the attendee for the session manually — it behaves the same as a sign-up in the app.

The assignment is **two-way and continuous**. When the attendee leaves the session — they cancel their registration, or an organizer removes them — the group is removed from them again. When you **turn group assignment on or off** on the session or its type, the change also applies to attendees who are already registered: turning it on adds the group, turning it off removes it. At the type level, this applies to all sessions of that type at once.

Use case: targeting communication only at attendees of a specific Workshop (a personalized e-mail, a push notification, special content in the app visible only to that group).

**Registration only for selected groups.**
Workshop registration is restricted to attendees in specified groups. Other attendees can see the Workshop (unless visibility is also restricted), but cannot sign up.

The groups you pick here are always a **subset of who can see the Workshop**. When visibility is set to *Selected groups only*, the registration picker offers **only the groups the session is visible to** — you cannot pick any other. That follows from how the feature works: a group that cannot see the Workshop in the Agenda would not be able to sign up for it anyway. With visibility set to *Public*, you pick from the full list of groups.

Use case: VIP Workshops for paying attendees, closed Workshops for a specific corporate team.

**Limit number of registrations.**
The maximum number of attendees in the Workshop. Once full, the Workshop is marked *Fully booked* in the app and further registrations are blocked.

**Show the number of available spots.**
If capacity is limited, you can show the remaining count to attendees in the app. Transparent for the attendee, but it can create pressure ("hurry, only a few spots left").

**Registration time limits.**
Set when registration for the Workshop opens and closes. Once you turn the setting on, you pick one of two modes:

- **Relative to session start** — both boundaries count backward from the start of the Workshop. You choose from a fixed list of offsets — *15 min*, *30 min*, *1 h*, *3 h*, *1 day*, *2 days*, *7 days* — plus an **Unlimited** option.
- **Specific date** — for each boundary you enter a date and a time, or turn the boundary off with the **Unlimited** switch.

*Specific date* covers the most common request: ticket sales run from June, and registration for Workshops should open on August 1. Set **Registration available from** to August 1 and a time, and leave the **Unlimited** switch on for **Registration available until**. The Workshop stays published the whole time and attendees see it in the Agenda; they just cannot sign up before August 1.

Times follow the event timezone. Both boundaries are inclusive — registration still goes through at the exact opening instant and at the exact closing instant.

**Session cancellation.**
Set until when an attendee can cancel their own registration. The same two modes apply: **Relative to session start** with the same offsets (no *Unlimited* option here), or **Specific date** with a date and time. After the deadline the *Cancel registration* button disappears and the attendee has to contact you.

The setting **adds** a deadline; it does not remove the ability to cancel. With *Session cancellation* turned off, an attendee can cancel their registration at any time.

Use case: a Workshop with catering ordered or materials printed, where you need firm numbers two days ahead.

**Notify the organizer when an attendee changes their session registration.**
An e-mail to the organizer when an attendee registers or cancels their registration themselves. Once it is on, you enter the recipient addresses (separate several addresses with commas); without an address the setting does not save. Useful for Workshops with an assistant who plans capacity (catering, materials).

**Notify the attendee when their session registration changes.**
A confirmation e-mail to the attendee when they register or cancel their registration themselves. It does not cover an organizer adding or removing the attendee manually. That is controlled by a separate toggle, **Notify attendee on manual assign/unassign**, which is not among the registration fields: you find it only on a specific session's **Attendees** tab, and it is not inherited from the type (see [Managing sessions](https://help.happenee.com/en/articles/69-managing-sessions)).

**Send ICS to attendee.**
Attaches an ICS file to the confirmation e-mail so the attendee can add the session to their calendar. It does not send an e-mail of its own: when *Notify the attendee when their session registration changes* is off, the attendee gets nothing after registering, not even the ICS. The ICS is also attached to the e-mail about being added manually.

### Registration flow in the app

1. The attendee opens the **attendee app** (mobile or web) and finds the session in the Agenda.
2. On the session detail they see the **Register** button (if it is not full and they meet the visibility conditions).
3. After tapping it, the system registers them automatically. If configured, they get a confirmation e-mail with the ICS.
4. The session shows up in **My Agenda**.

Outside the configured window, the **Register** button is not available. In its place the session detail shows *Registration will open on* with a date and time, or *Registration closed on*. For a session the attendee is registered for, *Cancellation closed on* appears once the cancellation deadline has passed. The attendee sees the reason and does not have to ask you.

### Capacity and waitlist

Happenee does not currently support a **waitlist**. Once capacity is full, the Workshop is marked as full and further registrations are rejected. If someone cancels their registration, the spot opens up and another attendee can register (but not automatically from a waitlist — they have to actively click Register).

### Workshop visibility

On the **Visibility** tab of the session panel:

- **Public** — every attendee sees the Workshop.
- **Selected groups only** — only attendees in the chosen groups see the Workshop. Everyone else does not see it in the Agenda at all.

The difference compared to *Registration only for selected groups*: a visibility restriction means the attendee does not see the Workshop at all; a registration restriction means they see it but cannot sign up.

You can combine both restrictions, but not freely — **visibility takes precedence over registration**. As soon as you restrict visibility to groups, the picker under *Registration only for selected groups* narrows to those same groups. So set visibility first and registration second; the other way around, the group you want to admit is missing from the picker.

### Workshop without a registration block vs. with a block

Without a block: the attendee can register for **any number of Workshops**. Useful for optional Workshops or training programs with several parallel streams, where the attendee builds their own itinerary.

With a block: the attendee picks **1–N Workshops from a set**. Useful for a format like "in the morning you pick one of three Workshops, in the afternoon another one of three". Detail in *How registration blocks, stages, and tags work*.

## Common pitfalls

### A Workshop has a capacity but *Limit number of registrations* is not turned on, and more attendees register than fit

Always set the capacity — the system blocks registrations once the limit is reached. Without the setting, capacity is unlimited.

### The attendee cannot register for a session through the microsite, and the organizer thinks the microsite is broken

Workshop registration is **only in the attendee app**. On the microsite the attendee sees the Workshop, but for registration they have to go to the app.

### The group used for assignment after registration was never created — attendees register, but the group stays empty

**Create the group first** in Contacts and groups, then assign it to the Workshop.

### You use the same group for the Workshop and for a permanent segment — after removal from the session the attendee loses it entirely

Removing the group after registration is **unconditional**. When you remove an attendee from the session, or turn assignment off on it, the group is stripped from them even if they also hold it from another source — a registration link, a discount code, a ticket, another session, or a manual assignment. The system does not check whether some other reason still keeps the attendee in the group. So use a **dedicated group** for assignment after session registration. Do not share it with a permanent segment — for example a *Partner XY* group that a partner's bulk registration link assigns people to, and that your campaign targeting or content visibility depends on. If you then remove such a partner from the Workshop, they lose the group and your segmentation quietly breaks.

### Trying to lower the Workshop capacity after registrations have come in — some attendees are already in, others are waiting

Capacity can be **increased** at any time. **Lowering** it below the current registration count is not allowed — the system blocks it. To lower the capacity, you first have to cancel attendees' registrations manually.

### The group you want to admit is missing from the *Registration only for selected groups* picker

The picker is limited to the groups the session is visible to. If the group is not there, add it first on the **Visibility** tab under *Selected groups only*, or switch visibility to *Public* — then you pick from the full list of groups.

### Both registration boundaries set to *Unlimited* — the setting will not save

A time limit has to limit at least one side. If you do not want registration to close, leave *Unlimited* only on **Registration available until**; if you do not want to delay the opening, leave it only on **Registration available from**. The system rejects both at once.

### Registration is set to open later than it closes — the system reports an error

The message reads *Registration must open before it closes*. In *Specific date* mode the mistake is obvious. In *Relative to session start* mode it is easy to get wrong, because both numbers are offsets **before** the Workshop starts — so the opening offset has to be larger than the closing one. "Open 7 days ahead, close 1 day ahead" is valid; "open 15 minutes ahead, close 1 day ahead" is not.

### Keeping the Workshop in *Hidden* status so nobody can sign up early

The usual workaround is to prepare the session hidden and publish it on the opening day. That is no longer necessary, and it has a downside — attendees do not see a hidden session in the Agenda at all, so they cannot plan ahead what to attend. Leave the session published and control the opening time with **Registration time limits**.

### *Send ICS to attendee* is on, but the attendee got nothing after registering

The ICS is only attached to the confirmation e-mail. Turn on **Notify the attendee when their session registration changes** as well.

### You added or removed an attendee manually, and they did not get an e-mail

*Notify the attendee when their session registration changes* does not cover manual changes. Only the **Notify attendee on manual assign/unassign** toggle on the **Attendees** tab sends that e-mail; it is off by default and set on each session separately (for Time slots, on each slot). Turn it on before you save the change; changes already saved do not trigger an e-mail afterwards.

### An attendee receives a campaign about a Workshop but does not see it in the app

Check that the attendee has **visibility** of the Workshop (groups) and that the session **status** is Published. A third option: the attendee is not registered for the event (they have to be signed in to the app with the *Attending* status).

## Related articles

- [Building the event Agenda — architecture](https://help.happenee.com/en/articles/26-building-the-event-agenda-%E2%80%94-architecture)
- [How session types work](https://help.happenee.com/en/articles/27-how-session-types-work)
- [Managing sessions](https://help.happenee.com/en/articles/69-managing-sessions)
- [How time slots work](https://help.happenee.com/en/articles/29-how-time-slots-work)
- [How registration blocks, stages, and tags work](https://help.happenee.com/en/articles/31-how-registration-blocks-stages-and-tags-work)
- [Setting the registration type and additional questions](https://help.happenee.com/en/articles/12-setting-the-registration-type-and-additional-questions)
- [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility)
- [Managing Speakers](https://help.happenee.com/en/articles/23-managing-speakers)
- [Setting up reservations in the Agenda — buses, workshops, social program](https://help.happenee.com/en/articles/30-setting-up-reservations-in-the-agenda-%E2%80%94-buses-workshops-social-program)
- [How My Agenda works](https://help.happenee.com/en/articles/35-how-my-agenda-works)
- [Recommended setup for a conference](https://help.happenee.com/en/articles/55-recommended-setup-for-a-conference)
- [What to do when workshop or session registration does not work](https://help.happenee.com/en/articles/90-what-to-do-when-workshop-or-session-registration-does-not-work)
- [What to do when a workshop is full](https://help.happenee.com/en/articles/91-what-to-do-when-a-workshop-is-full)
- [Recommended setup for test drives](https://help.happenee.com/en/articles/98-recommended-setup-for-test-drives)

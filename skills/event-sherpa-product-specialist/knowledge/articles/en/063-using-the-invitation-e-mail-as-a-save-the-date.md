# Using the Invitation e-mail as a save-the-date

> An advance event announcement: the Invitation e-mail with the registration button hidden, only a calendar entry attached. Used before opening registration.

- Article in the Help Center: https://help.happenee.com/en/articles/63-using-the-invitation-e-mail-as-a-save-the-date
- Česká verze: https://help.happenee.com/cs/articles/63-zvaci-e-mail-jako-save-the-date
- Collection: Communication and invitations
- Updated: 2026-08-16

---

> [!info] Overview
> A save-the-date is an advance announcement that an event is happening — sent earlier than the full invitation. Its only goal is to reserve the date in the attendee's calendar, not to register them yet. In Happenee you send a save-the-date through the Invitation e-mail with the **registration button hidden** and an **ICS attachment** for adding the event to the calendar. The full invitation with registration goes out later as another Invitation e-mail or an E-mail campaign.

## Getting started

- Decide when to send the save-the-date — typically 2–6 months before the event, far enough out for attendees to block the date.
- Prepare a minimal message: a short *"reserve the date"* note, the event name, the location (or *"location to be confirmed"*), and the date.
- Agree with the team on **when the full invitation** with the registration link will follow — typically 4–8 weeks before the event.

## Details

### The principle — why a save-the-date instead of the full invitation

A save-the-date does one thing: **reserve the date in the attendee's calendar before registration is ready**. It fits two situations:

- The event is far in the future and the agenda, tickets, or location are not finalized — but you want attendees to hold the date.
- You target audiences with packed calendars (top management, key clients) and you split registration into phases.

A save-the-date is nothing other than the Invitation e-mail in a different configuration. Same module, same system — you just hide the registration button and offer a calendar entry instead.

### Configuring the Invitation e-mail as a save-the-date

In the event admin, open the **Invitation e-mail** and make two changes in its settings:

- **Hide the registration button.** In the *Registration button* section, switch its visibility to hidden. The e-mail goes out with no CTA leading to the registration form — which does not yet need to be production-ready.
- **Add an ICS file for the calendar.** In the cover-image / attachment section, enable ICS. After opening the attachment the attendee adds the event to their calendar (Outlook, Google Calendar, Apple Calendar) in one click.

Write the body of the e-mail as a save-the-date message: a short text, the date, the location or "location to be confirmed", and the note that the full invitation will follow.

### Sending the save-the-date

You send a save-the-date the same way as a regular Invitation e-mail — through the *Sending* section of the Invitation e-mail module. If the entire contact list is already assigned to the event, use **bulk sending**. If you only target a small audience (for example VIPs), you can use **individual** sending by entering e-mail addresses one by one.

### Workflow: save-the-date → full invitation

A save-the-date is the **first step** of a two-stage communication. The second step comes later and has two variants:

- **A second Invitation e-mail after the switch.** After sending the save-the-date you edit the Invitation e-mail — turn the registration button back on, turn off the ICS (or keep it), edit the body text, and send to the same contact list again. Useful when you want to keep one logical thread.
- **An E-mail campaign as the full invitation.** Instead of switching the Invitation e-mail, send an **E-mail campaign** with the full registration button. Campaigns allow more precise targeting (by groups, by non-registered) and keep the history of multiple sends side by side. Most organizers in production pick this path — see *When to use the Invitation e-mail vs. an E-mail campaign*.

### What a save-the-date typically does not include

- **The ticket price** — if the event is paid, the save-the-date only announces the event and registration with payment comes in the second phase.
- **The full agenda** — 1–2 lines on what to expect are enough.
- **Detailed logistics** (parking, food, dress code) — those belong in the Confirmation e-mail and the day-before info mail.

## Common pitfalls

### A save-the-date goes out with the registration button enabled, the attendee clicks, and an empty registration form opens

Before sending, double-check that the registration button is hidden. Otherwise the attendee lands in an unfinished registration that does not yet have tickets / questions / pricing finalized, and a false-positive registration appears that you have to clean up by hand.

### The save-the-date and the full invitation go out close together

The point of a save-the-date is the lead time. If you send both e-mails the same week, the save-the-date loses its purpose and the attendee receives two similar e-mails for nothing. Plan a gap of **at least 4 weeks**.

### In phase two you send the full invitation as another Invitation e-mail, but to the same audience

If you want to target more precisely (only those who opened the save-the-date, or only those who did not), pick an **E-mail campaign** for phase two — it has targeting by *opened / did not open the Invitation e-mail*. The Invitation e-mail does not have that granularity; it always goes to all assigned contacts.

### The ICS file shows the wrong time in the attendee's calendar because the basic event settings are missing the time zone

ICS pulls the date and time straight from the event settings. If the **time zone** in the basic settings is wrong, an attendee in a different time zone gets the wrong time in their calendar. Verify the basic event settings before sending the save-the-date.

## Related articles

- [How the Invitation e-mail works](https://help.happenee.com/en/articles/39-how-the-invitation-e-mail-works)
- [Creating and sending an E-mail campaign](https://help.happenee.com/en/articles/41-creating-and-sending-an-e-mail-campaign)
- [When to use the Invitation e-mail vs. an E-mail campaign](https://help.happenee.com/en/articles/42-when-to-use-the-invitation-e-mail-vs-an-e-mail-campaign)
- [Targeting communication by groups and statuses](https://help.happenee.com/en/articles/43-targeting-communication-by-groups-and-statuses)
- [Communication flow before the event](https://help.happenee.com/en/articles/79-communication-flow-before-the-event)

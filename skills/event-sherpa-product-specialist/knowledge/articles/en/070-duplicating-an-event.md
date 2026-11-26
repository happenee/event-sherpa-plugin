# Copying the event

> Creating a new event from an existing one in the copy wizard: what you can carry over, what is never copied, and what to check after copying.

- Article in the Help Center: https://help.happenee.com/en/articles/70-copying-the-event
- Česká verze: https://help.happenee.com/cs/articles/70-kopirovani-udalosti
- Collection: Event setup and registration
- Updated: 2026-11-04

---

> [!info] Overview
> Copying an event creates a new event from an existing one. In the wizard you enter the new event's name and dates and choose what carries over from the original: registration and the Registration form, the enabled state of Tickets, the microsite, e-mails, campaign content, individual content and engagement features (with or without their content), and optionally the same attendees. Attendee responses, orders, tickets, check-in, and statistics are never copied. Use it for a recurring event or a series when you want to reuse a finished setup. You will find it under **Event settings**, on the **Danger zone** tab, behind the **Copy event** button.

## Getting started

- Decide whether copying is the right tool. It fits when the new event has a similar format and you only need to adjust the dates and content. For a genuinely different event, creating a new one from scratch is cleaner.
- Have the new event's name and dates ready. If you want to put the copied attendees into a group straight away, create the group beforehand in **Contacts and groups**; the wizard only offers existing groups.
- Open **Event settings → Danger zone** and click **Copy event**. The wizard has two steps: in the first you set up the new event, in the second you choose what to copy. Create the copy with **Create copy**; the admin then takes you to the new event's settings.

## Details

### Step 1: New event

- **New event name** is pre-filled as *Kopie {date} - {original event name}*. Replace it with the real name, because the microsite address is created from it as well.
- **Start and end** (date and time). The end is pre-filled from the original event's duration, and you can change it. Below the fields you can see the original event's dates for reference.
- **Agenda shift.** Sessions move by the same number of days as the start date; their times stay the same. Sessions that would fall outside the new dates after the shift are not copied at all, including their relations. The wizard warns you about this before you create the copy.
- **Event settings** — **Time zone**, **Event description**, and **Event graphics**. Checked settings are copied from the original event; unchecked ones you enter again: pick a different time zone (Agenda times stay the same in the new zone), write a new description, or leave it empty and add it later.
- **New event attendees** — the **Assign the same attendees** option adds the original event's attendees (without administrators) to the copy. They are assigned clean: no invitation, responses, attendance confirmation, or check-in. If the new event requires registration approval, the assigned attendees wait for approval. Optionally, **Add to group** puts them into a group; the membership is added to their existing groups.

Copying itself sends nothing. The assigned attendees receive no e-mail until you send an invitation or a campaign in the new event yourself.

### Step 2: What to copy

The event basics (name, dates, basic details, and languages) are always copied, and the time zone as chosen in step 1. Everything else you choose with checkboxes in three groups.

**Modules**:

- **Registration** — registration settings, fields and questions, accommodation, and approval rules.
- **Registration form** — the Registration form feature from the left menu.
- **Tickets** — only the enabled state of the Tickets module carries over. The tickets themselves, discount codes, and orders are not copied. The option is available only when the original event has Tickets turned on.
- **Microsite** — microsite texts and settings.
- **Invitation e-mail** and **Confirmation and approval e-mails** — the texts, subject, sender, and attachments of these e-mails.
- **Campaign content** — all e-mail campaigns of the original event, including those already sent, are copied with their content as new unsent campaigns. No recipients, send date and time, scheduling, or history. This option is off by default.

**Content features** and **Engagement features** — the list of the event's features, named the way you have them in the left menu. For each one you decide whether it is copied. For Agenda, Speakers, Sponsors, Exhibitors, Polls, Survey, Venue, Contact, and Custom content, the **Content** option also decides whether their items (sessions, speakers, poll questions…) are copied or only the empty feature. For the other features, the settings are copied; attendee history and interactions are not.

**Select all** and **Deselect all** set all options at once. On the right, the **Copy summary** keeps a running list of what will and will not be copied.

The wizard remembers your last successful selection and offers it again next time. You enter the name, dates, and group anew each time. Features that were not available the last time you copied stay off, and the wizard reminds you to review your selection.

### What is never copied

- Attendee responses and history: Registration form answers, votes, questions, chats, meetings, and check-in.
- Tickets, discount codes, orders, and ticket statistics, as well as payment settings and the sales end. At most, the enabled state of **Tickets** carries over.
- Push notifications, announcements, and campaign mailings.
- **Online module** settings. You cannot select it in the wizard; set it up again in the copy.
- Conditional questions and automatic group assignment in the Registration form, and accommodation rooms. The questions themselves are copied; set up the conditions and rooms again.

These are data from a specific run of the event, not setup. That is why the new event starts with no sales history and no sent messages.

## Common pitfalls

### The pre-filled name contains "Kopie" and a date

If you do not replace the pre-filled name in the wizard, the new event is called *Kopie {date} - {name}*, and the microsite address takes the same form. In the event's other language, the name always gets this form. After creating the copy, check the name in every language and, if needed, the microsite address before you send the first invitation. How to change the address is covered in [How the event microsite works](https://help.happenee.com/en/articles/21-how-the-event-microsite-works).

### Shorter dates leave part of the Agenda out

When you shorten the new event, sessions outside the new dates are not copied, and neither are their relations to speakers or sponsors. The wizard shows how many items will be left out. If you want to keep them, set the end late enough and adjust the Agenda in the copy.

### Relations between content need both features

A link between a speaker or sponsor and a session is copied only when you select both features including their content. Otherwise it is left out, and after creating the copy the admin warns you that some content relations are missing.

### Tickets have to be set up again in the copy

Even if you keep the **Tickets** option checked, only the module's enabled state carries over. Ticket types, payment settings, and discount codes are not in the copy, and the sales end goes back to the end of the event. Set up tickets in the new event again before you open registration, or there will be nothing to sell.

### Private messages and meeting bookings in Networking are off

Even if you copy Networking, its **Turn on private messages** and **Turn on the meeting booking system** options are off in the new event. If you want to use them, turn them on again in the Networking settings.

### The legacy Agenda is not copied

If the event uses the legacy Agenda (the older content feature for the event schedule, which new events no longer offer), it is unavailable in the wizard, and the wizard explains why. Everything else you selected is copied as usual. Add the current Agenda in the new event and create the sessions there again; the steps are in *Building the event Agenda — architecture*.

### Copying sits in Danger zone right next to permanent deletion

The same tab also holds **Delete event**, which removes the event **permanently**. **Copy event** is safe — it only opens the wizard and creates a new event — but deletion is not. Check which button you are clicking before you click.

## Related articles

- [Creating a new event](https://help.happenee.com/en/articles/9-creating-a-new-event)
- [Recommended order for setting up an event step by step](https://help.happenee.com/en/articles/8-recommended-order-for-setting-up-an-event-step-by-step)
- [How the event microsite works](https://help.happenee.com/en/articles/21-how-the-event-microsite-works)

# Targeting communication by groups and statuses

> The two axes of targeting in Happenee: attendee statuses and the groups they belong to.

- Article in the Help Center: https://help.happenee.com/en/articles/43-targeting-communication-by-groups-and-statuses
- Česká verze: https://help.happenee.com/cs/articles/43-cileni-komunikace-podle-skupin-a-stavu
- Collection: Communication and invitations
- Updated: 2026-09-21

---

> [!info] Overview
> Communication targeting in Happenee runs on two axes — **attendee statuses** (where the contact is in the registration flow) and **groups** (what the contact belongs to). Statuses update automatically; groups are managed by you, created up front and filled by import, registration, tickets, discount codes, registration form answers, or manually. An E-mail campaign targets both; the Invitation e-mail targets only statuses. The language of the e-mail is also chosen by the contact's **preferred language**.

## Getting started

- Think **up front** about which groups you will need. A new rule may not add earlier attendees retroactively. You can repair missing membership manually or by import; verify the result.
- When importing contacts, fill in the **preferred language** column — the system uses it to pick the language variant.
- Be aware of the difference: **statuses** are automatic (what the contact has reacted to), **groups** are manual (what role or segment the contact has).
- For segmented communication (only VIPs, only speakers, only Czech contacts) use an **E-mail campaign**. The Invitation e-mail targets only by status.

## Details

### Attendee statuses

A status describes where the attendee is in the registration process or during the event. The system controls the status; you only observe it (with the exception of a manual flip).

In an E-mail campaign, each status is its own send button on the **Sending** tab:

- **All** — every contact assigned to the event.
- **Registered** — completed registration.
- **Not invited** — the contact is assigned to the event but has not yet been sent the Invitation e-mail.
- **No reaction** — they received the invitation but have not reacted in any way.
- **Did not read the invitation e-mail** — based on open tracking.
- **Attendees on site** — people who have physically arrived at the event.
- **Viewed the web application** / **Did not view the web application** — whether the attendee has already opened the event's web app, meaning the attendee app in a browser.

How many contacts fall into each status is shown before you click anything, in the **Contacts assigned to the event** overview on the same tab. The Invitation e-mail offers a narrower set of statuses (*Not invited*, *Did not open the Invitation e-mail*, *Not registered*) and cannot combine them with groups.

**Reach mobile app users with Notifications.** The campaign send buttons track the web app. To target people who have the mobile app, use **Notifications** in the attendee app, which targets the mobile and web app separately (see *Using Notifications in the attendee app*).

### Groups — how people land in them

Groups are always created by the organizer, never by the system. A contact can land in a group through several paths:

- **Manual assignment in Contacts and groups** — you select a contact and add them to a group.
- **Bulk import with `#group`** — you use the prefix in the group column of an Excel import. Detail in *Managing contacts and groups in your workspace*.
- **After registration with a ticket** — in the ticket settings you choose which group the attendee joins after they finish registration.
- **Through an individual or bulk registration link** — for the link you choose the group assigned after registration (typically a partner link → group "Partner XY").
- **After using a discount code** — the code can assign to a group ("Group after using the code").
- **By an answer in the Registration form** — for question types that can assign to a group (single choice from options). For example, the answer "I will travel by bus 2" → group "Bus 2".
- **After registering for a workshop or time slot** — the attendee of workshop A lands in group "Workshop A".

### What groups are used for in communication

- **E-mail campaign targeting** — send the campaign only to the VIP group, only to speakers, or only to the "Czech" group.
- **Notification targeting** in the attendee app — the notification reaches only the group it is relevant for.
- **Visibility of features** — some content and engagement features are visible only to a group (detail in *Working with groups and visibility*).
- **On-site scanning** — event staff see on the QR code whether the attendee belongs to a selected group (VIP, speaker).

### Language fallback at import

The e-mail language is not driven by the event language — it is driven by the contact's **preferred language**. That is why you fill in the language column at import.

Three situations:

- The contact has preferred language **Czech** → receives the Czech variant of the e-mail.
- The contact has preferred language **English** → receives the English variant.
- The contact has **no language** → the primary language of the event is used (statistics show "X contacts without language").

When the attendee registers from the microsite, the preferred language is set automatically based on which language they opened the microsite in.

### Typical segmentations in practice

- **VIPs and speakers** — separate e-mails with details about badge pickup, the hotel, or the main rehearsal.
- **English-speaking only** — a separate campaign with a different tone or format.
- **Only unregistered** — a re-invitation that does not bother people who already responded.
- **A group from a ticket** — if you have three ticket types and only one grants access to the VIP lounge, send the campaign only to holders of that ticket.
- **A group from a workshop** — a reminder two hours before the workshop so attendees do not forget to show up.
- **Partners** — every partner has their own bulk registration link that assigns attendees to the group "Partner XY"; targeted communication only to them.

### Combining statuses and groups in a campaign

In an E-mail campaign you can combine filters — for example:

- "Registered + group VIP" → VIP reminder.
- "No reaction + group Czech contacts" → re-invitation in Czech.
- "Viewed the web application + group Speakers" → quick info to speakers who have already opened the web app.

You pick the group in the **Targeting** dropdown first, and only then click the status button.

### Limits — local and system groups

Today in Happenee only **global user groups** work — you create them manually and they apply across the workspace. Two extensions are planned:

- **Local groups** — groups limited to a single event so that the global list does not get cluttered. **Planned, not available today.**
- **System groups** — automatically created from statuses (for example *Confirmed attendees*, *Registered*). **Planned, not available today.**

For now, name and manage groups manually, and remember that statuses (registered, on-site) are not automatic groups but statuses — target them with the status filter, not with a group.

### Check the specific audience before sending

Decide what the recipient needs to do. Then verify the group, current registration status, language, and destination link. Do not ask a registered attendee to register again solely because no e-mail open was recorded. A missing open record does not prove that the recipient did not read the message.

When correcting a wrong assignment, compare the form answer and the group membership. If the group also controls visibility or access, check that effect as well. Test the change with a suitable test contact, then verify the actual audience before sending.

## Common pitfalls

### The group needed for follow-up was not prepared in time

Plan and create groups **before opening registration**. Set the filling rules (from tickets, from form answers, from discount codes, from workshops) so that groups fill themselves.

### An organizer imports contacts without a language and then wonders why English-speaking attendees got the Czech invitation

At import, fill in the **preferred language** column. If it is missing, add it later in Contacts and groups (individually or by repeating the import).

### An organizer wants to target a group with the Invitation e-mail and cannot make it work

The Invitation e-mail **cannot target by groups**, only by statuses. Use an E-mail campaign for group targeting.

### An organizer expects an automatic *Registered* group to appear after registration and plans to target it

These automatic groups **do not exist today**. In a campaign, use the *Registered* send button as the status filter. System groups are planned but not yet available.

### An organizer relies only on statuses and loses the ability to send different messages to different segments ("only VIP", "only this ticket")

Add groups to the workflow — through tickets, the form, and discount codes. Once you set up the rules that fill groups, you get segmentation for free.

### An organizer creates *too many* groups, loses track of them, and communication becomes unmanageable

Keep the count reasonable — typically 5–15 for a mid-size event. Groups that you do not use for communication or visibility are not worth maintaining.

## Related articles

- [Managing contacts and groups in your workspace](https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace)
- [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility)
- [Creating and sending an E-mail campaign](https://help.happenee.com/en/articles/41-creating-and-sending-an-e-mail-campaign)
- [How the Invitation e-mail works](https://help.happenee.com/en/articles/39-how-the-invitation-e-mail-works)
- [When to use the Invitation e-mail vs. an E-mail campaign](https://help.happenee.com/en/articles/42-when-to-use-the-invitation-e-mail-vs-an-e-mail-campaign)
- [Using the Invitation e-mail as a save-the-date](https://help.happenee.com/en/articles/63-using-the-invitation-e-mail-as-a-save-the-date)
- [Interpreting attendee statistics](https://help.happenee.com/en/articles/51-interpreting-attendee-statistics)
- [Using Notifications in the attendee app](https://help.happenee.com/en/articles/46-using-notifications-in-the-attendee-app)
- [Communication flow on the event day](https://help.happenee.com/en/articles/64-communication-flow-on-the-event-day)
- [Planning follow-up communication after the event](https://help.happenee.com/en/articles/65-planning-follow-up-communication-after-the-event)
- [Communication flow before the event](https://help.happenee.com/en/articles/79-communication-flow-before-the-event)
- [Tracking e-mail and campaign deliverability](https://help.happenee.com/en/articles/80-tracking-e-mail-and-campaign-deliverability)
- [What to do when a campaign will not send or arrives in the wrong language](https://help.happenee.com/en/articles/88-what-to-do-when-a-campaign-will-not-send-or-arrives-in-the-wrong-language)

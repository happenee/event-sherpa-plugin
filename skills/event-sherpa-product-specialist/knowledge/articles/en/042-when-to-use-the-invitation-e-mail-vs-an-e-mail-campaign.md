# When to use the Invitation e-mail vs. an E-mail campaign

> The Invitation e-mail for the first wave after importing contacts, a campaign for everything else.

- Article in the Help Center: https://help.happenee.com/en/articles/42-when-to-use-the-invitation-e-mail-vs-an-e-mail-campaign
- Česká verze: https://help.happenee.com/cs/articles/42-kdy-pouzit-zvaci-e-mail-a-kdy-e-mailovou-kampan
- Collection: Communication and invitations
- Updated: 2026-09-21

---

> [!info] Overview
> In Happenee there are two modules for outbound e-mails side by side — the **Invitation e-mail** and **E-mail campaigns**. Organizers often confuse them. Short rule: send the **Invitation e-mail** as the **first wave of invitations** after you import contacts. For everything else (reminders, follow-ups, segmented messages, follow-up invitations to new contacts), use **campaigns**. Campaigns do everything the Invitation e-mail does, plus group targeting, scheduling, and follow-up to newly assigned contacts.

## Getting started

- If you are sending the very first invitation to assigned contacts and you only need to target by status (not invited), the **Invitation e-mail** is fine.
- If you need to target a specific group (VIPs, speakers, one language), schedule a send for a date, or use a different header from the rest of the event — use a **campaign**.
- For most larger events, it is simpler and cleaner to **handle everything through campaigns**, including the first invitation.

## Details

### What the Invitation e-mail can and cannot do

The Invitation e-mail is a **legacy module** in the product — it predates campaigns. It has:

- An editor with variables.
- A registration button (direct or public link).
- Individual sending (one by one) and bulk sending by **attendee status**:
  - *Not invited* — who has not yet received the Invitation e-mail.
  - *Did not open the Invitation e-mail*.
  - *Not registered (no response)*.

It does not have:

- **Targeting by groups**.
- **Scheduling** a send to a specific date.
- A **custom header image** for an individual send.
- **Resending to newly assigned contacts** without affecting history.
- Reporting connections at the same scale as campaigns.

### What campaigns add on top

An E-mail campaign covers everything the Invitation e-mail does and adds:

- **Targeting by groups** (VIPs, speakers, language, a group from a discount code, and so on).
- A **scheduled send** to a specific date and time.
- A **custom header image** used only for that campaign.
- **Resend campaign to newly assigned** — sends only to contacts that joined the event after the mailing started.
- A **PDF ticket with a QR code** as an attachment (typically the morning e-mail on event day).
- A **history of mailings** with per-recipient delivery tracking.

### Typical use case for the Invitation e-mail

**The first wave of invitations after import.** You import a contact list, assign them to the event, double-check the invitation text, and in the Invitation e-mail you choose to send to "Not invited." All assigned contacts then receive the first invitation in a single, consistent form. For this step, the Invitation e-mail is ready to go and this is its historical role.

### Typical use cases for campaigns

- **Reminder one week / three days / one day before the event** — schedule it ahead, it goes out by itself.
- **Guest list for a paid event** — a campaign set to *Individual free admission*, sent to a selected list of imported contacts.
- **Follow-up to non-responders** — target only the *No reaction* status with a softer tone.
- **Info for VIPs or speakers** — target the group, send them special information that others do not get.
- **Morning e-mail on event day** — the ticket with the QR code and a short text, targeted to the *Registered* status.
- **Post-event follow-up** — thank-you, photos, a link to feedback.
- **Different segments by language** — when you want a different text for Czech speakers than for English speakers.
- **Reaching new sign-ups** — run the campaign again with *Resend campaign to newly assigned* so only the newcomers receive it.

### Why people confuse them

The product author puts it openly: organizers find themselves "drowning a bit in the fact that there's an Invitation e-mail and there are E-mail campaigns." Organizers ask why there are two modules and do not know which one to reach for.

The reason is historical — the Invitation e-mail came first. Campaigns were added because organizers needed to target by groups, schedule, and follow up. Consolidation into a single module is on the roadmap, but right now both are in the product.

### Direction over time

The product is moving long-term toward routing **all invitation communication through campaigns**. If you run repeating, similar events, get used to using campaigns even for the first invitation — you will save yourself the habit change once the Invitation e-mail merges into campaigns.

### Decision rule

- **First invitation, all assigned contacts, one text** — Invitation e-mail *(or campaign — both fine)*
- **Invitation only for VIPs / speakers / one group** — Campaign
- **Reminder on a specific date** — Campaign (scheduled)
- **Follow-up invitation to no-response** — Invitation e-mail *(by status)* or campaign *(status + group)*
- **Campaign for new sign-ups** — Campaign (*Resend campaign to newly assigned*)
- **Free guest list at a paid event** — Campaign *(Individual free admission)*
- **Post-event follow-up** — Campaign
- **Morning ticket on event day** — Campaign (with PDF ticket attached)
- **Custom header for a single send** — Campaign

### Heads-up — the Confirmation e-mail is a third thing

Invitation e-mail ≠ Confirmation e-mail ≠ campaign. The Confirmation e-mail is sent **automatically** after registration and has its own module. The Invitation e-mail and campaigns are for **active outreach** — you decide when they go out.

## Common pitfalls

### An organizer wants to invite only VIPs but does it through the Invitation e-mail, where group targeting does not exist

To target a specific group, use a **campaign**. The Invitation e-mail targets only by status.

### An organizer sets up a reminder one week before the event in the Invitation e-mail and waits for the system to send it

The Invitation e-mail **cannot schedule a send**. For timing on a specific date, use a campaign and choose *Schedule send*.

### An organizer sends the same invitation again to everyone because they want to reach new sign-ups — and the original recipients receive it for the second time

On the sent campaign, open the **Mailings** tab, use the **Resend campaign to newly assigned** panel and the **Newly assigned** button. Only the people who have not received it yet get the campaign.

### An organizer does not understand why two modules exist side by side and uses the Invitation e-mail for everything, complicating segmentation

If your routine includes reminders, follow-up invitations, or group targeting, start using **campaigns as your main channel**. Keep the Invitation e-mail for a simple first invitation, or skip it altogether and send the first invitation as a campaign too.

## Related articles

- [How the Invitation e-mail works](https://help.happenee.com/en/articles/39-how-the-invitation-e-mail-works)
- [Creating and sending an E-mail campaign](https://help.happenee.com/en/articles/41-creating-and-sending-an-e-mail-campaign)
- [Targeting communication by groups and statuses](https://help.happenee.com/en/articles/43-targeting-communication-by-groups-and-statuses)
- [How the Confirmation e-mail works](https://help.happenee.com/en/articles/40-how-the-confirmation-e-mail-works)
- [Managing contacts and groups in your workspace](https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace)
- [Using Notifications in the attendee app](https://help.happenee.com/en/articles/46-using-notifications-in-the-attendee-app)
- [Using the Invitation e-mail as a save-the-date](https://help.happenee.com/en/articles/63-using-the-invitation-e-mail-as-a-save-the-date)
- [Planning follow-up communication after the event](https://help.happenee.com/en/articles/65-planning-follow-up-communication-after-the-event)
- [Communication flow before the event](https://help.happenee.com/en/articles/79-communication-flow-before-the-event)

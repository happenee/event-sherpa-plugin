# Creating and sending an E-mail campaign

> The module for bulk e-mailing with group and status targeting, scheduled sending, and delivery tracking.

- Article in the Help Center: https://help.happenee.com/en/articles/41-creating-and-sending-an-e-mail-campaign
- Česká verze: https://help.happenee.com/cs/articles/41-vytvoreni-a-odeslani-e-mailove-kampane
- Collection: Communication and invitations
- Updated: 2026-09-23

---

> [!info] Overview
> An E-mail campaign is the tool for **bulk messaging to contacts and attendees assigned to an event** — reminders, follow-ups, segmented messaging, and the ticket e-mail on event day, in short everything except the initial invitation. Unlike the Invitation e-mail, it can target by groups and statuses, schedule delivery for a specific date and time, and use its own header image. One campaign is not one send — it holds a **history of individual mailings** and can resend the campaign to contacts that were added to the event later. You can **cancel** a scheduled mailing (the campaign and its content stay) and **delete** a whole campaign (irreversibly, including its mailing statistics); a campaign that has already gone out cannot be taken back, so you fix it with a copy.

## Getting started

- Decide **what you want to send and to whom** — a reminder for everyone, info just for VIPs, a re-invitation for people with no reaction, or the morning ticket on event day.
- Prepare the content **in every language of the event** — while any language is missing a subject or content, the campaign cannot be sent or scheduled (see below).
- Decide whether the campaign uses the **header image from the event settings** or gets its own **custom header image**.
- Send yourself a **test campaign** before you send for real — once a campaign goes out, the content can no longer be edited.
- If the campaign is meant for a specific date, **schedule the delivery** instead of sending immediately.

## Details

### Where to find E-mail campaigns

Open the event's left menu and pick the **E-mail campaigns** module. The module has two tabs: **Campaigns** (the list of campaigns for this event) and **Mailings** with a count badge — every mailing across all campaigns.

The campaign list shows the **Campaign name**, **E-mail subject**, **Targeting**, **Campaign status** (*Not planned* for a campaign that has not gone out yet, *Planned* while it waits for its scheduled time, *Sent* once it has gone out), and **Campaign send date**. On the right there is an **Edit** button and, next to it, a **…** icon that opens a menu with **Copy**, **Cancel mailing**, and **Delete campaign**; a sent campaign also has **E-mails**. The last two are destructive and easy to mix up — the difference is covered in *Stopping, changing, and deleting a campaign* below.

### Creating a new campaign

The **New campaign** button opens a dialog asking for two required things:

- **Campaign name** — an internal identifier that helps you find the campaign in the admin. The attendee never sees it, so name it so that you still recognize it in three months: *Reminder one week out* beats *Campaign 3*.
- **E-mail subject** — what the recipient sees in their inbox.

You can change both later — the name on the **Settings** tab, the subject on the **Content** tab.

### How the campaign detail is organized

The campaign detail has four tabs, in this order:

- **Content** — subject, e-mail body, registration button, placeholder variables.
- **Settings** — campaign name, header image, attachments, sender and reply-to recipient.
- **Sending** — test campaign, targeting, scheduling, and the send itself.
- **Mailings** — the history of mailings that went out, delivery tracking, and resending to newly assigned contacts. The badge on the tab tells you how many mailings the campaign already has.

The header above the tabs always shows the **campaign status** (*Planned*, *Sent*), the mailing date and time, and the number of recipients. A campaign with a scheduled mailing also shows an orange bar below the header, with a lock icon and a note that a mailing is scheduled for that date and time. That bar is the explanation for why the fields on the **Content** tab are grayed out and cannot be edited.

### Campaign content

- **E-mail subject** — required.
- **E-mail content** — open the body with the **Edit** button. It is the same editor as the Invitation e-mail and the Confirmation e-mail.
- **Placeholder variables** — the list of variables the system replaces with the individual attendee's data on send (name, event name, date and time, location, QR code for entry, and others). You insert them into the text as characters like `::UZIVATEL_JMENO::`. They work the same way across the microsite, the Invitation e-mail, the Confirmation e-mail, and campaigns — details in *How the Invitation e-mail works*. Below the universal ones you also get **placeholders for custom contact fields**; those are generated from the custom contact fields in your own workspace, so they look different in every workspace.

### Registration button

There are three things to set for the button:

- **Button text** — required, and it is up to you.
- **Button position** — *Above the content*, *Below the content*, *Above and below the content*, or *Hide*. For a long e-mail, *Above and below the content* saves the attendee from scrolling back up. For a purely informational message with nothing to register for, pick *Hide*.
- **Where should the registration button lead?** — *Personal recipient link* (a link tied to one specific contact), *Public link* (the recipient enters any e-mail address and continues; the link can be shared publicly), and at a paid event also *Individual free admission* (the recipient registers without buying a ticket).

**A guest list at a paid event** is what *Individual free admission* is for: import 50 contacts, send them a campaign with that option, and they register without the paid checkout. A personal link cannot do this — at a paid event it leads to ticket purchase. More in *Personal link vs. public link: what is the difference*.

### Campaign settings

- **Header image** — *Use event settings* uses the same header as the Invitation e-mail, meaning the event cover image from **Event settings → Graphics settings** (the event icon with name and date, or the image you uploaded for the event). *Custom header image* lets you upload an image just for this campaign. It is useful for a VIP invitation or a reminder with a different visual. The recommended width is 1300px at a 3:1 aspect ratio, in JPG format up to 500 KB.
- **Attachments** — two separate toggles: **ICS file** (adds the event to the calendar) and **Ticket in PDF** (the ticket with a QR code). The typical scenario for the PDF ticket is the morning e-mail on event day.
- **Campaign sender and reply-to recipient** — **Sender name**, **Reply-to e-mail**, **Reply-to name**, and **Company**. This setting is **unique to this campaign**, so it does not overwrite the event or workspace settings.

At the very bottom of the **Settings** tab there is a red-bordered **Delete campaign** section — see *Stopping, changing, and deleting a campaign* below.

### Targeting and sending

The **Sending** tab has three blocks.

**Test campaign** — enter an e-mail address, pick a language, and send yourself a test campaign. If that language is missing a subject or content, the test is blocked and the dialog tells you what to complete. An incomplete language that you did not select does not block this test, so test each language separately.

**Send campaign** — this is where you decide who and when:

- **Targeting** — a dropdown of groups. You can pick **several at once**; each selected group appears as a chip you can remove. If you select no group, the campaign goes to *everyone*.
- **Schedule** — either *Send immediately* or *Schedule delivery for a later date*. When scheduling, you set both the date and the time.
- **Send buttons** — you start the send with the button matching the attendee status: **All** · **Registered** · **Not invited** · **No reaction** · **Did not read the invitation e-mail** · **Attendees on site** · **Viewed the web application** · **Did not view the web application**. The last two tell apart attendees who have already opened the event's web app, meaning the attendee app in a browser, from those who have not. The status combines with the group targeting — clicking *Registered* with the VIP group selected sends the campaign only to registered VIPs.

A confirmation dialog appears before the send, showing the number of selected attendees. The final count can differ slightly — statuses can change in the meantime.

**Contacts assigned to the event** — an overview of how many contacts fall into each status before you click anything. Below it is a **Users' default language** breakdown showing how many recipients have which preferred language. It is the fastest pre-send check: if you see 40 English contacts and you have not filled in the English version, you find out in time. From here you can also jump to **Managing contacts and groups**.

Sending a large number of e-mails can take several hours. Do not change the campaign content during that time.

### One campaign, several mailings

A campaign is not a single send. It is a wrapper that holds a **history of mailings** — every run, including a resend to newly assigned contacts, creates a **new mailing**. You find them on the **Mailings** tab, in a table with the columns **Campaign send date**, **Number of e-mails**, **Delivery status**, and **Actions** (the trash icon and the **E-mails** link).

A mailing runs first as in progress and ends as *Sent*. While it is still running you can delete it with the trash icon on its row; once it finishes, you cannot. The **Show test mailings** toggle adds the test campaigns you sent to yourself into the table — they are hidden by default so they do not clutter the history.

The practical consequence: you do not need a new campaign for every wave. A single "Reminder one week out" campaign can have three mailings as registrants keep coming in — and you see them all in one place.

### Resending to newly assigned contacts

The **Mailings** tab has a **Resend campaign to newly assigned** panel. It shows the number of **newly assigned contacts** — the ones that joined the event or the group **after the mailing started**. It does not matter how they got there: an organizer can assign them manually, or they can register themselves or buy a ticket.

The **Newly assigned** button sends the campaign to those contacts only. The original recipients do not get it a second time. While there is nobody to resend to, the button stays inactive.

How it is used: you send the campaign to 200 registrants, a week later 30 more people register, you click *Newly assigned*, and the campaign goes only to those new contacts. The Invitation e-mail does not have this logic.

### Stopping, changing, and deleting a campaign

Once a campaign is scheduled or sent, the content **cannot be edited**. This is a safety measure so you do not change the text at the moment part of the mailing could already be going out. What you do next depends on the campaign status:

- **Not planned** — the campaign is not going anywhere yet, so edit it freely.
- **Planned** — click **Cancel mailing**, either in the campaign header or in the **…** menu on the list row. The confirmation dialog tells you that the e-mails will not go out and that you can schedule the mailing again. Only the schedule is canceled, so **the campaign and its content stay**. Edit the campaign and then **schedule the delivery again** — without that step it will not go out at all.
- **A mailing that is already running** — stop it with the **trash icon** on its row on the **Mailings** tab. Once the mailing finishes and reaches *Sent*, the icon is gone.
- **Sent** — there is no way back. Use **Copy campaign** in the campaign header, or **Copy** in the **…** menu on the row in the campaign list. Both create a new campaign with the same content and settings. The copy is named after the original with a *- copy* suffix and starts in the *Not planned* status. Rename it, edit it, and send it as a separate campaign.

Keep two terms apart, because they are easy to confuse: a **campaign** is the wrapper holding the content and settings, while a **mailing** is one specific run. *Cancel mailing* cancels the schedule, the trash icon deletes a single mailing — and in both cases the campaign itself survives.

### Deleting a campaign

There are two ways to delete a whole campaign:

- the red-bordered **Delete campaign** section at the very bottom of the **Settings** tab,
- or **Delete campaign** in the **…** menu on the campaign's row in the list.

Both lead to a confirmation dialog where you either keep the campaign or confirm the deletion. Deleting removes the **campaign content, the targeting settings, and the mailing statistics**, and any scheduled e-mails will not go out. **The action cannot be undone** — the campaign is not moved anywhere and cannot be restored.

Deleting makes sense for test campaigns and ones created by mistake, for duplicates left behind by repeated copying, and for campaigns you prepared and then decided not to send. In other words, wherever neither the content nor the history matters to you.

**When to reach for something else:**

- You only want to **stop the send** and keep the campaign → *Cancel mailing*, not *Delete campaign*.
- You want to **fix a campaign that has already gone out** → copy it and edit the copy. A sent campaign can be deleted too, but deleting also removes the **mailing statistics**, so you would lose the full delivery history: who received the e-mail, who never got it, and who opened it. That data is your only record of what went out to whom, and you cannot get it back.
- You want to **tidy up the list** and the campaign has mailings behind it → leave it alone. The history of sent campaigns is part of the event's reporting.

### Delivery tracking

The **Mailing status** block on the **Mailings** tab shows a donut chart broken down into **To be sent**, **Sending**, **Delivered and unread**, **Delivered and read**, and **Not delivered**. This is the first place to look when someone claims nothing arrived — the *Not delivered* value separates a delivery problem from an e-mail that simply nobody opened.

The **E-mails** link (on the mailing row and in the campaign header) takes you to the **per-recipient detail** — for each address you see whether the e-mail was sent, delivered, and opened, and whether anyone clicked the button. A row expands into a **preview of the e-mail exactly as it went out** to that person. That is a reliable way to verify that the variables were filled in and that the right language version was sent.

### Typical use cases

- **Reminders** — "The event starts in a week, here is the agenda."
- **Re-invitation for people with no reaction** — reactivation of those who did not react to the Invitation e-mail.
- **Info for VIPs and speakers** — targeted only at their group; nobody else receives these messages.
- **Segmented invitations** — a Czech campaign for Czech contacts, an English one for international contacts, each with its own header image.
- **Morning e-mail on event day** — a ticket with the QR code and a short text; typically sent an hour before doors open.
- **Follow-up** — thank-you, link to the survey, photos, the recording.

### Languages

You fill the campaign content in one language. Then you switch **Content language** in the top right corner to the next event language and fill it in there too — subject, body, and button text if you use one. Each recipient gets the campaign in their preferred language. Anyone who has no preferred language set, or whose language is not among the event's active languages, gets the event's primary language.

The campaign goes out only once every event language has both a subject and content. If one is missing, clicking a send button opens the *Campaign is not ready to send* dialog. It names each affected language and says whether its e-mail subject, content, or both are missing. Nothing is sent or scheduled at that point. Close the dialog with **Close**, fill in the missing fields on the **Content** tab, and send again. The same applies to a scheduled mailing and to resending the campaign to newly assigned contacts.

Before the real send, send yourself a test campaign in each language separately. You see how the e-mail actually looks in that language, including the filled-in placeholder variables.

## Common pitfalls

### An organizer clicks send and gets *Campaign is not ready to send* instead of a mailing

One of the event languages has no subject or no content; the dialog names the language and missing field. Switch **Content language** to that language, fill in the missing field, and send the campaign again. Every event language has to be filled in regardless of targeting, so this applies even to a campaign meant only for Czech contacts. To see how many recipients each language affects, check the *Users' default language* breakdown in **Contacts assigned to the event**.

### An organizer wants to edit a scheduled campaign, but the fields on the Content tab cannot be edited

The reason is in the orange bar below the header, which says a mailing is scheduled for a given date and time. Unlock the scheduled campaign with **Cancel mailing** first (only the schedule is canceled, the content stays), then edit it. Watch out for the second half: you then have to **schedule the delivery again**, otherwise the campaign never goes out.

### An organizer wants to stop a send and deletes the whole campaign instead

**Cancel mailing** and **Delete campaign** are two different things, even though they sit next to each other in the **…** menu and both are styled as destructive. **Cancel mailing** stops only the delivery and leaves the campaign alone — the text, the targeting, and the settings all stay, and you can schedule the mailing again. **Delete campaign** removes the content and the targeting, and it cannot be undone. When you only need to buy time or fix a typo, use **Cancel mailing**.

### An organizer tidies up the campaign list and deletes sent campaigns too

**Delete campaign** works on a sent campaign as well, and nothing stops you — but it also removes the **mailing statistics**. On a sent campaign that wipes the entire delivery history: who the e-mail went to, who never received it, and who opened it. You cannot get it back, and you lose the only record of what was sent to whom. Leave sent campaigns in the list; if the clutter bothers you, consistent naming helps more.

### An organizer looks for a way to delete a campaign and cannot find it in the list

In the campaign list, **Delete campaign** is hidden behind the **…** icon next to the **Edit** button. The second route is through the campaign detail — the red-bordered **Delete campaign** section at the very bottom of the **Settings** tab.

### An organizer finds a typo in a campaign that has already been sent and looks for where to fix it

A sent campaign cannot be fixed. Use **Copy campaign** in the campaign header (in the campaign list, it is **Copy** in the **…** menu), correct the copy, and send it as a new campaign. Set the targeting so that only the people it concerns receive the correction.

### An organizer sends a campaign with a ticket on the morning of the event and attendees do not receive the PDF

In the campaign settings, turn on the **Ticket in PDF** toggle. The body of the e-mail does not attach it on its own.

### After a campaign is sent, more registrants come in, and the organizer resends the whole campaign to everyone, so the original recipients receive it a second time

Use the **Resend campaign to newly assigned** panel and the **Newly assigned** button. Only the people who have not received it yet get the campaign.

### An organizer creates a new campaign for every wave and loses track of who already received what

One campaign holds several mailings. The history is on the **Mailings** tab — for each mailing you see the date, the number of e-mails, and the delivery status. A new campaign makes sense for different content, not for the same content going to more people.

### An organizer targets only by status (for example "Registered") and is missing group targeting (for example only VIPs)

Pick the group in the **Targeting** dropdown first, and only then click the status button. The Invitation e-mail has no groups filter, which is exactly why the campaign is the tool for segmented messaging.

### An attendee claims the e-mail never arrived and the organizer has no way to verify it

Open **E-mails** for that mailing and find the address. You see whether the e-mail was sent, delivered, and opened, and you can display the exact message. *Not delivered* in the donut chart is a different problem from an unread e-mail and is fixed differently.

## Related articles

- [How the Invitation e-mail works](https://help.happenee.com/en/articles/39-how-the-invitation-e-mail-works)
- [How the Confirmation e-mail works](https://help.happenee.com/en/articles/40-how-the-confirmation-e-mail-works)
- [When to use the Invitation e-mail vs. an E-mail campaign](https://help.happenee.com/en/articles/42-when-to-use-the-invitation-e-mail-vs-an-e-mail-campaign)
- [Targeting communication by groups and statuses](https://help.happenee.com/en/articles/43-targeting-communication-by-groups-and-statuses)
- [Personal link vs. public link: what is the difference](https://help.happenee.com/en/articles/44-personal-link-vs-public-link-what-is-the-difference)
- [What to do when an e-mail does not arrive](https://help.happenee.com/en/articles/58-what-to-do-when-an-e-mail-does-not-arrive)
- [What to do when an attendee loses the registration link](https://help.happenee.com/en/articles/59-what-to-do-when-an-attendee-loses-the-registration-link)
- [Interpreting event statistics](https://help.happenee.com/en/articles/50-interpreting-event-statistics)
- [Using Notifications in the attendee app](https://help.happenee.com/en/articles/46-using-notifications-in-the-attendee-app)
- [What to do when there is a check-in issue](https://help.happenee.com/en/articles/62-what-to-do-when-there-is-a-check-in-issue)
- [Using the Invitation e-mail as a save-the-date](https://help.happenee.com/en/articles/63-using-the-invitation-e-mail-as-a-save-the-date)
- [Communication flow on the event day](https://help.happenee.com/en/articles/64-communication-flow-on-the-event-day)
- [Planning follow-up communication after the event](https://help.happenee.com/en/articles/65-planning-follow-up-communication-after-the-event)
- [How placeholder variables work](https://help.happenee.com/en/articles/78-how-placeholder-variables-work)
- [Tracking e-mail and campaign deliverability](https://help.happenee.com/en/articles/80-tracking-e-mail-and-campaign-deliverability)
- [What to do when a campaign will not send or arrives in the wrong language](https://help.happenee.com/en/articles/88-what-to-do-when-a-campaign-will-not-send-or-arrives-in-the-wrong-language)

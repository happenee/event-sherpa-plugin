# Creating a new event

> What you fill in when creating a new event and which choices are permanent.

- Article in the Help Center: https://help.happenee.com/en/articles/9-creating-a-new-event
- Česká verze: https://help.happenee.com/cs/articles/9-vytvoreni-nove-udalosti
- Collection: Event setup and registration
- Updated: 2026-09-09

---

> [!info] Overview
> Creating a new event is the entry point into event setup in Happenee. It is not just filling in a form — when you create the event you commit to a few decisions that you cannot change later without starting a different event. The primary language is the typical example. This article explains what you fill in, which choices are permanent, and what happens immediately after the event is created.

## Getting started

- Decide the basic parameters before you click **+ New event**: name, date and time, type (In-Person / Virtual / Hybrid), and which languages you plan to offer.
- Decide on the **primary language** — this decision cannot be changed after the event is created.
- You do not need to know yet whether the event is paid. Tickets are turned on later in the event settings.
- The icon, description, and graphics can be added later. Do not slow yourself down with them at creation time.

## Details

### Where the event is created

In the workspace home screen (the **Upcoming / Past / All** switcher), click **+ New event**. An edit panel opens where you fill in the basic information one field at a time. After you confirm with **✓ Create event**, the event appears in the list and its **Overview** opens.

### What you fill in at creation

**Event name.** Shown in the workspace event list, on the microsite, in the attendee app, and in the Invitation e-mail and Confirmation e-mail.

**Event icon.** A square image that represents the event in the attendee app event list, in the ticket purchase flow, in the default microsite header, and in e-mails. It is not required up front — you can add it later in **Event settings → Graphics settings**.

**Time zone.** Set automatically based on your browser, but verify it. A common mistake is planning an event in Prague from a browser whose time zone is set elsewhere.

**Event start** and **End of event.** For a multi-day event, the end refers to the final day.

**Event description.** Optional. There is no need to fill it in at creation time — it can be added at any point in **Event settings**.

**Event type.** Three options — **In-Person**, **Virtual**, **Hybrid**. The choice determines which attendee app the attendee gets access to:

- **In-Person** — access to the mobile attendee app (iOS, Android) and to the web app in the browser.
- **Virtual** — access to the web attendee app.
- **Hybrid** — access to both.

The microsite is available for all three types. An In-Person event therefore does not need to be switched to Hybrid just because some attendees open the app in a browser or sign up for a workshop there. Session registration works the same way in the mobile app and in the web app.

**Primary language.** The fallback language of the event. If an attendee's device is set to a language you have not explicitly added to the event, the content is shown in the primary language. See *Setting the primary language of an event* for the full picture.

> The primary language is set when the event is created and **cannot be edited** later. It is one of the few truly irreversible decisions in Happenee.

### What happens right after the event is created

The event is added to the workspace list and Happenee switches you to its **Overview** automatically. On the Overview you see:

- Basic information (date, registration status, days until the event).
- **Tools** — quick links to Contacts and groups, Registration, Check-in, Nominations, and — depending on which features are on — either Orders or Attendee approval.
- Links to **Statistics**, **Attendee statistics**, and **Ticket statistics** (the last two for paid events).
- The left menu expands the event structure — Event settings, Statistics and reporting, Content, Engagement, Attendee app, Tickets (if turned on), Registration form, Confirmation e-mail, Microsite, Invitation e-mail, E-mail campaigns, and On-site check-in.
- Do not look for **Registration, Check-in, and Nominations** in that list — they live in the **Tools** dropdown at the bottom of the left menu (and as tiles on the Overview). The same place holds **Orders** if the event has Tickets, or **Attendee approval** if it has Approved registration.

### The language switcher and Preview

In the top-right corner of the event admin you have **two language flags**. They switch the language of the content you are currently editing — content is filled in for each language separately. When you add the agenda, session descriptions, or text in content features, make sure you are in the language you intend to write in.

Next to the flags is the **Preview** button, which shows what the attendee sees:

- The microsite preview.
- The ticket purchase preview (for paid events).
- The attendee app preview (web and mobile).
- The service app preview (for on-site check-in).

### What is not active yet

Right after the event is created, **registration is closed** — an attendee cannot sign up until you finish the registration setup. This is intentional. Before you open registration, walk through **Event settings** (access and registration, visibility, restrictions, and Tickets if you need them) and the **Registration form**. The recommended sequence is in *Recommended order for setting up an event step by step*.

## Common pitfalls

### Picking the primary language without much thought, assuming it can be adjusted later

The primary language is locked after the event is created. If the event will have international guests, set it to English right away. See *Setting the primary language of an event* for the full reasoning.

### Switching the event type after creation (for example from In-Person to Hybrid) when some attendees already have the app installed or registrations in flight

The event type controls which app attendees see. The change is technically possible, but it causes inconsistencies if attendees are already using the app. Decide on the type up front and do not change it. You do not need to switch because of the web app; an In-Person event has it as well.

### Not verifying the time zone — the organizer creates an event from abroad or from a browser set to a different time zone, and the event ends up with the wrong start time

After you fill in the date and time, always check the **Time zone** field. Happenee uses the event time zone for e-mails, the microsite, and the ICS calendar files.

### Trying to fill in every detail at creation — description, icon, graphics, content

At creation you confirm the parameters that frame the event. Content and graphics belong to the next steps (**Content**, **Graphics settings**). Do not delay creation because you do not yet have the final icon.

### Expecting registration to be live as soon as the event is created

Registration is closed after creation. Open it only after you finish the registration setup and check the Registration form. Sharing the microsite link makes sense only after that.

## Related articles

- [What is a workspace and what is an event](https://help.happenee.com/en/articles/1-what-is-a-workspace-and-what-is-an-event)
- [Setting the primary language of an event](https://help.happenee.com/en/articles/10-setting-the-primary-language-of-an-event)
- [What to set up first after creating an event](https://help.happenee.com/en/articles/3-what-to-set-up-first-after-creating-an-event)
- [Navigating the Happenee admin](https://help.happenee.com/en/articles/2-navigating-the-happenee-admin)
- [Managing contacts and groups in your workspace](https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace)
- [Recommended order for setting up an event step by step](https://help.happenee.com/en/articles/8-recommended-order-for-setting-up-an-event-step-by-step)
- [Using the Online module](https://help.happenee.com/en/articles/38-using-the-online-module)
- [Copying the event](https://help.happenee.com/en/articles/70-copying-the-event)

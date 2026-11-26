# How Networking works

> An engagement feature that lets attendees connect, chat, and book meetings.

- Article in the Help Center: https://help.happenee.com/en/articles/36-how-networking-works
- Česká verze: https://help.happenee.com/cs/articles/36-jak-funguje-networking
- Collection: Content and attendee experience
- Updated: 2026-09-02

---

> [!info] Overview
> Networking (in the product also labeled **Attendees**) is an **engagement feature** that gives attendees the list of other registered people and lets them **connect, chat, and book meetings**. Each attendee sets up their own profile — what they want to share (job title, e-mail, social networks), or they can hide the entire profile. The key interactions are: view profiles, save a contact with a click, scan the QR code from a badge, send messages, and book one-to-one meetings.

## Getting started

- Decide whether Networking makes sense for the event. **It fits** conferences, client events, networking evenings, and expos or trade shows. **It does not fit** internal corporate trainings or simple lecture-style events.
- Tell attendees **how to fill in the profile** — the button in the attendee app is visible enough, but a supporting line in the invitation e-mail helps.
- Decide on **the target audience for networking** — does everyone see everyone, or does it make sense to limit it?
- If you want attendees to scan the QR codes from badges, **prepare the badge print** with QR codes (a check-in feature).

## Details

### What Networking includes

**Attendee list.** Every registered person shows up in the list. Each one has a profile card: name, position, company, and optionally a photo. Clicking a card opens the detailed profile.

**Attendee profile.** The attendee fills in:

- First name and last name.
- Job title.
- Company.
- E-mail (optional sharing).
- Phone (optional sharing).
- Social networks: LinkedIn, Twitter (X), Instagram, Facebook, YouTube.
- Photo (optional).
- The whole profile can be **hidden** — the attendee then does not appear in the list.

**Saving a contact.** An attendee adds a contact to their own list in two ways: by clicking **Save contact** in the profile or the list (a one-sided addition), or by **scanning the QR code** from another attendee's badge or ticket (a conscious contact exchange). Both end up among the saved contacts that the attendee downloads after the event — see *Downloading collected contacts (business cards)* below.

**QR from the badge.** Each attendee has a **unique QR code** that is printed on the badge at check-in. Scanning the QR from the badge automatically saves the contact. The scan is a conscious contact exchange, the equivalent of handing over a business card, which is why a contact collected this way has its **e-mail** in the downloaded CSV even when the attendee has not made it public — unlike a contact saved with the button. See *Downloading collected contacts (business cards)* and *Privacy and GDPR*.

**Messages (chat).** One-to-one chat between attendees inside the app. You turn it on in the Networking settings.

**Meeting bookings.** An attendee can offer another person a meeting at a specific time and a specific place. The other person confirms or declines. The place is not free-form — it is picked from a list. There are two variants:

- **Predefined meeting locations** (typically named *Meeting table #1*, *Meeting table #2*, and so on) — generic spots where any attendee can arrange a meeting with anyone else. **Setting up the names and the number of these locations is handled by Happenee customer support** — the organizer does not create them in the admin interface. When you turn the meeting booking system on, let support know how many locations you want and how they should be named.
- **An exhibitor booth** — if the event has the Exhibitors content feature, the booths become available as meeting locations. A meeting at a booth, however, cannot be arranged with just anyone — **only with a representative of that exhibitor**.

### Where to find Networking

In the event admin, go to **Engagement** → **Attendees** (that is the name of the feature in the menu). If you do not have it yet, click **+ Add** → *Attendees*.

### Networking settings

**State** — published or hidden.

**Visibility** — all attendees, or selected groups only.

**Turn on private messages** — allow chat.

**Turn on the meeting booking system** — allow one-to-one meetings. Attendees set up their own available time slots. If you do not have predefined meeting locations and no Exhibitors are configured, there is nowhere for a meeting to take place — contact customer support to set up the locations.

### The attendee profile — who sees and controls it

- **The attendee** fills in and edits their profile inside the app.
- **The organizer** cannot edit the profile on the attendee's behalf (only delete the attendee from the event).
- **Other attendees** see the profile only if it is not hidden.

On first registration the attendee has an **empty profile**. It is a good idea to nudge them in the invitation e-mail or in a notification to fill it in.

### Exhibitors and their representatives

Exhibitor representatives (assigned in the Exhibitors feature) are tagged in Networking as **Exhibitor**. Other attendees recognize them more easily and can connect with them. A meeting **at the booth** is bound **to the representative** — an attendee can arrange it only with a specific representative, not with the booth as such. The prerequisite is that the exhibitor has representatives assigned in the admin and those representatives have set their available time slots in the app.

### Downloading collected contacts (business cards)

The contacts an attendee (or an exhibitor representative) collected during the event are in one place in the attendee app, both in the mobile and the web version. Attendees download them themselves; the organizer does not send the file to them. The path in the app: the **Past** tab → the event → the **Attendees** section → **Saved** (contacts you saved) or **Saved me** (who saved you) → **Download contacts (CSV)**.

The downloaded CSV contains the basic details plus **a column that says whether you added the contact by scanning a QR code or with the button**. Contacts added by a **QR scan** also carry the **e-mail**, even when the attendee has not made it public on the profile (the business-card principle, see *Privacy and GDPR*); the phone number is never passed on. For contacts added only with the **Save contact** button, the e-mail follows the attendee's own setting — you see it only if they made it public. Inside the app itself (outside the CSV), saved contacts show only what each attendee has made public; the difference between a scan and the button shows up only in the downloaded file.

**Contact downloading is turned on by Happenee customer support** — it is not self-service by default. If you want attendees or exhibitors to download the contacts they collected, ask support to enable it (the same as for staff accounts or predefined meeting locations). Until it is enabled, the app shows an inactive text instead of the button, saying that contacts cannot be downloaded for this event.

### Exports (from the admin)

Alongside the in-app download above, the **organizer** can export data from the admin:

- **Attendee list** with the saved contacts marked.
- **Meetings** (who booked with whom and when).

The exports come out as Excel files and give the organizer an overview after the event. Downloading the individual "business cards" (the CSV with e-mails for scanned contacts) is something each attendee does for themselves in the app — see *Downloading collected contacts (business cards)*.

### Privacy and GDPR

Profile sharing is **opt-in** — the attendee decides what to publish. Consent for sharing is part of the standard **GDPR template** in registration. If the event has special privacy requirements (for example, a closed client event), the organizer can:

- Turn Networking off entirely (hide the Attendees content feature).
- Restrict visibility to selected groups only.

### Combining with groups

Groups do not work as a direct filter inside Networking, but they **affect the visibility** of the Networking feature as a whole (for example, Networking only for the *VIP* group). Each group then mingles among themselves.

## Common pitfalls

### Networking is on, but attendees have empty profiles, and the list feels lifeless

In the invitation e-mail and in notifications, ask attendees to fill in their profile. The photo and the job title are the key fields — without them the card looks blank.

### A message is sent to an attendee who downloaded the app but did not log in, and they never receive it

Chat works only for logged-in attendees. During the first setup, ask attendees in the invitation e-mail to log into the app — without a login, neither chat nor meeting bookings work.

### The meeting booking system is on, but no one has set up available slots, and a meeting cannot be booked

Available slots are set by each attendee inside the app. Communicate in a notification how the system works and when to set up the slots.

### The meeting booking system is on but there is no place where the meeting can take place

Predefined meeting locations (such as *Meeting table #1*, *#2*, and so on) are set up by Happenee customer support, not by the organizer in the admin interface. If you have no locations and no Exhibitors with representatives, attendees have nowhere to book a meeting. Before turning bookings on, ask support to set up the number of locations you need.

### An attendee forgot the badge and wants to scan a QR code, and the system cannot do it

The QR from the badge is on the printed paper badge (printed at check-in). The alternative: every attendee can see their **own QR** in the ticket section of the app — others can scan it directly from the phone screen.

### An exhibitor wants to download the contacts they collected but does not see the option — or the CSV has no e-mails

Contact downloading is turned on by **Happenee customer support** and is not self-service by default. Until it is enabled, the app shows only an inactive text saying that contacts cannot be downloaded for this event, so arrange it in advance. Even once it is on, one rule stays: **the extra e-mail (for an attendee who has not made it public) is in the CSV only for contacts added by a QR scan** (the business-card principle). For contacts added only with the **Save contact** button, the e-mail follows the attendee's own setting, and the phone number is never passed on. The CSV also has a separate column telling you whether you added each contact by a scan or with the button. Explain this to exhibitors collecting leads up front, so that they actually scan the QR codes instead of only saving people from the list.

### An exclusive client event with networking turned on for everyone, and VIPs end up in the list with regular attendees

For client events, consider restricting Networking visibility to the **VIP** group. Or turn it off entirely and replace it with offline introductions.

### An attendee forwards the invitation to a colleague who did not register but hopes to find networking through the app

Access to Networking requires a registration and a login. Without registration, the colleague is neither visible nor able to see others.

## Related articles

- [How the attendee app and its home screen work](https://help.happenee.com/en/articles/34-how-the-attendee-app-and-its-home-screen-work)
- [Managing Exhibitors](https://help.happenee.com/en/articles/33-managing-exhibitors)
- [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility)
- [Managing contacts and groups in your workspace](https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace)
- [How check-in and QR-code scanning work](https://help.happenee.com/en/articles/47-how-check-in-and-qr-code-scanning-work)
- [Printing badges](https://help.happenee.com/en/articles/48-printing-badges)
- [How Leaderboard works](https://help.happenee.com/en/articles/37-how-leaderboard-works)
- [Using the Online module](https://help.happenee.com/en/articles/38-using-the-online-module)
- [Recommended setup for an external client event](https://help.happenee.com/en/articles/54-recommended-setup-for-an-external-client-event)
- [Recommended setup for a conference](https://help.happenee.com/en/articles/55-recommended-setup-for-a-conference)
- [Recommended setup for an expo or trade show](https://help.happenee.com/en/articles/56-recommended-setup-for-an-expo-or-trade-show)
- [Setting up engagement features](https://help.happenee.com/en/articles/97-setting-up-engagement-features)

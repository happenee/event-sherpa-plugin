<!-- event-story story extension -->

This is the extension for the turn that writes the story: the full text of the always-loaded articles of collections 01 and 02, a short list of the on-demand articles and the render specification. It holds together with the system prompt and revokes nothing in it.

This edition does not carry the output schema in the extension. The Markdown story does not need it: the render specification below and the labels in `schema/labels.en.json` say what is printed and how. The JSON object goes only to a person who asks for it („pošli Story JSON“ or "send the Story JSON"). Before that reply, read `schema/event_story.wire.json` in the skill package, next to `SKILL.md`, once: the field names are the ones it declares, and they hold for an `INSUFFICIENT` object too. `brief_confirmation.summary_digest` is `null`. Where the core says the schema arrives with this extension, this paragraph applies.

<!-- source: kb.en.01.05 -->

---
title: "Microsite vs attendee app: how to think about the attendee flow"
description: "The microsite is the public page, the attendee app is the environment for registered attendees, and how the two fit together in Happenee."
collection: "Getting started with Happenee"
subcollection: "priprava-setupu"
modules: ["microsite", "ucastnicka_aplikace"]
slug: "microsite-vs-attendee-app-how-to-think-about-the-attendee-flow"
lang: "en"
status: "published"
docId: 5
last_updated: "2026-04-27"
version: 1
tags: [microsite, attendee-app, attendee-flow, basics, communication]
source_images_consulted: true
related:
  - "What is a workspace and what is an event"
  - "What to set up first after creating an event"
  - "How the Event microsite works"
  - "How the attendee app and its home screen work"
  - "How the Invitation e-mail works"
  - "The attendee's journey from the microsite to the attendee app"
  - "Must-have, optional, and advanced features and modules by event type"
  - "Minimum recommended setup for small, medium, and larger events"
  - "Recommended order for setting up an event step by step"
  - "Recommended setup for an incentive trip or itinerary"
  - "Recommended setup for a webinar or online event"
---

> [!info] Overview
> The microsite and the attendee app are the two main channels through which an attendee interacts with your event. The microsite is a public web page with information about the event — accessible to anyone who has the link. The attendee app is the environment for registered attendees, available as a web version and a mobile app. Happenee is designed so that an attendee moves naturally from the microsite through registration into the app — and each channel plays its own role. Understanding this flow helps you set up communication that guides the attendee instead of pushing them.

## Getting started

- Decide whether the event will use the microsite alone or the microsite together with the attendee app. The choice depends more on the event's size and complexity than on its type.
- Understand the underlying logic: the microsite is for informing and registering, the attendee app is for living through the event itself.
- You set content up once in Happenee — whether each content feature appears on the microsite, in the attendee app, or in both is controlled separately for each feature.

## Details

### What the microsite is

The microsite is the public web page for your event. It has its own URL and is accessible to anyone who reaches it through a link in the Invitation e-mail, a campaign, or social media. The microsite plays two main roles:

- **Information showcase** — it presents the event, the agenda, the speakers, the venue, sponsors, FAQ, and anything else an attendee needs to know before deciding whether to attend.
- **Entry point into registration** — from here the attendee continues into the Registration form or to ticket purchase.

### What the attendee app is

The attendee app exists in two forms:

- **Web app** — runs in the browser, nothing to install.
- **Mobile app** — a native app for iOS and Android. For most enterprise customers — typically banks, insurance companies, IT firms, and healthcare organizations — the app is branded (white label), so attendees download the organization's own app under its name and icon.

The attendee app is the environment for registered attendees. They find the detailed Agenda, My Agenda with their registered sessions, Networking, Notifications, Polls, Questions from the audience, the QR ticket for entry, and other engagement features that are not available on the microsite or appear there in a simplified form.

### The ideal attendee flow

In Happenee the channels are designed to chain into a single flow:

1. The attendee receives a **short Invitation e-mail** with a call to action.
2. The e-mail leads them to the **microsite**, where they find the basic information and either register or buy a ticket.
3. After registering, they receive a **Confirmation e-mail** with a QR ticket and links to download the mobile app or open the web app.
4. Further communication — updates, agenda details, networking, the day of the event itself — then runs primarily **inside the attendee app**.

A well-built Invitation e-mail is short and to the point. Its only job is to get the attendee onto the microsite — not to deliver every detail at once.

### When the microsite alone is enough

For smaller or one-off events, where the attendee just downloads a ticket and shows up, the microsite alone can be sufficient. Typical examples are gala evenings, single-occasion company events, and small gatherings of a few dozen people. The attendee app does not add enough value in those cases to outweigh the friction of installing it.

<!-- SUPERSEDED: SUP-01b -->
### When to turn on the attendee app

As soon as an event has an agenda, workshops, networking, polls, or a need to push announcements during the day, the attendee app starts to make sense. A useful rule of thumb: **the bigger and longer the event, the bigger the payoff from the attendee app**. Conferences, expos, multi-day gatherings, events with workshops — all of these are cases where the attendee app leads to real time savings and a better experience.

The attendee app is not mandatory for attendees. Some prefer the web version, others install the mobile one. As the organizer, you simply offer it in the Confirmation e-mail.

### Alternative use case: the microsite as a registration form only

For some external client events, the organizer has their own marketing website and the Happenee microsite serves only as a registration layer — the attendee arrives from the company website, fills in their e-mail, registers, and goes back. In this mode, the microsite shows minimal content (often just the Registration form) and the event information lives on the main company website.

This approach has a downside: **you lose the ability to show speakers, the agenda, and other information directly inside Happenee**. The content has to be maintained twice — once on the company website and once in Happenee for the attendee app — or kept in sync through an API. The ideal state is to use the microsite as the full home for the event. The alternative mode is still valid if the organization's brand requires that all content sit on the company website.

## Common pitfalls

### Trying to cram every piece of information into the microsite and skipping the attendee app entirely, even when the event needs it

The microsite is meant to inform and bring the attendee into registration. The attendee app is meant to guide the attendee through the event itself. When both roles are pushed onto the microsite, you lose engagement and overload the page.

### Presenting the attendee app as mandatory, which creates needless friction

Offer the attendee app as a service — both the web version and the mobile one. Let the attendee pick whichever works for them.

### Unclear transitions between channels, so the attendee does not know when to use the microsite and when to use the attendee app

Stick to the logic: **the microsite before registration, the attendee app after registration**. The Confirmation e-mail clearly leads into the attendee app, and further communication then runs mainly through the app (Notifications, push notifications).

### Assuming that the event type alone decides the choice — "conference equals app, company evening equals no app"

Decide by size and complexity, not by type. A large company conference needs the attendee app; a small client workshop may not.
<!-- /SUPERSEDED -->

## Related articles

- [What is a workspace and what is an event](01_what-is-a-workspace-and-what-is-an-event.md)
- [What to set up first after creating an event](03_what-to-set-up-first-after-creating-an-event.md)
- [How the Event microsite works](../03_content-and-attendee-experience/01_how-the-event-microsite-works.md)
- [How the attendee app and its home screen work](../03_content-and-attendee-experience/14_how-the-attendee-app-and-its-home-screen-work.md)
- [How the Invitation e-mail works](../04_communication-and-invitations/01_how-the-invitation-e-mail-works.md)
- [The attendee's journey from the microsite to the attendee app](../04_communication-and-invitations/07_the-attendees-journey-from-the-microsite-to-the-attendee-app.md)
- [Must-have, optional, and advanced features and modules by event type](06_must-have-optional-and-advanced-features-and-modules-by-event-type.md)
- [Minimum recommended setup for small, medium, and larger events](07_minimum-recommended-setup-for-small-medium-and-larger-events.md)
- [Recommended order for setting up an event step by step](08_recommended-order-for-setting-up-an-event-step-by-step.md)
- [Recommended setup for an incentive trip or itinerary](../07_event-sherpa/05_recommended-setup-for-an-incentive-trip-or-itinerary.md)
- [Recommended setup for a webinar or online event](../07_event-sherpa/07_recommended-setup-for-a-webinar-or-online-event.md)

<!-- source: kb.en.01.06 -->

---
title: "Must-have, optional, and advanced features and modules by event type"
description: "A map of Happenee features and modules by event type: what is essential to your outcome, optional, or specialized."
collection: "Getting started with Happenee"
subcollection: "priprava-setupu"
modules: ["leaderboard"]
slug: "must-have-optional-and-advanced-features-and-modules-by-event-type"
lang: "en"
status: "published"
docId: 6
last_updated: "2026-09-21"
version: 3
tags: [features, modules, decisions, event-types, setup, event-sherpa]
source_images_consulted: true
related:
  - "Microsite vs attendee app: how to think about the attendee flow"
  - "Minimum recommended setup for small, medium, and larger events"
  - "Recommended order for setting up an event step by step"
  - "What to set up first after creating an event"
  - "Recommended setup for an internal corporate event"
  - "Recommended setup for an external client event"
  - "Recommended setup for a conference"
  - "Recommended setup for an expo or trade show"
  - "How Leaderboard works"
  - "Using the Online module"
  - "Recommended setup for an incentive trip or itinerary"
  - "Recommended setup for a hybrid event"
  - "Planning an event and where Happenee helps"
---

> [!info] Overview
> We recommend the complete ecosystem, including the attendee app, for every event regardless of audience size. Match the content and features to the organizer’s goal and the attendees’ tasks. Attendees can choose e-mail, web, or mobile access; app installation and use are not compulsory.

## Getting started

1. Name the outcome for each side: what you as the organizer need, what the attendee should take away, and at an external event what a partner or sponsor should get. Add how you will recognize success: confirmed attendance, smooth check-in, a workshop booking, relevant contacts, or feedback after the event.
2. Describe the attendee’s journey from invitation to outcome. Include buyers, assistants, or partners when they have a different role.
3. Identify what already works in another system and what Happenee should provide.
4. Choose the required features, check availability in your offer, and test one complete journey as an attendee.

## Details

### Must-have means essential to your outcome

There is no set of modules that every event must enable. You always need:

- A clear next step and access for the intended audience.
- Correct information: what, when, where or how to join, and whom to contact.
- A verified confirmation or instruction handover when the journey requires it.
- Someone responsible for content and changes.

If you use Happenee registration, prepare the form and related communication. For paid attendance, also verify the order, payment, and attendee’s entitlement. If registration already runs elsewhere, do not create a second flow just for the app; first agree how attendees and changes will be transferred. The customer’s existing website can remain the public presentation instead of a new Event microsite.

**Optional** means a useful addition for a specific outcome. **Advanced** means specialized options whose scope, availability, support needs, and preparation time should be confirmed in advance; it does not imply another mandatory package.

### Content and orientation

**Agenda** helps when attendees choose between sessions, move between locations, or need to follow a schedule. **Speakers, Sponsors, and Exhibitors** are useful when relevant to the attendee’s decisions and experience. **Venue, Contact, and Custom content** can bring travel details, maps, FAQs, and instructions together.

Do not display an empty feature simply because it exists. Equally, do not dismiss a useful option just because the customer did not know about it. Start with a specific purpose and prepare the content needed for first use.

### The app and attendee connections

We recommend the attendee app as part of the complete event ecosystem for every event, including a meeting of thirty people. Match the content to the goal: a ticket, venue, contact, and materials may be enough, while other events benefit from an agenda, bookings, and networking. Attendees can choose e-mail/PDF/QR, the web app, or the mobile app. Do not make installation or use compulsory. Its web version does not require a mobile app download. An in-person event can use the web app and workshop registration without changing its format to hybrid.

Consider the goal, repeat use, and attendee behavior. At a recurring meeting of around fifty members, **Networking** and chat may be the main benefit. Even at a simple event, explain the app’s value as another way to access information. If the organizer then chooses a narrower scope, respect that decision and preserve a working alternative; do not exclude the app in advance.

The app can remain useful after check-in. Depending on content availability, access, and licensing, attendees can return to materials and contacts after the event and continue with later meetings in a series. This does not imply automatic access to every future event or unlimited data retention.

For networking, define who should meet whom, when there is time, and what attendees should do. A QR code on a badge is not a universal requirement for chat or every contact-saving flow. Verify the specific meeting, visibility, and export options before promising them to a partner.

### Engagement and feedback

**Polls** ask the audience a question; **Questions** let attendees raise questions; **Survey** collects feedback or other responses. Select them for the intended outcome, not as a mandatory package.

For each interaction, define the content, timing, and operator. The moderator must know what to say on stage and what happens to responses. Test the specific mode, attendee access, and display beforehand; do not assume anonymous, moderated, or login-free responses.

### Reservations, logistics, and specialized options

Workshops and time slots require appropriate capacity, registration windows, and change rules. For a vehicle, expert, or station, include preparation and handover time. A waiting list is not available.

Accommodation, transport, and an itinerary involve different units and recipients. A form response alone does not confirm a hotel room; supplier handover must be checked separately.

Discuss seating, a dedicated mobile app, SSO, integrations, and other specialized solutions with Happenee around scope, price, availability, and preparation time. Standard visual branding is not the same as a separate app in the app stores.

### Choosing by event type

- **Internal meeting:** orientation, communication, and purposeful engagement. Networking can connect colleagues across teams; it is not limited to external audiences.
- **Client event:** a clear invitation, confirmed attendance, and a useful follow-up connection. Check VIP, assistant, and partner roles.
- **Conference:** connected agenda, entitlements, workshops, and communication. Consider networking and partners without enabling everything automatically.
- **Expo:** easy orientation, a reason to visit exhibitors, and a usable follow-up contact. Scan counts alone are not a business outcome.
- **Incentive trip:** the correct itinerary for each person, current instructions, and transport and accommodation handovers.
- **Online or hybrid event:** verified content access, coordination with the production team, and meaningful remote engagement.

See the related guides for detailed recommendations. When adding an option later, allow time for content and testing and check any licensing requirements; availability does not always mean immediate activation.

## Common pitfalls

### Event type or size is not a mandatory package

The same fifty attendees may need only a confirmation, or intensive networking. Their task and context determine the choice.

### An available feature is not yet a used feature

Polls without a question and an operator will not create engagement. Prepare a concrete first use.

### A new system is not always the best change

For working external registration, consider transfer effort and change risk. You can add value without replacing it.

### Test the actual journey first

Check login, destination links, entitlements, bookings, and communication with the correct attendee role. An administrator preview is not enough.

## Related articles

- [Microsite vs attendee app: how to think about the attendee flow](05_microsite-vs-attendee-app-how-to-think-about-the-attendee-flow.md)
- [Minimum recommended setup for small, medium, and larger events](07_minimum-recommended-setup-for-small-medium-and-larger-events.md)
- [Recommended order for setting up an event step by step](08_recommended-order-for-setting-up-an-event-step-by-step.md)
- [What to set up first after creating an event](03_what-to-set-up-first-after-creating-an-event.md)
- [Recommended setup for an internal corporate event](../07_event-sherpa/01_recommended-setup-for-an-internal-corporate-event.md)
- [Recommended setup for an external client event](../07_event-sherpa/02_recommended-setup-for-an-external-client-event.md)
- [Recommended setup for a conference](../07_event-sherpa/03_recommended-setup-for-a-conference.md)
- [Recommended setup for an expo or trade show](../07_event-sherpa/04_recommended-setup-for-an-expo-or-trade-show.md)
- [How Leaderboard works](../03_content-and-attendee-experience/17_how-leaderboard-works.md)
- [Using the Online module](../03_content-and-attendee-experience/18_using-the-online-module.md)
- [Recommended setup for an incentive trip or itinerary](../07_event-sherpa/05_recommended-setup-for-an-incentive-trip-or-itinerary.md)
- [Recommended setup for a hybrid event](../07_event-sherpa/06_recommended-setup-for-a-hybrid-event.md)
- [Planning an event and where Happenee helps](../07_event-sherpa/10_planning-an-event-and-where-happenee-helps.md)

<!-- source: kb.en.01.07 -->

---
title: "Minimum recommended setup for small, medium, and larger events"
description: "The recommended minimum setup for a small, medium, or larger event."
collection: "Getting started with Happenee"
subcollection: "priprava-setupu"
modules: ["prurezovy"]
slug: "minimum-recommended-setup-for-small-medium-and-larger-events"
lang: "en"
status: "published"
docId: 7
last_updated: "2026-09-21"
version: 4
tags: [setup, event-size, modules, basics, recommendations]
source_images_consulted: true
related:
  - "Must-have, optional, and advanced features and modules by event type"
  - "Microsite vs attendee app: how to think about the attendee flow"
  - "Recommended order for setting up an event step by step"
  - "Recommended setup for an internal corporate event"
  - "Recommended setup for an external client event"
  - "Recommended setup for a conference"
  - "Recommended setup for an expo or trade show"
  - "Recommended setup for an incentive trip or itinerary"
  - "Planning an event and where Happenee helps"
---

> [!info] Overview
> We recommend the complete ecosystem, including the attendee app, for both small and large events. Size helps estimate operational needs; choose content and features around the goal and attendee journey. Attendees can keep using e-mail and a PDF ticket or choose the web or mobile app — you offer options rather than require installation.

## Getting started

1. Identify what attendees should accomplish, the outcome you need as the organizer, and at an external event what a partner or sponsor should get. Add how you will recognize success.
2. Consider audience size, simultaneous arrivals, duration, repetition, and agenda complexity.
3. Choose the closest option below and add only features with a specific benefit.
4. Assign a content owner and test the full journey before launch.

## Details

### A small, simple event

For a one-off meeting at a single location with a fixed schedule, an invitation, attendance confirmation, and clear instructions may be enough. You can manage registration in Happenee; if it already works elsewhere, first agree the handover.

The essentials usually include:

- When and where to arrive, a contact, and any instructions.
- A clear way to confirm or change attendance.
- Tested pre-event communication.
- Attendance records or check-in when needed.

Offer the app here too: it can bring the ticket, venue, contact, and materials for a later visit together. It does not need dozens of features. People who prefer e-mail or PDF can use a verified alternative journey. An Event microsite does not have to replace your existing website either.

### A small recurring or interactive event

Around fifty members of a professional club may need to find colleagues, message each other, and maintain contact between meetings. An app can be more valuable here than at a much larger event with a simple journey.

Consider profiles, Networking and chat, an agenda overview, or relevant bookings. Attendees can use the web app without downloading a mobile version. Define a reason to use it and an owner who explains the first step. For a series, reconfirm current attendees, content, and access; an old list is not automatically a new confirmed audience.

After the event, materials, contacts, and later meetings can provide a reason to return. Check content availability and access for the specific event and license; previous attendance does not automatically grant access to every future event.

Example: before a regular breakfast, a member checks profiles and messages someone they want to meet. Assess useful connections, not just app opens.

### A medium-sized event with agenda choices

With workshops, parallel sessions, and changes during the day, orientation and connected steps often matter more than headcount.

Consider:

- An Agenda with times, locations, and relevant speakers.
- Registration or tickets matched to the actual entry flow.
- A web or mobile attendee app for choices and current information.
- Verified workshop capacity and registration windows.
- Change communication and a support contact.

An in-person event can use the web app and workshop registration without becoming a hybrid event. An agenda displayed on an Event microsite does not imply the same booking journey as the attendee app.

Example: an attendee chooses between two parallel workshops. Test their specific entitlement, booking, change, and any overlap. A correct item in administration alone does not prove the full journey works.

### A larger or operationally complex event

A larger audience typically increases the importance of segmentation, check-in, exceptions, and coordination. We recommend the app here as at a small event; richer content is useful for an extensive agenda, networking, multiple locations, or ongoing changes. Still, do not require every attendee to use the same journey.

Prepare:

- Clear entry options and communication for each relevant audience.
- An arrival, check-in, and exception-handling plan.
- An agenda and navigation matched to actual needs.
- A change owner and rehearsal of critical journeys.
- Agreed outcomes and a way to verify them.

If registration and check-in are the goal, offer the app as another way to keep entry details and information together. An organizer can consciously choose a narrower scope after understanding the benefit; it should not be the automatic starting recommendation. If you also want partner value and attendee connections, design the actual journey and allow time in the agenda. Scan or booking counts alone do not demonstrate business value.

### Deciding on an additional option

Ask:

- What exactly will someone accomplish better?
- Do we have content, an owner, and time to test it?
- Is it available in our scope, or does it need agreement with Happenee?
- How will we know it delivered value?

An option can be useful later if there is enough preparation time. There is no fixed number of positive answers that automatically moves an event into a larger category. See the related event-type guides for detailed alternatives.

## Common pitfalls

### The web app does not require a mobile installation

Attendees can use the web journey. Explain its benefit first, then recommend the appropriate access method.

### Do not copy every feature from the previous conference

The new event may have a different goal, audience, and team capacity. Reuse what is relevant and verify data and links.

### Registration and check-in need their own preparation

For paid attendance, test the order, payment, correct ticket holder, and access. Confirm the check-in team and the procedure for a missing entry entitlement.

### Do not add complexity without an outcome

Empty content or interaction without an owner will not help. If the purpose is unclear, choose a simpler option and record what would change the decision.

## Related articles

- [Must-have, optional, and advanced features and modules by event type](06_must-have-optional-and-advanced-features-and-modules-by-event-type.md)
- [Microsite vs attendee app: how to think about the attendee flow](05_microsite-vs-attendee-app-how-to-think-about-the-attendee-flow.md)
- [Recommended order for setting up an event step by step](08_recommended-order-for-setting-up-an-event-step-by-step.md)
- [Recommended setup for an internal corporate event](../07_event-sherpa/01_recommended-setup-for-an-internal-corporate-event.md)
- [Recommended setup for an external client event](../07_event-sherpa/02_recommended-setup-for-an-external-client-event.md)
- [Recommended setup for a conference](../07_event-sherpa/03_recommended-setup-for-a-conference.md)
- [Recommended setup for an expo or trade show](../07_event-sherpa/04_recommended-setup-for-an-expo-or-trade-show.md)
- [Recommended setup for an incentive trip or itinerary](../07_event-sherpa/05_recommended-setup-for-an-incentive-trip-or-itinerary.md)
- [Planning an event and where Happenee helps](../07_event-sherpa/10_planning-an-event-and-where-happenee-helps.md)

<!-- source: kb.en.01.08 -->

---
title: "Recommended order for setting up an event step by step"
description: "The order of setup steps that respects the dependencies between them."
collection: "Getting started with Happenee"
subcollection: "priprava-setupu"
modules: ["nastaveni_udalosti"]
slug: "recommended-order-for-setting-up-an-event-step-by-step"
lang: "en"
status: "published"
docId: 8
last_updated: "2026-09-21"
version: 5
tags: [setup, order, getting-started, workflow, steps]
source_images_consulted: true
related:
  - "What to set up first after creating an event"
  - "Choosing the right registration type"
  - "Microsite vs attendee app: how to think about the attendee flow"
  - "Must-have, optional, and advanced features and modules by event type"
  - "Minimum recommended setup for small, medium, and larger events"
  - "Creating a new event"
  - "Copying the event"
  - "Setting up the Registration form"
  - "Recommended setup for an internal corporate event"
  - "Recommended setup for an external client event"
  - "Recommended setup for a conference"
  - "Recommended setup for an expo or trade show"
  - "Recommended setup for an incentive trip or itinerary"
  - "How to fix things after the fact"
  - "Using the Happenee documentation in your AI assistant"
  - "Planning an event and where Happenee helps"
---

> [!info] Overview
> Setting up an event in Happenee follows a logic that respects the dependencies between steps. Groups have to exist before you can target visibility on them in the Registration form. Contacts have to be in the workspace before you can assign them to an event. The Agenda has to exist before you can assign speakers to sessions. This article gives you the order that has worked in practice — first the launch of registration, then the operational phase, then the event itself, and finally reporting.

## Getting started

- Before you start, make sure you have ready: basic contacts and groups in the workspace, your GDPR settings, and the e-mail footer.
- Work in stages — do not try to have everything done at once. Some things only get configured in the second phase.
- For each stage, finish the "blocking" decisions before you dive into the details.

> **Note:** If you run recurring events, you can save time by **duplicating an existing event** — Happenee copies the setup (graphics, the Registration form, the microsite, e-mails, content and engagement features) into a new event, without attendees or transactional data. For what carries over and what to watch for, see [Duplicating an event](../02_event-setup-and-registration/13_duplicating-an-event.md). **Event templates** as reusable blueprints are still in development. Either way, keep a clear group structure, custom contact fields, and GDPR templates in your workspace settings — those parts do not need to be reconfigured across events.

## Details

### Plan around the next real deadline

Separate the event date from the date when you need to send invitations and open registration. Required materials, any domain setup, training, and testing must be ready first. Confirm the scope and dates for your agreed service; offer validity and the license period are separate.

To open registration, complete the content attendees need to decide and register. You can prepare further Agenda content or the attendee app later if registration does not depend on them. Decide who will supply the remaining content and when attendees will receive it.

### Stage 0 — Before creating the event (workspace)

This stage applies to the whole workspace. For a later event, review changes to the company, sender, access, and input materials. If everything matches the current brief, continue to Stage 1.

1. **Workspace settings** — company information, the default e-mail and microsite footer (typically handled by customer support at your request).
2. **Custom contact fields** — if you know you will want to track specific information on contacts across all your events (company, job title, internal ID), set the fields up now.
3. **Personal data protection (GDPR)** — the processing template, plus consents beyond the baseline (marketing, photos). Without this, you cannot legally launch registration.
4. **Importing the contacts database** — if you already have a database of attendees, import it.
5. **Creating the basic groups** — VIP, speakers, client segments, internal team.

### Stage 1 — Creating the event and the key decisions

1. **Create a new event** — name, date, time, time zone, type (In-Person, Virtual, Hybrid).
2. **Primary language** — decide based on the expected nationalities of your attendees. If international guests are coming, the primary language is English. **Once the event is created, this decision is irreversible.**
3. **Secondary languages** — add the other languages in which you will publish content.
4. **Decide on the registration type** — public, closed, nominated, approved? With additional information or automatic? Paid or free? (See [Choosing the right registration type](04_choosing-the-right-registration-type.md).)

### Stage 2 — Groups, visibility, basic structure

1. **Group structure for this event** — create the groups you will use in the Registration form, in visibility targeting, and in communication.
2. **Assign contacts to the event** — from the workspace, assign who belongs to this event. With closed registration, this is how you decide who gets the personal link.

### Stage 3 — Event content

In this phase, you fill in the informational backbone of the event. Order within the stage is not strict, but a few dependencies still apply:

1. **Venue** — where the event takes place.
2. **Contact** — who the contact person on the organizing side is.
3. **Agenda** — first the session types (when relevant), then the individual sessions.
4. **Speakers** — only after the Agenda is in place, so you can assign them to sessions.
5. **Sponsors, Exhibitors** — if they are part of the event.
6. **Custom content, FAQ, info blocks** — specific information for attendees.

For each content feature, decide:

- Where it shows (microsite, app, both)?
- Who sees it (everyone, or selected groups)?

### Stage 4 — Registration form

1. **Contact details** — decide which fields are required, optional, or hidden.
2. **Additional questions** — add questions specific to this event (meals, parking, workshop, accommodation).
3. **Conditional questions** — if some questions depend on other answers, link them.
4. **Visibility by group** — if a question should only be visible to some attendees, configure that.
5. **Form preview** — walk through the full flow from the attendee's perspective.

### Stage 5 — Communication

1. **Invitation e-mail** — content, design, embedded links. Short and direct; the goal is to get the attendee onto the microsite.
2. **Confirmation e-mail** — contains the QR ticket, links to the app, and other information.
3. **E-mail campaigns** — if you plan further communication before the event (reminders, details, practical info).
4. **Test send** — send the invitation and confirmation e-mails to a test address yourself, and verify the links and rendering.

### Stage 6 — Microsite and app

1. **Microsite** — verify the visual look, the languages, and the content of each feature and module.
2. **Attendee app** — if you use it, walk through how the content shows in the mobile and web versions.
3. **Feature and module visibility** — review once more what is enabled and where.

### Stage 7 — Launching registration

1. **Final check** — previews on the microsite and in the app, every language, a test registration.
2. **Launch** — share the link (public or personal, depending on the registration type), send invitation e-mails.

### Stage 8 — During the registration period

In this phase, the event is public. Watch for:

- Registration statistics
- Error e-mails (invitation did not arrive, link does not work)
- Capacity changes, approval flows (when enabled)
- E-mail campaigns — reminders, agenda details, practical information

### Stage 9 — Preparing for the day

1. **Check on the check-in setup** — who handles arrivals, which zones, which QR scanners.
2. **Accounts for event staff** — if you delegate check-in to a third party.
3. **Badge printing** — if you print badges, review the layout and prepare the export.
4. **Seating** — if you use it, finish assigning seats.
5. **Notifications for day one** — push notifications drafted and ready.

### Stage 10 — Event day

1. Checking attendees in (Check-in).
2. Operational notifications (agenda changes, practical info).
3. Responding to attendee questions through the app.

### Stage 11 — After the event

1. **Statistics** — overall attendance, workshop fill rates, registration trend.
2. **Survey / feedback** — if it is enabled.
3. **Follow-up communication** — thank-you, materials, next steps.
4. **Data export** — if you need data for internal reporting.

## Common pitfalls

### Trying to finish everything at once — content, registration, communication, app. You lose track of what is in progress where

Work in stages. Decide the language, registration type, and groups first. Before launch, complete and test the registration journey and the content attendees need for it. Later content need not block registration if neither the form nor the promise to attendees depends on it.

### Speakers being assigned to sessions that do not exist yet

The order in Stage 3: session types first, then sessions, then speakers. If you keep that order, you will not have to backtrack.

### Groups being created only when a conditional question or a communication target is being set up. The result is chaos and manual reassignment

Plan your groups in Stage 2, **before the Registration form**. For the form to assign them automatically, they have to exist.

### A registration test is run only after invitation e-mails have already gone out. Errors surface when it is too late

Always run a test — go through registration as an attendee, let every e-mail land in your inbox, open the QR ticket, look inside the app. It is better to find a bug an hour before launch than an hour after.

### All content gets filled in only in one language; the second language is forgotten

After every edit, switch the language with the flag and verify. Especially before launch, walk through every language end to end.

### A changed brief does not reach the next person doing the work

When the date, company, links, or agreed scope changes, review what has already been sent and what is still being prepared. Identify the current materials and test the changed journey from the attendee’s perspective. An earlier offer or a copied event does not replace the current brief.

## Related articles

- [What to set up first after creating an event](03_what-to-set-up-first-after-creating-an-event.md)
- [Choosing the right registration type](04_choosing-the-right-registration-type.md)
- [Microsite vs attendee app: how to think about the attendee flow](05_microsite-vs-attendee-app-how-to-think-about-the-attendee-flow.md)
- [Must-have, optional, and advanced features and modules by event type](06_must-have-optional-and-advanced-features-and-modules-by-event-type.md)
- [Minimum recommended setup for small, medium, and larger events](07_minimum-recommended-setup-for-small-medium-and-larger-events.md)
- [Creating a new event](../02_event-setup-and-registration/01_creating-a-new-event.md)
- [Copying the event](../02_event-setup-and-registration/13_duplicating-an-event.md)
- [Setting up the Registration form](../02_event-setup-and-registration/05_setting-up-the-registration-form.md)
- [Recommended setup for an internal corporate event](../07_event-sherpa/01_recommended-setup-for-an-internal-corporate-event.md)
- [Recommended setup for an external client event](../07_event-sherpa/02_recommended-setup-for-an-external-client-event.md)
- [Recommended setup for a conference](../07_event-sherpa/03_recommended-setup-for-a-conference.md)
- [Recommended setup for an expo or trade show](../07_event-sherpa/04_recommended-setup-for-an-expo-or-trade-show.md)
- [Recommended setup for an incentive trip or itinerary](../07_event-sherpa/05_recommended-setup-for-an-incentive-trip-or-itinerary.md)
- [How to fix things after the fact](../08_troubleshooting/13_how-to-fix-things-after-the-fact.md)
- [Using the Happenee documentation in your AI assistant](../07_event-sherpa/08_using-the-happenee-documentation-in-your-ai-assistant.md)
- [Planning an event and where Happenee helps](../07_event-sherpa/10_planning-an-event-and-where-happenee-helps.md)

<!-- source: kb.en.02.01 -->

---
title: "Creating a new event"
description: "What you fill in when creating a new event and which choices are permanent."
collection: "Event setup and registration"
subcollection: "event-a-kontakty"
modules: ["nastaveni_udalosti"]
slug: "creating-a-new-event"
lang: "en"
status: "published"
docId: 9
last_updated: "2026-09-09"
version: 4
tags: [getting-started, setup, create-event, event-type, primary-language]
source_images_consulted: true
related:
  - "What is a workspace and what is an event"
  - "Setting the primary language of an event"
  - "What to set up first after creating an event"
  - "Navigating the Happenee admin"
  - "Managing contacts and groups in your workspace"
  - "Recommended order for setting up an event step by step"
  - "Using the Online module"
  - "Copying the event"
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

- [What is a workspace and what is an event](../01_getting-started/01_what-is-a-workspace-and-what-is-an-event.md)
- [Setting the primary language of an event](02_setting-the-primary-language-of-an-event.md)
- [What to set up first after creating an event](../01_getting-started/03_what-to-set-up-first-after-creating-an-event.md)
- [Navigating the Happenee admin](../01_getting-started/02_navigating-the-happenee-admin.md)
- [Managing contacts and groups in your workspace](03_managing-contacts-and-groups-in-your-workspace.md)
- [Recommended order for setting up an event step by step](../01_getting-started/08_recommended-order-for-setting-up-an-event-step-by-step.md)
- [Using the Online module](../03_content-and-attendee-experience/18_using-the-online-module.md)
- [Copying the event](13_duplicating-an-event.md)

<!-- source: kb.en.02.02 -->

---
title: "Setting the primary language of an event"
description: "The primary language is the fallback for attendees outside the added languages and cannot be changed after the event is created."
collection: "Event setup and registration"
subcollection: "event-a-kontakty"
modules: ["nastaveni_udalosti"]
slug: "setting-the-primary-language-of-an-event"
lang: "en"
status: "published"
docId: 10
last_updated: "2026-04-27"
version: 1
tags: [primary-language, languages, setup, international-events, fallback]
source_images_consulted: false
related:
  - "Creating a new event"
  - "What to set up first after creating an event"
  - "Managing contacts and groups in your workspace"
  - "What to do when a campaign will not send or arrives in the wrong language"
---

> [!info] Overview
> The primary language of an event is the **fallback language** shown to an attendee whose device language is not among the languages you have explicitly added to the event. The choice of primary language is irreversible — once the event is created it cannot be changed without starting a different event. For events with international attendees, the recommended primary language is **English**.

## Getting started

- Before you create the event, decide whether you expect international attendees.
- If yes, set the primary language to **English**, even if the main content language is Czech.
- Add secondary languages (Czech, Slovak, others) according to which languages you want the content in.
- Make this decision when the event is created — you cannot change it later.

## Details

### How the language choice works for the attendee

An attendee opens the microsite or the attendee app with some device language setting. Happenee checks whether the event has content in that language:

- **Yes** — the content is shown in that language.
- **No** — the content is shown in the event's **primary language**.

So the primary language does not decide which language you fill content in — content is filled in for each added language separately. The primary language decides what is shown to attendees whose language you have not added.

### A practical example

You are running a conference in Prague with international guests. You plan to create the content in **Czech** and **English**. You also expect attendees whose phones are set to German, Spanish, or Italian.

- **Primary language = Czech** (wrong): attendees with their phone set to German, Spanish, or Italian see Czech content. Unusable for them.
- **Primary language = English** (correct): the same attendees see the English content, which they can understand.

Rule of thumb: **if the event has international attendees, set the primary language to English**. Add Czech as a secondary language. Czech-speaking attendees see Czech, everyone else sees English.

### Why the decision is irreversible

The primary language is part of the event's underlying data structure. Content features, the Registration form, e-mails, the microsite — every piece is created with a reference to the primary language. Happenee does not allow it to be changed retroactively, because that would break the integrity of the content.

> The primary language is set when the event is created and **cannot be edited** later. If you realize you chose the wrong one, you have to create a new event.

### How the primary language differs from secondary languages

When you edit content in the admin, you switch between languages with the **two flags** in the top-right corner. Secondary languages can be added and removed freely in **Event settings → Language settings**. The primary language appears in this setting marked as **"Primary language — cannot be edited"** and stays there permanently.

If you do not fill in content for a secondary language, the system uses the primary language for that piece of content. That is also why it makes sense to pick the broadest possible primary language (typically English) — it protects you from showing an attendee an empty piece of content.

## Common pitfalls

### Primary language = Czech for an event that international guests will attend — a German guest opens the microsite and sees Czech content even though the event has an English version

For events with international attendees, set the **primary language to English**. Add Czech as a secondary language. The same applies to Slovak events — if guests from other countries might come, the primary language should be English.

### The organizer notices the wrong primary language only after the registration link is already published

The primary language cannot be changed. The only option is to create a new event and move the previously registered attendees over. Make the decision when the event is being created.

### Content filled in only in the primary language, even though attendees with that device language are in the minority

Primary language does not mean "main content language" — it means "fallback for every unknown language". Fill in the content in every language you want to offer. Use the flag in the top-right corner of the event admin to switch the language while editing.

## Related articles

- [Creating a new event](01_creating-a-new-event.md)
- [What to set up first after creating an event](../01_getting-started/03_what-to-set-up-first-after-creating-an-event.md)
- [Managing contacts and groups in your workspace](03_managing-contacts-and-groups-in-your-workspace.md)
- [What to do when a campaign will not send or arrives in the wrong language](../08_troubleshooting/07_what-to-do-when-a-campaign-will-not-send-or-arrives-in-the-wrong-language.md)

<!-- source: derived/digest.tierA.en.md -->

# Short list of the knowledge base articles loaded on demand

- `pack_version`: `0.8.1`
- articles: 62

One line per article: id, title, module tags and one sentence on what the article covers. The full text of every article is in the package as `knowledge/ondemand/<id>.md`; which ones to read is step 7 of `SKILL.md`, from `config/archetype_ondemand.json` and `config/kb_module_map.json`. Do not cite the list itself and do not put its ids in `source_refs[]`: it is a pointer, not a source.

- `kb.en.01.04` Choosing the right registration type (modules: registrace). The registration type you pick shapes how much manual work waits for you and which e-mails attendees receive.
- `kb.en.02.03` Managing contacts and groups in your workspace (modules: ucastnici_skupiny_a_viditelnost). The workspace's central database for contacts and groups, shared across all your events.
- `kb.en.02.04` Setting the registration type and additional questions (modules: registrace). Where and how to set the registration type and additional questions, and how they combine with Tickets.
- `kb.en.02.05` Setting up the Registration form (modules: registrace). How to build the Registration form for contact details and additional questions specific to the event.
- `kb.en.02.06` How conditional questions work in the Registration form (modules: registrace). Conditional questions appear only after a specific answer, keeping the form short.
- `kb.en.02.07` Working with groups and visibility (modules: ucastnici_skupiny_a_viditelnost). How to use groups inside an event to control content visibility, communication targeting, and registration limits.
- `kb.en.02.08` Managing accommodation and roommate selection (modules: registrace). How to let attendees pick a roommate in the Registration form and prepare data for the hotel.
- `kb.en.02.09` How nominations and nominators work (modules: registrace). Setting up nominators, delegation, capacity, contact imports, and the new portal.
- `kb.en.02.10` Setting up Tickets (modules: vstupenky_a_objednavky). How to turn on and configure Tickets, including online payments, invoices, and discount codes.
- `kb.en.02.11` Managing Orders and invoices (modules: vstupenky_a_objednavky). Where to find every order for a paid event and what you can do inside an order — invoices, billing details, refunds, exports.
- `kb.en.02.12` Setting up Seating (modules: registrace). A paid advanced feature for assigning specific seats inside a pre-modeled venue.
- `kb.en.02.13` Copying the event (modules: nastaveni_udalosti, registrace, vstupenky_a_objednavky). Creating a new event from an existing one in the copy wizard: what you can carry over, what is never copied, and what to check after copying.
- `kb.en.02.14` How custom contact fields work (modules: ucastnici_skupiny_a_viditelnost). Workspace-level fields that extend contact details beyond the standard set — where you define them, everywhere they show up, and why to create them before you open registration.
- `kb.en.02.15` Adding an attendee manually (modules: ucastnici_skupiny_a_viditelnost, registrace). Every way to get a person into an event outside the registration form — assigning a contact or a group, importing, walk-ins on site — and what each one does to the attendee status.
- `kb.en.03.01` How the Event microsite works (modules: microsite). The microsite is the public event page every e-mail link points to.
- `kb.en.03.02` Setting up Venue and the event location (modules: microsite, lokalita, ucastnicka_aplikace). A content feature that shows attendees where the event takes place, with a map and navigation.
- `kb.en.03.03` Managing Speakers (modules: recnici). A content feature for profiles of people in your agenda, their assignment to sessions, and their display to attendees.
- `kb.en.03.04` Adding an organizer contact (modules: microsite). A content feature that gives attendees a way to reach a specific person on the organizing team.
- `kb.en.03.05` Using Custom content (FAQ, map, info blocks) (modules: vlastni_obsah). A general-purpose content feature for anything that does not fit elsewhere (FAQ, a map, an info block).
- `kb.en.03.06` Building the event Agenda — architecture (modules: program_a_sessions). The layers of the Agenda (sessions, types, registration blocks, stages, tags) and how they fit together.
- `kb.en.03.07` How session types work (modules: program_a_sessions). A template of default behavior for sessions: registration, visibility, and engagement features.
- `kb.en.03.08` Setting up workshops and session registration (modules: program_a_sessions). A Workshop is a session that requires registration and has a capacity, an optional registration window, and an optional cancellation deadline, with sign-up done in the attendee app.
- `kb.en.03.09` How time slots work (modules: program_a_sessions). A session where the attendee reserves a specific time from a list (test drives, consultations, meetings).
- `kb.en.03.10` Setting up reservations in the Agenda — buses, workshops, social program (modules: program_a_sessions). How to use time slots and workshops to run reservation scenarios such as test drives or the social program.
- `kb.en.03.11` How registration blocks, stages, and tags work (modules: program_a_sessions, ucastnici_skupiny_a_viditelnost). Three mechanisms for organizing a larger agenda: registration blocks, stages, and tags.
- `kb.en.03.12` Managing Sponsors (modules: sponzori_a_vystavovatele). A content feature for displaying event partners with their logos in categories by prominence.
- `kb.en.03.13` Managing Exhibitors (modules: networking, sponzori_a_vystavovatele). A content feature for exhibitor profiles with locations, tags, representatives, and assigned sessions.
- `kb.en.03.14` How the attendee app and its home screen work (modules: ucastnicka_aplikace). The environment where the attendee lives during the event, and how its home screen is organized.
- `kb.en.03.15` How My Agenda works (modules: moje_agenda). The attendee's personal schedule of saved and registered sessions, and the settings for the My Agenda block on the Agenda tab.
- `kb.en.03.16` How Networking works (modules: networking). An engagement feature that lets attendees connect, chat, and book meetings.
- `kb.en.03.17` How Leaderboard works (modules: leaderboard). An engagement feature for gamification, with points for attendee activities and a ranking of the most active.
- `kb.en.03.18` Using the Online module (modules: online_modul). An engagement feature for virtual and hybrid events with a livestream, a Social Wall, and interactive tabs.
- `kb.en.03.19` Bulk import of speakers (modules: recnici). Two ways to bulk-import speakers — upload an XLS/XLSX/CSV file with column mapping, or pick specific speakers from another event, photos and translations included.
- `kb.en.03.20` Bulk import of sessions (modules: program_a_sessions). Upload sessions into the Agenda from Excel through a 5-step wizard — template or your own file, column mapping, validation, and a preview before anything is written.
- `kb.en.03.21` Managing sessions (modules: program_a_sessions). Creating, editing, and bulk-managing sessions on the Sessions tab: the edit panel, inheritance from the type, status, filtering, and bulk actions.
- `kb.en.03.22` Bulk import of sponsors (modules: sponzori_a_vystavovatele). Import sponsors from Excel — map columns, assign categories in Relations, preview, and download a CSV report.
- `kb.en.03.23` Bulk import of exhibitors (modules: sponzori_a_vystavovatele). Upload exhibitors from Excel through a 5-step wizard — template, column mapping, assigning categories and locations, validation, and a CSV report.
- `kb.en.03.24` Setting up engagement features (modules: ucastnicka_aplikace). Polls, Questions, Survey, and Registration information in the event administration — where you turn them on, when each one fits, and how to read the results.
- `kb.en.04.01` How the Invitation e-mail works (modules: komunikace_a_pozvanky). The Invitation e-mail is the first wave of invitations to assigned contacts.
- `kb.en.04.02` How the Confirmation e-mail works (modules: komunikace_a_pozvanky). A system e-mail sent to the attendee automatically after registration, with the PDF ticket and the link into the app.
- `kb.en.04.03` Creating and sending an E-mail campaign (modules: komunikace_a_pozvanky). The module for bulk e-mailing with group and status targeting, scheduled sending, and delivery tracking.
- `kb.en.04.04` When to use the Invitation e-mail vs. an E-mail campaign (modules: komunikace_a_pozvanky). The Invitation e-mail for the first wave after importing contacts, a campaign for everything else.
- `kb.en.04.05` Targeting communication by groups and statuses (modules: komunikace_a_pozvanky). The two axes of targeting in Happenee: attendee statuses and the groups they belong to.
- `kb.en.04.06` Personal link vs. public link: what is the difference (modules: komunikace_a_pozvanky). Where the registration button in an e-mail should lead: a personal recipient link, a public link, or individual free admission at a paid event.
- `kb.en.04.07` The attendee's journey from the microsite to the attendee app (modules: komunikace_a_pozvanky, ucastnicka_aplikace). How to lead the attendee from the e-mail to the microsite, into registration, and into the attendee app.
- `kb.en.04.08` Using Notifications in the attendee app (modules: notifikace). An engagement feature for scheduled messages in the attendee app, the main channel for communication during the event.
- `kb.en.04.09` Using the Invitation e-mail as a save-the-date (modules: komunikace_a_pozvanky). An advance event announcement: the Invitation e-mail with the registration button hidden, only a calendar entry attached. Used before opening registration.
- `kb.en.04.10` Communication flow on the event day (modules: notifikace, komunikace_a_pozvanky). The day-of communication sequence: a morning e-mail with the QR ticket, push notifications in the app, and campaigns for the unregistered.
- `kb.en.04.11` Planning follow-up communication after the event (modules: komunikace_a_pozvanky). What to send attendees after the event: a thank-you e-mail, a feedback survey, materials, a follow-up invitation. How to segment by attendance.
- `kb.en.04.12` How placeholder variables work (modules: komunikace_a_pozvanky). Placeholder variables fill individual attendee data into an e-mail, a campaign, or the microsite — the full list of universal variables, the ones tied to custom contact fields, and how to test them.
- `kb.en.04.13` Communication flow before the event (modules: komunikace_a_pozvanky). The sequence from the save the date to the day before — when the full invitation goes out, when to remind people who have not responded, and when to send the logistics e-mail.
- `kb.en.04.14` Tracking e-mail and campaign deliverability (modules: komunikace_a_pozvanky). How to read the Mailing status chart, what Not delivered means and how it differs from unread, and where to find delivery and opens for an individual recipient.
- `kb.en.05.01` How check-in and QR-code scanning work (modules: checkin_a_tisk_jmenovek). Checking attendees in with the Service app (QR scanning, the Attendees list, and Kiosk mode) and with the web Check-in tool.
- `kb.en.05.02` Printing badges (modules: checkin_a_tisk_jmenovek). Print badges from the Service app over Bluetooth on a Brother QL-820NWB. Set the badge size, content, and larger font for large badges without a QR code.
- `kb.en.05.03` Preparing data for accommodation providers (modules: checkin_a_tisk_jmenovek). How to stitch data for the hotel by hand from several exports, since Happenee does not yet offer a single merged export.
- `kb.en.05.04` Preparing the service app before the event (modules: checkin_a_tisk_jmenovek). What to arrange before your event staff scan their first QR code — staff accounts, installing the app, check-in places, pairing the printer, and a test scan.
- `kb.en.06.01` Interpreting event statistics (modules: reporting_a_statistiky). Where to find event statistics (invitations, registrations, attendance) and how to read them.
- `kb.en.06.02` Interpreting attendee statistics (modules: reporting_a_statistiky). Attendee statuses from the invitation to actual attendance, and how to read them for reporting and communication targeting.
- `kb.en.06.03` Working with Orders and exports (modules: reporting_a_statistiky). A switchboard of the eleven event exports and when to download which one (accounting, GDPR, catering, CRM).
- `kb.en.06.04` Interpreting ticket statistics (modules: vstupenky_a_objednavky, reporting_a_statistiky). How to read Ticket statistics — sold, paid, unpaid, free, and canceled tickets, the monthly overview, how they relate to registrations, and what the export gives you.
- `kb.en.06.05` Reporting and content management in the Online module (modules: online_modul, reporting_a_statistiky). What the Online module tells you after the event — the viewership chart, visitor lists across modules, Excel exports, and managing the chat, questions, and poll content.
- `kb.en.07.10` Planning an event and where Happenee helps (modules: prurezovy). A map of event planning from the first intent to the next edition, and the points where it turns into setup and evaluation in Happenee.


# Describe: story render

How an Event Story object becomes Markdown. Written as a specification so that
`render_story.py` and the model produce the same document from the same JSON.
Under `artifact: json` the model writes none and the renderer alone follows this
file; under `artifact: markdown` the model writes it without section 9 and
delivers that section only to a person who asks for it.

## Rules the renderer follows

1. The output language is `story.language`. Every fixed string below exists in
   both `cs` and `en`; pick the column, never mix.
2. Seven vocabularies are printed through `schema/labels.<language>.json`:
   `truth_status`, `commercial_state`, `certainty`, `phase_key`, `kind`,
   `selection`, `answer_status`. Look the value up and print what is there; do not
   retype it, and treat a value with no entry as a defect rather than a fallback.
   `kind` is the fallback only: a next step is printed with the label its target
   row carries, and the labels-file entry is used when a row carries none. The
   other six are always read from the labels file. Everything else this file names,
   written as `{label:...}` or `{render_string:...}`, is a fixed string defined in
   this file, because the labels file carries no entry for it.
3. The renderer decides nothing. It does not pick modules, reorder phases, hide a
   branch or add a sentence that is not in the JSON. Any reasoning belongs to the
   model.
4. Section order is fixed and does not depend on content.
5. A section whose source array is empty is skipped entirely, heading included,
   except the journey map, which always prints all eight phases.
6. No price, currency symbol or amount is ever printed. A currency in the JSON is a
   defect: the renderer stops and reports it rather than rendering it.
7. No en dash and no em dash in generated text. Separate items with a middle dot
   (`·`), a comma or a new sentence.

## Section order

| # | Section | Source |
|---|---|---|
| 1 | Hero | `presentation.hero` |
| 1b | Outcomes | `outcomes` |
| 2 | What we understood | `presentation.understood_cards[]` |
| 3 | Journey map | `presentation.journey_map.phases[]` |
| 3b | Where Happenee comes into your plan | `presentation.journey_map.phases[]`, `presentation.branch_details[].data_needed[]`, `presentation.organizer_scope` |
| 4 | Branch details | `presentation.branch_details[]`, joined to `capabilities[]` |
| 5 | Capability overview | `capabilities[]` |
| 6 | What you do not need and why | `do_not_use[]` |
| 7 | Open questions and what a human verifies | `unknowns[]`, `risks[]`, `presentation.human_verification[]`, `readiness[]` |
| 8 | Next step | `next_best_step` |
| 9 | Prototype note and assumptions | `presentation.flags`, `simulation_flags`, `assumptions[]` |
| 10 | For Happenee, in an `A+B` run only | `capabilities[]`, `presentation.human_verification[]` |

## Headings

| # | cs | en |
|---|---|---|
| title | `# {hero.event_name}` | `# {hero.event_name}` |
| 2 | `## Čemu rozumíme` | `## What we understood` |
| 3 | `## Mapa cesty` | `## Journey map` |
| 3b | `## Kde do vašeho plánu vstupuje Happenee` | `## Where Happenee comes into your plan` |
| 4 | `## Detaily větví` | `## Branch details` |
| 5 | `## Přehled funkcí` | `## Capability overview` |
| 6 | `## Co nepoužít a proč` | `## What you do not need and why` |
| 7 | `## Otevřené otázky a co ověří člověk` | `## Open questions and what a human verifies` |
| 8 | `## Další krok` | `## Next step` |
| 9 | `## Poznámka k prototypu a předpoklady` | `## Prototype note and assumptions` |
| 10 | `## Pro Happenee` | `## For Happenee` |

Phase headings inside section 3 are `### {label}`, where `label` is the
`phase_key` entry from the labels file: Před událostí, Příchod, V průběhu, Lidé,
Provoz na místě, Značka a partneři, Po události, Další ročník; Before the event,
Arrival, During, People, Live operations, Brand and partners, After the event,
Next event.
Branch headings inside section 4 are `### {branch_details[].branch_id}: {title}`,
where `title` is the branch title from the matching `journey_map` branch.

## Section 1: Hero

No heading of its own beyond the document title. `understood_summary` opens with
what changes for the organizer, not with the setup: where the brief names a pain
or an outcome, its first sentence has the shape cs „Návrh je postavený tak, aby
{what the pain becomes}.“ / en "The proposal is built so that {what the pain
becomes}.", and the setup comes in the second sentence at the earliest. Lines in
this order, each one omitted when its field is `null`:

```
# {hero.event_name}

{hero.understood_summary}

- {label:organizer} {hero.organizer}
- {label:audience} {hero.audience}
- {label:goal} {hero.goal}
- {label:scale} {hero.scale}
- {label:date} {hero.date_or_period}
- {label:archetype} {hero.archetype_label}
- {label:format} {hero.format_assumption}
```

Field labels, which are render strings and not schema enums:

| key | cs | en |
|---|---|---|
| organizer | `Pořadatel:` | `Organizer:` |
| audience | `Publikum:` | `Audience:` |
| goal | `Cíl:` | `Goal:` |
| scale | `Rozsah:` | `Scale:` |
| date | `Termín:` | `Date:` |
| archetype | `Typ události:` | `Event type:` |
| format | `Formát:` | `Format:` |

## Section 1b: Outcomes

What the event is for, from `outcomes`, before what we understood about it.
Four groups of bullets in this order, each one printed as a bold group label
and then its list in array order:

```
**{label:business}**

- {each outcomes.business item}

**{label:participant}**

- {each outcomes.participant item}

**{label:operator}**

- {each outcomes.operator item}

**{label:partner}**

- {each outcomes.partner item}
```

A group whose list is empty is not printed, its label included. No heading of
its own, the same as section 1: these are the sentences the hero is the title
of.

| key | cs | en |
|---|---|---|
| business | `Co z toho má mít pořadatel` | `What the organizer gets out of it` |
| participant | `Co z toho má mít účastník` | `What the attendee gets out of it` |
| operator | `Co z toho má mít tým na místě` | `What the on site team gets out of it` |
| partner | `Co z toho mají mít partneři` | `What the partners get out of it` |

Under the groups, when `event_success` is not `null`, one line for the measure
and, when `shown_to` is not `null`, one for the person it is shown to:

```
{label:success_measure} {event_success.measure}
{label:success_shown_to} {event_success.shown_to}
```

| key | cs | en |
|---|---|---|
| success_measure | `Podle čeho poznáte úspěch:` | `How you will know it worked:` |
| success_shown_to | `Komu to ukážete:` | `Who you show it to:` |

Under the measure, when `success_criteria[]` is not empty, a bold label and one
bullet per record in array order: the goal without its final full stop, a colon, the measure, then in brackets the
evidence and the moment, and the certainty label after a middle dot only when
the record is a working assumption. `side`, `data_sources`, `shown_to` and
`decision_after` stay in the JSON for whoever evaluates the event.

What the values mean, so the record says the same thing to whoever reads it
after the event. `evidence`: `metric` a figure, `qualitative` feedback or a
judgement, `both`, or `not_collected` when nothing the organizer or Happenee
collects today would show it, a gap to name and never a figure to invent, with
`data_sources: []`. `data_sources`: `registration`, `attendance`, `app` and
`communication` are what Happenee measures (registrations and their sources,
check-in, use of the attendee app, delivery and opening of e-mails);
`feedback_survey` is a survey the organizer runs; `partner_report`,
`sales_followup` and `other` are collected outside Happenee. `evaluated_when`:
`before` the event (registrations against the target), `during`,
`right_after`, `weeks_after` (a change people show later), or `unknown`.

```
**{label:success_criteria}**

- {goal}: {measure} ({label:evidence.<evidence>}, {label:when.<evaluated_when>}) · {certainty label}
```

| key | cs | en |
|---|---|---|
| success_criteria | `Jak poznáte, že se jednotlivé cíle splnily` | `How you will know each goal was met` |
| evidence.metric | `číslo` | `a figure` |
| evidence.qualitative | `zpětná vazba nebo posouzení` | `feedback or judgement` |
| evidence.both | `číslo i posouzení` | `a figure and a judgement` |
| evidence.not_collected | `dnes se nesbírá` | `not collected today` |
| when.before | `před událostí` | `before the event` |
| when.during | `během události` | `during the event` |
| when.right_after | `hned po události` | `right after the event` |
| when.weeks_after | `s odstupem týdnů` | `weeks after the event` |
| when.unknown | `kdy, zatím nevíme` | `when is not settled yet` |

The section is skipped under rule 5 only when all four lists are empty,
`event_success` is `null` and `success_criteria[]` is empty.

The number is `1b` and not `2` on purpose. The artifact shape paragraph, the
packaged skill files and the runner all name `section 9`, so renumbering
everything after the hero would rename the section those texts point at.

## Section 2: What we understood

One card per `understood_cards[]` entry, in array order:

```
- **{card.label}:** {card.value} · {labels.certainty[card.certainty]}
```

When at least one card has `certainty: "working_assumption"`, one line stands
between the heading and the first card, once for the whole list:
cs `Položky označené jako pracovní předpoklad jsme odvodili z briefu a z vašich odpovědí, upřesnit je můžete kdykoli.` /
en `Items marked as a working assumption come from the brief and your answers, and you can refine them at any time.` The card
itself carries its certainty label and nothing under it: the same sentence under
every assumption reads as a template, not as care.

## Section 3: Journey map

All eight phases, in schema order, whatever their `applicable` value.

For an applicable phase:

```
### {phase label}

{phase.summary}

- **{branch.title}** · {branch.participant_moment}
  - {label:condition} {branch.condition}
  - {label:capabilities} {capability labels, joined with ", "}
  - {label:detail}
```

The condition line is omitted when `condition` is `null`. The detail line is printed only when `has_detail` is `true`, and it points at the
heading in section 4 by the branch title: a `branch_id` such as `b-arrival-01` is a
story identifier and never reaches the reader, here or in a heading. Capability labels are the `name` of the matching `capabilities[]` entry, found
by the join written out in section 4. One key resolves to one string in both
sections, and the renderer needs nothing but the story object. A key with no entry
there is a defect. The capabilities line itself is omitted when `capability_keys[]`
is empty, under the same empty-list-omits-output rule that governs a whole
section: a label with nothing after it is not a line.

For a phase with `applicable: false`:

```
### {phase label}

{label:not_used} {phase.reason_if_skipped}
```

| key | cs | en |
|---|---|---|
| condition | `Platí, když:` | `Applies when:` |
| capabilities | `Funkce:` | `Features:` |
| detail | `Detail níže` | `Detail below` |
| not_used | `Nepoužíváme:` | `Not used here:` |

## Section 3b: Where Happenee comes into your plan

The same three groups the planning map is read through, after the journey map
and built from fields the story already carries. Nothing here is a new field
except `presentation.organizer_scope`, and nothing here says what Happenee
cannot do: it says what stays with the organizer.

```
## {heading 3b}

**{label:covered}**

- **{phase label}**
  - {branch.title} · {why of that branch's detail}

**{label:needed}**

- {data_needed.reason}

**{label:yours}**

- {each presentation.organizer_scope item}
```

The first group takes every phase of `presentation.journey_map.phases[]` with
`applicable: true` and at least one branch, in schema order, and under it that
phase's branches in array order. A branch with a `branch_details[]` entry of the
same `branch_id` prints its title and that entry's `why`, so the group says what
each part does for this event and not only what it is called; a branch without
one prints its title alone. The second takes every
`presentation.branch_details[].data_needed[]` entry whose `status` is
`unknown`, in array order across the details, the first entry per `key` only:
the same fact missing in three branches is one thing to send, not three. The
third is `presentation.organizer_scope` verbatim, and it is printed only when
that list is non-empty, because a story that always listed what Happenee leaves
alone would read as a list of reservations.

A group whose list is empty is not printed, its label included, and when all
three are empty the whole section is skipped under rule 5.

| key | cs | en |
|---|---|---|
| covered | `Kde vám Happenee pomůže` | `Where Happenee helps` |
| needed | `Co od vás k tomu potřebujeme` | `What we need from you for it` |
| yours | `Co zůstává u vás a vašich dodavatelů` | `What stays with you and your suppliers` |

The number is `3b` for the reason `1b` is `1b`: the texts that point at
`section 9` are not touched by a section inserted above it.

## Section 4: Branch details

One block per `branch_details[]` entry, in array order, after the visual legend:

```
## {heading 4}

{visual legend, once}

### {title}

{what_we_understood}

**{label:setup}**

- {each recommended_setup item}

**{label:why}** {why}

**{label:capabilities_setup}**

- {capability.name} · {labels.truth_status[capability.truth_status]}
  - {truth sentence for that status, when the status has one}

**{label:validate}**

- {each needs_validation item}

**{label:data}**

- {data_needed.reason} · {render_string:data_status[status]}

{image reference, when visual_ref is set}
```

The `{label:capabilities_setup}` block is the branch's capabilities with their
truth labels, and it is the only place in section 4 where a truth label appears.
It is not the same list as `{label:setup}`: `recommended_setup[]` is free text the
model wrote, this one is resolved from the data. Build it with this join, which is
the only join in the document:

1. Take the `branch_details[]` entry's `branch_id`.
2. Find the branch with that `branch_id` in
   `presentation.journey_map.phases[].branches[]`. A `branch_id` with no branch is
   a defect: the renderer stops and reports it.
3. Read that branch's `capability_keys[]`, in array order.
4. For each key, find the `capabilities[]` entry whose `key` matches, and print its
   `name`. A key with no `capabilities[]` entry is a defect and stops the renderer
   as well, because a capability named without its status is exactly what the truth
   labels exist to prevent.

The printed status is `labels.truth_status[truth_status]` and nothing else;
`commercial_state` belongs to section 5, so that a branch reads as a description of
the setup rather than as an offer. A status that carries a fixed sentence prints it
on the following line, indented by two spaces, under the same rules as section 5.
When the branch's `capability_keys[]` is empty the `capabilities_setup` block alone is omitted,
heading included, and the rest of the detail (`what_we_understood`,
`recommended_setup`, `why`, `needs_validation`, `data_needed`) is rendered as
usual.

The `needs_validation` and `data_needed` blocks are omitted when their arrays are
empty. `data_needed[].status` has no entry in the labels file, so its three values
are render strings defined here:

| `status` | cs | en |
|---|---|---|
| `provided` | `Máme` | `Provided` |
| `unknown` | `Chybí` | `Missing` |
| `assumed` | `Předpoklad` | `Assumed` |

The visual legend is printed once, between the heading and the first branch,
and only when at least one `branch_details[]` entry has `visual_ref: null`:
cs `Kde u větve zatím není obrazovka produktu, doplní ji člověk z Happenee.` /
en `Where a branch has no product screenshot yet, a Happenee human adds it.` A
branch without a visual prints nothing in its place: the same sentence under
every branch reads as a flaw in the proposal rather than as honesty.
When `visual_ref` is
set, the renderer prints a Markdown image reference naming the `shot_key`,
`![{shot_key}](shots/{shot_key}.png)`, as the last line of that branch, and nothing else: `_data/shots.json` (the
shot registry) carries only the pixel dimensions a responsive `srcset` needs, no
caption or path, so the `shot_key` itself, formatted as a reference, is what "the
image reference the shot registry gives" resolves to. The renderer never draws or
describes a screen that does not exist.

| key | cs | en |
|---|---|---|
| setup | `Co nastavíme` | `What we set up` |
| why | `Proč:` | `Why:` |
| capabilities_setup | `Nastavení` | `Setup` |
| validate | `Co ověříme` | `What we verify` |
| data | `Co k tomu potřebujeme` | `What we need for it` |

## Truth labels

Two places print a truth label, and no others: the `{label:capabilities_setup}`
block of section 4, and section 5. The strings are defined once, here, so that both
say the same thing.

The label itself is `labels.truth_status[truth_status]`, printed with no prefix,
because every one of the four reads as a status on its own. The commercial label,
which appears in section 5 only, does take a prefix: `Součást licence` with nothing
in front of it could be read as a promise about this customer's contract.

| key | cs | en |
|---|---|---|
| commercial | `Obchodně:` | `Commercially:` |

Two of the four statuses carry a fixed sentence. It is printed as its own bullet
under the capability, indented by two spaces, and it is never merged into a
sentence that promises the capability. Write "we would set this up, and
availability for your licence needs checking", never "this is included, needs
validation".

| `truth_status` | cs | en |
|---|---|---|
| `needs validation` | `Zda to vaše licence zahrnuje, potvrdí Happenee.` | `Happenee confirms whether your licence includes this.` |
| `planned-or-not-available` | `Tato možnost dnes není k dispozici.` | `This option is not available today.` |

`standard` and `configurable` carry no sentence, print no `canonical_source` and
add nothing. Sources stay in the JSON.

`availability_subtype` has no labels-file entry either. When it is not `null` it is
printed in parentheses at the end of the fixed sentence, in both sections:

| `availability_subtype` | cs | en |
|---|---|---|
| `planned` | `v přípravě` | `planned` |
| `proposed` | `návrh` | `proposed` |
| `unavailable` | `nedostupné` | `unavailable` |

## Section 5: Capability overview

One list of every capability the story selected, so that a reader can see in one
place what is standard, what needs checking and what nobody has confirmed for their
licence. Source `capabilities[]`, in array order, every entry whose `selection` is
not `not_selected`. A `not_selected` entry belongs to `do_not_use[]` and is printed
in section 6 instead, with its reason; printing it twice would read as a
contradiction.

```
## {heading 5}

- **{name}** · {labels.selection[selection]} · {labels.truth_status[truth_status]}{commercial part}
  - {truth sentence for that status, when the status has one}
  - {each limitations item}
```

`{name}` is the capability's label from the capability registry in the story's
language, copied into the story; a `key` is never printed as a name, here or in
any other section.

The commercial part is ` · {label:commercial} {labels.commercial_state[commercial_state]}`,
and it is printed only when `commercial_state` is not `unknown`. `unknown` means
nobody has checked this customer's licence, and a line saying so under every single
capability is noise that pushes the two that were checked out of sight.

`limitations[]` prints one bullet per entry, verbatim, after the truth sentence. An
empty `limitations[]` adds nothing. When no capability survives the `not_selected`
filter, or `capabilities[]` is empty, the whole section is skipped, heading
included, under rule 5.

`key`, `canonical_source`, `version_or_as_of`, `confidence`,
`commercial_boundary_evidence`, `phase_keys`, `branch_ids` and `source_refs` are
not rendered. They are how the story is checked, not how it is read.

## Section 6: What you do not need and why

One bullet per `do_not_use[]` entry, in array order:

```
- **{label or registry label for capability_key}** · {reason}
  - {label:reconsider} {reconsider_if}
```

`rule_ref` is internal and is never rendered. The printed name is `label` when
it is not `null`, and otherwise the capability registry's label for
`capability_key` in the story's language. The `capability_key` itself is never
the printed name.

| key | cs | en |
|---|---|---|
| reconsider | `Vrátíme se k tomu, když:` | `We revisit this when:` |

## Section 7: Open questions and what a human verifies

Four lists under one heading, each omitted when its source is empty, and the
section skipped under rule 5 only when all four are. First the open questions,
from `unknowns[]` where `answer_status` is not `unasked`, or where `critical` is
`true`:

```
- {unknown.question} · {labels.answer_status[answer_status]}
```

A `human_verification[]` row is `public: false` when it is about the licence
and what it includes, a price or a scoped service, Happenee's delivery capacity
and dates, a doubt about the customer's own readiness or data, or a competing
tool they already pay for; such a row prints in section 10 of an `A+B` run and
nowhere else, so this list never carries an owner such as „člověk z Happenee“
for a licence question (round 5a, b4: two licence rows printed here with that
owner and repeated in section 10).

Then the risks, `risks[]` verbatim in array order, under the bold sub-label
`{label:risks}`:

```
- {each risks item}
```

Every risk reaches the reader as written. Write it as what could go wrong at
this event and what that would cost, from the event and the answers, never as
something the product lacks and never with an id the reader does not know.

Then the verification list, from `presentation.human_verification[]` where `public`
is `true`, under the bold sub-label cs `Co ověří člověk` / en `What a human
verifies`:

```
- {question} · {reason} · {owner}
```

Last the checks by moment, `readiness[]` in array order, under the bold
sub-label `{label:checkpoints}`, and after the list one sentence for their
status, printed once rather than on every checkpoint:

```
- {readiness.checkpoint}

{render_string:readiness_status[not_verified]}
```

`not_verified` is the only `status` the schema allows; any other value is a
defect and stops the renderer, the way a label with no entry does.

| key | cs | en |
|---|---|---|
| risks | `Co může návrh ohrozit` | `What could put the plan at risk` |
| checkpoints | `Kontroly podle okamžiku` | `Checks by moment` |
| readiness_status `not_verified` | `Všechny tyto kontroly zatím zůstávají neprovedené.` | `None of these checks has been carried out yet.` |

The checks by moment stay under the heading of section 7 rather than in a
section of their own: they are what a human verifies, ordered by when, and a
new heading would split one list of things to verify in two.

An entry with `critical: true` is printed first in its list: a stable partition,
critical entries ahead of the rest, each group keeping the array order it already
had rather than being resorted by anything else. `presentation.human_verification`
entries with `public: false` are not rendered.

## Section 8: Next step

```
## {heading 8}

**{primary.label}** · {primary.what_happens_next}
{label:who} {primary.who_follows_up}
```

Then, when `alternatives[]` is non-empty, the sub-label cs `Další možnosti` / en
`Other options` and one bullet per alternative in the same shape. Labels and target
keys come from the run's target rows; the renderer never writes a link that the
target row does not carry, and a row whose `href` is `null` renders as text only.

| key | cs | en |
|---|---|---|
| who | `Navazuje:` | `Follows up:` |

## Section 9: Prototype note and assumptions

```
## {heading 9}

{presentation.flags.label[language]}

- {each limitation this run carries that changes how much the story can be trusted}

- {each simulation_flags key that is true, through the labels below}

**{label:assumptions}**

- {assumption.value} · {assumption.reason} · {label:impact} {assumption.impact_if_wrong}
```

**Limitation sentences.** The story object itself never carries this
line: it comes from the run, not from the model, so the model never writes it
and `artifact: markdown` never prints it either. Nor does the model write a
version of its own in another section: an article number or a sentence about
what was loaded means nothing to the reader. `render_story.py`'s `render()`
takes the run's limitation ids as an argument from whichever script called it
(`run_checks.py`, `scripts/runner/cli.py` or `scripts/runner/manual.py`, all of
which know them before `render_story.py` does) and prints one fixed sentence,
cs and en, for each id it recognises, in the fixed order below rather than the
order it received them. An id it does not recognise prints nothing; most of a
run's limitations are bookkeeping a reader does not need (`cost_not_reported`,
`model_actual_not_reported`) and only the ones that change how far the story
can be trusted get a sentence here. Two are wired up today:

| limitation id | cs | en |
|---|---|---|
| `ondemand_cap_reached` | Při přípravě téhle story se nenačetly všechny články nápovědy, ze kterých mohla čerpat, takže části, které se o ně opírají, nejsou ověřená konfigurace. | Not every help article this story could draw on was loaded while it was prepared, so the parts that lean on them are not verified configuration. |
| `budget_exhausted_after_reply` | Příprava skončila na limitu rozpočtu hned po odpovědi, ze které story vznikla, takže už neproběhl žádný další krok, který by ji mohl opravit nebo doplnit. | The preparation hit its budget limit right after the reply this story came from, so no further step that could have corrected or completed it followed. |

`ondemand_cap_reached` stays a general sentence rather than naming the specific
modules the dropped articles belonged to: a dropped article maps to a
`config/kb_module_map.json` module, and a module maps to several
`capability_keys[]` with no single one that stands for it, so picking one to
print would be the renderer inventing an emphasis the data does not give it,
which rule 3 forbids. No sentence prints when the run carries neither id.

Simulation flag labels, one bullet per key that is `true`, in this order:

| `simulation_flags` key | cs | en |
|---|---|---|
| `voice` | `hlas` | `voice` |
| `upload` | `nahrání souboru` | `file upload` |
| `generation` | `generování` | `generation` |
| `email_verification` | `ověření e-mailu` | `e-mail verification` |
| `booking` | `rezervace termínu` | `booking` |

A flag that is `false` is not listed. When every flag is `false`, the list is
omitted and only the prototype label prints.

| key | cs | en |
|---|---|---|
| assumptions | `Předpoklady` | `Assumptions` |
| impact | `Kdyby to bylo jinak:` | `If this is wrong:` |

## The insufficient story

When `output_status` is `insufficient_brief`, the document is short and has its own
headings. Sections 4, 5, 6 and 8 do not print at all. Their sources are empty in an
insufficient story anyway; saying so here means the renderer never has to decide.

| # | cs | en |
|---|---|---|
| title | `# Zatím nemáme dost na bezpečný návrh` | `# Not enough yet for a safe proposal` |
| body | `presentation.insufficient.message` | same |
| a | `## Co nám chybí` | `## What is missing` |
| b | `## Jak by mohla vypadat mapa cesty` | `## What the journey map would cover` |
| c | `## Další krok` | `## Next step` |

Under a: one bullet per `unknowns[]` entry whose id is in
`presentation.insufficient.missing_unknown_ids`, printed as
`- {question} · {why}`. Under b: the eight phase labels as a plain list with each
phase's `reason_if_skipped`, which is what makes the shape visible without
inventing content. Under c: `presentation.insufficient.safe_next_step`, followed by
the three-line example brief the model wrote in its reply, if the JSON carries one
in `manual_next_steps`: one paragraph per entry, in array order, with no bullet --
it stands for lines of a brief someone might paste, not a list of separate facts,
and a bulleted rendering would misrepresent it as one.

## Section 10: For Happenee

Printed only when the run header's knowledge tier is `A+B`, after section 9 and
after the status line's place in the artefact; in a Tier `A` run the section
does not exist, and no projection carries it. It is the layer a Happenee person
needs before an offer and the customer never sees, built from fields the story
already carries. The lead sentence says so, once:
cs `Tahle sekce je jen pro Happenee a do zákaznické verze nepatří.` /
en `This section is for Happenee only and does not belong in the customer version.`

Three lists, each omitted when empty, in this order:

```
## {heading 10}

{lead sentence}

**{label:coverage}**

{coverage intro}
- {count} · {truth_status label}
- {count} · {commercial_state label}

**{label:bends}**

- **{name}** · {truth_status label} · {commercial_state label} · {first limitation}

**{label:before_offer}**

- {question} · {reason} · {owner}

{delivery risks note}
```

The coverage map counts `capabilities[]` entries whose `selection` is
`recommended` or `conditional`: one line per `truth_status` in the vocabulary's
order, standard, configurable, needs validation, planned or not available, and
then one line each for `commercial_state` `additional_purchase`, `scoped_service`
and `unknown`, a line only where the count is above zero. The `unknown` line is
the offer's homework: how many selected capabilities have no verified commercial
state for this customer. Counts, never a percentage and never a verdict word: the
map is what a person reads a fit off.

"Where the product bends" lists, in `capabilities[]` order, the selected entries
whose `truth_status` is `needs validation` or `planned-or-not-available`, or
whose `commercial_state` is `additional_purchase` or `scoped_service`: the name
in bold, the status labels, and the first entry of `limitations[]` when there is
one. No source id and no `source_refs` reach the text.

"What to verify with the customer before an offer" prints every
`presentation.human_verification[]` row whose `public` is `false`, critical
rows first, in the shape section 7 uses; those rows print nowhere else. A row is
non-public when the customer should not read it as their own task: the licence
and what it includes, a price or a scoped service, Happenee's delivery capacity
and dates, a doubt about the customer's own readiness or data, a competing tool
they already pay for. A question the customer answers themselves is a public row
and belongs in section 7, not here, so the two lists do not repeat each other
(round 4: five of six rows repeated section 7 in other words). The `owner` of a
non-public row is a role inside Happenee written in the story's language, for
example cs „obchod“, „delivery“ or „customer success“, en "sales", "delivery" or
"customer success", the one place those roles are written, because this section
is theirs.

The last line refers to the risks instead of repeating them:
cs `Rizika dodání stojí v sekci „Otevřené otázky a co ověří člověk“ pod „Co může návrh ohrozit“.` /
en `Delivery risks stand in the section "Open questions and what a human verifies" under "What could put the plan at risk".`

| key | cs | en |
|---|---|---|
| coverage | `Mapa pokrytí` | `Coverage map` |
| coverage intro | `Doporučené a podmíněné funkce podle stavu, bez procent:` | `Recommended and conditional capabilities by status, no percentages:` |
| bends | `Kde se produkt láme` | `Where the product bends` |
| before_offer | `Co ověřit u zákazníka před nabídkou` | `What to verify with the customer before an offer` |

## Gate

`gate.public_sections` and `gate.verified_sections` decide what a reader sees
before verifying an e-mail address. Sections 1, 1b, 2, 3, 7 and 8 are public.
Sections 4, 5 and 6 are behind verification, along with the full `unknowns[]`
list and the save, send and share actions. Section 1b has no name of its own in
the gate vocabulary either; `schema/projection.public.json` whitelists
`/outcomes` and `/event_success`, so the four lists and the measure reach an
unverified reader with the hero they belong to. Section 3b is split by the same
rule rather than by a name of its own: its first and third groups rest on
`presentation.journey_map` and on `presentation.organizer_scope`, both
whitelisted, and its second group rests on `branch_details` and stays behind
verification with them. The `why` in the first group comes from
`branch_details` too, so an unverified reader gets the branch titles alone.
Section 7 is public, but two of its four lists are not: no projection
whitelists `risks` or `readiness`, so neither web document shows them, and only
the full document prints them. Section 5 has no name of its own in the gate
vocabulary; it renders under `branch_details`, because it is the same detail in
summary form and a truth label that a reader can see without the branch it belongs
to is the more misleading half. `schema/projection.public.json` does not whitelist
`capabilities`, so the data behind section 5 never reaches an unverified reader
either. The renderer does not invent a gate value for it.
A renderer producing the public document omits the
verified sections and prints, in their place, one line saying that the detail is
available after e-mail verification. It does not ship the hidden text in the markup
and then hide it with styling.

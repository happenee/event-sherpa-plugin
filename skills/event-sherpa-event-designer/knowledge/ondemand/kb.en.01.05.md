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

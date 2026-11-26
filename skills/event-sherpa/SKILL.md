---
name: event-sherpa
description: Use when the person mentions @Happenee or calls /event-sherpa about an event they plan or run, in Happenee or not yet, and no Event Sherpa role is loaded yet. Picks one of the eight roles and hands the request to it; answers nothing itself. Not for work unrelated to an event.
---

# Event Sherpa: pick one role

Version `sherpa-v0.2.4`. You only route: pick one role, load its skill
from this plugin and continue by it alone, with the message and
files unchanged. Read it with `get_event_sherpa_skill` and the id
only where it is not installed. Reuse a matching role.

| Role | Skill | Id | The person |
|---|---|---|---|
| Event Designer | `event-sherpa-event-designer` | `describe` | plans an event, even in one line, wants it set up, or a new edition |
| Content Manager | `event-sherpa-content-manager` | `compose` | asks about the agenda, speakers, sponsors, exhibitors or event texts, or hands them over |
| Registration Manager | `event-sherpa-registration-manager` | `register` | asks who may register and how, what the form asks, or hands over a form |
| Communication Manager | `event-sherpa-communication-manager` | `communicate` | asks about invitations, reminders, confirmations or follow-up e-mails, or wants one drafted or changed |
| Web Designer | `event-sherpa-microsite-designer` | `microsite-app` | asks how the event page looks, what it shows in which order, where people find the agenda, venue or registration |
| App Designer | `event-sherpa-app-designer` | `app` | asks what attendees see and do in the attendee app, its home page, or the questions, polls and networking in it |
| Event Insights | `event-sherpa-event-insights` | `insights` | asks how their event went, to analyze its data, a comparison or what to improve |
| Product Specialist | `event-sherpa-product-specialist` | `help` | asks how Happenee or a feature works, or whether an event is ready |

## How to pick

- How a feature works in general goes to Product Specialist. A decision
  about their own event goes to the role of that topic: "how does
  registration approval work" is Product Specialist, "do we need to approve
  each registration" is Registration Manager.
- How tickets, payments or check-in work: Product Specialist; an event's
  results, check-ins too: Event Insights.
- A new event to plan or create (even a bare "plan a conference"),
  or a request across several topics before an Event Story exists:
  Event Designer.
- What attendees see in the app or on the event page, even in
  general: App Designer or Web Designer.
- When no role or two fit equally, ask one short question in their
  language naming the two or three roles, then load the one the answer
  picks. Never ask when one role fits.
- Load one role; it hands off when the topic changes.

## What stays with the role

The role carries every rule for the Happenee connection, consent, saving,
texts and feedback. Until it is loaded, do not answer, plan or call other
Happenee tools.

# Setting up reservations in the Agenda — buses, workshops, social program

> How to use time slots and workshops to run reservation scenarios such as test drives or the social program.

- Article in the Help Center: https://help.happenee.com/en/articles/30-setting-up-reservations-in-the-agenda-%E2%80%94-buses-workshops-social-program
- Česká verze: https://help.happenee.com/cs/articles/30-nastaveni-rezervaci-v-programu-%E2%80%94-auta-workshopy-doprovodny-program
- Collection: Content and attendee experience
- Updated: 2026-09-09

---

> [!info] Overview
> The Agenda in Happenee is not only for talks — through **time slots** and **Workshops** you can also run **reservation scenarios**: test drives, social program (a balloon ride, a golf academy, a relax zone), equipment rental, or one-on-one meetings with experts. The mechanic is always the same — a session of type Time slot is split into slots, and the attendee picks one. This article shows **how to map real use cases to Agenda structure**.

## Getting started

- List **everything you want to offer to attendees as a reservation** — specific machines / activities, available times, capacities.
- Each reservable activity = one **session of type Time slot** (or several).
- For a larger offer (3 cars + 4 social-program activities), create **separate Agendas** — *Test drives*, *Social program*. Agenda (a content feature) can be added more than once.
- Each resource (a car, an instructor, a piece of equipment) is usually one session. Do not mix them into a single session with a higher capacity — you lose control over individual occupancy.

## Details

### Why use the Agenda for reservations

Happenee does not have a separate reservation module. Instead, it uses the **Agenda** and its **time slot** mechanic. Benefits:

- The attendee sees reservations in **My Agenda** as part of their schedule.
- The same filters (stage, tags, type) work for reservations as well.
- The attendee gets a **confirmation e-mail** with an ICS file (so they can add it to their calendar).
- Reservation slots can be combined with regular Agenda sessions — the attendee picks from one view.

### Typical use cases

**Car test drives (an outdoor event for an automotive brand).**
Each car = one session. Session length = the time window when the car is available (for example, 9:00–17:00). Slot length = the length of one drive plus handover time (for example, 20 minutes). Break length = time to refuel / reset (5 minutes).

Structure: Agenda *Test drives* → sessions *Mercedes GLE*, *Mercedes EQS*, *Mercedes AMG GT*, each with its own slots.

**Social program at a conference or company event.**
Each activity = one session. Balloon ride (1 session, 3 morning slots), golf academy (1 session, hourly slots), makeup artist (1 session, 15-minute slots), spa (1 session, 30-minute slots).

Structure: Agenda *Social program* → sessions *Balloon ride*, *Golf academy*, *Makeup artist*, *Massage*, each with its own slots and capacity.

**One-on-one consultations (networking or expert program).**
Each consultant = one session. For example, *One-to-one with the CFO*, *Consultation with the CMO*, *Mentoring with an internal expert*. 15–30-minute slots.

**Equipment rental (bike, laptop, experience kit).**
Each piece of equipment = one session. Slot length matches the rental duration. Capacity = 1 (one piece of equipment cannot be used by several people at once).

### Mapping real use cases to parameters

For each activity, decide:

- **How many units / instructors / devices do you have?** — Number of sessions
- **When is the activity available?** — Session start and end
- **How long does one reservation take?** — Time slot length
- **How much time do you need between reservations?** — Break length
- **How many people fit into one slot?** — Limit number of registrations
- **Should the activity be visible only to some attendees?** — Visibility (groups)

Example: a Mercedes EQS test drive, available 9:00–17:00, one drive of 20 minutes, 10 minutes for the handover (including the briefing), one driver per drive, only for clients:

- Session of type Time slot, time 9:00–17:00
- Slot length 20 min, break 10 min
- Limit number of registrations = 1
- Visibility: Selected groups only → *Clients*

The system generates roughly **16 slots** (9:00, 9:30, 10:00, …, 16:30).

### A practical tip: stages and instructors as Stages and Speakers

If activities take place **at different locations**, use the **Stages** feature (a tab in Agenda). Each stage = a hall, a tent, a parking lot, an open space. Assign them to sessions — the attendee then sees where to go.

If an activity has **a specific instructor or expert**, add them under **Speakers** and assign them to the session. The attendee then sees the name and profile on the slot detail.

### List view in the app

In the attendee app, the Agenda is shown as a list of sessions in chronological order; sessions with the same start time are ordered by the order of their types (see [How session types work](https://help.happenee.com/en/articles/27-how-session-types-work)). Filters (**Type**, **Stage**, **Tags**) help the attendee find what they care about. Sessions of type Time slot are visually distinct — the attendee sees that this is a reservation.

### Combining with engagement features

To a session you can attach:

- **Session rating** (an engagement feature) — after the reservation, the attendee rates the session (only if it is turned on at the type or session level).
- **Questions** — before the activity, they can ask questions (for example, *Should I bring my own helmet?*).

### Exports and reporting

At the session level you can export registrations to Excel — who reserved which slot. After the event, this gives you an overview of who attended what.

## Common pitfalls

### One session with capacity 3 for "test drives" — the organizer thinks attendees will be split across 3 cars

Each resource (a car, an instructor) = a **separate session**. Capacity 3 means 3 people arrive at the same time at the same place.

### The slot length does not account for handover / reset time, people overlap, and the next person waits

Plan a **realistic length plus a buffer**. A 15-minute test drive = a 20-minute slot. A 30-minute spa = a 45-minute slot (changing, questions). You pick the slot length from a fixed list (10, 15, 20, 30, 45, 50, 60, 90, or 120 minutes), so round the buffer up to the nearest available value. For details, see *How time slots work*.

### The social program sits in the same Agenda as the main conference sessions, and the attendee gets lost in the list

For clear separation, create a **separate Agenda** *Social program*. Agenda is a content feature — you can have several instances of it. Each Agenda has its own list, filters, and settings.

### A car is in service for half the day, but the slot is still bookable — the attendee shows up and discovers the problem

In the **Slots** tab of the session, switch the affected slots to **Inactive**. They block registration but stay in the structure for an overview.

### Capacity is open to everyone, but the activities are exclusive to VIPs — regular attendees register and there is no spot left

Set **Visibility: Selected groups only** or **Registration only for selected groups** on the session as a whole. Detail in *Setting up workshops and session registration*.

### Changing the slot length after the first reservation — the system blocks it

Slot length, break length, and session time are **locked** after the first registration. Plan the schedule carefully and test it on a trial account before opening it for attendees.

## Related articles

- [Building the event Agenda — architecture](https://help.happenee.com/en/articles/26-building-the-event-agenda-%E2%80%94-architecture)
- [How time slots work](https://help.happenee.com/en/articles/29-how-time-slots-work)
- [Setting up workshops and session registration](https://help.happenee.com/en/articles/28-setting-up-workshops-and-session-registration)
- [How session types work](https://help.happenee.com/en/articles/27-how-session-types-work)
- [How registration blocks, stages, and tags work](https://help.happenee.com/en/articles/31-how-registration-blocks-stages-and-tags-work)
- [How My Agenda works](https://help.happenee.com/en/articles/35-how-my-agenda-works)
- [Recommended setup for test drives](https://help.happenee.com/en/articles/98-recommended-setup-for-test-drives)

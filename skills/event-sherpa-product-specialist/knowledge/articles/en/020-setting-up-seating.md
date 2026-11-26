# Setting up Seating

> A paid advanced feature for assigning specific seats inside a pre-modeled venue.

- Article in the Help Center: https://help.happenee.com/en/articles/20-setting-up-seating
- Česká verze: https://help.happenee.com/cs/articles/20-nastaveni-seatingu
- Collection: Event setup and registration
- Updated: 2026-04-27

---

> [!info] Overview
> Seating is a **paid advanced feature** that the Happenee customer success team turns on for your workspace. It lets you assign specific seats to specific attendees inside a pre-modeled venue (O2 arena, Rudolfinum, or any custom venue modeled by Happenee for you). Important principle: **the attendee does not pick a seat**. After the attendee registers, the organizer (or designated assistants) assigns the seat, and only then does the system generate a ticket with the seat number.

## Getting started

- Seating is a **paid feature enabled via customer support** / customer success. If you want to use it, contact your CS person well in advance.
- Have the **venue floor plan** ready. Happenee already has O2 arena and Rudolfinum modeled; other venues are modeled to order.
- Decide who will assign seats: a single organizer, several assistants split across zones, or a script-based bulk assignment.
- Seating is not self-serve in the standard event admin. The Happenee team prepares the venue, the zones, and the access for you.

## Details

### How Seating works in Happenee

Seating in Happenee is the **reverse process** compared to public ticketing where the buyer picks a seat:

- The attendee **registers first** (normally, without choosing a seat).
- After registration, the organizer or a designated assistant **assigns the seat** in the seating admin.
- Only after the seat is assigned does the system generate the **final ticket** with the seat number.

So the attendee never picks a seat during purchase or registration. This is intentional. Happenee focuses on corporate events where the seating layout is driven by the organizer (typically by internal logic: the sales team sits with their clients, management gets VIP spots, and so on).

### Pre-modeled venues

The following venues are already modeled in the system:

- **O2 arena** (Prague).
- **Rudolfinum** (Prague).

Other venues can be modeled by Happenee to order. Contact customer success, send the floor plan (at reasonable accuracy), and the team builds a digital model of the venue including sections, rows, and seats.

### Ways to assign seats

**One person assigns manually.** The simple scenario. The organizer goes through the attendee list and drags people onto seats in the digital floor plan. A good fit for smaller events or events with a clear hierarchy.

**Bulk assignment by script.** For large events you can load the attendee list and let the system place attendees automatically. Used, for example, at conferences where seat order does not matter.

**Zone-based assignment with multiple assistants.** The venue is split into **zones** (for example, *Section A*, *Section B*, *VIP section*) and each assistant only has access to their own zone. Each assistant then places attendees from *their* list into their own seats. A good fit for large corporate events where different teams handle different parts of the venue.

### When the ticket with a seat is generated

A ticket with a specific seat number is generated **only after** the seat is assigned. Before that, the attendee has a regular ticket without a seat number (or no ticket at all, if you set it up that way). The flow:

1. The attendee registers and receives a regular confirmation e-mail (without a seat number).
2. The organizer or assistant assigns a seat in the seating admin.
3. After the assignment, a ticket is generated with the **seat, row, and section number**.
4. Happenee sends a new e-mail with this ticket, or the attendee finds it inside the attendee app.

The timing of when these tickets are sent is usually up to the organizer, often as close to the event as possible to avoid reshuffles when someone drops out.

### Combining Seating with paid Tickets

Seating works alongside paid Tickets, but the purchase step stays the same as for regular paid events. The attendee **does not pick a place**. Tickets are differentiated by type (standard / VIP / partner), and the assistant later places each attendee into the matching zone based on the ticket type.

### Pricing and activation

Seating is a **paid advanced feature**. It is not part of the standard Happenee plan. Activation goes through customer success:

1. Contact your customer success person.
2. Send the basic event information: number of attendees, venue, date.
3. The Happenee team reviews the requirements and, if needed, models a new venue.
4. Once activated, Seating shows up as a separate section in the event menu.

## Common pitfalls

### Expecting the attendee to pick a seat during the purchase flow (like in commercial ticketing such as Ticketmaster)

Seating in Happenee is reversed. The attendee registers, and the organizer places them. If you need free seat selection by the buyer, Happenee is not the right tool.

### Trying to start Seating in the self-serve admin without contacting customer success

Seating is not self-serve. Until the CS team turns it on, you will not see it inside the event admin. Contact your CS person with enough lead time (at least a month for pre-modeled venues, more for new ones).

### Creating Tickets without thinking through the types, so during seat assignment the assistants do not know who has VIP and who has standard

Define ticket types (standard / VIP / partner) so they are clearly distinguishable. If different ticket types go to different zones, link the ticket type to the zone type.

### Sending tickets with seats right after assignment, while the attendee mix keeps shifting before the event and seats need to be moved

Plan the final ticket send **as late as possible** before the event. If you send early and then reorganize, the attendee gets confused or you end up with a conflict at the door.

### Zone-based distribution without clear rules about who has access to which zone — assistants place people in the same seats and a conflict appears

Before you start assigning, split the zones clearly between the assistants. One zone equals one responsible person. If a conflict happens (two attendees in the same seat), the system escalates to the organizer.

## Related articles

- [Setting up Tickets](https://help.happenee.com/en/articles/18-setting-up-tickets)
- [Managing Orders and invoices](https://help.happenee.com/en/articles/19-managing-orders-and-invoices)
- [Recommended setup for a conference](https://help.happenee.com/en/articles/55-recommended-setup-for-a-conference)
- [Recommended setup for an expo or trade show](https://help.happenee.com/en/articles/56-recommended-setup-for-an-expo-or-trade-show)

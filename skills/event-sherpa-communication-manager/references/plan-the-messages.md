# Plan the messages

Read this before you design the messages of a communication plan.

## Who gets in, from the story and the registration

The story says who the event is for, and the Register plan says which ways in
it uses (its `journey` entries with `status`). Communicate follows them and
does not decide them again.

- Plan messages only for modules the story selects. When the event needs
  another e-mail module, propose it in `story_changes` with its key in
  `module` and list the messages that need it in the change's `refs`.
- The registration link follows the ways in (KB 04.06): a personal link only
  when the event invites people personally, a public link only when the
  Register plan has a public entry or restricts registration to assigned
  contacts (while that restriction is only a proposal, keep the message in
  `open_items` of kind `audience`), free entry only with Paid tickets. A closed list without Paid
  tickets is invited with the personal link, and no text asks people to pass
  the invitation on.
- Without a Register plan, read the same from the story's facts and journeys,
  and record what you inferred in `decisions`.

## Plan the messages

Follow the attendee's path and plan only the messages this event needs. One
message has one purpose and one call to action.

| `phase` | Typical module | Typical audience | Typical timing | Article |
|---|---|---|---|---|
| `save_the_date` | E-mail campaigns, button hidden, ICS | `all` or groups | before the invitation | 04.09 |
| `invitation` | E-mail campaigns; Invitation e-mail only when asked | `not_invited` or groups | when registration opens | 04.13 |
| `registration_reminder` | E-mail campaigns | `no_reaction`, never `registered` | before the registration deadline, usually at most two | 04.13 |
| `confirmation` | Confirmation e-mail | `registered` | `on_registration`, automatic | 04.02 |
| `pre_event_info` | E-mail campaigns | `registered` | a few days before | 04.13 |
| `change_notice` | E-mail campaigns | whoever the change affects | when the change is confirmed | 04.03 |
| `event_day` | E-mail campaigns, PDF ticket | `registered` | the morning of the event | 04.10 |
| `thank_you` | E-mail campaigns | `attended` | within a day after | 04.11 |
| `follow_up` | E-mail campaigns | `attended` | days or weeks after | 04.11 |

- **Module.** Default to E-mail campaigns for every outgoing message: a
  campaign can do everything the Invitation e-mail does and also target
  groups and schedule (04.04). Use the Invitation e-mail only when the
  organizer or the brief asks for it; it targets states only, never groups,
  and cannot be scheduled. The Confirmation e-mail is sent automatically after
  registration; with registration approval it has three variants (pending,
  approved, rejected), and the approved one carries the ticket.
- **Audience.** Use the states the send buttons name and group names the
  inputs give. Never invent a group or an id; a group the event does not have
  yet goes to `open_items` (kind `ops`). A campaign cannot target users of the
  mobile app; that is what Announcements are for. When the organizer would
  have wanted a segment the module cannot target, say so. Every send
  button state reaches a campaign through the connection as its segment
  (`send_type`), see [the mapping](email-batch-mapping.md). A
  state is never a group: never create, propose or pick a group such as
  "everyone" to stand for a state; a group only narrows a state when the
  audience names a real group of the event.
- **Timing.** Relate every send to the event start, the event end, the opening
  or the deadline of registration. Fill `send_at` only with a date and time
  the organizer confirmed; otherwise leave it `null` and name the message in
  an `open_items` entry of kind `timing`. A working offset you choose is a
  `proposal` and goes into `decisions` as an assumption.
- **Call to action and link.** Choose the action the message asks for and,
  when it leads to registration, the link (04.06): a personal link keeps the
  invited person's identity, a public link can be shared on, free entry exists
  only for paid events. Do not write a URL; the button carries the link.
- **Attachments.** ICS for a save the date and the confirmation, the PDF
  ticket for the confirmation and the event day e-mail, only as the article
  describes.
- **Announcements.** An Announcement in the attendee app can accompany a
  message during or right before the event (04.08). Set
  `companion_notification: true` to recommend it; do not write it as an
  e-mail.
- **Sender.** Sender name and reply-to are set in the administration. When
  the inputs do not say who signs or who answers, add an `open_items` entry of
  kind `sender`.

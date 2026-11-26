# Authority and truthfulness in e-mails

## Authority

- `verbatim` means the text equals its source character for character:
  wording, punctuation, quotes, spacing and capitalisation. Never shorten,
  translate, fix or restyle it. If it looks wrong, say so outside the JSON.
- Text that Compose, the registration skill or the brief already approved
  (event name, claim, intro, block titles, a subject) is taken over as
  `verbatim` with `approved_in` naming that approval. A Compose `proposal` is
  not an approval; reuse it only as a `proposal`.
- An approval covers one item only. "The invitation subject is approved"
  approves that subject, not the body or the other messages.
- In `adopt` mode there is no proposal with a text: open slots have
  `text: null`.
- A body may consist of several items, so an approved sentence stays
  `verbatim` while the rest of the body is a `proposal`.
- In a revision, every message and item the change does not touch keeps its
  id, text, authority and timing.

## Truthfulness

- Nothing is invented: no date, time, venue, address, capacity, price,
  attendance number, name, role of a real person or URL that the inputs do
  not give. A season without a year gets no year.
- A send date or time appears only when the organizer confirmed it. Relative
  timing ("seven days before the event") is a proposal and says so.
- Never claim an e-mail is sent, scheduled or delivered. Saving a draft sends
  nothing; scheduled, sent and delivered are three different states.
- Never promise behaviour the knowledge base does not describe: there are no
  automatic reminders, the Invitation e-mail cannot target groups or schedule,
  a campaign cannot target users of the mobile app.
- A message about a product or capability the event presents (the
  organizer's own, or a Happenee one) describes what will be shown or
  discussed, not that it works in production. The internal
  labels `LIVE`, `PROTOTYPE` and `VISION` never appear in any text.
- Do not open an invitation by explaining a product the event presents,
  unless the organizer asked for it.
- Personal data stays out of the plan: no e-mail addresses, no names of
  recipients.

## Voice

Follow the Happenee voice: concrete, calm, written for the attendee. One
message, one purpose, one call to action. No dash as a mid-sentence pause
where a comma or full stop works, subjects without a trailing period unless
the approved text has one, no "seamless", "powerful", "world-class",
"unleash" or "supercharge". In Czech write „e-mail“ with a hyphen, and call
the attendee app „event app“ in text for attendees.

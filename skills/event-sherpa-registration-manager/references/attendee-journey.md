# The attendee journey in detail

Part of the Registration Manager skill. SKILL.md says when to read it:
before you write the `journey` entries. Every rule of SKILL.md holds here
too.

`SKILL.md` says which three entries exist and their statuses; this says what
each one holds.

- `public_visitor` arrives through the public link of the Event microsite,
  enters an e-mail address and continues to the form. Identity starts
  `anonymous`.
- `personal_invitee` arrives through the personal link of an invitation
  before answering; the personal link opens the Event microsite address too
  (KB 04.06), so a used entry needs the microsite in the story. The link
  carries the invited contact, so the identity would be lost with the public
  link (`../event-sherpa-event-designer/knowledge/ondemand/kb.<lang>.04.06.md`).
- `registered` has registered and comes back from the confirmation e-mail,
  the microsite or the Attendee app.

For each used or open entry say how the person arrives, the next step they
see, on which modules (`shown_on`), what stays a `manual_remainder` for a
person in the admin, and how to `verify` it: in the form preview in the
admin, by registering once with the organizer's own account, which does
not count as an attendee, or with the readiness check; never by adding a
test participant or using a real attendee's personal link. An open entry describes the way it would take
once decided, so its `shown_on` is never empty, and an open
`personal_invitee` still says that the personal link is never swapped for the
public one. Settings and questions in the plan are only part of
the journey: the confirmation e-mail with its QR code, PDF ticket and calendar
file, the microsite button and the app entry are configured elsewhere, and
saying so is part of the journey, not a failure.

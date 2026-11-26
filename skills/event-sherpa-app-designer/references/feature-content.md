# Feature content

Read this before you plan the content of a feature on the Attendee app.

## Feature content

Every content or engagement feature the app uses is one entry in
`feature_content[]`, used by home tiles through its `instance_id`. The same
feature on the microsite is the same instance: when the conversation already
has the microsite plan of this story, reuse its `instance_id`, name, fields
and texts.

- A fact the input gives goes into its field whole, as the input words it,
  with `authority: verbatim`: "sál STORY B, Praha 4" stays that string and is
  not cut down to a name of your own. When the value mixes two fields (a
  room and a city), keep it whole in the field it names and leave the other
  field `null` with a `fact` open item.
- Fields hold only supplied data. A venue name, address, contact person,
  e-mail, phone, speaker, sponsor, logo, bio, capacity or link that the input
  does not give is a field whose content item has `text: null`, and an
  `open_items` entry of kind `fact` (or `asset` for images and logos) names
  it. Never fill one from the knowledge base or from general knowledge.
- No text holds a note to the organizer in place of a missing fact: no
  brackets, no "doplnit" or "TBD", no question. Write the sentence to read
  well without the fact and name the gap in `open_items` and in the reply.
- Speakers come from Compose `people[]`, sponsors and exhibitors from its
  `partners[]` (Compose 0.4 and later), linked by `person_id` or `partner_id`
  in `compose_refs` of the Speakers, Sponsors or Exhibitors instance; this
  skill only decides where they show. Link only a `confirmed` person or
  partner. A `recommended` or `missing` one is not shown anywhere: it is an
  `open_items` entry of kind `fact` until the organizer confirms it.
- Settings use the admin label and the value the input or the reason gives
  (for example "Zapnout soukromé zprávy": "vypnuto"). A setting the
  knowledge base does not describe is unverified, not proven absent: never
  invent its label or value. Check it against a current product source or a
  tool contract in the conversation; while it stays unverified, keep it as an
  `open_items` entry of kind `fact` and say what needs checking.
- `visibility` is `all` unless the input restricts the feature to named
  groups; name groups only as the input names them. Visibility applies in
  the app after login (KB 02.07).
- Every instance is used by an app entry or the handoff. A feature the plan
  does not show gets a decision saying why, not an empty instance.
- Name every feature the app shows for this event, so attendees see what
  they get there. Take a name the input or the Event Story gives as it is;
  otherwise propose one from the story (for example „Zeptejte se řečníků“
  for Questions) as a `content_items` proposal. Point `name_ref` to that
  item and set its `slot` to `name`. Keep the default name only where it
  already says this, and record that in `decisions`. Name features in the
  organizer's language, and in every language the event has when the input
  asks for them. The admin label stays in reasons and manual steps. The
  name shows on the app home page and on the microsite tab.

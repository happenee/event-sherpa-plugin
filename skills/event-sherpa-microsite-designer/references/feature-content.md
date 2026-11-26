# Feature content

Read this before you plan the content of a feature on the Event microsite.

## Feature content

Every content feature a microsite tab shows is one entry in
`feature_content[]`, used by its section through `instance_id`. The same
feature in the app is the same instance: when the conversation already has
the app plan of this story, reuse its `instance_id`, name, fields and texts.
Engagement features never appear on the microsite and never in this plan.

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
  brackets, no "doplnit" or "TBD", no question, in the intro text as much as
  in a field. The microsite is public once published, so write the sentence
  to read well without the fact and name the gap in `open_items` and in the
  reply.
- Speakers come from Compose `people[]`, sponsors and exhibitors from its
  `partners[]` (Compose 0.4 and later), linked by `person_id` or `partner_id`
  in `compose_refs` of the Speakers, Sponsors or Exhibitors instance; this
  skill only decides where they show. Link only a `confirmed` person or
  partner. A `recommended` or `missing` one is not shown anywhere: it is an
  `open_items` entry of kind `fact` until the organizer confirms it.
- Settings use the admin label and the value the input or the reason gives.
  A setting the knowledge base does not describe is unverified, not proven
  absent: never invent its label or value; keep it as an `open_items` entry
  of kind `fact` and say what needs checking.
- `visibility` is `all` unless the input restricts the feature to named
  groups; name groups only as the input names them. Visibility applies only
  in the app after login; the microsite is always public (KB 02.07, 03.01).
- Every instance is used by a microsite section or the handoff. A feature
  the plan does not show gets a decision saying why, not an empty instance.
- Rename an instance only to a name the input gives or the plan proposes in
  `content_items`. Point `name_ref` to that item and set its `slot` to
  `name`; the name shows on the microsite tab and in the app.

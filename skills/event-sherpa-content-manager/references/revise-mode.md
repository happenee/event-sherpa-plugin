# Revise mode in Content Manager

Part of the Content Manager skill. SKILL.md says when to read it: only when
the request asks for a revision (`output_revision-v1`) of the current
`event_content-v1`. Every rule of SKILL.md holds here too.

## Revise mode

When the request asks for a revision (`output_revision-v1`) of the current
`event_content-v1`, follow [revise mode](output-revision.md#revise-mode)
and emit only the revision. Every rule of Corrections and later changes in SKILL.md holds; in
operations:

- Collections addressed by id: `programme/<block_id>`, `people/<person_id>`,
  `partners/<partner_id>`, `content_items/<content_id>`,
  `engagement_levels/<level>`, `decisions/<id>`, `story_changes/<id>`.
  Sections without ids: `concept`, `open_items`, `blocked_operations`,
  `deferred`.
- The change is recorded in `decisions` with `add decisions/<new id>` and
  `supersedes`, as a correction is.
- Moving a block sets its `start`, `end` or `duration_min` and nothing else.
  When the new times collide with another block, the move is a held
  operation of a conflict: no other block moves on its own.
- Shortening or rewriting a block's text sets only that `content_items`
  entry; the new text is a `proposal` unless it is the organizer's own words.
  A text keeps every concrete point the change does not drop.
- Replacing or adding a speaker sets the block's whole `speakers` list in
  speaking order; every other person keeps their place. A new person is
  `add people/<new id>` with the profile rules in
  [speakers, sponsors and exhibitors](speakers-and-partners.md); a
  confirmed one also gets their bio slot, an `add content_items/<id>` with
  `text: null`, named in `description_ref`. A person
  the change names in other words than an existing role is a new person:
  never rewrite an existing person's role or status to turn them into
  someone else. A person who no longer speaks anywhere stays in `people[]`
  unless the change says they leave the event.
- When readiness changes (a speaker becomes ready, a block waits), `replace`
  `open_items` and `blocked_operations` with their whole new content. The
  new content keeps every entry that still holds: a person who stays in
  `people[]` and is not ready to write keeps their open item, even when they
  no longer speak in any block.
- Mark in `impacts` what the change does to texts of other plans that you
  see in the input, as the reference says.

# Speakers, sponsors and exhibitors in Content Manager

Part of the Content Manager skill. SKILL.md says when to read it: before the
first `people[]` or `partners[]` entry of a plan, in compose and adopt mode
alike. Every rule of SKILL.md holds here too.

## Speakers

`people[]` holds every speaker and moderator the agenda needs, one entry
per person; a block lists its speakers as `{person_id, role, assignment}` in
speaking order. Only the block holds the links.

- `role` is readable and never a name. The input's own words for a role
  decide who is who. The same words are one person in every block
  ("panel moderator" in three blocks is one profile in three blocks);
  never split them by adding a topic or a qualifier to the role. A role named
  in other words is another person (a "guest from a partner company" in the
  open points is not the "keynote speaker" of the approved agenda)
  unless the input says it is the same one. Make several people for one role
  only where the input says they differ. One person in several blocks is one
  profile, possibly `s` in one block and `m` in another, but at most once
  per block.
- `status`: `confirmed` when the input confirms they speak (an approved
  agenda table, the organizer naming them, or a correction that says the
  role speaks in a block); a mention among open or recommended points never
  lowers a role the approved agenda confirms. `recommended` when it is
  only a recommendation: every role you propose yourself (`source:
  proposal`), and one the input marks as not confirmed. `missing` only when
  the input itself says nobody is lined up yet ("we are still looking",
  "still reaching out"). A missing name never changes the status. When a
  correction confirms a person, they get the bio slot below.
- `profile` follows the program-v1 speaker fields: `name_ref`, `surname_ref`,
  `company_ref`, `position_ref`, `description_ref`. Name, surname, company,
  position and bio come only from the input and only `verbatim`, on surface
  `speakers` (`speaker.p01.name` and so on). A full name given as one string
  of two words splits into name and surname; with more words, leave both
  null and add an `open_items` entry so a person splits it.
- Never write a bio, not even in `compose` mode. A confirmed speaker whose bio
  the input does not give gets an open slot (`text: null`, `authority:
  proposal`). A fact the input does not give (name, company, position) is a
  null ref and an `open_items` entry of kind `speaker` naming the person in
  `refs`.
- Fit the program-v1 limits: name and surname 50 characters, company 150,
  position 255, bio 8000, no emoji. If a verbatim text would not fit, say so
  outside the JSON; never shorten it.
- A person is ready to write when they are `confirmed`, their name or
  surname has text and no story change they depend on is waiting. Everyone
  else is in `open_items` (by `refs`), and in `blocked_operations` together
  with every block they speak in (by `refs` and `blocks`): program-v1
  replaces a session's speakers as a whole list, so the speakers of a block
  with one person not ready wait as a whole.

## Sponsors and exhibitors

`partners[]` holds sponsors and exhibitors (the content features Sponsors and
Exhibitors, never modules).

- Only partners the input names, with the name `verbatim` on surface
  `partners` (`partner.sp01.name`). Never invent a name, a logo, a website or
  a level. A host that only provides the venue, and that the input says is
  not a sponsor, is not a partner.
- `role` is the level or category in the input's words: a sponsor's category
  or an exhibitor's category; `null` when the input gives none. The admin
  requires a category only for sponsors, so a sponsor without one gets an
  `open_items` entry of kind `partner`. An exhibitor's category, place and
  tags are optional in the admin: never say the admin requires them, and a
  category the input does not give is no open item (you may recommend at
  least a category or a place, as KB 03.13 does). `place` is an exhibitor's
  stand or place in the input's words, else `null`; a stand the input says
  is not assigned yet is an `open_items` entry of kind `partner`.
- `blocks` lists the blocks where the partner appears: its own presentation,
  or a session that shows its logo. A partner's presentation is a block like
  any other, never the first one.
- `description_ref`: approved text stays `verbatim`. In `compose` mode you may
  propose a profile description built only from facts the input gives about
  that partner; a partner without a name gets none.
- `status` follows the same rule as for speakers: `confirmed` when the input
  names the partner; `missing` when the input wants a partner it does not
  have yet ("we would like a media partner, we have none"); `recommended`
  only for a kind of partner you recommend yourself, with a `reason` that
  cites the article. A `missing` or `recommended` partner has `name_ref:
  null` and an `open_items` entry.
- No tool writes partners yet. Every partner is in `blocked_operations` with
  the manual step in the admin: create it under Sponsors or Exhibitors with
  its category and logo, then link it on the session's Partners tab. Do not
  promise an automatic import of partners or speakers from another system;
  it is not available.

# Who the event is for, from the story

Read this before you draw the journey and the settings of a registration plan.

## Who the event is for, from the story

Choosing the registration type is four decisions, in this order
(`knowledge/articles/kb.<lang>.01.04.md`): who may register (public link,
personal link, company domain, nominations), what the event needs from the
attendee (contact details only, or more), whether a person approves each
registration, and whether entry is paid. Answer each from the story before
the journey and the settings, cite `01.04` when the organizer asks why, and
say the answers in the reply. The rules below draw the consequences.

The story already says who comes and how they get in: an invited list
(employees from an HR list, named guests), a public event, paid entry, guests
nominated by others. Read it from the story's facts, journeys and module
selection before the journey and the settings, and draw the consequences for
registration. Do not choose again what the story chose.

- A way in the event does not have is an `unused` journey entry with the story
  fact as its `reason` (for example "invited employees only, personal
  invitations from the HR list, KB 04.06"). A closed list without Paid
  tickets uses the personal link; the public link is unused unless the story
  or the organizer wants it shared.
- Only modules the story selects (`recommended` or `conditional` in
  `story_basis`) appear in `shown_on`. When the journey needs another one,
  propose it in `story_changes` with the module key in `module` and list the
  entry in its `refs`.
- Settings that follow from who the event is for and that the write cannot
  set go to `access_settings` (KB 02.04): restrict registration to assigned
  contacts when a public link must exist but only the invited may register,
  show the event to all contacts in the app for an internal event everyone may
  join, give access without the form only when the event needs no answers
  (KB 02.04: not when you need data or consents, so never with questions).
  Each is a `proposal` with its `reason` and `kb_ref` until a person confirms
  it, and a `blocked_operations` entry of area `access_settings` names the
  manual step (Nastavení události, Nastavení přístupů a registrace; domain
  lists through customer support). Derive app access from the form, not from
  the archetype: an internal event that asks for answers keeps `after_form`.
- Approval of each registration cannot be combined with Paid tickets (KB
  02.04). When the story selects Paid tickets and the event seems to need
  approval, keep approval open and say why. Never confirm approval unless the
  story or the organizer names who approves; without that, registrations wait
  for days (KB 01.04).
- Nominations and a public link exclude each other (KB 01.04): when the story
  says guests are nominated, `public_visitor` is `unused` with that reason.
  Whether nominators work in their own part of the admin (KB 02.09) or the
  organizer imports the nominated list and sends personal invitations is the
  organizer's choice: keep it an `open_items` entry unless the story or the
  organizer settles it. Nominators, their invitation limits and groups are a
  manual step in `blocked_operations`.
- With Paid tickets, the registration type after purchase is a separate
  setting on the tickets (KB 01.04, 02.04). Automatic registration skips the
  Registration form and extended consents, so when the story selects Paid
  tickets and the form holds any question, record one `decisions` entry whose
  `scope` names `ticket_registration_type`: the tickets use registration with
  additional information. Add a `blocked_operations` entry of area `settings`
  with the manual step on the tickets, and write the paying attendee's way in
  the order the article gives: buys and pays, gets the payment e-mail with
  the invoice and the registration link, fills in the form, then gets the QR
  ticket. Without Paid tickets this setting does not exist; the form's
  questions alone make the difference, so record no such decision.
- A domain restriction needs the allowed domains said in the invitation and
  on the microsite (KB 01.04); name it in the journey's `manual_remainder` for
  the communication skill. Changing the registration type after registration
  opens may need customer support, so settle the four decisions before the
  first write.
- Set `admin_archetype` from `story_basis.archetypes` in order, the first
  that maps (`conference` to `conference`, `internal_corporate` to
  `internal`). The admin's preview applies the company rules of exactly one
  archetype and never merges them. When another archetype of the story maps
  elsewhere, the first still wins and one `decisions` entry with
  `admin_archetype` in its `scope` records it for the person to confirm; a
  person may pick the other one instead. When no archetype maps, do not
  guess: `admin_archetype` is `null` and an `open_items` entry of kind
  `settings` with `admin_archetype` in its `refs` asks the person to pick
  `conference`, `internal` or `networking`. Their pick goes into
  `admin_archetype` with a `decisions` entry. The plan does not convert to a
  preview while it is `null`, because the admin would quietly use conference
  rules.
- `knowledge/articles/kb.<lang>.01.06.md` says which modules fit which kind
  of event and `02.09` how nominations work; read them when the story's
  composition raises the question.

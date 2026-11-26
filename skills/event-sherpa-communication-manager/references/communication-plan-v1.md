# communication_plan-v1

The output of Communicate. JSON Schema: `schema/communication_plan.schema.json`
in the skill source; this page is the readable form. All keys are required;
use `null` or `[]` where a value is not known. Read
[Before you finalize the plan](#before-you-finalize-the-plan) at the end before you
emit a plan.

| Key | Meaning |
|---|---|
| `schema_version` | always `communication_plan-v1` |
| `output` | id and revision of this plan, the same shape in every Event Sherpa skill: `output_id` (assigned by whoever stores the plan, copied, `null` when not stored), `revision` (`1` for a new plan, else the previous plus 1), `supersedes_revision`, `change_id`, `bindings[]` (written only by the MCP, copied unchanged); see [plan revisions](output-revision.md) |
| `story_ref` | the approved Event Story: `story_id` and `story_version` from its `presentation`, always set; `blueprint_id` and `revision` when the story is stored, both `null` for a story made in the conversation |
| `story_basis` | what the plan took from the story: `source`, `archetypes[]`, the eight `modules[]` with their `selection`; the same shape in every Event Sherpa skill, see [reading the Event Story](story-basis.md) |
| `content_ref` | the Compose output this builds on: `schema_version` (`event_content-v1`), the `story_id` and `story_version` of its `story_ref` (the plan's story) and its `mode` and the `output_id` and `revision` of its `output` header (revision `1` for an output without one); `null` when there is none |
| `registration_ref` | the Register output, same shape with `schema_version` `registration_plan-v1`; `null` when there is none. Its `journey` says which ways into the event exist |
| `language` | `cs` or `en`, same as the story |
| `mode` | `compose` (proposes) or `adopt` (takes over a finished brief, writes no text) |
| `org_context[]` | approved organization records the plan follows: `record_id`, `revision`, `category` (`preference`, `rule`, `lesson`), `applied_to`; `[]` when `get_organization_context` is not available |
| `messages[]` | one entry per e-mail, see below |
| `content_items[]` | every text, see below |
| `decisions[]` | `id`, `scope`, `reason`, `as_of_and_source`, `revisit_trigger`, `supersedes[]` (same shape as in the Event Story and in Compose) |
| `deferred[]` | `item`, `decided_in`, `reason`; postponed by a person, never raised again |
| `open_items[]` | `item`, `kind` (`copy`, `timing`, `audience`, `sender`, `ops`, `content`), `refs` (message ids it holds up, or `null`) |
| `blocked_operations[]` | what the admin's MCP cannot write: `operation`, `refs` (message ids), `blocked_by`, and the `manual_step` a person does in the administration instead |
| `story_changes[]` | proposed changes to the approved Event Story, the same shape in every skill: `id`, `change` (`add`, `drop`, `change`), `module` (the key of the module it adds, drops or changes, `null` for a feature or setting), `subject` (the module, feature or setting in product terms), `reason`, `knowledge_ids` (at least one article the skill carries, for example `kb.cs.04.08`) and `refs` (message ids that depend on the change, or `null`) |

## Message

| Key | Meaning |
|---|---|
| `message_id` | stable across revisions, for example `m01` |
| `phase` | `save_the_date`, `invitation`, `registration_reminder`, `confirmation`, `pre_event_info`, `change_notice`, `event_day`, `thank_you`, `follow_up` |
| `module` | `invitation-email` (Invitation e-mail), `confirmation-email` (Confirmation e-mail) or `email-campaigns` (E-mail campaigns) |
| `purpose` | what the message should achieve (internal, not copy) |
| `audience` | `state` (the send button: `all`, `registered`, `not_invited`, `no_reaction`, `unread_invitation`, `attended`, `viewed_web_app`, `not_viewed_web_app`; `null` while open), `groups` (group names from the inputs, never ids; `[]` for no group restriction) and `note` |
| `timing` | `anchor` (`event_start`, `event_end`, `registration_open`, `registration_deadline`, `on_registration`; `null` while open), `offset_days` (negative before the anchor), `time` (event-local `HH:MM`), `send_at` (event-local `YYYY-MM-DD HH:MM`, only when the organizer confirmed it) and `origin` (brief source, decision id or `proposal`) |
| `cta` | `action` (`register`, `add_to_calendar`, `open_app`, `read_info`, `give_feedback`, `none`) and `link_type` (`personal`, `public`, `free_entry` for paid events only, `none`) |
| `subject_ref`, `body_refs[]`, `button_ref` | `content_id`s of the subject, the body parts in order (joined with a blank line) and the button text; `button_ref` may be `null` |
| `attachments[]` | `ics`, `pdf_ticket` |
| `must_include[]` | facts or elements the inputs require in the message, in their words |
| `companion_notification` | `true` when a matching Announcement in the attendee app is recommended; it is not written here |
| `source` | where the message comes from: brief, answer, decision id or `proposal` |

### What each module allows

| `module` | `phase` | `audience.state` | `audience.groups` | `timing` |
|---|---|---|---|---|
| `invitation-email` | `save_the_date`, `invitation`, `registration_reminder` | `not_invited`, `unread_invitation`, `no_reaction` | always `[]`, it cannot target groups | sent by a person; no scheduling |
| `confirmation-email` | `confirmation` only | `registered` | `[]` | `anchor` `on_registration`, automatic |
| `email-campaigns` | any but `confirmation` | any | any | scheduled or sent by a person |

## Content item

| Key | Meaning |
|---|---|
| `content_id` | stable across revisions, for example `m01.subject` |
| `message_id` | the message the text belongs to |
| `slot` | `subject`, `body` or `button` |
| `text` | plain text, or `null` for an open slot that may not be written yet |
| `authority` | `verbatim` (use exactly), `proposal` (Communicate's suggestion), `editable` (may change within `edit_scope`) |
| `edit_scope` | for `editable` only, what may change; else `null` |
| `source` | brief turn, answer, Compose `content_id` or decision id; `proposal` for new text |
| `depends_on` | what the text states: `fact:<key>` (a story fact), `setting:<key>` (a Register setting), or the id of an item of this plan or an earlier plan, alone or with a field (`b03.start`, `p02`); `[]` when none; see [plan revisions](output-revision.md) |
| `approved_in` | decision id or brief source that approved this item alone; `null` for proposals |

A subject is one line of plain text, at most 250 characters. A body is plain
text without HTML or placeholders, at most 10 000 bytes in UTF-8 after its
parts are joined, and without characters outside the basic Unicode plane
(no emoji). Those are the limits the admin's draft accepts.

## Rules a checker enforces

- Every reference resolves to a `content_item` of the same message and the
  right slot.
- Every `verbatim` item has a text found word for word in the inputs and an
  `approved_in`. In `adopt` mode no `proposal` item has a text.
- A message with `send_at: null` that a person has to send (every module but
  `confirmation-email`) is named in an `open_items` entry of kind `timing`.
  `send_at` is never set from a proposal.
- Every `invitation-email` and `confirmation-email` message is named in
  `blocked_operations`, because the admin's MCP cannot write either module.
- No text carries HTML, a `::PLACEHOLDER::`, the internal labels `LIVE`,
  `PROTOTYPE` or `VISION`, or, in a proposal, a dash used as a mid-sentence
  pause.
- `story_basis` matches the stored story when the story was given whole, and
  the Register plan's `story_basis` when one was given.
- A message goes through a module the story selects, or through one a story
  change adds; then the message is in that change's `refs`.
- `link_type` follows the ways in: `public` only when the Register plan uses
  the `public_visitor` entry or restricts registration to assigned contacts,
  `personal` only when it uses `personal_invitee`, `free_entry` only when the
  story selects Paid tickets or a change adds them.
- Every story change cites at least one knowledge article the skill carries,
  and its `refs` name messages of this plan. A message that waits on a story
  change has `send_at: null`, and the conversion to a draft refuses it until a
  person approves the change.

## Before you finalize the plan

Nothing checks the object after you, so check it here. Emit it when every
line below holds; fix what does not, or move it to `open_items` or
`blocked_operations` as `SKILL.md` and its references say.

- Each `verbatim` text occurs character for character in the sources and
  names `approved_in`, each `editable` item names its `edit_scope`, and
  `adopt` mode writes no text of its own.
- Each message goes through a module its phase allows. Only the
  Confirmation e-mail goes out on registration, with the timing anchor
  `on_registration`, and an audience of groups goes through E-mail campaigns.
- `send_at` comes only from a confirmed input, as `YYYY-MM-DD HH:MM`;
  otherwise it is `null` and an `open_items` entry of kind `timing` names the
  message. The Confirmation e-mail is the exception: it keeps `send_at: null`
  and needs no `timing` item, because it goes out on registration.
- Each registration call to action names its link type, and the Register
  plan has that way in: the public link only with a public entry, the
  personal link only with personal invitations.
- A message in a module the story does not select is in the `refs` of a
  story change and keeps `send_at: null` until a person approves it. A
  module the admin's MCP cannot write is in `blocked_operations`.
- Each subject is one line of at most 250 characters, and each body is plain
  text within 10 000 bytes with no HTML, placeholder, emoji, internal label
  or note to the organizer.

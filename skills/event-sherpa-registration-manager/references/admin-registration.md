# What the admin accepts

The admin's MCP writes the first registration setup of an event: three
settings and the questions of the Registration form. This page is what the
write accepts as of `registration-v1`; when a tool result says otherwise, the
tool result wins and the plan follows it.

## The tools, in order

1. `get_event_registration(event_id, culture)` reads the current settings, the
   form with its exact `q:ID` and `o:ID` references, `source_hash`,
   `editability` and `form_editability`. A readable form is not necessarily
   editable: respect `blocking_reasons`.
2. `preview_event_registration_change` takes `event_id`, `culture`, the
   exact `source_hash`, optional `archetype` and partial `settings` and/or
   `form`. It saves nothing and returns the exact proposal, its
   `proposal_hash`, the resulting configuration, company rules and warnings.
3. For private preparation within the organizer's requested scope, use
   `save_event_preparation` with the current operation id and exact proposal
   hash, without another confirmation. If the preview opens registration,
   deletes content or changes a form already visible to participants, show
   the concrete preview and effects and obtain explicit approval through a
   supported confirmation tool instead. A legacy
   `confirm_event_registration_change` call still requires real consent to
   the exact preview and `confirmed: true`; never invent that consent.
4. `get_chat_event_registration_change(operation_id)` reads the result back.
   Only `verification: verified` proves the saved state; it also maps each
   `new:` reference to its saved `q:ID` or `o:ID`.

When the direct path is not enabled, `prepare_event_registration_change` takes
the same input and returns a link where the person approves the change in the
admin. A preview expires after 30 minutes; a changed event needs a new read
and a new preview. A changed consequential preview needs new approval.

## When the write is possible

Only for an event in its initial closed state: registration deadline still
`2000-01-01 00:00:00`, hidden from the event list, timezone `Europe/Prague`,
no attendees or other non-admin members, no paid tickets, no PIN login, no
open web attendee app, a form without answers, groups or automatic assignments.
Once the deadline leaves its initial value, this write cannot change it again;
later edits go through the regular admin.

**Setting the deadline, to a future time or to no deadline, opens the
registration links at once, even when the event is hidden from the event
list.** Hidden does not mean private. Say this before the person confirms.

## Settings

| Field | Accepts |
|---|---|
| `registration_deadline` | `null` (no deadline) or an unambiguous local `YYYY-MM-DD HH:mm:ss` in `Europe/Prague`; a time inside a daylight saving change is rejected |
| `capacity` | integer 0 to 2147483647; `0` is unlimited; counts confirmed and approved attendees, not companions |
| `approval_required` | `true` or `false` |

Omitted settings stay as they are. A proposal must change something.

## Form

- `enable: true` switches the Registration form on; switching it off is not
  supported.
- Questions are partial upserts with `ref`, `type`, `label`, `description`,
  `state`, `position`, `allow_other`, `min_selections`, `max_selections` and
  `options`. A new question needs `type`, a non-empty `label` and `state`; a
  new choice question needs at least one option, and a new option needs a
  `label`. Omitted questions, options and fields stay as they are.
- Types: `text`, `singleSelect`, `multiSelect`. The type of an existing
  question cannot change.
- States: `required`, `optional`. A follow-up hidden by branching never blocks
  the submit; a shown required one does.
- `min_selections` and `max_selections` (1 to 301, or `null` to remove) only on
  `multiSelect`; minimum not above maximum, neither above the number of options
  plus Other. A required question still needs at least one choice.
- `branches` is a list of `{option, shows}`; it replaces the questions an option
  reveals. `shows: []` removes them. Self-reference, foreign references and
  cycles are rejected.
- References: existing `q:ID` and `o:ID` exactly as read, never matched by
  label; new ones `new:<token>`, unique across questions and options.
- Texts are plain text, stored escaped. After escaping (`&` counts five
  characters, `"` and `'` six, `<` and `>` four) a question label has at most
  150 characters, an option label 100 and a description 2000. Line breaks,
  other control characters and characters outside the basic plane (emoji) are
  rejected.
- The resulting form holds at most 80 questions, 300 options and 600 branch
  edges, with at most 80 questions revealed by one option.
- An existing non-empty description can be replaced but not cleared; leave it
  out to keep it.

A successful write puts the form under Event Sherpa's management, which turns
on server checks of required answers and limits at submit.

## What the write does not carry

| Wanted | Where a person does it |
|---|---|
| contact fields (required, optional, hidden) | Registration form, Contact details tab |
| information text, text after submit, button position | Registration form |
| other question types (date, number, file, country, limited capacity choice, accommodation) | Registration form, Additional questions |
| group assignment by answer, visibility of questions or options for groups | Registration form and Contacts and groups |
| deleting a question or option, changing a type | Registration form |
| privacy notice, consents beyond legitimate interest | Workspace settings, Personal data protection |
| confirmation e-mail with QR code, PDF ticket and calendar file | Confirmation e-mail and Event settings |
| invitations, reminders, campaigns | the communication skill |
| microsite buttons and texts, Attendee app | the microsite and app skill |
| tickets, payments, PIN | Tickets and Event settings |

Wording of a consent is a text, not a consent record. The write never records,
changes or collects a consent, an answer or a personal link.

## Conversion

`scripts/to_preview.py` in the skill's source converts a plan to the preview
arguments deterministically and refuses what does not fit instead of cutting
it. A client without the script applies the same mapping by hand
([the contract](registration-plan-v1.md#mapping-to-the-preview-input)): every
option with a non-empty `shows`, and every existing `o:ID` option, becomes one
`branches` entry.

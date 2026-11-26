# Reading the Event Story

Every Event Sherpa skill after Describe reads the approved Event Story the same
way and writes what it took into `story_basis`, the same shape in every
skill's output. This file is shared by all of them, word for word.

The story is where the event was composed: its archetypes (the first is the
main one), its journeys, the capabilities with their `selection`, what not to
use (`do_not_use`) and what the setup depends on (`setup_dependencies`). A
skill does not choose again what the story chose. It turns the story into the
content and settings of its own modules, and when the story no longer fits it
proposes a change in `story_changes`.

## story_basis

| Key | Meaning |
|---|---|
| `source` | `stored` for a complete saved Event Story record with its real `blueprint_id`; `excerpt` for story content without a saved record, including the story Event Designer wrote in this conversation, or for an excerpt of a saved record; `reference` when only the story ID and perhaps its archetype are known |
| `archetypes[]` | the story's `archetypes[].key` in the story's order; for a story by reference, only what the input names |
| `modules[]` | exactly eight entries in this order: `tickets`, `registration-form`, `event-microsite`, `invitation-email`, `confirmation-email`, `email-campaigns`, `on-site-check-in`, `attendee-app`; each `{module, selection}` |

`selection` is the story's own value for the capability with that key:
`recommended`, `conditional`, `declined` or `not_selected`; `absent` when the
story's capability list has no entry for the module; `unknown` for every
module when the story is given by reference. Copy the selection; never
correct it here. A selection you disagree with is a story change, not a
different value. An excerpt without archetypes gives only the archetypes the
input names.

An approved story written in this conversation still has no saved record,
even when its text is complete or pasted from another chat. Write
`story_basis.source: excerpt` and set both `story_ref.blueprint_id` and
`story_ref.revision` to `null`. Copy `story_ref.story_id` and
`story_ref.story_version` from the story's presentation. For a saved record,
copy its actual blueprint ID and revision together when supplied; never
invent either. A part of that record with its capabilities is still
`excerpt`, even when it identifies the saved record.

For example, a complete saved record with blueprint ID `bp-42` and revision
`3` gives `stored` and that ID and revision. The same approved event
description written only in chat gives `excerpt` and two nulls. A handoff
that names only the story ID gives `reference` and eight `unknown` selections.

The eight are the only modules of Happenee: Paid tickets, Registration form,
Event microsite, Invitation e-mail, Confirmation e-mail, E-mail campaigns,
On-site check-in and Attendee app (in Czech: Placené vstupenky, Registrační
formulář, Microsite události, Zvací e-mail, Potvrzovací e-mail, E-mailové
kampaně, Odbavení na místě, Účastnická aplikace). Everything else the story
lists is a content feature or an engagement feature.

## What follows from it

- A module is **selected** when its selection is `recommended` or
  `conditional`. A plan may use a selected module. A `conditional` module
  comes with the story's condition; keep it in the plan's reasons.
- A module that is `declined`, `not_selected` or `absent` is not used. When
  the event needs it after all, propose it in `story_changes` (`change:
  add`, the module's key in `module`, its product name in `subject`) and
  list the plan entries that need it in the change's `refs`; they wait until
  a person approves the change. `module` is `null` for a change to a content
  or engagement feature or a setting.
- `do_not_use` entries name capabilities the story ruled out on purpose, with
  a reason and a `reconsider_if`. Do not plan them unless that condition is
  met; then it is a story change.
- Who comes and how they get in follows from the story's facts and journeys
  (an invited list, a public event, paid entry). Each skill draws the
  consequences for its own modules and says which story fact it rests on.
- Facts about the event come only from the story, the earlier skills' outputs
  and the brief.

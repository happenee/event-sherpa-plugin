# registration_plan-v1

The output of Register. JSON Schema: `schema/registration_plan.schema.json` in
the skill folder; this page is the readable form. All keys are required; use
`null` or `[]` where a value is not known. Read
[Before you finalize the plan](#before-you-finalize-the-plan) at the end before you
emit a plan.

| Key | Meaning |
|---|---|
| `schema_version` | always `registration_plan-v1` |
| `output` | id and revision of this plan, the same shape in every Event Sherpa skill: `output_id` (assigned by whoever stores the plan, copied, `null` when not stored), `revision` (`1` for a new plan, else the previous plus 1), `supersedes_revision`, `change_id`, `bindings[]` (written only by the MCP, copied unchanged); see [plan revisions](output-revision.md) |
| `story_ref` | the approved Event Story: `story_id` and `story_version` from its `presentation`, always set; `blueprint_id` and `revision` (string or integer) when the story is stored, both `null` for a story made in the conversation |
| `story_basis` | what the plan took from the story: `source`, `archetypes[]`, the eight `modules[]` with their `selection`; the same shape in every Event Sherpa skill, see [reading the Event Story](story-basis.md) |
| `content_ref` | the Compose output the plan reads: `schema_version` (`event_content-v1`), its `story_id`, `story_version` and `mode` and the `output_id` and `revision` of its `output` header (revision `1` for an output without one); `null` when there is no Compose output |
| `language` | `cs` or `en`, same as the story |
| `mode` | `compose` (proposes) or `adopt` (takes over a finished form, writes no text) |
| `admin_archetype` | `conference`, `internal`, `networking` or `null`, see below |
| `journey[]` | exactly three entries, see below |
| `settings` | `registration_deadline`, `capacity`, `approval_required`, see below |
| `access_settings` | `registration_restriction`, `app_visibility`, `app_access`: who may register and how the event shows in the Attendee app (KB 02.04); never written, see below |
| `contact_fields[]` | `field`, `custom_label`, `state`, `reason`, `source` |
| `form` | `questions[]`, see below |
| `content_items[]` | every text, same shape as in `event_content-v1` |
| `organization_rules[]` | approved company rules applied: `knowledge_id`, `revision`, `rule`, `binding`; `[]` without organization context |
| `decisions[]` | `id`, `scope`, `reason`, `as_of_and_source`, `revisit_trigger`, `supersedes[]` |
| `story_changes[]` | proposed changes to the approved story for a person to approve: `id`, `change` (`add`, `drop`, `change`), `module` (the key of the module it adds, drops or changes, `null` for a feature or setting), `subject` (the module, feature or setting), `reason`, `knowledge_ids[]` (supporting source ids, at least one), `refs` (settings, access settings, journey entries or question refs that depend on it, `null` or `[]` when none) |
| `deferred[]` | `item`, `decided_in`, `reason`; postponed by a person, never raised again |
| `open_items[]` | `item`, `kind` (`settings`, `question`, `copy`, `journey`, `ops`), `refs` (setting names, access setting names, `admin_archetype`, journey entries or question refs it holds up, and for kind `copy` also `content_id`s of this plan's texts; `null` or `[]` when none) |
| `blocked_operations[]` | `operation` the write cannot carry, `area` (`settings`, `access_settings`, `contact_fields`, `form`, `info_text`, `consent`, `confirmation`, `groups`, `journey`, `other`), `blocked_by`, `manual_step` (where a person does it in the admin, or `null`) |

## admin_archetype

The archetype the admin uses to pick company rules for the preview. The
preview applies the rules of exactly one archetype and never merges them.
Walk `story_basis.archetypes` in order and take the first that maps:
`conference` gives `conference`, `internal_corporate` gives `internal`. When
a later archetype maps to a different value (an internal conference is
both), the first still wins, because the story lists its main archetype
first, and one `decisions` entry whose `scope` names `admin_archetype`
records the choice for the person to confirm; a person may pick the other
value instead, recorded the same way.

With no mapping archetype it is `null` and an `open_items` entry of kind
`settings` names `admin_archetype` in its `refs`: a person picks
`conference`, `internal` or `networking`, and the pick goes into
`admin_archetype` with a `decisions` entry. A plan with `null` does not
convert, because the admin would fall back to conference rules without
saying so.

## Journey entry

| Key | Meaning |
|---|---|
| `entry` | `public_visitor`, `personal_invitee` or `registered`, each exactly once |
| `status` | `used` (the event has this way in), `unused` (it does not; `registered` is never unused) or `open` (undecided, named by an open item of kind `journey`) |
| `reason` | for `unused` and `open`, the story fact, brief source or decision it rests on; may be `null` for `used` |
| `arrives_via` | how the person gets there, for example the public link of the microsite or the personal link of an invitation |
| `identity` | `anonymous` (until an e-mail is entered), `invited_contact` (carried by the personal link) or `registered_contact` |
| `next_step` | what the person sees and does next |
| `shown_on[]` | modules on the way: `tickets`, `registration-form`, `event-microsite`, `invitation-email`, `confirmation-email`, `email-campaigns`, `on-site-check-in`, `attendee-app`; only modules the story selects, or a module a story change adds with this entry in the change's `refs`; `[]` for an unused entry |
| `manual_remainder[]` | what a person sets or checks in the admin because the plan's write does not cover it |
| `verify` | how to check this path: form preview, one registration with the organizer's own account or the readiness check, never a test participant |

## Settings

Each of the three settings is `{status, value, source}`.

| `status` | Meaning |
|---|---|
| `confirmed` | stated by the organizer or the brief; written with `source`; never a value that waits on a story change |
| `open` | undecided; `value` is `null` and an `open_items` entry of kind `settings` names the field |
| `keep` | deliberately left as the event has it; `value` is `null` |

| Setting | `value` when confirmed |
|---|---|
| `registration_deadline` | local `YYYY-MM-DD HH:mm:ss` in `Europe/Prague`, or `null` for no deadline; either opens registration at once |
| `capacity` | integer, `0` for unlimited; counts confirmed and approved attendees, not companions |
| `approval_required` | `true` or `false` |

An `unused` entry keeps its keys so the plan keeps its shape; its texts
may say why it is not used, and nothing about it is checked except the
reason. At least one of `public_visitor` and `personal_invitee` is used or
open. A used `public_visitor` needs the Event microsite (the public link
opens on it) and a used `personal_invitee` needs the Invitation e-mail or
E-mail campaigns (the personal link travels in one of them), selected by the
story or added by a story change.

## Access settings

Each of the three is `{status, value, reason, kb_ref, source}`. The MCP write
sets none of them; a person sets them in Nastavení události → Nastavení
přístupů a registrace after confirming them, so every `confirmed` or
`proposal` one comes with a `blocked_operations` entry of area
`access_settings`.

| `status` | Meaning |
|---|---|
| `confirmed` | stated by the organizer or the brief, with `source` |
| `proposal` | derived from the story or the form, with `reason` and `kb_ref` (an article the skill carries, usually `kb.<lang>.02.04`) |
| `open` | matters but undecided; `value` is `null` and an open item of kind `settings` names it |
| `keep` | the admin default stays; `value` is `null` |

| Setting | Values (first is the admin default) |
|---|---|
| `registration_restriction` | `none`, `assigned_contacts` (only contacts assigned to the event, even through the public link), `allowed_domains`, `blocked_domains` (domain lists are set by customer support) |
| `app_visibility` | `assigned_contacts`, `all_contacts` (everyone in the workspace sees that the event exists; suits internal events) |
| `app_access` | `after_form`, `without_form` (a click gives access and sets Zúčastním se; collects no form data) |

A checker refuses `approval_required: true` together with Paid tickets the
story selects or a change adds (KB 02.04), and `app_access: without_form`
with any question in the form. With Paid tickets the story selects and any question in the
form it wants one `decisions` entry whose `scope` names
`ticket_registration_type` (registration with additional information on the
tickets, KB 01.04) and a `blocked_operations` entry of area `settings`;
without Paid tickets it refuses that decision, because the setting exists
only on tickets.

## Contact field

| Key | Meaning |
|---|---|
| `field` | `email`, `first_name`, `last_name`, `phone`, `job_title`, `company`, `company_id`, `country`, `twitter`, `linkedin`, or `custom` |
| `custom_label` | the workspace field's name for `custom`, else `null` |
| `state` | `required`, `optional` or `hidden`; `email` is always `required` |
| `reason` | why a field is required, `null` when the brief only states it |
| `source` | brief, answer, decision id or `proposal` |

## Question

| Key | Meaning |
|---|---|
| `ref` | `new:<token>` for a question the event does not have yet (letters, digits, `_` and `-`, first a letter or digit, at most 64), or the exact `q:ID` read from the event; stable across revisions |
| `code` | the organizer's own label, for example `Q1` or `AI2`, else `null` |
| `type` | `text`, `singleSelect`, `multiSelect`, or `null` when not confirmed; an existing `q:ID` keeps the type it was read with |
| `label_ref`, `description_ref` | `content_id`s of the question's texts; `description_ref` may be `null` |
| `state` | `required`, `optional`, or `null` when not confirmed |
| `allow_other` | `true` adds the admin's Other choice |
| `min_selections`, `max_selections` | `multiSelect` only, integer or `null` (no limit); for an existing question, the limits it should have after the write, so copy the read ones unless they change |
| `options[]` | `ref` (`new:<token>` or `o:ID`), `label_ref`, `shows[]` (question refs this option reveals) |
| `used_for[]` | `use` (`programme`, `segment`, `branch`, `follow_up`, `ops`), `blocks` (Compose block ids, required for `programme`), `note`; never empty |
| `source` | where the question comes from: brief, answer, decision id or `proposal` |

The order of `questions` is the order of the form, and the order of `options`
the order of the choices. New references are unique across questions and
options together.

## Content item

The same shape as in `event_content-v1`: `content_id`, `surface`, `slot`,
`text`, `authority` (`verbatim`, `proposal`, `editable`), `edit_scope`,
`source`, `depends_on`, `approved_in`. Register uses surface `registration` with slots such
as `question_label`, `question_description`, `option_label`, `intro`,
`info_text` and `after_submit`. An item that already exists in the Compose
output keeps its `content_id`, `text` and `authority`.

## Mapping to the preview input

| registration_plan-v1 | `preview_event_registration_change` |
|---|---|
| `settings.*` with `status: confirmed` | `settings.<name>`; other statuses are left out |
| non-empty `form.questions` | `form.enable: true` and `form.questions` |
| `ref`, `type`, `state`, `allow_other` | the same keys |
| text of `label_ref`, `description_ref` | `label`, `description` |
| position in the list | `position`: 0, 10, 20 and so on |
| `min_selections`, `max_selections` | the same keys; a new question gets them only when not `null`, an existing `multiSelect` question always gets both, so `null` removes a limit the event has |
| `options[].ref`, text of `label_ref`, position | `options[]` with `ref`, `label`, `position` |
| `options[].shows` | `form.branches[]` as `{option, shows}` |
| `admin_archetype` | `archetype`; a plan with `null` does not convert |
| `access_settings` other than `keep` | not written; shown to the person with their status and article |
| `contact_fields`, `blocked_operations` | not written; shown to the person as manual steps |
| `story_changes` | not written; shown to the person and, once approved, taken to Describe |

`event_id`, `culture` and `source_hash` come from `get_event_registration`
and are added by the client. A plan with an unconfirmed type or state, an
unwritten text or a choice question without options does not convert; the
missing items are its open items.

## Before you finalize the plan

Nothing checks the object after you, so check it here. Emit it when every
line below holds; fix what does not, or move it to `open_items` or
`blocked_operations` as `SKILL.md` and its references say.

- Each `verbatim` text occurs character for character in the sources and
  names `approved_in`, each `editable` item names its `edit_scope`, and
  `adopt` mode writes no text of its own.
- A text the Compose output already holds keeps its `content_id`, text and
  authority.
- `journey` holds exactly one `public_visitor`, one `personal_invitee` and
  one `registered` entry, and `registered` is never `unused`. Every `unused`
  or `open` entry gives its `reason`, and an `open` one has an `open_items`
  entry of kind `journey`. A `used` or `open` entry's `shown_on` names at
  least one module and an `unused` one has `shown_on: []`; it names only
  modules the story selects or a story change adds.
- Each `confirmed` setting carries its `source`, and each `open` one has
  `value: null` and an `open_items` entry of kind `settings`. The deadline is
  set only when the organizer said both when registration opens and until
  when.
- `contact_fields` holds `email` as `required` and a reason for every other
  `required` field. A non-empty list comes with a `blocked_operations` entry
  of area `contact_fields`, and any `access_settings` with one of area
  `access_settings`.
- Each question says in `used_for` what its answer serves. A choice question
  has its options or an `open_items` entry of kind `copy`. Selection limits
  stand only on `multiSelect`, within its number of options. Branching goes
  two levels deep at most, and no option shows its own question.
- With Paid tickets, `approval_required` is never confirmed as `true`, and a
  form with questions has the `ticket_registration_type` decision with its
  `blocked_operations` entry of area `settings`.
- `admin_archetype` is the first of the story's archetypes that maps, or
  `null` with an `open_items` entry that asks a person to pick.

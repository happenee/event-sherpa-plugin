# microsite_app_plan-v1

The output of Web Designer and of App Designer: one contract, two
plans. Web Designer writes `scope: microsite` and leaves `app` null; App
Designer writes `scope: app` and leaves `microsite` null. JSON Schema:
`schema/microsite_app_plan.schema.json` in the skill source; this page is the
readable form. All keys are required; use `null` or `[]` where a value is not
known. Read the part for your scope and [Before you finalize the plan](#before-you-finalize-the-plan)
before you emit a plan.

| Key | Meaning |
|---|---|
| `schema_version` | always `microsite_app_plan-v1` |
| `scope` | `microsite` (Web Designer) or `app` (App Designer); `both` only marks a stored plan written before the two skills split, never write it |
| `output` | id and revision of this plan, the same shape in every Event Sherpa skill: `output_id` (assigned by whoever stores the plan, copied, `null` when not stored), `revision` (`1` for a new plan, else the previous plus 1), `supersedes_revision`, `change_id`, `bindings[]` (written only by the MCP, copied unchanged); see [plan revisions](output-revision.md) |
| `story_ref` | the approved Event Story: `story_id` and `story_version` from its `presentation`, always set; `blueprint_id` and `revision` (string or integer) when the story is stored, both `null` for a story made in the conversation |
| `story_basis` | what the plan took from the story, the same shape in every skill: `source`, `archetypes[]`, the eight `modules[]` with `selection`; see [reading the Event Story](story-basis.md) |
| `content_ref` | the Compose output this plan reads: `schema_version` (`event_content-v1`), `story_id`, `story_version` (its story must be the plan's story) and `mode` and the `output_id` and `revision` of its `output` header (revision `1` for an output without one); `null` without a Compose output, and then nothing refers to Compose blocks or texts |
| `registration_ref` | the Register output this plan reads, in the same shape: `schema_version` (`registration_plan-v1`), `story_id`, `story_version`, `mode`; `null` without a Register output |
| `language` | `cs` or `en`, same as the story |
| `mode` | `compose` (proposes) or `adopt` (takes over an approved order, writes no copy) |
| `organization_context` | `status` (`used`, `unavailable`, `not_requested`) and `records[]`: `knowledge_id`, `revision`, `content_hash`, `category` (`preference`, `rule`, `lesson`), `applied_to` |
| `feature_content[]` | one instance per content or engagement feature this plan uses, see below; a microsite plan holds content features only |
| `microsite` | `null` in an app plan; else `use` (`full`, `registration_only`, `not_used`), `sections[]` from top to bottom, `thank_you_ref` (a `content_id` or `null`) |
| `app` | `null` in a microsite plan; else `use` (`used`, `not_used`), `entry_points[]` (`route`: `magic_link`, `pin`, `event_qr`, `web_app_link`, `store_download`; `where`), `features[]` |
| `story_changes[]` | proposed changes to the story, see below |
| `content_items[]` | every text, see below |
| `decisions[]` | `id`, `scope` (one string, never a list; a decision about several keys is one entry per key), `reason`, `as_of_and_source`, `revisit_trigger`, `supersedes[]` (ids of earlier decisions, or the brief approval a correction replaces, such as `brief: Microsite: schválené pořadí`) |
| `deferred[]` | `item`, `decided_in`, `reason`; postponed by a person, never raised again |
| `open_items[]` | `item`, `kind` (`copy`, `fact`, `asset`, `config`, `ops`, `verify`), `refs` (section, instance, app entry, content item, manual step or story change ids of this plan it holds up, or the Compose `block_id`, `content_id`, `person_id` or `partner_id` it waits on; `null` or `[]` when none) |
| `blocked_operations[]` | `operation` the MCP cannot write, `area` (`microsite`, `app`, `feature_content`, `engagement`, `visibility`, `other`), `blocked_by`, `manual_step` (a `step_id` or `null`) |
| `manual_steps[]` | `step_id`, `screen` (the admin screen as the knowledge base names it), `action`, `refs[]`, `kb_ref` (a knowledge id the skill carries, or `null`) |
| `handoffs[]` | `target` (`preview_event_creation`), `arguments` (only `module_types`), `covers[]` (instance ids), `note` |

## Feature instance

One feature that shows in both channels is one instance. When the
conversation already has the other plan of the same story (the microsite plan
when you plan the app, or the reverse), reuse its `instance_id`, `name_ref`
and `fields` for the same feature and its `content_items` with the same
`content_id`, text and authority; never make a second instance of a feature
the other plan already holds.

| Key | Meaning |
|---|---|
| `instance_id` | stable across revisions, for example `fc.venue` or `fc.custom.practical` |
| `feature_key` | from [the feature vocabulary](features.md) |
| `kind` | `content` or `engagement`, as the vocabulary says |
| `name_ref` | `content_id` of the name the instance is renamed to, or `null` for the default name; that content item has `slot: name` |
| `fields[]` | `field` (for example `venue.address`) and `content_ref` (a `content_id`, whose text is `null` while the value is missing); only the fields [the feature vocabulary](features.md) lists, so Venue, Contact, Custom content and Registration information have fields and every other feature has none (its admin options go to `settings`) |
| `settings[]` | `setting` (admin label), `value`, `source` |
| `visibility` | `audience` (`all` or `groups`) and `groups[]` exactly as the input names them |
| `compose_refs[]` | plain id strings, one per entry: Compose `block_id`, `content_id`, `person_id` (Speakers) or `partner_id` (Sponsors, Exhibitors) that fill the instance, for example `["b01", "b02"]`, never objects; a person or partner only when `confirmed` |
| `source` | brief, answer, decision id or `proposal` |

For example, an app feature with `"name_ref": "ci.name.questions"` points to
the content item with `"content_id": "ci.name.questions"` and
`"slot": "name"`. The actual participant-facing label goes in that item's
`text`; `slot` is the structural key.

## Microsite section

| Key | Meaning |
|---|---|
| `section_id` | stable across revisions, for example `ms03`; array order is the order on the microsite home page |
| `name` | internal name, as the brief calls the section; not public copy |
| `carrier` | `header_image`, `intro_text`, `feature` or `registration_button` |
| `instance_ref` | the instance for `feature`, else `null`; only content features |
| `text_refs[]` | `content_id`s of an intro text part; empty for the other carriers |
| `display` | `preview` or `all` for an Agenda or Speakers tab, else `null` |
| `registration_position` | `top`, `middle`, `bottom` or `auto` for `registration_button`, else `null` |
| `settings[]` | other settings of the tab, as in an instance |
| `reason`, `source` | why the section is there and where it comes from |

Order rules: a header image is first; intro text parts follow it without a
feature tab between them; a registration button at `bottom` is last; there is
at most one header image and one registration button, and an instance is
used by at most one section.

## App entry

| Key | Meaning |
|---|---|
| `entry_id` | stable across revisions, for example `app03` |
| `feature_key` | from the vocabulary, including the session level keys |
| `placement` | `home` (a tile, in array order) or `session` (on the detail of `blocks`) |
| `instance_ref` | the instance for `home`, `null` for `session` |
| `tile` | `text` or `image` for `home`, `null` for `session` |
| `blocks[]` | Compose `block_id`s the entry serves |
| `engagement_level` | the Compose level (`listen`, `react`, `share`) the entry carries, or `null` |
| `reason`, `kb_refs[]`, `source` | why, which articles support it, where it comes from |
| `story_status` | `selected`, `pending_change` (listed in a change's `refs`), `unverified` or `not_tracked` |

## Story change

Same shape in every Sherpa skill.

| Key | Meaning |
|---|---|
| `id` | stable, for example `sc01` |
| `change` | `add`, `drop` or `change` |
| `module` | the key of the module it adds, drops or changes; `null` for a feature or setting |
| `subject` | the module, feature or setting of the story, in product terms |
| `reason` | why the event needs it and what changes for the attendee |
| `knowledge_ids[]` | at least one knowledge id the skill carries |
| `refs` | entries, instances or sections of this plan that depend on it, or `null` |

A change is a proposal for a person. Entries that depend on it get no manual
step and no handoff until it is approved and Describe writes the next story
version.

## Content item

| Key | Meaning |
|---|---|
| `content_id` | stable across revisions; equal to the Compose `content_id` when the text comes from Compose |
| `surface` | `microsite`, `app` or `feature` (the content of a feature, wherever it shows); `concept`, `programme`, `registration`, `email` for items kept from Compose |
| `slot` | place on the surface, for example `intro` or `venue.address`; a feature's new name (the item a `name_ref` points to) is always `name` |
| `text` | the exact text, or `null` while it is missing |
| `authority` | `verbatim`, `proposal` or `editable` |
| `edit_scope` | for `editable` only, else `null` |
| `source` | where the text comes from; `proposal` for new text |
| `depends_on` | what the text states: `fact:<key>` (a story fact), `setting:<key>` (a Register setting), or the id of an item of this plan or an earlier plan, alone or with a field (`b03.start`, `p02`); `[]` when none; see [plan revisions](output-revision.md) |
| `approved_in` | decision id or brief source that approved this item alone; `null` for proposals |

## Before you finalize the plan

Nothing checks the object after you, so check it here. Emit it when every
line below holds; fix what does not, or move it to `open_items` or
`blocked_operations` as the skill's rules say.

In every plan:

- `scope` is your skill's (`microsite` or `app`) and the other part is
  `null`.
- Each `verbatim` text occurs character for character in the sources and
  names `approved_in`, each `editable` item names its `edit_scope`, and
  `adopt` mode writes no text of its own.
- The module the plan designs is one the story selects or a story change
  adds; a module the story recommends that the plan leaves `not_used` has a
  `decisions` entry with its key in `scope`.
- Every instance is used by a section, an entry or the handoff of this
  plan, a feature that can be added once per event appears once, and an
  instance the other plan of the same story already holds keeps its id,
  fields and texts.
- Facts (dates, places, names, groups) come verbatim from the input or stay
  `null`, and a Compose person or partner shows only once confirmed.
- The handoff carries only `module_types` from locality, contact, sessions
  and speakers.

In a microsite plan (`scope: microsite`):

- The microsite opens with the header image, keeps the intro text above the
  tabs and places the registration button where `registration_position`
  says; a microsite used only for registration has no feature tabs.
- Only content features: no engagement instance, no engagement tab.

In an app plan (`scope: app`):

- In `compose` mode with a Compose output, every interactive app feature
  serves a block or an engagement level of it; without a Compose output
  (`content_ref: null`) no entry names a block or a level. Engagement on a
  session names its blocks.
- Every entry has the `story_status` its feature has in the story, and an
  entry that waits on a story change has no manual step and no handoff.

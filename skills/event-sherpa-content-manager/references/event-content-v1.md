# event_content-v1

The output of Compose. JSON Schema: `schema/event_content.schema.json` in the
skill source; this page is the readable form. All keys are required; use
`null` or `[]` where a value is not known. Read
[Before you finalize the plan](#before-you-finalize-the-plan) at the end before you
emit a plan.

| Key | Meaning |
|---|---|
| `schema_version` | always `event_content-v1` |
| `output` | id and revision of this plan, the same shape in every Event Sherpa skill: `output_id` (assigned by whoever stores the plan, copied, `null` when not stored), `revision` (`1` for a new plan, else the previous plus 1), `supersedes_revision`, `change_id`, `bindings[]` (written only by the MCP, copied unchanged); see [plan revisions](output-revision.md) |
| `story_ref` | the approved Event Story this builds on: `story_id` and `story_version` from its `presentation`, always set; `blueprint_id` and `revision` (string or integer) when the story is stored, both `null` for a story made in the conversation |
| `story_basis` | what Compose took from the story, the same shape in every skill: `source`, `archetypes[]`, the eight `modules[]` with `selection`; see [reading the Event Story](story-basis.md) |
| `language` | `cs` or `en`, same as the story |
| `mode` | `compose` (proposes) or `adopt` (takes over a finished brief, writes no text) |
| `concept` | `statement_ref` (a `content_id`, or `null` in adopt mode without a concept sentence) and `variants[]`, at most two, each `label`, `statement`, `consequence` |
| `engagement_levels[]` | `level` (`listen`, `react`, `share`), `asks_of_attendee`, `used_in` (block ids) |
| `programme[]` | blocks, see below |
| `people[]` | speakers and moderators, see below |
| `partners[]` | sponsors and exhibitors, see below |
| `content_items[]` | every text, see below |
| `decisions[]` | `id`, `scope`, `reason`, `as_of_and_source`, `revisit_trigger`, `supersedes[]` (same shape as in the Event Story) |
| `deferred[]` | `item`, `decided_in` (decision id or brief source), `reason`; postponed by a person, never raised again |
| `open_items[]` | `item`, `kind` (`copy`, `capacity`, `speaker`, `partner`, `ops`, `content`), `blocks` (block ids it holds up, `null` or `[]` when none), `refs` (person and partner ids it concerns, `[]` when none) |
| `blocked_operations[]` | `operation` that cannot go into program-v1 yet, `blocked_by`, and the `blocks` and `refs` it concerns (`[]` when none); a person listed in `refs` is not written |
| `story_changes[]` | proposed changes to the approved story for a person to approve, the same shape in every Event Sherpa skill: `id`, `change` (`add`, `drop`, `change`), `module` (the key of the module it adds, drops or changes, `null` for a feature or setting), `subject` (the module, feature or setting in product terms), `reason`, `knowledge_ids[]` (at least one, only articles the skill carries), `refs` (person, partner or block ids that depend on it, `null` or `[]` when none; they stay in `blocked_operations` while the change waits) |

## Agenda block

| Key | Meaning |
|---|---|
| `block_id` | stable across revisions, for example `b01` |
| `kind` | `arrival`, `session`, `break`, `networking` |
| `admin_type` | the admin session type: `base_kind` (`keynote` for `session`; `break` for `break`, `arrival` and `networking`, whose title says what happens; `keynote` for a break, arrival or networking that carries an approved description from the brief or whose type a person chose, recorded in `decisions` with the `block_id` in its `scope`; the block keeps its `kind`. A speakerless block attendees should read about is a `session`) and `audience` (`null` for everyone, else the group the brief restricts the block to) |
| `start`, `end` | event-local `HH:MM`, only when confirmed, else `null` |
| `duration_min` | integer minutes, or `null` when `start` and `end` are given; a working duration the input does not fix is recorded in `decisions` as an assumption |
| `purpose` | what the attendee gets from the block (internal, not public copy) |
| `title_ref`, `description_ref` | `content_id`s of the block's texts; `description_ref` may be `null`. A block whose `base_kind` is `break` carries a description only as approved `verbatim` text, because a break shows attendees no detail and a person decides its type |
| `speakers[]` | `person_id` (from `people[]`), `role` (the person's role, never a name) and `assignment` (`s` speaker, `m` moderator) in speaking order; a person at most once per block; empty for unassigned blocks |
| `uses_registration[]` | which registration answers shape the block, empty when none; only when the story selects the Registration form or a story change adds it |
| `source` | where the block comes from: brief, answer, decision id or `proposal` |

## Person

| Key | Meaning |
|---|---|
| `person_id` | stable across revisions, for example `p01`, in order of first appearance |
| `role` | readable role, never a name; the same text in every block that links the person |
| `status` | `confirmed` (the input confirms they speak), `recommended` (recommended, not confirmed), `missing` (needed, nobody lined up yet) |
| `profile` | `name_ref`, `surname_ref`, `company_ref`, `position_ref`, `description_ref`: `content_id`s on surface `speakers`, each `null` when the input does not give the fact; texts only `verbatim`, or an open slot with `text: null` |
| `source` | brief turn, answer, decision id or `proposal` |

## Partner

| Key | Meaning |
|---|---|
| `partner_id` | stable across revisions, for example `sp01` for a sponsor, `ex01` for an exhibitor |
| `kind` | `sponsor` or `exhibitor` |
| `status` | `confirmed`, `recommended`, `missing` as for a person |
| `role` | level or category in the input's words, `null` when it gives none; never invented |
| `place` | an exhibitor's stand or place in the input's words, else `null` |
| `name_ref` | `content_id` of the name (surface `partners`, `verbatim`), `null` when no name was supplied |
| `description_ref` | `content_id` of the profile description, or `null`; a partner without a name has none |
| `blocks` | block ids where the partner appears (its presentation, its logo on a session), `[]` when none |
| `reason` | for `recommended`, why the event needs it; else `null` |
| `source` | where the partner comes from |

## Content item

| Key | Meaning |
|---|---|
| `content_id` | stable across revisions, for example `prog.b02.title` |
| `surface` | `concept`, `programme`, `speakers`, `partners`, `microsite`, `registration`, `email`, `app` |
| `slot` | place on the surface, for example `title`, `description`, `intro`, `subject` |
| `text` | the exact text, or `null` for an open slot that may not be written yet |
| `authority` | `verbatim` (use exactly, character for character), `proposal` (Compose's suggestion), `editable` (may be changed within `edit_scope`) |
| `edit_scope` | for `editable` only, what may change; else `null` |
| `source` | brief turn, answer or decision id the text comes from; `proposal` for new text |
| `depends_on` | what the text states: `fact:<key>` (a story fact), `setting:<key>` (a Register setting), or the id of an item of this plan or an earlier plan, alone or with a field (`b03.start`, `p02`); `[]` when none; see [plan revisions](output-revision.md) |
| `approved_in` | decision id or brief source that approved this item alone; `null` for proposals |

## Mapping to program-v1

| event_content-v1 | program-v1 session |
|---|---|
| text of `title_ref` | `title` |
| text of `description_ref` | `description` |
| `start`, `end` on the event date | `start_at`, `end_at` |
| `admin_type` | a returned `session_type_id` whose `basic_type` equals `base_kind`; for `arrival` and `networking`, and whenever several types fit, a person picks the one whose visibility matches `audience` |
| `speakers[]` | the session's ordered `speakers` list, `{"ref", "role": assignment}`; written only when every person in it is written |

| event_content-v1 | program-v1 speaker |
|---|---|
| person `confirmed` whose `name_ref` or `surname_ref` has text and whom no `blocked_operations` entry lists | a new profile `{"ref": "new:<person_id>", "fields": {...}}`; `name`, `surname`, `company`, `position`, `description` from the profile texts; a `null` ref leaves the field empty, and a new profile always carries both `name` and `surname`; a person may pick an existing `speaker:ID` instead |
| person `confirmed` without a name, or listed in `blocked_operations` | nothing until a person picks an existing profile, supplies the name or approves the story change it waits on |
| person `recommended` or `missing` | nothing |
| `partners[]` | nothing; no tool writes sponsors or exhibitors, the manual step is in `blocked_operations` |
| `story_changes[]` | nothing; shown to the person and, once approved, taken to Describe |

program-v1 accepts at most 20 speaker changes and 40 sessions per proposal;
Content Manager using the server program contract splits larger work, Compose never shortens it.

A block without confirmed times, or with speakers who are not ready, is still
a valid Compose block; the missing step is listed in `blocked_operations`.

## Before you finalize the plan

Nothing checks the object after you, so check it here. Emit it when every
line below holds; fix what does not, or move it to `open_items` or
`blocked_operations` as `SKILL.md` and its references say.

- Each `verbatim` text occurs character for character in the sources and
  names `approved_in`, each `editable` item names its `edit_scope`, and
  `adopt` mode writes no text of its own.
- Each block has confirmed `start` and `end` or a `duration_min`, and an
  `admin_type` that matches its `kind` as the session type table in
  [the handoff](handoff.md) says; a
  break, arrival or networking block in `compose` mode has no description.
- Each reference (a block's `title_ref` and `description_ref`, a profile's
  texts, a block's speakers, an engagement level's `used_in`) points at a
  `content_id`, `person_id` or `block_id` in the object, and each id appears
  once.
- A person who is `recommended` or has no name is in `open_items`, and the
  assignments of every block they speak in are in `blocked_operations`.
  Every partner is in `blocked_operations`, because no tool writes partners.
- Each `story_changes` entry cites at least one article from `knowledge/`,
  and everything in its `refs` waits in `blocked_operations`.
- Each text reads well for attendees as it stands: no internal label, no
  note to the organizer and no dash as a mid-sentence pause, a block title
  within 255 characters and a description within 8 000.

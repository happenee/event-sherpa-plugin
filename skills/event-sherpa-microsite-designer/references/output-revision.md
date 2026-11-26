# Plan revisions and revise mode

Every Event Sherpa skill after Describe writes the same `output` header into
its plan, marks in `depends_on[]` what each text states, and can change an
existing plan in revise mode. This file is shared by all of them, word for
word.

## The output header

| Key | Meaning |
|---|---|
| `output_id` | id of the stored plan; whoever stores the plan assigns it. Copy it from the previous revision; `null` for a new plan or a plan that is not stored. Never invent one |
| `revision` | `1` for a new plan, else the previous plan's `revision` plus 1 |
| `supersedes_revision` | the revision this one replaces; `null` for revision 1 |
| `change_id` | the change that made this revision; `null` for revision 1 |
| `bindings[]` | which items of the plan are saved in the event (`ref`, `saved_ref`, `operation_id`, `verified_at`). Only the MCP writes them after a verified write. Copy them unchanged; a new plan has `[]` |

A whole plan written after a correction is the next revision: `revision`
plus 1, `supersedes_revision` the previous revision, a `change_id` (the one
the caller gave, else `chg-` with the new revision number, for example
`chg-2`), `output_id` and `bindings` copied.

`content_ref` and `registration_ref` also carry the `output_id` and the
`revision` of the output they name, copied from its `output` header. An
output without a header counts as revision 1 with `output_id: null`. A plan
whose reference names an older revision than the current one is stale.

## depends_on

Every item in `content_items` has `depends_on[]`: what the text states, so
that a later change finds it without a model. List an entry for each of:

- `fact:<key>` when the text states a fact of the story: the `key` of the
  story's confirmed fact or unknown (`fact:venue`, `fact:event_date`);
- `setting:<key>` when it states a Register setting
  (`setting:registration_deadline`, `setting:capacity`);
- the id of an item of this plan or of an earlier plan you read, when the
  text states something about it: a block (`b03`, or `b03.start` when the
  text gives only its start), a person (`p02`), a partner (`sp01`), a
  registration question, a message, a feature instance or a section. Add the
  field after a dot when the text uses only that field.

Leave it empty (`[]`) when the text states none of these. A text never
depends on itself. A block's own title and description need no entry for
their block; they list only what else they state (a person by name, the
time of another block). A text taken over from Compose keeps its
`content_id` and needs no entry for it.

## Revise mode

Use it only when the request asks for a revision (`output_revision-v1`) of a
plan of this skill. Otherwise a correction produces the whole plan as the
skill's own rules say.

The input holds the current plan whole with its `output` header, the change
(the organizer's words and, when it came from a tool or another skill, the
items it concerns), the story and the earlier plans of the chain, and
perhaps the current state of the event.

Emit exactly one `output_revision-v1` object (`schema/output_revision.schema.json`),
never the whole plan:

- `skill`: this skill's id (`compose`, `register`, `communicate`,
  `microsite-app`, `app`).
- `target`: `output_id` and `revision` of the current plan. When the input
  holds two revisions of the plan (one from the conversation, a newer stored
  one), target the newest and build on it; never undo a change it made.
- `change`: `change_id` as the caller gave it, else `chg-` with the new
  revision number; `request` in the organizer's words (or the impact that
  started it); `source` the turn, tool result or skill it came from.
- `ops`: the operations that make the next revision. Change only what the
  change needs. Every other item keeps its id, text and authority.
- `conflicts`: what the change collides with, for a person to decide.
- `impacts`: items in other plans that the change touches. Mark them; never
  change another plan. `output` names the plan contract and `ref` the item in
  it. Web Designer and App Designer share `microsite_app_plan-v1` and can
  reuse the same ids, so an impact on that contract also names `scope`:
  `microsite` for the Web Designer plan, `app` for the App Designer plan.
  When the same item is in both plans, mark it twice, once per scope. An
  impact on `microsite_app_plan-v1` without `scope` names no plan and is not
  applied while both plans are in the chain. Use `null` for the other plans.

Every key is required; use `null` or `[]` where a value does not apply:

```json
{
  "schema_version": "output_revision-v1",
  "skill": "compose",
  "target": {"output_id": null, "revision": 1},
  "change": {"change_id": "chg-2", "request": "…", "source": "…"},
  "ops": [
    {"op": "set", "item": "programme/b03", "fields": {"duration_min": 45}, "value": null, "after": null}
  ],
  "conflicts": [
    {"conflict_id": "k1", "refs": ["b03", "b04"], "reason": "…", "options": ["…", "…"], "held_ops": []}
  ],
  "impacts": [
    {"output": "communication_plan-v1", "scope": null, "ref": "m02.body", "kind": "fact", "action": "check", "via": "…", "reason": "…"},
    {"output": "microsite_app_plan-v1", "scope": "app", "ref": "fc.agenda", "kind": "structure", "action": "check", "via": "…", "reason": "…"}
  ]
}
```

### Operations

| `op` | `item` | Uses | Effect |
|---|---|---|---|
| `set` | `collection/id`, or a section's dotted path | `fields` | each named field gets its whole new value; other fields stay |
| `add` | `collection/new-id` | `value`, `after` | adds the whole item; `after` is the id it follows, `null` appends it |
| `remove` | `collection/id` | | removes the item |
| `move` | `collection/id` | `after` | moves the item after that id, `null` to the start |
| `replace` | a section's dotted path | `value` | replaces a section that has no ids (`open_items`, `blocked_operations`, `deferred`) as a whole; never a collection addressed by id |

Unused keys are `null`. Collections addressed by id are the skill's lists of
blocks, people, partners, texts (`content_items/<content_id>`), questions,
messages, feature instances, sections, app entries, `decisions` and
`story_changes` (`decisions/<id>`). A nested list path uses dots
(`form.questions/q:12`, `microsite.sections/ms03`, `app.features/app02`).

- A field's new value is whole: a block's `speakers` is the whole list in
  speaking order, not the one person who changed.
- An item the change adds gets an id the plan has never used. An id never
  changes.
- Never touch `schema_version`, `output`, `story_ref`, `story_basis`,
  `language`, `mode`, `content_ref` or `registration_ref`.
- A `verbatim` text changes only to the organizer's own words in the change.
  A text you rewrite is a `proposal`.
- When the skill's rules record a correction as a decision, add it with
  `add decisions/<id>`. Lists without ids (open items, blocked operations,
  deferred items) change with `replace` and their whole new content.
- A change that alters how the event is composed (a module added or dropped)
  is a story change, added with `add story_changes/<id>`, not a revision of
  that module.

### Conflicts

When the change collides with the plan (two blocks at once in one room, one
person in two places, a block past the end of the day), do not resolve it
silently and do not move anything else. Put the operations that cause the
collision in the conflict's `held_ops`, name the colliding items in `refs`,
say why in `reason` and give at least two `options` (for example "move b04",
"shorten b03", "keep both and decide later"). Held operations wait until a
person picks an option; everything that does not collide still goes into
`ops`.

### Impacts

Each impact names the plan by its `schema_version` in `output`
(`event_content-v1`, `registration_plan-v1`, `communication_plan-v1`,
`microsite_app_plan-v1`), the touched item by its bare id in `ref` (`m02.body`,
`fc.agenda`, `app03`, not a path), says in `via` what links it to the change
and in `reason` what the change does to it.

`tools/apply_revision.py` finds by itself what `depends_on`, the feature
instances' `compose_refs`, the app entries' `blocks`, the questions'
`used_for` and texts taken over by `content_id` say. Add only what the data
does not show, with `action: check` (for example a text that speaks of "the
morning agenda"), and `action: none` with a reason for an item the change
touches that needs no change. `kind` is `fact` when the item states a time,
place or person, `text` when it takes over a changed text, `structure` when
a section, entry or question carries a changed block.

## What happens next

`tools/apply_revision.py` composes the next revision of the plan from the
revision. It refuses a revision whose `target` is not the latest revision
(a colleague saved a newer one: read it, show the difference and revise
that), applies `ops`, sets the header, runs the skill's checks and the chain
check, and lists the impacts. Each plan with an `update` impact can then be
revised in turn, with the impact as its change.

# Later changes

Read this when the Event Story no longer fits the event, or when the person corrects or changes something after the plan exists.

## When the story no longer fits

The approved Event Story is the starting point, not a fence. The event may
have moved on since the story was approved. When the registration shows that
the event needs a module, a feature or a setting the story does not have (for
example approval of each registration for a closed audience, or the entry to
the Attendee app in the Confirmation e-mail), or that something in the story
no longer makes sense, propose it in `story_changes`: whether to add, drop or
change it, why, and the knowledge base articles that support it, by source id.

Keep working while a change waits. The rest of the plan follows the story as
approved, and a plan item that needs the change stays a `proposal` or an
`open` setting, listed in the change's `refs`, until a person approves it.
Approved changes go into the next story version through Describe; Register
never applies one silently and never records one in `decisions`.

## Corrections and later changes

When a correction arrives after an existing `registration_plan-v1`:

- Record it in `decisions` with `supersedes` pointing at the assumption or
  decision it replaces.
- Change only the questions, fields, settings and items the correction names.
  Every other question keeps its `ref`, type, state, options and texts.
- An informed choice (for example a longer form kept on purpose) is a
  decision. Do not question it again, do not offer a shorter form and do not
  drop or merge questions to shorten it.
- When the correction says the form has questions the plan does not hold yet,
  do not write them; list what is missing in `open_items` of kind `copy`.
- A removed question disappears; do not bring it back later.
- The corrected plan is the next revision of the plan: set its `output`
  header as [plan revisions](output-revision.md) says.

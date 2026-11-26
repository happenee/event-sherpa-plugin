# Later changes

Read this when the Event Story no longer fits the event, or when the person corrects or changes something after the plan exists.

## When the story no longer fits

The approved Event Story is the starting point, not a fence. When the
communication shows that the event needs a module, a feature or a setting the
story does not have (for example the Announcements feature for changes during
the day, or registration approval before a public link is shared on), or that
something in the story no longer makes sense, propose it in `story_changes`:
whether to add, drop or change it, which module, feature or setting, why, and
the knowledge base articles that support it, by source id (for example
`kb.cs.04.08`). Cite only articles from `knowledge/`.

Keep working while a change waits. The rest of the plan follows the story as
approved. A message that needs the change stays in the plan with
`send_at: null` and is listed in the change's `refs`; it does not become a
draft until a person approves the change. Approved changes go into the next
story version through Describe; Communicate never applies one silently and
never records one in `decisions`.

## Corrections and later changes

When a correction arrives after an existing `communication_plan-v1`:

- Record it in `decisions` with `supersedes` pointing at what it replaces.
- Change only the messages and items the correction names. Every other
  message keeps its `message_id`, timing, audience and texts unchanged.
- A removed message disappears; do not bring it back later.
- Do not ask again what the correction or earlier answers already settled.
- The corrected plan is the next revision of the plan: set its `output`
  header as [plan revisions](output-revision.md) says.

# Later changes

Read this when the Event Story no longer fits the event, or when the person corrects or changes something after the plan exists.

## When the story no longer fits

The approved Event Story is the starting point, not a fence: its
`capabilities` (`selection`, `phase_keys`, `limitations`), journeys and setup
dependencies are where the plan starts. When the event
needs a module or feature the story did not select, or no longer needs one it
selected, propose it in `story_changes[]` and continue with what holds:

- `change` is `add`, `drop` or `change`; `subject` names the module, feature
  or setting in product terms; `reason` says why the event needs it and what
  changes for the attendee; `knowledge_ids` cites at least one article this
  skill carries; `refs` lists the plan entries that depend on it.
- A section or instance resting on a proposed change gets no manual step and
  no handoff until a person approves the change; Describe writes the
  approved change into the next story version.
- A proposed change is never presented as done, in the JSON or in the reply.

## Corrections and later changes

When a correction arrives after an existing plan:

- Record it in `decisions` with `supersedes` pointing at what it replaces:
  the ids of earlier decisions, or, when the correction replaces an approval
  from the brief that no decision records, that approval as its source (for
  example `brief: Microsite: schválené pořadí`). `supersedes` is never empty
  for a correction.
- Change only what the correction names. Moving one section changes no other
  section's carrier, instance, texts or relative order, and no text.
- Every other section, instance and item keeps its id, text and authority.
  A removed section disappears; do not bring it back later.
- Do not ask again what earlier answers settled.
- The corrected plan is the next revision of the plan: set its `output`
  header as [plan revisions](output-revision.md) says.

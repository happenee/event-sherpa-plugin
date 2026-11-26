# Handoff to the admin

Part of the Content Manager skill. SKILL.md says when to read it: before you
set a block's `admin_type` or write `blocked_operations`.
Every rule of SKILL.md holds here too.

Content Manager prepares content and native agenda proposals using
[Native agenda craft](native-program.md). The current server adapter and its
program-v1 contract govern tool execution, saving, confirmation and read-back.
Read those server references before applying content; this handoff only
says how the plan maps to the agenda and defines no saving or approval rule.
Shape every block so it converts one to one: `title_ref` and
`description_ref` give `title` and `description`, confirmed `start` and `end`
give the times, `admin_type` names the session type, a ready person becomes
a new speaker profile `new:<person_id>` with the texts of their profile, and
a block's speakers become its ordered assignments. A person picks an existing
profile in the admin instead when one exists; Compose does not know record
ids. Sponsors and exhibitors are not part of program-v1. What cannot be
written yet goes to `blocked_operations` with the `blocks` and `refs` it
concerns (for example "assign speakers: roles without names", "session
times: date not confirmed", "create sponsors and link them to sessions").

## Session type of every block

Every block carries `admin_type`. A Happenee session type has one of four base
behaviours (Lecture, Workshop, Time slots, Break; `knowledge/articles/kb.<lang>.03.07.md`),
and the event_content-v1 plan represents only `keynote` (Lecture) and `break`.
Native capabilities are read from the server; they do not widen this plan schema. A targeted change to an agenda the event already has works with its native types ([native agenda craft](native-program.md)). A Lecture shows its
description to attendees; a break shows only its title, place and tags, plus an
internal organizer note. A block without a speaker is therefore not a break by
default: the type follows from whether attendees need to read what happens.

| `kind` | `base_kind` |
|---|---|
| `session` | `keynote` |
| `break`, `arrival`, `networking` | `break`; `keynote` when an approved description goes with it, or when a person chose it |

- `break` is for an actual pause, a meal, arrival or a simple check-in, where a
  short title says everything (for example "Příchod & networking"). A
  speakerless block where something happens that attendees should read about
  (a welcome, a demonstration, a moderated discussion, a dinner with its own
  agenda) is a `session`.
- In `compose` mode a break, arrival or networking block gets no description.
  Put what happens into a short title instead; `description_ref` is `null`.
- In `adopt` mode a supplied description stays `verbatim` in `description_ref`,
  because it is approved text, and the block takes `base_kind: keynote`, so
  the description reaches attendees instead of disappearing behind a break.
  Record it in `decisions` with the block's `block_id` in its `scope` and the
  brief as its source. A supplied break without a description stays `break`.
  The Lecture type is still your proposal, not the brief's: the brief gave a
  description, not a type. Before the first save, name these blocks, say
  that a Lecture shows the description to attendees and a break shows only
  the title, recommend the Lecture and ask once. Save them as the person
  chose; when they keep the break, the block becomes `base_kind: break`
  with `description_ref: null` and the choice goes to `decisions`.
- On an event that already holds the agenda, every block keeps the session
  type and the texts it has there. When the plan would change either (a
  break that would become a Lecture, a description the brief words
  differently, a text changed earlier in this conversation or in the
  admin), list those blocks with the current and the new value before the
  first save and ask once which to keep. Never overwrite them silently; a
  change the person made earlier wins unless they say otherwise.
- A person may still move any of these blocks to the other type; record that
  choice in `decisions` the same way. The block keeps its `kind` and
  `block_id`: a break with a Lecture type is still a `break` block.

An event can have several break types, for example one for everyone and one
visible only to some groups. `audience` is `null` when the block is for
everyone, else the group the brief restricts it to; never guess a group. The
admin can also set visibility on a single session, but `program-v1` cannot,
so through the pilot visibility comes from the type. Do not put the type
choice in `blocked_operations`. When the agenda has an arrival, break
or networking block that stays `base_kind: break`, add one `open_items` entry
of kind `ops` listing those blocks: a person picks the break type whose
visibility matches `audience`, because the native program contract writes them only
into a type a person chose.

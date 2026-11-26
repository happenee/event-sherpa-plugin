# Adopt mode in Content Manager

Part of the Content Manager skill. SKILL.md says when to read it: after you
choose `mode: adopt`. Every rule of SKILL.md holds here too.

1. Every agenda row becomes one block: confirmed `start` and `end`, `kind`
   (`arrival`, `break`, `networking` or `session`) with its `admin_type`,
   its speakers in the given order linked to `people[]`, and title and
   description as `verbatim` items with `source` naming the brief.
2. Other approved strings the brief marks as final (event name, subtitle,
   registration intro block, e-mail subject) become `verbatim` items too.
3. Items the brief lists as still open: copy that is not written yet (for
   example invitation texts, speaker bios) becomes a `content_items` slot with
   `text: null` and `authority: proposal`; everything that is not copy
   (capacity, catering, AV, a speaker's name) goes to `open_items`. A
   recommended but unconfirmed speaker is a `people[]` entry with status
   `recommended` and an `open_items` entry. Do not fill any of them.
4. Things the organizer postponed on purpose go to `deferred` with
   `decided_in`; they are not open questions and are not raised again.
5. Ask no question while you build the plan. If something truly blocks the
   handoff, it belongs in `blocked_operations`, not in a question. The one
   question before the save, about session types and texts the event
   already holds, is in [the handoff to the admin](handoff.md).

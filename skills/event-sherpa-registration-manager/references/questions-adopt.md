# Questions in adopt mode

Part of the Registration Manager skill. SKILL.md says when to read it: in
`mode: adopt`, before the first question. Every rule of SKILL.md holds here
too.

You take the brief's form over and write nothing of your own.

1. Every listed question becomes one question in the given order, with its
   label as a `verbatim` item. Keep the organizer's codes (`Q1`, `AI2`) in
   `code`.
2. Take the type only from the brief: "at most two" or "one or at most two"
   means `multiSelect` with `max_selections: 2`; "one answer" and yes/no
   gates mean `singleSelect`; "open text" means `text`. When the brief does not
   say the type, `type` is `null` and an `open_items` entry of kind `question`
   names it. A type cannot be changed after the write, so it is never guessed.
3. Options listed in the brief become `verbatim` option items. When a choice
   question has no listed options, `options` is `[]` and an `open_items` entry
   of kind `copy` names the question. Do not write options.
4. Take `required` and `optional` from the brief. When the brief marks only
   some questions optional, the others are required; record that reading once
   in `decisions` as an assumption to confirm.
5. Information blocks (an intro, a photo and video notice) are texts, not
   questions. They go into `content_items` and, because the MCP write has no
   information text, into `blocked_operations` with their manual step.
6. Things the organizer postponed on purpose go to `deferred`. Ask no
   question; what truly blocks the write goes to `blocked_operations`.

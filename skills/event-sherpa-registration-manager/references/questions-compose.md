# Questions in compose mode

Part of the Registration Manager skill. SKILL.md says when to read it: in
`mode: compose`, before the first question. Every rule of SKILL.md holds
here too.

The questions are your `proposal`; every text the organizer approved stays
`verbatim`.

1. Start from what the answers will be used for. Every question has `used_for`:
   which agenda blocks it shapes (block ids from the Compose output whose
   `uses_registration` asks for it), which segment it separates, which
   follow-up it enables, or which operational need it serves. A question with
   no use is not asked. Nothing is asked "just in case" and no separate survey
   follows the registration.
2. Prefer choice questions an attendee can answer with a click. Use `text` only
   where an answer cannot be listed. Give each option a short label; add
   `allow_other` when the list cannot be complete.
3. A question is `optional` unless the event cannot work without its answer.
   Do not make answers required to make the data look complete.
4. Write a `min_selections` or `max_selections` only for `multiSelect` and only
   when the organizer or the purpose sets the limit (for example "at most two"
   to keep a ranking honest). Explain the limit in the question's description.
5. Use branching when a follow-up concerns only some attendees: an option
   `shows` the follow-up questions. Keep it to two levels. A follow-up shown
   only after a choice may be `required`; hidden questions never block the
   submit.
6. Texts follow the Happenee voice: short, concrete, written for the attendee,
   no dash as a mid-sentence pause.

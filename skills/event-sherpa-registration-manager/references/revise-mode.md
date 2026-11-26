# Revise mode in Registration Manager

Part of the Registration Manager skill. SKILL.md says when to read it: only
when the request asks for a revision (`output_revision-v1`) of the current
`registration_plan-v1`. Every rule of SKILL.md holds here too.

## Revise mode

When the request asks for a revision (`output_revision-v1`) of the current
`registration_plan-v1`, follow [revise mode](output-revision.md#revise-mode)
and emit only the revision. Every rule of Corrections and later changes in SKILL.md holds; in
operations a question is `form.questions/<ref>`, a journey entry
`journey/<entry>`, a text `content_items/<content_id>`, a rule
`organization_rules/<knowledge_id>`, and `decisions/<id>` and
`story_changes/<id>` as everywhere; a setting changes with `set settings` and
the fields that change, and contact fields, open items, blocked operations
and deferred items change with `replace`. A change to
a Compose block that a question feeds (`used_for`) is checked, not rewritten,
unless the change says what the question becomes.

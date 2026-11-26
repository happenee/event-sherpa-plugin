# Revise mode in Communication Manager

Part of the Communication Manager skill. SKILL.md says when to read it: only
when the request asks for a revision (`output_revision-v1`) of the current
`communication_plan-v1`. Every rule of SKILL.md holds here too.

## Revise mode

When the request asks for a revision (`output_revision-v1`) of the current
`communication_plan-v1`, follow [revise mode](output-revision.md#revise-mode)
and emit only the revision. Every rule of Corrections and later changes in SKILL.md holds; in
operations a message is `messages/<message_id>`, a text
`content_items/<content_id>`, an organization record
`org_context/<record_id>`, and `decisions/<id>` and `story_changes/<id>` as
everywhere; open items, blocked operations and deferred items change with
`replace`. When the change comes from another plan (a
block moved, a place changed), update only the texts that state what
changed, keep the rest of each message word for word, and never treat an
e-mail that was already sent as changed: telling attendees about the change
is a new message for a person to approve.

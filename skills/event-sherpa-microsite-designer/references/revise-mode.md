# Revise mode in Web Designer

Part of the Web Designer skill. SKILL.md says when to read it: only
when the request asks for a revision (`output_revision-v1`) of the current
`microsite_app_plan-v1`. Every rule of SKILL.md holds here too.

## Revise mode

When the request asks for a revision (`output_revision-v1`) of the current
plan, follow [revise mode](output-revision.md#revise-mode) and
emit only the revision, with `skill: microsite-app`. Every rule of
Corrections and later changes in SKILL.md holds; in operations a feature
instance is `feature_content/<instance_id>`, a section
`microsite.sections/<section_id>` (moved with `move`), a text
`content_items/<content_id>`, a manual step `manual_steps/<step_id>`, an
organization record `organization_context.records/<knowledge_id>`, and
`decisions/<id>` and `story_changes/<id>` as everywhere; handoffs, open
items, blocked operations and deferred items change with `replace`. A
Compose block that changed reaches an instance through its `compose_refs`;
check it, and change it only when the block was added, removed or now serves
another feature.

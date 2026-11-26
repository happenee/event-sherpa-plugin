# Handoff to the admin

Part of the Registration Manager skill. SKILL.md says when to read it:
before you show a preview, save anything or ask for approval. Every rule of
SKILL.md holds here too.

Register itself does not write. The admin's MCP previews the first registration
setup through `preview_event_registration_change`, and the approval rule of
the section "Rules every role keeps" in SKILL.md decides what is saved as a private draft
and what waits for approval: opening registration and a change of a form
participants already see are never private drafts
([what the admin accepts](admin-registration.md)). The plan
converts one to one: confirmed settings become `settings`; questions,
options, limits and `shows` become `form`. The client adds `event_id`,
`culture` and `source_hash` after reading `get_event_registration`, and uses
existing `q:ID` and `o:ID` references exactly as read. An existing question
keeps the type it was read with; the write refuses a different one. Run
`scripts/to_preview.py` where it is available; it refuses a plan that does not
fit instead of cutting it, and its reasons are the next open items.

Before a consequential change, show the exact preview, the company rules it
returned, every access setting to set by hand and everything in
`blocked_operations` that stays manual. When the preview opens registration,
explain that the links start working and obtain approval before saving.
Small edits to the plan need no repeated confirmation.

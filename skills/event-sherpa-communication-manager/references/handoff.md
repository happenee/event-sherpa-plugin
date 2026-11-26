# Handoff to the admin

Part of the Communication Manager skill. SKILL.md says when to read it:
before you prepare a draft, save anything or ask for approval. Every rule of
SKILL.md holds here too.

Communicate saves and sends nothing. Two paths remain, and every message says
which one it takes:

- A message of E-mail campaigns can become an unsent draft through
  `prepare_event_email_batch` when the organizer asks for it. Follow
  [the mapping](email-batch-mapping.md) exactly. Save requested
  private preparation through `save_event_preparation`, then read it back
  and report the real audience and remaining manual steps.
- A message of the Invitation e-mail or the Confirmation e-mail goes to
  Happenee only through a tool the conversation offers for it, with the
  preview and read back that tool asks for. A template that already affects
  participants is never a private draft. Where no such tool is offered, list
  it in `blocked_operations` with the manual step in the administration.

Placeholders, the registration button, attachments and other languages are
manual steps in the administration unless a tool offered in the conversation
covers them. Sending, scheduling and deleting follow the approval rule of
the section "Rules every role keeps" in SKILL.md.

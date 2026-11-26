# Handoff, manual steps and what stays blocked

Part of the Web Designer skill. SKILL.md says when to read it: before
you write manual steps or a handoff, and before anything is saved through the
connection. Every rule of SKILL.md holds here too.

This skill itself writes nothing. Use the connection for steps its current
tools support; the remaining steps are set up by a person. The microsite is
already public: its content and the shared Cover image change immediately,
so every save to them waits for approval as the section "Rules every role keeps" in
SKILL.md says.

- `manual_steps[]` say, per admin screen as the knowledge base names it
  (Microsite události, Obsah, Nastavení grafiky), what to set, with `refs`
  to the plan entries and `kb_ref` to the article.
- `blocked_operations[]` list what the MCP cannot write yet (intro text,
  tab order and display, feature content), each with the `manual_step`
  that does it by hand.
- Only for a new event, the structure of Venue, Contact, Agenda and Speakers
  may go to `preview_event_creation` as `handoffs[]` with
  `arguments.module_types` from `locality`, `contact`, `sessions`,
  `speakers` (code names of the creation tool, not product terms). It
  creates the features empty and unpublished; say so in `note`. One handoff
  per event: when the app plan of the same story already hands these over,
  do not repeat it. The agenda itself goes from Compose through
  Content Manager using the server program contract, not from this plan.

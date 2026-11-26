# Write the texts

Part of the Communication Manager skill. SKILL.md says when to read it:
before you write the subject, body or button text of any message. Every rule
of SKILL.md holds here too.

- Plain text only: no HTML, no Markdown, no URLs. The body is stored as plain
  text and line breaks are kept.
- No placeholders such as `::UZIVATEL_JMENO::` or `::QRCODE::` in any text:
  whether they survive the draft path is not verified. When a message needs a
  personal greeting, the QR code or the attendee's registration data, write
  the text so it reads well without it and list the placeholder in
  `blocked_operations` as a manual step.
- A subject at most 250 characters on one line; a body at most 10 000 bytes;
  no emoji. Short is better: a reminder is three to five sentences.
- Reuse what is approved. When Compose or the brief approved a sentence, it
  is its own `verbatim` body part in `body_refs`, not merged into a proposal.
- Facts in a text (date, time, place, agenda times) come only from the
  inputs. What is unknown stays out of the text and goes to `open_items`.
  No text holds a note to the organizer in place of a missing fact: no
  brackets, no "doplnit" or "TBD", no question. A draft can be sent without
  another read, so write the sentence to read well without the fact and name
  the gap in `open_items` and in the reply.
- An agenda in an e-mail lists exactly the blocks the event's program
  holds, read from Happenee, with their own titles and times. Never add a
  line the program does not have, such as the end of the event or a
  closing („16:00 Závěr“, „Konec setkání“); the end time of the event goes
  into a sentence, not into the agenda.

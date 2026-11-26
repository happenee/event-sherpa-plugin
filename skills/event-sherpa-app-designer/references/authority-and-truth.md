# Authority and truthfulness

## Authority

- `verbatim` means the text equals its source character for character:
  wording, punctuation, quotes, spacing and capitalisation. Never shorten,
  translate, fix or restyle it. If it looks wrong, say so outside the JSON.
- A text taken from the Compose output keeps its Compose `content_id`, text
  and authority. This skill never rewrites Compose copy; it only places it.
  A section that shows an approved Compose text points at that `content_id`
  in `text_refs`; it does not copy the text into a new item, least of all
  with authority `proposal`.
- An approval covers one item only. An approved microsite order approves the
  order and the names in it, not texts the brief does not give.
- `proposal` is this skill's own text. In `adopt` mode there is no proposal
  with a text: open copy slots have `text: null` and an `open_items` entry of
  kind `copy`.
- `editable` is for text the organizer allowed to adjust; `edit_scope` says
  how far (for example "length only, keep the meaning").
- In a revision, an item that the change does not touch keeps its
  `content_id`, `text` and `authority`.

## Truthfulness

- Nothing is invented: no venue name or address, contact person, e-mail,
  phone, link, speaker, bio, sponsor, exhibitor, logo, photo, capacity,
  attendance number, price, date or year that the input does not give. Such
  a value is a field with `text: null` and an open item of kind `fact` or
  `asset`.
- Dates, times, e-mail addresses, phone numbers and links in any text come
  from the input word for word.
- A section about a product or capability the event presents (the
  organizer's own, or a Happenee one) is content of the event, not a promise
  that the capability is available. Describe what
  will be shown, not that it works in production.
- Internal labels `LIVE`, `PROTOTYPE` and `VISION` never appear in any text,
  not even in an open item that forbids them; write "internal labels"
  („interní štítky“) instead.
- A feature behaviour the knowledge base does not describe (for example
  attendees voting on each other's questions, when the article describes
  likes only in the projection view) is not promised. Record it as an open
  item of kind `verify`, to check in the rendered app before anyone tells
  attendees about it.
- What a person postponed on purpose (a header image, speaker photos) goes to
  `deferred` with `decided_in`. It is not an error and is not raised again.

## Voice

Follow the Happenee voice: concrete, calm, written for the attendee. No dash
as a mid-sentence pause where a comma or full stop works, headlines without a
trailing period, no "seamless", "powerful", "world-class", "unleash" or
"supercharge". In Czech write „e-mail“ with a hyphen. Call the Attendee app
the "event app" in texts for attendees and use the exact admin labels in
steps for the organizer. Never call a content or engagement feature a module.

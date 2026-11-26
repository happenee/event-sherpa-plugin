# Compose mode in Content Manager

Part of the Content Manager skill. SKILL.md says when to read it: after you
choose `mode: compose`. Every rule of SKILL.md holds here too.

Every text you write here is a `proposal`; every text the organizer approved
stays `verbatim`.

1. **Concept.** One sentence: for whom and why they should come. Add at most
   two variants, only when they differ in substance (audience, format or
   outcome), each with one sentence on what it changes. The concept sentence
   goes into `content_items` with surface `concept`.
2. **Engagement levels.** Do not rely on a room starting to talk or run a
   workshop on its own. Offer up to three levels (`listen`, `react`, `share`),
   each saying what it asks of the attendee and which blocks use it. Sharing
   is voluntary; an answer in a form is not a nomination for the stage. A
   block where attendees share needs a prepared backbone that carries it
   when nobody volunteers: a moderator with examples from the registration
   answers, short contributions agreed in advance, or a simple reaction
   such as a click; volunteers add to it, never fill it alone.
3. **Agenda.** Blocks in order, each with a `purpose` that says what the
   attendee gets from it. Speakers are people from `people[]` in speaking
   order, named by role (for example "keynote speaker", "panel
   moderator"); see [speakers, sponsors and exhibitors](speakers-and-partners.md). The session type of each block is in [the handoff](handoff.md). Use `start` and `end` only for confirmed
   times; otherwise give `duration_min` and leave the times null. Every block
   without confirmed times has a `duration_min`. When the input does not fix it
   (for example the remaining minutes are split between a break and a closing
   block), choose a working duration that fits the known frame and record it in
   `decisions` as an assumption for the organizer to confirm; never leave both
   times and duration empty. When the event presents a product, show it
   inside the topic it helps, not as a separate roadmap pitch, unless the
   organizer asks for a product block. If registration
   answers should shape the agenda, say in `uses_registration` which answers
   feed which block; do not add a separate questionnaire after registration.
4. **Texts.** Titles and descriptions of blocks (a title only for a break,
   arrival or networking block) go into `content_items` as `proposal`, written
   per the Happenee voice (short, concrete, no hype, no dash as a mid-sentence
   pause). Copy for the registration form, the e-mails, the microsite and the
   attendee app belongs to the skills of those modules; write it here only
   when the organizer asks for it in this step.
5. **Unknowns.** Capacity, venue, date, names, bios and numbers that the input
   does not give stay out of every text. List them in `open_items`. A working
   estimate the organizer called an estimate is an open item, not a fact.
   No text holds a note to the organizer in place of a missing fact: no
   brackets, no "doplnit" or "TBD", no question. Texts are saved where
   attendees can see them, so write the sentence to read well without the
   fact and name the gap in `open_items` and in the reply.
6. **Speakers, sponsors, exhibitors.** Fill `people[]` and `partners[]` as
   [speakers, sponsors and exhibitors](speakers-and-partners.md)
   says. Roles you propose are `recommended` until the organizer
   confirms them.

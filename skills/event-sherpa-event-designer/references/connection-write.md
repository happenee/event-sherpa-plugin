# Changes in Happenee through the connection

Part of the section With the Happenee connection in SKILL.md, which says
when to read this file: before the first call that prepares, saves,
confirms, publishes, sends or deletes anything, and before a preview of
such a change. Every rule of SKILL.md holds here too.

- **The tools decide which technical steps can be carried out.** Where this
  skill says a step is manual, a handoff or for a person in the admin only
  because the skill has no connection and writes nothing, the Happenee tools
  in the conversation may cover it. Check their descriptions, schemas and
  access requirements first: a step a tool covers goes through that tool and
  the plan says so; only what no tool covers stays a manual step. Missing
  scope or access is reported as missing access, never as a missing
  capability. A connection resolves none of the other blockers: missing
  facts, unconfirmed people, conflicting requirements, a pending change to
  the Event Story or a limit on whose wording a text may use stay blocked
  until the condition this skill states for them is met, even when a tool
  could write the step. Carry out only the parts that are ready and keep the
  rest in the plan as open.
- **How a change is made.** Through the tools only, using their current
  schemas and access checks, under the approval rule of Rules every role
  keeps. Keep any technical preview the tool requires, save a private draft
  through `save_event_preparation` when it supports that draft, read the
  saved result back and say what was saved. A preview required by the
  protocol is not a reason to ask for the same scope again. Before an
  approval, show the content, audience or count, timing and effects by
  names and dates; never ask the person to copy an id or a hash.
  Adding, importing or changing participants is never a private draft:
  show who is added or changed, with which state and which e-mails they may
  receive, and obtain explicit approval before the confirming call, even
  for one test contact. Say in advance what will be saved as a private
  draft (an agenda, a form, an e-mail) and never promise a separate
  approval for a step you then save without asking. The same boundary applies to a small edit of an
  already published item. A broader or materially different change needs
  its own agreed scope.
  Prepare and save what depends on the date and venue (agenda, deadlines,
  e-mail copy) against the date and venue Happenee holds now. When a
  change of date or venue does not go through, still save everything that
  would be the same under either value, and never hold other work back for
  it. Anything that would state or be computed from the new date or venue
  (e-mail copy naming it, reminders, deadlines, moved agenda times) stays an
  unsaved proposal written for the requested value, shown to the person
  with the reason, and is saved once the change is in Happenee. Never save
  such content against the old date or venue the person asked to leave.
  A saved draft is neither published, opened nor sent, so say which of these
  happened. The Event microsite is the exception: it is published for now,
  so text saved to it and the event's Cover image (Úvodní obrázek, shared
  with the e-mails and the app) are visible at once. The same applies to
  changing a published speaker's photo. Show that effect and obtain the
  concrete approval before saving; these are not private draft changes.
  Never promise an unpublished microsite and never warn that its
  direct address may or may not be reachable.

- **A targeted change to an existing event needs no Event Story.** When
  the person names one thing the event already has and what it should say
  or be (a block's description, a form question, a reminder's subject, a
  microsite text), read the event and make that one change the way the
  rule above says, even when the event has no Event Story: this skill's
  "without an approved story, stop" covers designing a plan, not this.
  Before the save, say which other places the change touches (an e-mail
  or the microsite that names a moved block) and fix none of them
  unasked; change nothing else and add no improvements of your own. Never
  say the change matches an Event Story you have not read. A request that
  needs content you would have to invent, or that adds or restructures
  something (new blocks, a new campaign, the form's structure, the order
  of sections), is design work, and the skill's rule on the story holds;
  when it is unclear which of the two it is, say how you read it and ask
  once.

- **Images.** A preview of a speaker photo or of the Cover image shows only
  the file that goes to the tool, and its size only as the tool returned it;
  never show a picture from a web search or any image other than the one
  sent to the tool as that preview. The tools take a file in the chat, not a
  web address: when the person gives a link, say at once that they need to
  attach the file. When the person asks you to generate the Cover image or
  a speaker photo and your client can, generate it and send that generated
  file to the image tool as the file in the chat, then continue to the
  preview; never stop after generating and never ask them to save and
  attach it first. If the tool refuses the file, or your client cannot hand
  it over, use `create_event_image_upload`: when your client can read and
  send the file, upload it there; otherwise offer the `file_picker_url` of
  that same operation, so the person picks the file once. Never ask them to
  download the image and attach it again. After either way read the image
  with `get_event_image` under the same operation and show the Happenee card
  with the picture itself; a link to the full image is only an addition to
  that card. Never say it is in Happenee until a reading shows it there.
  Generate an image in the organizer's own brand (logo, colours, typeface)
  when they gave it; without it ask once for it or say that the image is
  neutral, never invent a brand. Send the file itself, never its name, a link or a description of
  it; a refusal of a wrong argument is your mistake, not a fault of
  Happenee.
- **Fresh previews.** Prepare a preview right before asking for its
  approval, after every other save of the same turn: a preview prepared
  earlier goes stale when another change reaches the event, and Happenee
  then refuses it. Publish content features together in one preview.
- **Participants together.** Contacts the person supplied together go into
  one preview and one approval, when the tool takes several: on the
  Happenee card, or in a client without cards through the review link the
  preview returns. Never split them into one approval per contact. Afterwards read
  the result and name each contact that was added by name and e-mail, and
  any that still waits. An existing contact keeps its own name, company and
  position; say so before, never promise the values you proposed. Adding
  the first participant locks changes to the registration form through
  the connection, so finish the form before adding anyone and say this
  before the first add. Never ask the organizer to pick by hand a contact
  whose e-mail they gave; when a next step needs a participant the
  connection cannot hand over, say it is a step in the admin.
- **Several asks at once.** When one message asks for several things (for
  example speakers, venue, contact, an image, registration and the app),
  carry out every part that is ready, each with its own preview or save as
  the approval rule says, and let no part wait for another that does not
  depend on it; an image never holds up the rest. End with one bullet per
  part and its state: saved and read back, waiting for approval, blocked
  and why, a manual step in the admin, or not done and why. Never drop a
  part silently and never ask again for what the person already said.

- **Creating an event.** The event type follows the venue: In-Person
  (Fyzická) for an event that happens at a place, Virtual (Virtuální) only
  when it happens online, Hybrid (Hybridní) for both. Name the type in
  words in the creation preview, read it back after the save and say which
  type Happenee holds; when it differs from the preview, say so and offer
  the fix. What the creation tool calls `locality`, `contact`, `sessions` and
  `speakers` are the content features Venue, Contact, Agenda and Speakers
  (Lokalita, Kontakt, Program, Řečníci), never modules. Pass only the
  features the Event Story or the brief needs and say in the preview why
  each is there: Venue for an event at a place, Agenda when it has
  sessions, Speakers when it names people who speak, Contact when the
  person gives one; never add one only because the tool offers it.
  When the plan or the brief has an agenda, pass its blocks, word for word
  and with their times, to the creation when the creation tool takes them,
  so they are in the creation preview. After the creation read the new
  event's program back and report the blocks as Happenee holds them. Only
  what the read back shows counts as created. Add through a program change
  only the blocks the read back lacks, never all of them again, so no
  block is in the program twice.
  When an Event Story or another plan was saved for this event before it
  existed, attach it right after the creation: save its current revision
  once more unchanged with the new event's id (`save_event_role_plan`
  takes `event_id`, and an event can be attached once) and read it back,
  so later roles and new chats find it with the event.
  Settings the Event
  Story or the person asked for, such as Approved registration (Schvalovaná
  registrace), go into the creation or the first registration preview when
  a tool takes them, the same way in every language; what no tool takes
  stays an open step, said in words.
  Approval follows the Happenee card: when the card offers a button for
  creating the event or applying the change, the person approves there, and
  when the card reports success, continue with the next step of the request
  (for a new event, its program) without waiting for them to write again.
  Only when the card has no button or the client cannot show it, give the
  review link the preview returned, say the person approves there under
  their own account, and wait. A reply in the chat ("create it", „založ“)
  does not replace either step. Once they approved, complete the same
  operation with the same proposal, never a new preview or a second
  creation, then read the event back. When the completion is refused as
  not approved yet, say so in one sentence and point to the same card or
  link again.
- **Access.** Registration only for invited contacts, Individual
  registration links and similar access settings count as set only when a
  tool result or read back shows them. Until then they are an open step,
  and no text promises them: not a reply, not the Event Story and not the
  copy of an e-mail ("confirm through your personal invitation", "osobní
  pozvánka", "osobní registrační odkaz").

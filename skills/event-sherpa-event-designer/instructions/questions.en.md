The question bank for this run. Ask from it: the id of a question goes into `presentation.conversation.questions_asked[]`. It came with this turn and holds for the whole conversation.

# Describe: question bank

The only questions CLARIFY may ask. One or two per turn, ordered by how much the
answer moves the proposal, never one already answered or already on a card.

Ask like an experienced event professional would, from the brief: name the event
and its people the way the brief did. Under every question stand the two
sentences S4 asks for, both of them every time: why the answer changes what you
propose, and what you will assume if the answer is "I don't know", which is the
item's `default` in the person's words. A candidate read from the brief stands
in for neither, and a wording below that already carries one of them still
needs the other. The wordings below are the base, not a script. Ask
about what the organizer wants from the event and what they expect of it, never
about a setting they cannot know yet at their moment in the planning (the table
under "Where in the planning the person is"): a person with an intent and no
date is not asked how people will get in, and nobody is asked about groups,
on-site changes or a recording as a question in its own right. Those items are
assumed by default and the story shows the assumption; they are asked only
where the brief itself raises the topic and leaves it open.

A person who says they are new to this or do not know what to write gets, under
each question, two or three short answers to pick from, drawn from the brief, or
one example answer. A question they say they did not understand comes back
shorter and with an example, never in the same words, and stays open.

How many in all depends on the surface the run header names. On `web`, at most
three questions before the first artifact, and one turn of them is
`goals_per_side` with `success_measure`; the third is whichever other item moves
the proposal most. On `codex`, the surface the ChatGPT packages run on, at most one further round
after that, and `access_model` in it only where the story cannot be drawn without it; that
round is the last, whatever is still open after it becomes an assumption, and the
next turn is CONFIRM. On `claude-code` and inside the product, at most two further
rounds after that. On the web
`audience_relationship` is asked only where the brief really does not say what
the attendees are to the organizer.

Every item carries the same fields:

- `why` says what changes in the proposal. If nothing changes, the question does
  not belong in the turn.
- `default` is the assumption to carry when the person says they do not know, and
  how it gets marked.
- `cs` and `en` are the wordings. Keep their meaning and their register, tie them
  to the brief; keep the vykání, the hyphen in "e-mail" and the absence of dashes.
- `skip_if` says when the brief already answers it.
- `ask_only_if`, where present, says the item is assumed by default and asked
  only in that case; without it the default applies and the card says
  `unasked`.
- `source` is the rule or article behind it, for the source map. It is internal and
  never appears in customer-facing text.

## How an unknown is marked

Every carried assumption is written in four places, so that a reader can see it was
an assumption and not a fact:

1. `assumptions[]` gets `{id: a-NN, key, value, reason, impact_if_wrong, accepted_in_confirmation, source_refs}`.
2. The matching `unknowns[]` entry gets `assumption: "a-NN"` and
   `answer_status: "answered_unknown"`.
3. The understood card for that key gets `certainty: "working_assumption"` and the
   assumption id in `assumption_ids[]`.
4. Where the assumption drives a branch, that branch's `data_needed[]` entry gets
   `status: "assumed"` with the same `key`, and the branch's `needs_validation[]`
   says in one sentence what a human has to confirm. The link starts at step 1:
   a `data_needed[]` item is `assumed` only with the key of an entry written
   there, and with no such entry it is `unknown`.

`answered_unknown` is for a question that was put to the person and answered
with "I do not know". An item you chose not to ask is `unasked`, and its card
says so instead of reading as an answer; the default still applies.

An answer is recorded at the strength it was given, and the four places above are
for the weak end of that range. A yes is the other end: where the person accepts
a capability you named, that capability goes into `capabilities[]` as
`recommended` or `conditional` with its branch, and the card for it is
`confirmed`. Writing down the nearest smaller thing you were going to propose
anyway, or marking the phase `applicable: false`, turns an answer into a
narrowing nobody agreed to. `applicable: false` is for a phase the person ruled
out, and for nothing else.

An unknown a reader ends up seeing is one sentence in three parts: what we do
not know yet, why it matters, and what it would change in the proposal. That is
`assumptions[]` in the order the story prints it, `value`, `reason`,
`impact_if_wrong`. The tone is help rather than a reservation, and none of these
sentences makes the next step wait for an answer.

Three things have no safe default, and none of them is a question in this bank: the
event type or goal, the audience, and the scale or date. If any one of the three is
unknown, do not assume, do not draw a map, and say that the proposal is blocked
until it is known; that is the INSUFFICIENT bar, and it is met only when all three
are there. A map built on a guessed audience looks finished and is wrong in every
phase. Every item below is safe to assume precisely because the three are already
known when CLARIFY starts.

Any goal-shaped sentence clears that bar, an operational one included, which is
why `goals_per_side` still asks what the event itself is meant to lead to.
Clearing the bar and knowing the goal are two different things.

## Where in the planning the person is

Read it off the brief and never ask for it. It changes what the story leans on,
not whether there is a story.

| moment | how it shows in the brief | what the story does |
|---|---|---|
| intent only | no date and no venue, the brief says what the event should bring | clears the INSUFFICIENT bar on the stated goal; lead with the goals and the sides, sketch the setup with scale and date as named assumptions that say which size band and season the sketch is built for, say what follows once a date and a venue exist |
| frame known | a date or a venue, the programme still being put together | the whole story, with the open things named as assumptions |
| preparation running | people are invited, registration or the communication is being handled | start from what already runs and do not propose it a second time |
| days away | the date is weeks off and the day itself is the subject | weight on arrival and live operations, the rest as advice for next time |
| after the event | it has happened | weight on the evaluation, on bringing people back to the content, and on the next event |

## Items

### QB-01 `access_model`

- **why:** Decides whether the path starts with an open registration form, an
  invitation to a named list, an approval step, or a nomination by someone else.
  That choice changes who owns the list, which e-mail goes out first, and whether
  hiding a page is enough or a real authorization is needed.
- **default:** Invitation to a named list, because most briefs that mention a
  known audience mean that. Marked as an assumption on `access_model`.
- **cs:** „Jak se k vám lidé dostanou: zvete konkrétní lidi, může se přihlásit kdokoli, nebo o účasti někdo rozhoduje?“
- **en:** "How do people get to you: do you invite specific people, can anyone sign up, or does someone decide who takes part?"
- **skip_if:** The brief already names invitations, a public sign-up page, an
  approval step or nominations; or the moment is "intent only", where the
  default is assumed and named.
- **source:** V6-R04, V6-R11, kb.cs.01.06, kb.cs.07.01

### QB-02 `paid_or_free`

- **why:** Paid entry brings an order, a payer, a holder and a payment state, which
  are four different objects and need their own checks. Free entry means ticketing
  is excluded, with a reason, instead of quietly offered.
- **default:** Free entry. Marked as an assumption on `paid_or_free`; if it
  holds, `tickets` goes to `do_not_use` with the free entry as the reason and
  paid entry as the revisit trigger. Where the audience is internal, the reason
  is the internal audience itself, not an assumption about what such events
  usually do.
- **cs:** „Kdo účast platí: účastník, vaše firma, nebo partner?“
- **en:** "Who pays for taking part: the attendee, your company, or a partner?"
- **skip_if:** The brief names a price, a ticket, a sponsor-funded entry or says
  entry is free. Where `audience_relationship` settled the audience as internal
  and no third party pays, the question is not asked at all: nobody sells their
  own people a ticket, and `tickets` goes to `do_not_use` with the internal
  audience as the reason.
- **source:** V6-R05, V6-R13, kb.cs.07.03

### QB-03 `format`

- **why:** Physical, online and hybrid have different arrival phases: a queue and a
  badge, a join link, or both at once with two audiences that need the same
  content. Using the web app at a physical event does not make it hybrid, so the
  question has to be asked rather than inferred.
- **default:** Physical, on-site only. Marked as an assumption on `format`; the
  `arrival` phase then describes on-site arrival and the online branch is
  conditional.
- **cs:** „Potkáte se na místě, online, nebo obojí?“
- **en:** "Will you meet in person, online, or both?"
- **skip_if:** The brief names a venue with no remote audience, a webinar, a
  livestream or an explicit hybrid setup; or the moment is "intent only".
- **source:** V6-R10, kb.cs.07.06, kb.cs.07.07

### QB-04 `existing_systems`

- **why:** If registration, ticketing or the public website already works
  elsewhere, the right proposal is to connect to it, not to open a second one.
  A second registration beside a working one splits the list and breaks the count.
- **default:** Nothing runs elsewhere. Marked as an assumption on
  `existing_systems`; if it turns out wrong, the whole `before` phase changes, so
  `impact_if_wrong` says exactly that.
- **cs:** „Co z toho už dnes máte a má zůstat, jak je?“
- **en:** "What of this do you already have today that should stay as it is?"
- **skip_if:** The brief names the tools in use, or says this is the first event of
  its kind.
- **ask_only_if:** The brief mentions a spreadsheet, e-mails, another tool or a
  website already in use and does not say whether it stays.
- **source:** V6-R07, V9-R02, kb.cs.01.06

### QB-05 `groups_with_different_content`

- **why:** One event with several audiences, such as employees and their guests, or
  VIPs and general admission, means different content, different e-mails and
  different entitlements. Groups are global in a workspace, so the naming matters
  before anything is built.
- **default:** One audience with the same content for everyone. Marked as an
  assumption on `groups_with_different_content`.
- **cs:** „Jsou na akci lidé, kterým chcete říkat něco jiného než ostatním, třeba partneři, hosté nebo VIP?“
- **en:** "Are there people at the event you want to tell something different from the rest, such as partners, guests or VIPs?"
- **skip_if:** The brief names roles, tracks, VIPs, guests or branch teams with
  distinct content.
- **ask_only_if:** The brief names two kinds of people at the event and does
  not say whether they see the same thing.
- **source:** V6-R06, V6-R11, kb.cs.07.02

### QB-06 `live_changes`

- **why:** Changes during the event decide whether notifications, an on-site
  operator and a fallback channel belong in the story. It also decides how much of
  `live_operations` is real work rather than a heading.
- **default:** Small changes happen and one person handles them. Marked as an
  assumption on `live_changes`; the notification branch stays conditional.
- **cs:** „Když se v den akce něco posune, kdo to bude řešit?“
- **en:** "When something shifts on the day, who will handle it?"
- **skip_if:** The brief already names an on-site team, a production schedule or
  says the programme is fixed.
- **ask_only_if:** The brief itself says the programme moves on the day and
  does not say who handles it.
- **source:** V6-R18, V6-R22, kb.cs.07.03

### QB-07 `networking_purpose`

- **why:** Connecting people needs a purpose, a reason for the attendee, time in
  the programme and a permission model. Without those, profiles and chat are an
  empty feature, and QR exchange is not the same thing as a booked meeting.
- **default:** No structured networking, only informal meeting. Marked as an
  assumption on `networking_purpose`; if it holds, `matchmaking` and `attendees-feature`
  go to `do_not_use` with the missing purpose as the reason.
- **cs:** „Stačí, když se lidé najdou a vymění si kontakt, nebo má být část programu vyhrazená setkávání?“
- **en:** "Is it enough that people find each other and swap contacts, or should part of the programme be set aside for meeting?"
- **skip_if:** The brief or the answers say people should meet, swap contacts or
  network, without a word about meetings: that is the informal default. Also
  where the brief names matchmaking, one-to-one meetings, a partner meeting
  agenda or explicitly rules them out.
- **source:** V6-R08, V6-R21, kb.cs.07.04

### QB-08 `after_materials`

- **why:** Promised materials decide whether the `after` phase has content at all,
  and who has to produce it before the event ends. Access after the event depends
  on the licence, which is not visible here, so it is marked rather than promised.
- **default:** Slides and practical information are shared afterwards. Marked as an
  assumption on `after_materials`; availability is `needs validation`.
- **cs:** „Co si mají lidé po události odnést a jak dlouho se k tomu mají vracet?“
- **en:** "What should people take away after the event, and for how long should they be able to come back to it?"
- **skip_if:** The brief names post-event materials, certificates or says there are
  none.
- **source:** V6-R19, kb.cs.01.06, kb.cs.07.01

### QB-09 `after_recording`

- **why:** A recording brings two separate questions that nobody answers by
  default: who owns the rights to publish it, and who actually produces the file.
  Video production is outside the product, so an unasked recording turns into a
  promise Happenee cannot keep.
- **default:** No recording. Marked as an assumption on `after_recording`; if a
  recording is wanted later, production and rights are named as manual next steps.
- **cs:** „Má z události zůstat záznam, a pro koho?“
- **en:** "Should a recording remain from the event, and for whom?"
- **skip_if:** The brief names a recording, a livestream archive or says there will
  be none.
- **ask_only_if:** The brief mentions a stream, a video or a recording and does
  not say who gets it afterwards.
- **source:** V6-R14, kb.cs.07.07

### QB-10 `after_contacts`

- **why:** The contacts an attendee made are the part of the event they keep. It
  decides whether the app has a reason to exist after the last session, and, where
  partners are involved, what data may be handed over and to whom.
- **default:** Attendees keep their own contacts; nothing is handed to third
  parties. Marked as an assumption on `after_contacts`.
- **cs:** „Mají si účastníci po události odnést kontakty? A má někdo další, třeba partner, dostat data z události?“
- **en:** "Should attendees keep the contacts they made? And should anyone else, a partner for instance, receive data from the event?"
- **skip_if:** The brief names lead capture, a partner data handover or an explicit
  rule against it.
- **ask_only_if:** The brief mentions partners or leads and does not say what
  they get after the event.
- **source:** V6-R21, V6-R15, kb.cs.07.04

### QB-11 `after_followup_programme`

- **why:** A follow-up session, a training path or a community changes the `after`
  and `next_event` phases from a closing note into a real branch, and it changes
  what is worth keeping in the app.
- **default:** No follow-up programme. Marked as an assumption on
  `after_followup_programme`; `next_event` stays applicable but thin.
- **cs:** „Navazuje na událost něco dalšího? Například školení, další setkání nebo komunita.“
- **en:** "Does anything follow this event? A training course, another meeting or a community, for example."
- **skip_if:** The brief names a series, a programme, a community or a one-off
  event.
- **source:** V6-R19, kb.cs.01.07

### QB-12 `repetition`

- **why:** A recurring event is copied, and copying carries old dates, old people
  and unverified import templates. Knowing it repeats moves work into `next_event`
  and adds a comparison of source and target to the setup dependencies.
- **default:** One-off event. Marked as an assumption on `repetition`;
  `next_event` describes what would be reusable if it does repeat.
- **cs:** „Bude se událost opakovat, třeba každý rok nebo každé čtvrtletí? Nebo je jednorázová?“
- **en:** "Will this event repeat, yearly or quarterly for instance? Or is it a one-off?"
- **skip_if:** The brief names an edition, a year, a series or says it is the first
  and only one.
- **source:** V6-R03, V6-R19, kb.cs.01.07

### QB-13 `agency_client_brand`

- **why:** An agency describing a client's event is a different setup from the
  client describing their own: branding, billing and workspace access are three
  separate decisions, and the person in the chat may not be the one who decides.
- **default:** The person organizes their own event. Marked as an assumption on
  `agency_client_brand`; `presentation.agency_context` stays `null` until it is
  confirmed.
- **cs:** „Pořádáte událost pro sebe, nebo ji připravujete pro klienta? Zajímá nás, čí značka bude na microsite a kdo rozhoduje o rozsahu.“
- **en:** "Are you running this event for yourself, or preparing it for a client? We need to know whose brand the microsite carries and who decides the scope."
- **skip_if:** The brief names an agency, a client, or the organizer's own company
  as the host.
- **source:** V6-R13, V6-R19, kb.cs.07.02

### QB-14 `partners`

- **why:** Partners, sponsors and exhibitors expect something specific, and what
  they expect decides whether profiles, meetings, lead capture or none of them
  belong in `brand_partners`. A guest list is not a substitute for the leads a
  partner was promised.
- **default:** No partners. Marked as an assumption on `partners`; the
  `brand_partners` phase stays applicable and describes the organizer's own brand
  only.
- **cs:** „Jsou na události partneři, sponzoři nebo vystavovatelé? Pokud ano, co konkrétně od účasti očekávají?“
- **en:** "Are there partners, sponsors or exhibitors at the event? If so, what exactly do they expect to get out of it?"
- **skip_if:** The brief names sponsors, exhibitors, partner stands, or says the
  event has none. Where `audience_relationship` settled the audience as internal
  and no third party pays for the event, the question is not asked;
  `goals_per_side` asks instead who inside the company commissioned it.
- **source:** V6-R21, kb.cs.07.04, kb.cs.07.03

### QB-15 `brand_assets`

- **why:** Decides whether the Event Story is shown in the customer's own brand
  or in a neutral one. It changes nothing in the proposed setup, which is why it
  is last, and it changes what the person actually sees, which is why it is here
  at all. The answer goes to `presentation.brand` and nowhere else: it is never a
  recommended setting, a capability or a dependency. The question offers a link
  to the website as an answer, so an address, from this answer or already in the
  brief, goes to `presentation.brand.site_url` with the matching `source`,
  written the way the person wrote it, scheme or no scheme (S12). It is where
  the site is, not what the brand is: an address on its own leaves `confirmed`
  false.
- **default:** A neutral look in Happenee's own brand, added later if the assets
  arrive. Marked as an assumption on `brand_assets`; `presentation.brand.confirmed`
  stays `false`, because nothing concrete was confirmed (S12). An address alone
  does not change that default; it only says where to look later.
- **cs:** „Máte k události logo a hlavní barvu, které bychom měli použít v návrhu? Stačí odkaz na web nebo jen barva slovy. Pokud ne, připravíme návrh v neutrální podobě a doplní se později.“
- **en:** "Do you have a logo and a main colour for the event that we should use in the proposal? A link to your website or the colour in words is enough. If not, we prepare the proposal in a neutral look and it can be added later."
- **skip_if:** The brief carries a logo, a hex code, a colour named with a link, a
  web address, or a mention of a brand manual or an attachment.
- **source:** V6-R13, design brief §8 personalizace

### QB-16 `goals_per_side`

- **why:** What each side wants decides which branches of the story carry weight
  and what the setup is argued from. Without it a story can say what to set up
  and not why anybody wanted it.
- **default:** Where the brief states the organizer's goal, carry it as the
  brief states it, marked as an assumption on `goals_per_side`. Where the brief
  names a pain, an outcome or a past problem instead, the candidate read from
  it: offered in the question, and when unconfirmed carried into `hero.goal`
  and `outcomes.business` as a working assumption whose text ends with
  `pracovní předpoklad` or `working assumption`. Where the brief names nothing,
  the assumption's `value` is that no goal has been set and that the story is
  argued from what has to work. Never write a goal of your own as that value
  and never derive one from the type of event: "it is about keeping the
  relationship with partners" is a guess when nobody said it and nothing in the
  brief points at it. The goals of the other sides stay unknowns and are never
  estimated from the type of event. Where the person says they do not know
  because the goal has to come from whoever commissioned the event (management,
  HR, sales), the next turn does not ask again: it offers two or three working
  variants read from the brief, each with what it would change in the event,
  and the one or two questions to take back to that commissioner. The variant
  the person leans to is carried as a working assumption; no approval by the
  commissioner is ever implied.
- **cs:** „Rozumím, co má při přípravě a na místě fungovat. A k čemu má událost sama vést? Co z ní máte mít vy jako pořadatel, co účastníci a s jakým dojmem mají odcházet, a pokud tam budou, co partneři nebo vystavovatelé. Stačí jedna věta ke každému, a když to u někoho zatím nevíte, řekněte to.“
- **en:** "I understand what has to work in the run-up and on the day. What is the event itself meant to lead to? What should you as the organiser get out of it, what should the attendees get and what feeling should they leave with, and what should partners or exhibitors get if there are any. One sentence each is enough, and if you do not know yet for one of them, say so."
- **skip_if:** The brief says what the event is meant to lead to for the
  organizer and for the attendees, both. A sentence about what has to work,
  what a tool has to be able to do, or what should remain after the event,
  handling the workshop sign-ups, getting guests in without a queue, leaving
  people the materials and the contacts, is the run of the event and not what
  it is for, so it does not skip this question. Where `audience_relationship` settled the audience as internal
  and no third party pays, the part about partners drops out and the question
  asks instead who inside the company commissioned the event: management, HR or
  sales. What that commissioner wants is the organizer's side and goes into
  `outcomes.business`; `outcomes.partner` is for sponsors and exhibitors only.
- **source:** V6-R01, V6-R21, kb.cs.07.03, kb.cs.07.04

### QB-17 `success_measure`

- **why:** A measure agreed before the event decides what has to be collected
  and where; afterwards nobody defines one. The second half of the question, who
  the result is shown to, is who the story is written for.
- **default:** Where the brief names a pain or an outcome, the candidate measure
  that would show it was met: offered in the question, and when unconfirmed
  carried into `event_success.measure` as a working assumption whose text ends
  with `pracovní předpoklad` or `working assumption`, with `shown_to` `null`.
  Otherwise no agreed measure, carried as an unknown and marked as an assumption
  on `success_measure`; `event_success` stays `null`. No number is invented in either case; the candidate is a sentence about the
  event, not a figure, and never the attendance target: „100 až 140 přítomných“
  is how many came, not whether it worked. A requirement written as what people should have
  afterwards is an outcome and carries a candidate: „partneři mají mít všechny
  kurzy a data navždy“ gives the goal that partners keep coming back to the
  content after the course, and the measure that they do. Whatever the answer,
  each goal it covers lands in its own `success_criteria[]` record; the answer
  is never stretched over goals it did not name, and their records keep the
  candidate as a working assumption.
- **cs:** „Podle čeho po události poznáte, že se povedla, a komu to budete ukazovat?“
- **en:** "How will you tell afterwards that the event worked, and who will you be showing that to?"
- **skip_if:** The brief names a measure, or the person the result is shown to.
  Briefs rarely name either, so this question is asked in most runs.
- **source:** V6-R20, V6-R14, kb.cs.07.03, kb.cs.07.06

### QB-18 `audience_relationship`

- **why:** Decides which of the other questions get asked at all. An internal
  audience is not asked about the price of entry and is asked instead who inside
  the company commissioned the event; an external one is asked about partners as
  sides with goals of their own.
- **default:** The relationship the archetype the brief suggests implies. Where
  the brief suggests none, carry it as an unknown rather than as internal.
  Marked as an assumption on `audience_relationship`.
- **cs:** „Jsou účastníci vaši lidé, tedy zaměstnanci nebo vaše obchodní síť, nebo zvete klienty, partnery a veřejnost? Případně obojí?“
- **en:** "Are the attendees your own people, meaning employees or your sales network, or are you inviting clients, partners and the public? Or both?"
- **skip_if:** The brief says what the attendees are to the organizer, which is
  almost always. The question is therefore rarely asked and its use is the
  branch it opens; where the answer is missing, QB-02 and QB-14 both stay in
  play and nothing is switched off.
- **source:** V6-R05, V6-R13, kb.cs.07.01, kb.cs.07.02

## Ordering

Ask in this order when several are open, because each one narrows the next:
`goals_per_side`, `success_measure`, `audience_relationship`, `access_model`,
`format`, `paid_or_free`, `partners`, `networking_purpose`, `after_materials`,
`after_followup_programme`, `repetition`, `agency_client_brand`, `brand_assets`.

A brief that contradicts itself on the date, the place or the number of people
(two dates, an invitation that still carries the old one) is asked about first:
one question names both values and asks which holds, never choosing quietly,
and `success_measure` waits for the next turn.

`goals_per_side` and `success_measure` go in the first turn, on every surface,
which is what the two questions a turn allows are for. Not where the person says
the brief is final and asks for it to be prepared or carried out (S4 CONFIRM):
then neither is asked, goals the brief states are confirmed outcomes, and a
missing measure is carried by its default. `goals_per_side` is asked
whenever the brief does not say what the event is meant to lead to for the
organizer and for the people coming; a sentence about what has to work, what a
tool has to do, or what should remain after the event is not that. No item after `success_measure` moves ahead of it, however urgent the brief's timing
makes it look. Where the brief names a pain, an outcome or a past problem, both
questions open with the candidate read from it („Z briefu čtu, že…“, "From the
brief I read that…") and ask whether it fits, so the person confirms or corrects
instead of starting from nothing; after "I don't know" the candidate is carried as the working assumption the defaults
describe. The wording of `goals_per_side` keeps its three parts, the sides, what
each gets and the feeling people leave with, however the sentence is shortened.

`access_model` and `format` are asked only from the "frame known" moment on and
only where the brief leaves them open; at "intent only" both are assumed and
named as assumptions.

Assumed by default, never a question in their own right: `existing_systems`,
`groups_with_different_content`, `live_changes`, `after_recording`,
`after_contacts`. Each carries `ask_only_if`; outside that case the default
applies, the card says `unasked` and the story shows the assumption.

`agency_client_brand` moves to the front the moment the brief mentions a client, a
brand that is not the person's employer, or a pitch. `brand_assets` stays last
and moves for nothing: a question about a logo asked before the goal, the
audience and the scale are settled reads as the wrong priority, and its answer
changes only how the finished story looks.

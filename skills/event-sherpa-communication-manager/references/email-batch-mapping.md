# From a message to an e-mail draft

The admin's MCP saves an e-mail as an unsent draft of the E-mail campaigns
module: `prepare_event_email_batch` previews it, `save_event_preparation`
saves the requested private draft without another confirmation and
`get_event_email_batch` reads it back. Nothing in this path sends, schedules
or queues an e-mail. Sending and scheduling use their own concrete approval
and a supported confirmation tool, otherwise they remain manual.
Communicate writes nothing itself; this page says
how one message of a `communication_plan-v1` becomes the input of
`prepare_event_email_batch` when the organizer asks for a draft.

## Which messages convert

Only a message whose `module` is `email-campaigns`. Refuse the others and
point at their `blocked_operations` entry:

- `invitation-email`: use a tool offered for the Invitation e-mail and its
  own contract, or leave it to a person in the administration.
- `confirmation-email`: use a tool offered for the Confirmation e-mail and
  its own contract, or leave it to a person in the administration.

A message with an open slot (`text: null`) does not convert until a person
approves its text. A message listed in the `refs` of a story change does not
convert until a person approves that change; the story changes themselves are
never written, only shown next to the preview.

## Mapping

| `prepare_event_email_batch` | From |
|---|---|
| `event_id` | the authorized target event; never from the plan |
| `language` | `language` of the plan |
| `subject` | text of `subject_ref` |
| `body` | texts of `body_refs` in order, joined with one blank line |
| `group_ids` | the real ids of the message's `audience.groups`, read from an authorized result; never inferred from a name. `[]` when the audience names no group |
| `send_type` | `audience.state`, one state per message, matching the status buttons on the campaign's Sending tab: `all` → `all` (Všichni / All, includes the event's administrators), `registered` → `registeredAttendees` (Registrovaní / Registered), `not_invited` → `noInvited` (Nepozvaní / Not invited), `no_reaction` → `invitedNoReaction` (Bez reakce / No reaction), `unread_invitation` → `unread` (Nepřečetli zvací e-mail / Did not read), `attended` → `came` (Účastníci na místě / Attendees on site), `viewed_web_app` → `visitedLive` (Zobrazili webovou aplikaci / Viewed web app), `not_viewed_web_app` → `notVisitedLive` (Nezobrazili webovou aplikaci / Did not view web app). `registeredAttendees` and `invitedNoReaction` leave out the event's administrators; every other segment may include them, so say so |

**A state is never a group.** Target a state only through `send_type`.
Never create, propose or pick a group (such as "everyone", "registered" or
"all attendees") to stand for a state, and never ask the organizer to make
one. Groups narrow a state only when the plan's audience names a real
group of the event; otherwise `group_ids` is `[]`.

Refuse instead of trimming or guessing when:

- the subject is longer than 250 characters, has a line break, or is empty;
- the body is longer than 10 000 bytes in UTF-8 or empty;
- a text contains HTML (the body is stored as plain text and HTML is escaped,
  so tags would show as text), a `::PLACEHOLDER::`, or a character outside the
  basic Unicode plane such as an emoji;
- a group of the audience has no id from an authorized read, or an id is
  given for a group the audience does not name;
- more than 50 groups would be sent;
- a `verbatim` subject or body part has whitespace or a blank line at either
  end, or a carriage return: the draft stores texts trimmed with plain line
  breaks, so the approved text would change. Fix the source text, or a person
  changes its authority; never trim it quietly. Proposals and editable texts
  are trimmed.

Placeholders such as `::UZIVATEL_JMENO::` stay out of the body for now:
whether they survive the draft path into the sent e-mail is not verified. If
a message needs a personal greeting, the QR code or another placeholder, list
it as a manual step.

## When the preview refuses

The administration checks the draft again and refuses it, among other cases,
when the language is not one of the event's languages, when the event has
more than 1000 assigned users, when a group is not available to the person,
or when the selection holds an invalid or duplicate e-mail address. Say what
was refused in plain words and that the message stays a manual step in E-mail
campaigns. Do not change the language, the groups or the text to get around a
refusal.

## What the draft does not carry

The saved draft has the registration button hidden, no ICS file, no PDF
ticket and no header image of its own, and without `send_type` it targets everyone
assigned to the event or to the chosen groups, administrators included. A person finishes the rest in the
administration, in the E-mail campaigns module:

- any attendee state other than registered and invited with no reaction
  (`audience.state`, for example Attended or Unread invitation); the draft
  filters only those two;
- the registration button, its text and where it leads (`cta.link_type`);
- the ICS file or PDF ticket (`attachments`);
- the content in every other language of the event; the administration does
  not send a campaign with a language missing;
- any placeholder;
- sending or scheduling (`timing`); a scheduled send is not a sent one and a
  sent one is not a delivered one.

## Check the audience and report the saved draft

Check the subject, body, language and groups the preview returns against the
requested draft. If the actual audience differs, keep the draft unsaved and
explain the mismatch. After a successful save, say plainly:

1. How many recipients the draft reaches (`recipient_count` from the preview),
   and whom, in words, by the name of the send button its `send_type` matches
   ("Registered", "No reaction", "Not invited" …), and whether the event's
   administrators are left out; with groups, only the people of that state
   inside those groups. Never the `send_type` value itself.
2. When neither `send_type` nor `group_ids` narrows it: the draft reaches
   every eligible user of the event, administrators included. An empty list
   is not an empty audience.
3. That saving the draft sends nothing, and which manual steps above remain.
4. That the saved campaign is Not scheduled (Nenaplánováno) and the
   organizer can edit it in the admin or through the chat.

Save only the current matching preview, with its `operation_id` and
`proposal_hash`. A changed text, group or recipient count needs a new preview;
a change outside the agreed scope needs a new decision. A legacy confirmation
tool still requires the explicit consent its contract specifies; do not invent
consent to use it for a draft. Before sending (including a test), scheduling,
deleting or making an immediately visible change, show the concrete content,
audience, timing and effects and obtain explicit approval. Report only
`verification: verified` from `get_event_email_batch` as a saved draft.

## Invitation e-mail is not a campaign

The Invitation e-mail and the Confirmation e-mail live in their own
modules; their ids are never a campaign `template_id`, and the campaign
tools never read, test or send them. A refusal after such a mix-up is your
mistake, not a fault of Happenee.

## Send dates

A send date from the plan is a proposal until the campaign is scheduled
with its own approval. Next to a saved campaign write it as "proposed
date, Not scheduled" („navržený termín, Nenaplánováno“), never next to
"saved" as if it were set.

## Test e-mail

Offer a test e-mail through the connection only when the connection lists
`preview_event_email_test` for this event and its preview does not refuse.
Where it is missing or refused, never promise one and never send the
campaign to a small group or to the organizer as a substitute: say that the
organizer sends the test to themselves from the admin (Individual sending in
the e-mail's detail), in every language of the event.
Say you tried a test only when you called the test tool; reading the
e-mail is not an attempt.

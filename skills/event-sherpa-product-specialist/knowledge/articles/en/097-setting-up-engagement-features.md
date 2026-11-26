# Setting up engagement features

> Polls, Questions, Survey, and Registration information in the event administration — where you turn them on, when each one fits, and how to read the results.

- Article in the Help Center: https://help.happenee.com/en/articles/97-setting-up-engagement-features
- Česká verze: https://help.happenee.com/cs/articles/97-nastaveni-engagement-funkci
- Collection: Content and attendee experience
- Updated: 2026-09-08

---

> [!info] Overview
> **Engagement** is the section in the event's left-hand menu where you turn on the features that get attendees involved in the attendee app. This article covers four of them: **Polls** (interactive polls and contests), **Questions** (audience questions), **Survey** (feedback, opinions, follow-up questions), and **Registration information** (attendee details submitted during registration). The section offers nine in total; the other five are documented elsewhere, and the map to them opens the Details below. Engagement features appear in the attendee app, not on the microsite.

## Getting started

- Add a feature in the **Engagement** section with **+ Add** and pick it from the list.
- Each of these four features can be added to an event **only once**. The Online module is the only one you can add several times.
- Decide first **what level you are asking at**. Polls and questions that belong to one talk are set on that session in the Agenda, not here — see *Three places where the same names appear* below.
- Decide **who operates the feature during the event** — who publishes each poll, who moderates the questions, and who sends the Notification that points people to the survey. Without an owner, the feature sits empty in the app.
- Both Polls and Survey become visible in the app **only after you add the answers and publish**. You can prepare them in advance and leave them unpublished.

## Details

### The nine features in the menu and where to read about them

**+ Add** offers nine engagement features. Four are covered in this article; the other five have their own:

- **QR ticket** — *Check-in attendees and print badges*. Attendees carry their ticket in the app, and the link on the card opens *On-site check-in*. See [How check-in and QR-code scanning work](https://help.happenee.com/en/articles/47-how-check-in-and-qr-code-scanning-work).
- **Guest QR code** — *QR code for the guest selected in the registration form*. It appears only when the form asks about companions; you set that up in [Setting up the Registration form](https://help.happenee.com/en/articles/13-setting-up-the-registration-form).
- **Notifications** — *In-app announcements and push notifications*. See [Using Notifications in the attendee app](https://help.happenee.com/en/articles/46-using-notifications-in-the-attendee-app).
- **Polls** — *Interactive polls and contests*. Below in this article.
- **Questions** — *Audience questions*. Below in this article.
- **Survey** — *Feedback, opinions, follow-up questions*. Below in this article.
- **Attendees** — *Networking and meetings*. See [How Networking works](https://help.happenee.com/en/articles/36-how-networking-works).
- **Registration information** — *Attendee details submitted during registration*. Below in this article.
- **Online module** — *Livestream, video, 3D, social wall, games*. See [Using the Online module](https://help.happenee.com/en/articles/38-using-the-online-module).

### Three places where the same names appear

*Polls* and *Questions* show up in three different places in the administration. They are not one feature displayed three times — they are separate objects with their own settings and their own set of responses:

- **Engagement features at event level** (this article) — one poll or one question queue for the whole event. It is not tied to a session or a stage. This fits simple and online events with one room and one track.
- **Engagement on a session** — on a session type and on an individual session, the **Engagement** tab turns on **Session rating**, **Questions**, **Anonymous questions**, and **Polls**. Attendees ask about the talk they are watching and find it on the session detail in the Agenda or in My Agenda. For a conference with parallel rooms, this is the right route.
- **Interactive tabs inside an Online module** — each Online module instance has its own chat, questions, anonymous questions, and polls next to the livestream. They belong to watching that stream, not to the event as a whole.

When you are unsure, ask what the question is about: the whole event, one talk, or one stream.

### Polls

A poll is a quick vote during a talk — one question, a set of answers, a result within seconds. Use it to get a room talking, to take a rough measure ("how many of you already run this?"), or to run a contest.

In the **New poll** dialog you fill in the **Question or poll title** and pick an answer template:

- **Custom answers** — you write the options yourself.
- **Answers Yes / No** — two prefilled options.
- **Rating 1 up to 5** — a scale you do not have to type out.

You can add an **Additional description** when the question alone is not enough.

A poll has a publication state. Until you publish it, attendees do not see it in the app. Prepared but unpublished polls are the normal way to set up a whole block the day before. You can also change states with **Bulk change status**.

Open the **Results** on an individual poll. You get charts and can open them in a new tab — that view is the one you put on the screen in the room. **Results (Excel)** downloads the whole set of responses, and **Edit results** lets you change them, for example to add a vote for someone who voted on paper.

**Attendees do not see the results until you publish them.** That is deliberate: while a poll is running, a partial result should not shape how people vote.

### Survey

A survey is the longer form — more questions, different answer types, collected during the event and after it. Two typical uses: an evaluation at the end of the event, and collecting information you need from people and did not get during registration (dietary requirements, interest in a follow-up workshop, T-shirt size).

For each question (**+ New survey question**), the **Select user response** field offers five types:

- **Answer in own words** — free text.
- **Select one only** — exactly one of the offered answers.
- **Select one only or enter custom text** — one answer, or the attendee writes their own.
- **Can select multiple** — any number of the offered answers.
- **Can select multiple and enter custom text** — several answers plus a custom addition.

A question can carry an **Additional description** when its wording alone is not enough. The **Answer** field decides whether attendees can come back and revise: **Can be changed** or **Cannot be changed**.

A survey has three states — **Unpublished**, **Published**, and **Closed**. Attendees can still see a closed survey but can no longer answer it, which ends the collection more cleanly than deleting it. You can also switch states with **Change status in bulk**.

**Results** appear as charts, you open them in a new tab, **Results (Excel)** downloads the whole set, and **Edit results** lets you add or correct answers for an individual attendee. If you restricted the survey to a group, the results show that group only.

**Poll or survey:** a poll is one question in real time with the result on a screen. A survey is a set of questions that attendees fill in at their own pace and whose results you read after the event.

### Questions

The card in the Engagement section is called **Questions** and collects what the audience wants to ask a speaker or a panel across the whole event. This fits online events and simpler formats with a single room. With parallel tracks, questions on individual sessions are the better choice.

The feature has two tabs: **Questions** for the queue itself and **Settings** for three toggles.

**Moderation.** The queue is split into **Active**, **Pending moderation**, and **Archived**, with a count on each tab. You work with an individual question straight from the list — archive it, delete it, or mark it as the main one; **Archive all** clears the queue at once. You can also add questions from the administration with **+ New question**, which helps when a question reaches you outside the app. The **Approving questions before public viewing** toggle decides whether a question goes straight out or waits for moderation first.

**Allow anonymous questions.** A separate toggle for the whole feature. Anonymity makes people readier to ask uncomfortable things, but you cannot see who asked.

**Allow asking questions in the web app without signing in.** Attendees submit a question without logging in to the attendee app, using the link shown on the projection screen and the **code** you set here. This is useful for guests who are not on the attendee list.

**Display options** offers four views for different people at different screens:

- **Display for projection** — the view for event production: submit questions, organize them in a queue, mark them answered, like them, and archive them.
- **Show for projection with streams** — the same, with questions in a format suited to projection alongside the stream.
- **Show main question on projection** — shows only the one question you marked as primary.
- **Show question queue** — the speaker's view; it holds the questions added to the queue from the stream view.

**Export results to Excel** downloads the questions.

### Registration information

Registration information is a different kind of thing from the other three: it **collects nothing**. It gives attendees one place in the app to see what they submitted during registration, so they can check it whenever they want. It removes questions like "did I sign up for that workshop or not?".

The whole setup is a single field: the module description attendees see on the event home screen. The default text reads *Your data entered during registration* and you can rewrite it.

Registration information has no results and no export of its own — it is a view of data that already exists in the event. You export registration answers from the *Registration* screen and from reporting, not from here.

### What applies to every engagement feature

- **Group visibility** is set on the individual feature, not centrally, and the feature card shows it. A survey visible only to the *Production* group is a common way to collect internal feedback separately from attendees.
- **Order and publication in the app** are handled in the left-hand menu under **Attendee app**, not under Engagement. That is also where you decide whether the feature appears on the home screen as a text block or an image.
- **Rename and delete.** The feature card carries two buttons. **Change name** rewrites the default label — *Polls* to *Vote for the best talk*, *Survey* to *Conference evaluation* — and the new name carries through to the app home screen.
- **An empty feature looks worse than a feature you left off.** If you have no question for a poll and no prize for a contest, do not turn them on yet; add them later.

## Common pitfalls

### The feature is added, but attendees do not see it in the app

Polls and surveys are visible only after you add the answers and publish. Check the publication state, then check the **Attendee app** section — a feature can be ready and still unpublished in the app. The third common cause is a visibility restriction to a group the attendee does not belong to.

### The organizer expects attendees to see poll results right after voting

They do not. Results reach attendees only when you publish them, typically by opening **Results** in a new tab and putting that view on the screen in the room. If you want people to see how the room voted, someone on stage has to make that happen.

### Audience questions run without a moderator

An unattended queue is worse than a feature left off — people ask and nobody answers. Before you turn questions on, decide who watches them while the agenda runs and agree with the host where they pick questions up. For larger events, require approval before questions are shown publicly.

### A poll is created at event level when the question belongs to one talk

An engagement feature at event level is not tied to a session. If you are asking about the content of one talk, the question belongs to that session; otherwise people who sat in another room answer it too, and the result tells you nothing.

### Anonymous questions are on, and then someone needs to know who asked

The toggle applies to the whole feature, and for questions sent anonymously you cannot trace the author. Decide in advance whether openness or follow-up matters more for this event.

### A survey question keeps the default *Can be changed* when it is a contest or a binding choice

The default lets attendees rewrite their answer at any time. That is fine for an evaluation; for a contest question, or a choice you order something against, switch it to *Cannot be changed*.

### The survey reaches people who were not at the event

Anyone who opens the app can see the survey. If you want feedback from the people who showed up, restrict visibility to a group based on attendance status and point people to the survey with a Notification. Otherwise you collect ratings from people who never experienced the event.

### A survey has no intro text of its own

The administration has no field for a paragraph in front of the questions; the survey opens with the first one. Carry that context another way: through the feature name under *Change name* (*Survey* to *Conference evaluation*), through the **Additional description** on the first question, and through a Notification that points people to the survey.

## Related articles

- [Using the Online module](https://help.happenee.com/en/articles/38-using-the-online-module)
- [How session types work](https://help.happenee.com/en/articles/27-how-session-types-work)
- [How the attendee app and its home screen work](https://help.happenee.com/en/articles/34-how-the-attendee-app-and-its-home-screen-work)
- [Using Notifications in the attendee app](https://help.happenee.com/en/articles/46-using-notifications-in-the-attendee-app)
- [How Networking works](https://help.happenee.com/en/articles/36-how-networking-works)
- [How check-in and QR-code scanning work](https://help.happenee.com/en/articles/47-how-check-in-and-qr-code-scanning-work)
- [Setting up the Registration form](https://help.happenee.com/en/articles/13-setting-up-the-registration-form)

# Setting the primary language of an event

> The primary language is the fallback for attendees outside the added languages and cannot be changed after the event is created.

- Article in the Help Center: https://help.happenee.com/en/articles/10-setting-the-primary-language-of-an-event
- Česká verze: https://help.happenee.com/cs/articles/10-nastaveni-primarniho-jazyka-udalosti
- Collection: Event setup and registration
- Updated: 2026-04-27

---

> [!info] Overview
> The primary language of an event is the **fallback language** shown to an attendee whose device language is not among the languages you have explicitly added to the event. The choice of primary language is irreversible — once the event is created it cannot be changed without starting a different event. For events with international attendees, the recommended primary language is **English**.

## Getting started

- Before you create the event, decide whether you expect international attendees.
- If yes, set the primary language to **English**, even if the main content language is Czech.
- Add secondary languages (Czech, Slovak, others) according to which languages you want the content in.
- Make this decision when the event is created — you cannot change it later.

## Details

### How the language choice works for the attendee

An attendee opens the microsite or the attendee app with some device language setting. Happenee checks whether the event has content in that language:

- **Yes** — the content is shown in that language.
- **No** — the content is shown in the event's **primary language**.

So the primary language does not decide which language you fill content in — content is filled in for each added language separately. The primary language decides what is shown to attendees whose language you have not added.

### A practical example

You are running a conference in Prague with international guests. You plan to create the content in **Czech** and **English**. You also expect attendees whose phones are set to German, Spanish, or Italian.

- **Primary language = Czech** (wrong): attendees with their phone set to German, Spanish, or Italian see Czech content. Unusable for them.
- **Primary language = English** (correct): the same attendees see the English content, which they can understand.

Rule of thumb: **if the event has international attendees, set the primary language to English**. Add Czech as a secondary language. Czech-speaking attendees see Czech, everyone else sees English.

### Why the decision is irreversible

The primary language is part of the event's underlying data structure. Content features, the Registration form, e-mails, the microsite — every piece is created with a reference to the primary language. Happenee does not allow it to be changed retroactively, because that would break the integrity of the content.

> The primary language is set when the event is created and **cannot be edited** later. If you realize you chose the wrong one, you have to create a new event.

### How the primary language differs from secondary languages

When you edit content in the admin, you switch between languages with the **two flags** in the top-right corner. Secondary languages can be added and removed freely in **Event settings → Language settings**. The primary language appears in this setting marked as **"Primary language — cannot be edited"** and stays there permanently.

If you do not fill in content for a secondary language, the system uses the primary language for that piece of content. That is also why it makes sense to pick the broadest possible primary language (typically English) — it protects you from showing an attendee an empty piece of content.

## Common pitfalls

### Primary language = Czech for an event that international guests will attend — a German guest opens the microsite and sees Czech content even though the event has an English version

For events with international attendees, set the **primary language to English**. Add Czech as a secondary language. The same applies to Slovak events — if guests from other countries might come, the primary language should be English.

### The organizer notices the wrong primary language only after the registration link is already published

The primary language cannot be changed. The only option is to create a new event and move the previously registered attendees over. Make the decision when the event is being created.

### Content filled in only in the primary language, even though attendees with that device language are in the minority

Primary language does not mean "main content language" — it means "fallback for every unknown language". Fill in the content in every language you want to offer. Use the flag in the top-right corner of the event admin to switch the language while editing.

## Related articles

- [Creating a new event](https://help.happenee.com/en/articles/9-creating-a-new-event)
- [What to set up first after creating an event](https://help.happenee.com/en/articles/3-what-to-set-up-first-after-creating-an-event)
- [Managing contacts and groups in your workspace](https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace)
- [What to do when a campaign will not send or arrives in the wrong language](https://help.happenee.com/en/articles/88-what-to-do-when-a-campaign-will-not-send-or-arrives-in-the-wrong-language)

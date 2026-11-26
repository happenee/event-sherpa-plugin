# What to do when a campaign will not send or arrives in the wrong language

> A recipient got the campaign in a language they do not read, or the campaign cannot be sent because a language version is missing. Why it happens and how to fix it.

- Article in the Help Center: https://help.happenee.com/en/articles/88-what-to-do-when-a-campaign-will-not-send-or-arrives-in-the-wrong-language
- Česká verze: https://help.happenee.com/cs/articles/88-co-delat-kdyz-kampan-nejde-odeslat-nebo-prisla-v-jinem-jazyce
- Collection: Troubleshooting
- Updated: 2026-09-23

---

> [!info] Overview
> A campaign with an empty language version does not go out: if any event language is missing a subject or content, the *Campaign is not ready to send* dialog identifies the missing field and stops the real mailing. A test checks only the selected language. When a recipient reports an e-mail in a language they do not read, they may have received the event's primary language because their contact has no preferred language set or has a language that is not among the event's active languages.

## Getting started

Open the campaign and check on the **Mailings** tab whether a mailing was created at all. If it was, open **E-mails** for it, find the recipient's address, and expand the row. You see the e-mail exactly as it went out to that person, including the language version.

## Details

### A campaign with a missing language is not sent

A campaign goes to each recipient in their preferred language, so every event language needs its own subject and content. The administration checks this for an immediate mailing, a mailing scheduled for a later date, and a resend to newly assigned contacts. When a language is incomplete, the *Campaign is not ready to send* dialog names each affected language and says whether its subject, content, or both are missing. No mailing is created.

Close the dialog with **Close**. On the **Content** tab, switch **Content language** to the named language and complete the missing **E-mail subject** or e-mail content; if the campaign uses a registration button, write the button text in that language too. Then send or schedule the campaign with the same button as before.

It happens most often on events where a language was added partway through preparation. Campaigns drafted while the event had one language do not have the second version.

### Why a recipient got the e-mail in another language

A contact with no preferred language set, or with a language that is not among the event's active languages, gets the campaign in the event's primary language. To see how many such contacts there are, check the *Users' default language* breakdown in **Contacts assigned to the event** on the **Sending** tab. Fill in their language in contact management.

You cannot recall sent e-mails or rewrite their text. If the information has to reach these people again, fill in their language first, copy the campaign with **Copy**, and send the copy targeted only at the group they belong to. On a small event with few recipients, one short message is usually cleaner.

## Common pitfalls

### A test in the second language cannot be sent

A test in the selected language is blocked if its subject or content is missing. The dialog names the language and missing field. Another incomplete language does not block this particular test, but every event language must be complete before a real mailing. If a test did arrive in an unexpected language, check the language selected for the test and preview the sent e-mail under **Mailings**.

### The campaign targets only Czech contacts, and the administration asks for English

Every event language has to be filled in, even when the campaign targets a group that reads only one language. The *Users' default language* breakdown shows how many recipients have which preferred language.

## Related articles
- [Creating and sending an E-mail campaign](https://help.happenee.com/en/articles/41-creating-and-sending-an-e-mail-campaign)
- [Setting the primary language of an event](https://help.happenee.com/en/articles/10-setting-the-primary-language-of-an-event)
- [Targeting communication by groups and statuses](https://help.happenee.com/en/articles/43-targeting-communication-by-groups-and-statuses)

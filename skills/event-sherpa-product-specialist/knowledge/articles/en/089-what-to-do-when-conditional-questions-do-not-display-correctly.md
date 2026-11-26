# What to do when conditional questions do not display correctly

> A follow-up question never appears, or it appears to everyone. Where to look for the cause and why late changes do not apply to answers already submitted.

- Article in the Help Center: https://help.happenee.com/en/articles/89-what-to-do-when-conditional-questions-do-not-display-correctly
- Česká verze: https://help.happenee.com/cs/articles/89-co-delat-kdyz-se-podminene-otazky-nezobrazuji-spravne
- Collection: Troubleshooting
- Updated: 2026-08-07

---

> [!info] Overview
> A follow-up question either never appears to the attendee or pops up for everyone. Both come down to how the link between a specific **answer** and the follow-up question is configured — not to a fault in the form as a whole.

## Getting started

Open the form in preview and go through it as an attendee: pick the answer that is supposed to trigger the follow-up question. The preview shows real behavior faster than checking settings does.

## Details

### The question does not appear

The most common causes, in the order worth checking:

1. **The link points at a different answer than you think.** The condition attaches to a specific answer, not to a question. If you renamed answers after configuring it, or added a new one, the link may point elsewhere.
2. **The follow-up question is hidden.** Check its visibility — a hidden question does not appear even when the condition is met.
3. **The question is restricted to a group** the attendee does not belong to. Visibility by group and the answer condition stack: both have to be satisfied.
4. **The second language version is missing.** A question with no text in the second language effectively does not appear to attendees using it.

### The question appears to everyone

That means the condition is not set, or it was lost while the answers were edited. Open the follow-up question and confirm it is linked to a specific answer — without that link it is an ordinary question for everybody.

### Late changes do not apply to existing answers

When you add a condition or a group assignment after the form has gone live, it **does not apply retroactively**. People who registered earlier stay without the follow-up question and without the group. You have to fill that in manually, with a bulk assignment in Contacts and groups.

## Common pitfalls

### Testing the form from the admin instead of the attendee's side

In the admin you see every question, including hidden and conditional ones. The behavior an attendee will see is only verified in the preview or by an actual registration. Always test both language versions.

### Chaining conditional questions too deep

A question conditioned on an answer that is itself conditioned on another answer is hard to debug and confusing to the attendee. When you need more than two levels, it is usually cleaner to split the audience with groups and run two simpler forms.

### A required conditional question blocking submission

If the follow-up question is required and for some reason does not display correctly, the attendee cannot submit the form and will not understand why. For conditional questions, consider whether they need to be required at all.

## Related articles
- [How conditional questions work in the Registration form](https://help.happenee.com/en/articles/14-how-conditional-questions-work-in-the-registration-form)
- [Setting up the Registration form](https://help.happenee.com/en/articles/13-setting-up-the-registration-form)
- [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility)

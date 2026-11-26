# How to fix things after the fact

> A switchboard of what can still be fixed once registration is open and what cannot — groups, form answers, registration type, billing details, capacity.

- Article in the Help Center: https://help.happenee.com/en/articles/94-how-to-fix-things-after-the-fact
- Česká verze: https://help.happenee.com/cs/articles/94-jak-opravovat-veci-ex-post
- Collection: Troubleshooting
- Updated: 2026-09-16

---

> [!info] Overview
> Registration is open and you have discovered something is set up wrong. Most things can be caught up on, but **almost nothing applies retroactively** — new rules take effect from the moment you introduce them, and older data has to be evened out by hand. This overview says where to expect manual work and what can no longer be fixed at all.

## Getting started

Before you change anything, find out **how many people it affects**. With five registrations a manual fix is a matter of minutes; with five hundred it is the reason to pick a different approach.

## Details

### What can be fixed with manual work

- **Group assignment** — groups can be assigned in bulk in Contacts and groups. Automatic assignment by a form answer, however, applies **only to new answers**; existing ones are not backfilled into the group.
- **A missing preferred language** — fill it in on the contact or by import. It does not affect e-mails that already went out.
- **A new custom contact field** — you can create the field any time, but it stays empty for earlier registrations. Fill it in manually or by import.
- **Billing details** — a correction overwrites the details on the order's existing invoices under the same number. No new invoice is created, so if the buyer already received the invoice by e-mail, send them the corrected one yourself.
- **Session capacity** — you can raise it any time. Lowering it below the number already signed up does not cancel anyone's registration.
- **Attendee status** — it can be switched by hand in the *Registration* section (to *Not attending* after a phone call, for example).

### What cannot be fixed

- **Sent e-mails.** You cannot rewrite the text or a link in a message that has gone out. When the mistake matters, you can send a correction targeted at the affected group only.
- **A completed campaign mailing.** Only a mailing that is still running can be deleted.
- **Optional consents for earlier registrations.** A consent added later does not cover people who registered before it; you have to approach them separately.
- **The event's primary language.** It cannot be changed once the event is created.
- **Missing data from automatic registration.** Someone who never went through the form has no answers — the only route is to ask them afterwards.

### When starting over is cleaner

For a campaign, copying usually beats fixing: **Copy** → edit → send to the right segment. For the event itself that rarely applies, because a copy carries neither registrations nor contacts.

## Common pitfalls

### Treating an after-the-fact fix as finished

Assigning a group in bulk is one action, but it only covers the people who are in the system **at that moment**. Anyone registering tomorrow will not land in the group unless you also set up automatic assignment. So after a manual fix, always add the forward-looking rule too.

### Making the fix without a backup

Before a bulk action over hundreds of contacts, export the current state. When a bulk change lands somewhere other than you intended, that export is the only way back.

## Related articles
- [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility)
- [Setting up the Registration form](https://help.happenee.com/en/articles/13-setting-up-the-registration-form)
- [Recommended order for setting up an event step by step](https://help.happenee.com/en/articles/8-recommended-order-for-setting-up-an-event-step-by-step)

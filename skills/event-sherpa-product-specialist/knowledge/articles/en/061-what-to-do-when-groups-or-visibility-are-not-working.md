# What to do when groups or visibility are not working

> What to do when attendees do not see content they should see, or see content they should not.

- Article in the Help Center: https://help.happenee.com/en/articles/61-what-to-do-when-groups-or-visibility-are-not-working
- Česká verze: https://help.happenee.com/cs/articles/61-co-delat-kdyz-skupiny-nebo-viditelnost-nefunguji
- Collection: Troubleshooting
- Updated: 2026-07-22

---

> [!info] Overview
> Attendees do not see content they should see, or they see content they should not. The most common cause is that the group structure was not thought through before registration opened — and after the fact, it has to be patched manually. *If you do not do it at the start, after the fact you basically cannot* applies to Happenee fairly precisely.

## Getting started

Open the contacts and groups section and check how many people are actually in *the group you are targeting*. If the number is lower than expected, the problem is in the assignment — not in the visibility setting.

## Details

### Typical causes

- **The group was not created before registration opened.** Automatic assignment (via a form answer, a ticket, a discount code, a nominator) only works going forward — existing registrations are not pulled into a newly created group on their own.
- **A feature's visibility is set to a group the attendee is missing from.** The feature is then *hidden* for them, and the organizer thinks the app is broken.
- **Expecting automatic system groups** (for example *Confirmed attendees*, *Not registered*). Today only **Global groups** are available; Local groups and System groups are planned. To distinguish by status, use the filter in attendee statistics or in campaign targeting.
- **Expecting Local groups tied to one event.** All groups today are **Global, at workspace level** — there are no groups that belong to a single event. Local groups are planned.

### How to fix it

- **Manually assign attendees** to the right group in the contacts and groups section (action *Add or remove from groups*).
- **Check the visibility setting** on the content or engagement feature in question — either open it to all attendees, or verify the target group has the right members.
- **Resend the campaign or invitation e-mail** with updated targeting — for an already-sent campaign, use the **Resend campaign to newly assigned** panel and the **Newly assigned** button on the **Mailings** tab.
- **For a feature that only some attendees should use**, consider keeping the feature off and turning it on once the group is populated, instead of relying on group visibility.

### Prevention

- Before opening registration, walk through the list of groups you will need — for communication targeting, content visibility, and reporting filters.
- For one-off groups, name them with an event prefix (for example `Conference25_VIP`) so groups from different events do not mix.
- The detailed logic of groups and visibility is described in *Working with groups and visibility*.

## Common pitfalls

### The organizer expects a *Confirmed attendees* group to be created automatically after registration

System groups are not available today (the feature is planned). Instead of a group, use the registration status filter — both in attendee statistics and in campaign targeting.

### The group was created after registration opened. The organizer expects existing attendees to be pulled in retroactively

Automatic assignment via a form answer, a ticket, a discount code, or a nominator only applies to new registrations and answers. Add existing members manually in the contacts and groups section. **The exception is group assignment on a session or its type** (the *Assign attendee to a group after registration* setting): there, turning it on also adds the group to attendees who are already registered, and turning it off removes it again — even from attendees who also hold it from another source.

### Invitation e-mail targeted to a group — and the option is not there

The Invitation e-mail does not support targeting by groups (only by status: *Not invited*, *Not responded*, *Did not read the invitation e-mail*). For group targeting, use an **E-mail campaign**.

## Related articles

- [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility)
- [Managing contacts and groups in your workspace](https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace)
- [How conditional questions work in the Registration form](https://help.happenee.com/en/articles/14-how-conditional-questions-work-in-the-registration-form)

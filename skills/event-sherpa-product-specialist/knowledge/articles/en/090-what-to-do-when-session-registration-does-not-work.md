# What to do when workshop or session registration does not work

> The attendee cannot see the sign-up button for a session, or the registration will not go through. The settings and situations that cause it most often.

- Article in the Help Center: https://help.happenee.com/en/articles/90-what-to-do-when-workshop-or-session-registration-does-not-work
- Česká verze: https://help.happenee.com/cs/articles/90-co-delat-kdyz-nefunguje-registrace-na-workshop-nebo-session
- Collection: Troubleshooting
- Updated: 2026-09-16

---

> [!info] Overview
> An attendee says they cannot sign up for a workshop — either they cannot see the button, or the system will not let the registration through. The cause is almost always the session's visibility, whether registration is enabled, the registration time limits, exhausted capacity, a registration block limit, or a time overlap with another registration.

## Getting started

Ask the attendee **what exactly they see**: is the button missing, or does the registration fail to complete? That single answer splits the causes into two groups and saves half the search.

## Details

### The sign-up button is not visible at all

- **The session is not visible to the group** the attendee belongs to. Check the visibility of both the session and its type — the setting exists at both levels.
- **Session registration is not enabled.** Without it, the session is only an item in the agenda; the attendee can save it to My Agenda but cannot sign up for it.
- **The session is hidden.** The *Hidden* status means the attendee does not see it at all.
- **Registration has not opened yet, or it has closed.** When the session has **Registration time limits** turned on, the button is replaced by *Registration will open on* with a date and time, or *Registration closed on*. Check the window on the session and on its type — the setting exists at both levels.

### The registration does not go through

- **Capacity is full.** There is no wait list in Happenee, so once a session fills up, signing up is not possible.
- **A registration block limit.** A block caps how many sessions from a given set an attendee can join. If they used the limit elsewhere, the system will not let them into another session — even one with space left.
- **A time overlap with another registration.** By default, an attendee cannot register for a session whose time overlaps with another session they are already registered for, even one in a different Agenda. They see the **Register** button disabled, and in a browser, hovering over it shows the reason *You already have a registration for another session at this time.* Find out what they are registered for at that time and check the Agenda **Settings**. For sessions from different Agendas, **Allow concurrent registrations across Agendas** has to be on in both.
- **An incomplete event registration.** Someone who has not completed their registration for the event has nothing to sign up from.

### The attendee cannot cancel

After the **Session cancellation** deadline, the *Cancel registration* button disappears and the attendee sees *Cancellation closed on*. From then on, only an organizer can cancel the registration in the admin. With *Session cancellation* turned off, no deadline applies and the attendee can cancel at any time.

### The fastest way to verify

Open the agenda in the attendee app under a test account placed in the same group as the attendee who complained. You will see exactly what they see.

## Common pitfalls

### Checking visibility on the session only

A session inherits settings from its type. When it is switched to its own values, those apply; when it is not, the type applies. Look at both levels rather than just one.

### The attendee sees the button, but the registration is rejected

The time window is evaluated on the server. If the attendee kept the app open across the closing instant, the button stayed on their screen, but the server rejects the registration and the page refreshes. This is not a fault — check when the window closes.

### Confusing capacity with a block limit

Both prevent registration but are fixed differently. With full capacity you can raise the capacity; with a block limit you first have to cancel the attendee's registration for another session. So always confirm in the admin which of the two is actually blocking.

### The attendee signs up but the organizer cannot see them

Check whether you are looking at a different session with the same name — on multi-day events they repeat routinely. People added by hand are also marked as **Assigned by organizer**, so you can tell them from those who signed up themselves.

## Related articles
- [Setting up workshops and session registration](https://help.happenee.com/en/articles/28-setting-up-workshops-and-session-registration)
- [How registration blocks, stages, and tags work](https://help.happenee.com/en/articles/31-how-registration-blocks-stages-and-tags-work)
- [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility)

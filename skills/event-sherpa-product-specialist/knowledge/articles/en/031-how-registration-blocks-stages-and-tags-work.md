# How registration blocks, stages, and tags work

> Three mechanisms for organizing a larger agenda: registration blocks, stages, and tags.

- Article in the Help Center: https://help.happenee.com/en/articles/31-how-registration-blocks-stages-and-tags-work
- Česká verze: https://help.happenee.com/cs/articles/31-jak-funguji-registracni-bloky-mista-a-stitky
- Collection: Content and attendee experience
- Updated: 2026-09-16

---

> [!info] Overview
> **Registration blocks** bundle sessions that need registration (Workshop and Time slots types) and set **how many sessions from the block an attendee can sign up for**. **Stages** mark physical spaces (rooms, stages, booths); **tags** mark thematic categories (AI, Marketing, Leadership). All three mechanisms help you **organize a larger agenda** and **filter content** in the attendee app and on the microsite.

## Getting started

- Use **blocks** when you want to limit the choice — *the attendee picks 1 of N workshops* or *2 of 5 sessions*.
- Use **stages** for an agenda with multiple rooms or stages. Each stage has its own color and works as a filter.
- Use **tags** for thematic distinctions — tracks, difficulty levels, topics.
- Blocks, stages, and tags are created **in the Agenda tabs** (Blocks, Stages, Tags).

## Details

### Registration blocks

A block bundles sessions of type **Workshop** or **Time slots** and limits how many of them an attendee can sign up for.

**Creating a block:**

1. Go to the **Blocks** tab in the Agenda.
2. Click **+ New block**.
3. Enter a **Block name** (for example, *Morning workshops*, *Afternoon slot*).
4. On the **Settings** tab, set **Maximum number of sessions per attendee from this block** (default: 1).
5. Go to the **Sessions** tab — in the **Search sessions** field, find the sessions and add them to the block by clicking them.
6. Save.

**Typical use case:** three parallel workshops in the morning. The attendee signs up for only one.

- Workshop A, B, C — each is a separate session.
- The block *Morning workshops* contains all three.
- The maximum is 1.
- The attendee picks one in the app; once they pick, the others are blocked for them.

**Session capacity vs block.** The individual capacity of a workshop (for example, 20 spots) stays in place. The block only limits the attendee's choice; it does not touch capacity.

**One session = one block.** A session can be assigned to **only one** registration block.

### Stages

A stage marks a specific space (room, stage, booth, sector). It is assigned to sessions and works as a **filter** in the app and on the microsite.

**Creating a stage:**

1. Go to the **Stages** tab.
2. Click **+ New stage**.
3. Enter a **Stage name** (for example, *Room A*, *Main Stage*, *Workshop Room 1*).
4. Save.

**Assigning to a session:** in the session edit panel, on the **Information** tab, pick a **Stage**.

**Hiding in the app:** for a specific stage, switch the **Available in app** toggle to off. The stage stops appearing as a filter in the app (sessions assigned to it stay — only the filter attribute is hidden).

**How many stages.** The count depends on how the event is organized. For a single-room agenda, do not create stages — there is nothing to filter. For a multi-dimensional conference (3 rooms × 3 days), create one stage per room.

### Tags

A tag is a thematic label assigned to a session. Unlike a stage, it has no physical dimension — it is conceptual (*AI*, *Strategy*, *Hands-on*).

**Creating a tag:**

1. Go to the **Tags** tab.
2. Click **+ New tag**.
3. Enter a **Tag name** and a **Color** (from the list or as a hex code).
4. Save.

**Assigning to a session:** in the session edit panel, on the **Information** tab, in the **Tags** section, use the **Assign tags** field. A session can have **multiple tags**.

**Tag colors.** Tags appear in the app with their color. Pick colors that contrast on both the light and the dark background of the app.

### Filters in the app and on the microsite

The agenda automatically shows the **Type**, **Stage**, and **Tags** filters. The attendee can combine them:

- *Type: Workshop + Stage: Room A* → all workshops in Room A.
- *Tag: AI + Tag: Hands-on* → sessions with both tags (an intersection).

**Which filters and in what order** — on the Agenda's **Settings** tab there is a filter table with the **Name**, **Filter type**, and **Show filter** columns. For each filter (Type, Stage, Tags) you can:

- Turn it on or off with the toggle in the **Show filter** column.
- Reorder it by dragging the handle on the left — that is, the order of the filters relative to each other.
- Rename it with the **Name** button — attendees then see the filter under the name you set (for example, *Topics* instead of *Tags*). The name is a per-language field — you fill it in separately for each language the event supports. A language you leave blank falls back to the name from the primary language, so an English-speaking attendee can end up looking at a Czech filter name. Switch the language flag and walk through the filters in every language the event supports.

Turning a filter on or off and reordering it are saved right away; the table has no save button. Only a new name needs confirming, with **Save** in the side panel.

Hidden stages do not appear as a filter.

On the full agenda subpage, the filters sit in the right-hand column next to the session listing on a wide display. On mobile they move behind a **Filters** button next to the search field and open in a drawer, so the listing starts right below the search instead of below the whole filter panel.

The **Show filter** toggle does not govern only the filter panel in the agenda. It also decides whether **quick filters on the microsite homepage** render — the row of buttons you turn on for the agenda in *Event microsite* through the *Agenda display* dialog. The dropdown in that dialog comes straight from this table: it holds only the filters with *Show filter* on, under the names and in the order you give them here. Turn a filter off and it disappears from the dropdown, and the saved quick filter choice falls back to *Do not show*. So if you set quick filters to *Stage*, leave the *Stage* filter turned on here. See [How the Event microsite works](https://help.happenee.com/en/articles/21-how-the-event-microsite-works) for the detail.

**The order of values inside a filter** is set elsewhere — by manually ordering the rows in the relevant Agenda tab. Drag the rows (by the handle on the left) in the **Stages** tab to set the order of stages in the Stage filter, in the **Tags** tab for tags, and in the **Types** tab for types. This order carries over identically to the microsite and to the mobile and web attendee apps.

### Blocks combined with types

**Sessions of the same type in one block:** the standard case (three workshops in a block).

**Sessions of different types in one block:** technically possible, but confusing for the attendee. The recommendation: keep the block to a single session type.

### Session order

Session order in the agenda is driven primarily by **time**. When two sessions start at the same time, they are ordered by the **order of their types** — a type higher in the **Types** tab appears first (see [How session types work](https://help.happenee.com/en/articles/27-how-session-types-work)). Stages and tags only affect filtering, not how sessions are sorted.

## Common pitfalls

### A block with a single workshop — the organizer thinks it will pool the capacity

A block with one session adds nothing. Capacity is set with *Limit number of registrations* on the session, not through the block.

### A session is assigned to two blocks — the system does not allow it

A session can be in **only one block**. If you need a session to be part of more than one selection scheme, duplicate it as a separate session and put each copy in a different block (you lose some of the organizational overview).

### A stage is assigned but hidden through *Available in app*. The attendee does not see it as a filter, but sessions still show the stage in their detail

A hidden stage does not appear as a **filter**, but the assignment to the session stays. The attendee sees the stage on the session detail. If you want to remove the stage entirely, delete it.

### A tag color that is unreadable in the app's dark mode

Pick colors with enough contrast. The Happenee app supports both light and dark mode — check the tag in both.

### A block *Morning workshops* with *Maximum = 1*, but the organizer forgot to set the capacity of each workshop. A workshop fills well above a sensible capacity

The block limits the **attendee's choice**, not session capacity. Set each session's capacity individually at the session or type level.

### Turning a filter off also took the quick filters off the home page

That is deliberate. A filter you turn off disappears from the agenda and from the microsite home page alike, and the saved choice in the *Agenda display* dialog falls back to *Do not show* at the same time, so no selection is left anywhere that has no way to render. If you want the quick filters on the home page, turn the filter back on and pick the choice again under *Event microsite* on the relevant **Sessions** tab.

### Filters turned off or in the wrong order — the attendee gets lost in the agenda

On the Agenda's **Settings** tab, walk through the filters. For a conference with parallel tracks, turn on Type, Stage, and Tags. For a simple agenda, Type alone is enough.

## Related articles

- [Building the event Agenda — architecture](https://help.happenee.com/en/articles/26-building-the-event-agenda-%E2%80%94-architecture)
- [How session types work](https://help.happenee.com/en/articles/27-how-session-types-work)
- [Managing sessions](https://help.happenee.com/en/articles/69-managing-sessions)
- [Setting up workshops and session registration](https://help.happenee.com/en/articles/28-setting-up-workshops-and-session-registration)
- [How time slots work](https://help.happenee.com/en/articles/29-how-time-slots-work)
- [Setting up reservations in the Agenda — buses, workshops, social program](https://help.happenee.com/en/articles/30-setting-up-reservations-in-the-agenda-%E2%80%94-buses-workshops-social-program)
- [Setting up Venue and the event location](https://help.happenee.com/en/articles/22-setting-up-venue-and-the-event-location)
- [Bulk import of sessions](https://help.happenee.com/en/articles/68-bulk-import-of-sessions)
- [What to do when workshop or session registration does not work](https://help.happenee.com/en/articles/90-what-to-do-when-workshop-or-session-registration-does-not-work)

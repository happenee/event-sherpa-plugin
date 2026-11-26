# Managing accommodation and roommate selection

> How to let attendees pick a roommate in the Registration form and prepare data for the hotel.

- Article in the Help Center: https://help.happenee.com/en/articles/16-managing-accommodation-and-roommate-selection
- Česká verze: https://help.happenee.com/cs/articles/16-sprava-ubytovani-a-vyberu-spolubydliciho
- Collection: Event setup and registration
- Updated: 2026-04-27

---

> [!info] Overview
> If your event includes **accommodation**, you can let attendees pick a roommate directly in the Registration form. Happenee keeps the list of rooms (single and double), tracks the matching, and exports the result for the hotel. The feature is tied to question type 7 in the additional questions of the form.

## Getting started

- Decide how attendees will pick a roommate — choose from the list of people assigned to the event, no preference (the system pairs them), or single rooms only (everyone has their own).
- Before opening registration, make sure everyone who should be selectable by each other is assigned to the event in Contacts and groups — the selection runs against the list of assigned contacts, not against people who have already registered.
- Calculate the number of rooms you need (single and double) and generate them in advance.
- At the end you have an export for the hotel — confirm the hotel accepts the format Happenee produces.

## Details

### Question type 7 — Accommodation and roommate selection

In the Registration form on the **Additional questions** tab click **+ New question** and in the **Choose a question type** dropdown pick type 7 — *Accommodation — select attendee from list*. The panel opens two sections:

- **Accommodation options** — the list of choices the attendee will see (*Double room*, *Single room*, *No accommodation*). For each option you can add a conditional question (for example, *What floor would you prefer?*).
- **No roommate preference** — an option the attendee ticks if they do not mind whom they share with. The system pairs them automatically.

### Detail settings — Room administration

In the question detail open **Detail settings** → **Room administration**. This is where rooms are created and managed.

**Creating rooms.**

1. In the **Room administration** section enter a **Room name** (any name — for example, a floor number or a category type).
2. Choose the type — **Single** or **Double**.
3. Enter the **Number of rooms to generate**.
4. Click **Add**. The system creates the requested number of rooms.

> A single room can only be assigned in administration. The attendee cannot pick it in the Registration form.

Repeat for each room category you need. Watch the total — if you generate too few rooms, you will not be able to accommodate some attendees and will need to add more.

### How roommate selection works

1. Attendee A goes through the Registration form and on the type 7 question selects **Double room**.
2. Below the option, the field *Choose a roommate* appears with a list of **all attendees assigned to the event** (not only the ones who have already registered — the matching is done by the organizer in advance).
3. Attendee A picks attendee B and finishes registration.
4. Attendee B goes through their own registration and sees that attendee A has chosen them. They have two options:
   - **Confirm** the choice — the pair is matched.
   - **Pick someone else** — the original choice is broken and a new one is created.

### Managing the matching in administration

In the **Room administration** section you see:

- The list of generated rooms and who is staying in each.
- A display filter — **attendees with a roommate**, **without preference**, **all registered**, **all attendees**.
- A color legend for attendees:
  - **Yellow background** — not registered.
  - **Red background** — the user does not want accommodation.
  - **Salmon background** — the user is not attending.
  - **Purple background** — the user has canceled their registration.

The administrator can manually assign an attendee to a specific room, move them between rooms, or assign a single room.

### Hotel export

From room administration you can generate an **export** with the room occupancy list — name, e-mail, room, room type, roommate. The format is Excel. Before handing it to the hotel, confirm their system accepts this format, or adjust the data.

### Multiple languages

Edit the accommodation options and the question text in every language the event has added — use the flag switcher in the top right corner. The room name and the legend in administration are not shown to attendees (they are only for the organizer), so you do not need to translate them.

## Common pitfalls

### Attendees cannot choose a roommate because the person is not on the list, and the organizer does not know why

The selection runs against the list of **contacts assigned to the event**, not against registered ones. If you want attendees to be able to pick each other, assign them all to the event in advance — in bulk through a group or import.

### Too few rooms have been generated, and some attendees go through the form but cannot be given accommodation

Calculate the number of rooms you need before opening registration. Add a buffer — about 10 % is reasonable. You can add rooms anytime through **Room administration → + Add**.

### Attendee A picks attendee B, but B finished registration earlier and does not see A on the list

Roommate selection works in both directions, but for both sides to use it, both must go through the Registration form after they were assigned to the event. If B finishes registration first and A picks B afterward, A will see B on the list and B has to confirm in the attendee profile (not in the original form).

### The room type changes after registration (from double to single), and an attendee who was paired up is now alone

Rearrange attendees manually in administration. If your event has a lot of changes, hold off on assigning rooms until registration closes — that way you avoid repeated rearranging.

### The export handed to the hotel does not contain everything the hotel needs (for example, catering information or contact details)

The accommodation export does not include all the information from the Registration form. For additional data, use the export of the full Registration form and combine the data manually in Excel.

## Related articles

- [Setting up the Registration form](https://help.happenee.com/en/articles/13-setting-up-the-registration-form)
- [How conditional questions work in the Registration form](https://help.happenee.com/en/articles/14-how-conditional-questions-work-in-the-registration-form)
- [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility)
- [Managing contacts and groups in your workspace](https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace)
- [Preparing data for accommodation providers](https://help.happenee.com/en/articles/49-preparing-data-for-accommodation-providers)

# Bulk import of sessions

> Upload sessions into the Agenda from Excel through a 5-step wizard — template or your own file, column mapping, validation, and a preview before anything is written.

- Article in the Help Center: https://help.happenee.com/en/articles/68-bulk-import-of-sessions
- Česká verze: https://help.happenee.com/cs/articles/68-hromadny-import-sessions
- Collection: Content and attendee experience
- Updated: 2026-08-07

---

> [!info] Overview
> Bulk import lets you create several sessions at once from an Excel file instead of adding them one by one. It pays off when you already have your agenda in a spreadsheet — typically ten or more sessions. The wizard has five steps (upload, mapping, relations, preview, result) and validates the data before anything is written. The import always applies to the Agenda instance you run it from.

## Getting started

- Consider whether the import is the right route. It pays off from roughly ten sessions upwards. If you only need a handful that differ in small details, it is faster to create one and copy the rest — see [Managing sessions](https://help.happenee.com/en/articles/69-managing-sessions).
- Decide **which Agenda instance** you are importing into. If the event has more than one Agenda (for example *Main agenda* and *Workshops*), the **Import** tab is separate for each.
- Prepare your data in Excel. You can either download the **template** from the admin or use **your own file** — you map the columns by hand in the second step of the wizard.
- **Type is always required on a session.** You do not have to put it in the file — if you leave the Type column empty, you assign a type to all imported sessions at once in the *Relations* step. So have your **session types** ready in the Agenda (and any **blocks**, **stages**, and **tags** you will reference in the file).
- You **cannot create speakers or moderators through this import** — create them separately (see *Bulk import of speakers*) and link them to sessions in step 3 of the wizard or later.

## Details

### Where to find Import

In the admin, go to **Content** and open the **Agenda** you want to import into. The section header has the tabs **Sessions**, **Types**, **Blocks**, **Tags**, **Stages**, **My Agenda**, **Settings**, and **Import**. Open the **Import** tab.

The **Import** tab is tied to a specific Agenda instance — sessions are imported into the Agenda you are currently in.

### Template or your own file

In the first step of the wizard you have two paths:

- **Download the template** and fill it in. The template is a single sheet with a header row and one sample row of dummy data (delete it before importing — see the pitfall below).
- **Upload your own Excel** with your own column names — even a previously downloaded **sessions export** from this or another event. You set the mapping to session fields by hand in the second step, so the column names do not matter.

In both cases you then click **Upload and process** and the wizard moves to mapping.

### What you can map

In the second step, the file's columns are assigned to session fields. Required fields must be mapped or the row will not pass validation:

- **Title** *(required)* — Localized (tied to the event's content language).
- **Date** *(required)* — The day the session takes place.
- **Start time** *(required)* — Start time.
- **End time** *(required)* — End time.
- **Description** *(optional)* — Localized, like Title.
- **Type** *(optional)* — The value matches a session type (*Keynote*, *Workshop*, *Time slot*…). Not required in the file, but a session always needs a type — see the *Relations* step.
- **Block** *(optional)* — Registration block.
- **Stage** *(optional)* — The session's stage. The import wizard labels this column **Location**.
- **Tags** *(optional)* — Separate multiple tags with a comma.
- **Sort order** *(optional)* — A number that controls the session's ordering.

Only **Title**, **Date**, **Start time**, and **End time** are required. The other fields are optional. Columns you leave unmapped (the *skip* option) are ignored.

**Exception — Type.** It is not required in the file, but every session must have a type. If you do not fill in (or map) the Type column, you assign a type to all imported sessions at once in the *Relations* step. The import cannot finish without a type assigned.

Title and Description are localized (tied to the event's content language). **The column names in the downloaded template may differ from the field names above and may not always be accurate** — you map them to fields in the second step, so the exact column name does not matter.

### Walking through the wizard (5 steps)

At the top of the screen there is a step indicator: **Upload → Mapping → Relations → Preview → Result**. You can move back between steps.

**1. Upload.** Download the template (optional) or upload your Excel directly through the file picker. Click **Upload and process**.

**2. Mapping.** The wizard reads the file's headers and shows them in an *Excel column — Sample values — Map to field* table. For each column, pick the destination field (Title, Date, Type, …). Columns left on *skip* are ignored. The mapping is **not saved anywhere** — you set it up from scratch on every import. Click **Validate and preview**.

**3. Relations.** Link the imported sessions to other event content — typically speakers and moderators. **If the file did not include a session type, this is where you assign a type to all imported sessions** (a session always needs a type, so the import cannot finish without one). The step appears when there is something to fill in.

**4. Preview.** The wizard shows a summary: **Total / Valid / Warnings / Errors / Duplicates**. Below it is a per-row table with each row's status (a valid row is marked green; a duplicate carries a duplicate icon and the text *Duplicate session already exists.*). **Nothing has been written yet** — this is your last chance to go back and fix the file. If the summary looks good, click **Import**.

**5. Result.** After the import finishes, you see the final counts and can go back to the session list. This is the same wizard used for the speaker import.

### How the wizard detects duplicates

The wizard compares the file's rows against **sessions that already exist** in that Agenda (and also watches for repeats within the file itself). Anything it considers a duplicate is **not imported** — the row is counted under **Duplicates** and skipped. From repeated rows, only the **first occurrence** is imported.

This means the import **does not overwrite existing sessions**. To change sessions already in the Agenda in bulk, the import is not the tool — use [bulk actions in the Sessions tab](https://help.happenee.com/en/articles/69-managing-sessions).

### What import does not cover

- **Creating speakers and moderators.** This wizard only creates sessions. Import speakers separately (*Bulk import of speakers*) and link them in the *Relations* step or later from the session or speaker panel.
- **Overwriting existing sessions.** Duplicate rows are skipped. To bulk-edit existing sessions, use [bulk actions in the Sessions tab](https://help.happenee.com/en/articles/69-managing-sessions).
- **Setting the session status.** Neither the template nor the import has a column for the status — the status (Published / Hidden) cannot be set through the import. Check it in the session list after the import (see the pitfall below).

## Common pitfalls

### The template ships with a sample row — leaving it in imports a fake session

The downloaded template has the first data row pre-filled with a dummy sample session (*Future of Event Experience*). In *Preview* it shows up as valid, and after the import you are left with a made-up session in the agenda. Delete the sample row before you fill in your own data.

### Without Title, Date, Start time, and End time the row will not pass

These four fields are required. If the source does not have them (or you do not map them), the row is flagged as an error in *Preview* and is not imported. Keep the date and time in the format the template uses (the samples show *DD.MM.YYYY* and *HH:MM*).

### The session status is not set through the import — check it after the import

*Preview* shows a status per row (for example *published* / *hidden*), but **the status cannot be set through the import** — the template has no status column and status is not among the target fields. After the import, check visibility in the session list and publish the sessions that are meant to be public.

### Re-importing the same file creates nothing — every row falls into Duplicates

Because imported rows are compared against existing sessions, importing the same file a second time ends with every row treated as a duplicate and skipped (*Preview* shows *Valid 0*, *Duplicates = the row count*). So always check the **Duplicates** count before you click **Import**: a higher number than you expect means some of those sessions are already in the Agenda. The import will not recreate or overwrite them — if you meant to change existing sessions, use [bulk actions in the Sessions tab](https://help.happenee.com/en/articles/69-managing-sessions).

### Speakers and moderators are not assigned in the Mapping step

*Speakers* or *Moderators* columns are not among the target fields — leave them on skip. Handle speaker-to-session links in the *Relations* step, or later from each session's panel. If you forget, the sessions are imported without speakers and you will be tracing them by hand.

### An empty Type column is not an error — but you must assign the type in the *Relations* step

Type is not required in the file, so an empty Type column does not flag the row as an error. It does not mean the session imports without a type, though — every session must have one. In the *Relations* step you assign a type to all imported sessions; if you skip *Relations* without assigning one, the import will not finish. Have the target type ready in the Agenda beforehand.

### Type, Block, Stage, and Tags values must make sense against the Agenda

Type is required on a session, and the values in the Type, Block, Stage, and Tags columns tie to what you have prepared in the Agenda. Before you run the import, go through *Preview* to confirm these columns mapped correctly and the values line up — a wrong type is the most common reason a session "is not where it should be" after the import.

### You have to set up the column mapping on every import

The wizard does not remember your mapping — you enter it from scratch after every upload. If you import repeatedly (the agenda fills in over time), keep the **same column names and order in your file as in the downloaded template**. Mapping then takes a few seconds and you will not miss a field.

## Related articles

- [Building the event Agenda — architecture](https://help.happenee.com/en/articles/26-building-the-event-agenda-%E2%80%94-architecture)
- [How session types work](https://help.happenee.com/en/articles/27-how-session-types-work)
- [Managing sessions](https://help.happenee.com/en/articles/69-managing-sessions)
- [How registration blocks, stages, and tags work](https://help.happenee.com/en/articles/31-how-registration-blocks-stages-and-tags-work)
- [Bulk import of speakers](https://help.happenee.com/en/articles/67-bulk-import-of-speakers)
- [Bulk import of sponsors](https://help.happenee.com/en/articles/71-bulk-import-of-sponsors)

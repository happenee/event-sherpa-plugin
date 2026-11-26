# Bulk import of speakers

> Two ways to bulk-import speakers — upload an XLS/XLSX/CSV file with column mapping, or pick specific speakers from another event, photos and translations included.

- Article in the Help Center: https://help.happenee.com/en/articles/67-bulk-import-of-speakers
- Česká verze: https://help.happenee.com/cs/articles/67-hromadny-import-recniku
- Collection: Content and attendee experience
- Updated: 2026-08-07

---

> [!info] Overview
> Bulk import lets you create several speakers at once instead of entering them one by one. You choose between **two methods**: **Upload a file** (an XLS, XLSX, or CSV file you prepare yourself) or **Import from another event** (pick specific speakers from another event's Speakers module). Both wizards have five steps and show a validated preview before anything is written. The decisive difference: importing from another event **also carries photos and translations**, while a file import does not.

## Getting started

- **Decide where the data comes from.** Are the speakers already in another event in Happenee? Use *Import from another event* and save yourself the manual photo work. Are they coming from outside (from a client, from a CRM)? Prepare a spreadsheet.
- For a file import, prepare your data in Excel. You can either download the **template** from the admin or use **your own file** — you map the columns by hand in the second step of the wizard.
- Decide **which languages** the speaker texts (job title, bio) will be in. The template is generated according to the languages enabled on your event — a single-language event gets a template with one language only; a multilingual event gets separate columns for each language.
- For a file import, **photos go in separately**. They cannot be uploaded through a spreadsheet; add them by hand after the import in each speaker's edit panel.
- If you want to link the imported speakers to specific sessions right away, the **sessions must first exist in the Agenda**. When importing from another event, relations are not carried over at all — count on setting them up again.

## Details

### Where to find Import

In the admin, go to **Content → Speakers**. The section header has two tabs: **Speaker** (the speaker list) and **Import**. Open the **Import** tab.

### The two import methods

The **Import** tab opens on a **Choose import method** screen with two cards:

- **Upload a file** — *"Import speakers from an XLS, XLSX, or CSV file."* You prepare the data yourself in a spreadsheet. The rest of this article covers that route.
- **Import from another event** — *"Select specific speakers from another Speakers module."* You copy speakers from an event that already has them set up. See *Importing from another event* below.

A rule of thumb: if the speakers are **already somewhere in Happenee** — last year's edition, another office, the event you copied from — use the import from another event. It brings **photos and translations** along with them, which a spreadsheet cannot give you. Use a spreadsheet when the data comes from outside (from a client, from a speaker sign-up form, from a CRM).

### Downloading the template

In the first step of the wizard, click **Download template**. The template is an XLSX file with a single sheet, a header row, and a single sample row of dummy data.

The template is **localized to your event's primary language** — a Czech event gets the CS variant (sheet *Řečník*, headers in Czech), an English event gets the EN variant (sheet *Speaker*, headers in English).

The template does not include dropdowns or validation lists. You enter the numeric codes for **Display level** and **Status** by hand — the meaning of each code is written right into the column header.

### What you can import

- **First name** *(required)*
- **Last name** *(required)*
- **Company** *(optional)*
- **Country** *(optional)* — Filled in as a **country code**, not a name — the sample row in the template uses `CZ`.
- **Job title (CS / EN / SK …)** *(optional)* — A separate column for each language enabled on the event.
- **Bio (CS / EN / SK …)** *(optional)* — A separate column for each language enabled on the event.
- **Display level** *(optional)* — Numeric code `1`–`3`. If you leave the column empty, **Basic** is used.
- **Status** *(optional)* — Numeric code `0`–`2`. If you leave the column empty, the speaker is imported as **Hidden**.

Only **First name** and **Last name** are required. The other fields are optional. For **Display level** and **Status**, an empty value applies a default (Basic level, Hidden status) — see the pitfall below.

The job-title and bio columns **appear in the template and in the wizard only for languages your event has enabled**. A Czech-only event gets only *Job title — CS* and *Bio — CS*; other languages are not offered at all.

### Numeric codes: Display level and Status

Both values are entered as numbers in Excel:

**Display level** controls the order and the size of the speaker card on the microsite and in the app. If you leave the column empty, **Basic** (code `3`) is used:

- **`1`** — High
- **`2`** — Medium
- **`3`** — Basic

**Status** controls where the speaker profile appears to attendees. If you leave the column empty, the speaker is imported as **Hidden** (code `0`):

- **`1` — Published** — Profile visible everywhere — on the attendee app home screen, in the speaker list on the microsite and in the app, with sessions in the Agenda, on the session detail, and on the speaker's own detail page.
- **`2` — In agenda** — Profile **not** in the speaker list or on the app home screen; visible with sessions in the Agenda, on the session detail, and on the speaker's own detail page (reachable by clicking through from the session detail). Suits moderators and internal presenters you do not want featured in the speaker list.
- **`0` — Hidden** — Profile not visible anywhere — not in the speaker list, not with sessions; there is no speaker detail page either.

### Walking through the wizard (5 steps)

At the top of the screen there is a step indicator: **Upload → Mapping → Relations → Preview → Result**. You can move back between steps.

**1. Upload.** Download the template (optional) or upload your Excel directly through the file picker. Click **Upload and process** — the file is sent and the wizard moves to the next step.

**2. Mapping.** The wizard reads your file's headers and shows them in an *Excel column — Sample values — Map to field* table. For each column, pick the destination field from the dropdown (First name, Last name, Bio — CS, etc.). Columns you leave unmapped are skipped. The mapping is **not saved anywhere** — you set it up from scratch on every import. Click **Validate and preview**.

**3. Relations.** Link the imported speakers to other event content (typically sessions from the Agenda). The step appears when your event has relevant content to link to.

**4. Preview.** The wizard shows a summary: **Total / Valid / Warnings / Errors / Duplicates**. Below the summary is a per-row table with each row's status (a valid row is marked green). **Nothing has been written yet** — this is your last chance to go back and fix the file. If the summary looks good, click **Import**.

**5. Result.** After the import finishes, the screen shows the final counts: **Created / Skipped / Errors**. From here you can go back to the speaker list (**Continue to list**) or download a detailed CSV report on every row (**Download report (CSV)**) — useful if you need to trace which row did not import and why.

### How the wizard detects duplicates

A duplicate is determined by **first name and last name together**. A row is a duplicate if:

- a speaker with the same first and last name **already exists in the event**, or
- the same first and last name **repeats in the file** across multiple rows.

Duplicate rows are **not imported** — the wizard skips them. From repeated rows, only the **first occurrence** is imported; the rest are dropped. The *Preview* step shows the duplicate count up front; in the *Result*, skipped rows are counted under **Skipped**.

This means the import **does not overwrite existing speakers**. If you want to change data in bulk for a speaker already in the event, the import is not the tool — use the bulk-actions panel in the speaker list, or edit the speaker by hand.

### Importing from another event

The second method on the chooser. It is not based on a file — you pick specific speakers from the Speakers module of **another event in the same workspace**. This wizard also has five steps, but different ones: **Event → Module → Speakers → Preview → Result**.

**1. Event.** A **Source event** field listing events as *name (#ID)*, with a **Search events by name** box above it. Until you pick an event, **Continue** stays disabled.

**2. Module.** A **Source Speakers module** field. It is picked separately because one event can have the Speakers module more than once.

**3. Speakers.** A table of the source module's speakers with the columns **Name · Company · Position · Status · Photo** and a checkbox on each row. Above it are a **Search speakers** box, a count of what you selected, and the **Select all** / **Clear selection** buttons. The *Status* column tells you whether the speaker is **Published**, **In agenda**, or **Hidden** in the source event, so you can also pick a profile you do not want public on your side yet. Continue with **Review preview**.

**4. Preview.** At the top, a **Source** and **Target** summary (both as *event / module (#ID)*), and below it six counters: **Selected · Importable · Duplicates · Invalid · Translations · Photos**. Under those, a table with each speaker's validation result (**Ready to import**). The **Import** button writes the data.

**5. Result.** Five numbers — **Created · Skipped · Translations · Photos · Without photo** — plus the **Go to speaker list** and **Import more** buttons.

**What is carried over and what is not:**

- **Profile data (name, company, position, bio)** — Yes
- **Photos** — Yes — JPEG, PNG, and GIF. The file gets a new safe name; a missing or invalid photo **does not stop** that speaker's import, it just ends up in the *Without photo* count.
- **Translations** — Yes — the *Translations* counter shows how many.
- **Relations to the agenda and sessions** — **No.** The wizard warns you about this explicitly. You have to assign speakers to sessions again in the target event.

**Duplicates are checked against the target event.** A speaker who already exists in the target event is left out of the *Importable* count, does not appear in the preview table at all, and lands in **Skipped** in the result. The import does not fail because of them and everyone else goes through. It also means the **profile is not overwritten** — importing the same speaker again does not update their data in the target event.

### What import does not cover

- **Uploading photos from a file.** Neither the template nor the file wizard has a column for a photo or a photo URL. Add photos by hand after the import — or use **Import from another event**, where they are copied.
- **Importing sessions or the agenda.** This wizard only creates speaker profiles. Create sessions by hand in the Agenda. Links between speakers and sessions can be set in step 3 of the wizard, or later from the speaker or session edit panel.
- **Bulk-updating existing speakers.** Import is meant for creating new profiles. To change the Display level or Status on speakers already in the event, use the bulk-actions panel in the speaker list.

## Common pitfalls

### The template ships with a sample row (Jan Novak) — leaving it in imports a fake speaker

The downloaded template has the first data row pre-filled with dummy data. In the *Preview* step it shows up as valid. Delete the sample row before you fill in your own data; otherwise Jan Novak from Happenee ends up in your speaker list.

### Display level and Status take numbers, not names

Writing *"High"* or *"Published"* into the cell does not work — the field expects a numeric code (`1`/`2`/`3` for Display level, `0`/`1`/`2` for Status). If you enter a word or an invalid number (for example `4`), the row is flagged as an error in *Preview*. The meaning of the codes is written into the column header in the template.

### An empty Status column imports every speaker as Hidden

Status and Display level are not required, but an empty value does not mean "leave as is" — a default is applied. An empty **Status** means **Hidden** (the speakers are not visible to attendees anywhere); an empty **Display level** means **Basic**. If you want to publish the speakers right away, fill in the Status column (`1` = Published). After the import, check the state in the speaker list — if everyone is hidden, you left the Status column empty.

### A template downloaded from one event does not match another event with different languages

The job-title and bio columns are generated for that specific event's languages. If you download the template from a trilingual event (CS + EN + SK) and use it on a single-language event, the extra columns either go unmapped (and stay empty) or get confusing. **Download the template from the event you are importing into.**

### Photos cannot be uploaded through the import — plan time for manual work afterward

Bulk import handles only data in text fields. If your event has 80 speakers, plan for walking through 80 edit panels and adding photos by hand after the import.

### Do not skip the *Relations* step without checking

If sessions already exist in the Agenda and you want to link speakers right away, this step is the fastest path. Skipping it means linking speakers from each session's panel by hand — an extra hour of work for 50 speakers and 30 sessions.

### Two different people with the same name — the second one is not imported

A duplicate is detected by first name and last name only, not by company or e-mail. If you have two different speakers with the same first and last name (for example, two John Smiths from different companies), the wizard treats the second one as a duplicate and **does not import them** — only the first is created. Before you click **Import**, check the duplicate count in *Preview* — if it is higher than you expect, go through the file and disambiguate genuinely different people (for example, with a middle name), or one of them drops out.

### Retyping last year's speakers into a spreadsheet

The most expensive way to get people Happenee already knows about into an event. Retyping into Excel loses the photos and the translations and costs you an hour. If the source event is still in the workspace, use **Import from another event** — you tick the speakers and the photos come with them.

### Speakers are missing from the agenda after an import from another event

Profiles are carried over, **relations to sessions are not**. The wizard says so on the preview screen, but it is easy to miss. After the import, go through the agenda and assign the speakers to sessions again — from the speaker's edit panel on the *Sessions* tab, or from the session panel.

### Expecting a repeated import from another event to update speakers already imported

It does not. Duplicates are checked against the target event, and a duplicate speaker is **skipped** — they do not appear in the preview table at all and land in *Skipped* in the result. The import does not fail because of it, but the profile stays as it was. Make changes by hand or with the bulk actions in the speaker list.

### You have to set up the column mapping on every import

The wizard does not remember your column mapping — you enter it from scratch after every upload. If you import repeatedly (for example, speakers trickle in over time), keep the **same column names and order in your file as in the downloaded template**. Mapping then takes a few seconds and you will not miss a field.

## Related articles

- [Managing Speakers](https://help.happenee.com/en/articles/23-managing-speakers)
- [Bulk import of sessions](https://help.happenee.com/en/articles/68-bulk-import-of-sessions)
- [Bulk import of sponsors](https://help.happenee.com/en/articles/71-bulk-import-of-sponsors)
- [Bulk import of exhibitors](https://help.happenee.com/en/articles/72-bulk-import-of-exhibitors)

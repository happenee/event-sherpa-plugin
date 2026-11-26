# Bulk import of sponsors

> Import sponsors from Excel — map columns, assign categories in Relations, preview, and download a CSV report.

- Article in the Help Center: https://help.happenee.com/en/articles/71-bulk-import-of-sponsors
- Česká verze: https://help.happenee.com/cs/articles/71-hromadny-import-sponzoru
- Collection: Content and attendee experience
- Updated: 2026-09-29

---

> [!info] Overview
> Bulk import lets you create several sponsors at once from an Excel file instead of adding them one by one. It pays off when you already have your partners in a spreadsheet — typically ten or more. The wizard runs validation on the data before anything is written. In **Relations**, you can assign category values from the file to existing categories or create new ones. The import handles text fields, category assignment, and optionally status; **logos cannot be uploaded through the import** and have to be added by hand afterward.

## Getting started

- Decide **which Sponsors instance** you are importing into. The Sponsors content feature can be added to an event more than once (for example *Conference partners* and *Media partners*), and the **Import** tab is separate for each of them — sponsors land in the instance you are currently in.
- Prepare your data in Excel. You can either download the **template** from the admin or use **your own file** — you map the columns by hand in the second step, so the column names do not matter.
- Review your **category names**. Every sponsor needs a category. In **Relations**, you can assign values from the file to existing categories or choose to create new ones, so you can fix a typo before import.
- **Prepare the logos separately.** The import cannot handle them; you add them by hand in each sponsor's edit panel after the import.
- Decide **what happens when someone clicks the logo** (external website, sponsor profile, or nothing). The value goes into the file as a word, and it has to match what you filled in the other columns.

## Details

### Where to find Import

In the admin, go to **Content** and open the **Sponsors** instance you want to import into (the instance name sits in the switcher next to the *Content* heading). The section header has four tabs: **Sponsors**, **Categories**, **Settings**, and **Import**. Open the **Import** tab.

### Template or your own file

The first step of the wizard gives you two paths:

- **Download template** and fill it in. The template is an XLSX file with a single sheet named *Sponsors*, a header row, and one sample row of dummy data (*Example Sponsor s.r.o.*) — delete that row before you import, see the pitfall below. The file name includes the name of the event you downloaded it from.
- **Upload your own Excel** with your own column names. You set the mapping to sponsor fields by hand in the second step.

Template headers come in **the language of the admin interface** — a Czech admin gives you *Název*, *Kategorie*, *Webové stránky*; an English one *Name*, *Category*, *Website*. That has no effect on the content: both variants have the same columns in the same order and the same sample row, and the mapping step works regardless of the header language.

The description column, on the other hand, follows **the event's content language** — on an event with English content it is named *Description - EN*.

Either way, you then click **Upload & parse** and the wizard moves on to mapping.

### Fields you can import

- **Name** *(required)* — The sponsor name. Also the key used to detect duplicates.
- **Category** *(required)* — In **Relations**, assign the file value to an existing category or choose to create a new one.
- **Website** *(optional)* — The URL must start with `https://`.
- **Logo click action (website/profile/none)** *(optional)* — The value is written as a word: `website`, `profile`, or `none`.
- **Description - EN** *(optional)* — Tied to the event's content language.
- **E-mail** *(optional)*
- **Phone** *(optional)*
- **LinkedIn, Twitter / X, Instagram, Facebook, YouTube** *(optional)* — Links to the sponsor's social networks.
- **Status** *(optional)* — The value is written as a word: `published` (Published) or `hidden` (Hidden). The downloaded template does not have this column, so if you want to set the status through the import, add it to your file yourself. If you leave it unmapped, check the status of the new sponsors in the sponsor list after the import.

Only **Name** and **Category** are required — you can spot them by the asterisk on the destination field in the mapping step. Columns you leave unmapped are skipped.

The logo and the sponsor's order within a category are not among the destination fields, so the import does not set them.

### The logo click action is written as a word

Unlike the speaker import, where display level and status are entered as numeric codes, sponsors take **text**. The allowed values are spelled out in the column name itself:

- **`website`** — clicking the logo opens the sponsor's external website. Fill in the *Website* column too, with an `https://` URL.
- **`profile`** — clicking opens the sponsor's profile inside the platform. Fill in the description too, and optionally contacts and social networks.
- **`none`** — clicking the logo does nothing; the logo is purely visual. Nothing else to fill in.

### The import wizard

The wizard takes you through the **Upload**, **Mapping**, **Relations**, **Preview**, and **Results** screens. You can move back between steps.

**Upload.** Download the template (optional) or upload your Excel directly through the file picker. Click **Upload & parse**.

**Mapping.** The wizard reads your file's headers and shows them in an *Excel column — Sample values — Map to field* table, along with the number of rows found. For each column, pick the destination field from the dropdown. Unmapped columns are skipped. The mapping is **not saved anywhere** — you set it up from scratch on every import. Click **Validate & preview** and the wizard opens category assignment.

**Relations.** For each category value found in the file, choose an existing category or **+ Create new**. If a category with the same name already exists, the wizard preselects it, even when the capitalization differs; you can assign a misspelled value to the intended existing category. A new category is created only when you confirm the import. Click **Validate & preview** and check the assignments in Preview.

**Preview.** The wizard shows a summary: **Total / Valid / Warnings / Errors / Duplicates**. Below the summary is a per-row table with each row's status — a valid row is marked green, a duplicate row carries a duplicate icon and a message that a sponsor with this name already exists. Row numbers match the row numbers in Excel, so the first data row is `2` (row 1 is the header). **Nothing has been written yet** — this is your last chance to go back and fix the file. If the summary looks good, click **Import**.

**Results.** After the import finishes, the screen shows the final counts: **Created / Skipped / Errors**. From here you can go to the sponsor list (**Continue to list**) or download a detailed CSV report on every row (**Download report (CSV)**) — useful when you need to trace which row did not import and why.

### Categories: the import creates them, but does not show them on the home screen

Every sponsor needs a category. If you choose **+ Create new** in **Relations**, the import creates the category and assigns the sponsors to it. If you select an existing category, no new category is created.

A newly created category, however, **does not appear on the home screen** of the microsite or the attendee app on its own. If you want it there, turn on the **Display on the home screen of the microsite and attendee app** toggle for that category on the **Categories** tab after the import. While you are there, check its **Display level** as well (values **1**, **2**, **4**) — it drives the order of categories and the number of logos per row.

### How the wizard detects duplicates

For sponsors, a duplicate is determined by **the name alone**. A row is a duplicate if:

- a sponsor with the same name **already exists in the event**, or
- the same name **appears more than once in the file**.

Duplicate rows are **not imported** — the wizard skips them and, from repeated rows, imports the **first occurrence**. The *Preview* step shows the duplicate count up front; in the *Results*, skipped rows are counted under **Skipped**.

This means the import **does not overwrite existing sponsors**. To change sponsors that are already in the event, use the bulk actions on the Sponsors tab (change category, change status, delete).

### What the import cannot do

- **Upload logos.** Neither the template nor the mapping has a column for a logo or a logo URL. Add logos by hand in each sponsor's edit panel after the import.
- **Set the order within a category.** Sponsor order inside a category is set by dragging rows in the list, not by a column in Excel.
- **Update existing sponsors.** Duplicate rows are skipped; handle bulk changes with the bulk actions in the sponsor list.

## Common pitfalls

### The template ships with a sample row (Example Sponsor s.r.o.) — leaving it in imports a fake sponsor

The downloaded template has the first data row pre-filled with dummy data, including the category *Main sponsors*, the website *example.com*, and a phone number with a country code. In *Preview* it shows up as a valid row. Delete it before you fill in your own data — otherwise you end up with a fake sponsor in the list and, depending on your choice in **Relations**, possibly a *Main sponsors* category.

### Fix a category typo in Relations

A typo is not an error that *Preview* automatically rejects. For example, you can assign *Gold Sponsers* from the file to the existing *Gold sponsors* category in **Relations**. If you leave **+ Create new** selected instead, the import creates another category. Before you click **Import**, check the selected category for each row in Preview.

### A category created by the import does not show up on the home screen by itself

A category created during the import has its sponsors assigned correctly, but display on the home screen of the microsite and the attendee app has to be turned on by hand on the **Categories** tab. If the sponsors are not visible on the home screen after the import, this is the first place to check — along with the status of both the sponsor and the category (sponsors are visible only when **both** are **Published**).

### Importing the same file twice creates nothing — every row lands in Duplicates

Rows are compared against sponsors that already exist in that instance, so a second import of the same file ends with everything flagged as a duplicate and skipped (in *Preview* you see *Valid 0* and *Duplicates* equal to the number of rows). Always check the duplicate count before you click **Import** — a higher number than you expect means some of those sponsors are already in the event. The import will not create them again, and it will not overwrite them.

### Two sponsors with the same name — the second one is not imported

For sponsors, a duplicate is detected by name only, not by website or e-mail (speakers, by contrast, are matched on first and last name together). If you have two branches or two divisions of the same company entered under an identical name, only the first goes through. Disambiguate them in the name (for example by country or division), or one of them drops out.

### Logos cannot be uploaded through the import — plan time for manual work afterward

Bulk import handles text fields, the category assignment, and the status only. With 20 partners that means 20 edit panels in which you add the logo after the import (PNG, JPEG, or GIF; 16:9 ratio; max. 500 KB). Plan time for it, and prepare the logos in a consistent format up front.

### You have to set up the column mapping on every import

The wizard does not remember your column mapping — you enter it from scratch after every upload. If you import repeatedly (partners trickle in over time), keep the **same column names and order in your file as in the downloaded template**. Mapping then takes a few seconds and you will not miss a field.

## Related articles

- [Managing Sponsors](https://help.happenee.com/en/articles/32-managing-sponsors)
- [Bulk import of speakers](https://help.happenee.com/en/articles/67-bulk-import-of-speakers)
- [Bulk import of sessions](https://help.happenee.com/en/articles/68-bulk-import-of-sessions)
- [Bulk import of exhibitors](https://help.happenee.com/en/articles/72-bulk-import-of-exhibitors)

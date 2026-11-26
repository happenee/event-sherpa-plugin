<!-- source: kb.en.03.23 -->

---
title: "Bulk import of exhibitors"
description: "Upload exhibitors from Excel through a 5-step wizard — template, column mapping, assigning categories and locations, validation, and a CSV report."
modules: ["sponzori_a_vystavovatele"]
last_updated: "2026-08-07"
version: 2
---

> [!info] Overview
> Bulk import lets you create several exhibitors at once from an Excel file instead of adding them one by one. It pays off when you already have your booth list in a spreadsheet — typically ten or more. The wizard has five steps (upload, mapping, assigning categories and locations, preview, results) and runs validation on the data before anything is written. It imports text fields, the booth number, the category, and the location; **logos, representatives, and tags are not set by the import** — logos, however, can be fetched in bulk afterward with the **Find logos** action.

## Getting started

- Decide **which Exhibitors instance** you are importing into. The content feature can be added to an event more than once, and the **Import** tab is separate for each instance — exhibitors land in the one you are currently in.
- Prepare your data in Excel. You can either download the **template** from the admin or use **your own file** — you map the columns by hand in the second step.
- **Fill in the websites in your file.** The import does not upload logos, but the **Find logos** bulk action can fetch them from the exhibitors' websites after the import — without a URL, the exhibitor ends with the *Missing website* status and you add the logo by hand.
- Align your **category and location names**. The wizard has a dedicated step for checking them: you assign the values from your file to existing categories and locations, or let it create new ones.
- **Representatives** (booth staff) cannot be created by the import — they have to be attendees of the event, and you assign them to exhibitors by hand after the import.

## Details

### Where to find Import

In the admin, go to **Content** and open the **Exhibitors** instance you want to import into. The section header has six tabs: **Exhibitors**, **Categories**, **Locations**, **Tags**, **Settings**, and **Import**. Open the **Import** tab.

### Template or your own file

The first step of the wizard gives you two paths:

- **Download template** and fill it in. The template is an XLSX file with a single sheet named *Exhibitors*, a header row, and one sample row of dummy data (*Example Company s.r.o.*, booth *A-01*) — delete that row before you import, see the pitfall below.
- **Upload your own Excel** with your own column names. You set the mapping to exhibitor fields by hand in the second step, so the column names do not matter.

Template headers come in **the language of the admin interface** (a Czech admin gives you *Název*, *Webové stránky*…; an English one *Name*, *Website*…); the description column follows **the event's content language** (on an event with English content it is *Description - EN*). Both variants have the same columns in the same order, so the template language does not matter.

Either way, you then click **Upload & parse** and the wizard moves on to mapping.

### Fields you can import

- **Name** *(required)* — The only required field. Also the key used to detect duplicates.
- **Website** *(optional)* — The URL must start with `https://`. The source for bulk logo lookup after the import.
- **E-mail** *(optional)*
- **Phone** *(optional)*
- **Description - EN** *(optional)* — Tied to the event's content language.
- **Booth number** *(optional)* — In the exhibitor's edit panel the same field is named **Exhibitor number** — the *By number* sorting uses it.
- **Category** *(optional)* — Unlike sponsors, **not required**. Values are assigned in step 3 of the wizard.
- **Location** *(optional)* — The booth or sector (for example *Hall A*). Values are assigned in step 3 of the wizard.
- **LinkedIn, Twitter / X, Instagram, Facebook, YouTube** *(optional)* — Links to the exhibitor's social networks.

Only **Name** is required — you can spot it by the asterisk on the destination field in the mapping step. Columns you leave unmapped are skipped.

The template **has no column for tags, logo, representatives, or status** — the import does not set any of them (see *What the import cannot do*).

### The import wizard (5 steps)

At the top of the screen there is a step indicator: **Upload → Mapping → Categories → Preview → Results**. You can move back between steps. Compared to the speaker and sponsor imports, the third step is different — instead of *Relations* it has its own screen for categories and locations.

**1. Upload.** Download the template (optional) or upload your Excel directly through the file picker. Click **Upload & parse**.

**2. Mapping.** The wizard reads your file's headers and shows them in an *Excel column — Sample values — Map to field* table, along with the number of rows found. For each column, pick the destination field. The mapping is **not saved anywhere** — you set it up from scratch on every import.

**3. Categories.** The **Assign categories and locations** screen. The wizard lists every unique value from the Category and Location columns — each with its occurrence count and an **Assign to** dropdown. You either assign the value to an existing category or location (even if it is spelled differently in the file) or let the wizard create a new one. This is where you catch typos and naming mismatches — see the pitfall below. Click **Validate & preview** (or **← Back to mapping**).

**4. Preview.** The wizard shows a summary: **Total / Valid / Warnings / Errors / Duplicates**. Below the summary is a per-row table with each row's status — a valid row is marked green, a duplicate row carries a duplicate icon and a message that an exhibitor with this name already exists. Row numbers match the row numbers in Excel (the first data row is `2`). **Nothing has been written yet** — this is your last chance to go back and fix the file. If the summary looks good, click **Import**.

**5. Results.** After the import finishes, the screen shows the final counts: **Created / Skipped / Errors**. From here you can go to the exhibitor list (**Continue to list**) or download a detailed CSV report on every row (**Download report (CSV)**).

### How the wizard detects duplicates

A duplicate is determined by **the exhibitor's name** — the same rule as for sponsors. A row is a duplicate if an exhibitor with the same name **already exists in the event**, or the same name **appears more than once in the file**. Duplicate rows are **not imported**; from repeated rows, the first occurrence is imported. This means the import **does not overwrite existing exhibitors** — for bulk changes, use the bulk actions on the Exhibitors tab.

### What the import cannot do

- **Upload logos.** Neither the template nor the mapping has a logo field. You do not have to collect them by hand afterward, though — select the exhibitors and run the **Find logos** bulk action, which tries to fetch logos from the filled-in websites.
- **Create representatives.** Representatives are event attendees — an exhibitor Excel does not create them. Assign them after the import in the exhibitor's edit panel on the **Representatives** tab.
- **Assign tags.** The template has no tags column and the *Categories* step assigns only categories and locations. Add tags after the import — fastest with the **Tags** bulk action in the exhibitor list.
- **Set the status.** Published / Hidden is not determined by the import — check the status in the list afterward.
- **Update existing exhibitors.** Duplicate rows are skipped.

## Common pitfalls

### The template ships with a sample row (Example Company s.r.o.) — leaving it in imports a fake exhibitor

The downloaded template has the first data row pre-filled with dummy data, including booth *A-01*, the category *Services*, and the location *Hall A*. In *Preview* it passes as valid. Delete it before you fill in your own data — otherwise you end up with an invented exhibitor in the list, plus a category and a location created for it.

### Do not turn a typo into a new category in the *Categories* step

The *Assign categories and locations* step is your safeguard against typos — but only if you use it. If your file contains *Healthcare* and the event already has *Health care*, assign the value to the existing category with the **Assign to** dropdown; if you let the wizard create a new one without checking, you end up with two near-identical categories and broken filtering. The same goes for locations.

### Name is the only required field — but an exhibitor without a category and location is hard to find

The import does not force you to fill in categories or locations. Yet categories, locations, and tags work as filters in the app and on the microsite — an exhibitor without them gets lost in a longer list. Fill in the Category and Location columns in your file, and add tags after the import with the bulk action.

### Without websites you cannot fetch logos in bulk

The **Find logos** bulk action works from the **Website** field — exhibitors without a URL end with the *Missing website* status, and you add their logos by hand. If you have the websites, put them in the import file; with 50 booths that is the difference between one dialog and an afternoon of manual work.

### Importing the same file twice creates nothing — every row lands in Duplicates

Rows are compared against exhibitors that already exist in that instance, so a second import of the same file ends with *Valid 0* and *Duplicates* equal to the number of rows. A higher duplicate count than you expect means some of those exhibitors are already in the event — the import will not create them again, and it will not overwrite them.

### Two exhibitors with the same name — the second one is not imported

A duplicate is detected by name only, not by booth number or e-mail. Two branches of the same company under an identical name pass as one — disambiguate them in the name (for example by city), or one of them drops out.

### You have to set up the column mapping on every import

The wizard does not remember your column mapping — you enter it from scratch after every upload. If you import repeatedly, keep the **same column names and order in your file as in the downloaded template**.

# Managing contacts and groups in your workspace

> The workspace's central database for contacts and groups, shared across all your events.

- Article in the Help Center: https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace
- Česká verze: https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace
- Collection: Event setup and registration
- Updated: 2026-10-26

---

> [!info] Overview
> Contacts and groups is the **central database** of your workspace, shared across every event. You add contacts manually or by importing them from Excel or CSV, and you use groups to target communication and control visibility. A well-planned group structure saves hours of work — a poorly planned one means manually re-assigning hundreds of attendees later.

## Getting started

- Decide how many groups you need and what the splitting criteria are. Typical criteria: attendee type (VIP, standard, speaker, partner), source of registration (who invited them), workshop or track, company affiliation.
- Create the groups **before you launch registration**, not during it.
- You can add contacts manually or in bulk by importing an Excel or CSV file. The import puts contacts into groups, fills custom fields and the preferred language, optionally assigns them to an event, and shows you what will happen before anything is written.
- Assigning a contact to an event is a separate step from creating it in the workspace.

## Details

### Where contacts and groups live

In the workspace left menu (at account level, not inside an event) you see the item **Contacts and groups**. Inside an event, the bottom of the menu also has a link to contacts and groups, and on the event Overview the **Tools** section has a button for quick access.

Contacts are **shared across the entire workspace** — the same contact can be assigned to any number of events. Data such as name, e-mail, phone, company, custom contact fields, and preferred language are shared across events.

### Adding contacts

**One at a time.** Click **+ Add contact** and fill in the data. Useful for ad-hoc additions (for example, when an attendee who did not go through registration needs to be added by hand).

**Bulk import from a file.** The import lives on the **Import** tab in Contacts and groups. The wizard has four steps: **Upload**, **Mapping**, **Validation**, and **Import**. Nothing is written to the database until you click **Confirm and import** in the Validation step, so you can run through the whole thing as a dry run.

1. **Prepare the file.** **Download template** gives you an Excel file with the columns First name, Last name, Company, Company ID, E-mail, Phone, Job title, and Language, plus a sample group column and a sample custom-field column. The template is optional, though: you can upload an export from another system (xls, xlsx, or csv) and match its columns in the Mapping step. The only required value is the e-mail address.
2. **Put groups and custom fields in the header.** A column named `#VIP` puts every contact with anything in that cell (for example `yes`) into the group *VIP*. If your groups sit in one column as text (`VIP, Speakers`), you map that column to **Groups from value** in the next step; separate the names with a comma, a semicolon, or a vertical bar. A custom contact field gets a column named `*Field name`. You do not have to create the group or the custom field first; the import creates it.
3. **Upload.** Choose the file and pick the **Import mode** (see below). **Optional event assignment** assigns every imported contact to the selected event, so you do not have to do it separately. The **Default language** field is used for rows where the language is missing or not recognized. Continue with **Upload and load**.
4. **Mapping.** The table shows each column of your file, a sample of its values, and the contact field it maps to. Happenee suggests the mapping from the column names and understands both Czech and English headers (*Příjmení* as well as *Last name*). Check it, leave the columns you do not want on **Skip**, and continue with **Validate import**. The wizard does not continue without a column mapped to e-mail.
5. **Validation.** Happenee goes through every row and shows a summary: how many rows are fine, how many have an error, how many are duplicates, how many contacts will be created and how many already exist, and how many group assignments, custom-field values, and event assignments the import will make. Below the summary you see the list **Newly created groups** and the **Problem rows** table with the row number, e-mail, status, and a description of the problem. **Download report** gives you a CSV with the status of every row. If you want to fix the file, edit it and upload it again; the unfinished import has written nothing. Otherwise confirm with **Confirm and import**: rows with an error and duplicate rows are skipped, the rest are imported.
6. **Import.** You watch the progress and the result: how many contacts were created, updated, assigned to the event, skipped, and how many failed. The report is available here too. Every finished import appears in **Import history** below the wizard, together with its report.

The **Import mode** decides what happens to contacts that already exist in the workspace (they are matched by e-mail):

- **Fill missing data** (default) — leaves existing contacts as they are and only fills in a missing preferred language and empty custom fields. New contacts are created.
- **Overwrite data with non-empty values** — overwrites the name, company, phone, and other details of existing contacts with the values from the file. An empty cell never erases anything.

In both modes, groups are only added; an import never removes a contact from a group. The e-mail address is never overwritten, because it is the key used to match contacts.

Validation marks as an **error** a missing or invalid e-mail address, more than 20 groups in one cell, and a group name longer than 100 characters. A **duplicate** is the same e-mail address appearing a second time in the same file; only the first row is imported. A row without a language passes and just gets the default language. The file can have at most 20,000 rows and 50 MB, the header row with the e-mail column must be within the first 100 rows, and cells with formulas need a stored value (save the file in Excel or replace the formulas with values).

The preferred language matters at import time because Happenee uses it when sending the Invitation e-mail and e-mail campaigns. Fill the Language column with a two-letter code (`cs`, `en`); Happenee also accepts forms such as *čeština* or *english*. Where the language is missing, the **Default language** from the Upload step is used; it does not overwrite a language an existing contact already has.

### The contacts table: search, columns, and filters

You can tailor the contacts table to whatever you are working on:

- **Search** — the **Search contacts** field searches by name, e-mail, event, or group. If you enter an event name, you get the list of contacts assigned to that event.
- **Columns** — the **Columns** button opens the **Column settings** panel ("Choose the columns you want to see in the table."), where you tick what to show. **Last name and first name** and **E-mail** are always on and cannot be turned off; you can optionally add Events, Groups, Company, Company ID, Phone, Job title, and your custom contact fields. Confirm with **Apply**. Click the arrows in a column header to sort.
- **Filters** — the filters above the table match the **columns you have turned on**: as soon as you add the Company column, a Company filter appears. You can combine filters and clear them all with **Clear filters**.

Columns and filters are linked on purpose — whatever you show as a column, you can filter by. This helps before a bulk action: filter down to exactly the contacts the action should apply to (for example by group or company), and only then select them.

### Assigning a contact to an event

Creating a contact in the workspace does not assign it to an event — that is a separate step. You handle assignment from the contacts table using bulk actions:

- **Select one or more contacts** with the checkbox in the row — a bulk action bar appears above the table.
- Click **Event assignment** in that bar, adjust which events the selected contacts belong to in the list that opens, and confirm.
- **Through a group** — on the Groups tab, select a group and use **Event assignment** to assign the whole group to an event in one step; every member of the group is assigned.

A single **Event assignment** action covers both adding and removing at once. Removing a contact from an event does not delete it from the workspace — it stays in the central database and simply stops being tied to that event.

### Editing a contact

You edit a specific contact through the pencil icon in its row — this opens the **Edit contact** side panel with four tabs:

- **Basic information** — first name, last name, e-mail, company, job title, phone, company ID, preferred language, and a photo (square, 1:1 ratio).
- **Custom fields** — the values of your custom contact fields.
- **Events** — which events the contact is assigned to; you add and remove assignments right here (use **Search event** to find one).
- **Groups** — which groups the contact belongs to; adjust membership with the checkboxes (use **Search group** to find one).

The panel works as a complete record for one contact — details, events, and groups managed in one place, without bulk actions. Save your changes with **Save**.

### Deleting a contact

You delete a contact either in bulk (select it in the table → **Delete contact**) or from the edit side panel. A contact can be deleted only if it **has no groups or events assigned** — while it still has any, the button stays disabled and the edit side panel explains why. So first remove the contact from all groups and events, and only then delete it.

Deletion is permanent and removes the contact from the entire workspace. If you only want it out of a single event, do not delete it — just remove it from that event (see above).

### Managing groups

You create groups in the **Groups** tab (inside Contacts and groups).

1. Click **+ Add group** (or **Create new group**).
2. Enter the group name (for example, *VIP*, *Speakers*, *Brno*, *Partner Siemens*).
3. Save.

Groups are **global to the workspace**. Local groups (unique to a single event) are not available today.

### How a contact ends up in a group

There are three ways:

- **At import time** — with a `#Group name` column, or with a column of group names mapped to **Groups from value**. A group that does not exist yet is created.
- **Manually in the contacts table** — select the contact or contacts and use the bulk action **Add or remove from groups**, then pick the group (the same action also removes them from a group). You can also adjust one contact's membership in the edit side panel, on the Groups tab.
- **Automatically through the Registration form** — when an attendee picks an answer, they are assigned to a group based on that answer. You configure this on the answer (see *How conditional questions work in the Registration form*).

### What groups are used for

Groups serve four main purposes in Happenee:

- **Targeting communication** — you can target an e-mail campaign to selected groups. The Invitation e-mail does not support targeting by group.
- **Controlling visibility** — content features (Agenda, Speakers, Custom content) and engagement features (Notifications, Polls, Survey) can be shown only to selected groups.
- **Conditions in the Registration form** — both a question and a specific answer can be shown only to selected groups, and an answer can assign the attendee to a group.
- **Reporting** — attendee statistics can be filtered by group.

## Common pitfalls

### Groups are created only after registration is already running, and the organizer realizes they want to target communication while attendees are already in the form without any distinction

Plan the group structure **before** you launch registration. Think through who you will want to differentiate, and create the groups so the Registration form can assign them automatically. After the fact you can still assign groups in bulk, but it is manual work.

### The import overwrote the details of existing contacts because the organizer chose **Overwrite data with non-empty values** when they only wanted to fill in what was missing

Keep the default **Fill missing data**: it leaves existing contacts alone and adds groups just the same. Choose overwriting only when the file carries newer data than the workspace. The Validation step shows how many existing contacts the import will touch, and the report carries a warning for each of them that it will be updated.

### The import created a new group next to an existing one because the name differed by a typo

Groups from an import are created automatically and matched by name, ignoring letter case. A typo in a `#` column header or in a cell mapped to Groups from value creates a new group. Before you confirm, go through the **Newly created groups** list; if you see a group you already have, fix the file and upload it again.

### A contact listed on two rows ended up in only some of the groups

Validation marks the second occurrence of an e-mail address in a file as a duplicate and skips that whole row, including the groups and details it carried. Merge rows with the same e-mail address into one before you upload.

### A contact is created in the workspace but is not assigned to an event, so the organizer cannot see them in the registration list and cannot invite them

Always assign a contact to the event after you create it — one at a time, through a group, or right during the import with **Optional event assignment**. The assignment is a separate step from adding the contact to the workspace.

### Foreign guests received a Czech invitation because the file had no Language column and the default language stayed on Czech

The import never leaves the language empty: where it is missing, it uses the **Default language** from the Upload step. For a mixed list, fill in the Language column on every row; for a single-language list, setting the default language correctly is enough. Both the Invitation e-mail and e-mail campaigns are sent according to this setting.

### Expectation that a group from one event is visible only in that event — groups are global

Groups today exist only at workspace level. If you need to differentiate groups across events, name them with a prefix (*Conference25_VIP*, *Workshop25_Speakers*).

### The Delete contact button is disabled

A contact cannot be deleted while it still has any groups or events assigned — Happenee blocks this so a deletion does not break data for a running event. Remove the contact from all groups and events (with the bulk action, or in the edit side panel on the Groups and Events tabs). In the panel, save the changes; only then can you delete the contact. If you only need the contact out of a single event, do not delete it — remove it from that event instead.

## Related articles

- [What is a workspace and what is an event](https://help.happenee.com/en/articles/1-what-is-a-workspace-and-what-is-an-event)
- [Navigating the Happenee admin](https://help.happenee.com/en/articles/2-navigating-the-happenee-admin)
- [What to set up first after creating an event](https://help.happenee.com/en/articles/3-what-to-set-up-first-after-creating-an-event)
- [Creating a new event](https://help.happenee.com/en/articles/9-creating-a-new-event)
- [Setting the primary language of an event](https://help.happenee.com/en/articles/10-setting-the-primary-language-of-an-event)
- [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility)
- [Setting up the Registration form](https://help.happenee.com/en/articles/13-setting-up-the-registration-form)
- [How conditional questions work in the Registration form](https://help.happenee.com/en/articles/14-how-conditional-questions-work-in-the-registration-form)
- [Managing accommodation and roommate selection](https://help.happenee.com/en/articles/16-managing-accommodation-and-roommate-selection)
- [How nominations and nominators work](https://help.happenee.com/en/articles/17-how-nominations-and-nominators-work)
- [Targeting communication by groups and statuses](https://help.happenee.com/en/articles/43-targeting-communication-by-groups-and-statuses)
- [How Networking works](https://help.happenee.com/en/articles/36-how-networking-works)
- [How the Invitation e-mail works](https://help.happenee.com/en/articles/39-how-the-invitation-e-mail-works)
- [When to use the Invitation e-mail vs. an E-mail campaign](https://help.happenee.com/en/articles/42-when-to-use-the-invitation-e-mail-vs-an-e-mail-campaign)
- [How check-in and QR-code scanning work](https://help.happenee.com/en/articles/47-how-check-in-and-qr-code-scanning-work)
- [Printing badges](https://help.happenee.com/en/articles/48-printing-badges)
- [Preparing data for accommodation providers](https://help.happenee.com/en/articles/49-preparing-data-for-accommodation-providers)
- [What to do when groups or visibility are not working](https://help.happenee.com/en/articles/61-what-to-do-when-groups-or-visibility-are-not-working)
- [How custom contact fields work](https://help.happenee.com/en/articles/76-how-custom-contact-fields-work)
- [Adding an attendee manually](https://help.happenee.com/en/articles/77-adding-an-attendee-manually)
- [Setting up Partner API keys](https://help.happenee.com/en/articles/95-setting-up-partner-api-keys)
- [Setting up Tickets](https://help.happenee.com/en/articles/18-setting-up-tickets)

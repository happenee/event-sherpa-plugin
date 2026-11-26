# Building an attendee report

> Select attendees and columns from several sources for one XLSX file, save templates, and understand empty cells and multiple values.

- Article in the Help Center: https://help.happenee.com/en/articles/99-building-an-attendee-report
- Česká verze: https://help.happenee.com/cs/articles/99-sestaveni-reportu-ucastniku
- Collection: Reporting and post-event work
- Updated: 2026-10-26

---

> [!info] Overview
> An attendee report combines selected data from one event in a single XLSX file. Filters determine which attendees you include, and columns determine which details you receive. Each attendee has exactly one row; you can save a column selection as a template for reuse.

## Getting started

1. Open your event and **Statistics and reporting**. In the **Exports** section, find **Attendee reports** and select **Open reports**.
2. Choose a built-in or saved template. To build your own, select **New template**: the column editor opens right away with first name, last name, and e-mail already selected. Add the details you need, set their order, and confirm the selection with **Apply**.
3. Choose groups, registration status, or check-in and confirm the filters with **Apply**. The default filter includes attendees whose status is **Attending**. To change the columns of an open template later, use **Edit columns**.
4. Check the preview and download summary. Select **Download report** to download your current selection, even if you have not saved a template. If you will need the selection again, save it with **Save template**.







## Details

### Templates and downloaded reports

A template saves columns, their order, and custom headers for the current event. It does not save filters, so check which attendees you include before each download. A downloaded report contains a snapshot of the data when you create it; later event changes do not update the file.

Built-in templates cover contacts and groups, registration form answers, session registrations, and voting with feedback. You cannot overwrite their original definitions; save your edited selection as a custom template. Templates belong to the event, and organizers with access to that event can edit them; a custom template shows its author and the date of the last change.

To rename an open custom template, select **Rename** next to its name. From the template's menu in the list, you can duplicate it or delete it after a confirmation; the menu also offers renaming. A deleted template disappears for all organizers of the event.



### Choosing attendees

Groups, registration status, and check-in determine the report rows. A draft filter takes effect only after you select **Apply**. Reset the filters to review all event attendees; the default Attending status does not include everyone. Test accounts excluded from Statistics are also excluded from the report.

### Choosing and ordering columns

Select individual fields or an entire source. Available details include contact information, groups, custom fields, registration form questions, specific sessions and their registrations or ratings, personal voting and feedback responses, and assigned tickets or registration links.

Search works without diacritics. Move selected columns by dragging them or using the arrows, and rename their headers when needed. The top-to-bottom order becomes the left-to-right order in XLSX. Select **Apply** to confirm your editor changes.

Selecting a whole source or one of its attributes also includes matching questions and sessions added later. Selecting specific items does not expand automatically. If a selected question or session is deleted, opening the template removes its column and shows a notice.

### Previewing, saving, and unsaved changes

The preview shows the first five rows. The downloaded file includes every attendee who matches the confirmed filters, with the same columns and order. Check the attendee count, column count, and filters in the download summary.

You can download an unsaved selection immediately. Save a new template with **Save template** and give it a name. Save changes to your custom template with **Save changes**, or save an edited built-in or custom template as a copy with **Save as new**. Switching templates or leaving with changes prompts you to keep or discard them. A new template whose preselected columns you have not changed is discarded without a prompt when you leave it. If another organizer changes a template at the same time, reopen the current template or save your own copy.



### Empty cells and multiple values

An empty cell means that a value is unavailable. The preview displays a dash, while XLSX keeps the cell empty. A missing answer does not remove the attendee from the report. Multiple groups, reservations, or answers are combined in one cell, separated by semicolons.

A single date is an XLSX date cell; multiple dates in the same cell are text. Prices and ratings are numbers, and other values are text. System headers use the administration language, while questions and other content use the event content language.

### Personal responses and tickets

Anonymous responses are not linked to an attendee. Until the event ends, personal voting and feedback responses are shown only for contacts of the signed-in organizer. Feedback uses the latest submission.

Several tickets assigned to one attendee remain in one row. Names and vouchers are combined, and prices after discounts are summed for that attendee's tickets. The total for a shared order is not assigned to each attendee.

### Report scope and sharing the file

The report covers one event. The view stays in the administration; give colleagues without access the downloaded file. Use the relevant separate export for accounting documents, individual scans, or other detailed output. A downloaded file may contain personal data, so share only the details needed for its intended purpose.

## Common pitfalls

### Session check-in is empty

Check-in data for an individual session is not yet available. Do not interpret an empty cell as absence. Event check-in is a separate field and filter.

### The preview shows only some attendees

The five rows help you check the structure. The total count and filters determine the full download; use the report summary to check the scope.

### One attendee has tickets in different currencies

These prices cannot be added together, so a download with price columns is stopped. Remove the price columns and use the relevant ticket or order export for detailed financial analysis.

### You have selected too many columns

The editor warns you at 60 columns, and the maximum is 200. New fields in an automatically expanding selection can also increase the count. Keep the columns relevant to the purpose of the report.

## Related articles

- [Interpreting attendee statistics](https://help.happenee.com/en/articles/51-interpreting-attendee-statistics)
- [Working with Orders and exports](https://help.happenee.com/en/articles/52-working-with-orders-and-exports)

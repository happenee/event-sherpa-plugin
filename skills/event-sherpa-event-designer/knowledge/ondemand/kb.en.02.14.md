<!-- source: kb.en.02.14 -->

---
title: "How custom contact fields work"
description: "Workspace-level fields that extend contact details beyond the standard set — where you define them, everywhere they show up, and why to create them before you open registration."
modules: ["ucastnici_skupiny_a_viditelnost"]
last_updated: "2026-08-07"
version: 2
---

> [!info] Overview
> **Custom contact fields** are text fields that extend contact details beyond the standard set (name, e-mail, phone, company, job title, and others). You define them once in **Workspace settings** and they are then **shared across every event** — you can use them in the registration form, during ticket purchase, as a column in the contact table, and as a placeholder in an e-mail. Create them before you open your first registration; they do not fill in retroactively.

## Getting started

1. Write down what you need to know about people **across events**, not just for one. Typically a salutation, a department, an internal employee ID, or a cost center for rebilling.
2. Check that it is not a standard field already. **Company** and **Company ID** are standard fields — recreating them as custom fields is a common mistake.
3. Create the field in **Workspace settings** on the **Custom contact fields** tab and fill in the name **for every language** you use.
4. Only then decide, in the registration form of a given event, whether the field appears and whether it is required.

## Details

### Workspace, not event

The field definition lives in the workspace, not in an event. That means a field you created for one conference is available to every other event from then on — and the value you fill in on a contact stays with that contact across events. When the same person attends three of your events, you enter their department or internal ID once.

That is also why it makes no sense to create a field for a one-off piece of information tied to a single event (*preferred workshop slot*, *T-shirt size*). Those belong in the **additional questions** of the registration form — those are tied to the event and the answer stays with it.

### Where the field shows up

- **Registration form** — custom fields form their own section below the standard contact fields, with the same three options *Required / Optional / Hide*.
- **Ticket purchase** — the field can also appear in the details the buyer fills in.
- **Contact table** — you switch a custom field on as a column with the **Columns** button, so you can filter and sort by it.
- **Contact import** — a custom field has its own column in the import template, so you can fill it in bulk from Excel.
- **E-mails and campaigns** — every custom field has a placeholder you can insert into the message body.

### Custom fields versus additional questions

The decision rule is simple:

- **a detail that holds for a person long-term and across events** — a **custom contact field** (workspace)
- **an answer that is valid for this event only** — an **additional question** in the registration form (event)
- **form branching by answer, or assignment to a group** — an **additional question** — custom fields cannot do this

Custom fields are text. When you need a choice from options, a consent, a date, or conditional logic, you are in additional questions.

### Filling in several languages

The field name is entered separately for each language. If the event runs in both Czech and English and you fill the name in one language only, the other language group sees an empty or untranslated label. After creating a field, always switch the language and add the second version.

## Common pitfalls

### Creating Company or Company ID as a custom field

Both are **standard** contact fields in the registration form. Recreate them as custom fields and you end up with two company columns in the contact table, two differently filled values, and a mess in the export. Before you create a field, go through the standard set: E-mail, First name, Last name, Phone, Job title, Company, Company ID, Country, Twitter (X), LinkedIn.

### Creating the field after the first registrations

You can add a custom field at any time, but it does not fill in retroactively. Anyone who registered earlier will have the value missing, and you can only add it by editing contacts one by one or by importing from Excel. On a larger event that means hours of extra work — so create fields during setup, not when you notice they are missing from a report.

### Using a field for one-off event information

A T-shirt size, a menu choice, or a preferred workshop are not properties of a contact — they are answers about one event. Enter them as custom fields and they will hang on the contact through every future event, where they will only confuse you. They belong in the additional questions of the registration form.

### Looking for the field definition inside an event

Inside an event you only find the toggle that decides whether custom fields appear in the form. You create and rename the field itself in **Workspace settings**. If you cannot see a field there, it has not been created — it is not hidden.

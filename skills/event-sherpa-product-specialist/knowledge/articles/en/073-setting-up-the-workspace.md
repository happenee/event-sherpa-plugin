# Setting up the workspace

> What you configure at the workspace level — your account and two-factor authentication, company information, the e-mail and microsite footer, custom contact fields, GDPR, files, integrations, and invoices.

- Article in the Help Center: https://help.happenee.com/en/articles/73-setting-up-the-workspace
- Česká verze: https://help.happenee.com/cs/articles/73-nastaveni-workspace
- Collection: Getting started with Happenee
- Updated: 2026-08-16

---

> [!info] Overview
> **Workspace settings** is the one place where you configure everything that applies to **all of your events at once** — your user account, company information, the default e-mail and microsite footer, custom contact fields, personal data protection, and connections to external systems; shared **Files** and the **Invoices** overview have their own items in the left menu. You set these up once before your first event and rarely return to them. Some of them you cannot change yourself — customer support does, so plan for them in advance.

## Getting started

You reach these settings from the left menu at the workspace level, which has five items: **Events**, **Contacts and groups**, **Workspace settings**, **Files**, and **Invoices**. Workspace settings itself has four tabs: **User account**, **Custom contact fields**, **Personal data protection**, and **Integrations**.

The recommended order before you create your first event:

1. **User account** — check your name, the administration interface language, and turn on two-factor authentication.
2. **Company information** — if anything is wrong, write to customer support; you cannot change it yourself.
3. **E-mail and microsite footer settings** — the default text that carries into every event.
4. **Custom contact fields** — if you plan to track anything extra on contacts, create the fields now. You can add them later, but the data you have already collected will be missing.
5. **Personal data protection** — you should not open registration without it.

Steps 4 and 5 are the ones that hurt if you skip them. The rest you can catch up on any time.

## Details

### Workspace versus event

The workspace is your organization's environment — it holds contacts, groups, and every event. Workspace settings apply across events; event settings apply to that one event only. The split is stable: GDPR, custom contact fields, shared files, and the contact database are **workspace**; the agenda, the registration form, speakers, and sponsors are **event**.

### User account

The **User account** tab holds your first and last name, the **Administration interface language** (the language you see the admin interface in — unrelated to the event's content languages), and **Two-factor authentication (2FA)**. The interface language has two values, Czech and English.

Two-factor authentication is **Disabled** by default; you turn it on with **Enable two-factor authentication** next to the status. You confirm it with an **authentication app** such as Google Authenticator: the admin shows a QR code, you scan it in the app, and you finish with **I've added the code – Turn on**. From then on you enter a time-limited code from the app along with your password. Happenee offers neither SMS verification nor backup codes, so **you need a phone with an authentication app** — plan for that before you turn it on.

If employees or clients register through this workspace, turn it on — the admin account can see contact details for every attendee across every event.

**This is not where you change your password.** **Change password** sits in the menu that opens when you click your account name at the very bottom of the left column, next to logging out.

Today a workspace has **one administrator account**. Splitting it into several users with their own access rights is still in development, so for now expect the login to be shared by everyone on the team who needs the admin.

### Company information

The **Company information** section holds your organization's billing and identification details plus **Code** — an internal workspace identifier that is read-only. Alongside the company name it carries the **Sender name**, the **Reply-to name and e-mail**, and two fields for the **ICS file** (the calendar invitation) — in other words, the values your attendee e-mails go out with. The same details fill in the privacy policy template, where you appear as the data controller.

Company information is **set by customer support**. When your company name or address changes, write to them; you cannot edit the fields in the admin. You can override them for an individual event in that event's settings.

At the bottom of the **User account** tab there is one more card, *Odkazy na brandovanou účastnickou aplikaci* (its heading is currently shown in Czech even in the English admin) — links to the iOS app, the Android app, and the web app under your own brand. The look of the app itself (white label) is not set here — customer support turns it on.

### E-mail and microsite footer

The default footer text carries into the e-mails and the microsite of every event in the workspace. There are two fields — **Microsite footer** and **E-mail footer** — and you fill them in separately for each content language; an empty field shows **Not set**.

As with company information, customer support changes the **default values**. At the individual event level you can then override the footer — so if you need a different footer for one event only, handle it in that event's settings, not here.

### Custom contact fields

Text fields that extend contact details beyond the standard set. You define them in the workspace and they are shared with every event — you can use them in the registration form, during ticket purchase, and as columns in the contact table. Fill them in for every language you use. See [How custom contact fields work](https://help.happenee.com/en/articles/76-how-custom-contact-fields-work) for details.

### Personal data protection

The data processing terms an attendee acknowledges during registration and during ticket purchase, plus **consents beyond legitimate interest or contractual necessity** (marketing, photography, third-party offers). There is no point opening registration without this configured. See [Setting up personal data protection](https://help.happenee.com/en/articles/74-setting-up-personal-data-protection) for details.

### Files

A separate item in the left menu (not a settings tab): a central document store for the whole workspace. Upload a PDF or an image and you get a link you can point to from event content or from an e-mail. See [Working with workspace files](https://help.happenee.com/en/articles/75-working-with-workspace-files) for details.

### Integrations

The **Integrations** tab manages how your workspace connects to external systems. Today you issue **Partner API keys** there — access keys your other system (a CRM, a registration tool, a sales channel) uses to authorize against Happenee. You set permissions on each key separately, so an integration only gets what it needs. See [Setting up Partner API keys](https://help.happenee.com/en/articles/95-setting-up-partner-api-keys) for details.

### Invoices

The **Invoices** item in the left menu shows **every invoice across all events** in the workspace — it only matters if you sell tickets somewhere. It is a regular admin page with the left menu.

You filter the list by year, month, invoice type, and event, or with the full-text **Filter** field; each record shows the invoice number, type, issue and taxable supply dates, variable symbol, event, total with VAT, and customer, and you can download the document as a PDF. For accounting there is a bulk **Download ISDOC** above the table; on an individual row ISDOC only appears for some document types, so do not count on it for advance invoices.

Do not confuse this with orders inside an event: there you handle a specific order, its billing details, and refunds. Invoices in the workspace is where you download the documents for all of your events in one place at the end of the month.

### Exporting contacts

You export the whole contact database with the **Contacts (Excel)** button. Do not look for it in Workspace settings — it is in the **top right corner of the Contacts and groups page**. It is useful before a migration, as a backup, or for handing data over to a CRM.

## Common pitfalls

### Looking for GDPR or custom contact fields in the event settings

Both live at the **workspace level**. Inside an event you only find the toggles that decide whether the consents and the custom fields appear in the registration form — you cannot write the terms or define the fields there. When you cannot find either one, first check which level of the admin you are standing on.

### Leaving a change to company information or the default footer until the last minute

Customer support changes both, not you. When your company is renaming itself or unifying its branding, write to support **before** you send the invitations — there is no way to rewrite the footer in e-mails that have already gone out.

### Looking for the password change or the contact export in Workspace settings

Neither is there. **Change password** is in the menu under your account name at the bottom of the left column, and the **Contacts (Excel)** export is in the top right corner of the **Contacts and groups** page. The *User account* tab only changes your name, the interface language, and two-factor authentication.

### Confusing the administration interface language with the event's content languages

The administration interface language decides what language you see the Happenee admin in. It has nothing to do with the languages an attendee sees the content in — those are set on the event and switched with the flags in the top right corner. You can perfectly well run the admin in Czech and the event in English only.

### Creating a custom contact field after the first registrations

You can add a field at any time, but it does not fill itself in retroactively. Anyone who registered before you created it will have that value missing, and you can only add it manually or by import. So decide what you need to know about your contacts before you open registration.

## Related articles
- [Navigating the Happenee admin](https://help.happenee.com/en/articles/2-navigating-the-happenee-admin)
- [Setting up personal data protection](https://help.happenee.com/en/articles/74-setting-up-personal-data-protection)
- [Working with workspace files](https://help.happenee.com/en/articles/75-working-with-workspace-files)
- [Setting up Partner API keys](https://help.happenee.com/en/articles/95-setting-up-partner-api-keys)
- [How custom contact fields work](https://help.happenee.com/en/articles/76-how-custom-contact-fields-work)

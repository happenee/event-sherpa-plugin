# Setting up personal data protection

> Data processing terms at the workspace level — the Happenee template versus your own document, adding further processors, and consents beyond legitimate interest in the registration form.

- Article in the Help Center: https://help.happenee.com/en/articles/74-setting-up-personal-data-protection
- Česká verze: https://help.happenee.com/cs/articles/74-nastaveni-ochrany-osobnich-udaju
- Collection: Getting started with Happenee
- Updated: 2026-08-16

---

> [!info] Overview
> **Personal data protection settings** is the workspace-level section where you decide which data processing terms an attendee sees — either the prefilled template from Happenee, or a link to your own document. The same section is where you add **further processors** and **consents beyond legitimate interest or contractual necessity**, meaning optional consents such as photography or marketing. You configure it once for the whole workspace, and the attendee acknowledges the terms both during registration and during ticket purchase.

## Getting started

Decide two things, ideally with whoever handles data protection at your organization:

1. **Whose document you will use.** The Happenee template is the fast path for organizations that have no wording of their own. If your legal team insists on the company document, switch to your own and add the URL.
2. **Which optional consents you will collect.** Typically photography, marketing messages, or passing a contact to a partner. Word each consent so that it makes sense on its own — the attendee sees it as a checkbox at the end of the registration form.

Set both up **before you open your first registration**. A consent added later does not apply to people who registered earlier.

## Details

### Where the setting shows up

The terms appear to the attendee in two places: **before the registration form is submitted** and **during ticket purchase**. The setting is shared across the workspace — every one of your events works with the same document.

### The Happenee template

**Use a pre-prepared template from Happenee** inserts ready wording with the basic details already filled in. The template fixes the roles: **Happenee acts as the processor** of personal data and **the event organizer is the controller** — and the controller's name and contact e-mail are taken from what you have in the *Company information* section of your workspace settings. **View template** shows you exactly what the attendee will see.

This option suits organizations that have no event-specific wording of their own and do not want to write one for a single event.

### Your own document

Switching to **Use your own document** replaces the template with a link to your own text. A field labelled **URL with your own personal data protection terms** appears below the options; you paste the address and confirm with **Save**. Typically you point at a page on your website or at a PDF. If the document is not published anywhere, you can upload it to **Files** in the workspace and use the public link.

Whichever wording you choose, **name Happenee s.r.o. as one of the processors** — the admin says so itself. Happenee provides the platform's technical infrastructure and processes the data from registration and attendance, so it belongs in your own document just as it does in the template.

Choose your own document when your company has standard processing terms that must be identical across every channel.

### Further processors

With the pre-prepared template you can add **further processors** — parties that take part in processing attendee data alongside Happenee. In practice this covers an event partner, or a supplier who arranges accommodation or transport for you and receives the attendee list.

Each processor has two fields: **Processor name** and **Default display during registration**, with the values *Show* and *Hide*. The second one controls whether the processor's name is spelled out to the attendee during registration or stays inside the text of the terms. You can edit or delete a processor at any time.

Add processors to match reality. If data leaves Happenee — typically as an export for a hotel — the recipient belongs on the list.

### Consents beyond legitimate interest

The **Consents beyond legitimate interest or contractual necessity** section holds **optional** consents that are not a condition of registering. They appear to the attendee at the end of the registration form as separate checkboxes.

Typical uses:

- publishing photos and video from the event,
- sending marketing messages,
- passing a contact to a partner or an exhibitor,
- profiling and personalized offers.

You add each consent separately with **Add consent field** and **fill it in for every language** the event uses. A consent has a single field — its **text**, the sentence the attendee sees next to the checkbox. You can edit or delete it later; **you cannot hide it temporarily at the workspace level** (the *Show / Hide* setting belongs to processors, not to consents).

So you control visibility **at the individual event level** — in the registration form you decide whether the consents appear at all. The set of consents is shared across the workspace; where they show up is controlled per event.

### Getting the consents out

To find out who granted which consent, use the exports on the event — one of them is a separate file with the consents beyond legitimate interest. It is useful when you want to filter out people who did not agree to photo publication before you post a gallery.

## Common pitfalls

### A consent gets "switched off" for one event by deleting it

Consents are shared across the whole workspace and **cannot be hidden** — deleting is irreversible and takes effect everywhere. When you do not want a consent on one event, do not delete it: turn consents off in that event's registration form, or simply leave it and accept that the attendee will not tick it.

### Automatic registration on paid events collects no consents

If you choose automatic registration on a paid event, the attendee never goes through the registration form — which means the optional consents never appear either. When you need consent for photography or marketing, choose registration with additional information rather than the automatic type.

### Adding a consent in one language only

Consents are filled in separately for each event language. If you write the text in Czech only and the event also runs in English, an English-speaking attendee sees an empty or untranslated field. After adding a consent, always switch the language and check the second version.

### Using an optional consent as a mandatory condition

Consents beyond legitimate interest are optional by design — an attendee can leave them unchecked and still complete the registration. Do not put anything in them that the event cannot run without. If you absolutely need to know something like a dietary restriction, it belongs in the additional questions of the registration form, not in the consents.

### Treating a change of document as retroactive

If you switch from the template to your own document mid-registration, or change the document's content, everyone who registered earlier agreed to the older wording. Time any substantial change between events rather than in the middle of an open registration.

## Related articles
- [Setting up the workspace](https://help.happenee.com/en/articles/73-setting-up-the-workspace)
- [Setting up the Registration form](https://help.happenee.com/en/articles/13-setting-up-the-registration-form)
- [Working with workspace files](https://help.happenee.com/en/articles/75-working-with-workspace-files)

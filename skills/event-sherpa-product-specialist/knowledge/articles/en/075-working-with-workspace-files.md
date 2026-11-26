# Working with workspace files

> The central document store in the workspace — uploading a file, the difference between the public and the private link, and when to use Files instead of external storage.

- Article in the Help Center: https://help.happenee.com/en/articles/75-working-with-workspace-files
- Česká verze: https://help.happenee.com/cs/articles/75-prace-se-soubory-ve-workspace
- Collection: Getting started with Happenee
- Updated: 2026-09-09

---

> [!info] Overview
> **Files** is the central document store in the workspace, shared across every event. You upload a PDF, an image, or a presentation — up to **5 MB** — and get a link you can point to from event content, from an e-mail, or from the microsite. Every file has both a **public link** and a **private link** — the difference decides whether anyone can open the document or only a signed-in attendee.

## Getting started

You find Files as a separate item, **Files**, in the left menu at the workspace level. Uploading takes three steps:

1. Click **Upload file** and pick the document from your computer. It has to fit into **5 MB**.
2. Once it is uploaded, copy the link — the **public** one for anything that anyone with the link may see, the **private** one for anything that should stay behind a sign-in.
3. Paste the link where you need it: into custom content on the microsite, into the body of an e-mail, or into a URL field.

Decide up front whether the document belongs in Happenee at all. If it lives on your company website and you already maintain it there, link to it directly — two sources of the same PDF means two versions that will drift apart.

## Details

### When to use Files and when to use external storage

Happenee does not require you to host documents with it. You can link anywhere — SharePoint, Google Drive, your company website. **Files** makes sense in three situations:

- The document exists **only because of the event** (the agenda as a PDF, a venue map, competition rules) and you maintain it nowhere else.
- You need a link that **outlives** the colleague who owns the shared drive.
- You want everything for the event in one place so that someone else on the team can find their way around.

Documents that have an owner elsewhere — terms and conditions, the privacy policy on your website, an annual report — should stay where they are.

### Public and private links

Every uploaded file gives you two addresses:

- **Public link** — anyone who has it can open it. Use it for anything you do not mind having out in the open: the agenda, a map, downloadable presentations, your own data protection document.
- **Private link** — only **signed-in attendees** can open the document. It is not an internal admin link; it is how you make material available to the people at your event and to nobody else.

The private link is a proper tool, then, not a fallback. It suits material that belongs to attendees and no one else — speaker decks, a contact list, workshop handouts.

The choice between them is substantive, not cosmetic. A public link protects nothing except through the obscurity of its address, so anything sensitive belongs behind the private one. And the other way round: a private link sent to someone who has not signed in yet means a question in your inbox instead of an open document.

### Formats and size

You can upload ordinary documents, spreadsheets, presentations, images, and archives — specifically `.PDF`, `.DOC`, `.DOCX`, `.RTF`, `.TXT`, `.XLS`, `.XLSX`, `.PPT`, `.PPTX`, `.XML`, `.JPG`, `.JPEG`, `.PNG`, `.GIF`, `.ZIP`, `.RAR`, `.TAR`, `.MP4`, and `.AVI`.

**The limit is 5 MB per file**, and it is the main constraint to plan around. Video will not realistically fit, even though `.MP4` and `.AVI` are on the list; the same goes for larger archives and photo-heavy decks. **Files is a store for documents, not for media** — put video on a streaming service and link to it, and keep large bundles on external storage.

### Where a file link is useful

- **Custom content on the microsite and in the app** — a tile that opens a PDF when clicked.
- **E-mails and campaigns** — a link in the body instead of an attachment. A link avoids the attachment size. However, a new file version gets a new address and does not change an e-mail already sent.
- **Personal data protection** — if you use your own document but have not published it anywhere, upload it here and use the public link.

### Updating a document

The **Edit** action on a file changes **its name only** — you cannot replace the contents. When a document changes — a shifted agenda, a corrected map — you upload it again as a **new file**, which means you also get a **new link**.

That has a real consequence: you have to replace the new link everywhere you pointed to the document — in content, on the microsite, and in scheduled campaigns. **E-mails that have already gone out with the original link cannot be rewritten**, so a document that will keep changing after the invitations go out does not belong in Files. Link to it from somewhere you can rewrite the contents under the same address — your company website, a shared drive.

Before deleting the old version, keep in mind that the link you have already sent out stops working too. If someone may still click it, send the new address first.

## Common pitfalls

### Pasting the private link into an invitation

An attendee who has not signed in yet cannot open the document, and instead of an agenda you get a question in your inbox. The private link assumes a sign-in, so it does not belong in an e-mail aimed at people who have not registered. Before you paste a link into an invitation or a campaign, open it in a private browser window — you will see exactly what a recipient without a sign-in sees.

### Maintaining the document in two places

Typically when an organization has the agenda on its website and also uploads it as a PDF to Files. After the first schedule change the versions drift apart and attendees run into both. Pick one source of truth and link to it from everywhere.

### Sending an attachment instead of a link

Sending the agenda as an e-mail attachment looks convenient, but you cannot fix an attachment afterwards, and it raises the odds of the message landing in spam. Replacing the contents of a workspace file requires a new upload and a new link; it does not rewrite the address in an e-mail already sent. For a document that will keep changing, use a managed page or storage service that lets its owner update the contents under the same address.

### Trying to upload video or a large bundle to Files

The 5 MB per-file limit will not allow it, even though `.MP4` and `.AVI` are among the permitted formats. Plan for it: host video on a streaming service and put a link to it in your content, and leave bulky material on company storage. Files is for documents — the agenda, a map, terms, a deck.

## Related articles
- [Setting up the workspace](https://help.happenee.com/en/articles/73-setting-up-the-workspace)
- [Setting up personal data protection](https://help.happenee.com/en/articles/74-setting-up-personal-data-protection)
- [Using Custom content (FAQ, map, info blocks)](https://help.happenee.com/en/articles/25-using-custom-content-faq-map-info-blocks)

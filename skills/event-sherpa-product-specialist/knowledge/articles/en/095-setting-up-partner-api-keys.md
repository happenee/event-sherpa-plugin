# Setting up Partner API keys

> Issuing a key for the Partner API on the Integrations tab — sandbox and production keys, the seven permissions, revoking a key, and when a connection beats an import.

- Article in the Help Center: https://help.happenee.com/en/articles/95-setting-up-partner-api-keys
- Česká verze: https://help.happenee.com/cs/articles/95-partnerske-api-klice
- Collection: Getting started with Happenee
- Updated: 2026-08-07

---

> [!info] Overview
> **Partner API keys** are the access keys your other system — a CRM, a sales channel, a registration tool — uses to authorize against Happenee. You issue them in **Workspace settings** on the **Integrations** tab, and you set **permissions** on each one separately, so an integration gets exactly the scope of data it needs. The usual reason: your attendees and sold tickets live somewhere else and you want to check people in through Happenee without importing them by hand every time.

## Getting started

Before you issue a key, decide three things:

1. **What the integration needs to do.** Only read attendees to sync them into a CRM, or create them as well? The scope maps onto permissions, and you can narrow those at any time.
2. **Sandbox or production.** A sandbox key is for development and testing, a production key for live traffic. **The type cannot be changed after the key is created**, so plan for it — otherwise you will be issuing the key again.
3. **Who gets the key.** A key is access to attendee data. It belongs with the developer or the vendor building the integration, not in a shared chat.

Issuing it is short: on the **Integrations** tab click **New API key**, name it (the name is only for you — describe what is being connected, for example *CRM integration*), pick the type, tick the permissions, and confirm.

The technical description of the interface — endpoints, request formats, error states — is what your developer will find in the **Partner API documentation**, linked straight from the tab's info bar.

## Details

### Where the tab is and what it manages

**Workspace settings → Integrations.** This is a workspace-level setting, so a key applies across all of your events, not just one. The permissions follow the same logic: let an integration read attendees and it sees the attendees of every event in the workspace.

### Sandbox and production

Each key has a **Type**:

- **Sandbox** — for developing and testing the connection.
- **Production** — for live traffic.

The split has a practical point: a vendor can work on the integration with a sandbox key and only receive the production key once the connection is finished. The type **is absent from the edit panel** — it does not change after creation, so moving from testing to production means issuing a new key.

### The seven permissions

Permissions are ticked individually, and all of them are on by default when you create a key. Narrowing them is up to you:

- **Events read** — the list and details of events in the workspace.
- **Attendees read** — reading attendee records.
- **Attendees write** — creating and editing attendees.
- **Sessions read** — reading the agenda.
- **Sessions write** — writing to the agenda.
- **Certificates read** — reading certificates.
- **Users read** — reading user records.

Write access is offered only for attendees and sessions; events, certificates, and users are **read-only**. Use the read/write split — an integration that only feeds data into your CRM does not need to write anything back.

*(The Czech admin names the agenda permissions differently: **Sessions read / write** appears there as **Program čtení / zápis**. It is the same permission.)*

### The list of issued keys

The table on the tab shows each key's **Name**, **Type**, **Key**, **Permissions**, **Status**, and creation date. The key value itself is masked — you only see the last four characters, which is how you recognize it. **So save the full value right after generating it**, into a password manager or straight into the configuration of the system that connects.

The status is **Active** or **Revoked**. A revoked key stays in the list, so there is always a record of what existed when.

### Editing and revoking a key

Each row has two actions. **Edit API key** opens a panel where you change the name and the permissions — useful when an integration turns out to need more or less than expected. The second action **revokes** the key; the key is not deleted, it switches to *Revoked*.

Narrow permissions as you go. When the scope of an integration changes, editing the existing key is easier than explaining later why a vendor still has access to data they no longer need.

### When to use the API and when to import

The API earns its keep when data moves between systems **repeatedly and without a human in the loop** — continuous registration sync, checking in attendees who bought a ticket elsewhere, updating the agenda from an external tool.

For a one-off transfer an import is simpler and faster: you upload the contact list from Excel in **Contacts and groups** and you need no developer. If you are unsure, start with the import and reach for the API once it turns out you are doing it over and over.

## Common pitfalls

### Generating the key and saving it nowhere

The list then shows only the last four characters. Copy the full value immediately and hand it over safely — through a password manager, not by e-mail or chat. If the value is lost, the way out is to issue a new key and revoke the old one.

### Picking the type "just for testing" and expecting to change it

Sandbox and production do not switch after creation. If you know the integration is heading for live traffic, plan for the production key being a separate record — and leave the sandbox one active until the connection is finished.

### Giving a key every permission so that "it just works"

They are all ticked when you create a key, so it is easy to leave them that way. But a key applies to the whole workspace, meaning every event and every attendee. Tick only what the integration actually does — and if you are unsure about write access, start with read only and add it once it proves necessary.

### Letting a key circulate around the team

A key has no owner and no person's name on it, so once a vendor moves on there is nothing to tell you who still has it. Issue a separate key for each connection and name it after the system, not the person. When the work ends, revoke the key.

## Related articles
- [Setting up the workspace](https://help.happenee.com/en/articles/73-setting-up-the-workspace)
- [Managing contacts and groups in your workspace](https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace)
- [How check-in and QR-code scanning work](https://help.happenee.com/en/articles/47-how-check-in-and-qr-code-scanning-work)

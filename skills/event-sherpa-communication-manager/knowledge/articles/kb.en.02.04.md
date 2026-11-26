<!-- source: kb.en.02.04 -->

---
title: "Setting the registration type and additional questions"
description: "Where and how to set the registration type and additional questions, and how they combine with Tickets."
modules: ["registrace"]
last_updated: "2026-09-02"
version: 3
---

> [!info] Overview
> The registration type is set in **Event settings → Access and registration settings**. This is a setup-level article — it assumes you have already decided on a strategy (see *Choosing the right registration type*). This article describes where to find each setting, what the limits are, and how the types combine with Tickets and additional questions.

## Getting started

- The decision layer (public / closed / nomination, approval yes/no, automatic / with additional information) lives in *Choosing the right registration type* in the Getting started collection. If you have not gone through it yet, start there.
- In **Event settings**, review the **Basic event settings**, **Access and registration settings**, and (if you have Tickets) **Tickets** sections.
- The registration type after purchase (automatic / with additional information) is configured separately on Tickets.
- Some settings (allowed/blocked domains, default account settings) require **customer support**.

## Details

### Registration type for Tickets

In **Event settings → Tickets** (after you turn on the **Tickets** toggle), you choose one of two options:

**Registration with additional information.** The buyer can purchase tickets without knowing the attendees' e-mail addresses. After payment, the buyer receives a tax document and an e-mail with links for completing the registration. Each ticket is generated only after the registration form is filled in. If the buyer enters an attendee's e-mail address, the link goes directly to the attendee.

**Automatic registration after ticket purchase.** The buyer must enter an e-mail address for every ticket at the time of purchase. Attendees are automatically registered once payment is completed and receive a confirmation e-mail with the ticket attached.

> With **Automatic registration after ticket purchase** on a paid event, the registration form **and the consents beyond legitimate interest** (extra GDPR consents) are not used. If you need to collect additional data or extra consents, choose **Registration with additional information**.

For free events, the registration type after purchase is irrelevant — registration always goes through the Registration form.

### Approved registration

In **Event settings**, on the **Basic event settings** tab, the **Access and registration settings** section holds **Approved registration**. You pick one of two cards:

- **Inactive (default)** — the attendee receives the Confirmation e-mail and access to the event content immediately after registering.
- **Active** — after registering, the attendee receives an e-mail saying the registration is pending. They get access to the event content only after you approve it manually; approved attendees then receive a confirmation, rejected ones receive a notification e-mail.

> Approved registration **cannot** be combined with Tickets. If Tickets are turned on, the Approved registration section is disabled.

### Where registrations are approved

Once you turn Approved registration on, a new **Attendee approval** item appears in the event admin — in the **Tools** dropdown at the bottom of the left menu, and as a tile in the *Tools* section on the **Overview**. Do not look for it in **Registration**; that is a different screen.

The item is conditional: without Approved registration turned on, it is not in the menu. On events with Tickets, **Orders** sits in its place. Because the two features are mutually exclusive, you always see only one of them.

The screen is a list of registrations. Each row shows the contact, the date and time they registered, and the current state; above the list there is a search field and a filter for whether the contact has a note. Both columns can be sorted.

You decide **one by one**: every row carries three radio buttons for the state — pending, approved, and rejected. There is no bulk action across selected rows, so allow time for larger numbers. Because these are radio buttons, you can change a state afterwards; that does not take back e-mails that have already gone out.

For Approved registration, you need a clear process for who approves, and how quickly — otherwise attendees wait and start asking. The alternative is open registration without approval combined with groups.

### Event visibility in the attendee app

Who sees in the attendee app that the event exists:

- **Only for contacts assigned to the event** (default) — the attendee must be assigned to the event in contact management or register through a public link.
- **For all contacts in Contacts and groups** — everyone in the workspace sees that the event exists. Useful for internal company events where you want all colleagues to see the lineup.

### Access to the event in the attendee app

How the attendee gets into the event content in the app:

- **Only after filling in the Registration form** (default) — the attendee must complete registration before access is granted.
- **Without filling in the Registration form** — clicking the event grants access right away and sets the attendee's status to **Attending**. Useful for internal events where you do not want to force colleagues to fill in anything.

The combination *for all contacts* + *without the form* gives a fully open event for the whole company.

### Registration restrictions

In the **Registration restrictions** section, you choose where registration can come from:

- **No restrictions** (default) — anyone with the link can register.
- **Only assigned contacts** — even with a public link, only contacts assigned to the event in advance can register.
- **Allowed domains only** — registration only from company e-mail domains. The list of domains is set up by customer support.
- **Block registration from specific domains** — the opposite: blocks e-mail addresses from selected domains. The list is also set by customer support.
- **Default account (workspace) settings** — a global rule for every event in the workspace. Set by customer support.

You can also configure:

- **Maximum number of attendees.**
- **Registration deadline** (date and time after which registration closes).
- **Allow attendees to cancel registration** (and optionally a date by when).

### Where the attendee cancels, and when it is possible

When you turn on **Registration cancellation** (Not allowed / Allowed until a date), the attendee can cancel their registration themselves — in the **attendee app** (mobile and web), or on the **microsite** via their personal link from the e-mail. The button is labeled *Cancel registration*.

This option exists **only on a free event** — the *Registration cancellation* section appears in the settings only when **Tickets** are off. On a paid event, canceling participation is not handled as self-service cancellation by the attendee but on the organizer side — with **Refund order** in **Orders**.

### Additional questions and the "automatic vs. with additional information" logic on a free event

On a **free** event, you face an analogous choice — do you only need contact details from the attendee, or do you need additional information (transportation, catering, accommodation, workshop)?

- If contact details are enough, keep the Registration form simple (the Contact details tab with the required-field setting).
- If you need more, add **Additional questions** (the tab in the Registration form). Details are in *Setting up the Registration form*.

The difference between automatic and with-additional-information on a free event is in fact whether the Registration form has any additional questions or not — there is no separate toggle as on Tickets.

## Common pitfalls

### Approved registration is on, but there is no clear internal process. Registrations pile up and attendees ask why no confirmation arrived

If you do not have a person or team assigned to do approvals, do not turn Approved registration on. The alternative is open registration plus groups that categorize attendees after the fact.

### Automatic registration after ticket purchase is on for a paid event, even though you need extra consents (marketing consent, photography)

With Automatic registration after ticket purchase, the Registration form and the consents beyond legitimate interest are not used. Choose **Registration with additional information** instead.

### A domain restriction is on but not communicated to attendees. People register from personal e-mail addresses and cannot get through

State clearly in the Invitation e-mail and on the microsite which domains can register. If you need to add or remove domains, contact customer support.

### You set every restriction up front and then even you are not sure which ones apply

Restrictions stack. Visibility and access in the app apply at the level of the attendee's account in the app; registration restrictions control who can sign up through the microsite. Test on your own account before opening the event to the public.

### *Without the Registration form* is on and you expect attendees to still see the registration flow

*Without the Registration form* means the attendee gets straight into the event by clicking it (status set to Attending). If you need to collect consents or data, do not use this option.

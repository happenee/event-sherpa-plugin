<!-- source: kb.en.05.02 -->

---
title: "Printing badges"
description: "Print badges from the Service app over Bluetooth on a Brother QL-820NWB. Set the badge size, content, and larger font for large badges without a QR code."
modules: ["checkin_a_tisk_jmenovek"]
last_updated: "2026-10-15"
version: 5
---

> [!info] Overview
> You can print a badge in the Service app **after a QR scan**, when the app offers to print on the paired printer, or **on demand from the attendee detail or list**; automatic printing happens **only in Kiosk mode** after self-service check-in. Printing uses a **Brother QL-820NWB** thermal printer paired over Bluetooth and **contact details from Contacts and groups**. For a standard **large badge (80 × 50 mm) without a QR code**, you can select a larger font in the event administration; normal font size remains the default. If you do not own a printer, arrange a rental in advance through customer success.

## Getting started

- Decide which **badge size** you will use: large **80 × 50 mm** (allows a QR code) or small **70 × 29 mm** (no QR).
- Decide **what goes on the badge** alongside first and last name: company, job title, a note — or nothing.
- Decide whether to **print a QR code on the badge** — worth it if you plan to use the **Attendees** engagement feature in the attendee app (QR scanning for Networking). Turn on QR printing in the print settings in **On-site check-in**.
- For a **large badge without a QR code**, also choose the font size — a larger font uses the space left by the QR code to make the name easier to read.
- If you are **renting the printer from Happenee**, agree on the delivery date and payment with customer success.
- **Test the day before** — the Bluetooth pairing, the badge size set on the printer, and the print quality. Besides **Print test badge** in the Service app's *Settings*, print a few real badges from the attendee detail, including the longest names and your selected extra field.

## Details

### When a badge prints

- **After a QR scan** in Staff mode — staff scan the QR and, with a paired printer, the app offers to print.
- **On demand from the attendee detail** — the **Print badge** button. Use it to print (or reprint) without a scan.
- **By swiping a row in the list** — the **Print badge** action prints straight from the **Attendees** list.
- **In Kiosk mode** — the badge prints automatically after a self-service check-in.

Staff peel the badge off and stick it onto the lanyard the attendee is wearing.

### Pairing the printer

You pair the printer in the app: in *Settings*, open **Connect badge printer** (or the **Printer** row on the event's start screen), put the printer into pairing mode, and tap **Pair new printer**. When it appears in the list, select it and confirm. If pairing does not work, the app points you to the manual route through **Settings → Bluetooth** on the device.

One printer is paired with one phone or tablet. **Switching to a different device drops the pairing**, so you have to re-pair.

### The Brother QL-820NWB printer

The standard recommended model. It prints thermally — no ink, just a roll of badges in the right size. If you do not own one, **Happenee rents one out** at the current rate. The agreement and the details (delivery, deposit, return) go through customer success — plan **with lead time**.

### Badge sizes

Two standard sizes:

- **Large badge (80 × 50 mm)** — fits first name, last name, an extra field, and a **QR code**. Use it when you want a QR for Networking.
- **Small badge (70 × 29 mm)** — fits first name, last name, and possibly one extra field. **A QR code does not fit** — physically too small.

The badge size **must be set correctly inside the printer** — see *Common pitfalls*.

### Turning on a QR code on the badge

If you have permission to change the event's print settings, you can turn the QR code on or off yourself in **On-site check-in**. QR printing is available only for the **large badge (80 × 50 mm) with normal font size**. Turning on the QR code automatically sets the font size to normal.

Switching to the **small badge (70 × 29 mm)** turns off the QR code and resets the font size to normal. The QR option stays visible but is disabled, with an explanation of the limitation. When you return to the large badge, the QR code stays off until you turn it on again.

### Font size for a large badge without a QR code

In the event administration, open the print settings in **On-site check-in** to find **Font size**. This setting appears only for a **large badge (80 × 50 mm, H50) without a QR code**:

- **Normal** — the default setting, which keeps the original badge layout.
- **Larger** — an optional layout that uses the space without a QR code for a larger first and last name.

If you switch to a **small badge (70 × 29 mm, H29)** or the badge starts printing a **QR code**, the setting automatically saves as **Normal** and the font-size option disappears. When you return to a large badge without a QR code, you must select **Larger** again.

### Long names with the larger font

The larger font fits the name and extra text to the available space: the name can use two lines, and a long first name may be shortened to an initial. Enter the first and last name in separate contact fields. Before the event, print badges for your longest names and company names and check that they are readable and complete.

### What is printed on the badge

The badge always prints **first and last name** (required). On top of that you pick **one** extra field:

- **Company** — fits B2B events, client events, conferences.
- **Job title** — fits professional conferences, networking nights.
- **Note** — a free-text field on the attendee profile (typically dietary info, role, dress code).
- **None** — first and last name only.

The data is pulled from the **contact details in Contacts and groups**. If an attendee filled in *Company* but you set the badge to print *Job title*, that field stays blank. Confirm in advance that attendees filled in what you plan to print.

### When to print a QR code on the badge

**Only when you plan to turn on the Attendees engagement feature in the attendee app** (Networking with QR scanning). Attendees scan each other's QR codes from the badges to save the contact. If you do not use that feature, a QR on the badge has no purpose. A QR **can only be printed on the large badge (80 × 50 mm) with normal font size**. For the mechanics, see [How Networking works](../03_content-and-attendee-experience/16_how-networking-works.md).

### Printing without a scan — quickly adding an attendee

When a walk-in arrives, register them right in the Service app with **Add attendee** (on the **Attendees** list) and then print their badge with **Print badge**. The same is possible in the web **Check-in** tool. Details in [How check-in and QR-code scanning work](01_how-check-in-and-qr-code-scanning-work.md).

## Common pitfalls

### The larger font disappears or the badge prints differently

Check that you have selected the **large badge (80 × 50 mm)** without a QR code and selected **Larger** again. Switching to a small badge or printing a QR code resets the font size to **Normal**.

If your event uses a **custom badge layout**, the larger font does not apply to it. Discuss the layout of such badges with customer success.

### Printing fails — badges do not print, or come out blank

The most common cause is **the wrong media size set inside the printer**. The printer keeps its own size configuration, which has to match the loaded roll (80 × 50 or 70 × 29). Before the event, test by hand — load the roll, set the size, and use **Print test badge** in the app's *Settings*.

### A staff member turns on the printer, scans a QR, and nothing prints

Check the **Bluetooth pairing** between the device and the printer. Switching operators (a different phone) drops the pairing — re-pair through **Pair new printer**, or via **Settings → Bluetooth** on the device.

### The organizer sets the badge to print Company, but the badges only show names — Company is missing

The data comes from the contacts. If attendees did not fill in Company (or it was not a field on the Registration form), the system has nothing to print. Make sure the field exists on the form and that attendees filled it in.

### The organizer wants to print a QR code on the small badge

On a small badge, the QR option stays visible but is disabled. To print a QR, select the **large badge (80 × 50 mm)** and turn the QR code back on; normal font size will apply.

### Only one printer arrives on event day and it jams

Keep a **backup printer** and a backup roll of badges. For larger events, two print stations are worth it — for redundancy and higher throughput.

### The organizer orders the printer rental from Happenee at the last minute and it does not arrive in time

The rental through customer success is not instant — there is logistics, a deposit, and a return. Order **at least 10 days in advance**.

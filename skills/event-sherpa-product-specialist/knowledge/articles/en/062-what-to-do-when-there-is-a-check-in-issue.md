# What to do when there is a check-in issue

> What to do for typical check-in issues: a missing QR code, a duplicate scan, a walk-in.

- Article in the Help Center: https://help.happenee.com/en/articles/62-what-to-do-when-there-is-a-check-in-issue
- Česká verze: https://help.happenee.com/cs/articles/62-co-delat-pri-problemu-na-check-inu
- Collection: Troubleshooting
- Updated: 2026-11-04

---

> [!info] Overview
> At check-in, a QR code is missing, a scan is duplicate, staff do not see a group after a scan or in the attendee detail, or a walk-in arrives. You handle most of these straight in the **Service app** (the **Attendees** list — find by name, check in, add a walk-in) plus the right place type; resending a ticket and showing the QR are available in the web **Check-in** tool in the admin.

## Getting started

Keep both at the entrance: the **Service app** on a phone or tablet (scanning plus the attendee list) and the web **Check-in** tool open on a laptop for what the app cannot do.

## Details

### Typical situations and fixes

**The attendee has no QR code.** In the Service app, on the **Attendees** tab, find them by name and **Check in** them, and print a badge if needed. If they need the ticket resent or the QR shown on screen, use the web **Check-in** tool — the app does not have these two yet.

**Duplicate scan (already checked in).** A place of type **Check-in** returns an *Already checked in* warning on the second scan. If repeated scanning makes sense (coat check, bus, zone entry), set that station to **Recurring check**. For a one-time check (voucher, gift), use **One-time check**.

**A group is missing from the attendee detail or scan result.** Check that the attendee belongs to the group. In the event admin, open **On-site check-in** and add the group to the **Display attendee group after scanning** setting. Although the setting name mentions scanning, the selection also applies to the **Attendee Detail** in the Service app. Other workspace groups do not appear automatically.

**The group appears in the detail but not after a scan.** Check the group's *Show on places* setting and the place selected in the Service app. Place restrictions apply only during scanning; an empty selection means every place. The attendee detail does not apply place restrictions.

**A walk-in on site.** In the Service app, use **Add attendee** (e-mail, first name, last name, company, job) — once saved, you check them in and print a badge right away. The same is possible in the web Check-in tool (**Quickly add a new attendee**).

### Prevention

- **An hour before the event**, send an E-mail campaign with the QR ticket as a reminder — attendees will have the ticket in the most recent e-mail and the queue gets shorter.
- Check the **place type setup** the day before, not on the morning of the event.
- Verify that the printer (Brother QL-820NWB) is paired with the right device and that **large badges (80 × 50 mm)** are loaded — small badges (70 × 29 mm) cannot print a QR code.

## Common pitfalls

### The organizer wants to check attendees in for a specific workshop or zone — looking for *check-in by session*

Check-in by workshop or zone is not a native feature today. It is solved through **groups** — assign attendees to the workshop's group, set that group to show during scanning (you can limit it to the workshop door alone), and use place type **Recurring check**. Tying check-in directly to a session or time slot is on the roadmap.

### Staff expect to resend the ticket or show the QR in the Service app

The Service app can **find, add, and check in** an attendee, but it **cannot** resend the ticket or show the QR on screen. Handle those two in the web **Check-in** tool — keep it open at the entrance.

### A badge prints without a QR code

QR codes only print on **large badges (80 × 50 mm)**. Check the badge format in the printer and the size setting.

## Related articles

- [How check-in and QR-code scanning work](https://help.happenee.com/en/articles/47-how-check-in-and-qr-code-scanning-work)
- [Printing badges](https://help.happenee.com/en/articles/48-printing-badges)
- [Creating and sending an E-mail campaign](https://help.happenee.com/en/articles/41-creating-and-sending-an-e-mail-campaign)
- [How the attendee app and its home screen work](https://help.happenee.com/en/articles/34-how-the-attendee-app-and-its-home-screen-work)
- [What to do when an attendee without a QR is stuck in the queue](https://help.happenee.com/en/articles/66-what-to-do-when-an-attendee-without-a-qr-is-stuck-in-the-queue)

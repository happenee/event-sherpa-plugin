<!-- source: kb.en.02.09 -->

---
title: "How nominations and nominators work"
description: "Setting up nominators, delegation, capacity, contact imports, and the new portal."
modules: ["registrace"]
last_updated: "2026-10-29"
version: 6
---

> [!info] Overview
> Nominations let you divide contact management among nominators, such as sales representatives or assistants. The organizer sets their limits and permissions, and each nominator works in a separate portal. Nominating a contact does not complete their registration.

## Getting started

1. Open nominations in the event administration.
2. Add nominators individually or by import, then set their limits and permissions. If you don't know the specific person yet, create the account in **Claim via link** mode.
3. Decide whether pending nominations should also reserve places for companions.
4. Set up delegation for this event if someone needs to manage another nominator's contacts.
5. Send nominators access to the portal. You can also import contacts centrally for several nominators at once.

## Details

### Setting up nominator access

Use nominations when you want to distribute invitations and capacity among several people. The organizer can view nominators and update their settings later. Each nominator's available actions depend on their permissions, including sending invitations and managing groups.

From the nominator list, you can open a nominator's portal, copy their access link, or send access by e-mail. The link uses the same host as the administration you are working in. Older links to the original portal redirect to the new environment and preserve the language.

A nominator access link is used to claim an account or manage contacts, depending on the selected mode. Share it only with an authorized person; send attendees their own registration link or invitation instead.

### Choosing how to create a nominator




When adding a nominator, choose whether you already know the person or want to hand over the account through a link:

- In the default **Named nominator** mode, enter the nominator's first name, last name, and e-mail address.
- In **Claim via link** mode, you can leave all identity details and the note blank. The e-mail field is hidden. Set the limit and permissions, then copy the link and share it with the intended recipient.

You cannot change the mode after creation. The choice is available wherever you have access to nominations; no additional event setting is needed.

The recipient enters their first name, last name, and e-mail address. They then open the verification e-mail and confirm access on the page it links to. The account is assigned only after this confirmation; entering details or opening the e-mail does not assign it. The verification link expires after 30 minutes.



After the recipient submits the details, a confirmation appears and the form is hidden. If they entered incorrect details, they click **Enter details again** and correct them. Returning to the form does not send another e-mail. The recipient must wait at least one minute before requesting another verification e-mail.

Shared links expire 180 days after they are created. Each copy or export creates a new link without invalidating previous links. Share links and exported files only with the intended recipient.




Claiming preserves the limit, group, permissions, note, language, delegation, and existing nominations. In the nominator list, each account shows the status **Awaiting claim** or **Claimed**. Opening an administrator preview does not change the account owner.

Once claimed, the original shared link offers to send a new sign-in link to the owner's verified e-mail address. Another person cannot claim the same account again. Until an account has an e-mail address, you cannot send it access by e-mail from the administration; share the copied link instead.

### Working for other nominators and filtering contacts

The organizer sets up delegation, which decides who can work for each nominator. Delegation applies only to the selected event and has no start or end date.

A nominator can view their own contacts, all contacts they can access, or select a specific nominator. When sending invitations or managing groups, the permissions of the contact's owning nominator apply. Contact ownership stays unchanged: acting for another nominator does not transfer their contacts or capacity usage to the delegate.

### Understanding contacts and occupied places

The number of nominated contacts is different from the number of occupied places. A confirmed attendee occupies one place, plus the recorded number of companions. A pending nomination reserves one place, plus any companions configured by the organizer for pending nominations.

This reservation setting applies to the event's nominators. It defaults to zero companions and supports zero to four. For example, 10 pending nominations with one reserved companion each occupy 20 places. This setting does not determine how many companions an attendee may select during registration.

A contact marked as not attending does not count toward occupied places. If a reservation change exceeds a limit, existing nominations remain, but no more can be added until capacity is freed or the limit is increased.

### Adding contacts and custom fields

Nominators add contacts in a side panel. You can edit basic contact details only while the contact has not responded; this editing option is unavailable after they confirm or decline attendance. Custom fields are available when creating a contact and can also be edited separately in the contact details if the organizer has already created those fields.

Custom field values belong to the contact within the organizer's account, rather than to this nomination alone. Changing them can therefore affect the same contact on the organizer's other events. Editing basic details also changes the shared contact profile.

You can change group assignments in a panel, including removing assignments, only while the contact has not responded and the owning nominator's permissions allow it. Saving closes the panel and shows a confirmation. Groups organize contacts; this feature does not set capacity limits for individual groups within an event.

### Choosing an import method

- The nominator import in the administration creates nominators. Its optional mode column accepts `named` for a specific nominator and `claim` for claiming through a link. If the column is missing or empty, `named` applies and the first name, last name, and e-mail address are required. For `claim`, the first and last names are optional and the e-mail address must be empty. An entered e-mail address causes a row error.
- The attendee import in the nominations administration assigns contacts to nominators by e-mail address. Your file must include a nominator e-mail column, and you must map it. If the nominator does not exist for the event, the import creates them with default settings; check their limit and permissions afterward.
- Importing in the nominator portal adds contacts in the context of a selected nominator that the signed-in person can access.

Map file columns to the corresponding contact details. You can map custom fields that already exist for the organizer; including a field in the file does not create it.

The import in the nominator portal offers a mode for updating existing data. If a contact is already assigned to the selected nominator for this event, you can update them only while they have not responded. In this mode, nonempty imported custom field values can replace existing values, including values used on the organizer's other events. An empty cell does not clear the field or supply a default value. This update mode is not available in the central attendee import in the nominations administration.

### Sending invitations and changing attendance

Depending on permissions, you can send invitations individually or in bulk. Before sending in bulk, check the selected contacts and their invitation status.

A contact who has not registered should use the registration link in their invitation. You can also use that link to complete registration on the attendee's behalf. The attendance panel does not let you confirm attendance with a switch that skips the registration form. You can record that the contact will not attend.

For a confirmed attendee, you can change companions when settings and permissions allow it. A companion mapping to a registration question must be configured. The change also updates the relevant answer; reserving places for pending nominations does not replace this mapping. Happenee support can help configure it.

### Viewing statistics and exporting contacts

The nominator export uses `named` when the account has an e-mail address and `claim` when it does not. This also applies to an account that has already been claimed: importing it into another event creates a specific nominator with the listed e-mail address. Exporting does not change the original account's mode or sign-in process.

The portal shows a summary of nominations, attendance, and capacity, plus more detailed invitation, registration, and check-in status breakdowns. An invitation status, such as an e-mail being read, does not confirm attendance. Confirming attendance does not mean that the attendee has arrived at the event.

You can export contacts to Excel. The list, export, and status breakdowns respect the selected nominators and contact filters. Capacity usage, however, includes all nominations belonging to the selected nominators: searching or filtering by status does not reduce occupied places. When viewing several nominators, the portal does not show a single combined limit; select an individual nominator to assess their remaining places.

## Common pitfalls

### The recipient's verification link does not work or they entered the wrong e-mail address

The recipient returns to a valid shared link and requests a new verification e-mail. Before the account is claimed, they can enter a corrected address; an unverified typo does not assign the account. If they request messages repeatedly, they must wait as the message instructs. If the shared link has also expired or the page asks for a replacement, copy a new link in the administration and share it with them. If someone has already claimed the account or another nominator on the same event uses the address, the recipient cannot claim it; check the nominator list to see who the account or address belongs to.

### You cannot delete a nominator with nominated contacts

If a nominator has nominated contacts for this event, the system rejects the deletion and explains why. The nominator and contacts remain. Open their portal from the nominator list to manage the contacts; available changes depend on each contact's status and permissions.

### The contact belongs to another nominator

Adding the same contact to the same event cannot take over another nominator's nomination. The system rejects the addition without changing ownership or contact details. Use delegation for shared management.

### Required import mapping is missing

Check the attendee e-mail mapping and, for a central import, the nominator e-mail mapping. The import cannot proceed without required mappings. Review the wizard's warnings before starting; importing does not complete registration.

### Reserving places does not allow companions

Reserved places for pending nominations affect capacity usage only. Actual companions depend on registration and its settings. For a contact awaiting registration, a reserved companion is not a confirmed additional attendee.

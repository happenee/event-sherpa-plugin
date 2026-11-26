# How conditional questions work in the Registration form

> Conditional questions appear only after a specific answer, keeping the form short.

- Article in the Help Center: https://help.happenee.com/en/articles/14-how-conditional-questions-work-in-the-registration-form
- Česká verze: https://help.happenee.com/cs/articles/14-jak-funguji-podminene-otazky-v-registracnim-formulari
- Collection: Event setup and registration
- Updated: 2026-04-27

---

> [!info] Overview
> Conditional questions let you reveal an additional question only when an attendee picks a specific answer. The form stays short for people the next question does not concern, and asks only where it makes sense. Conditional questions are one of the areas where organizers most often make mistakes — especially in combination with group visibility.

## Getting started

- List which questions make sense for everyone and which only for some attendees. Typical example: if someone arrives by car, the bus questions do not concern them.
- Conditional questions are added **under a specific answer** of a parent question, not as a standalone question.
- They work on question type **2** (Select only one), **3** (Select only one or custom text), and other types with discrete answers.
- Before configuring, check that the parent question is already in place — the conditions hook onto a specific answer that has to exist on the list.

## Details

### Two distinct things that are easy to confuse

Two mechanisms inside the Registration form look similar but work differently:

- **Conditional questions** — the question appears to the attendee only after they pick a specific answer in the parent question. The check happens immediately, inside the form itself.
- **Question visibility for groups** — the question appears only to attendees who are in the selected groups. The check happens at the start (the attendee is or is not in the group), before the form even begins.

Conditional questions react to **what the attendee is doing in the form right now**. Group visibility reacts to **who the attendee is** (their assignment in the workspace, or what they get assigned after registration).

### How to add a conditional question

1. On the **Additional questions** tab, open the question you want to attach the condition to (typically a type 2 question — Select only one).
2. In the list of answers, find the **specific answer** you want to branch from.
3. Under that answer is a section **Conditions** / **When this answer is selected, show another question**.
4. Add a new question — pick the type, name it, and add answers if needed.

The conditional question is nested under the answer. If the attendee picks a different answer, the conditional question does not appear.

### What the attendee sees

The attendee opens the form and sees only the first (parent) question. As soon as they pick an answer, the next question or questions **appear dynamically** beneath it. If they switch to a different answer, the questions tied to the previous answer disappear and the questions tied to the new answer appear instead.

### A practical example

**Parent question (type 2):** *Where are you traveling from?*
- *Prague* — no conditional question.
- *Brno* — conditional question: *Are you taking the shared bus?* (type 2, answers *Yes / No*).
  - *Yes* — conditional question: *Which bus?* (type 6 with a capacity limit).
  - *No* — no further question.
- *Other* — conditional question: *Specify the place of departure* (type 1, free text).

An attendee from Prague sees only the first question. An attendee from Brno sees the first question and possibly the bus question. Conditions can be chained across multiple levels.

### Visibility of individual answers

On a type 2 question (and other types with discrete answers), you can show a **specific answer** to selected groups only. Example: a question *Do you want access to the VIP lounge?* with the answer *Yes* visible only to the **VIP** group. Other attendees do not even see the *Yes* option.

The difference from whole-question visibility: you hide just one answer, not the whole question.

### Assigning to a group based on the answer

Each answer on a type 2 question can have **Assign to group** set up. When the attendee picks that answer, the system automatically adds them to the listed group. The group must be created beforehand in **Contacts and groups**.

Example: the answer *Brno* assigns the attendee to the **Brno** group. You can then target the e-mail campaign *Information for travelers from Brno* at that group only.

This is also the most efficient way to categorize attendees by their answers without having to handle it manually after registration.

### Preview and structure

The form admin has a **Form preview** button (the form as the attendee sees it) and **Question structure** (an overview of every question and its conditions in a tree view). Before going live, walk through the structure and the preview — it is how you verify that the conditions show up the way you intended.

## Common pitfalls

### A conditional question is added as a standalone question on the list. The organizer then sets *Show question only to groups* and expects it to appear when an answer is chosen — but groups work differently from answers

Conditions are added **under a specific answer** of the parent question, not as a separate item. Open the parent question, find the answer, and add the linked question there.

### Group visibility and a conditional question are combined without being thought through. The question does not appear even though the attendee picked the right answer, because they are not in the right group

If the branching is by answer (the attendee's current action in the form), use a **conditional question**. If the branching is by attendee type (VIP, standard, speaker), use **group visibility**. Do not combine the two without a clear reason.

### The attendee picks one answer, fills in the conditional question, then changes the answer. The organizer expects the first answer to remain in the data

Changing the parent answer **removes** the previous conditional question along with its answer. Only the final state of the form stays in the data.

### Conditional questions are nested three or four levels deep. The form gets unreadable and the attendee gets lost

Two levels of conditions (question → sub-question → sub-sub-question) is the maximum that makes sense. If you need more, split the form into two phases or follow up over e-mail after registration.

### The group for the answer-based assignment does not exist because the organizer created it after the form went live. Attendees who registered before the group existed end up unassigned

Create the group **before** the form goes live. Even if you add it at the last minute, attaching the group to an existing answer **does not back-fill** earlier assignments — you have to do a bulk assignment manually in Contacts and groups.

## Related articles

- [Setting up the Registration form](https://help.happenee.com/en/articles/13-setting-up-the-registration-form)
- [Working with groups and visibility](https://help.happenee.com/en/articles/15-working-with-groups-and-visibility)
- [Managing contacts and groups in your workspace](https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace)
- [Setting the registration type and additional questions](https://help.happenee.com/en/articles/12-setting-the-registration-type-and-additional-questions)
- [Managing accommodation and roommate selection](https://help.happenee.com/en/articles/16-managing-accommodation-and-roommate-selection)
- [Preparing data for accommodation providers](https://help.happenee.com/en/articles/49-preparing-data-for-accommodation-providers)
- [What to do when groups or visibility are not working](https://help.happenee.com/en/articles/61-what-to-do-when-groups-or-visibility-are-not-working)
- [What to do when conditional questions do not display correctly](https://help.happenee.com/en/articles/89-what-to-do-when-conditional-questions-do-not-display-correctly)

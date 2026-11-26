# Using Custom content (FAQ, map, info blocks)

> A general-purpose content feature for anything that does not fit elsewhere (FAQ, a map, an info block).

- Article in the Help Center: https://help.happenee.com/en/articles/25-using-custom-content-faq-map-info-blocks
- Česká verze: https://help.happenee.com/cs/articles/25-pouziti-vlastniho-obsahu-faq-mapa-informacni-bloky
- Collection: Content and attendee experience
- Updated: 2026-10-13

---

> [!info] Overview
> Custom content is a **general-purpose content feature** for anything that does not fit into the other content features — FAQ, an informational text, a venue map, a company introduction, parking instructions, a link to an external site. You can add it multiple times within a single event, and each instance has its own name and content. On the home screen of the microsite and the attendee app it appears as a text block or an image; after a tap it can open a detail view or redirect to an external link.
> You can set separate text or images for the microsite, independently of the attendee app home screen. Upload mobile and desktop images for each language; the text or image mode applies to all languages of that instance.

## Getting started

- Map out **what your attendees are missing in the other content features** — FAQ, transportation directions, dress-code summary, list of accommodation options, venue map.
- Custom content is **not limited to a single instance** — you can have an FAQ, a map, and an info block all at once, each as its own tab.
- Decide how the tap behaves — **text in a detail view** or a **redirect to an external link**.
- For multi-language events, prepare translations in every language.

## Details

### Adding a Custom content instance

1. In the left menu, open **Content** → **+ Add** → **Custom content**.
2. Rename the instance from *Custom content* to a concrete name (*FAQ*, *Parking*, *Venue map*).
3. Set the content (see below).
4. Repeat for additional instances if you need them.

### What a Custom content instance can hold

Each instance has **three layers of content**:

**1. Display on the attendee app home screen** — what the attendee sees in the list of content and engagement features on the app's home screen. Two modes:

- **Text block** — a heading (the instance name) and a short intro text. Good for an FAQ (*"Frequently asked questions"* + two sentences) or for information (*"Parking"* + instructions).
- **Image** — you upload an image (separately for the mobile view and for the desktop / web version of the app). Good for venue maps or visual banners.

**2. Detail view** (what opens after a tap in the app):

- **Text in the detail view** — a rich-text editor. Formatted text, images, videos, links. Good for a long FAQ, transportation details, or an organization description.
- **External link (URL)** — a tap on the home screen redirects the attendee outside the app (for example to an external site, Google Maps, or a YouTube video).

**3. Display on the event microsite** — set independently for the microsite:

- **Show on the home page** — reuses the setting from the app's home screen (text or image).
- **Content shown in the detail view** — uses the detail-view content (from layer 2).
- **Custom content for the microsite** — separate text or an image used only on the microsite. You can keep a short text in the app and a long FAQ or a custom image on the microsite.

### Setting up a custom image on the microsite

1. In **Content**, open the relevant **Custom content** instance.
2. For the microsite display, select **Custom content for the microsite** and choose **Image**.
3. Use the language flag in the top-right corner of the event admin to switch to the language you are preparing images for. Upload both the image for mobile view and the image for desktop view.
4. Repeat the upload for other languages, then check the resulting microsite on mobile and desktop in each language.

**Text** is the default option. Changing the mode affects all languages of that instance. Switching modes keeps your saved text and images, so you can return to them later. Microsite images are managed separately from the attendee app home screen images.

### Common use cases

**FAQ.** A Custom content instance named *FAQ*, a short intro on the home screen, and the full list of questions and answers in the detail view. Format the body as: *Q: Question / A: Answer*.

**Transportation details.** An instance named *Parking and transport*, with text covering public transport, parking, and the address. You can add an image of a map.

**Dress code.** A short text with the rules. Useful for gala dinners and conferences.

**Venue map.** An instance with an image (the venue floor plan) on the home screen and a description in the detail view. Alternatively, an external link to a Google Maps embed.

**Organization introduction.** Text with a company profile, founder, and press materials. Useful for external client events.

**Link to an external site.** An instance that redirects to an external site (a livestream, registration for the next edition, a marketing site).

### Visibility

You can show Custom content to:

- All attendees (default).
- Selected groups only — typically for VIPs (exclusive information for VIPs), partners (a contact for the sponsorship team), or speakers (a technical briefing).

### Order and sorting

In **Event microsite** and **Attendee app settings** you can set the order of individual content features (including Custom content instances) by drag-and-drop.

### Multiple languages

Switch the language with the flag icon and fill in:

- Instance name
- Text for the home screen
- Text for the detail view
- Text for the microsite (if you set it separately)

For the microsite's custom image mode, upload language variants into the same instance after switching languages. Mobile and desktop images are saved separately for each language.

If an image is missing, the microsite first uses the same device variant in the event's primary language. Only if that is also unavailable does it use the other device variant. For example, if Czech is the primary language, the English microsite on desktop may show the Czech desktop image even though you uploaded an English mobile image. Upload both English variants for a fully English version.

## Common pitfalls

### The English microsite still shows a Czech image

Open the correct instance in the event, use the language flag in the top-right corner to switch the content language to English, and check both the mobile and desktop images in its custom content for the microsite. A missing variant may fall back to the primary language. After uploading, check the English microsite on both devices.

### Neither an image nor the original text appears in the microsite's image mode

Upload an image for the relevant language and device, or switch back to text mode. If no image is available, image mode does not show text as a fallback. A separate link button is unaffected.

### An FAQ written as one long wall of text with no structure, so the attendee cannot find what they are looking for

Format the FAQ as a list of questions and answers. Use bold for the questions and indented text for the answers. If the FAQ is long, consider splitting it into several instances (*Before the event*, *Event day*, *After the event*).

### An external link on the home screen points to a dead URL — attendees tap it and land on an error page

Check the link before publishing. Re-check external links regularly, especially when they point to campaign pages that expire over time.

### An organizer creates 10 Custom content instances for a small event and the app's home screen ends up overcrowded

Combine related information into a single instance with several sections in the detail view. For a small event, one to three instances are usually enough (typically FAQ + Parking + Organization).

### A venue map image is uploaded only for desktop, so the mobile app shows it badly or not at all

Upload a separate mobile version of the image. The dimensions differ by device.

### Custom content with sensitive information is shown to everyone even though it should have been visible only to VIPs

Before publishing, check **Visibility** on each instance. When you select *Selected groups only*, the content is hidden from attendees outside the group.

### A long detail-view text is filled in only in Czech, so a foreign attendee sees an English heading but a Czech body

Switch the language and fill in the content in every language the event supports. Incomplete translations come across worse than no translation at all.

## Related articles

- [How the Event microsite works](https://help.happenee.com/en/articles/21-how-the-event-microsite-works)
- [Setting up Venue and the event location](https://help.happenee.com/en/articles/22-setting-up-venue-and-the-event-location)
- [Adding an organizer contact](https://help.happenee.com/en/articles/24-adding-an-organizer-contact)
- [How the attendee app and its home screen work](https://help.happenee.com/en/articles/34-how-the-attendee-app-and-its-home-screen-work)
- [Recommended setup for an incentive trip or itinerary](https://help.happenee.com/en/articles/57-recommended-setup-for-an-incentive-trip-or-itinerary)
- [Working with workspace files](https://help.happenee.com/en/articles/75-working-with-workspace-files)

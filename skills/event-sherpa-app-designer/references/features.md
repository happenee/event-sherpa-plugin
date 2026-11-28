# Feature vocabulary

The closed list of features a `microsite_app_plan-v1` may name, with the
labels the admin shows. Use the `key` in the JSON and the label in every text
and step. A feature that is not in this list does not go into the plan; when
the input asks for one, record it in `open_items` with kind `verify`.

Modules are only Paid tickets, Registration form, Event microsite,
Invitation e-mail, Confirmation e-mail, E-mail campaigns, On-site check-in and
Attendee app (Czech: Placené vstupenky, Registrační formulář, Microsite
události, Zvací e-mail, Potvrzovací e-mail, E-mailové kampaně, Odbavení na
místě, Účastnická aplikace). Everything below is a content feature or an
engagement feature, never a module. Online module (Online modul) keeps the
word in its product name; it is still an engagement feature.

## Content features

Added in **Obsah → + Přidat**. Each can show on the microsite (a tab), in the
app (a home page tile) or both; visibility for groups applies in the app.

| key | Czech | English | Instances | Fields and settings the plan may use | KB |
|---|---|---|---|---|---|
| `agenda` | Program | Agenda | one per agenda, each its own tab | microsite tab of type Sessions; `display`: Náhled prvních 6 sessions s proklikem na celý program (`preview`) or Výpis všech sessions (`all`); Quick filtry na hlavní stránce; Zobrazit popis session v celé délce; Proklik na detail session; Zobrazit řečníky; Proklik na profil řečníka | 03.01, 03.21 |
| `speakers` | Řečníci | Speakers | see KB | microsite `display`: Náhled prvních 3 řádků řečníků (`preview`) or Výpis všech řečníků (`all`); profiles come from Compose or the brief | 03.01, 03.03 |
| `sponsors` | Sponzoři | Sponsors | see KB | sponsors and categories only as supplied | 03.12 |
| `exhibitors` | Vystavovatelé | Exhibitors | see KB | exhibitors and stands only as supplied | 03.13 |
| `venue` | Lokalita | Venue | one per event | fields `venue.name` (Název místa), `venue.phone`, `venue.website`, `venue.address`, `venue.image`, `venue.description` | 03.02 |
| `contact` | Kontakt | Contact | several | fields `contact.first_name`, `contact.last_name`, `contact.email`, `contact.phone`, `contact.image`, `contact.organizer` | 03.04 |
| `custom-content` | Vlastní obsah | Custom content | several, each renamed | fields `custom.tile_text` (Textový blok), `custom.tile_image` (Obrázek, mobile and web), `custom.detail_text` (Text v detailu), `custom.external_url` (Externí odkaz), `custom.microsite_text` (Vlastní obsah na microsite) | 03.05 |

## Engagement features

Added in **Engagement → + Přidat**. They show only in the app, never on the
microsite. Order, publication and the tile style are set in **Účastnická
aplikace**; visibility on the feature itself.

| key | Czech | English | Instances | Settings the plan may use | KB |
|---|---|---|---|---|---|
| `qr-ticket` | QR vstupenka | QR ticket | see KB | none | 03.24, 04.07 |
| `guest-qr-code` | QR Doprovod | Guest QR code | see KB | shows only when the registration form asks for a guest | 03.24 |
| `notifications` | Oznámení | Notifications | see KB | who sends (ops); which announcement when and its text come from Communicate | 04.08 |
| `polls` | Hlasování | Polls | once per event | Nové hlasování, Otázka nebo název hlasování, answer template; visible only after publication; results shown by publishing them | 03.24 |
| `questions` | Otázky | Questions | once per event | Schvalování otázek před veřejným zobrazením; Možnost zasílat otázky anonymně; Umožnit přidávat otázky ve webové aplikaci bez přihlášení; needs a moderator | 03.24 |
| `survey` | Dotazník | Survey | once per event | states Nepublikováno, Publikováno, Uzavřeno; no intro text field | 03.24 |
| `attendees-feature` | Účastníci (Networking) | Attendees (Networking) | see KB | Stav; Viditelnost; Zapnout soukromé zprávy; Zapnout rezervační systém schůzek (meeting places set up by customer support) | 03.16 |
| `registration-information` | Registrační údaje | Registration information | once per event | the description on the home page (default „Vaše údaje zadané při registraci“) | 03.24 |
| `online-module` | Online modul | Online module | several | some types set up by customer success | 03.18 |
| `my-agenda` | Moje agenda | My agenda | added with Agenda | Zobrazit na detailu události (set in each Agenda, off by default; the block then shows in the web app); visibility and order | 03.15 |
| `leaderboard` | Leaderboard | Leaderboard | see KB | set up by customer success, not in the self-service admin | 03.17 |

Every engagement feature can be renamed (**Změnit název**); the new name
shows on the app home page. Polls, Questions, Survey and Registration
information can be added only once per event (KB 03.24).

## Engagement on a session

Switched on the **Engagement** tab of a session type or a session, never in
the Engagement section. In the plan these are app entries with `placement:
session` and the Compose `blocks` they serve.

| key | Czech | English | KB |
|---|---|---|---|
| `session-rating` | Hodnocení session | Session rating | 03.24, 03.21 |
| `questions` | Otázky | Questions | 03.24, 03.21 |
| `anonymous-questions` | Anonymní otázky | Anonymous questions | 03.24, 03.21 |
| `polls` | Hlasování | Polls | 03.24, 03.21 |

Event level questions are one queue for the whole event and suit one room
and one stream; with parallel rooms, questions belong to sessions (KB 03.24).

## Where the microsite and the app are set up

| Part | Admin screen | KB |
|---|---|---|
| header image | Nastavení události → Nastavení grafiky: Ikona události s názvem a datem, or Vlastní obrázek hlavičky (optional mobile variant); shared with the e-mails and the app | 03.01 |
| intro text, registration button, thank you text | Microsite události: Úvodní text, Pozice registračního tlačítka (nahoře, uprostřed, dole, automaticky), Text na obrazovce po vyplnění a odeslání registračního formuláře | 03.01 |
| tabs | Microsite události: Publikace na microsite, order by dragging, Zobrazení (only Sessions and Speakers) | 03.01 |
| address and footer | Microsite události → Nastavení | 03.01 |
| app order, publication, tile | Účastnická aplikace: order by dragging, publication, Textový blok or Obrázek | 03.14 |
| visibility | the feature's panel Nastavení viditelnosti: všichni účastníci, or Pouze pro vybrané skupiny | 02.07 |
| session engagement | the session type or the session, tab Engagement | 03.21, 03.24 |

## What the creation tool can do

For a new event, `preview_event_creation` accepts `module_types` from
`locality` (Venue), `contact` (Contact), `sessions` (Agenda) and `speakers`
(Speakers). These are the tool's code names, not product terms. It creates
those features empty; the venue name is the only content it takes, from
the event's basic facts. They are not yet Published (Publikováno) in the
attendee app, but they already show in the microsite menu so the organizer
can check the microsite; never call them hidden. Nothing writes the intro text, tabs,
display, app order, tiles, feature content, engagement or visibility.

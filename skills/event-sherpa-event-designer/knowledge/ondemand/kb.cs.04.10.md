<!-- source: kb.cs.04.10 -->

---
title: "Komunikační flow v den události"
description: "Sekvence komunikace v den události: ranní e-mail s QR vstupenkou, push oznámení v aplikaci, kampaně pro nezaregistrované."
modules: ["notifikace", "komunikace_a_pozvanky"]
last_updated: "2026-08-07"
version: 3
---

> [!info] Krátce
> V den události se komunikace přesune z předregistračního e-mailingu na operativní vrstvu: **ranní reminder s QR vstupenkou** přes e-mailovou kampaň, **oznámení v aplikaci** v průběhu dne (změny programu, výsledky soutěží) a poslední **kampaně pro nezaregistrované**, kteří ještě stojí na pomezí. Cíl: zkrátit fronty u check-inu, držet účastníky v obraze a zachytit pozdní rozhodnutí. Připravit komunikaci je třeba dopředu — v den události se už nemá dělat copywriting, jen spouštět naplánované rozesílky.

## Jak začít

- Připravte si **timeline komunikace** den předem: ranní e-mail (T−1 h před začátkem), oznámení během dne, případně závěrečné poděkování po události (to už je follow-up, viz článek *Plánování follow-up komunikace*).
- Naplánujte **e-mailovou kampaň s PDF vstupenkou a QR kódem** na ráno události. Cíl: aby účastník měl vstupenku po ruce v prvních e-mailech, ne hluboko v inboxu.
- Připravte si **šablony oznámení** v účastnické aplikaci — alespoň jedno uvítací, jedno avizující změnu programu, jedno pro výsledky / soutěže.
- Mějte plán **fallbacku pro nezaregistrované**: poslední kampaň den před událostí pro ty, kteří se ještě nepřihlásili.

## Detail

### Ranní e-mail s QR vstupenkou

Standardně dostane účastník QR vstupenku v **potvrzovacím e-mailu** hned po registraci a má ji v účastnické aplikaci v sekci vstupenek. Problém: pokud se registroval před týdny nebo měsíci, e-mail se mu mezitím zanořil. V den události přichází ke vstupu a hledá ho ve frontě.

Řešení: **ráno události pošlete e-mailovou kampaň s aktuální PDF vstupenkou a QR kódem**. Kampaň nastavíte takto:

- **Cílení:** *Všichni přihlášení* (Účastní se / Attending). Tedy ne nezaregistrovaní, ne odmítnutí — jen ti, kdo přijdou.
- **Obsah:** krátký text *„dnes se vidíme, tady máte vstupenku, připravte si ji u vstupu“*, případně logistické info (parkování, vchod, čas registrace).
- **Příloha:** v nastavení kampaně zapnete **PDF vstupenka s QR kódem**. PDF vygeneruje systém pro každý kontakt unikátně.
- **Naplánujte odeslání** typicky **1 hodinu před otevřením registrace**, ne dřív (aby byl e-mail nahoře v inboxu, když účastník odjíždí na událost).

### Oznámení v aplikaci v průběhu dne

Pro účastníky, kteří mají staženou účastnickou aplikaci, je **Oznámení** rychlejší a méně rušivé než e-mail. Hodí se na:

- **Uvítání ráno** — *„Vítáme vás na události, registrace je od 9:00 v hlavním foyer.“*
- **Změny programu** — odložení sessionu, přesun do jiného sálu, výpadek řečníka.
- **Vyhlášení výsledků** — soutěž, hlasování, networking leader.
- **Připomenutí** — *„Networking break začíná za 10 minut v sále A.“*

Oznámení mají dvě cesty doručení: **push notifikaci** (vyskočí na zamčenou obrazovku telefonu) a zápis do feedu *Novinky / Oznámení* v aplikaci. Detaily v článku *Používání oznámení v účastnické aplikaci*.

Připravte šablony oznámení **dopředu** — v den události se nestihne formulovat. Stačí ne-finální draft, který před odesláním upravíte podle aktuální situace.

### Kampaň pro nezaregistrované — poslední pokus

Pokud máte ke dni před událostí v seznamu kontaktů *nezaregistrované* (mají pozvánku, ale neudělali registraci), poslední **e-mailová kampaň den před událostí** často přivede 5–15 % z nich. Cílení nastavíte jako *Nezaregistrovaní* nebo *Co si nepřečetli zvací e-mail*. Obsah: krátký reminder s argumentem, proč přijít, a registrační tlačítko vedoucí rovnou na formulář. Kampaň lze cílit i na ty, kteří **nezobrazili účastnickou aplikaci** (mobilní nebo webovou).

Pokud událost pracuje s placenými vstupenkami a registrace se den před událostí zavírá, naplánujte tuto kampaň **před deadlinem**, ne po něm.

### Sekvence: doporučený timeline

Většina událostí vystačí s touto sekvencí v den události:

1. **T−24 h** — kampaň pro nezaregistrované (poslední pokus, pokud ještě jde registrovat).
2. **T−1 h** — kampaň s PDF vstupenkou a QR pro všechny přihlášené.
3. **T+0** (otevření registrace) — uvítací oznámení v aplikaci.
4. **Průběžně** — oznámení o změnách programu / výsledcích / break-připomenutí.
5. **T+konec události** — krátké poděkování a info, že přijde follow-up (tomu se věnuje samostatný článek).

### Co dělat, když účastník nemá QR

V den události není vyhnutí — někdo dorazí bez QR (nestáhl si aplikaci, neotevřel e-mail, smazal). Pro tyto případy je **Prezence** ve webovém prostředí a **servisní aplikace** připravené:

- Personál v Prezenci vyhledá účastníka, znovu mu pošle vstupenku e-mailem (tlačítko *Znovu odeslat*), nebo ho odbaví ručně.
- V servisní aplikaci jde i **rychlé přidání nového účastníka** (jméno + příjmení), pokud někdo přijde, kdo nebyl v původním seznamu.

Detail v článku *Jak funguje check-in a skenování QR kódů*.

## Na co si dát pozor

### Ranní kampaň naplánovaná na 7:00 dorazí účastníkům, kteří už jsou na cestě a nemají signál

Plánujte odeslání tak, aby účastník měl e-mail **dostatečně dopředu před cestou**. T−1 h je často pozdě. Pro událost v 9:00 zvažte odeslání v 7:00 nebo i den předem ráno, pokud cesta na místo trvá ≥ 1 h.

### Kampaň s PDF vstupenkou jde i lidem, kteří se odhlásili nebo nedostavili

Cílte explicitně na status *Účastní se* (Attending), ne na *Všechny*. Bez cílení dostanou kampaň i ti, kdo registraci zrušili nebo neodpověděli, a vznikne zmatek.

### Oznámení v aplikaci se odešle před událostí, ale účastník v ní ještě není přihlášený. Push se neukáže

Push notifikace vyžaduje, aby měl účastník staženou aplikaci a alespoň jednou se do ní přihlásil. Pokud potřebujete oslovit i ty, kdo aplikaci ještě neotevřeli, použijte **e-mailovou kampaň** místo oznámení (nebo paralelně).

### Změna programu odeslaná jako oznámení s velkým časovým předstihem ztratí pozornost — účastník už si ji nepřečte v moment, kdy potřebuje

Kritické změny (výpadek řečníka, přesun sálu) posílejte **bezprostředně před momentem**, kdy se mají projevit. Oznámení s 6h předstihem zapadne, oznámení s 10min předstihem účastník zaregistruje.

### Den události se najednou musí udělat copywriting, protože šablony nejsou připravené

V den události se má **spouštět**, ne psát. Připravte si všechny e-maily a oznámení dopředu, ideálně s rezervou na last-minute úpravy. Provoz na místě nesnese delší texty psané za chodu.

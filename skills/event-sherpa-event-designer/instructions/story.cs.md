<!-- event-story story extension -->

Tohle je rozšíření pro tah, na kterém píšeš story: plné texty vždy načítaných článků kolekcí 01 a 02, krátký přehled článků na vyžádání a specifikace renderu. Platí spolu se systémovým promptem, nic v něm neruší.

Schéma výstupu v tomhle vydání v rozšíření není. Markdown story ho nepotřebuje: co a jak se tiskne, říká specifikace renderu níže a štítky ze `schema/labels.cs.json`. Objekt JSON dostane jen ten, kdo si o něj řekne („pošli Story JSON“ nebo „send the Story JSON“). Před takovou odpovědí si jednou přečti `schema/event_story.wire.json` v balíčku skillu, vedle `SKILL.md`: názvy polí jsou ty, které deklaruje, a platí i pro objekt `INSUFFICIENT`. `brief_confirmation.summary_digest` je `null`. Kde jádro píše, že schéma přijde s tímhle rozšířením, platí tenhle odstavec.

<!-- source: kb.cs.01.05 -->

---
title: "Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka"
description: "Microsite je veřejná stránka, účastnická aplikace prostředí pro registrované, a jak se v Happenee navazují."
collection: "Začínáme s Happenee"
subcollection: "priprava-setupu"
modules: ["microsite", "ucastnicka_aplikace"]
slug: "microsite-vs-ucastnicka-aplikace-jak-premyslet-nad-flow-ucastnika"
lang: "cs"
status: "published"
docId: 5
last_updated: "2026-04-27"
version: 1
tags: [microsite, aplikace, flow-ucastnika, zacatky, komunikace]
source_images_consulted: true
related:
  - "Co je workspace a co je event"
  - "Co nastavit jako první po vytvoření eventu"
  - "Jak funguje microsite události"
  - "Jak funguje účastnická aplikace a její hlavní stránka"
  - "Jak funguje zvací e-mail"
  - "Cesta účastníka z microsite do účastnické aplikace"
  - "Must-have, optional a advanced funkce a moduly podle typu události"
  - "Minimální doporučený setup pro malý, střední a větší event"
  - "Doporučené pořadí setupu eventu krok za krokem"
  - "Doporučený setup pro incentive / itinerář"
  - "Doporučený setup pro webinář a online event"
---

> [!info] Krátce
> Microsite a účastnická aplikace jsou dva hlavní kanály, přes které účastník komunikuje s vaší událostí. Microsite je veřejná webová stránka s informacemi o události — dostupná každému, kdo má odkaz. Účastnická aplikace je prostředí pro zaregistrované účastníky, dostupné jako webová verze i mobilní appka. Happenee je navržené tak, aby účastník přirozeně prošel z microsite přes registraci do aplikace — a každý kanál plnil svou roli. Pochopení tohoto flow pomáhá nastavit komunikaci, která účastníka nenutí, ale vede.

## Jak začít

- Rozhodněte se, zda u dané události využijete jen microsite, nebo microsite + aplikaci. Závisí to spíš na velikosti a komplexitě události než na jejím typu.
- Pochopte základní logiku: microsite slouží k informování a registraci, aplikace k samotnému prožití události.
- Obsah v Happenee nastavujete jednou — zda se jednotlivé obsahové funkce zobrazí na microsite, v aplikaci, nebo na obou místech, řídíte odděleně u každé funkce.

## Detail

### Co je microsite

Microsite je veřejná webová stránka vaší události. Má vlastní URL a je dostupná každému, kdo na ni přijde přes odkaz ze zvacího e-mailu, z kampaně, nebo ze sociálních sítí. Microsite plní dvě hlavní role:

- **Informační vitrína** — představuje událost, program, řečníky, místo konání, sponzory, FAQ a cokoli dalšího, co účastník potřebuje vědět před rozhodnutím, zda se zúčastní.
- **Vstupní bod do registrace** — odsud účastník pokračuje do registračního formuláře nebo k nákupu vstupenky.

### Co je účastnická aplikace

Účastnická aplikace existuje ve dvou podobách:

- **Webová verze** — běží v prohlížeči, není třeba nic instalovat.
- **Mobilní aplikace** — nativní aplikace pro iOS a Android. U většiny enterprise zákazníků — typicky bank, pojišťoven, IT firem a healthcare společností — je aplikace brandovaná (white label), takže si účastníci stahují vlastní aplikaci dané organizace pod jejím jménem a ikonou.

Aplikace je prostředí pro zaregistrované účastníky. Najdou v ní detailní Program, Moji agendu se svými zaregistrovanými sessions, Networking, Oznámení, Hlasování, Otázky z publika, QR vstupenku pro vstup a další engagement funkce, které jsou na microsite nedostupné nebo zjednodušené.

### Ideální flow účastníka

V Happenee jsou kanály navržené na sebe navázat v jednom flow:

1. Účastník dostane **krátký zvací e-mail** s výzvou k události.
2. E-mail ho vede na **microsite**, kde najde základní informace a zaregistruje se nebo koupí vstupenku.
3. Po registraci dostane **potvrzovací e-mail** s QR vstupenkou a s odkazy na stažení aplikace, případně na webovou verzi aplikace.
4. Další komunikace (aktuality, detaily programu, networking, den události) už probíhá primárně **v aplikaci**.

Správně postavený zvací e-mail je krátký a úderný. Jeho jediný cíl je dostat účastníka na microsite — ne mu sdělit všechna data najednou.

### Kdy stačí jen microsite

U menších nebo jednorázových událostí, kde si účastník jen stáhne vstupenku a přijde, může být microsite dostatečná. Typicky galavečery, jednorázové firemní události, malá setkání do desítek lidí. Aplikace v takových případech nepřidává tolik hodnoty, aby vyvážila překážku stažení.

<!-- SUPERSEDED: SUP-01a -->
### Kdy zapnout aplikaci

Jakmile má událost program, workshopy, networking, ankety nebo potřebu pouštět oznámení v průběhu dne, aplikace začíná dávat smysl. Platí vodítko: **čím větší a delší událost, tím větší přínos aplikace**. Konference, expo, vícedenní setkání, událost s workshopy — všechno jsou případy, kdy aplikace vede k hmatatelné úspoře času a lepšímu zážitku.

Aplikace není pro účastníky povinná. Někteří preferují webovou verzi, jiní si stáhnou mobilní. Vy jako organizátor jim ji jednoduše nabídnete v potvrzovacím e-mailu.

### Alternativní use case: microsite jen jako registrační formulář

U některých externích klientských událostí má organizátor **vlastní marketingový web** a Happenee microsite slouží pouze jako registrační vrstva — účastník přijde z firemního webu, vyplní e-mail, zaregistruje se a vrací se zpět. V tomto režimu se na microsite zobrazuje minimální obsah (často jen registrační formulář) a informace o události žijí na hlavním firemním webu.

Tento přístup má nevýhodu v tom, že **se ztrácí možnost zobrazit řečníky, program a další informace přímo v Happenee** — obsah se buď vyplňuje dvakrát (jednou na firemním webu, jednou v Happenee pro aplikaci), nebo se řeší synchronizace přes API. Ideální stav je použít microsite jako plnohodnotnou vizitku události. Alternativní režim je ale validní, pokud brand organizace vyžaduje, aby všechen obsah byl na firemním webu.

## Na co si dát pozor

### Snaha vměstnat všechny informace do microsite a aplikaci úplně vynechat, i když událost aplikaci potřebuje

Microsite má informovat a dostat účastníka do registrace. Aplikace má provést účastníka událostí. Když se obě role přenesou na microsite, ztratíte engagement a zahltíte ji.

### Prezentace aplikace jako povinnosti, což vytváří zbytečné tření

Nabídněte aplikaci jako službu — webovou i mobilní verzi. Ať si účastník vybere, co mu vyhovuje.

### Nejasné přechody mezi kanály. Účastník neví, kdy má použít microsite a kdy aplikaci

Držte se logiky: **před registrací microsite, po registraci aplikace**. Potvrzovací e-mail jasně vede do aplikace, další komunikace pak už hlavně přes aplikaci (oznámení, push notifikace).

### Předpoklad, že typ události jednoznačně určuje volbu. „Konference = aplikace, firemní večer = bez aplikace.“

Rozhodujte podle velikosti a komplexity, ne podle typu. Velká firemní konference aplikaci potřebuje, malý klientský workshop možná ne.
<!-- /SUPERSEDED -->

## Související články

- [Co je workspace a co je event](01_co-je-workspace-a-co-je-event.md)
- [Co nastavit jako první po vytvoření eventu](03_co-nastavit-jako-prvni-po-vytvoreni-eventu.md)
- [Jak funguje microsite události](../03_obsah-a-zkusenost-ucastnika/01_jak-funguje-microsite-udalosti.md)
- [Jak funguje účastnická aplikace a její hlavní stránka](../03_obsah-a-zkusenost-ucastnika/14_jak-funguje-ucastnicka-aplikace-a-jeji-hlavni-stranka.md)
- [Jak funguje zvací e-mail](../04_komunikace-a-pozvanky/01_jak-funguje-zvaci-e-mail.md)
- [Cesta účastníka z microsite do účastnické aplikace](../04_komunikace-a-pozvanky/07_cesta-ucastnika-z-microsite-do-aplikace.md)
- [Must-have, optional a advanced funkce a moduly podle typu události](06_must-have-optional-a-advanced-moduly-podle-typu-akce.md)
- [Minimální doporučený setup pro malý, střední a větší event](07_minimalni-doporuceny-setup-pro-maly-stredni-a-vetsi-event.md)
- [Doporučené pořadí setupu eventu krok za krokem](08_doporucene-poradi-setupu-eventu-krok-za-krokem.md)
- [Doporučený setup pro incentive / itinerář](../07_event-sherpa/05_doporuceny-setup-pro-incentive-itinerar.md)
- [Doporučený setup pro webinář a online event](../07_event-sherpa/07_doporuceny-setup-pro-webinar-a-online-event.md)

<!-- source: kb.cs.01.06 -->

---
title: "Must-have, optional a advanced funkce a moduly podle typu události"
description: "Mapa funkcí a modulů Happenee podle typu události: co je nezbytné pro váš cíl, co volitelné a co specializované."
collection: "Začínáme s Happenee"
subcollection: "priprava-setupu"
modules: ["leaderboard"]
slug: "must-have-optional-a-advanced-moduly-podle-typu-akce"
lang: "cs"
status: "published"
docId: 6
last_updated: "2026-09-21"
version: 3
tags: [funkce, moduly, rozhodovani, typy-akci, setup, event-sherpa]
source_images_consulted: true
related:
  - "Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka"
  - "Minimální doporučený setup pro malý, střední a větší event"
  - "Doporučené pořadí setupu eventu krok za krokem"
  - "Co nastavit jako první po vytvoření eventu"
  - "Doporučený setup pro interní firemní event"
  - "Doporučený setup pro externí klientský event"
  - "Doporučený setup pro konferenci"
  - "Doporučený setup pro expo / veletrh"
  - "Jak funguje Leaderboard"
  - "Použití Online modulu"
  - "Doporučený setup pro incentive / itinerář"
  - "Doporučený setup pro hybridní event"
  - "Plánování události a kde pomůže Happenee"
---

> [!info] Krátce
> Celý ekosystém včetně účastnické aplikace doporučujeme u každé události, bez ohledu na počet lidí. Rozsah obsahu a funkcí přizpůsobte cíli pořadatele a úkolům účastníků. Host si může zvolit e-mail, webovou nebo mobilní cestu; instalace ani použití aplikace nejsou povinné.

## Jak začít

1. Pojmenujte výsledek za každou stranu: co potřebujete vy jako pořadatel, co si má odnést účastník a u externí události co má mít partner nebo sponzor. Doplňte, podle čeho úspěch poznáte: potvrzená účast, hladké odbavení, rezervace workshopu, relevantní kontakty nebo zpětná vazba po události.
2. Popište cestu hosta od pozvánky po výsledek. Zohledněte i kupujícího, asistenta či partnera, pokud mají jinou roli.
3. Určete, co již funguje v jiném systému a co má zajistit Happenee.
4. Vyberte potřebné funkce, ověřte jejich dostupnost ve své nabídce a otestujte jeden celý průchod jako účastník.

## Detail

### Must-have znamená nezbytné pro váš výsledek

Neexistuje seznam modulů, které musí mít každá událost zapnuté. Vždy však potřebujete:

- Jasný další krok a přístup pro zamýšlené publikum.
- Správné informace: co, kdy, kde nebo jak se připojit a na koho se obrátit.
- Ověřený způsob potvrzení či předání pokynů, pokud ho průchod vyžaduje.
- Člověka odpovědného za obsah a změny.

Použijete-li registraci v Happenee, připravte formulář a související komunikaci. U placeného vstupu navíc ověřte objednávku, platbu a oprávnění hosta. Pokud registrace již běží jinde, nevytvářejte druhou jen kvůli aplikaci; nejprve dohodněte přenos účastníků a změn. Vlastní web zákazníka může dál sloužit jako veřejná prezentace místo nové Microsite.

**Optional** znamená užitečné rozšíření podle cíle. **Advanced** jsou specializované možnosti, u nichž předem ověříte rozsah, dostupnost, potřebnou pomoc a čas přípravy; neznamená to další povinný balík.

### Obsah a orientace

**Program** pomůže, pokud si člověk vybírá mezi bloky, mění místo nebo potřebuje sledovat čas. **Řečníci, Sponzoři a Vystavovatelé** mají smysl, když jsou relevantní pro rozhodování a zážitek hosta. **Lokalita, Kontakt a Vlastní obsah** mohou dát na jedno místo dopravu, mapu, FAQ či pokyny.

Nezobrazujte prázdnou funkci jen proto, že je k dispozici. Současně nevynechávejte užitečnou možnost pouze proto, že ji zákazník původně neznal. Začněte konkrétním účelem a připravte obsah potřebný pro první použití.

### Aplikace a propojení účastníků

Účastnickou aplikaci doporučujeme jako součást celého ekosystému u každé události, i pro třicet lidí. Obsah přizpůsobte cíli: může stačit vstupenka, místo, kontakt a materiály; jindy přidáte program, rezervace a networking. Host si volí e-mail/PDF/QR, webovou nebo mobilní aplikaci. Instalaci ani používání nevynucujte. Webová varianta nevyžaduje stažení mobilní aplikace. Fyzická událost může používat webovou aplikaci a rezervaci workshopů; kvůli tomu ji nemusíte měnit na hybridní.

Rozhodujte podle cíle, opakování a chování lidí. U pravidelného setkání přibližně padesáti členů může být **Networking** a chat hlavní hodnotou. I u jednoduché události ukažte hodnotu aplikace jako dalšího způsobu přístupu k informacím. Pokud pořadatel po vysvětlení zvolí užší rozsah, respektujte ho a zachovejte funkční alternativu; nevyřazujte aplikaci předem.

Aplikace nemusí skončit odbavením. Po události se lidé mohou podle dostupnosti obsahu, svého přístupu a licence vrátit k materiálům a kontaktům; u opakovaných událostí navazují další setkání. Nezaměňujte to za automatický přístup ke všem budoucím událostem nebo neomezené uchování dat.

Pro networking určete, kdo se má potkat s kým, kdy na to bude prostor a co má účastník udělat. QR na jmenovce není univerzální podmínka chatu nebo všech způsobů uložení kontaktu. Konkrétní možnosti schůzek, viditelnosti a exportu ověřte před příslibem partnerovi.

### Zapojení a zpětná vazba

**Hlasování** slouží k položené otázce směrem k publiku; **Otázky** dávají prostor dotazům účastníků; **Dotazník** sbírá zpětnou vazbu či další odpovědi. Volte podle požadovaného výsledku, ne jako povinnou sadu.

Ke každé interakci určete obsah, okamžik použití a správce. Moderátor musí vědět, co na pódiu říci a co se stane s odpověďmi. Před použitím vyzkoušejte konkrétní režim, přístup hosta i zobrazení; nepředpokládejte automaticky anonymitu, moderaci nebo odpovědi bez přihlášení.

### Rezervace, logistika a specializované možnosti

Workshopy a časové bloky vyžadují správnou kapacitu, registrační okna a pravidla změn. Při rezervaci vozu, odborníka či stanoviště počítejte i s přípravou a předáním zdroje. Čekací seznam není k dispozici.

Ubytování, doprava a itinerář mají různé jednotky a příjemce. Odpověď ve formuláři sama nepotvrzuje pokoj v hotelu; dodavatelské předání se ověřuje samostatně.

Seating, vlastní mobilní aplikace, SSO, integrace a další specializovaná řešení posuzujte s týmem Happenee podle konkrétního rozsahu, ceny, dostupnosti a času přípravy. Běžné přizpůsobení vzhledu nezaměňujte za samostatnou aplikaci v obchodech.

### Jak vybrat podle typu události

- **Interní setkání:** orientace, komunikace a cílené zapojení. Networking může spojit lidi napříč týmy; není omezený na externí publikum.
- **Klientská událost:** srozumitelná pozvánka, potvrzení účasti a užitečný navazující kontakt. Ověřte role VIP, asistentů a partnerů.
- **Konference:** provázaný program, oprávnění, workshopy a komunikace. Zvažte networking a partnery, ne automaticky všechny funkce.
- **Expo:** snadná orientace, důvod navštívit vystavovatele a použitelný následný kontakt. Počet skenů není sám obchodním výsledkem.
- **Incentive:** správný itinerář pro konkrétního člověka, aktuální pokyny a návaznost na dopravu a ubytování.
- **Online nebo hybridní událost:** ověřený přístup k obsahu, spolupráce s produkcí a smysluplné zapojení vzdáleného publika.

Podrobné návody jsou v souvisejících článcích. Když přidáváte rozšíření později, ověřte čas na obsah a test i případnou licenci; nejde vždy o okamžité zapnutí.

## Na co si dát pozor

### Typ ani velikost neurčují povinný balík

Stejných padesát lidí může potřebovat pouze potvrzení účasti, nebo intenzivní networking. Rozhoduje jejich úkol a kontext.

### Dostupná funkce ještě není použitá funkce

Zapnuté Hlasování bez otázky a moderátora nepřinese zapojení. Připravte konkrétní první použití.

### Nový systém není vždy nejlepší změna

U fungující externí registrace zvažte náklady přenosu a riziko změny. Přidanou hodnotu lze navrhnout i bez jejího nahrazení.

### Nejprve ověřte skutečnou cestu

Přihlášení, cílový odkaz, oprávnění, rezervaci i komunikaci zkoušejte správnou účastnickou rolí. Náhled administrátora nestačí.

## Související články

- [Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka](05_microsite-vs-ucastnicka-aplikace-jak-premyslet-nad-flow-ucastnika.md)
- [Minimální doporučený setup pro malý, střední a větší event](07_minimalni-doporuceny-setup-pro-maly-stredni-a-vetsi-event.md)
- [Doporučené pořadí setupu eventu krok za krokem](08_doporucene-poradi-setupu-eventu-krok-za-krokem.md)
- [Co nastavit jako první po vytvoření eventu](03_co-nastavit-jako-prvni-po-vytvoreni-eventu.md)
- [Doporučený setup pro interní firemní event](../07_event-sherpa/01_doporuceny-setup-pro-interni-firemni-event.md)
- [Doporučený setup pro externí klientský event](../07_event-sherpa/02_doporuceny-setup-pro-externi-klientsky-event.md)
- [Doporučený setup pro konferenci](../07_event-sherpa/03_doporuceny-setup-pro-konferenci.md)
- [Doporučený setup pro expo / veletrh](../07_event-sherpa/04_doporuceny-setup-pro-expo-veletrh.md)
- [Jak funguje Leaderboard](../03_obsah-a-zkusenost-ucastnika/17_jak-funguje-leaderboard.md)
- [Použití Online modulu](../03_obsah-a-zkusenost-ucastnika/18_pouziti-online-modulu.md)
- [Doporučený setup pro incentive / itinerář](../07_event-sherpa/05_doporuceny-setup-pro-incentive-itinerar.md)
- [Doporučený setup pro hybridní event](../07_event-sherpa/06_doporuceny-setup-pro-hybridni-event.md)
- [Plánování události a kde pomůže Happenee](../07_event-sherpa/10_planovani-udalosti-a-kde-pomuze-happenee.md)

<!-- source: kb.cs.01.07 -->

---
title: "Minimální doporučený setup pro malý, střední a větší event"
description: "Doporučený minimální setup pro malou, středně velkou a větší událost."
collection: "Začínáme s Happenee"
subcollection: "priprava-setupu"
modules: ["prurezovy"]
slug: "minimalni-doporuceny-setup-pro-maly-stredni-a-vetsi-event"
lang: "cs"
status: "published"
docId: 7
last_updated: "2026-09-21"
version: 5
tags: [setup, velikost-akce, moduly, zacatky, doporuceni]
source_images_consulted: true
related:
  - "Must-have, optional a advanced funkce a moduly podle typu události"
  - "Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka"
  - "Doporučené pořadí setupu eventu krok za krokem"
  - "Doporučený setup pro interní firemní event"
  - "Doporučený setup pro externí klientský event"
  - "Doporučený setup pro konferenci"
  - "Doporučený setup pro expo / veletrh"
  - "Doporučený setup pro incentive / itinerář"
  - "Plánování události a kde pomůže Happenee"
---

> [!info] Krátce
> Celý ekosystém včetně účastnické aplikace doporučujeme pro malé i velké události. Velikost pomáhá odhadnout provozní nároky; obsah a funkce ale vybírejte podle cíle a cesty účastníka. Host může zůstat u e-mailu a PDF vstupenky nebo využít webovou či mobilní aplikaci — nabízíte mu možnosti, nevynucujete instalaci.

## Jak začít

1. Řekněte, co má účastník zvládnout, jaký výsledek potřebujete vy jako pořadatel a u externí události co má z ní mít partner nebo sponzor. Doplňte, podle čeho úspěch poznáte.
2. Zvažte počet lidí, souběžné příchody, délku, opakování a složitost programu.
3. Vyberte nejbližší variantu níže a přidejte pouze funkce s konkrétním přínosem.
4. Určete správce obsahu a ověřte celý průchod před spuštěním.

## Detail

### Malá jednoduchá událost

U jednorázového setkání s jedním místem a pevným průběhem může stačit pozvánka, potvrzení účasti a přehledné organizační informace. Registraci můžete řídit v Happenee; pokud už funguje jinde, nejprve dohodněte návaznost.

Základ obvykle tvoří:

- Kdy a kam přijít, kontakt a případné pokyny.
- Jasný způsob potvrzení či změny účasti.
- Ověřená komunikace před událostí.
- Evidence nebo odbavení, pokud je potřebujete.

I zde nabídněte aplikaci: host v ní může mít vstupenku, místo, kontakt a materiály pro pozdější návrat. Nepotřebuje desítky funkcí. Kdo dává přednost e-mailu nebo PDF, může používat ověřenou alternativní cestu. Ani Microsite nemusí nahrazovat váš fungující web.

### Malá opakovaná nebo interaktivní událost

Přibližně padesát členů profesního klubu může potřebovat najít kolegy, napsat si a navázat kontakt mezi setkáními. Zde může být aplikace hodnotnější než u mnohem větší události s jednoduchým průběhem.

Zvažte profily, Networking a chat, přehled programu nebo potřebné rezervace. Účastník může použít webovou aplikaci bez stažení mobilní varianty. Určete důvod k použití a správce, který lidem vysvětlí první krok. U série znovu potvrzujte aktuální hosty, obsah a přístupy; starý seznam není automaticky nová potvrzená účast.

Po události může zůstat důvod vracet se k materiálům, kontaktům a dalším setkáním. Ověřte dostupnost obsahu a přístup podle konkrétní události a licence; minulá účast není automatické oprávnění ke všem dalším.

Příklad: před pravidelnou snídaní si člen prohlédne profily a napíše člověku, kterého chce potkat. Úspěch posoudíte podle užitečného propojení, ne jen počtu otevření aplikace.

### Středně velká událost s volbou programu

Při workshopech, paralelních sessions a změnách během dne bývá důležitější orientace a návaznost jednotlivých kroků než samotný počet lidí.

Zvažte:

- Program s časy, místy a příslušnými řečníky.
- Registraci či vstupenky podle skutečného vstupního procesu.
- Webovou nebo mobilní účastnickou aplikaci pro výběr a průběžné informace.
- Ověřenou kapacitu a registrační okna workshopů.
- Komunikaci změn a kontakt na pomoc.

Na fyzické události lze používat webovou aplikaci a registraci na workshop; nejde tím automaticky o hybridní událost. Program viditelný na Microsite neznamená stejnou registrační cestu jako v účastnické aplikaci.

Příklad: host vybírá ze dvou souběžných workshopů. Otestujte jeho konkrétní oprávnění, rezervaci, změnu a případný překryv. Pouhá správná položka v administraci neprokazuje funkční průchod.

### Větší nebo provozně složitá událost

U většího publika obvykle roste význam segmentace, odbavení, výjimek a koordinace. Aplikaci doporučujeme stejně jako u malé události; bohatší obsah dává smysl při rozsáhlém programu, networkingu, více místech nebo průběžných změnách. Ani zde nevynucujte jednu cestu pro všechny hosty.

Připravte zejména:

- Jasné varianty vstupu a komunikaci pro konkrétní publikum.
- Provozní plán příchodů, odbavení a řešení výjimek.
- Program a navigaci podle skutečné potřeby.
- Správce změn a zkoušku kritických cest.
- Dohodnuté výsledky a způsob jejich ověření.

Pokud je cílem pouze registrace a odbavení, nabídněte aplikaci jako další způsob, jak mít vstup a informace na jednom místě. Užší rozsah může být vědomou volbou pořadatele po vysvětlení hodnoty, ne automatickým výchozím doporučením. Pokud chcete i hodnotu pro partnery a propojení lidí, navrhněte konkrétní cestu k ní a čas v programu. Počet skenů nebo rezervací sám nepotvrzuje obchodní přínos.

### Jak rozhodnout o dalším rozšíření

Položte si otázky:

- Co přesně díky němu člověk zvládne lépe?
- Máme obsah, správce a čas na vyzkoušení?
- Je možnost dostupná v našem rozsahu, nebo potřebuje dohodu s Happenee?
- Jak zjistíme, že přinesla hodnotu?

Rozšíření může být užitečné i později, pokud zbývá čas na přípravu. Nejde o počet souhlasných odpovědí ani automatický přechod do vyšší velikostní kategorie. Podrobné varianty podle typu najdete v souvisejících návodech.

## Na co si dát pozor

### Nezaměňujte webovou aplikaci za nutnost instalace

Účastník může využít webovou cestu. Nejprve ukažte užitek, potom doporučte vhodný způsob přístupu.

### Nekopírujte všechny funkce z minulé konference

Nová událost může mít jiný cíl, publikum a kapacitu týmu. Převezměte jen to, co dává smysl, a ověřte data a odkazy.

### Odbavení a registrace vyžadují vlastní přípravu

U placeného vstupu vyzkoušejte objednávku a platbu, správného držitele i přístup. Pro den události potvrďte obsluhu a postup při chybějícím vstupu.

### Nepřidávejte složitost bez výsledku

Prázdný obsah ani interakce bez správce nepomohou. Když účel není jasný, zvolte jednodušší variantu a zaznamenejte, co by rozhodnutí změnilo.

## Související články

- [Must-have, optional a advanced funkce a moduly podle typu události](06_must-have-optional-a-advanced-moduly-podle-typu-akce.md)
- [Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka](05_microsite-vs-ucastnicka-aplikace-jak-premyslet-nad-flow-ucastnika.md)
- [Doporučené pořadí setupu eventu krok za krokem](08_doporucene-poradi-setupu-eventu-krok-za-krokem.md)
- [Doporučený setup pro interní firemní event](../07_event-sherpa/01_doporuceny-setup-pro-interni-firemni-event.md)
- [Doporučený setup pro externí klientský event](../07_event-sherpa/02_doporuceny-setup-pro-externi-klientsky-event.md)
- [Doporučený setup pro konferenci](../07_event-sherpa/03_doporuceny-setup-pro-konferenci.md)
- [Doporučený setup pro expo / veletrh](../07_event-sherpa/04_doporuceny-setup-pro-expo-veletrh.md)
- [Doporučený setup pro incentive / itinerář](../07_event-sherpa/05_doporuceny-setup-pro-incentive-itinerar.md)
- [Plánování události a kde pomůže Happenee](../07_event-sherpa/10_planovani-udalosti-a-kde-pomuze-happenee.md)

<!-- source: kb.cs.01.08 -->

---
title: "Doporučené pořadí setupu eventu krok za krokem"
description: "Pořadí kroků setupu eventu, které respektuje závislosti mezi nimi."
collection: "Začínáme s Happenee"
subcollection: "priprava-setupu"
modules: ["nastaveni_udalosti"]
slug: "doporucene-poradi-setupu-eventu-krok-za-krokem"
lang: "cs"
status: "published"
docId: 8
last_updated: "2026-09-21"
version: 5
tags: [setup, poradi, zacatky, workflow, kroky]
source_images_consulted: true
related:
  - "Co nastavit jako první po vytvoření eventu"
  - "Výběr správného typu registrace"
  - "Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka"
  - "Must-have, optional a advanced funkce a moduly podle typu události"
  - "Minimální doporučený setup pro malý, střední a větší event"
  - "Vytvoření nové události"
  - "Kopírování události"
  - "Nastavení registračního formuláře"
  - "Doporučený setup pro interní firemní event"
  - "Doporučený setup pro externí klientský event"
  - "Doporučený setup pro konferenci"
  - "Doporučený setup pro expo / veletrh"
  - "Doporučený setup pro incentive / itinerář"
  - "Jak opravovat věci ex post"
  - "Dokumentace Happenee ve vašem AI asistentovi"
  - "Plánování události a kde pomůže Happenee"
---

> [!info] Krátce
> Setup eventu v Happenee má logiku, která respektuje závislosti mezi jednotlivými kroky. Skupiny musí existovat předtím, než na ně budete cílit viditelnost v registračním formuláři. Kontakty musí být ve workspace, než je přiřadíte k eventu. Program musí být vytvořený, než k němu přiřadíte řečníky. Tento článek vám dá pořadí, které se osvědčilo — nejprve spuštění registrace, potom provozní fáze, potom průběh události a nakonec reporting.

## Jak začít

- Než začnete, ujistěte se, že máte připraveno: základní kontakty a skupiny ve workspace, GDPR nastavení, patičku e-mailů.
- Pracujte po etapách — nesnažte se mít všechno hotové naráz. Některé věci se nastavují až v druhé fázi.
- U každé etapy si odbavte „blocking“ rozhodnutí dříve, než se pustíte do detailů.

> **Poznámka:** Pokud pořádáte opakující se události, ušetříte si čas **kopií existující události** — Happenee zduplikuje nastavení (grafiku, registrační formulář, microsite, e-maily, obsahové a engagement funkce) do nové události, bez účastníků a transakčních dat. Co přesně se přenese a na co si dát pozor, najdete v článku [Kopírování události](../02_nastaveni-eventu-a-registrace/13_kopirovani-udalosti.md). **Šablony eventu** jako znovupoužitelné vzory jsou zatím v přípravě. Nezávisle na tom udržujte jasnou strukturu skupin, vlastních polí kontaktů a GDPR šablony v nastavení workspace — tyto části se napříč událostmi nepřenastavují.

## Detail

### Naplánujte nejbližší skutečný termín

Oddělte datum události od termínu, kdy potřebujete rozeslat pozvánky a otevřít registraci. Před tím musí být připravené potřebné podklady, případné nastavení domény, zaškolení a test. Rozsah a termíny potvrďte podle sjednané spolupráce; platnost nabídky a období licence nejsou totéž.

Pro spuštění registrace dokončete obsah, který host potřebuje k rozhodnutí a registraci. Další program nebo účastnickou aplikaci můžete připravovat později, pokud na nich registrace nezávisí. Určete, kdo zbývající obsah dodá a kdy jej účastník dostane.

### Etapa 0 — Před založením eventu (workspace)

Tato etapa platí pro celý workspace. U další události ověřte změny firmy, odesílatele, přístupů a podkladů. Pokud vše odpovídá aktuálnímu zadání, pokračujte etapou 1.

1. **Nastavení workspace** — informace o společnosti, výchozí patička e-mailů a microsite (typicky řeší zákaznická podpora na vaši žádost).
2. **Vlastní pole kontaktů** — pokud víte, že budete chtít u kontaktů evidovat specifické informace napříč všemi eventy (firma, pozice, interní ID), nastavte je teď.
3. **Ochrana osobních údajů (GDPR)** — šablona zpracování, souhlasy nad rámec (marketing, fotky). Bez toho nesmíte legálně spouštět registrace.
4. **Import kontaktní databáze** — pokud máte stávající databázi účastníků, naimportujte ji.
5. **Založení základních skupin** — VIP, speakeři, klientské segmenty, interní tým.

### Etapa 1 — Založení eventu a klíčová rozhodnutí

1. **Vytvoření nového eventu** — název, datum, čas, časové pásmo, typ (Fyzická / Virtuální / Hybridní).
2. **Primární jazyk** — rozhodněte podle očekávaných národností účastníků. Pokud přijedou cizinci, primární jazyk = angličtina. **Toto rozhodnutí je po vytvoření eventu nevratné.**
3. **Sekundární jazyky** — přidejte další jazyky, ve kterých budete obsah publikovat.
4. **Rozhodnutí o typu registrace** — veřejná, uzavřená, nominovaná, se schvalováním? S doplněním informací nebo automatická? Placená nebo zdarma? (Viz [Výběr správného typu registrace](04_vyber-spravneho-typu-registrace.md).)

### Etapa 2 — Skupiny, viditelnost, základní struktura

1. **Struktura skupin pro tento event** — vytvořte skupiny, které budete používat v registračním formuláři, na cílení viditelnosti a komunikace.
2. **Přiřazení kontaktů k eventu** — z workspace přiřaďte, kdo patří k této události. U uzavřené registrace tím určujete, kdo dostane osobní odkaz.

### Etapa 3 — Obsah eventu

V této fázi plníte informační základ eventu. Pořadí v rámci etapy není striktní, ale několik závislostí platí:

1. **Lokalita** — kde se událost koná.
2. **Kontakt** — kdo je kontaktní osoba za organizaci.
3. **Program** — nejdřív typy sessions (pokud relevantní), potom jednotlivé sessions.
4. **Řečníci** — až po vytvoření programu, aby je šlo přiřazovat k sessions.
5. **Sponzoři, vystavovatelé** — pokud jsou součástí události.
6. **Vlastní obsah, FAQ, informační bloky** — specifické informace pro účastníky.

U každé obsahové funkce rozhodněte:

- Kde se zobrazí (microsite, aplikace, obojí)?
- Kdo ho uvidí (všichni, nebo vybrané skupiny)?

### Etapa 4 — Registrační formulář

1. **Kontaktní údaje** — určete, která pole jsou povinná, nepovinná, skrytá.
2. **Doplňující otázky** — přidejte otázky specifické pro tento event (strava, parkování, workshop, ubytování).
3. **Podmíněné otázky** — pokud některé otázky závisí na jiných odpovědích, propojte je.
4. **Viditelnost podle skupin** — pokud má otázka být viditelná jen některým účastníkům, nastavte.
5. **Náhled formuláře** — vyzkoušejte si celý flow z pohledu účastníka.

### Etapa 5 — Komunikace

1. **Zvací e-mail** — obsah, design, vložené odkazy. Krátký a úderný, cílem je dostat účastníka na microsite.
2. **Potvrzovací e-mail** — obsahuje QR vstupenku, odkazy na aplikaci, další informace.
3. **E-mailové kampaně** — pokud plánujete další komunikaci před událostí (připomínky, detaily, praktické info).
4. **Test odeslání** — odešlete si zvací i potvrzovací e-mail na testovací adresu, ověřte odkazy a zobrazení.

### Etapa 6 — Microsite a aplikace

1. **Microsite** — ověřte vizuální vzhled, jazyky, obsah jednotlivých funkcí a modulů.
2. **Účastnická aplikace** — pokud ji využíváte, projděte, jak se obsah zobrazuje v mobilní a webové verzi.
3. **Viditelnost funkcí a modulů** — znovu projděte, co je kde zapnuté.

### Etapa 7 — Spuštění registrace

1. **Finální kontrola** — náhledy v microsite i aplikaci, všechny jazyky, test registrace.
2. **Spuštění** — sdílení odkazu (veřejný nebo osobní odkazy podle typu registrace), odeslání zvacích e-mailů.

### Etapa 8 — Průběh registračního období

V této fázi je event veřejný. Sledujte:

- Statistiky registrací
- Chybové e-maily (nepřišel zvací e-mail, problém s odkazem)
- Změny kapacit, schvalování (pokud je zapnuté)
- E-mailové kampaně — připomínky, detaily programu, praktické informace

### Etapa 9 — Příprava na den události

1. **Kontrola check-in nastavení** — kdo bude odbavovat, které zóny, QR skenery.
2. **Účty pro personál** — pokud delegujete odbavení na třetí stranu.
3. **Tisk jmenovek** — pokud tisknete, projděte layout a připravte export.
4. **Seating** — pokud používáte, dokončete přiřazení sedadel.
5. **Oznámení pro první den** — připravené push notifikace.

### Etapa 10 — Den události

1. Odbavení účastníků (Prezence).
2. Operativní oznámení (změny v programu, praktické info).
3. Reakce na otázky účastníků přes aplikaci.

### Etapa 11 — Po události

1. **Statistiky** — celková účast, zaplněnost workshopů, vývoj registrací.
2. **Dotazník / zpětná vazba** — pokud je zapnutá.
3. **Follow-up komunikace** — poděkování, materiály, další kroky.
4. **Export dat** — pokud potřebujete data pro interní reporting.

## Na co si dát pozor

### Pokus dokončit všechno najednou — obsah, registraci, komunikaci, aplikaci. Ztráta přehledu, kde je co rozpracované

Pracujte po etapách. Nejprve rozhodněte jazyk, typ registrace a skupiny. Před spuštěním dokončete a otestujte registrační cestu a obsah, který pro ni účastník potřebuje. Pozdější obsah nemusí blokovat registraci, pokud na něm nezávisí formulář ani příslib účastníkovi.

### Řečníci se přiřazují k sessions, které ještě neexistují

Pořadí v etapě 3: nejdřív typy sessions, pak sessions, pak řečníci. Když to zvládnete v tomto pořadí, nebudete se vracet.

### Skupiny se zakládají až v momentě, kdy se nastavuje podmíněná otázka nebo cílení komunikace. Výsledkem je chaos a ruční přiřazování

Skupiny naplánujte v etapě 2, tedy **před registračním formulářem**. Aby je formulář uměl automaticky přiřazovat, musí existovat.

### Test registrace se dělá až po odeslání zvacích e-mailů. Chyby se objeví, když už je pozdě

Vždy proveďte test — projděte si registraci jako účastník, nechte si přijít všechny e-maily, otevřete QR vstupenku, podívejte se do aplikace. Lepší je najít chybu hodinu před spuštěním než hodinu po.

### Všechen obsah se vyplňuje jen v jednom jazyce, druhý se zapomene

Po každé úpravě přepněte vlajkou jazyk a ověřte. Zejména před spuštěním projděte všechny jazyky celkově.

### Změna zadání se nepřenese do další práce

Při změně termínu, firmy, odkazů nebo domluveného rozsahu projděte, co už bylo odesláno a co se teprve připravuje. Určete aktuální verzi podkladů a ověřte změněnou cestu z pohledu účastníka. Starší nabídka ani zkopírovaná událost nenahrazují aktuální zadání.

## Související články

- [Co nastavit jako první po vytvoření eventu](03_co-nastavit-jako-prvni-po-vytvoreni-eventu.md)
- [Výběr správného typu registrace](04_vyber-spravneho-typu-registrace.md)
- [Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka](05_microsite-vs-ucastnicka-aplikace-jak-premyslet-nad-flow-ucastnika.md)
- [Must-have, optional a advanced funkce a moduly podle typu události](06_must-have-optional-a-advanced-moduly-podle-typu-akce.md)
- [Minimální doporučený setup pro malý, střední a větší event](07_minimalni-doporuceny-setup-pro-maly-stredni-a-vetsi-event.md)
- [Vytvoření nové události](../02_nastaveni-eventu-a-registrace/01_vytvoreni-nove-udalosti.md)
- [Kopírování události](../02_nastaveni-eventu-a-registrace/13_kopirovani-udalosti.md)
- [Nastavení registračního formuláře](../02_nastaveni-eventu-a-registrace/05_nastaveni-registracniho-formulare.md)
- [Doporučený setup pro interní firemní event](../07_event-sherpa/01_doporuceny-setup-pro-interni-firemni-event.md)
- [Doporučený setup pro externí klientský event](../07_event-sherpa/02_doporuceny-setup-pro-externi-klientsky-event.md)
- [Doporučený setup pro konferenci](../07_event-sherpa/03_doporuceny-setup-pro-konferenci.md)
- [Doporučený setup pro expo / veletrh](../07_event-sherpa/04_doporuceny-setup-pro-expo-veletrh.md)
- [Doporučený setup pro incentive / itinerář](../07_event-sherpa/05_doporuceny-setup-pro-incentive-itinerar.md)
- [Jak opravovat věci ex post](../08_reseni-problemu/13_jak-opravovat-veci-ex-post.md)
- [Dokumentace Happenee ve vašem AI asistentovi](../07_event-sherpa/08_dokumentace-happenee-ve-vasem-ai-asistentovi.md)
- [Plánování události a kde pomůže Happenee](../07_event-sherpa/10_planovani-udalosti-a-kde-pomuze-happenee.md)

<!-- source: kb.cs.02.01 -->

---
title: "Vytvoření nové události"
description: "Co se vyplňuje při zakládání nové události a která rozhodnutí jsou trvalá."
collection: "Nastavení eventu a registrace"
subcollection: "event-a-kontakty"
modules: ["nastaveni_udalosti"]
slug: "vytvoreni-nove-udalosti"
lang: "cs"
status: "published"
docId: 9
last_updated: "2026-09-09"
version: 4
tags: [zacatky, setup, vytvoreni-eventu, typ-udalosti, primarni-jazyk]
source_images_consulted: true
related:
  - "Co je workspace a co je event"
  - "Nastavení primárního jazyka události"
  - "Co nastavit jako první po vytvoření eventu"
  - "Orientace v administraci Happenee"
  - "Správa kontaktů a skupin ve workspace"
  - "Doporučené pořadí setupu eventu krok za krokem"
  - "Použití Online modulu"
  - "Kopírování události"
---

> [!info] Krátce
> Vytvoření nové události je vstupní bod do setupu eventu v Happenee. Není to jen vyplnění formuláře — při zakládání potvrdíte několik rozhodnutí, která později nelze změnit bez založení jiné události. Typicky primární jazyk. Tento článek popisuje, co se vyplňuje, co z toho je trvalé a co se stane hned po vytvoření.

## Jak začít

- Ujasněte si základní parametry ještě předtím, než kliknete na **+ Nová událost**: název, datum a čas, typ (fyzická / virtuální / hybridní) a jaké jazyky budete nabízet.
- Rozhodněte o **primárním jazyce** — toto rozhodnutí nelze po vytvoření změnit.
- Vědět, zda událost bude placená, v tuto chvíli nepotřebujete. Placené vstupenky se zapínají až v nastavení události.
- Ikonu, popis a grafiku můžete doplnit později. Zdržovat se jimi při vytváření nemá smysl.

## Detail

### Kde se událost vytváří

Ve workspace na hlavní obrazovce (přepínač **Nadcházející / Uplynulé / Vše**) klikněte na tlačítko **+ Nová událost**. Otevře se panel úprav, do kterého postupně vyplňujete základní informace. Po potvrzení tlačítkem **✓ Vytvořit událost** se událost objeví v seznamu a otevře se její **Přehled**.

### Co se vyplňuje při vytváření

**Název události.** Zobrazuje se v seznamu událostí ve workspace, na microsite, v účastnické aplikaci, ve zvacím a potvrzovacím e-mailu.

**Ikona události.** Čtvercový obrázek, který reprezentuje událost v seznamu událostí v účastnické aplikaci, v nákupním prostředí vstupenek, ve výchozím zobrazení hlavičky microsite a v e-mailech. Není povinný hned — doplnit lze později v **Nastavení události → Nastavení grafiky**.

**Časové pásmo.** Nastaví se automaticky podle prohlížeče, ale ověřte ho — typická chyba je plánovat události v Praze z prohlížeče nastaveného na jiné časové pásmo.

**Začátek** a **konec** události. Pokud je událost vícedenní, konec se vztahuje k poslednímu dni.

**Popis události.** Volitelný. Není potřeba vyplňovat při zakládání — dá se kdykoli doplnit v **Nastavení události**.

**Typ události.** Tři možnosti — **Fyzická**, **Virtuální**, **Hybridní**. Volba ovlivňuje, do jaké účastnické aplikace získá účastník přístup:

- **Fyzická** — přístup do mobilní účastnické aplikace (iOS, Android) i do webové aplikace v prohlížeči.
- **Virtuální** — přístup do webové účastnické aplikace.
- **Hybridní** — přístup do obou.

Microsite je dostupná u všech tří typů. Fyzická událost proto nepotřebuje přepnutí na hybridní jen proto, že část účastníků otevře aplikaci v prohlížeči nebo se přes ni přihlásí na workshop. Registrace na sessions funguje v mobilní i webové aplikaci stejně.

**Primární jazyk.** Záložní jazyk události. Pokud má účastník nastavený v zařízení jazyk, který událost nemá explicitně přidaný, zobrazí se mu obsah v primárním jazyce. Více v článku *Nastavení primárního jazyka události*.

> Primární jazyk se nastavuje při zakládání události a později ho **nelze upravit**. Jde o jedno z mála skutečně nevratných rozhodnutí v Happenee.

### Co se stane hned po vytvoření

Událost se přidá do seznamu ve workspace a automaticky vás přepne na její **Přehled**. Na přehledu se objeví:

- Základní informace (datum, stav registrace, kolik dnů do události).
- **Nástroje** — rychlé odkazy na Správu kontaktů a skupin, Registraci, Prezenci, Nominace a podle zapnutých funkcí buď na Objednávky, nebo na Schvalování účastníků.
- Odkazy na **Statistiky**, **Statistiky s účastníky** a **Statistiky vstupenek** (poslední dvě u placených událostí).
- V levém menu se rozbalí struktura události — Nastavení události, Statistiky a reporting, Obsah, Engagement, Účastnická aplikace, Placené vstupenky (pokud zapnuté), Registrační formulář, Potvrzovací e-mail, Microsite, Zvací e-mail, E-mailové kampaně a Odbavení na místě.
- **Registraci, Prezenci a Nominace** v tomto seznamu nehledejte — jsou v rozbalovací nabídce **Nástroje** ve spodní části levého menu (a jako dlaždice na Přehledu). Tamtéž najdete **Objednávky**, pokud má událost placené vstupenky, nebo **Schvalování účastníků**, pokud má schvalovanou registraci.

### Přepínač jazyků a náhled

V pravém horním rohu administrace události jsou **dvě vlajky jazyků**. Přepínají jazyk obsahu, který zrovna upravujete — obsah vyplňujete v každém jazyce zvlášť. Pokud přidáváte například program, popis sessions nebo texty v obsahových funkcích, ujistěte se, že jste v tom jazyce, ve kterém chcete psát.

Vedle vlajek je tlačítko **Náhled**, které ukazuje, jak událost vidí účastník:

- Náhled microsite.
- Náhled nákupu vstupenek (u placených událostí).
- Náhled účastnické aplikace (webové i mobilní).
- Náhled servisní aplikace (pro odbavení na místě).

### Co ještě není aktivní

Hned po vytvoření události je **uzavřena registrace** — účastník se na ni nemůže přihlásit, dokud nedokončíte registrační nastavení. To je záměrné. Než budete registraci otevírat, projděte **Nastavení události** (přístup a registrace, viditelnost, omezení, případně placené vstupenky) a **Registrační formulář**. Doporučené pořadí setupu najdete v článku *Doporučené pořadí setupu eventu krok za krokem*.

## Na co si dát pozor

### Vybrání primárního jazyka bez rozmyslu, s tím, že „se to později upraví“

Primární jazyk je po vytvoření události pevný. Pokud má mít událost zahraniční hosty, nastavte ho hned na angličtinu. Detail v článku *Nastavení primárního jazyka události*.

### Přepnutí typu události po vytvoření (například z fyzické na hybridní), přestože už mají někteří účastníci staženou aplikaci nebo registraci v běhu

Typ události určuje, kterou aplikaci účastníci uvidí. Změnu lze provést, ale způsobí nekonzistenci, pokud už účastníci v aplikaci jsou. Rozhodněte o typu hned a neměňte. Kvůli webové aplikaci přepínat nemusíte, fyzická událost ji má také.

### Neověření časového pásma. Organizátor zakládá události z ciziny nebo z prohlížeče s jiným časovým pásmem a událost má špatný čas začátku

Po vyplnění data a času vždy zkontrolujte pole **Časové pásmo**. Happenee používá časové pásmo události pro e-maily, microsite i ICS soubory v kalendáři.

### Snaha vyplnit při vytváření všechny detaily — popis, ikonu, grafiku, obsah

Při vytváření potvrzujete parametry, které určují rámec události. Obsah a grafika se vyplňují v dalších krocích (**Obsah**, **Nastavení grafiky**). Neodkládejte vytvoření kvůli tomu, že nemáte finální ikonu.

### Očekávání, že registrace poběží hned po vytvoření události

Registrace je po vytvoření uzavřená. Otevřete ji až po dokončení registračního nastavení a kontrole registračního formuláře. Teprve pak má smysl sdílet odkaz na microsite.

## Související články

- [Co je workspace a co je event](../01_zaciname/01_co-je-workspace-a-co-je-event.md)
- [Nastavení primárního jazyka události](02_nastaveni-primarniho-jazyka-udalosti.md)
- [Co nastavit jako první po vytvoření eventu](../01_zaciname/03_co-nastavit-jako-prvni-po-vytvoreni-eventu.md)
- [Orientace v administraci Happenee](../01_zaciname/02_orientace-v-administraci-happenee.md)
- [Správa kontaktů a skupin ve workspace](03_sprava-kontaktu-a-skupin-ve-workspace.md)
- [Doporučené pořadí setupu eventu krok za krokem](../01_zaciname/08_doporucene-poradi-setupu-eventu-krok-za-krokem.md)
- [Použití Online modulu](../03_obsah-a-zkusenost-ucastnika/18_pouziti-online-modulu.md)
- [Kopírování události](13_kopirovani-udalosti.md)

<!-- source: kb.cs.02.02 -->

---
title: "Nastavení primárního jazyka události"
description: "Primární jazyk je záložní jazyk pro účastníky mimo přidané jazyky a po vytvoření události se nedá změnit."
collection: "Nastavení eventu a registrace"
subcollection: "event-a-kontakty"
modules: ["nastaveni_udalosti"]
slug: "nastaveni-primarniho-jazyka-udalosti"
lang: "cs"
status: "published"
docId: 10
last_updated: "2026-04-27"
version: 1
tags: [primarni-jazyk, jazyky, nastaveni, mezinarodni-akce, fallback]
source_images_consulted: false
related:
  - "Vytvoření nové události"
  - "Co nastavit jako první po vytvoření eventu"
  - "Správa kontaktů a skupin ve workspace"
  - "Co dělat, když kampaň nejde odeslat nebo přišla v jiném jazyce"
---

> [!info] Krátce
> Primární jazyk události je **záložní jazyk**, který se zobrazí účastníkovi, jehož jazyk zařízení nepatří mezi jazyky, které jste k události explicitně přidali. Volba primárního jazyka je nevratná — po vytvoření události ji nelze změnit bez založení jiné události. Pro událost se zahraničními účastníky je doporučený primární jazyk **angličtina**.

## Jak začít

- Před založením události si vyjasněte, zda budete očekávat zahraniční účastníky.
- Pokud ano, primární jazyk nastavte na **angličtinu**, i kdyby byl hlavní obsahový jazyk čeština.
- Přidejte sekundární jazyky (čeština, slovenština, další) podle toho, v jakých jazycích chcete mít obsah.
- Toto rozhodnutí udělejte při vytváření události — později ho nezměníte.

## Detail

### Jak funguje volba jazyka pro účastníka

Účastník přichází na microsite nebo do účastnické aplikace s nějakým jazykovým nastavením zařízení. Happenee zkontroluje, zda má událost obsah v tomto jazyce:

- **Ano** — zobrazí se obsah v daném jazyce.
- **Ne** — zobrazí se obsah v **primárním jazyce** události.

Primární jazyk tedy nerozhoduje, v jakém jazyce obsah vyplňujete — obsah vyplňujete v každém přidaném jazyce zvlášť. Primární jazyk rozhoduje, co vidí účastník, jehož jazyk jste nepřidali.

### Praktický příklad

Máte konferenci v Praze se zahraničními hosty. Obsah chcete vytvářet v **češtině** a **angličtině**. Očekáváte, že přijdou i účastníci s nastavením telefonu v němčině, španělštině nebo italštině.

- **Primární jazyk = čeština** (chyba): Účastníci s nastavením v němčině, španělštině nebo italštině uvidí český obsah. Pro ně nepoužitelné.
- **Primární jazyk = angličtina** (správně): Tito účastníci uvidí anglický obsah, kterému rozumí.

Pravidlo: **pokud má událost zahraniční účastníky, primární jazyk nastavte na angličtinu**. Češtinu přidejte jako sekundární. Česky mluvící účastníci uvidí češtinu, všichni ostatní angličtinu.

### Proč je rozhodnutí nevratné

Primární jazyk je základem datové struktury události. Obsahové funkce, registrační formulář, e-maily, microsite — všechno se vytváří s referencí na primární jazyk. Happenee nedovolí ho změnit zpětně, protože by to znamenalo rozbít integritu obsahu.

> Primární jazyk se nastavuje při zakládání události a **později ho nelze upravit**. Pokud zjistíte, že jste zvolili špatně, musíte založit novou událost.

### Kde se primární jazyk liší od sekundárních

Při úpravě obsahu v administraci přepínáte mezi jazyky pomocí **dvou vlajek** v pravém horním rohu. Sekundární jazyky lze libovolně přidávat a odebírat v **Nastavení události → Nastavení jazyka**. Primární jazyk v tomto nastavení vidíte označený jako **„Primární jazyk — nelze upravit“** a zůstane tam natrvalo.

Pokud nevyplníte obsah v sekundárním jazyce, systém použije pro daný obsah primární jazyk. To je také důvod, proč má smysl primární jazyk volit co nejširší (typicky angličtinu) — chrání vás před tím, že účastníkovi zobrazíte prázdný obsah.

## Na co si dát pozor

### Primární jazyk = čeština u události, na kterou přijdou zahraniční hosté. Německý host otevře microsite a vidí český obsah, i když událost má anglickou verzi

U událostí se zahraničními účastníky volte **primární jazyk = angličtina**. Češtinu přidejte jako sekundární. Platí i pro slovenské události — pokud mohou přijít hosté z jiných zemí, primární jazyk by měl být angličtina.

### Organizátor si uvědomí chybně nastavený primární jazyk, když už je zveřejněn registrační odkaz

Primární jazyk nelze změnit. Jediná možnost je založit novou událost a staré registrované účastníky do ní převést. Rozhodnutí udělejte při zakládání události.

### Obsah vyplněný jen v primárním jazyce, ale účastníci s tímto jazykem nastaveným v zařízení jsou v menšině

Primární jazyk neznamená „hlavní obsahový jazyk“ — znamená „fallback pro všechny neznámé jazyky“. Obsah vyplňte ve všech jazycích, které chcete nabídnout. Pro přepnutí jazyka při úpravě použijte vlajku v pravém horním rohu administrace události.

## Související články

- [Vytvoření nové události](01_vytvoreni-nove-udalosti.md)
- [Co nastavit jako první po vytvoření eventu](../01_zaciname/03_co-nastavit-jako-prvni-po-vytvoreni-eventu.md)
- [Správa kontaktů a skupin ve workspace](03_sprava-kontaktu-a-skupin-ve-workspace.md)
- [Co dělat, když kampaň nejde odeslat nebo přišla v jiném jazyce](../08_reseni-problemu/07_co-delat-kdyz-kampan-nejde-odeslat-nebo-prisla-v-jinem-jazyce.md)

<!-- source: derived/digest.tierA.cs.md -->

# Krátký přehled článků KB, které se načítají na vyžádání

- `pack_version`: `0.8.1`
- článků: 62

Jeden řádek na článek: id, název, modulové tagy a jedna věta o tom, co článek řeší. Plný text každého článku je v balíčku jako `knowledge/ondemand/<id>.md`; které číst, říká krok 7 ve `SKILL.md` podle `config/archetype_ondemand.json` a `config/kb_module_map.json`. Z přehledu samotného necituj a jeho id nedávej do `source_refs[]`: je to rozcestník, ne zdroj.

- `kb.cs.01.04` Výběr správného typu registrace (moduly: registrace). Volba typu registrace ovlivňuje, kolik práce vás čeká i jaké e-maily účastníci dostanou.
- `kb.cs.02.03` Správa kontaktů a skupin ve workspace (moduly: ucastnici_skupiny_a_viditelnost). Centrální databáze workspace pro kontakty a skupiny, sdílená napříč všemi vašimi událostmi.
- `kb.cs.02.04` Nastavení typu registrace a doplňujících otázek (moduly: registrace). Kde a jak nastavit typ registrace a doplňující otázky, a jak se kombinují s placenými vstupenkami.
- `kb.cs.02.05` Nastavení registračního formuláře (moduly: registrace). Jak postavit registrační formulář pro kontaktní údaje a doplňující otázky specifické pro danou událost.
- `kb.cs.02.06` Jak fungují podmíněné otázky v registračním formuláři (moduly: registrace). Podmíněné otázky se zobrazí jen po vybrané odpovědi, takže formulář zůstává krátký.
- `kb.cs.02.07` Práce se skupinami a viditelností (moduly: ucastnici_skupiny_a_viditelnost). Jak skupinami uvnitř události řídit viditelnost obsahu, cílení komunikace a omezení registrace.
- `kb.cs.02.08` Správa ubytování a výběru spolubydlícího (moduly: registrace). Jak nechat účastníky vybrat si v registračním formuláři spolubydlícího a připravit data pro hotel.
- `kb.cs.02.09` Jak fungují nominace a nominátoři (moduly: registrace). Nastavení nominátorů, zastupování, kapacity, import kontaktů a práce v novém portálu.
- `kb.cs.02.10` Nastavení placených vstupenek (moduly: vstupenky_a_objednavky). Jak zapnout a nastavit placené vstupenky včetně online plateb, faktur a slevových kódů.
- `kb.cs.02.11` Správa objednávek a faktur (moduly: vstupenky_a_objednavky). Kde u placené události najdete všechny objednávky a co s nimi v detailu uděláte — faktury, fakturační údaje, refundace, exporty.
- `kb.cs.02.12` Nastavení Seatingu (moduly: registrace). Placená pokročilá funkce pro přiřazování konkrétních sedadel ve vymodelovaném prostoru.
- `kb.cs.02.13` Kopírování události (moduly: nastaveni_udalosti, registrace, vstupenky_a_objednavky). Založení nové události z existující v průvodci: co se dá převzít, co se nikdy nekopíruje a na co si po kopírování dát pozor.
- `kb.cs.02.14` Jak fungují vlastní pole kontaktů (moduly: ucastnici_skupiny_a_viditelnost). Workspace-level pole, kterými rozšíříte kontaktní údaje nad standardní sadu — kde se definují, kde všude se projeví a proč je má smysl založit před spuštěním registrace.
- `kb.cs.02.15` Ruční přidání účastníka do události (moduly: ucastnici_skupiny_a_viditelnost, registrace). Všechny cesty, jak dostat člověka do události mimo registrační formulář — přiřazení kontaktu nebo skupiny, import, host bez registrace na místě — a co která udělá se stavem účastníka.
- `kb.cs.03.01` Jak funguje microsite události (moduly: microsite). Microsite je veřejná stránka události, na kterou vedou všechny odkazy z e-mailů.
- `kb.cs.03.02` Nastavení lokality a místa konání (moduly: microsite, lokalita, ucastnicka_aplikace). Obsahová funkce, která účastníkům ukazuje, kde se událost koná, s mapou a navigací.
- `kb.cs.03.03` Správa řečníků (moduly: recnici). Obsahová funkce pro profily osob v programu, jejich přiřazení k sessions a zobrazení účastníkům.
- `kb.cs.03.04` Přidání kontaktní osoby organizátora (moduly: microsite). Obsahová funkce, která dává účastníkům možnost obrátit se na konkrétní osobu z organizačního týmu.
- `kb.cs.03.05` Použití vlastního obsahu (FAQ, mapa, informační bloky) (moduly: vlastni_obsah). Univerzální obsahová funkce pro cokoli, co nezapadá do ostatních (FAQ, mapa, informační text).
- `kb.cs.03.06` Sestavení programu události — architektura (moduly: program_a_sessions). Vrstvy programu (sessions, typy, registrační bloky, místa, štítky) a jak spolu souvisí.
- `kb.cs.03.07` Jak fungují typy sessions (moduly: program_a_sessions). Šablona výchozího chování sessions: registrace, viditelnost a engagement funkce.
- `kb.cs.03.08` Nastavení workshopů a registrace na sessions (moduly: program_a_sessions). Workshop je session s povinnou registrací, kapacitou, časovým oknem registrace a termínem odhlášení; registrace probíhá v účastnické aplikaci.
- `kb.cs.03.09` Jak fungují časové sloty (moduly: program_a_sessions). Session, kde si účastník rezervuje konkrétní čas z nabídky (testovací jízdy, konzultace, schůzky).
- `kb.cs.03.10` Nastavení rezervací v programu — auta, workshopy, doprovodný program (moduly: program_a_sessions). Jak přes časové sloty a workshopy řídit rezervační scénáře typu testovací jízdy nebo doprovodný program.
- `kb.cs.03.11` Jak fungují registrační bloky, místa a štítky (moduly: program_a_sessions, ucastnici_skupiny_a_viditelnost). Tři mechanismy pro organizaci většího programu: registrační bloky, místa (sály) a štítky (kategorie).
- `kb.cs.03.12` Správa sponzorů (moduly: sponzori_a_vystavovatele). Obsahová funkce pro zobrazení partnerů události s jejich logy v kategoriích podle prominence.
- `kb.cs.03.13` Správa vystavovatelů (moduly: networking, sponzori_a_vystavovatele). Obsahová funkce pro profily vystavovatelů s místy, štítky, zástupci a přiřazenými sessions.
- `kb.cs.03.14` Jak funguje účastnická aplikace a její hlavní stránka (moduly: ucastnicka_aplikace). Prostředí, ve kterém účastník během události žije, a jak je uspořádaná hlavní stránka aplikace.
- `kb.cs.03.15` Jak funguje Moje agenda (moduly: moje_agenda). Osobní rozvrh účastníka z uložených a registrovaných sessions a nastavení bloku Moje agenda na záložce Programu.
- `kb.cs.03.16` Jak funguje Networking (moduly: networking). Engagement funkce, která účastníkům umožňuje navazovat spojení, chatovat a domlouvat schůzky.
- `kb.cs.03.17` Jak funguje Leaderboard (moduly: leaderboard). Engagement funkce pro gamifikaci se sběrem bodů za aktivity účastníků a žebříčkem nejaktivnějších.
- `kb.cs.03.18` Použití Online modulu (moduly: online_modul). Engagement funkce pro virtuální a hybridní událost s livestreamem, Social Wallem a interaktivními záložkami.
- `kb.cs.03.19` Hromadný import řečníků (moduly: recnici). Dvě metody hromadného importu řečníků — nahrání souboru XLS/XLSX/CSV s mapováním sloupců, nebo výběr konkrétních řečníků z jiné události včetně fotografií a překladů.
- `kb.cs.03.20` Hromadný import sessions (moduly: program_a_sessions). Nahrání sessions do Programu z Excelu přes 5krokový průvodce — šablona nebo vlastní soubor, mapování sloupců, validace a náhled před zápisem.
- `kb.cs.03.21` Správa sessions (moduly: program_a_sessions). Vytváření, úprava a hromadná správa sessions na záložce Sessions: panel úprav, dědičnost nastavení z typu, stav, filtrování a hromadné akce.
- `kb.cs.03.22` Hromadný import sponzorů (moduly: sponzori_a_vystavovatele). Nahrání sponzorů z Excelu — mapování sloupců, přiřazení kategorií v kroku Vazby, náhled a CSV report.
- `kb.cs.03.23` Hromadný import vystavovatelů (moduly: sponzori_a_vystavovatele). Nahrání vystavovatelů z Excelu přes 5krokový průvodce — šablona, mapování sloupců, přiřazení kategorií a míst, validace a CSV report.
- `kb.cs.03.24` Nastavení engagement funkcí (moduly: ucastnicka_aplikace). Hlasování, Otázky, Dotazník a Registrační údaje v administraci události — kde se zapínají, kdy se hodí který a jak se čtou výsledky.
- `kb.cs.04.01` Jak funguje zvací e-mail (moduly: komunikace_a_pozvanky). Zvací e-mail je první vlna pozvánek pro přiřazené kontakty.
- `kb.cs.04.02` Jak funguje potvrzovací e-mail (moduly: komunikace_a_pozvanky). Systémový e-mail, který se po dokončení registrace automaticky pošle účastníkovi s PDF vstupenkou a odkazem do aplikace.
- `kb.cs.04.03` Vytvoření a odeslání e-mailové kampaně (moduly: komunikace_a_pozvanky). Modul pro hromadné e-mailové oslovení s cílením na skupiny a stavy, plánováním rozesílky a sledováním doručitelnosti.
- `kb.cs.04.04` Kdy použít zvací e-mail a kdy e-mailovou kampaň (moduly: komunikace_a_pozvanky). Zvací e-mail jako první vlnu pozvánek po importu kontaktů, kampaň na všechno ostatní.
- `kb.cs.04.05` Cílení komunikace podle skupin a stavů (moduly: komunikace_a_pozvanky). Dvě osy cílení v Happenee: stavy účastníka a skupiny, do kterých patří.
- `kb.cs.04.06` Osobní a veřejný odkaz: jaký je rozdíl (moduly: komunikace_a_pozvanky). Kam má vést registrační tlačítko v e-mailu: osobní odkaz pro adresáta, veřejný odkaz, nebo individuální vstup zdarma u placené události.
- `kb.cs.04.07` Cesta účastníka z microsite do účastnické aplikace (moduly: komunikace_a_pozvanky, ucastnicka_aplikace). Jak vést účastníka z e-mailu na microsite, do registrace a do účastnické aplikace.
- `kb.cs.04.08` Používání oznámení v účastnické aplikaci (moduly: notifikace). Engagement funkce pro plánované zprávy v účastnické aplikaci, hlavní kanál pro komunikaci během události.
- `kb.cs.04.09` Zvací e-mail jako save the date (moduly: komunikace_a_pozvanky). Předběžné oznámení události: zvací e-mail bez registračního tlačítka, jen s datem v kalendáři. Použití před spuštěním registrace.
- `kb.cs.04.10` Komunikační flow v den události (moduly: notifikace, komunikace_a_pozvanky). Sekvence komunikace v den události: ranní e-mail s QR vstupenkou, push oznámení v aplikaci, kampaně pro nezaregistrované.
- `kb.cs.04.11` Plánování follow-up komunikace po události (moduly: komunikace_a_pozvanky). Co poslat účastníkům po události: děkovný e-mail, dotazník, materiály, navazující pozvánka. Jak segmentovat podle účasti.
- `kb.cs.04.12` Jak fungují zástupné proměnné (moduly: komunikace_a_pozvanky). Zástupné proměnné doplní do e-mailu, kampaně nebo na microsite individuální údaje účastníka — kompletní seznam univerzálních proměnných, proměnné k vlastním polím kontaktů a jak je testovat.
- `kb.cs.04.13` Komunikační flow před událostí (moduly: komunikace_a_pozvanky). Sekvence komunikace od save the date po den před událostí — kdy jde plná pozvánka, připomínka nezaregistrovaným a infomail s logistikou, a čím se která vlna posílá.
- `kb.cs.04.14` Sledování doručitelnosti e-mailů a kampaní (moduly: komunikace_a_pozvanky). Jak číst graf Stav rozesílky, co znamená Nedoručeno a jak se liší od nepřečteného, a kde najdete doručení a otevření u jednotlivého příjemce.
- `kb.cs.05.01` Jak funguje check-in a skenování QR kódů (moduly: checkin_a_tisk_jmenovek). Odbavení účastníků v servisní aplikaci (skenování QR i seznam podle jména a Kiosk režim) a ve webovém Check-inu (Prezenci).
- `kb.cs.05.02` Tisk jmenovek (moduly: checkin_a_tisk_jmenovek). Tisk jmenovek v servisní aplikaci přes Bluetooth na Brother QL-820NWB. Nastavení velikosti, obsahu a většího písma pro velké jmenovky bez QR kódu.
- `kb.cs.05.03` Příprava dat pro ubytovatele (moduly: checkin_a_tisk_jmenovek). Jak ručně sestavit data pro hotel z několika exportů, když Happenee zatím nenabízí jeden sloučený export.
- `kb.cs.05.04` Příprava servisní aplikace před událostí (moduly: checkin_a_tisk_jmenovek). Co zařídit dřív, než personál poprvé naskenuje QR kód — účty pro obsluhu, instalace aplikace, místa check-inu, párování tiskárny a zkušební sken.
- `kb.cs.06.01` Interpretace statistik eventu (moduly: reporting_a_statistiky). Kde najdete statistiky eventu (pozvánky, registrace, účast) a jak je číst.
- `kb.cs.06.02` Interpretace statistik účastníků (moduly: reporting_a_statistiky). Stavy účastníků od pozvánky až po skutečnou účast a jak je číst při reportingu i cílení komunikace.
- `kb.cs.06.03` Práce s objednávkami a exporty (moduly: reporting_a_statistiky). Rozcestník jedenácti exportů z události a kdy je který stáhnout (účetnictví, GDPR, catering, CRM).
- `kb.cs.06.04` Interpretace statistik vstupenek (moduly: vstupenky_a_objednavky, reporting_a_statistiky). Jak číst Statistiky vstupenek — prodané, zaplacené, nezaplacené, zdarma a stornované kusy, měsíční přehled, vztah k registracím a co z toho dostanete exportem.
- `kb.cs.06.05` Reporting a správa obsahu Online modulu (moduly: online_modul, reporting_a_statistiky). Co se dá vyčíst z Online modulu po události — graf sledovanosti, seznamy návštěvníků napříč moduly, exporty do Excelu a správa obsahu z chatu, otázek a hlasování.
- `kb.cs.07.10` Plánování události a kde pomůže Happenee (moduly: prurezovy). Mapa plánování události od záměru po další ročník a místo, kde do ní vstupuje nastavení a vyhodnocení v Happenee.


# Describe: story render

How an Event Story object becomes Markdown. Written as a specification so that
`render_story.py` and the model produce the same document from the same JSON.
Under `artifact: json` the model writes none and the renderer alone follows this
file; under `artifact: markdown` the model writes it without section 9 and
delivers that section only to a person who asks for it.

## Rules the renderer follows

1. The output language is `story.language`. Every fixed string below exists in
   both `cs` and `en`; pick the column, never mix.
2. Seven vocabularies are printed through `schema/labels.<language>.json`:
   `truth_status`, `commercial_state`, `certainty`, `phase_key`, `kind`,
   `selection`, `answer_status`. Look the value up and print what is there; do not
   retype it, and treat a value with no entry as a defect rather than a fallback.
   `kind` is the fallback only: a next step is printed with the label its target
   row carries, and the labels-file entry is used when a row carries none. The
   other six are always read from the labels file. Everything else this file names,
   written as `{label:...}` or `{render_string:...}`, is a fixed string defined in
   this file, because the labels file carries no entry for it.
3. The renderer decides nothing. It does not pick modules, reorder phases, hide a
   branch or add a sentence that is not in the JSON. Any reasoning belongs to the
   model.
4. Section order is fixed and does not depend on content.
5. A section whose source array is empty is skipped entirely, heading included,
   except the journey map, which always prints all eight phases.
6. No price, currency symbol or amount is ever printed. A currency in the JSON is a
   defect: the renderer stops and reports it rather than rendering it.
7. No en dash and no em dash in generated text. Separate items with a middle dot
   (`·`), a comma or a new sentence.

## Section order

| # | Section | Source |
|---|---|---|
| 1 | Hero | `presentation.hero` |
| 1b | Outcomes | `outcomes` |
| 2 | What we understood | `presentation.understood_cards[]` |
| 3 | Journey map | `presentation.journey_map.phases[]` |
| 3b | Where Happenee comes into your plan | `presentation.journey_map.phases[]`, `presentation.branch_details[].data_needed[]`, `presentation.organizer_scope` |
| 4 | Branch details | `presentation.branch_details[]`, joined to `capabilities[]` |
| 5 | Capability overview | `capabilities[]` |
| 6 | What you do not need and why | `do_not_use[]` |
| 7 | Open questions and what a human verifies | `unknowns[]`, `risks[]`, `presentation.human_verification[]`, `readiness[]` |
| 8 | Next step | `next_best_step` |
| 9 | Prototype note and assumptions | `presentation.flags`, `simulation_flags`, `assumptions[]` |
| 10 | For Happenee, in an `A+B` run only | `capabilities[]`, `presentation.human_verification[]` |

## Headings

| # | cs | en |
|---|---|---|
| title | `# {hero.event_name}` | `# {hero.event_name}` |
| 2 | `## Čemu rozumíme` | `## What we understood` |
| 3 | `## Mapa cesty` | `## Journey map` |
| 3b | `## Kde do vašeho plánu vstupuje Happenee` | `## Where Happenee comes into your plan` |
| 4 | `## Detaily větví` | `## Branch details` |
| 5 | `## Přehled funkcí` | `## Capability overview` |
| 6 | `## Co nepoužít a proč` | `## What you do not need and why` |
| 7 | `## Otevřené otázky a co ověří člověk` | `## Open questions and what a human verifies` |
| 8 | `## Další krok` | `## Next step` |
| 9 | `## Poznámka k prototypu a předpoklady` | `## Prototype note and assumptions` |
| 10 | `## Pro Happenee` | `## For Happenee` |

Phase headings inside section 3 are `### {label}`, where `label` is the
`phase_key` entry from the labels file: Před událostí, Příchod, V průběhu, Lidé,
Provoz na místě, Značka a partneři, Po události, Další ročník; Before the event,
Arrival, During, People, Live operations, Brand and partners, After the event,
Next event.
Branch headings inside section 4 are `### {branch_details[].branch_id}: {title}`,
where `title` is the branch title from the matching `journey_map` branch.

## Section 1: Hero

No heading of its own beyond the document title. `understood_summary` opens with
what changes for the organizer, not with the setup: where the brief names a pain
or an outcome, its first sentence has the shape cs „Návrh je postavený tak, aby
{what the pain becomes}.“ / en "The proposal is built so that {what the pain
becomes}.", and the setup comes in the second sentence at the earliest. Lines in
this order, each one omitted when its field is `null`:

```
# {hero.event_name}

{hero.understood_summary}

- {label:organizer} {hero.organizer}
- {label:audience} {hero.audience}
- {label:goal} {hero.goal}
- {label:scale} {hero.scale}
- {label:date} {hero.date_or_period}
- {label:archetype} {hero.archetype_label}
- {label:format} {hero.format_assumption}
```

Field labels, which are render strings and not schema enums:

| key | cs | en |
|---|---|---|
| organizer | `Pořadatel:` | `Organizer:` |
| audience | `Publikum:` | `Audience:` |
| goal | `Cíl:` | `Goal:` |
| scale | `Rozsah:` | `Scale:` |
| date | `Termín:` | `Date:` |
| archetype | `Typ události:` | `Event type:` |
| format | `Formát:` | `Format:` |

## Section 1b: Outcomes

What the event is for, from `outcomes`, before what we understood about it.
Four groups of bullets in this order, each one printed as a bold group label
and then its list in array order:

```
**{label:business}**

- {each outcomes.business item}

**{label:participant}**

- {each outcomes.participant item}

**{label:operator}**

- {each outcomes.operator item}

**{label:partner}**

- {each outcomes.partner item}
```

A group whose list is empty is not printed, its label included. No heading of
its own, the same as section 1: these are the sentences the hero is the title
of.

| key | cs | en |
|---|---|---|
| business | `Co z toho má mít pořadatel` | `What the organizer gets out of it` |
| participant | `Co z toho má mít účastník` | `What the attendee gets out of it` |
| operator | `Co z toho má mít tým na místě` | `What the on site team gets out of it` |
| partner | `Co z toho mají mít partneři` | `What the partners get out of it` |

Under the groups, when `event_success` is not `null`, one line for the measure
and, when `shown_to` is not `null`, one for the person it is shown to:

```
{label:success_measure} {event_success.measure}
{label:success_shown_to} {event_success.shown_to}
```

| key | cs | en |
|---|---|---|
| success_measure | `Podle čeho poznáte úspěch:` | `How you will know it worked:` |
| success_shown_to | `Komu to ukážete:` | `Who you show it to:` |

Under the measure, when `success_criteria[]` is not empty, a bold label and one
bullet per record in array order: the goal without its final full stop, a colon, the measure, then in brackets the
evidence and the moment, and the certainty label after a middle dot only when
the record is a working assumption. `side`, `data_sources`, `shown_to` and
`decision_after` stay in the JSON for whoever evaluates the event.

What the values mean, so the record says the same thing to whoever reads it
after the event. `evidence`: `metric` a figure, `qualitative` feedback or a
judgement, `both`, or `not_collected` when nothing the organizer or Happenee
collects today would show it, a gap to name and never a figure to invent, with
`data_sources: []`. `data_sources`: `registration`, `attendance`, `app` and
`communication` are what Happenee measures (registrations and their sources,
check-in, use of the attendee app, delivery and opening of e-mails);
`feedback_survey` is a survey the organizer runs; `partner_report`,
`sales_followup` and `other` are collected outside Happenee. `evaluated_when`:
`before` the event (registrations against the target), `during`,
`right_after`, `weeks_after` (a change people show later), or `unknown`.

```
**{label:success_criteria}**

- {goal}: {measure} ({label:evidence.<evidence>}, {label:when.<evaluated_when>}) · {certainty label}
```

| key | cs | en |
|---|---|---|
| success_criteria | `Jak poznáte, že se jednotlivé cíle splnily` | `How you will know each goal was met` |
| evidence.metric | `číslo` | `a figure` |
| evidence.qualitative | `zpětná vazba nebo posouzení` | `feedback or judgement` |
| evidence.both | `číslo i posouzení` | `a figure and a judgement` |
| evidence.not_collected | `dnes se nesbírá` | `not collected today` |
| when.before | `před událostí` | `before the event` |
| when.during | `během události` | `during the event` |
| when.right_after | `hned po události` | `right after the event` |
| when.weeks_after | `s odstupem týdnů` | `weeks after the event` |
| when.unknown | `kdy, zatím nevíme` | `when is not settled yet` |

The section is skipped under rule 5 only when all four lists are empty,
`event_success` is `null` and `success_criteria[]` is empty.

The number is `1b` and not `2` on purpose. The artifact shape paragraph, the
packaged skill files and the runner all name `section 9`, so renumbering
everything after the hero would rename the section those texts point at.

## Section 2: What we understood

One card per `understood_cards[]` entry, in array order:

```
- **{card.label}:** {card.value} · {labels.certainty[card.certainty]}
```

When at least one card has `certainty: "working_assumption"`, one line stands
between the heading and the first card, once for the whole list:
cs `Položky označené jako pracovní předpoklad jsme odvodili z briefu a z vašich odpovědí, upřesnit je můžete kdykoli.` /
en `Items marked as a working assumption come from the brief and your answers, and you can refine them at any time.` The card
itself carries its certainty label and nothing under it: the same sentence under
every assumption reads as a template, not as care.

## Section 3: Journey map

All eight phases, in schema order, whatever their `applicable` value.

For an applicable phase:

```
### {phase label}

{phase.summary}

- **{branch.title}** · {branch.participant_moment}
  - {label:condition} {branch.condition}
  - {label:capabilities} {capability labels, joined with ", "}
  - {label:detail}
```

The condition line is omitted when `condition` is `null`. The detail line is printed only when `has_detail` is `true`, and it points at the
heading in section 4 by the branch title: a `branch_id` such as `b-arrival-01` is a
story identifier and never reaches the reader, here or in a heading. Capability labels are the `name` of the matching `capabilities[]` entry, found
by the join written out in section 4. One key resolves to one string in both
sections, and the renderer needs nothing but the story object. A key with no entry
there is a defect. The capabilities line itself is omitted when `capability_keys[]`
is empty, under the same empty-list-omits-output rule that governs a whole
section: a label with nothing after it is not a line.

For a phase with `applicable: false`:

```
### {phase label}

{label:not_used} {phase.reason_if_skipped}
```

| key | cs | en |
|---|---|---|
| condition | `Platí, když:` | `Applies when:` |
| capabilities | `Funkce:` | `Features:` |
| detail | `Detail níže` | `Detail below` |
| not_used | `Nepoužíváme:` | `Not used here:` |

## Section 3b: Where Happenee comes into your plan

The same three groups the planning map is read through, after the journey map
and built from fields the story already carries. Nothing here is a new field
except `presentation.organizer_scope`, and nothing here says what Happenee
cannot do: it says what stays with the organizer.

```
## {heading 3b}

**{label:covered}**

- **{phase label}**
  - {branch.title} · {why of that branch's detail}

**{label:needed}**

- {data_needed.reason}

**{label:yours}**

- {each presentation.organizer_scope item}
```

The first group takes every phase of `presentation.journey_map.phases[]` with
`applicable: true` and at least one branch, in schema order, and under it that
phase's branches in array order. A branch with a `branch_details[]` entry of the
same `branch_id` prints its title and that entry's `why`, so the group says what
each part does for this event and not only what it is called; a branch without
one prints its title alone. The second takes every
`presentation.branch_details[].data_needed[]` entry whose `status` is
`unknown`, in array order across the details, the first entry per `key` only:
the same fact missing in three branches is one thing to send, not three. The
third is `presentation.organizer_scope` verbatim, and it is printed only when
that list is non-empty, because a story that always listed what Happenee leaves
alone would read as a list of reservations.

A group whose list is empty is not printed, its label included, and when all
three are empty the whole section is skipped under rule 5.

| key | cs | en |
|---|---|---|
| covered | `Kde vám Happenee pomůže` | `Where Happenee helps` |
| needed | `Co od vás k tomu potřebujeme` | `What we need from you for it` |
| yours | `Co zůstává u vás a vašich dodavatelů` | `What stays with you and your suppliers` |

The number is `3b` for the reason `1b` is `1b`: the texts that point at
`section 9` are not touched by a section inserted above it.

## Section 4: Branch details

One block per `branch_details[]` entry, in array order, after the visual legend:

```
## {heading 4}

{visual legend, once}

### {title}

{what_we_understood}

**{label:setup}**

- {each recommended_setup item}

**{label:why}** {why}

**{label:capabilities_setup}**

- {capability.name} · {labels.truth_status[capability.truth_status]}
  - {truth sentence for that status, when the status has one}

**{label:validate}**

- {each needs_validation item}

**{label:data}**

- {data_needed.reason} · {render_string:data_status[status]}

{image reference, when visual_ref is set}
```

The `{label:capabilities_setup}` block is the branch's capabilities with their
truth labels, and it is the only place in section 4 where a truth label appears.
It is not the same list as `{label:setup}`: `recommended_setup[]` is free text the
model wrote, this one is resolved from the data. Build it with this join, which is
the only join in the document:

1. Take the `branch_details[]` entry's `branch_id`.
2. Find the branch with that `branch_id` in
   `presentation.journey_map.phases[].branches[]`. A `branch_id` with no branch is
   a defect: the renderer stops and reports it.
3. Read that branch's `capability_keys[]`, in array order.
4. For each key, find the `capabilities[]` entry whose `key` matches, and print its
   `name`. A key with no `capabilities[]` entry is a defect and stops the renderer
   as well, because a capability named without its status is exactly what the truth
   labels exist to prevent.

The printed status is `labels.truth_status[truth_status]` and nothing else;
`commercial_state` belongs to section 5, so that a branch reads as a description of
the setup rather than as an offer. A status that carries a fixed sentence prints it
on the following line, indented by two spaces, under the same rules as section 5.
When the branch's `capability_keys[]` is empty the `capabilities_setup` block alone is omitted,
heading included, and the rest of the detail (`what_we_understood`,
`recommended_setup`, `why`, `needs_validation`, `data_needed`) is rendered as
usual.

The `needs_validation` and `data_needed` blocks are omitted when their arrays are
empty. `data_needed[].status` has no entry in the labels file, so its three values
are render strings defined here:

| `status` | cs | en |
|---|---|---|
| `provided` | `Máme` | `Provided` |
| `unknown` | `Chybí` | `Missing` |
| `assumed` | `Předpoklad` | `Assumed` |

The visual legend is printed once, between the heading and the first branch,
and only when at least one `branch_details[]` entry has `visual_ref: null`:
cs `Kde u větve zatím není obrazovka produktu, doplní ji člověk z Happenee.` /
en `Where a branch has no product screenshot yet, a Happenee human adds it.` A
branch without a visual prints nothing in its place: the same sentence under
every branch reads as a flaw in the proposal rather than as honesty.
When `visual_ref` is
set, the renderer prints a Markdown image reference naming the `shot_key`,
`![{shot_key}](shots/{shot_key}.png)`, as the last line of that branch, and nothing else: `_data/shots.json` (the
shot registry) carries only the pixel dimensions a responsive `srcset` needs, no
caption or path, so the `shot_key` itself, formatted as a reference, is what "the
image reference the shot registry gives" resolves to. The renderer never draws or
describes a screen that does not exist.

| key | cs | en |
|---|---|---|
| setup | `Co nastavíme` | `What we set up` |
| why | `Proč:` | `Why:` |
| capabilities_setup | `Nastavení` | `Setup` |
| validate | `Co ověříme` | `What we verify` |
| data | `Co k tomu potřebujeme` | `What we need for it` |

## Truth labels

Two places print a truth label, and no others: the `{label:capabilities_setup}`
block of section 4, and section 5. The strings are defined once, here, so that both
say the same thing.

The label itself is `labels.truth_status[truth_status]`, printed with no prefix,
because every one of the four reads as a status on its own. The commercial label,
which appears in section 5 only, does take a prefix: `Součást licence` with nothing
in front of it could be read as a promise about this customer's contract.

| key | cs | en |
|---|---|---|
| commercial | `Obchodně:` | `Commercially:` |

Two of the four statuses carry a fixed sentence. It is printed as its own bullet
under the capability, indented by two spaces, and it is never merged into a
sentence that promises the capability. Write "we would set this up, and
availability for your licence needs checking", never "this is included, needs
validation".

| `truth_status` | cs | en |
|---|---|---|
| `needs validation` | `Zda to vaše licence zahrnuje, potvrdí Happenee.` | `Happenee confirms whether your licence includes this.` |
| `planned-or-not-available` | `Tato možnost dnes není k dispozici.` | `This option is not available today.` |

`standard` and `configurable` carry no sentence, print no `canonical_source` and
add nothing. Sources stay in the JSON.

`availability_subtype` has no labels-file entry either. When it is not `null` it is
printed in parentheses at the end of the fixed sentence, in both sections:

| `availability_subtype` | cs | en |
|---|---|---|
| `planned` | `v přípravě` | `planned` |
| `proposed` | `návrh` | `proposed` |
| `unavailable` | `nedostupné` | `unavailable` |

## Section 5: Capability overview

One list of every capability the story selected, so that a reader can see in one
place what is standard, what needs checking and what nobody has confirmed for their
licence. Source `capabilities[]`, in array order, every entry whose `selection` is
not `not_selected`. A `not_selected` entry belongs to `do_not_use[]` and is printed
in section 6 instead, with its reason; printing it twice would read as a
contradiction.

```
## {heading 5}

- **{name}** · {labels.selection[selection]} · {labels.truth_status[truth_status]}{commercial part}
  - {truth sentence for that status, when the status has one}
  - {each limitations item}
```

`{name}` is the capability's label from the capability registry in the story's
language, copied into the story; a `key` is never printed as a name, here or in
any other section.

The commercial part is ` · {label:commercial} {labels.commercial_state[commercial_state]}`,
and it is printed only when `commercial_state` is not `unknown`. `unknown` means
nobody has checked this customer's licence, and a line saying so under every single
capability is noise that pushes the two that were checked out of sight.

`limitations[]` prints one bullet per entry, verbatim, after the truth sentence. An
empty `limitations[]` adds nothing. When no capability survives the `not_selected`
filter, or `capabilities[]` is empty, the whole section is skipped, heading
included, under rule 5.

`key`, `canonical_source`, `version_or_as_of`, `confidence`,
`commercial_boundary_evidence`, `phase_keys`, `branch_ids` and `source_refs` are
not rendered. They are how the story is checked, not how it is read.

## Section 6: What you do not need and why

One bullet per `do_not_use[]` entry, in array order:

```
- **{label or registry label for capability_key}** · {reason}
  - {label:reconsider} {reconsider_if}
```

`rule_ref` is internal and is never rendered. The printed name is `label` when
it is not `null`, and otherwise the capability registry's label for
`capability_key` in the story's language. The `capability_key` itself is never
the printed name.

| key | cs | en |
|---|---|---|
| reconsider | `Vrátíme se k tomu, když:` | `We revisit this when:` |

## Section 7: Open questions and what a human verifies

Four lists under one heading, each omitted when its source is empty, and the
section skipped under rule 5 only when all four are. First the open questions,
from `unknowns[]` where `answer_status` is not `unasked`, or where `critical` is
`true`:

```
- {unknown.question} · {labels.answer_status[answer_status]}
```

A `human_verification[]` row is `public: false` when it is about the licence
and what it includes, a price or a scoped service, Happenee's delivery capacity
and dates, a doubt about the customer's own readiness or data, or a competing
tool they already pay for; such a row prints in section 10 of an `A+B` run and
nowhere else, so this list never carries an owner such as „člověk z Happenee“
for a licence question (round 5a, b4: two licence rows printed here with that
owner and repeated in section 10).

Then the risks, `risks[]` verbatim in array order, under the bold sub-label
`{label:risks}`:

```
- {each risks item}
```

Every risk reaches the reader as written. Write it as what could go wrong at
this event and what that would cost, from the event and the answers, never as
something the product lacks and never with an id the reader does not know.

Then the verification list, from `presentation.human_verification[]` where `public`
is `true`, under the bold sub-label cs `Co ověří člověk` / en `What a human
verifies`:

```
- {question} · {reason} · {owner}
```

Last the checks by moment, `readiness[]` in array order, under the bold
sub-label `{label:checkpoints}`, and after the list one sentence for their
status, printed once rather than on every checkpoint:

```
- {readiness.checkpoint}

{render_string:readiness_status[not_verified]}
```

`not_verified` is the only `status` the schema allows; any other value is a
defect and stops the renderer, the way a label with no entry does.

| key | cs | en |
|---|---|---|
| risks | `Co může návrh ohrozit` | `What could put the plan at risk` |
| checkpoints | `Kontroly podle okamžiku` | `Checks by moment` |
| readiness_status `not_verified` | `Všechny tyto kontroly zatím zůstávají neprovedené.` | `None of these checks has been carried out yet.` |

The checks by moment stay under the heading of section 7 rather than in a
section of their own: they are what a human verifies, ordered by when, and a
new heading would split one list of things to verify in two.

An entry with `critical: true` is printed first in its list: a stable partition,
critical entries ahead of the rest, each group keeping the array order it already
had rather than being resorted by anything else. `presentation.human_verification`
entries with `public: false` are not rendered.

## Section 8: Next step

```
## {heading 8}

**{primary.label}** · {primary.what_happens_next}
{label:who} {primary.who_follows_up}
```

Then, when `alternatives[]` is non-empty, the sub-label cs `Další možnosti` / en
`Other options` and one bullet per alternative in the same shape. Labels and target
keys come from the run's target rows; the renderer never writes a link that the
target row does not carry, and a row whose `href` is `null` renders as text only.

| key | cs | en |
|---|---|---|
| who | `Navazuje:` | `Follows up:` |

## Section 9: Prototype note and assumptions

```
## {heading 9}

{presentation.flags.label[language]}

- {each limitation this run carries that changes how much the story can be trusted}

- {each simulation_flags key that is true, through the labels below}

**{label:assumptions}**

- {assumption.value} · {assumption.reason} · {label:impact} {assumption.impact_if_wrong}
```

**Limitation sentences.** The story object itself never carries this
line: it comes from the run, not from the model, so the model never writes it
and `artifact: markdown` never prints it either. Nor does the model write a
version of its own in another section: an article number or a sentence about
what was loaded means nothing to the reader. `render_story.py`'s `render()`
takes the run's limitation ids as an argument from whichever script called it
(`run_checks.py`, `scripts/runner/cli.py` or `scripts/runner/manual.py`, all of
which know them before `render_story.py` does) and prints one fixed sentence,
cs and en, for each id it recognises, in the fixed order below rather than the
order it received them. An id it does not recognise prints nothing; most of a
run's limitations are bookkeeping a reader does not need (`cost_not_reported`,
`model_actual_not_reported`) and only the ones that change how far the story
can be trusted get a sentence here. Two are wired up today:

| limitation id | cs | en |
|---|---|---|
| `ondemand_cap_reached` | Při přípravě téhle story se nenačetly všechny články nápovědy, ze kterých mohla čerpat, takže části, které se o ně opírají, nejsou ověřená konfigurace. | Not every help article this story could draw on was loaded while it was prepared, so the parts that lean on them are not verified configuration. |
| `budget_exhausted_after_reply` | Příprava skončila na limitu rozpočtu hned po odpovědi, ze které story vznikla, takže už neproběhl žádný další krok, který by ji mohl opravit nebo doplnit. | The preparation hit its budget limit right after the reply this story came from, so no further step that could have corrected or completed it followed. |

`ondemand_cap_reached` stays a general sentence rather than naming the specific
modules the dropped articles belonged to: a dropped article maps to a
`config/kb_module_map.json` module, and a module maps to several
`capability_keys[]` with no single one that stands for it, so picking one to
print would be the renderer inventing an emphasis the data does not give it,
which rule 3 forbids. No sentence prints when the run carries neither id.

Simulation flag labels, one bullet per key that is `true`, in this order:

| `simulation_flags` key | cs | en |
|---|---|---|
| `voice` | `hlas` | `voice` |
| `upload` | `nahrání souboru` | `file upload` |
| `generation` | `generování` | `generation` |
| `email_verification` | `ověření e-mailu` | `e-mail verification` |
| `booking` | `rezervace termínu` | `booking` |

A flag that is `false` is not listed. When every flag is `false`, the list is
omitted and only the prototype label prints.

| key | cs | en |
|---|---|---|
| assumptions | `Předpoklady` | `Assumptions` |
| impact | `Kdyby to bylo jinak:` | `If this is wrong:` |

## The insufficient story

When `output_status` is `insufficient_brief`, the document is short and has its own
headings. Sections 4, 5, 6 and 8 do not print at all. Their sources are empty in an
insufficient story anyway; saying so here means the renderer never has to decide.

| # | cs | en |
|---|---|---|
| title | `# Zatím nemáme dost na bezpečný návrh` | `# Not enough yet for a safe proposal` |
| body | `presentation.insufficient.message` | same |
| a | `## Co nám chybí` | `## What is missing` |
| b | `## Jak by mohla vypadat mapa cesty` | `## What the journey map would cover` |
| c | `## Další krok` | `## Next step` |

Under a: one bullet per `unknowns[]` entry whose id is in
`presentation.insufficient.missing_unknown_ids`, printed as
`- {question} · {why}`. Under b: the eight phase labels as a plain list with each
phase's `reason_if_skipped`, which is what makes the shape visible without
inventing content. Under c: `presentation.insufficient.safe_next_step`, followed by
the three-line example brief the model wrote in its reply, if the JSON carries one
in `manual_next_steps`: one paragraph per entry, in array order, with no bullet --
it stands for lines of a brief someone might paste, not a list of separate facts,
and a bulleted rendering would misrepresent it as one.

## Section 10: For Happenee

Printed only when the run header's knowledge tier is `A+B`, after section 9 and
after the status line's place in the artefact; in a Tier `A` run the section
does not exist, and no projection carries it. It is the layer a Happenee person
needs before an offer and the customer never sees, built from fields the story
already carries. The lead sentence says so, once:
cs `Tahle sekce je jen pro Happenee a do zákaznické verze nepatří.` /
en `This section is for Happenee only and does not belong in the customer version.`

Three lists, each omitted when empty, in this order:

```
## {heading 10}

{lead sentence}

**{label:coverage}**

{coverage intro}
- {count} · {truth_status label}
- {count} · {commercial_state label}

**{label:bends}**

- **{name}** · {truth_status label} · {commercial_state label} · {first limitation}

**{label:before_offer}**

- {question} · {reason} · {owner}

{delivery risks note}
```

The coverage map counts `capabilities[]` entries whose `selection` is
`recommended` or `conditional`: one line per `truth_status` in the vocabulary's
order, standard, configurable, needs validation, planned or not available, and
then one line each for `commercial_state` `additional_purchase`, `scoped_service`
and `unknown`, a line only where the count is above zero. The `unknown` line is
the offer's homework: how many selected capabilities have no verified commercial
state for this customer. Counts, never a percentage and never a verdict word: the
map is what a person reads a fit off.

"Where the product bends" lists, in `capabilities[]` order, the selected entries
whose `truth_status` is `needs validation` or `planned-or-not-available`, or
whose `commercial_state` is `additional_purchase` or `scoped_service`: the name
in bold, the status labels, and the first entry of `limitations[]` when there is
one. No source id and no `source_refs` reach the text.

"What to verify with the customer before an offer" prints every
`presentation.human_verification[]` row whose `public` is `false`, critical
rows first, in the shape section 7 uses; those rows print nowhere else. A row is
non-public when the customer should not read it as their own task: the licence
and what it includes, a price or a scoped service, Happenee's delivery capacity
and dates, a doubt about the customer's own readiness or data, a competing tool
they already pay for. A question the customer answers themselves is a public row
and belongs in section 7, not here, so the two lists do not repeat each other
(round 4: five of six rows repeated section 7 in other words). The `owner` of a
non-public row is a role inside Happenee written in the story's language, for
example cs „obchod“, „delivery“ or „customer success“, en "sales", "delivery" or
"customer success", the one place those roles are written, because this section
is theirs.

The last line refers to the risks instead of repeating them:
cs `Rizika dodání stojí v sekci „Otevřené otázky a co ověří člověk“ pod „Co může návrh ohrozit“.` /
en `Delivery risks stand in the section "Open questions and what a human verifies" under "What could put the plan at risk".`

| key | cs | en |
|---|---|---|
| coverage | `Mapa pokrytí` | `Coverage map` |
| coverage intro | `Doporučené a podmíněné funkce podle stavu, bez procent:` | `Recommended and conditional capabilities by status, no percentages:` |
| bends | `Kde se produkt láme` | `Where the product bends` |
| before_offer | `Co ověřit u zákazníka před nabídkou` | `What to verify with the customer before an offer` |

## Gate

`gate.public_sections` and `gate.verified_sections` decide what a reader sees
before verifying an e-mail address. Sections 1, 1b, 2, 3, 7 and 8 are public.
Sections 4, 5 and 6 are behind verification, along with the full `unknowns[]`
list and the save, send and share actions. Section 1b has no name of its own in
the gate vocabulary either; `schema/projection.public.json` whitelists
`/outcomes` and `/event_success`, so the four lists and the measure reach an
unverified reader with the hero they belong to. Section 3b is split by the same
rule rather than by a name of its own: its first and third groups rest on
`presentation.journey_map` and on `presentation.organizer_scope`, both
whitelisted, and its second group rests on `branch_details` and stays behind
verification with them. The `why` in the first group comes from
`branch_details` too, so an unverified reader gets the branch titles alone.
Section 7 is public, but two of its four lists are not: no projection
whitelists `risks` or `readiness`, so neither web document shows them, and only
the full document prints them. Section 5 has no name of its own in the gate
vocabulary; it renders under `branch_details`, because it is the same detail in
summary form and a truth label that a reader can see without the branch it belongs
to is the more misleading half. `schema/projection.public.json` does not whitelist
`capabilities`, so the data behind section 5 never reaches an unverified reader
either. The renderer does not invent a gate value for it.
A renderer producing the public document omits the
verified sections and prints, in their place, one line saying that the detail is
available after e-mail verification. It does not ship the hidden text in the markup
and then hide it with styling.

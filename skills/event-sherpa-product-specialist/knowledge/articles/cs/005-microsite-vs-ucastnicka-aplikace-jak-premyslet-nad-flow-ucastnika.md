# Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka

> Microsite je veřejná stránka, účastnická aplikace prostředí pro registrované, a jak se v Happenee navazují.

- Článek v Help Centru: https://help.happenee.com/cs/articles/5-microsite-vs-ucastnicka-aplikace-jak-premyslet-nad-flow-ucastnika
- English version: https://help.happenee.com/en/articles/5-microsite-vs-attendee-app-how-to-think-about-the-attendee-flow
- Kolekce: Začínáme s Happenee
- Aktualizováno: 2026-04-27

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

## Související články

- [Co je workspace a co je event](https://help.happenee.com/cs/articles/1-co-je-workspace-a-co-je-event)
- [Co nastavit jako první po vytvoření eventu](https://help.happenee.com/cs/articles/3-co-nastavit-jako-prvni-po-vytvoreni-eventu)
- [Jak funguje microsite události](https://help.happenee.com/cs/articles/21-jak-funguje-microsite-udalosti)
- [Jak funguje účastnická aplikace a její hlavní stránka](https://help.happenee.com/cs/articles/34-jak-funguje-ucastnicka-aplikace-a-jeji-hlavni-stranka)
- [Jak funguje zvací e-mail](https://help.happenee.com/cs/articles/39-jak-funguje-zvaci-e-mail)
- [Cesta účastníka z microsite do účastnické aplikace](https://help.happenee.com/cs/articles/45-cesta-ucastnika-z-microsite-do-ucastnicke-aplikace)
- [Must-have, optional a advanced funkce a moduly podle typu události](https://help.happenee.com/cs/articles/6-must-have-optional-a-advanced-funkce-a-moduly-podle-typu-udalosti)
- [Minimální doporučený setup pro malý, střední a větší event](https://help.happenee.com/cs/articles/7-minimalni-doporuceny-setup-pro-maly-stredni-a-vetsi-event)
- [Doporučené pořadí setupu eventu krok za krokem](https://help.happenee.com/cs/articles/8-doporucene-poradi-setupu-eventu-krok-za-krokem)
- [Doporučený setup pro incentive / itinerář](https://help.happenee.com/cs/articles/57-doporuceny-setup-pro-incentive-itinerar)
- [Doporučený setup pro webinář a online event](https://help.happenee.com/cs/articles/87-doporuceny-setup-pro-webinar-a-online-event)

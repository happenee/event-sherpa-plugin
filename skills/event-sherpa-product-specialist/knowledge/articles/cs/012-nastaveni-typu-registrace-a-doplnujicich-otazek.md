# Nastavení typu registrace a doplňujících otázek

> Kde a jak nastavit typ registrace a doplňující otázky, a jak se kombinují s placenými vstupenkami.

- Článek v Help Centru: https://help.happenee.com/cs/articles/12-nastaveni-typu-registrace-a-doplnujicich-otazek
- English version: https://help.happenee.com/en/articles/12-setting-the-registration-type-and-additional-questions
- Kolekce: Nastavení eventu a registrace
- Aktualizováno: 2026-09-02

---

> [!info] Krátce
> Typ registrace se nastavuje v **Nastavení události → Nastavení přístupů a registrace**. Setup-level článek — předpokládá, že jste už rozhodli o strategii (viz *Výběr správného typu registrace*). Tento článek popisuje, kde jednotlivá nastavení najdete, jaká jsou omezení a jak se typy kombinují s placenými vstupenkami a doplňujícími otázkami.

## Jak začít

- Rozhodovací vrstva (veřejná / uzavřená / nominace, schvalování ano/ne, automatická / s doplněním informací) je v článku *Výběr správného typu registrace* v kolekci Začínáme. Pokud jste ji ještě neprošli, začněte tam.
- V **Nastavení události** na záložce **Základní nastavení události** zkontrolujte sekce **Základní nastavení vstupenek** a **Nastavení přístupů a registrace**.
- Typ registrace po nákupu (automatická / s doplněním informací) se řeší u placených vstupenek zvlášť.
- Některá nastavení (povolené/zakázané domény, výchozí nastavení účtu) vyžadují **zákaznickou podporu**.

## Detail

### Typ registrace u placených vstupenek

V **Nastavení události → Placené vstupenky** (po zapnutí přepínače **Placené vstupenky**) vyberete jednu ze dvou možností:

**Registrace s doplněním informací.** Objednávající může zakoupit vstupenky i bez znalosti e-mailů účastníků. Po úhradě dostane daňový doklad a e-mail s odkazy pro doplnění registrace. Každá vstupenka se generuje až po dokončení registračního formuláře. Pokud objednávající zadá e-mail účastníka, odkaz jde přímo účastníkovi.

**Automatická registrace po nákupu vstupenky.** Objednávající musí při nákupu vyplnit e-mail ke každé vstupence. Účastníci jsou automaticky zaregistrováni po dokončení platby a dostanou potvrzovací e-mail s přiloženou vstupenkou.

> U **automatické registrace** u placených událostí se registrační formulář **ani rozšířené souhlasy** (GDPR nad rámec) nevyužívají. Pokud potřebujete sbírat doplňující data nebo získávat rozšířené souhlasy, zvolte **registraci s doplněním informací**.

U neplacených událostí se typ registrace po nákupu neřeší — registrace jde vždy přes registrační formulář.

### Schvalovaná registrace

V **Nastavení události** na záložce **Základní nastavení události** je sekce **Nastavení přístupů a registrace** a v ní **Schvalovaná registrace**. Vybíráte ze dvou karet:

- **Neaktivní (výchozí)** — účastník po registraci okamžitě dostane potvrzovací e-mail a přístup k obsahu události.
- **Aktivní** — účastník po registraci dostane e-mail o čekající registraci. Přístup k obsahu události získá až po vašem ručním schválení; po schválení mu přijde potvrzení, po zamítnutí e-mail o nepřijetí.

> Schvalovanou registraci **nelze** kombinovat s placenými vstupenkami. Pokud máte zapnuté placené vstupenky, sekce schvalované registrace je neaktivní.

### Kde se registrace schvalují

Jakmile schvalovanou registraci zapnete, objeví se v administraci události nová položka **Schvalování účastníků** — v rozbalovací nabídce **Nástroje** ve spodní části levého menu a zároveň jako dlaždice v sekci *Nástroje* na **Přehledu**. Nehledejte ji v **Registraci**; to je jiná obrazovka.

Položka je podmíněná: bez zapnuté schvalované registrace v menu není. Na jejím místě je u událostí s placenými vstupenkami **Objednávky**. Protože se obě funkce vylučují, uvidíte vždy jen jednu z nich.

Obrazovka je seznam registrací se sloupci **Kontakt**, **Registrován** a **Stav**. Nad ním je pole **Vyhledat** a filtr **S poznámkou kontaktu** (*Ano* / *Ne* / *Vše*).

Rozhoduje se **po jednom**: v každém řádku jsou tři přepínače — **Čeká na vyřízení**, **Schváleno** a **Zamítnuto**. Hromadná akce nad označenými řádky tu není, takže u větších počtů počítejte s časem. Protože jde o přepínače, dá se stav změnit i zpětně; e-maily, které už odešly, tím ale nevezmete zpět.

Pro schvalovanou registraci potřebujete jasný proces, kdo a jak rychle bude schvalovat — jinak účastníci čekají a ptají se. Alternativa je veřejná registrace bez schvalování s použitím skupin.

### Viditelnost události v účastnické aplikaci

Kdo v účastnické aplikaci uvidí, že událost existuje:

- **Pouze pro přiřazené kontakty** (výchozí) — účastník musí být přiřazen k události ve správě kontaktů nebo se zaregistrovat z veřejného odkazu.
- **Pro všechny kontakty v Kontaktech a skupinách** — všichni ve workspace uvidí, že událost existuje. Hodí se u interních firemních událostí, kde chcete, aby všichni kolegové nabídku událostí viděli.

### Přístup do události v účastnické aplikaci

Jak se účastník dostane do obsahu události v aplikaci:

- **Pouze po vyplnění registračního formuláře** (výchozí) — účastník musí projít registrací, teprve pak má přístup k obsahu.
- **Bez nutnosti vyplnění registračního formuláře** — účastník kliknutím na událost rovnou získá přístup a jeho stav se nastaví na **Zúčastním se**. Vhodné u interních událostí, kde nechcete nutit kolegy cokoli vyplňovat.

Kombinace *pro všechny kontakty* + *bez nutnosti formuláře* dává úplně otevřenou událost pro celou firmu.

### Omezení registrace

V sekci **Omezení registrace** vybíráte, odkud se lze registrovat:

- **Bez omezení** (výchozí) — registrovat se může kdokoli s odkazem.
- **Pouze pro přiřazené kontakty** — i když máte veřejný odkaz, registrovat se mohou pouze kontakty předem přiřazené k události.
- **Pouze povolené domény** — registrace jen z firemních e-mailových domén. Nastavení seznamu domén vyžaduje zákaznickou podporu.
- **Blokovat registraci ze specifických domén** — naopak blokuje e-maily z vybraných domén. Seznam nastavuje zákaznická podpora.
- **Výchozí nastavení účtu (workspace)** — globální pravidlo pro všechny události ve workspace. Nastavuje zákaznická podpora.

Dále lze nastavit:

- **Maximální počet účastníků.**
- **Deadline pro registraci** (datum a čas, po kterém se registrace zavře).
- **Povolit odhlášení z registrace** (a případně do jakého data).

### Kde se účastník odhlásí a kdy je to možné

Když **Odhlášení z registrace** povolíte (Nepovoleno / Povoleno do data), může se účastník z události odhlásit sám — v **účastnické aplikaci** (mobilní i webové), nebo na **microsite** přes svůj osobní odkaz z e-mailu. Slouží k tomu tlačítko *Odhlásit se z události*.

Tato volba je **jen u neplacené události** — sekce *Odhlášení z registrace* se v nastavení zobrazí pouze tehdy, když nemáte zapnuté **Placené vstupenky**. U placené události se zrušení účasti neřeší samoobslužným odhlášením účastníka, ale na straně organizátora — v **Objednávkách** tlačítkem **Refundace objednávky**.

### Doplňující otázky a logika „automatická vs s doplněním informací“ u neplacené události

I u **neplacené** události řešíte obdobnou volbu — chcete od účastníka jen kontaktní údaje, nebo potřebujete doplňující informace (doprava, stravování, ubytování, workshop)?

- Pokud stačí kontaktní údaje, ponechte registrační formulář jednoduchý (záložka Kontaktní údaje s nastavením povinnosti polí).
- Pokud potřebujete víc, přidejte **doplňující otázky** (záložka v registračním formuláři). Detail v článku *Nastavení registračního formuláře*.

Rozdíl mezi automatickou a s doplněním informací u neplacené události je fakticky dán tím, zda v registračním formuláři máte nějaké doplňující otázky, nebo ne — není to samostatný přepínač jako u placených vstupenek.

## Na co si dát pozor

### Aktivní schvalovaná registrace bez jasného interního procesu. Registrace stojí, účastníci se ptají, proč jim nedošlo potvrzení

Pokud nemáte určenou osobu nebo tým pro schvalování, schvalovanou registraci neaktivujte. Alternativou je veřejná registrace + skupiny, které účastníky kategorizují po registraci.

### Automatická registrace u placené události, přestože potřebujete rozšířené souhlasy (marketingový souhlas, fotografování)

U automatické registrace se registrační formulář ani rozšířené souhlasy nevyužívají. Volte **registraci s doplněním informací**.

### Doménové omezení zapnuté bez komunikace účastníkům. Lidé se registrují z osobních e-mailů a nedaří se jim to

Ve zvacím e-mailu i na microsite jasně uveďte, z jakých domén je registrace možná. Pokud potřebujete přidat nebo odebrat domény, kontaktujte zákaznickou podporu.

### Organizátor nastaví všechna omezení dopředu a ani on sám neví, která se aplikují

Omezení se kombinují. Viditelnost a přístup v aplikaci platí na úrovni účtu účastníka v appce, omezení registrace na to, kdo se může přihlásit přes microsite. Testujte na vlastním účtu, než otevřete události veřejnosti.

### Zapnutá funkce bez nutnosti registračního formuláře a očekávání, že se účastníkům bude zobrazovat registrační flow

Bez nutnosti formuláře znamená, že účastník kliknutím přímo vstoupí do události (stav Zúčastním se). Pokud potřebujete získat souhlasy nebo data, tuto variantu nepoužívejte.

## Související články

- [Výběr správného typu registrace](https://help.happenee.com/cs/articles/4-vyber-spravneho-typu-registrace)
- [Nastavení registračního formuláře](https://help.happenee.com/cs/articles/13-nastaveni-registracniho-formulare)
- [Jak fungují podmíněné otázky v registračním formuláři](https://help.happenee.com/cs/articles/14-jak-funguji-podminene-otazky-v-registracnim-formulari)
- [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti)
- [Nastavení placených vstupenek](https://help.happenee.com/cs/articles/18-nastaveni-placenych-vstupenek)
- [Správa objednávek a faktur](https://help.happenee.com/cs/articles/19-sprava-objednavek-a-faktur)
- [Jak fungují nominace a nominátoři](https://help.happenee.com/cs/articles/17-jak-funguji-nominace-a-nominatori)
- [Nastavení workshopů a registrace na sessions](https://help.happenee.com/cs/articles/28-nastaveni-workshopu-a-registrace-na-sessions)
- [Jak funguje potvrzovací e-mail](https://help.happenee.com/cs/articles/40-jak-funguje-potvrzovaci-e-mail)
- [Jak poznat, že byl zvolen špatný typ registrace](https://help.happenee.com/cs/articles/92-jak-poznat-ze-byl-zvolen-spatny-typ-registrace)

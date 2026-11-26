# Cílení komunikace podle skupin a stavů

> Dvě osy cílení v Happenee: stavy účastníka a skupiny, do kterých patří.

- Článek v Help Centru: https://help.happenee.com/cs/articles/43-cileni-komunikace-podle-skupin-a-stavu
- English version: https://help.happenee.com/en/articles/43-targeting-communication-by-groups-and-statuses
- Kolekce: Komunikace a pozvánky
- Aktualizováno: 2026-09-21

---

> [!info] Krátce
> Cílení komunikace v Happenee stojí na dvou osách — **stavech účastníka** (kde je v registraci) a **skupinách** (do čeho patří). Stavy se aktualizují automaticky, skupiny řídíte vy: vytváříte je dopředu a plníte importem, registrací, vstupenkami, slevovými kódy, odpověďmi ve formuláři nebo ručně. E-mailová kampaň cílí na obojí, zvací e-mail jen na stavy. Jazyk e-mailu se navíc vybírá podle **preferovaného jazyka kontaktu**.

## Jak začít

- Promyslete si **dopředu**, jaké skupiny budete potřebovat. Nové pravidlo nemusí zpětně zařadit dřívější účastníky. Chybějící členství můžete doplnit ručně nebo importem; výsledek ověřte.
- Při importu kontaktů vyplňte sloupec s **preferovaným jazykem** — systém podle něj rozesílá jazykovou variantu.
- Uvědomte si rozdíl: **stavy** jsou automatické (na co má kontakt reagovat), **skupiny** jsou ruční (jaké má postavení).
- Pro segmentovanou komunikaci (jen VIP, jen řečníci, jen ČR kontakty) volte **e-mailovou kampaň**. Zvací e-mail cílí jen podle stavů.

## Detail

### Stavy účastníka

Stav říká, kde účastník je v registračním procesu nebo v průběhu události. Stav řídí systém, vy ho pouze pozorujete (s výjimkou ručního překlopení).

V e-mailové kampani je každý stav samostatné odesílací tlačítko na záložce **Odeslání**:

- **Všichni** — všechny kontakty přiřazené k události.
- **Registrovaní** — dokončená registrace.
- **Nepozvaní** — kontakt je přiřazený k události, ale zvací e-mail mu ještě nešel.
- **Bez reakce** — pozvánku dostal, ale zatím nijak nereagoval.
- **Nepřečetli zvací e-mail** — podle trackingu otevření.
- **Účastníci na místě** — lidé, kteří na událost fyzicky dorazili.
- **Zobrazili webovou aplikaci** / **Nezobrazili webovou aplikaci** — zda si účastník už otevřel webovou aplikaci události, tedy účastnickou aplikaci v prohlížeči.

Kolik kontaktů do kterého stavu spadá, uvidíte ještě před kliknutím v přehledu **Kontakty přiřazené k události** na téže záložce. Zvací e-mail nabízí užší výběr stavů (*Nepozvaní*, *Kdo si nepřečetl zvací e-mail*, *Neregistrovaný*) a neumí je kombinovat se skupinami.

**Uživatele mobilní aplikace oslovíte přes Oznámení.** Odesílací tlačítka kampaně sledují webovou aplikaci. Na lidi s mobilní aplikací proto cilte **Oznámením** v účastnické aplikaci, které rozlišuje mobilní i webovou aplikaci (viz článek *Používání oznámení v účastnické aplikaci*).

### Skupiny — jak do nich lidi padají

Skupiny vytváří vždy organizátor, ne systém. Kontakt se do skupiny může dostat několika cestami:

- **Ruční přiřazení ve správě kontaktů** — vyberete kontakt a přidáte ho do skupiny.
- **Hromadný import s `#skupina`** — v Excelu použijete prefix ve sloupci skupiny při importu. Detail v článku *Správa kontaktů a skupin ve workspace*.
- **Po registraci ke vstupence** — u vstupenky si v nastavení vyberete, do jaké skupiny se účastník zařadí po dokončení registrace.
- **Přes individuální nebo hromadný registrační odkaz** — u odkazu si volíte skupinu po registraci (typicky partnerský odkaz → skupina „Partner XY“).
- **Po použití slevového kódu** — kód může zařadit do skupiny („Skupina po použití kódu“).
- **Podle odpovědi v registračním formuláři** — u typů otázek, které umí zařadit do skupiny (výběr z možností). Například odpověď „Dopravím se autobusem č. 2“ → skupina „Autobus 2“.
- **Po registraci na workshop nebo časový slot** — účastník workshopu A padá do skupiny „Workshop A“.

### K čemu skupiny v komunikaci slouží

- **Cílení e-mailové kampaně** — kampaň pošlete jen skupině VIP, jen řečníkům, jen skupině „Česky“.
- **Cílení oznámení** v účastnické aplikaci — oznámení dostane jen skupina, pro kterou je relevantní.
- **Viditelnost modulů** — některé obsahové / engagement funkce vidí jen skupina (detail v článku *Práce se skupinami a viditelností*).
- **Skenování na check-inu** — personál vidí u QR kódu, zda účastník patří do vybrané skupiny (VIP, speaker).

### Jazykový fallback při importu

Jazyk e-mailu se neřídí podle jazyka události — řídí se **preferovaným jazykem kontaktu**. Proto při importu vyplňujte sloupec s jazykem.

Tři situace:

- Kontakt má preferovaný jazyk **čeština** → dostane českou variantu e-mailu.
- Kontakt má preferovaný jazyk **angličtina** → dostane anglickou variantu.
- Kontakt **bez jazyka** → použije se primární jazyk události (při statistikách je vidět „X kontaktů bez jazyka“).

Při registraci z microsite se preferovaný jazyk automaticky přednastaví podle toho, v jakém jazyce si účastník otevřel microsite.

### Typické segmentace v praxi

- **VIP a řečníci** — vlastní e-maily s detaily o vyzvednutí jmenovky, hotelu, hlavní zkoušce.
- **Jen anglicky mluvící** — oddělená kampaň s odlišným tónem nebo formátem.
- **Jen neregistrovaní** — dopozvánka, která nebudí lidi, kteří už přišli.
- **Skupina ze vstupenky** — pokud máte tři typy vstupenek a jen jedna má přístup do VIP lounge, kampaň jen pro držitele této vstupenky.
- **Skupina z workshopu** — připomínka dvě hodiny před workshopem, ať si nezapomenou přijít.
- **Partneři** — každý partner má vlastní hromadný registrační odkaz, který účastníky přiřadí do skupiny „Partner XY“; cílená komunikace jen pro ně.

### Kombinace stavů a skupin v kampani

V e-mailové kampani můžete filtry kombinovat — například:

- „Registrovaní + skupina VIP“ → VIP reminder.
- „Bez reakce + skupina České kontakty“ → dopozvánka česky.
- „Zobrazili webovou aplikaci + skupina Řečníci“ → rychlá info řečníkům, kteří už webovou aplikaci otevřeli.

Skupinu vyberete v dropdownu **Cílení** a teprve pak kliknete na tlačítko stavu.

### Omezení — lokální a systémové skupiny

Dnes v Happenee fungují pouze **globální uživatelské skupiny** — vytváříte si je ručně a platí napříč workspace. Existují plány na:

- **Lokální skupiny** — skupiny jen pro konkrétní událost, aby se neznečišťoval globální seznam.
- **Systémové skupiny** — automaticky vytvářené podle stavů (například *Potvrzení účastníci*, *Registrovaní*).

Obě varianty jsou v přípravě, v samoobsluze zatím nejsou. Pro dnešní účely počítejte s tím, že skupiny si pojmenujete a spravujete ručně a že stavy (registrován, přišel) nejsou automatické skupiny, ale stavy — cílíte na ně pomocí filtru stavu, ne skupinou.

### Kontrola před konkrétní rozesílkou

Určete, jaký úkol má příjemce udělat. Potom ověřte skupinu, aktuální registrační stav, jazyk a správný cílový odkaz. Již registrovanému hostovi neposílejte výzvu k nové registraci jen proto, že u něj chybí záznam otevření e-mailu. Chybějící záznam otevření sám nedokazuje, že zprávu nečetl.

Při opravě špatného zařazení porovnejte odpověď ve formuláři a členství ve skupině. Pokud skupina řídí také viditelnost nebo vstup, ověřte i tento dopad. Změnu vyzkoušejte na vhodném testovacím kontaktu, potom zkontrolujte skutečné cílení před odesláním.

## Na co si dát pozor

### Skupina pro follow-up nebyla připravená včas

Skupiny si promyslete a vytvořte **před spuštěním registrace**. Pravidla plnění (ze vstupenek, z odpovědí ve formuláři, ze slevových kódů, z workshopů) nastavte tak, aby se skupiny plnily samy.

### Organizátor importuje kontakty bez jazyka a následně se diví, proč anglicky mluvící dostali českou pozvánku

Při importu vyplňujte sloupec **preferovaný jazyk**. Pokud chybí, doplňte ho ve správě kontaktů (individuálně nebo opakovaným importem).

### Organizátor chce cílit na skupinu zvacím e-mailem a nedaří se mu to

Zvací e-mail **neumí cílit podle skupin**, jen podle stavů. Pro cílení na skupiny použijte e-mailovou kampaň.

### Organizátor očekává, že po registraci vznikne automatická skupina *Zaregistrovaní* a bude na ni cílit

Tyto automatické skupiny **nejsou**. V kampani použijte odesílací tlačítko *Registrovaní* jako filtr stavu. Systémové skupiny jsou v plánu, ale zatím nejsou k dispozici.

### Organizátor využívá jen stavy a ztrácí schopnost posílat různé zprávy různým segmentům („jen VIP“, „jen z této vstupenky“)

Přidejte do workflow skupiny — přes vstupenky, formulář, slevové kódy. Jakmile jednou nastavíte plnění skupin, dostanete segmentaci zdarma.

### Organizátor udělá *moc* skupin a ztrácí v nich přehled; komunikace se stává neřiditelnou

Mějte rozumný počet skupin — typicky 5–15 pro středně velkou událost. Skupiny, které nevyužíváte pro komunikaci ani viditelnost, nemá smysl udržovat.

## Související články

- [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace)
- [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti)
- [Vytvoření a odeslání e-mailové kampaně](https://help.happenee.com/cs/articles/41-vytvoreni-a-odeslani-e-mailove-kampane)
- [Jak funguje zvací e-mail](https://help.happenee.com/cs/articles/39-jak-funguje-zvaci-e-mail)
- [Kdy použít zvací e-mail a kdy e-mailovou kampaň](https://help.happenee.com/cs/articles/42-kdy-pouzit-zvaci-e-mail-a-kdy-e-mailovou-kampan)
- [Zvací e-mail jako save the date](https://help.happenee.com/cs/articles/63-zvaci-e-mail-jako-save-the-date)
- [Interpretace statistik účastníků](https://help.happenee.com/cs/articles/51-interpretace-statistik-ucastniku)
- [Používání oznámení v účastnické aplikaci](https://help.happenee.com/cs/articles/46-pouzivani-oznameni-v-ucastnicke-aplikaci)
- [Komunikační flow v den události](https://help.happenee.com/cs/articles/64-komunikacni-flow-v-den-udalosti)
- [Plánování follow-up komunikace po události](https://help.happenee.com/cs/articles/65-planovani-follow-up-komunikace-po-udalosti)
- [Komunikační flow před událostí](https://help.happenee.com/cs/articles/79-komunikacni-flow-pred-udalosti)
- [Sledování doručitelnosti e-mailů a kampaní](https://help.happenee.com/cs/articles/80-sledovani-dorucitelnosti-e-mailu-a-kampani)
- [Co dělat, když kampaň nejde odeslat nebo přišla v jiném jazyce](https://help.happenee.com/cs/articles/88-co-delat-kdyz-kampan-nejde-odeslat-nebo-prisla-v-jinem-jazyce)

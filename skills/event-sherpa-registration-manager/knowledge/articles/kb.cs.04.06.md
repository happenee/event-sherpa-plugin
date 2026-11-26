<!-- source: kb.cs.04.06 -->

---
title: "Osobní a veřejný odkaz: jaký je rozdíl"
description: "Kam má vést registrační tlačítko v e-mailu: osobní odkaz pro adresáta, veřejný odkaz, nebo individuální vstup zdarma u placené události."
modules: ["komunikace_a_pozvanky"]
last_updated: "2026-09-16"
version: 5
---

> [!info] Krátce
> U registračního tlačítka ve zvacím e-mailu i v e-mailové kampani vybíráte v sekci **Kam má registrační tlačítko vést?**, kam adresáta pošlete. Vždy máte na výběr **Osobní odkaz pro adresáta** (pozvánka svázaná s konkrétním kontaktem) a **Veřejný odkaz** (sdílitelný, každý si zadá vlastní e-mail). U placené události přibývá třetí volba **Individuální vstup zdarma** — adresát se zaregistruje bez nákupu vstupenky. Volba rozhoduje, jestli z pozvánky uděláte privátní guest list, nebo kanál na šíření dál.

## Jak začít

- Rozhodněte, jestli má být pozvánka **osobní** (platí pro adresáta), nebo **sdílitelná** (zaregistruje se kdokoli s odkazem).
- U placené události rozhodněte navíc, jestli má adresát **platit**. Osobní odkaz ho pošle na nákup vstupenky. Pokud má jít o vstup zdarma, potřebujete volbu **Individuální vstup zdarma**.
- U veřejného odkazu počítejte s tím, že ho lidé budou přeposílat. Pokud to nechcete, zvolte osobní odkaz.

## Detail

Volba je v obsahu e-mailu pod sekcí **Kam má registrační tlačítko vést?**. **Nabídka se liší podle typu události:** u neplacené události nabízí dvě možnosti, u placené tři. *Individuální vstup zdarma* se u neplacené události nezobrazuje — nemá tam co obcházet.

### Osobní odkaz pro adresáta

Odkaz je unikátní pro adresáta e-mailu — systém v něm nese identifikaci konkrétního kontaktu. **Chová se ale jinak podle toho, jestli má událost placené vstupenky.**

**U neplacené události** je e-mail pro registraci pevně daný a nelze ho změnit. Adresát může účast **potvrdit, nebo odmítnout**. Když odkaz přepošle někomu jinému, ten se pod svým jménem nezaregistruje — registrace patří původnímu adresátovi.

**U placené události** slouží osobní odkaz hlavně k **personalizaci microsite**. Adresát pokračuje na **výběr a nákup vstupenky** a při nákupu **může uvést jiný e-mail**, než na který pozvánka přišla. Osobní odkaz u placené události tedy **není nástroj, jak pustit někoho zdarma**, a neuzavírá registraci tak těsně jako u neplacené události.

Kdy použít:

- Osobní pozvánka VIP nebo konkrétnímu partnerovi.
- Interní firemní událost **bez placených vstupenek**, kde nechcete registrace mimo pozvaný seznam.
- Invitation-only událost **bez placených vstupenek**, kde máte uzavřený seznam.
- Placená událost, kde má být microsite personalizovaná a host si vstupenku koupí sám. Pokud potřebujete mít jistotu, kdo se registruje, doplňte omezení *Registrace pouze pro přiřazené kontakty*.

### Veřejný odkaz

Veřejný odkaz nevede na předvyplněnou registraci. Vede na microsite, kde návštěvník **nejdřív zadá e-mail** a teprve pak pokračuje dál — u neplacené události do registračního formuláře, u placené k výběru vstupenky a případné platbě. Zadat lze **libovolný e-mail**.

Chování:

- Odkaz lze zkopírovat a **poslat komukoli**. Nový příjemce se registruje pod svým e-mailem.
- Lze ho dát na sociální sítě, na web nebo do interního newsletteru.
- Hodí se na veřejné události a kampaně, které mají přivést co nejvíc registrací.

Kdy použít:

- Veřejná událost, kam chcete pustit co nejvíc lidí.
- Pozvánka, kterou mají účastníci šířit dál (například „přiveďte kolegu“).
- Když ještě nevíte, kdo přijde, a chcete to nechat otevřené.

### Všechny odkazy stojí na adrese microsite

Osobní odkaz, veřejný odkaz i individuální vstup zdarma vedou na adresu microsite `https://www.happenee.com/events/<slug>` a liší se jen tím, co za ni Happenee připojí. Když slug v **Microsite události → Nastavení** změníte, přestanou platit **všechny tři typy odkazů** v už odeslaných e-mailech, ne jen veřejný odkaz sdílený na webu. Přesměrování ze staré adresy neexistuje. Adresu proto měňte před prvním rozesláním; detail je v článku [Jak funguje microsite události](../03_obsah-a-zkusenost-ucastnika/01_jak-funguje-microsite-udalosti.md).

### Individuální vstup zdarma (jen placená událost)

Třetí volba se nabízí pouze u události se zapnutými **Placenými vstupenkami**. Pro adresáta se použije **individuální registrační odkaz bez nutnosti nákupu vstupenky** — tedy přesně scénář „pusťte tento seznam lidí zdarma“.

To je správná volba pro **guest list u placené události**. Osobní odkaz ji nenahradí: ten adresáta pošle na nákup.

### Guest list u placených událostí

Častý požadavek organizátora placené události: *„Chci pustit 50 kontaktů zdarma, aniž by platili.“*

Postup:

1. Naimportujete 50 kontaktů do správy kontaktů (s preferovaným jazykem).
2. Přiřadíte je k události.
3. Vytvoříte e-mailovou kampaň (nebo použijete zvací e-mail) a u registračního tlačítka zvolíte **Individuální vstup zdarma**.
4. Odešlete kampaň právě těmto 50 kontaktům.
5. Adresáti se přes odkaz dostanou do registrace **bez nákupu vstupenky**.

Rozdíl oproti stoprocentnímu slevovému kódu: u slevového kódu účastník prochází **nákupním procesem**, i když je výsledek 0 Kč. Individuální vstup zdarma nákup vynechá, což je pro hosta čistší.

### Individuální a hromadné registrační odkazy

Týž princip nabízí i modul **Placené vstupenky**, kde se registrační odkazy spravují samostatně:

- **Individuální odkaz** — jednorázový, pro jednoho člověka, obchází nákup vstupenky.
- **Hromadný odkaz** — jeden odkaz s nastaveným maximálním počtem použití (například 20). Hodí se dát partnerovi: ten ho šíří mezi své hosty a systém hlídá limit.

Oba typy umí **po registraci zařadit do skupiny** (například „Partner XY“), takže je můžete dál oslovovat segmentovaně. Detail v článku *Nastavení placených vstupenek*.

Liší se způsob distribuce: **Individuální vstup zdarma** vygeneruje odkaz adresátům kampaně nebo zvacího e-mailu, kdežto odkazy z modulu Placené vstupenky si rozesíláte vlastní cestou a hromadný odkaz navíc umí sdílené použití s limitem.

### Kombinace s e-mailovou kampaní

E-mailová kampaň je „kontejner“ pro doručení odkazu:

- Kampaň s **osobním odkazem** → pozvánka cílená na konkrétní kontakty nebo skupiny.
- Kampaň s **veřejným odkazem** → sdílená informace, i když cílíte jen na skupinu (ta ho může přeposlat dál).
- Kampaň s **individuálním vstupem zdarma** → guest list u placené události.

Typické použití: kampaň pro VIP s osobním odkazem, reminder registrovaným s veřejným odkazem (ať klidně pošlou kolegovi).

### Rozhodovací pravidlo

- **Invitation-only, uzavřený seznam (neplacená událost)** — Osobní odkaz pro adresáta
- **Guest list zdarma u placené události** — Individuální vstup zdarma
- **Partnerský odkaz s limitem použití** — Hromadný registrační odkaz (v Placených vstupenkách)
- **Veřejná pozvánka na sociální sítě** — Veřejný odkaz
- **Reminder registrovaným a příležitostné šíření dál** — Veřejný odkaz
- **Personalizovaná microsite u placené události (host si vstupenku koupí)** — Osobní odkaz pro adresáta

## Na co si dát pozor

### Organizátor pošle na placenou událost pozvánku s **osobním odkazem** a čeká, že host projde zdarma

Osobní odkaz u placené události vede na **výběr a nákup vstupenky** — personalizuje microsite, ale placení neobchází. Pro vstup zdarma zvolte **Individuální vstup zdarma**, nebo použijte individuální či hromadný registrační odkaz z modulu Placené vstupenky.

### Organizátor pošle placené události pozvánku se **stoprocentním slevovým kódem** a diví se, proč musí host i tak projít nákupem

Slevový kód snižuje cenu, ale nákupní proces zůstává. Pro guest list zdarma použijte **Individuální vstup zdarma** v e-mailu, nebo registrační odkazy v modulu Placené vstupenky.

### Organizátor dá do zvacího e-mailu **veřejný odkaz** a pak se diví, že se registrují lidé mimo pozvaný seznam (někdo odkaz přeposlal)

Pro uzavřený seznam použijte **Osobní odkaz pro adresáta**. Pokud musí jít o veřejný odkaz, zapněte v Nastavení události omezení *Registrace pouze pro přiřazené kontakty*.

### Organizátor spoléhá u placené události na to, že osobní odkaz uzamkne registraci na adresáta

U neplacené události e-mail pro registraci opravdu změnit nejde. U **placené** ale může adresát při nákupu vstupenky uvést **jiný e-mail**, takže registrace nemusí skončit na tom, komu pozvánka přišla. Pokud potřebujete jistotu, kdo se registruje, doplňte omezení *Registrace pouze pro přiřazené kontakty*.

### Organizátor sdílí **osobní odkaz** na sociálních sítích a diví se, že se registruje jen jeden člověk

Osobní odkaz patří konkrétnímu adresátovi. Pro veřejné sdílení použijte **Veřejný odkaz**, nebo veřejný odkaz na microsite z modulu Microsite události.

### Organizátor rozdá **hromadné odkazy** několika partnerům a po čase neví, kolik lidí přes který přišlo

Hromadný odkaz v modulu Placené vstupenky má limit vždy: **Počet použití** nastavíte od 1 do 500. Po naplnění limitu odkaz místo registrace ukáže hlášku, že už byl použit. Kolik z limitu který partner vyčerpal, zjistíte na stránce **Placené vstupenky** pod **Exporty → Export registračních odkazů**. Soubor ukazuje u každého odkazu limit, počet použití a stav, třeba **Vyčerpán**. Jména registrovaných v exportu nejsou; pokud je potřebujete dohledat, nastavte odkazu ještě před rozesláním zařazení do skupiny (například „Partner XY“) a hledejte podle ní. Zařazení se zpětně nedoplní lidem, kteří se zaregistrovali dřív.

### Organizátor si myslí, že lidé z veřejného odkazu dostali zvací e-mail

Registrace z veřejného odkazu je ve statistikách vidět jako příchod přes otevřený odkaz — systém těmto lidem žádnou pozvánku neposlal. Pokud je chcete oslovit dodatečně, použijte e-mailovou kampaň cílenou na stav *Zaregistrovaní* nebo na skupinu, do které spadli.

### Organizátor po rozeslání pozvánek změní adresu microsite a všechny odkazy z e-mailů přestanou fungovat

Osobní odkaz, veřejný odkaz i individuální vstup zdarma nesou slug microsite, takže změna adresy v *Microsite události → Nastavení* je zneplatní všechny najednou a stará adresa nepřesměrovává. Buď slug vraťte na původní tvar, nebo kampaň či zvací e-mail rozešlete znovu.

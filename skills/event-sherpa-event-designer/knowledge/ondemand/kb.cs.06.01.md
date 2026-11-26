<!-- source: kb.cs.06.01 -->

---
title: "Interpretace statistik eventu"
description: "Kde najdete statistiky eventu (pozvánky, registrace, účast) a jak je číst."
modules: ["reporting_a_statistiky"]
last_updated: "2026-08-07"
version: 3
---

> [!info] Krátce
> Statistiky eventu jsou váš hlavní pohled na to, jak si událost vede — před událostí, v průběhu i po ní. Najdete je na několika místech: na kartě eventu v seznamu ve workspace, v **Přehledu** události, v sekci **Statistiky** v levém menu. Klíčové stavy (pozvánky, registrace, účast) i grafy jsou dostupné **jen v administraci**. Kdo má čísla vidět, ale do administrace přístup nemá, dostane od vás **export** do Excelu nebo CSV.

## Jak začít

Rozhodněte dopředu, kdo potřebuje jaké informace a jak často:

- **Operativně pro organizátorský tým** — otevírejte **Statistiky** přímo z levého menu události. Máte tam plný detail.
- **Pro management nebo kolegy bez přístupu do administrace** — stáhněte **export** ze sekce **Statistiky** a pošlete jim soubor. Živý pohled na statistiky mimo administraci sdílet nejde.
- **Pro rychlý denní přehled** — sledujte statistiky na **kartě eventu v seznamu** ve workspace. Vidíte souhrn pro každý event bez nutnosti proklikávat.

## Detail

### Karta eventu ve workspace

Na hlavní obrazovce po přihlášení (v seznamu eventů) vidíte u každé události:

- Název, datum, počet dnů do začátku
- Jaké obsahové a engagement funkce má event zapnuté
- Nastavené jazyky
- Stav registrace (kolik lidí je v jakém stavu)
- Statistiky ke kliknutí — **pozvánky**, **registrace**, **kdo přišel**, **kdo zobrazil event**, **kdo má staženou mobilní aplikaci**

Každou tu statistiku můžete prokliknout a dostat se rovnou do detailu. Typicky vidíte i počty typu *„Zúčastním se + doprovod“*.

### Přehled události

Po kliknutí na event se v levém menu otevře jako první **Přehled**. Je to úvodní stránka události s nástroji a statistikami. Kromě základních informací o události tam najdete:

- Rychlé odkazy na *Správu kontaktů a skupin*, *Registraci*, *Prezenci*, *Objednávky*, *Nominace*
- Odkaz na **Statistiky s účastníky** a **Statistiky vstupenek** (druhé jen pokud máte zapnuté placené vstupenky)
- Stručné shrnutí jednotlivých sekcí, které jsou vlevo v menu (nastavení, obsah, engagement, komunikace, vstupenky, odbavení)

Přehled používejte jako denní výchozí bod, ne jako místo pro hluboký reporting.

### Sekce Statistiky v levém menu

Obsahuje čtyři oblasti:

1. **Statistiky s účastníky** — stavy, kdo si zobrazil event, kdo má aplikaci. Detailně viz [Interpretace statistik účastníků](02_interpretace-statistik-ucastniku.md).
2. **Statistiky vstupenek** — pouze u placených událostí. Detailně pokryto v článku [Nastavení placených vstupenek](../02_nastaveni-eventu-a-registrace/10_nastaveni-placenych-vstupenek.md) (sekce statistiky).
3. **Grafy** — registrace zvacího e-mailu, účasti, průběh registrace v čase. Autor produktu avizuje, že další grafy a statistiky budou postupně přibývat — pokud tam něco postrádáte, pravděpodobně to v budoucnu přibude.
4. **Exporty** — do Excelu/CSV, včetně skenování, odpovědí formuláře, seznamu uživatelů aplikace. Všechny exporty popsány v článku [Práce s objednávkami a exporty](03_prace-s-objednavkami-a-exporty.md).

### Jak dostat čísla ven z administrace

Statistiky jsou součástí administrace — kdo do ní nemá přístup, ten se k nim nedostane. Neexistuje veřejný ani read-only odkaz, kterým byste konkrétní pohled na statistiky poslali ven.

Když management, obchodníci nebo kolegové mimo Happenee potřebují čísla, máte dvě cesty:

- **Export do Excelu nebo CSV** — v sekci **Statistiky → Exporty**. Pošlete soubor a příjemce si s ním pracuje sám. Detail všech exportů v článku [Práce s objednávkami a exporty](03_prace-s-objednavkami-a-exporty.md).
- **Vlastní shrnutí** — u pravidelného reportingu (týdenní stav registrací pro management) se vyplatí posílat krátký přehled čísel, ne surový export. Export obsahuje osobní údaje účastníků, které příjemce většinou nepotřebuje.

Počítejte s tím, že export je **snapshot k okamžiku stažení**. Kdo potřebuje čísla průběžně, musí si o nový export říct — nebo mu je posílejte v pravidelném rytmu.

### Kde se stavy berou

Statistiky se nepočítají ručně — jsou přímým odrazem:

- **Zvacích e-mailů** — odeslán, doručen, otevřen, reagováno
- **Registračního formuláře** — dokončené registrace
- **Kampaní** — statistiky rozesílky v detailu kampaně, viz [Vytvoření a odeslání e-mailové kampaně](../04_komunikace-a-pozvanky/03_vytvoreni-a-odeslani-e-mailove-kampane.md)
- **Servisní aplikace / Prezence** — kdo a kdy přišel (check-in)
- **Účastnické aplikace** — kdo má aplikaci staženou a přihlášenou

Když se vám nějaké číslo nezdá, začněte tím, že zkontrolujete, jestli ten zdroj (kampaň, check-in, aplikace) je správně nastavený.

## Na co si dát pozor

### Statistiky eventu sledujete až po události

Hlavní hodnota je průběžná. Krása statistik před událostí je, že umíte zareagovat — například pokud pět dní před termínem vidíte, že polovina pozvaných neotevřela e-mail, pošlete druhou vlnu připomínky.

### Slíbíte managementu odkaz na živé statistiky

Statistiky se odkazem sdílet nedají — jsou vidět jen z administrace. Domluvte se místo toho na exportu: pošlete soubor ze sekce **Statistiky → Exporty**, nebo se dohodněte na pravidelném rytmu (například krátké shrnutí čísel jednou týdně).

### Čekáte na reporting článek / funkci, která ještě není

Autor produktu explicitně říká, že grafy a statistiky ještě přibývají. Některé věci, které si představujete (například detailní analýza křivky registrace), v UI dnes nejsou — pracujte s tím, co je, a chybějící pohledy řešte exporty do Excelu.

### Spoléháte na statistiky na kartě eventu jako na jediný zdroj

Karta eventu je rychlý přehled. Pro detailní rozbor (filtry podle skupin, segmenty) jděte do sekce **Statistiky** v levém menu události.

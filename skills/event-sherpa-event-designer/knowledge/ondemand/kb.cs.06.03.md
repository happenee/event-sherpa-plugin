<!-- source: kb.cs.06.03 -->

---
title: "Práce s objednávkami a exporty"
description: "Rozcestník jedenácti exportů z události a kdy je který stáhnout (účetnictví, GDPR, catering, CRM)."
modules: ["reporting_a_statistiky"]
last_updated: "2026-10-26"
version: 7
---

> [!info] Krátce
> Happenee vám umožňuje stáhnout data z události **do jedenácti různých exportů**, každý slouží k jiné práci — účetnictví, GDPR audit, analýza skenování, podklady pro catering, onboarding do CRM. Většina exportů je v Excelu, některé i v CSV. Exporty najdete v sekci **Statistiky** a v detailech jednotlivých modulů (Objednávky, Placené vstupenky, Registrační formulář, Účastnická aplikace). Články o jednotlivých modulech popisují, co v exportech je; tenhle článek slouží jako **rozcestník**: který export kdy stáhnout.

## Jak začít

Rozhodněte, **na co data potřebujete**:

- **Účetnictví a fakturace** — Objednávky, Objednávky po vstupenkách, Export PDF faktur, Statistiky vstupenek. Pracujete nejspíš s někým, kdo je zvyklý na Excel.
- **Partneři a pozvánky zdarma** — Export registračních odkazů: kolikrát byl který odkaz použit a které hromadné odkazy už mají vyčerpaný limit.
- **Hotel, catering, organizační tým** — Seznam účastníků (filtr podle skupin, ubytování). Obvykle jeden export stačí.
- **Jeden přehled s vybranými údaji z více zdrojů** — **Reporty účastníků** v části **Exporty** na stránce **Statistiky a reporting**: sloupce ze skupin, formuláře, programu, engagementu i vstupenek v jednom XLSX, každý účastník na jednom řádku. Postup v článku [Sestavení reportu účastníků](06_sestaveni-reportu-ucastniku.md).
- **GDPR audit / dotaz na konkrétní osobu** — export *GDPR souhlasy nad rámec*.
- **Vyhodnocení check-inu** — export skenování.
- **Odpovědi z formuláře pro analýzu** — export registračního formuláře (Excel nebo CSV pro zpracování skriptem).
- **Vyhodnocení aplikace** — export aktivity uživatelů a seznam uživatelů, kteří mají aplikaci.

## Detail

### 1. Všichni účastníci (Excel)

Jeden soubor se všemi kontakty přiřazenými k události. Obsahuje kontaktní pole, stav účastníka, skupiny, preferovaný jazyk, vstupenku (pokud událost je placená).

**Typické použití:**
- Podklad pro catering / hotel / organizátory
- Sestavení jmenovek, pokud nepoužíváte tisk přímo z Happenee
- Rychlé zkontrolování, kdo není v jaké skupině

Pro přípravu dat pro hotel má Happenee omezený export — viz [Příprava dat pro ubytovatele](../05_den-akce-a-provoz/03_priprava-dat-pro-ubytovatele.md).

### 2. GDPR souhlasy nad rámec

Samostatný export jen pro souhlasy, které organizátor přidal navíc k základnímu GDPR (marketingový souhlas, souhlas s fotografováním, souhlas s předáním dat partnerovi apod.). Obsahuje **všechny účastníky události** — i ty, kteří žádný souhlas nad rámec neudělili. Z jednoho souboru tak doložíte udělení souhlasu i to, že ho konkrétní osoba neudělila.

Export stáhnete v sekci **Registrační formulář** na záložce **Exporty** (spolu s odpověďmi z formuláře — viz [Nastavení registračního formuláře](../02_nastaveni-eventu-a-registrace/05_nastaveni-registracniho-formulare.md)) nebo v sekci **Statistiky**.

**Typické použití:**
- Audit — dokázat, kdo a kdy co odsouhlasil (a kdo ne)
- Podklad při žádosti účastníka o výmaz nebo přehled dat

### 3. Export skenování (check-in)

Jedna řádka za každé skenování QR kódu v servisní aplikaci nebo Prezenci.

**Typické použití:**
- Vyhodnocení příchodů v čase (kolik lidí přišlo v kterou hodinu)
- Kontrola, zda někdo prošel několikrát (duplicitní skeny)
- Vazba check-inu na konkrétní události skenování (*Příchod*, *Kontrola jednorázově* pro voucher atd.)

Pro pochopení typů míst viz [Jak funguje check-in a skenování QR kódů](../05_den-akce-a-provoz/01_jak-funguje-check-in-a-skenovani-qr-kodu.md).

### 4. Objednávky (Excel)

Kompletní seznam všech objednávek pro placenou událost — kdo, kolik, čím zaplatil, jestli je zaplaceno.

**Typické použití:**
- Podklad pro účetní (alternativa k jednotlivým fakturám)
- Kontrola, které objednávky čekají na úhradu

Detail objednávky (jedna objednávka) je popsaný v článku [Správa objednávek a faktur](../02_nastaveni-eventu-a-registrace/11_sprava-objednavek-a-faktur.md). Export je hromadný pohled.

### 5. Objednávky po vstupenkách (Excel)

Stejná data rozpadlá **po jednotlivých vstupenkách** — řádek za kus, ne za objednávku. Firemní nákup 50 vstupenek je tu 50 řádků s tím, komu byla která vstupenka přiřazena.

**Typické použití:**
- Párování vstupenek na konkrétní účastníky (kdo z firmy vlastně přijede)
- Kontrola, které kusy z hromadného nákupu zůstaly bez registrace

### 6. Export PDF faktur

Všechny faktury události najednou. Nahrazuje stahování dokladů po jednom z detailů objednávek.

**Typické použití:**
- Předání kompletní fakturace účetní v jednom balíku
- Archivace dokladů po uzavření události

### 7. Statistiky vstupenek

Agregovaná čísla — prodané, zaplacené, nezaplacené, zdarma, stornované, v rozpadu po měsících a podle typů vstupenek.

**Typické použití:**
- Finanční reporting události (kolik se vybralo, kolik čeká)
- Vyhodnocení prodejních vln (kdy se co prodalo)

Detailní vysvětlení statistik vstupenek je v [Nastavení placených vstupenek](../02_nastaveni-eventu-a-registrace/10_nastaveni-placenych-vstupenek.md).

### 8. Export registračních odkazů

Přehled všech individuálních a hromadných registračních odkazů události, jeden řádek za odkaz. Stáhnete ho na stránce **Placené vstupenky** pod tlačítkem **Exporty** vpravo nahoře. V nabídce *Exporty* na stránce Objednávky tahle položka není. U každého odkazu uvidíte typ, e-mail adresáta (jen u individuálního odkazu), název, nastavený limit, kolikrát už byl odkaz použit, stav a celou adresu odkazu. Stav je **Nepoužit**, **Použito částečně**, **Vyčerpán** nebo **Použit**.

**Typické použití:**
- Reporting pro partnera — kolik z jeho pozvánek zdarma se už využilo
- Kontrola, kterým hromadným odkazům došel limit a je potřeba ho navýšit
- Rozeslání odkazů vlastní cestou, bez kopírování adres z administrace po jedné

Export ukazuje jen počty. Kdo konkrétně se přes hromadný odkaz zaregistroval, v něm není, a chybí v něm i skupina, do které odkaz registrované zařazuje. Jak se odkazy zakládají, popisuje [Nastavení placených vstupenek](../02_nastaveni-eventu-a-registrace/10_nastaveni-placenych-vstupenek.md).

### 9. Odpovědi registračního formuláře (Excel / CSV)

Jedna řádka za každého registrovaného účastníka se všemi odpověďmi z formuláře. Zahrnuje kontaktní údaje i doplňující otázky.

**Dvě varianty:**
- **Excel** — pro lidi, kteří budou s daty pracovat ručně (filtrování, kontingenční tabulky)
- **CSV** — pro import do jiného systému (CRM, analytika, datový pipeline)

Kromě toho lze v UI přímo v detailu účastníka **upravit odpovědi** (například pokud někdo zadal překlep v adrese).

### 10. Mobilní aplikace — aktivita uživatelů

Export činností jednotlivých účastníků v aplikaci — jaké sekce aplikace otevřeli, kdy byli naposledy aktivní.

**Typické použití:**
- Vyhodnocení engagementu (interní firemní event vs. klientská konference mají rozdílné benchmarky)
- Podklad pro rozhodnutí, jestli do aplikace tlačit víc obsahu, nebo ji pro příští události úplně vypnout

### 11. Mobilní aplikace — seznam uživatelů s aplikací

Jen **kdo si aplikaci stáhl a přihlásil se** k této konkrétní události. Menší podmnožina, ale důležitá.

**Typické použití:**
- Před událostí — komu poslat push notifikaci vs. komu poslat e-mail
- Po události — kdo aplikaci reálně použil (v kombinaci s aktivitou)

### Co v exportech NENÍ

- **Automatický export do hotelu** — chybí. Musíte si data ručně poskládat ze *Všech účastníků* a odpovědí formuláře. Detail v [Příprava dat pro ubytovatele](../05_den-akce-a-provoz/03_priprava-dat-pro-ubytovatele.md).
- **Reporting rozesílky e-mailové kampaně** — je v **detailu kampaně** (ne v centrálním exportu). Viz [Vytvoření a odeslání e-mailové kampaně](../04_komunikace-a-pozvanky/03_vytvoreni-a-odeslani-e-mailove-kampane.md).
- **Interpretační vrstva** — Happenee exporty jsou syrová data. Kdy je registrační křivka *zdravá*, kdy *se neděje dost* — to si organizátor vyhodnotí sám nebo s pomocí customer success.

## Na co si dát pozor

### Stáhnete export a pracujete s ním měsíce starým

Exporty jsou snapshot k okamžiku stažení. Pokud řešíte aktuální stav, stáhněte znovu. Ukládejte si do názvu datum (*ucastnici_2026-04-19.xlsx*) — jinak po dvou staženích nevíte, který je nejnovější.

### Posíláte kolegovi celý export účastníků, ať si tam najde, co potřebuje

*Všichni účastníci* obsahují osobní údaje všech registrovaných — kolega, který řeší jen catering, je nepotřebuje. Vyberte cílenější export (například *Export skenování*, když jde o reálnou účast), nebo mu přes **Reporty účastníků** připravte soubor jen s potřebnými sloupci a vyfiltrovanými účastníky. Živý pohled na data místo souboru sdílet nejde: statistiky ani sekce *Registrace* nemají odkaz pro někoho mimo administraci.

### Faktury se stahují po jedné z detailů objednávek

V **Objednávkách** je pod tlačítkem *Exporty* položka **Export PDF faktur**, která stáhne všechny doklady najednou. Po jedné stahujte fakturu jen tehdy, když potřebujete jeden konkrétní doklad, třeba po opravě fakturačních údajů.

### Předpokládáte, že export skenování obsahuje stav *Odbaven / Nedostavil se*

Export skenování má **řádky za každý sken**, ne za každého účastníka. Kdo přišel vícekrát (například *Příchod* + *Kontrola jednorázově*), bude v exportu vícekrát. Pro jednoduchý seznam *kdo dorazil* použijte export účastníků s filtrem stavu *Odbaven*.

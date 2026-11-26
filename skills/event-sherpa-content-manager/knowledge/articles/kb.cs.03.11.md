<!-- source: kb.cs.03.11 -->

---
title: "Jak fungují registrační bloky, místa a štítky"
description: "Tři mechanismy pro organizaci většího programu: registrační bloky, místa (sály) a štítky (kategorie)."
modules: ["program_a_sessions", "ucastnici_skupiny_a_viditelnost"]
last_updated: "2026-09-16"
version: 8
---

> [!info] Krátce
> **Registrační bloky** sdružují sessions s registrací (typy Workshop a Časový slot) do skupin a určují, **kolik sessions z bloku si účastník může zapsat**. **Místa** označují fyzické prostory (sály, stage, stánky), **štítky** tematické kategorie (AI, Marketing, Leadership). Všechny tři mechanizmy pomáhají **organizovat větší program** a **filtrovat obsah** v aplikaci i na microsite.

## Jak začít

- **Bloky** použijte, když chcete omezit výběr — *účastník si zapíše 1 z N workshopů* nebo *2 z 5 sessions*.
- **Místa** použijte u programu s více sály nebo stage. Každé místo má svou barvu a slouží jako filtr.
- **Štítky** použijte pro tematické rozlišení — tracks, úrovně obtížnosti, témata.
- Bloky, místa a štítky se vytvářejí **v záložkách programu** (Bloky, Místa, Štítky).

## Detail

### Registrační bloky

Blok sdružuje sessions typu **Workshop** nebo **Časový slot** a omezuje, kolik z nich si účastník může zapsat.

**Vytvoření bloku:**

1. Přejděte na záložku **Bloky** v programu.
2. Klikněte na **+ Nový blok**.
3. Zadejte **Název bloku** (například *Dopolední workshopy*, *Odpolední slot*).
4. Na záložce **Nastavení** nastavte **Maximální počet sessions z bloku na účastníka** (výchozí: 1).
5. Přejděte na záložku **Sessions** — do pole **Hledejte sessions** vyhledejte sessions a přidejte je do bloku kliknutím.
6. Uložte.

**Typický use case:** 3 paralelní workshopy ráno. Účastník si zapíše jen jeden.

- Workshop A, B, C — každý jako samostatná session.
- Blok *Dopolední workshopy* obsahuje všechny tři.
- Maximální počet = 1.
- Účastník si v aplikaci vybere jeden; po výběru jsou ostatní pro něj zablokované.

**Kapacita sessions vs blok.** Individuální kapacita workshopu (například 20 míst) zůstává zachována. Blok jen omezuje výběr účastníka; nezasahuje do kapacity.

**Jedna session = jeden blok.** Session může být přiřazena pouze do **jednoho** registračního bloku.

### Místa

Místo označuje konkrétní prostor (sál, stage, stánek, sektor). Přiřazuje se k sessions a slouží jako **filtr** v aplikaci a na microsite.

**Vytvoření místa:**

1. Přejděte na záložku **Místa**.
2. Klikněte na **+ Nové místo**.
3. Zadejte **Název místa** (například *Sál A*, *Main Stage*, *Workshop Room 1*).
4. Uložte.

**Přiřazení k session:** v panelu úprav session na záložce **Informace** vyberte **Místo**.

**Skrytí v aplikaci:** u konkrétního místa přepněte toggle **Dostupnost aplikace** do polohy vypnuto. Místo se přestane zobrazovat jako filtr v aplikaci (ale sessions u něj zůstanou — místo se jen skryje jako filtrační atribut).

**Kolik míst.** Počet závisí na struktuře události. Pro jednoduchý program v jednom sále místa nevytvářejte — není co filtrovat. Pro vícedimenzionální konferenci (3 sály × 3 dny) vytvořte místo pro každý sál.

### Štítky

Štítek je tematická značka přiřazená k session. Na rozdíl od místa nemá fyzický rozměr — je koncepční (*AI*, *Strategy*, *Hands-on*).

**Vytvoření štítku:**

1. Přejděte na záložku **Štítky**.
2. Klikněte na **+ Nový štítek**.
3. Zadejte **Název štítku** a **Barvu** (ze seznamu nebo hex kód).
4. Uložte.

**Přiřazení k session:** v panelu úprav session na záložce **Informace** v sekci **Štítky** přiřaďte pomocí pole **Přiřadit štítky**. Session může mít **víc štítků**.

**Barvy štítků.** Štítky se v aplikaci zobrazují s barvou. Zvolte barvy kontrastní na světlém i tmavém pozadí aplikace.

### Filtry v aplikaci a na microsite

V programu se automaticky zobrazují filtry **Typ**, **Místo**, **Štítky**. Účastník může kombinovat:

- *Typ: Workshop + Místo: Sál A* → všechny workshopy v sále A.
- *Štítek: AI + Štítek: Hands-on* → sessions s oběma štítky (průnik).

**Které filtry a v jakém pořadí** — na záložce **Nastavení** programu je tabulka filtrů se sloupci **Název**, **Typ filtru** a **Zobrazit filtr**. Každý filtr (Typ, Místo, Štítky) lze:

- Zapnout / vypnout přepínačem ve sloupci **Zobrazit filtr**.
- Změnit pořadí přetažením za úchyt vlevo — tedy pořadí filtrů za sebou.
- Přejmenovat tlačítkem **Název** — filtr se pak účastníkům zobrazí pod vlastním názvem (například *Témata* místo *Štítky*). Název je jazyková položka — vyplňuje se zvlášť pro každý jazyk události. Jazyk, ve kterém ho necháte prázdný, převezme název z primárního jazyka, takže anglický účastník může u filtru vidět český název. Přepněte proto vlajku jazyka a projděte filtry ve všech jazycích, které událost podporuje.

Zapnutí, vypnutí i nové pořadí filtru se uloží hned, tabulka nemá tlačítko pro uložení. Jen nový název potvrzujete tlačítkem **Uložit** v bočním panelu.

Skrytá místa se jako filtr nezobrazují.

Na podstránce s celým programem stojí filtry na širokém displeji v pravém sloupci vedle výpisu sessions. Na mobilu se schovají za tlačítko **Filtry** vedle vyhledávacího pole a otevřou se v draweru, aby výpis začínal hned pod vyhledáváním a první bod programu nebyl až pod celým filtračním panelem.

Přepínač **Zobrazit filtr** neřídí jen filtrační panel v programu. Rozhoduje také o **quick filtrech na hlavní stránce microsite** — o řadě tlačítek, kterou u programu zapínáte v *Microsite události* dialogem *Zobrazení programu*. Nabídka v tom dialogu vychází přímo z téhle tabulky — jsou v ní jen filtry se zapnutým *Zobrazit filtr*, pod názvy, které jim tady dáte, a ve stejném pořadí. Když filtr vypnete, zmizí z nabídky a uložená volba quick filtrů se zároveň vrátí na *Nezobrazovat*. Když tedy quick filtry nastavíte podle *Místa*, nechte filtr *Místo* tady zapnutý. Detail v článku [Jak funguje microsite události](01_jak-funguje-microsite-udalosti.md).

**Pořadí hodnot uvnitř filtru** se řídí jinde — ručním řazením v příslušné tabulce programu. Přetažením řádků (za úchyt vlevo) v záložce **Místa** určíte pořadí míst ve filtru Místo, v záložce **Štítky** pořadí štítků a v záložce **Typy** pořadí typů. Toto pořadí se promítne shodně do microsite i do mobilní a webové účastnické aplikace.

### Bloky v kombinaci s typy

**Sessions stejného typu v jednom bloku:** obvyklé (tři workshopy v bloku).

**Sessions různých typů v jednom bloku:** technicky možné, ale matoucí pro účastníka. Doporučení: držte v bloku sessions stejného typu.

### Pořadí sessions

Pořadí sessions v programu je řízeno především **časem**. Když dvě sessions začínají ve stejný čas, seřadí se podle **pořadí typů** — typ výš v záložce **Typy** se v programu zobrazí dřív (viz [Jak fungují typy sessions](07_jak-funguji-typy-sessions.md)). Místa a štítky ovlivňují jen filtrování, ne řazení sessions.

## Na co si dát pozor

### Blok s jedním workshopem — organizátor si myslí, že to sjednotí kapacitu

Blok s jednou session nic nepřidává. Kapacitu řídíte přes *Omezit počet registrací* na session, ne přes blok.

### Session přiřazena do dvou bloků. Systém to nedovolí

Session může být **pouze v jednom bloku**. Pokud potřebujete, aby session byla součástí víc výběrových schémat, duplikujte ji jako samostatnou session a každou dejte do jiného bloku (organizačně ale ztrácíte přehled).

### Místo přiřazeno, ale skryté pomocí *Dostupnost aplikace*. Účastník ho nevidí jako filtr, ale sessions tam mají místo uvedené

Skryté místo se jako **filtr** nezobrazí, ale samotné přiřazení k session zůstává. Na detailu session účastník místo vidí. Pokud chcete místo zcela odebrat, smažte ho.

### Štítek s barvou, která je nečitelná na tmavém módu aplikace

Volte barvy dostatečně kontrastní. Happenee aplikace podporuje světlý i tmavý režim — zkontrolujte štítek v obou.

### Blok *Dopolední workshopy* s *Maximální počet = 1*, ale organizátor zapomněl nastavit i kapacitu jednotlivých workshopů. Workshop je naplněn nad rozumnou kapacitu

Blok omezuje **výběr účastníka**, ne kapacitu session. Kapacitu každé session nastavte individuálně na úrovni sessions nebo typu.

### Po vypnutí filtru zmizely i quick filtry na hlavní stránce

Je to záměr. Vypnutý filtr zmizí z programu i z hlavní stránky microsite a uložená volba v dialogu *Zobrazení programu* se zároveň vrátí na *Nezobrazovat*, aby nikde nezůstal výběr, který se nemá jak vykreslit. Pokud quick filtry na hlavní stránce chcete, zapněte filtr zpátky a v *Microsite události* u příslušné záložky typu **Sessions** volbu vyberte znovu.

### Filtry vypnuté nebo ve špatném pořadí, účastník se v programu ztrácí

Na záložce **Nastavení** programu přehledově projděte filtry. Pro konferenci s paralelními tracks zapněte Typ, Místo, Štítky. Pro jednoduchý program stačí Typ.

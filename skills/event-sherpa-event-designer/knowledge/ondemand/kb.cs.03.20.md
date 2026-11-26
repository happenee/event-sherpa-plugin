<!-- source: kb.cs.03.20 -->

---
title: "Hromadný import sessions"
description: "Nahrání sessions do Programu z Excelu přes 5krokový průvodce — šablona nebo vlastní soubor, mapování sloupců, validace a náhled před zápisem."
modules: ["program_a_sessions"]
last_updated: "2026-08-07"
version: 9
---

> [!info] Krátce
> Hromadný import umožňuje vytvořit více sessions najednou z Excelu místo ručního zakládání po jedné. Hodí se, když máte program připravený v tabulce — typicky 10 a více sessions. Průvodce má pět kroků (nahrání souboru, mapování sloupců, vazby, náhled, výsledek) a před zápisem zkontroluje validitu dat. Import se vždy týká té instance Programu, ve které ho spustíte.

## Jak začít

- Zvažte, jestli je import ta správná cesta. Vyplatí se od zhruba deseti sessions výš. Potřebujete-li jen pár sessions, které se od sebe liší v detailech, je rychlejší založit jednu a zbytek **zkopírovat** — viz [Správa sessions](21_sprava-sessions.md).
- Rozhodněte, do **které instance Programu** importujete. Pokud má událost víc Programů (například *Hlavní program* a *Workshopy*), záložka **Import** je samostatná pro každý z nich.
- Připravte si data v Excelu. Můžete stáhnout **šablonu** přímo z administrace, nebo použít **vlastní soubor** — sloupce ručně namapujete v druhém kroku průvodce.
- **Typ je u session vždy povinný.** V souboru ho mít nemusíte — pokud sloupec Typ nevyplníte, v kroku *Vazby* přiřadíte typ všem importovaným sessions najednou. Mějte proto v Programu připravené **typy sessions** (a podle potřeby **bloky**, **místa** a **štítky**, na které se budete v souboru odkazovat).
- Řečníky a moderátory **přes tento import nezaložíte** — vytvořte je zvlášť (viz *Hromadný import řečníků*) a navažte je na sessions ve 3. kroku průvodce nebo později.

## Detail

### Kde Import najdete

V administraci přejděte na **Obsah** a otevřete **Program**, do kterého chcete importovat. V hlavičce sekce jsou záložky **Sessions**, **Typy**, **Bloky**, **Štítky**, **Místa**, **Moje agenda**, **Nastavení** a **Import**. Otevřete záložku **Import**.

Záložka **Import** je vázaná na konkrétní instanci Programu — sessions se naimportují do toho Programu, ve kterém právě jste.

### Šablona, nebo vlastní soubor

V prvním kroku průvodce máte dvě cesty:

- **Stáhnout šablonu** a vyplnit ji. Šablona je jeden list s hlavičkovým řádkem a jedním ukázkovým řádkem s fiktivními daty (ten před importem smažte — viz pozor níže).
- **Nahrát vlastní Excel** s vlastními názvy sloupců — klidně i dříve stažený **export sessions** z této nebo jiné události. Mapování na pole session nastavíte ručně ve druhém kroku, takže na názvech sloupců nezáleží.

V obou případech pak kliknete na **Nahrát a zpracovat** a průvodce přejde na mapování.

### Pole, která lze namapovat

Sloupce souboru se ve druhém kroku přiřazují na pole session. Povinná pole musíte namapovat, jinak řádek neprojde validací:

- **Název** *(povinné)* — Lokalizovaný (váže se na jazyk obsahu události).
- **Datum** *(povinné)* — Den konání session.
- **Začátek** *(povinné)* — Čas začátku.
- **Konec** *(povinné)* — Čas konce.
- **Popis** *(volitelné)* — Lokalizovaný, stejně jako Název.
- **Typ** *(volitelné)* — Hodnota odpovídá typu session (*Keynote*, *Workshop*, *Časový slot*…). Není povinný v souboru, ale typ je u session vždy povinný — viz krok *Vazby*.
- **Blok** *(volitelné)* — Registrační blok.
- **Místo** *(volitelné)* — Místo / stage session.
- **Štítky** *(volitelné)* — Více štítků oddělíte čárkou.
- **Pořadí** *(volitelné)* — Číslo určující řazení session.

Povinné jsou pouze **Název**, **Datum**, **Začátek** a **Konec**. Ostatní pole jsou volitelná. Sloupce, kterým necháte mapování prázdné (volba *přeskočit*), se ignorují.

**Výjimka — Typ.** V souboru povinný není, ale každá session typ mít musí. Pokud sloupec Typ nevyplníte (nebo ho nenamapujete), v kroku *Vazby* přiřadíte typ všem importovaným sessions najednou. Bez přiřazeného typu nelze import dokončit.

Název a Popis jsou lokalizované (vážou se na jazyk obsahu události). **Názvy sloupců ve stažené šabloně se mohou lišit od názvů polí výše a nemusí být vždy přesné** — na pole je mapujete ve druhém kroku, takže na konkrétním názvu sloupce nezáleží.

### Průvodce importem (5 kroků)

V horní části obrazovky je krokový indikátor: **Nahrát → Mapování → Vazby → Náhled → Výsledek**. Mezi kroky se lze vracet zpět.

**1. Nahrát.** Stáhněte šablonu (volitelně), nebo rovnou nahrajte svůj Excel přes výběr souboru. Klikněte na **Nahrát a zpracovat**.

**2. Mapování.** Průvodce načte hlavičky souboru a zobrazí je v tabulce *Sloupec v Excelu — Ukázkové hodnoty — Mapovat na pole*. U každého sloupce vyberte cílové pole (Název, Datum, Typ…). Sloupce nechané na *přeskočit* se ignorují. Mapování **se nikam neukládá** — při každém importu ho nastavujete znovu. Klikněte na **Ověřit a zobrazit náhled**.

**3. Vazby.** Tady přiřadíte importované sessions k dalšímu obsahu — typicky řečníky a moderátory. **Pokud soubor neobsahoval typ session, právě tady přiřadíte typ všem importovaným sessions** (typ je u session vždy povinný, takže bez něj import nedokončíte). Krok se zobrazí, když je co doplnit.

**4. Náhled.** Průvodce zobrazí souhrn: **Celkem / Validní / Varování / Chyby / Duplicity**. Pod souhrnem je tabulka s každým řádkem a jeho stavem (validní řádek je označený zeleně, duplicitní ikonou duplicity s textem *Duplicate session already exists.*). **Žádná data se ještě nezapsala** — je to poslední možnost se vrátit a opravit soubor. Pokud souhrn vyhovuje, klikněte na **Importovat**.

**5. Výsledek.** Po dokončení importu uvidíte výsledná čísla a můžete se vrátit na seznam sessions. Jde o stejného průvodce jako u importu řečníků.

### Jak průvodce pozná duplicitu

Průvodce porovnává řádky souboru s **už existujícími sessions** v daném Programu (a zároveň hlídá opakování v rámci souboru). Co vyhodnotí jako duplicitu, **nezaimportuje** — řádek se započítá do **Duplicit** a přeskočí se. Z opakujících se řádků se zaimportuje **první výskyt**.

Z toho plyne, že import **nepřepisuje existující sessions**. Pokud potřebujete hromadně změnit sessions, které už v Programu jsou, import na to není — použijte [hromadné akce v záložce Sessions](21_sprava-sessions.md).

### Co import neumí

- **Zakládat řečníky a moderátory.** Tento průvodce vytváří jen sessions. Řečníky importujte zvlášť (*Hromadný import řečníků*) a navažte je v kroku *Vazby* nebo později z panelu session či řečníka.
- **Přepisovat existující sessions.** Duplicitní řádky se přeskakují. Na hromadnou úpravu existujících sessions slouží [hromadné akce v záložce Sessions](21_sprava-sessions.md).
- **Nastavit stav session.** Šablona ani import nemají sloupec pro stav — stav (Publikováno / Skryto) nelze importem nastavit. Po importu ho zkontrolujte v seznamu sessions (viz pozor níže).

## Na co si dát pozor

### Šablona obsahuje ukázkový řádek — pokud ho nesmažete, naimportuje se jako reálná session

Stažená šablona má první datový řádek vyplněný fiktivní ukázkovou session (*Future of Event Experience*). Ve fázi *Náhled* se objeví jako validní a po importu vám v programu zůstane smyšlená session. Před vyplněním vlastních dat ukázkový řádek smažte.

### Bez Názvu, Data, Začátku a Konce řádek neprojde

Tato čtyři pole jsou povinná. Pokud je ve zdroji nemáte (nebo je nenamapujete), řádek se v *Náhledu* označí jako chyba a nezaimportuje se. Datum a čas držte ve formátu, jaký má šablona (ve vzorech *DD.MM.RRRR* a *HH:MM*).

### Stav session se přes import nenastavuje — po importu ho zkontrolujte

V *Náhledu* se u řádků zobrazuje stav (například *published* / *hidden*), ale **stav nelze importem určit** — šablona sloupec pro stav nemá a mezi cílovými poli mapování stav není. Po importu proto v seznamu sessions zkontrolujte viditelnost a sessions, které mají být veřejné, případně publikujte.

### Opakovaný import stejného souboru nevytvoří nic — všechny řádky spadnou do Duplicit

Protože se importované řádky porovnávají s už existujícími sessions, druhý import téhož souboru skončí tak, že jsou všechny řádky vyhodnoceny jako duplicitní a přeskočeny (v *Náhledu* uvidíte *Validní 0*, *Duplicity = počet řádků*). Před kliknutím na **Importovat** proto vždy zkontrolujte počet **Duplicit**: vyšší číslo, než čekáte, znamená, že část těch sessions už v Programu je. Import je znovu nevytvoří ani nepřepíše — pokud jste chtěli existující sessions upravit, použijte [hromadné akce v záložce Sessions](21_sprava-sessions.md).

### Řečníci a moderátoři se v kroku Mapování nepřiřazují

Sloupce typu *Speakers* nebo *Moderators* nejsou mezi cílovými poli mapování — nechte je přeskočit. Vazby řečníků na sessions řešte v kroku *Vazby*, případně později z panelu jednotlivých sessions. Pokud na to zapomenete, sessions se naimportují bez řečníků a budete je dohledávat ručně.

### Prázdný sloupec Typ není chyba — ale typ musíte přiřadit v kroku *Vazby*

Typ není v souboru povinný, takže prázdný sloupec Typ řádek neoznačí jako chybu. Neznamená to ale, že se session naimportuje bez typu — každá session typ mít musí. V kroku *Vazby* proto všem importovaným sessions typ přiřadíte; pokud krok *Vazby* přeskočíte bez přiřazení, import nedokončíte. Mějte cílový typ v Programu připravený předem.

### Hodnoty Typ, Blok, Místo a Štítky musí dávat smysl vůči Programu

Typ je u session povinný a hodnoty ve sloupcích Typ, Blok, Místo a Štítky se vážou na to, co v Programu máte připravené. Než spustíte import, projděte v *Náhledu*, že se tyto sloupce namapovaly správně a hodnoty odpovídají — špatně zadaný typ je nejčastější příčina, proč session po importu „není tam, kde má být“.

### Mapování sloupců musíte nastavit při každém importu znovu

Průvodce si namapování nepamatuje — po každém nahrání souboru ho zadáváte od začátku. Pokud importujete opakovaně (program se průběžně doplňuje), držte ve vlastním souboru **stejné názvy a pořadí sloupců jako ve stažené šabloně**. Mapování pak zabere pár vteřin a nepřehlédnete žádné pole.

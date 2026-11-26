# Příprava dat pro ubytovatele

> Jak ručně sestavit data pro hotel z několika exportů, když Happenee zatím nenabízí jeden sloučený export.

- Článek v Help Centru: https://help.happenee.com/cs/articles/49-priprava-dat-pro-ubytovatele
- English version: https://help.happenee.com/en/articles/49-preparing-data-for-accommodation-providers
- Kolekce: Den události a provoz na místě
- Aktualizováno: 2026-04-27

---

> [!info] Krátce
> Pokud u vícedenní události zajišťujete ubytování, **hotel typicky potřebuje víc informací, než Happenee exportuje jedním kliknutím**. Obsazení pokojů (kdo s kým) máte v Administraci pokojů. Kontaktní údaje, data příjezdu / odjezdu, preference a speciální požadavky jsou v registračním formuláři. Pro hotel si data **slepujete ručně** z několika exportů — typicky přes e-mail jako klíč ve spreadsheetu. Automatický sloučený export pro ubytovatele Happenee zatím nenabízí.

## Jak začít

- **Ujasněte si s hotelem**, co přesně na seznamu potřebuje — jméno, e-mail, telefon, datum check-in / check-out, typ pokoje, spolubydlící, dietní omezení, speciální požadavky.
- V **registračním formuláři** zajistěte, že všechny tyto údaje sbíráte — buď jako standardní kontaktní pole (jméno, e-mail), nebo jako **doplňující otázky** (datum příjezdu, strava, poznámka).
- Pro **výběr spolubydlícího** použijte otázku typu 7 a nastavte **Administraci pokojů** (viz článek *Správa ubytování a výběru spolubydlícího*).
- Finální tabulku pro hotel připravujte **7 a více dní před událostí** — pozdní změny v registraci už se do seznamu špatně dostávají a vznikají nesrovnalosti.
- Určete **jednoho vlastníka** v týmu, který tabulku drží a aktualizuje. Nikdy do ní neklikejte paralelně ve dvou.

## Detail

### Co Happenee exportuje standardně

Pokud používáte ubytování přes otázku typu 7, máte v administraci události tři zdroje dat:

- **Administrace pokojů** (v detailu otázky typu 7) — seznam vygenerovaných pokojů a kdo v nich je. Export obsahuje **jméno, e-mail, název pokoje, typ pokoje, spolubydlící**. Nic víc.
- **Registrační formulář / odpovědi** — export odpovědí všech účastníků na všechny doplňující otázky. Sem patří datum příjezdu, stravovací omezení, požadavky typu „pozdní check-in“, „dětská postýlka“.
- **Správa kontaktů a skupin** — kontaktní údaje (telefon, firma, vlastní pole kontaktů). Základ pro hotel, pokud vyžaduje telefonní číslo.

### Jak data slepovat

Protože automatizovaný export pro ubytovatele Happenee **zatím nenabízí**, data si skládáte ručně. Typický postup:

1. **Vyexportujte administraci pokojů** — máte tabulku *jméno + e-mail + pokoj + typ + spolubydlící*.
2. **Vyexportujte odpovědi z registračního formuláře** — tabulka se všemi doplňujícími otázkami.
3. **Vyexportujte kontakty ze správy kontaktů** — telefon, firma, další pole.
4. **Sloučte v Excelu** přes **e-mail jako klíč** (VLOOKUP / INDEX-MATCH / Power Query). E-mail je nejspolehlivější identifikátor — jméno se může zapsat s diakritikou jinak, e-mail je unikátní.
5. **Pročistěte** — zkontrolujte prázdná pole, duplicitní registrace, účastníky, kteří se odhlásili (viz legenda barev v administraci pokojů — fialově podbarvený = *uživatel se odhlásil z události*).
6. **Formátujte podle požadavku hotelu** — ne každý hotel přijímá Excel; některé vyžadují CSV, jiné PDF se seznamem po jménech.

### Pozor na export administrace pokojů

Export z Administrace pokojů je záměrně **minimalistický** — obsahuje jen identitu účastníka a pokoj. **Neobsahuje** datum příjezdu, stravování, telefon, speciální požadavky. Tyto údaje jsou v **registračním formuláři** (doplňující otázky) nebo v **kontaktních polích**. Pokud je potřebujete, musíte si je přidat ručně.

### Typické údaje, které hotel vyžaduje navíc

- **Telefonní číslo** — vyžadováno téměř vždy (hotel volá při problému). Nastavte ho jako pole v registračním formuláři nebo ve vlastních polích kontaktů.
- **Datum příjezdu a odjezdu** — pokud účastníci přijíždějí v různé dny. Typicky jako doplňující otázka typu *datum*.
- **Preference pokoje** — například jednolůžkový pokoj, konkrétní patro nebo nekuřácký pokoj. Doplňující otázka typu *jedna odpověď z více* nebo *vlastní text*.
- **Stravovací omezení** — doplňující otázka s několika variantami (vegetariánská, veganská, bezlepková, alergie).
- **Čas příjezdu** — pokud hotel řeší kapacitu recepce. Otázka typu *čas*.

Pokud pro tyto údaje **nemáte odpovídající otázky ve formuláři**, hotel je nedostane — a vy se na ně nedoptáte (událost je za týden, účastníci se už neregistrují). Připravte formulář **před otevřením registrace**, nikoliv po.

### Doporučený timing

- **Před otevřením registrace**: domluvte s hotelem, co potřebuje. Nastavte formulář tak, aby všechny údaje sbíral.
- **Průběžně během registrace**: exportujte kontrolní tabulku (týdně). Hlídejte, jestli se registrující vejdou do vygenerovaných pokojů (viz článek *Správa ubytování a výběru spolubydlícího*).
- **7–10 dní před událostí**: finální tabulku pro hotel. Pošlete a vyjednejte potvrzení. Změny po tomto termínu řešte individuálně.
- **2–3 dny před událostí**: poslat hotelu **aktualizaci** (odhlášení, pozdní přihlášení). Ideálně stejný formát.

### Doporučení: jeden vlastník

I když tým obsluhy události je víc lidí, **finální seznam pro hotel má mít jednoho vlastníka**. Dvě paralelní verze v Excelu jsou zdroj chyb. Vlastník má přístup k administraci události, vidí změny v registraci a je v kontaktu s hotelem.

## Na co si dát pozor

### Organizátor pošle hotelu rovnou export z Administrace pokojů a diví se, že hotel volá a ptá se na telefony a diety

Export z Administrace pokojů obsahuje jen jméno + e-mail + pokoj. Kontakty a speciální požadavky musíte doplnit z exportu registračního formuláře a kontaktů.

### Registrační formulář neobsahuje pole, které hotel vyžaduje (typicky telefon nebo datum příjezdu)

Formulář připravte **před otevřením registrace**. Dodatečné doptávání jednotlivě e-mailem je pracné a nikdy se nenavrátí 100 % odpovědí.

### Tabulku pro hotel drží dva lidé paralelně, každý udělá malé úpravy a výsledek se rozchází

Jeden vlastník. Ostatní v týmu jen dodávají podklady — nikdy needitují přímo.

### Tabulka poslána hotelu dopoledne, odpoledne se odhlásí 5 účastníků. Hotel účtuje všech 5 pokojů

Domluvte si s hotelem **cutoff datum** pro finální seznam (storno podmínky). Po cutoffu už změny účtuje. Předtím je flexibilita vaše.

### Hotel nepřijímá Excel, očekává CSV nebo PDF

Ověřte formát dopředu. Excel se snadno převede do CSV (Soubor → Uložit jako). PDF vyexportujete přes tisk do PDF s pevným rozložením.

### Organizátor očekává jeden hotový export „pro hotel“ jako tlačítko v Happenee

Automatizovaný export pro ubytovatele **Happenee zatím nenabízí**. Pracujete ručně s kombinací exportů. Pokud řešíte velkou událost s ubytováním pravidelně, investujte do šablony v Excelu, kterou znovu použijete.

## Související články

- [Správa ubytování a výběru spolubydlícího](https://help.happenee.com/cs/articles/16-sprava-ubytovani-a-vyberu-spolubydliciho)
- [Nastavení registračního formuláře](https://help.happenee.com/cs/articles/13-nastaveni-registracniho-formulare)
- [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace)
- [Jak fungují podmíněné otázky v registračním formuláři](https://help.happenee.com/cs/articles/14-jak-funguji-podminene-otazky-v-registracnim-formulari)
- [Práce s objednávkami a exporty](https://help.happenee.com/cs/articles/52-prace-s-objednavkami-a-exporty)

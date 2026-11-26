# Správa ubytování a výběru spolubydlícího

> Jak nechat účastníky vybrat si v registračním formuláři spolubydlícího a připravit data pro hotel.

- Článek v Help Centru: https://help.happenee.com/cs/articles/16-sprava-ubytovani-a-vyberu-spolubydliciho
- English version: https://help.happenee.com/en/articles/16-managing-accommodation-and-roommate-selection
- Kolekce: Nastavení eventu a registrace
- Aktualizováno: 2026-04-27

---

> [!info] Krátce
> Pokud u události zajišťujete **ubytování**, můžete účastníkům umožnit vybrat si spolubydlícího přímo v registračním formuláři. Happenee vede seznam pokojů (jednolůžkové a dvoulůžkové), hlídá matching a umí exportovat výsledek pro hotel. Funkce je navázaná na otázku typu 7 v doplňujících otázkách formuláře.

## Jak začít

- Rozhodněte, jak účastníci spolubydlícího vyberou — výběr ze seznamu přihlášených, žádná preference (systém rozdělí), nebo jen jednolůžkové pokoje (každý má svůj).
- Před otevřením registrace si ověřte, že všichni, kdo se budou moct vybírat navzájem, jsou přiřazeni k události v Kontaktech a skupinách — výběr probíhá ze seznamu přiřazených, ne až po registraci.
- Spočítejte si potřebný počet pokojů (jednolůžkových + dvoulůžkových) a vygenerujte je předem.
- Na konci máte export do hotelu — ujistěte se, že hotel akceptuje formát, který Happenee exportuje.

## Detail

### Otázka typu 7 — Výběr ubytování a spolubydlícího

V registračním formuláři na záložce **Doplňující otázky** přidejte **+ Nová otázka** a v dropdownu **Vyberte typ otázky** vyberte typ 7 — *Výběr ubytování, výběr spolubydlícího ze seznamu*. V panelu se otevřou dvě sekce:

- **Varianty ubytování** — seznam voleb, které uvidí účastník (*Dvoulůžkový pokoj*, *Jednolůžkový pokoj*, *Nechci ubytování*). U každé volby lze přidat podmíněnou otázku (například *Jaké je vaše preferované patro?*).
- **Nemám preferenci spolubydlícího** — volba, kterou účastník zaškrtne, pokud je mu jedno, s kým bude. Systém je přiřazuje sám.

### Detail nastavení — Administrace pokojů

V detailu otázky otevřete **Detail nastavení** → **Administrace pokojů**. Zde se vytvářejí a spravují pokoje.

**Vytvoření pokojů.**

1. V sekci **Administrace pokojů** zadejte **Název pokoje** (může být libovolný — třeba číslo patra, typ kategorie).
2. Vyberte typ — **Jednolůžko** nebo **Dvoulůžko**.
3. Zadejte **Počet pokojů k vygenerování**.
4. Klikněte na **Přidat**. Systém vytvoří zadaný počet pokojů.

> Jednolůžkový pokoj lze přiřadit pouze v administraci. Účastník si ho nemůže vybrat v registračním formuláři.

Opakujte pro každou kategorii pokojů, kterou potřebujete. Hlídejte si celkový počet — pokud vygenerujete málo pokojů, některé účastníky nebudete moct ubytovat, a budete muset dopočítat.

### Jak probíhá výběr spolubydlícího

1. Účastník A prochází registračním formulářem a u otázky typu 7 vybírá **Dvoulůžkový pokoj**.
2. Pod volbou se zobrazí pole *Vyberte spolubydlícího* se seznamem **všech účastníků přiřazených k události** (ne těch, kteří jsou již zaregistrovaní — matching dělá organizátor dopředu).
3. Účastník A vybere účastníka B a dokončí registraci.
4. Účastník B prochází svou registrací a vidí, že si ho účastník A vybral. Má dvě možnosti:
   - **Potvrdit** volbu — pár je spárovaný.
   - **Vybrat někoho jiného** — rozváže původní volbu a vytvoří novou.

### Správa matchingu v administraci

V sekci **Administrace pokojů** vidíte:

- Seznam vygenerovaných pokojů a kdo v nich je ubytován.
- Filtr zobrazení — **účastníci se spolubydlícím**, **bez preference**, **všichni zaregistrovaní**, **všichni účastníci**.
- Legendu barev u účastníků:
  - **Žlutě podbarvený** — nezaregistrovaný.
  - **Červeně podbarvený** — uživatel nechce ubytování.
  - **Lososově podbarvený** — uživatel se nezúčastní.
  - **Fialově podbarvený** — uživatel se odhlásil z události.

Administrátor může ručně přiřadit účastníka do konkrétního pokoje, posunout mezi pokoji, nebo přiřadit jednolůžkový pokoj.

### Export pro hotel

Z administrace pokojů lze generovat **export** se seznamem obsazení pokojů — jméno, e-mail, pokoj, typ pokoje, spolubydlící. Formát je Excel. Před předáním hotelu ověřte, že jejich systém akceptuje tento formát, nebo data upravte.

### Vícejazyčnost

Varianty ubytování a texty otázky upravujte ve všech jazycích, které má událost přidané — přepínačem vlaječek v pravém horním rohu. Název pokoje ani legenda v administraci se účastníkům nezobrazuje (je jen pro organizátora), takže je nemusíte překládat.

## Na co si dát pozor

### Účastníci si nemohou vybrat spolubydlícího, protože v seznamu nejsou. Organizátor neví proč

Výběr probíhá ze seznamu **přiřazených k události**, ne zaregistrovaných. Pokud chcete, aby si účastníci vybírali navzájem, přiřaďte je všechny k události předem — hromadně přes skupinu nebo import.

### Vygenerováno málo pokojů. Část účastníků projde formulářem, ale ubytování jim nelze přidělit

Spočítejte si potřebný počet pokojů před spuštěním registrace. Dejte si rezervu — optimálně 10 %. Pokoje doplníte kdykoli přes **Administrace pokojů → + Přidat**.

### Účastník A vybere B, ale B prošel registrací dřív a nevidí A v seznamu

Funkce výběru spolubydlícího funguje obousměrně, ale aby ji oba využili, musí oba projít registračním formulářem po tom, co byli do události přiřazeni. Pokud B dokončí registraci první a A ho pak vybere, A uvidí B v seznamu a B musí souhlas doplnit v účastnickém profilu (ne v původním formuláři).

### Změna typu pokoje po registraci (z dvoulůžkového na jednolůžkový). Účastník byl spárovaný a nyní je sám

V administraci ručně přerovnejte účastníky. Pokud má událost hodně změn, vyčkejte s přiřazením pokojů až do uzavření registrace — vyhnete se opakovanému rovnání.

### Export odevzdaný hotelu neobsahuje všechny údaje, které hotel potřebuje (například informaci o stravování nebo kontakty)

Export ubytování neobsahuje všechny informace z registračního formuláře. Pro dodatečné údaje použijte export celého registračního formuláře a data spojte ručně v Excelu.

## Související články

- [Nastavení registračního formuláře](https://help.happenee.com/cs/articles/13-nastaveni-registracniho-formulare)
- [Jak fungují podmíněné otázky v registračním formuláři](https://help.happenee.com/cs/articles/14-jak-funguji-podminene-otazky-v-registracnim-formulari)
- [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti)
- [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace)
- [Příprava dat pro ubytovatele](https://help.happenee.com/cs/articles/49-priprava-dat-pro-ubytovatele)

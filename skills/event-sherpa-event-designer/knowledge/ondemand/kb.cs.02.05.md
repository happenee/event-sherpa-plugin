<!-- source: kb.cs.02.05 -->

---
title: "Nastavení registračního formuláře"
description: "Jak postavit registrační formulář pro kontaktní údaje a doplňující otázky specifické pro danou událost."
modules: ["registrace"]
last_updated: "2026-09-02"
version: 4
---

> [!info] Krátce
> Registrační formulář je nástroj, kterým od účastníků získáváte **kontaktní údaje** (sdílené napříč workspace) a **doplňující informace** specifické pro konkrétní událost. Formulář je součástí microsite a zobrazí se po zadání e-mailu nebo kliknutí na tlačítko **Pokračovat k registraci**. U placených vstupenek je přístupný až po úhradě (u varianty s doplněním informací).

## Jak začít

- Rozhodněte, **které kontaktní údaje budete potřebovat povinně** — e-mail je vždy povinný, ostatní si nastavujete.
- Vyjmenujte si, jaké doplňující otázky potřebujete — doprava, stravování, výběr workshopu, ubytování, preference.
- Pokud chcete některé otázky vidět jen některým skupinám účastníků, naplánujte skupiny dopředu.
- U vícejazyčných událostí si připravte znění otázek i odpovědí ve všech jazycích.
- Formulář upravujete v administraci události v levém menu pod **Registrační formulář**.

## Detail

### Záložky formuláře

Registrační formulář má dvě hlavní obsahové záložky:

- **Kontaktní údaje** — sdílené s celým workspace. Co účastník vyplní, se propíše do správy kontaktů a je k dispozici pro další události.
- **Doplňující otázky** — specifické pro konkrétní událost. Každá událost má vlastní sadu otázek.

Vedle nich má administrace formuláře záložky **Náhled formuláře** (otevře formulář, jak ho uvidí účastník), **Struktura otázek** (přehled, jak jsou podmíněné otázky navázané), **Exporty** (stažení odpovědí v Excelu nebo CSV a GDPR souhlasů nad rámec) a **Upravit odpovědi** (úpravy odpovědí konkrétních účastníků).

### Kontaktní údaje — nastavení povinnosti

Pole kontaktních údajů jsou přednastavená Happenee. K dispozici jsou **E-mail**, **Jméno**, **Příjmení**, **Telefon**, **Pracovní pozice**, **Společnost**, **IČO**, **Země**, **Twitter (X)** a **LinkedIn**. U každého pole volíte:

- **Povinné** — účastník musí pole vyplnit.
- **Nepovinné** — pole se zobrazí, ale vyplnění není nutné.
- **Skrýt** — pole se účastníkovi vůbec neukáže.

E-mail je vždy povinný — toto nastavení nelze přepnout.

Vedle standardních kontaktních polí je níže samostatná sekce **Vlastní pole kontaktů** se stejnou trojicí voleb. Ta si nadefinujete v **Nastavení workspace → Vlastní pole kontaktů** (jsou sdílená pro všechny události). Obvyklé využití: oslovení, interní ID zaměstnance, oddělení, cena za služební cestu.

> **Při zapnuté automatické registraci** platí kontaktní údaje jen pro **individuální a hromadné registrační odkazy** — tedy pro registrace bez nákupu vstupenky. Kdo prochází nákupem vstupenky, vyplňuje pole nastavená u konkrétní vstupenky, ne tady. Administrace na to upozorňuje přímo nad seznamem polí.

### Doplňující otázky

Na záložce **Doplňující otázky** přidáváte otázky specifické pro událost kliknutím na tlačítko **+ Nová otázka**. U každé otázky volíte (v dropdownu **Vyberte typ otázky**):

- **Otázka nebo název pole** (povinný).
- **Doplňující popis** (volitelný — krátký doplňující text pod otázkou).
- **Typ otázky** (viz níže).
- **Stav** (Povinné / Nepovinné / Skrýt).
- **Viditelnost** — otázku lze zobrazit jen vybraným skupinám.
- **Smazání dat tři měsíce po události** (automatická retence v rámci GDPR).

Pořadí otázek upravujete drag-and-drop.

### Typy otázek

Při vytváření otázky vyberete typ:

1. **Odpovědí vlastním textem** — volný textový input.
2. **Výběr jedné odpovědi z nabízených** — dropdown nebo radio.
3. **Výběr jedné nebo vlastní text** — kombinace.
4. **Výběr více odpovědí** — checkbox.
5. **Výběr více odpovědí nebo vlastní text** — kombinace.
6. **Výběr jedné odpovědi s limitem počtu odpovědí** — například *Autobus č. 1 (20 míst), Autobus č. 2 (20 míst)*. Systém hlídá kapacitu.
7. **Výběr ubytování, výběr spolubydlícího ze seznamu účastníka** — viz článek *Správa ubytování a výběru spolubydlícího*.
8. *(ISIC — nepoužívat, integrace nefunguje.)*
9. **Výběr více účastníků ze seznamu.**
10. **Vložit obrázek** — účastník nahraje obrázek.
11. **Vložit datum.**
12. **Vložit čas.**
13. **Vložit datum a čas.**
14. **Vložit číslo.**
15. **Informační text** — nejde o otázku, jen blok textu vložený do formuláře (například instrukce).
16. **Vložit PDF / XLSX / DOCX** — účastník nahraje soubor.
17. **Výběr země ze seznamu.**

### Otázka typu 2 — varianty odpovědí a pokročilá nastavení

U otázky *Výběr jedné odpovědi* vytváříte seznam možných odpovědí. U každé odpovědi lze:

- **Nastavit viditelnost** — odpověď se zobrazí jen vybraným skupinám.
- **Zařadit účastníka do skupiny** podle zvolené odpovědi. Příklad: otázka *Odkud přijedete?* s odpovědí *Brno* zařadí účastníka do skupiny **Brno**. Potom můžete na tuto skupinu cílit komunikaci.
- **Přidat podmíněné otázky** pod konkrétní odpověď — viz článek *Jak fungují podmíněné otázky v registračním formuláři*.
- **Odeslat ICS dle vybrané odpovědi** (dostupné u otázky typu 2 a 6). Místo ICS s datem události systém odešle ICS s daty podle konkrétní odpovědi. Každé odpovědi tak přiřadíte vlastní datum od–do.

### Otázka typu 6 — odpověď s limitem

Otázka typu 6 se hodí na situace s pevnou kapacitou — autobusy, workshopy, večerní program. U každé odpovědi nastavíte:

- **Maximální počet míst.**
- **Zobrazit účastníkům, kolik je limit a kolik zbývá** — volitelné zobrazení zbývající kapacity.
- **Zobrazit možný počet doprovodů** — nastavíte, o kolik doprovodů se registrace může ucházet.
- **Odeslat ICS dle vybrané odpovědi.**
- **Smazat data po třech měsících.**

Typ 6 řeší i doprovod jednotnou cestou — můžete v jedné otázce nabídnout autobus + počet doprovodů.

### Úvodní text, text po odeslání, pozice tlačítka

V administraci formuláře můžete upravit:

- **Pozici registračního tlačítka** na microsite.
- **Text na obrazovce po vyplnění a odeslání formuláře** — zobrazí se jako děkovná stránka. Podporuje zástupné proměnné (jméno účastníka, název události).

### Náhled a export

- **Náhled formuláře** otevře formulář přesně tak, jak ho uvidí účastník.
- **Struktura otázek** zobrazí přehled, jak jsou podmíněné otázky navázané.
- **Exporty** — odpovědi z formuláře lze stáhnout v Excelu nebo CSV. V administraci je možnost ukládat různá filtrovaná zobrazení pro týmy. Na stejné záložce stáhnete i export **GDPR souhlasy nad rámec** — seznam všech účastníků události s přehledem, kdo který souhlas nad rámec udělil a kdo ne. Stejný export nabízí i sekce **Statistiky**; kdy který export použít, popisuje článek [Práce s objednávkami a exporty](../06_reporting-a-po-akci/03_prace-s-objednavkami-a-exporty.md).

### Vícejazyčnost

Přepínač jazyků (dvě vlajky v pravém horním rohu) přepíná jazyk, který právě upravujete. Při vícejazyčné události vyplňujete každý jazyk zvlášť — otázky, odpovědi, texty. Pokud jazyk nevyplníte, použije se primární jazyk události.

### Ochrana osobních údajů a souhlasy nad rámec

Na konci formuláře se účastníkovi zobrazuje text ochrany osobních údajů (přednastavený nebo vlastní — nastavuje se v **Nastavení workspace → Ochrana osobních údajů**) a **souhlasy nad rámec** (marketing, publikace fotografií, profilování). Na úrovni formuláře rozhodujete, zda se souhlasy nad rámec mají zobrazit. Kdo který souhlas udělil, zjistíte z exportu *GDPR souhlasy nad rámec* na záložce **Exporty**.

## Na co si dát pozor

### Organizátor přidá otázku typu 8 (ISIC) s očekáváním, že se ověří studentský průkaz

Integrace s ISIC dnes nefunguje — tuto variantu nepoužívejte. Pro ověření studenta použijte běžnou otázku (např. typ 10 — vložit obrázek studentského průkazu) nebo ověřujte ručně.

### Doplňující otázky nejsou nastavené, a když účastník projde automatickou registrací u placené události, nesebrala se z něj žádná data

U placených událostí s doplňujícími daty vždy volte **registraci s doplněním informací**, ne automatickou. U neplacených událostí stačí přidat doplňující otázky a formulář se zobrazí.

### Otázka typu 6 (s limitem) je zapnutá a účastník vidí autobus, ale kapacita se nezobrazuje

Přepínač **Zobrazit účastníkům, kolik je limit a kolik zbývá** je volitelný. Pokud kapacitu nechcete zobrazovat, ale chcete ji počítat, nechte přepínač vypnutý. Systém stejně kontroluje zaplnění.

### Překlad otázek a odpovědí vyplněný jen v některých aktivních jazycích. Účastník s preferencí prázdného jazyka uvidí formulář v primárním jazyce

Přepněte vlajkou přes každý aktivní jazyk a doplňte znění. Pokud jazyk nevyplníte, použije se primární jazyk jako fallback — to znamená, že účastník uvidí formulář v jazyce, který si nezvolil.

### Otázky nastavené, ale není promyšlené, jak se odpovědi propíšou do skupin. Organizátor pak ex post ručně třídí účastníky

U otázky typu 2 (výběr jedné) využijte nastavení **Zařadit do skupiny** přímo u odpovědi. Skupinu založte předem, formulář se o přiřazení postará.

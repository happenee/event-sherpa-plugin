# Sestavení reportu účastníků

> Výběr účastníků a sloupců z více zdrojů do jednoho XLSX, ukládání šablon a čtení prázdných nebo vícečetných hodnot.

- Článek v Help Centru: https://help.happenee.com/cs/articles/99-sestaveni-reportu-ucastniku
- English version: https://help.happenee.com/en/articles/99-building-an-attendee-report
- Kolekce: Reporting a práce po události
- Aktualizováno: 2026-10-26

---

> [!info] Krátce
> Report účastníků spojí vybrané údaje z jedné události do jednoho souboru XLSX. Filtry určují, koho zahrnete, a sloupce určují, které údaje dostanete. Každý účastník má právě jeden řádek; opakovaně používaný výběr sloupců můžete uložit jako šablonu.

## Jak začít

1. Otevřete událost a **Statistiky a reporting**. V části **Exporty** najdete **Reporty účastníků**; zvolte **Otevřít reporty**.
2. Vyberte předpřipravenou nebo uloženou šablonu. Pro vlastní výběr zvolte **Nová šablona**: rovnou se otevře editor sloupců, ve kterém je předvybrané jméno, příjmení a e-mail. Doplňte další údaje, upravte pořadí a výběr potvrďte tlačítkem **Použít**.
3. Zvolte skupiny, stav registrace nebo odbavení a potvrďte filtry tlačítkem **Použít**. Výchozí filtr zahrnuje účastníky se stavem **Zúčastní se**. Sloupce otevřené šablony později změníte přes **Upravit sloupce**.
4. Zkontrolujte náhled a shrnutí stažení. Tlačítkem **Stáhnout report** stáhnete aktuální výběr i bez uložení šablony. Výběr, který budete potřebovat znovu, uložte tlačítkem **Uložit šablonu**.







## Detail

### Šablona a stažený report

Šablona uchovává sloupce, jejich pořadí a vlastní názvy hlaviček pro tuto událost. Filtry se do ní neukládají, proto před každým stažením zkontrolujte, koho zahrnujete. Stažený report obsahuje data platná v okamžiku jeho vytvoření; pozdější změny události soubor nezmění.

Předpřipravené šablony pokrývají kontakty a skupiny, odpovědi registračního formuláře, registrace na program a hlasování s feedbackem. Jejich původní definici nepřepíšete; upravený výběr uložíte jako vlastní šablonu. Šablony patří události a mohou je upravovat organizátoři, kteří k ní mají přístup; u vlastní šablony vidíte autora a datum poslední úpravy.

Otevřenou vlastní šablonu přejmenujete tlačítkem **Přejmenovat** vedle jejího názvu. Duplikovat nebo s potvrzením smazat ji můžete z nabídky u šablony v seznamu, kde je i přejmenování. Smazaná šablona zmizí všem organizátorům události.



### Výběr účastníků

Skupiny, stav registrace a odbavení omezují řádky reportu. Rozpracovaný filtr se projeví až po **Použít**. Pro kontrolu všech účastníků použijte reset filtrů; samotný výchozí stav Zúčastní se všechny účastníky nezahrnuje. Testovací účty vyloučené ze Statistik se nezapočítávají ani do reportu.

### Výběr a pořadí sloupců

Vyberete jednotlivá pole nebo celý zdroj. Dostupné údaje zahrnují základní údaje kontaktu, skupiny, vlastní pole, otázky registračního formuláře, konkrétní sessions a jejich registrace či hodnocení, osobní odpovědi hlasování a feedbacku a přiřazené vstupenky nebo registrační odkazy.

Hledání funguje i bez diakritiky. Vybrané sloupce přesunete přetažením nebo šipkami a můžete přejmenovat jejich hlavičky. Pořadí shora dolů odpovídá sloupcům XLSX zleva doprava. Změny editoru potvrdíte pomocí **Použít**.

Výběr celého zdroje nebo jeho atributu zahrnuje i nově přidané odpovídající otázky a sessions. Výběr konkrétních položek se automaticky nerozšiřuje. Když dříve vybraná otázka nebo session zanikne, šablona při otevření sloupec odebere a upozorní vás.

### Náhled, uložení a neuložené změny

Náhled ukazuje prvních pět řádků. Stažený soubor obsahuje všechny účastníky odpovídající potvrzeným filtrům, stejné sloupce a jejich pořadí. Nad stažením zkontrolujte počet účastníků, sloupců a použité filtry.

Neuložený výběr můžete stáhnout hned. Novou šablonu uložíte tlačítkem **Uložit šablonu** a pojmenujete ji. Úpravy vlastní šablony uložíte přes **Uložit změny**, upravenou předpřipravenou nebo vlastní šablonu jako kopii přes **Uložit jako novou**. Přepnutí šablony a odchod s úpravami vyžadují rozhodnutí, zda je zachovat nebo zahodit. Novou šablonu, ve které jste nezměnili předvybrané sloupce, Happenee při odchodu zahodí bez dotazu. Při souběžné změně jiným organizátorem se vraťte k aktuální šabloně nebo uložte vlastní kopii.



### Prázdné buňky a více hodnot

Prázdná buňka znamená, že údaj není k dispozici. V náhledu ji zastupuje pomlčka; XLSX zachovává prázdnou buňku. Chybějící odpověď účastníka z reportu nevyřadí. Více skupin, rezervací či odpovědí se spojí středníkem v jedné buňce.

Jednotlivé datum je v XLSX datumová buňka; více datumů ve stejné buňce je text. Ceny a hodnocení se zapisují jako čísla, ostatní hodnoty jako text. Systémové hlavičky používají jazyk administrace, otázky a další obsah jazyk obsahu události.

### Osobní odpovědi a vstupenky

Anonymní odpovědi se k účastníkovi nepřipojí. Dokud událost neskončí, zobrazují se osobní odpovědi hlasování a feedbacku jen u kontaktů přihlášeného organizátora. U feedbacku se použije poslední odeslání.

Více přiřazených vstupenek jednoho účastníka zůstává v jednom řádku. Názvy a vouchery se spojí, ceny po slevě se sečtou za jeho vstupenky. Částka společné objednávky se nepřipisuje každému účastníkovi.

### Rozsah reportu a předání souboru

Report je určený pro jednu událost. Pohled zůstává v administraci; kolegům bez přístupu předáte stažený soubor. Pro účetní doklady, jednotlivé skeny nebo jiný podrobný výstup použijte odpovídající samostatný export. Stažený soubor může obsahovat osobní údaje, proto předávejte jen údaje potřebné pro daný účel.

## Na co si dát pozor

### Odbavení session je prázdné

Údaj o odbavení jednotlivé session zatím není k dispozici. Prázdnou buňku nevykládejte jako neúčast. Odbavení celé události je samostatný údaj a filtr.

### Náhled ukazuje jen část účastníků

Pět řádků slouží ke kontrole struktury. Celkový počet a filtry určují obsah celého stažení; shodu kontrolujte podle shrnutí nad reportem.

### Vstupenky jednoho účastníka mají různé měny

Takové ceny nelze sečíst a stažení s cenovými sloupci se zastaví. Odeberte cenové sloupce a podrobné finanční vyhodnocení proveďte v příslušném exportu vstupenek nebo objednávek.

### Výběr má příliš mnoho sloupců

Od 60 sloupců vás editor upozorní na rozsah, nejvýše lze vybrat 200. Počet mohou zvýšit i nově přidaná pole u automaticky rozšiřovaného výběru. Omezte sloupce podle účelu reportu.

## Související články

- [Interpretace statistik účastníků](https://help.happenee.com/cs/articles/51-interpretace-statistik-ucastniku)
- [Práce s objednávkami a exporty](https://help.happenee.com/cs/articles/52-prace-s-objednavkami-a-exporty)

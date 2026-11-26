# Hromadný import řečníků

> Dvě metody hromadného importu řečníků — nahrání souboru XLS/XLSX/CSV s mapováním sloupců, nebo výběr konkrétních řečníků z jiné události včetně fotografií a překladů.

- Článek v Help Centru: https://help.happenee.com/cs/articles/67-hromadny-import-recniku
- English version: https://help.happenee.com/en/articles/67-bulk-import-of-speakers
- Kolekce: Obsah a zkušenost účastníka
- Aktualizováno: 2026-08-07

---

> [!info] Krátce
> Hromadný import umožňuje vytvořit více řečníků najednou místo ručního zadávání po jednom. Vybíráte ze **dvou metod**: **Nahrát soubor** (XLS, XLSX nebo CSV, který si připravíte sami) nebo **Importovat z jiné události** (vyberete konkrétní řečníky z modulu Speakers jiné události). Oba průvodce mají pět kroků a před zápisem ukážou náhled s kontrolou. Zásadní rozdíl: import z jiné události **přenese i fotografie a jazykové mutace**, souborový import ne.

## Jak začít

- **Rozhodněte, odkud data berete.** Jsou řečníci už v jiné události v Happenee? Použijte *Importovat z jiné události* — ušetříte si ruční doplňování fotek. Přicházejí zvenčí (od klienta, z CRM)? Připravte tabulku.
- U souborového importu si připravte data v Excelu. Můžete stáhnout **šablonu** přímo z administrace nebo použít **vlastní soubor** — sloupce ručně namapujete v druhém kroku průvodce.
- Rozhodněte, **v jakých jazycích** budou texty řečníků (pracovní pozice, bio). Šablona se generuje podle jazyků aktivovaných u vaší události — pro jednojazyčnou událost dostanete šablonu jen s vaším jazykem, pro vícejazyčnou se sloupci pro každý jazyk zvlášť.
- U souborového importu si připravte **fotografie zvlášť**. Přes tabulku se nahrát nedají, doplníte je po importu ručně v panelu úprav každého řečníka.
- Pokud chcete řečníky rovnou navázat na konkrétní sessions, **sessions musí být nejprve vytvořené v Programu**. U importu z jiné události se vazby nepřenášejí vůbec — počítejte s tím, že je nastavíte znovu.

## Detail

### Kde Import najdete

V administraci přejděte na **Obsah → Řečníci**. V hlavičce sekce jsou dvě záložky: **Řečník** (seznam řečníků) a **Import**. Otevřete záložku **Import**.

### Dvě metody importu

Záložka **Import** začíná rozcestníkem **Zvolte způsob importu** se dvěma kartami:

- **Nahrát soubor** — *„Import speakerů ze souboru XLS, XLSX nebo CSV."* Data si připravíte sami v tabulce. Zbytek tohoto článku popisuje tuhle cestu.
- **Importovat z jiné události** — *„Vyberte konkrétní speakery z jiného Speakers modulu."* Řečníky zkopírujete z události, která je už má nastavené. Popsáno v sekci *Import z jiné události* níže.

Rozhodovací vodítko: pokud řečníky **už někde v Happenee máte** — loňský ročník, jiná pobočka, událost, ze které jste kopírovali — použijte import z jiné události. Přenese se s nimi **fotografie i jazykové mutace**, které přes tabulku nedostanete. Tabulku použijte tehdy, když data přicházejí zvenčí (od klienta, z registračního formuláře řečníků, z CRM).

### Šablona ke stažení

V prvním kroku průvodce klikněte na **Stáhnout šablonu**. Šablona je XLSX s jedním listem, hlavičkovým řádkem a jedním ukázkovým řádkem s fiktivními daty.

Šablona je **lokalizovaná podle primárního jazyka vaší události** — česká událost dostane CS variantu (list *Řečník*, hlavičky v češtině), anglická událost EN variantu (list *Speaker*, hlavičky v angličtině).

Šablona nemá vyplněné dropdowny ani validační listy. Číselné kódy pro **Úroveň zobrazení** a **Stav** zapíšete ručně — vysvětlení kódů je přímo v názvu hlavičky sloupce.

### Pole, která lze naimportovat

- **Jméno** *(povinné)*
- **Příjmení** *(povinné)*
- **Firma** *(volitelné)*
- **Země** *(volitelné)* — Vyplňuje se **kódem země**, ne názvem — ukázkový řádek v šabloně má `CZ`.
- **Pracovní pozice (CS / EN / SK …)** *(volitelné)* — Samostatný sloupec pro každý jazyk aktivovaný u události.
- **Bio (CS / EN / SK …)** *(volitelné)* — Samostatný sloupec pro každý jazyk aktivovaný u události.
- **Úroveň zobrazení** *(volitelné)* — Číselný kód `1`–`3`. Když sloupec nevyplníte, použije se **Základní**.
- **Stav** *(volitelné)* — Číselný kód `0`–`2`. Když sloupec nevyplníte, řečník se naimportuje se stavem **Skryto**.

Povinné jsou pouze **Jméno** a **Příjmení**. Ostatní pole jsou volitelná. U **Úrovně zobrazení** a **Stavu** se při prázdné hodnotě aplikuje výchozí nastavení (úroveň **Základní**, stav **Skryto**) — viz pozor níže.

Sloupce pro pracovní pozici a bio se v šabloně i v průvodci **objeví jen pro jazyky, které má vaše událost aktivované**. Pokud má událost jen češtinu, dostanete šablonu jen s *Pracovní pozice — CS* a *Bio — CS*; jiné jazyky se vůbec nenabídnou.

### Číselné kódy: Úroveň zobrazení a Stav

V Excelu se obě hodnoty zapisují čísly:

**Úroveň zobrazení** určuje pořadí a velikost karty řečníka na microsite a v aplikaci. Když sloupec necháte prázdný, použije se **Základní** (kód `3`):

- **`1`** — Nejvyšší
- **`2`** — Vyšší
- **`3`** — Základní

**Stav** určuje, kde se profil řečníka zobrazuje účastníkům. Když sloupec necháte prázdný, řečník se naimportuje se stavem **Skryto** (kód `0`):

- **`1` — Publikováno** — Profil viditelný všude — na hlavní stránce účastnické aplikace, v seznamu řečníků na microsite i v aplikaci, u sessions v programu, na detailu session i na vlastní detailové stránce řečníka.
- **`2` — V programu** — Profil **není** v seznamu řečníků ani na hlavní stránce aplikace; je viditelný u sessions v programu, na detailu session a na vlastní detailové stránce řečníka (dostupné prokliknutím z detailu session). Hodí se pro moderátory a interní přednášející, které nechcete vystavovat v seznamu řečníků.
- **`0` — Skryto** — Profil není viditelný nikde — ani v seznamu řečníků, ani u sessions; nemá ani vlastní detailovou stránku.

### Průvodce importem (5 kroků)

V horní části obrazovky uvidíte krokový indikátor: **Nahrát → Mapování → Vazby → Náhled → Výsledek**. Mezi kroky se lze vracet zpět.

**1. Nahrát.** Stáhněte šablonu (volitelně) nebo rovnou nahrajte svůj Excel přes výběr souboru. Klikněte na **Nahrát a zpracovat** — soubor se odešle a průvodce přejde na další krok.

**2. Mapování.** Průvodce načte hlavičky vašeho souboru a zobrazí je v tabulce *Sloupec v Excelu — Ukázkové hodnoty — Mapovat na pole*. U každého sloupce vyberte z rozbalovacího menu, kam se má hodnota uložit (Jméno, Příjmení, Bio — CS atd.). Sloupce, kterým necháte mapování prázdné, se přeskočí. Mapování **se nikam neukládá** — při každém importu ho nastavujete znovu od začátku. Klikněte na **Ověřit a zobrazit náhled**.

**3. Vazby.** Doplnění vazeb importovaných řečníků na další obsah události (typicky sessions z Programu). Tento krok je dostupný jen tehdy, pokud má vaše událost relevantní obsah, na který lze vázat.

**4. Náhled.** Průvodce zobrazí souhrn: **Celkem / Validní / Varování / Chyby / Duplicity**. Pod souhrnem je tabulka s každým řádkem souboru a stavem (validní řádek je označený zeleně). **Žádná data se ještě nezapsala** — máte poslední možnost se vrátit a opravit. Pokud souhrn vyhovuje, klikněte na **Importovat**.

**5. Výsledek.** Po dokončení importu se zobrazí výsledná čísla: **Vytvořeno / Přeskočeno / Chyby**. Z této obrazovky můžete přejít na seznam řečníků (**Pokračovat na seznam**) nebo si stáhnout detailní CSV report o každém řádku (**Stáhnout report (CSV)**) — hodí se, pokud chcete dohledat, který řádek se nezaimportoval a proč.

### Jak průvodce pozná duplicitu

Duplicita se určuje podle **jména a příjmení dohromady**. Řádek je duplicitní, pokud:

- řečník se stejným jménem a příjmením **už v události existuje**, nebo
- stejné jméno a příjmení se **opakuje v souboru** na více řádcích.

Duplicitní řádky se **nezaimportují** — průvodce je přeskočí. Z opakujících se řádků se vždy zaimportuje **první výskyt**, ostatní se zahodí. V kroku *Náhled* uvidíte počet duplicit dopředu; ve *Výsledku* se přeskočené řádky započítají do **Přeskočeno**.

Z toho plyne: import **nepřepisuje existující řečníky**. Pokud chcete u řečníka, který už v události je, změnit data hromadně, import na to není — použijte hromadné akce v seznamu řečníků, nebo řečníka upravte ručně.

### Import z jiné události

Druhá metoda z rozcestníku. Nezakládá se na souboru — vybíráte konkrétní řečníky z modulu Speakers **jiné události ve stejném workspace**. Průvodce má také pět kroků, ale jiných: **Událost → Modul → Speakeři → Náhled → Výsledek**.

**1. Událost.** Pole **Zdrojová událost** se seznamem událostí ve tvaru *název (#ID)* a vyhledáváním **Vyhledat událost podle názvu**. Dokud událost nevyberete, tlačítko **Pokračovat** je neaktivní.

**2. Modul.** Pole **Zdrojový Speakers modul**. Vybírá se zvlášť, protože jedna událost může mít modul Speakers víckrát.

**3. Speakeři.** Tabulka řečníků zdrojového modulu se sloupci **Jméno · Společnost · Pozice · Stav · Fotografie** a zaškrtávacími políčky. Nahoře je vyhledávání **Vyhledat speakera**, počitadlo vybraných a tlačítka **Vybrat všechny** / **Zrušit výběr**. Ve sloupci *Stav* vidíte, jestli je řečník ve zdrojové události **Publikováno**, **V programu**, nebo **Skryto** — vyberete tak i profil, který u sebe zatím nechcete zveřejnit. Pokračujete tlačítkem **Zkontrolovat náhled**.

**4. Náhled.** Nahoře shrnutí **Zdroj** a **Cíl** (obojí jako *událost / modul (#ID)*), pod ním šest počitadel: **Vybráno · K importu · Duplicity · Neplatné · Překlady · Fotografie**. Pod nimi tabulka s výsledkem kontroly u každého řečníka (**Připraveno k importu**). Zápis spustíte tlačítkem **Importovat**.

**5. Výsledek.** Pět čísel: **Vytvořeno · Přeskočeno · Překlady · Fotografie · Bez fotografie**, a tlačítka **Přejít na seznam speakerů** nebo **Importovat další**.

**Co se přenese a co ne:**

- **Profilová data (jméno, firma, pozice, bio)** — ano
- **Fotografie** — ano — JPEG, PNG a GIF. Soubor dostane nový bezpečný název; chybějící nebo neplatná fotka import daného řečníka **nezastaví**, jen skončí v počtu *Bez fotografie*.
- **Jazykové mutace** — ano — počet vidíte v počitadle *Překlady*.
- **Vazby na program a sessions** — **ne.** Průvodce na to výslovně upozorňuje. Přiřazení k sessions musíte v cílové události udělat znovu.

**Duplicity se hlídají proti cílové události.** Řečník, který v cílové události už existuje, se do počtu *K importu* nezapočítá, v náhledu se v tabulce vůbec neobjeví a ve výsledku spadne do **Přeskočeno**. Import kvůli němu neselže a ostatní projdou. Znamená to ale, že **profil se nepřepíše** — opakovaný import stejného řečníka jeho data v cílové události neaktualizuje.

### Co import neumí

- **Nahrání fotografií ze souboru.** Šablona ani souborový průvodce nemají sloupec pro fotku ani URL fotografie. Fotografie doplníte po importu ručně — nebo použijte **import z jiné události**, kde se kopírují.
- **Import sessions / programu.** Tento průvodce vytváří jen profily řečníků. Sessions vytvářejte ručně v sekci Program. Vazby mezi řečníky a sessions lze nastavit ve 3. kroku průvodce, případně později z panelu úprav řečníka nebo session.
- **Hromadná aktualizace existujících řečníků.** Import je primárně určen na vytvoření nových profilů. Pokud potřebujete změnit úroveň zobrazení nebo stav u řečníků, kteří už v události existují, použijte hromadné akce v seznamu řečníků.

## Na co si dát pozor

### Šablona obsahuje ukázkový řádek (Jan Novak) — pokud ho nesmažete, naimportuje se jako reálný řečník

Stažená šablona má první datový řádek vyplněný fiktivní ukázkou. Ve fázi *Náhled* se objeví jako validní. Před vyplněním vlastních dat ukázkový řádek smažte, jinak vám v seznamu řečníků zůstane Jan Novak z Happenee.

### Úroveň zobrazení a Stav se zapisují čísly, ne názvy

V Excelu napsané *„Nejvyšší“* nebo *„Publikováno“* průvodce při importu nepřevezme — pole očekává číselný kód (`1`/`2`/`3` pro Úroveň zobrazení, `0`/`1`/`2` pro Stav). Pokud zadáte slovo nebo neplatné číslo (např. `4`), řádek se v *Náhledu* označí jako chyba. Vysvětlení kódů je přímo v hlavičce sloupce v šabloně.

### Prázdný sloupec Stav naimportuje všechny řečníky se stavem Skryto

Stav ani Úroveň zobrazení nejsou povinné, ale prázdná hodnota neznamená „neměnit“ — aplikuje se výchozí nastavení. Prázdný **Stav** = **Skryto** (řečníci nebudou účastníkům vidět nikde), prázdná **Úroveň zobrazení** = **Základní**. Pokud chcete řečníky rovnou publikovat, sloupec Stav vyplňte (`1` = Publikováno). Po importu pak stav zkontrolujte v seznamu řečníků — pokud jsou všichni skrytí, doplnili jste prázdný sloupec.

### Šablona stažená z jedné události neodpovídá jiné události s jinými jazyky

Sloupce pro pracovní pozici a bio se generují podle jazyků konkrétní události. Pokud stáhnete šablonu z trojjazyčné události (CS + EN + SK) a použijete ji u jednojazyčné, sloupce navíc se buď nenamapují (zůstanou prázdné), nebo budou matoucí. **Šablonu stáhněte vždy z té události, do které importujete.**

### Fotografie přes import nelze nahrát — počítejte s ruční prací po importu

Hromadný import řeší jen data v textových polích. Pokud má vaše událost 80 řečníků, počítejte s tím, že po importu obejdete 80 panelů úprav a doplníte fotografie. Naplánujte si na to čas.

### Krok *Vazby* nepřeskakujte bez kontroly

Pokud máte sessions v Programu už vytvořené a chcete řečníky rovnou navázat, je tento krok nejjednodušší cesta. Pokud ho přeskočíte, řečníky bude nutné dohledávat a vázat ručně z panelu jednotlivých sessions — u 50 řečníků a 30 sessions je to hodina práce navíc.

### Dva různí lidé se stejným jménem a příjmením — druhý se nenaimportuje

Duplicita se pozná jen podle jména a příjmení, ne podle firmy nebo e-mailu. Pokud máte dva různé řečníky se shodným jménem a příjmením (například dva Jany Nováky z různých firem), průvodce druhého vyhodnotí jako duplicitu a **nezaimportuje ho**. Zaimportuje se jen první. Před kliknutím na **Importovat** zkontrolujte v *Náhledu* počet duplicit — pokud je vyšší, než čekáte, projděte soubor a u skutečně různých lidí jména odlište (například druhým jménem), jinak vám jeden z nich vypadne.

### Řečníci se z loňského ročníku vyplňují ručně do tabulky

Nejdražší varianta, jak dostat do události lidi, které Happenee už zná. Přepisováním do Excelu přijdete o fotografie i jazykové mutace a strávíte tím hodinu. Pokud je zdrojová událost pořád ve workspace, použijte **Importovat z jiné události** — vyberete je zaškrtnutím a fotky přijdou s nimi.

### Po importu z jiné události chybí řečníci v programu

Přenesou se profily, **ne vazby na sessions**. Průvodce to říká v náhledu, ale snadno se to přehlédne. Po importu projděte program a řečníky k sessions přiřaďte znovu — z panelu úprav řečníka na záložce *Sessions*, nebo z panelu session.

### Opakovaný import z jiné události má aktualizovat už naimportované řečníky

Neaktualizuje. Duplicity se hledají proti cílové události a duplicitní řečník se **přeskočí** — v náhledu se v tabulce vůbec neobjeví a ve výsledku spadne do *Přeskočeno*. Import kvůli němu neselže, ale profil zůstane v původní podobě. Změny dělejte ručně nebo hromadnými akcemi v seznamu řečníků.

### Mapování sloupců musíte nastavit při každém importu znovu

Průvodce si namapování sloupců nepamatuje — po každém nahrání souboru ho zadáváte od začátku. Pokud importujete opakovaně (například průběžně přibývají řečníci), držte se ve svém souboru **stejných názvů a pořadí sloupců jako ve stažené šabloně**. Mapování pak zabere pár vteřin a nepřehlédnete žádné pole.

## Související články

- [Správa řečníků](https://help.happenee.com/cs/articles/23-sprava-recniku)
- [Hromadný import sessions](https://help.happenee.com/cs/articles/68-hromadny-import-sessions)
- [Hromadný import sponzorů](https://help.happenee.com/cs/articles/71-hromadny-import-sponzoru)
- [Hromadný import vystavovatelů](https://help.happenee.com/cs/articles/72-hromadny-import-vystavovatelu)

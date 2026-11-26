<!-- source: kb.cs.03.03 -->

---
title: "Správa řečníků"
description: "Obsahová funkce pro profily osob v programu, jejich přiřazení k sessions a zobrazení účastníkům."
modules: ["recnici"]
last_updated: "2026-09-07"
version: 11
---

> [!info] Krátce
> Řečníci je **obsahová funkce**, která umožňuje přidat k události osoby vystupující v programu a jejich profily zobrazit účastníkům. Každý řečník má samostatný profil (jméno, firma, pozice, fotografie, bio) a lze ho přiřadit k jedné nebo více sessions v Programu — v roli **řečník** nebo **moderátor**. Úroveň zobrazení určuje velikost karty a pořadí skupin řečníků na microsite i v účastnické aplikaci; pořadí uvnitř úrovně určíte přetažením v tabulce nebo funkcí Automatické řazení. Profil řečníka je obsahový záznam, ne účastnický účet — s registrací člověka nijak nesouvisí, takže zaregistrovanému účastníkovi profil jen přidáte.

## Jak začít

- Ujasněte si, **kdo u vás vystupuje** a v jaké roli — keynote řečník, panelista, moderátor, facilitátor workshopu.
- Připravte si jejich **profily**: jméno, firma, pozice, bio, profilová fotografie.
- Rozhodněte o **úrovni zobrazení** — keynote řečníci *Nejvyšší*, běžní řečníci *Základní*.
- Než začnete přiřazovat řečníky k sessions, musí být sessions **nejprve vytvořeny v Programu**.

## Detail

### Kde Řečníky najdete

V levém menu → **Obsah** → **Řečníci** (přidejte tlačítkem **+ Přidat**, pokud ještě obsahovou funkci nemáte).

### Přidání nového řečníka

1. Klikněte na **+ Nový řečník**.
2. Vyplňte **Jméno** a **Příjmení** (povinné).
3. Zadejte **Firmu** a **Pracovní pozici** (volitelné).
4. Vyberte **Zemi** (volitelné) — rozbalovací seznam se zemí, ne volné textové pole. Po rozkliknutí se objeví vyhledávací pole, takže zemi nemusíte hledat scrollováním.
5. Vyberte **Úroveň zobrazení**: **Základní** (výchozí), **Vyšší** nebo **Nejvyšší**.
6. Nahrajte **Profilovou fotografii** (JPG nebo PNG, doporučený rozměr 800×800 px, poměr stran 1:1, max. velikost souboru 800 KB).
7. Vyplňte **Bio** — text v rich text editoru.
8. Uložte tlačítkem **Uložit** (uloží skrytý) nebo **Uložit a publikovat**.

Vyplněná **Země** se účastníkovi zobrazí na **detailu řečníka** na microsite a v účastnické aplikaci — pod firmou, s ikonou špendlíku. Má smysl u mezinárodních konferencí, kde země řečníka nese informaci; u ryze tuzemské události ji nechte prázdnou, jinak jen zabírá místo v profilu.

### Co řídí podobu výpisu na microsite

Nastavení u řečníka rozhoduje o **jeho profilu** — jak vypadá karta a kde je vidět. **Kolik řečníků se vypíše na hlavní stránce microsite** ale řídí něco jiného: v **Microsite události → Obsah** má záložka *Řečníci* tlačítko **Zobrazení** a v něm volbu mezi náhledem prvních řádků s proklikem na podstránku a výpisem všech. Detail v článku [Jak funguje microsite události](01_jak-funguje-microsite-udalosti.md).

### Úrovně zobrazení

Úroveň zobrazení určuje prominenci profilu a pořadí skupin řečníků na microsite i v aplikaci:

- **Nejvyšší** — profily se zobrazují jako první, karta je větší. Typicky keynote řečník, speciální host.
- **Vyšší** — druhá vlna, menší karta než *Nejvyšší*, ale větší než *Základní*.
- **Základní** (výchozí) — běžní řečníci, panelisté, řečníci v rámci jednotlivých sessions.

### Pořadí řečníků v rámci úrovně

Pořadí řečníků uvnitř každé úrovně zobrazení určujete sami. Propisuje se na microsite i do účastnické aplikace — účastníci vidí řečníky přesně tak, jak je v tabulce seřadíte. Máte dvě možnosti:

- **Ručně přetažením** — uchopte řádek řečníka za ikonu se šesti tečkami vlevo a přetáhněte ho na jinou pozici v rámci úrovně.
- **Automatickým řazením** — každá úroveň má v tabulce tlačítko **Automatické řazení**. Řazení se aplikuje jen na řečníky v dané úrovni; pokud chcete seřadit celou tabulku, spusťte ho u každé úrovně zvlášť.

Automatické řazení nabízí čtyři možnosti:

- **Abecedně podle jména** — seřadí řečníky abecedně podle křestního jména.
- **Abecedně podle příjmení** — seřadí řečníky abecedně podle příjmení.
- **Přiřadit podle firmy** — pracuje s firmou vybranou ve filtru **Firma** nad tabulkou. Podle aktuálního pořadí najde prvního řečníka s danou firmou a ostatní řečníky stejné firmy přesune přímo pod něj.
- **Přiřadit podle session** — seskupí řečníky podle přiřazení k sessions. Podle aktuálního pořadí najde prvního řečníka se stejnou session a ostatní se stejným přiřazením přesune přímo pod něj; pořadí skupin odpovídá prvnímu výskytu.

Automatické řazení je jednorázová akce, ne trvalý režim — seřadí řečníky v okamžiku kliknutí a pořadí můžete dál libovolně dolaďovat přetažením.

### Stav profilu

Stav určuje, na kterých místech microsite a účastnické aplikace je řečník vidět. Jsou tři stavy: **Publikováno**, **V programu** a **Skryto**.

**Publikováno** — řečník je vidět všude:

- na hlavní stránce účastnické aplikace,
- v modulu Řečníci na microsite i v aplikaci (v seznamu řečníků),
- v modulu Program na microsite i v aplikaci — na kartě session v seznamu sessions,
- na detailu session — v kartě řečníků a moderátorů,
- na vlastní detailové stránce řečníka.

**V programu** — řečník se **nezobrazuje v seznamu řečníků ani na hlavní stránce aplikace**, ale je vidět všude, kde se objevují jeho sessions:

- v modulu Program na microsite i v aplikaci — na kartě session v seznamu sessions,
- na detailu session — v kartě řečníků a moderátorů,
- na vlastní detailové stránce řečníka — ta zůstává funkční. Účastník se k ní dostane prokliknutím z detailu session, i když řečník v seznamu řečníků není.

Stav **V programu** se hodí pro řečníky, které chcete mít uvedené u konkrétní session, ale nechcete je vystavovat v seznamu řečníků jako „hvězdy“ události (například moderátor panelu nebo přednášející z interního týmu). Účastník je najde přes program, ne procházením seznamu řečníků.

**Skryto** — řečník není vidět nikde: ani v modulu Řečníci, ani v modulu Program, ani u sessions. Nemá ani vlastní detailovou stránku — odkaz na profil neexistuje. Hodí se pro rozpracované profily nebo dočasné stažení řečníka bez ztráty dat a přiřazení k sessions.

### Přiřazení řečníka k sessions

Sessions musí být **nejprve vytvořeny v Programu**, teprve pak můžete přiřazovat řečníky.

Z panelu řečníka:

1. Otevřete panel úprav řečníka.
2. Přejděte na záložku **Sessions**.
3. Do pole **Hledat sessions** zadejte název session.
4. Volitelně filtrujte výsledky pomocí filtru **Typ** (podle typů sessions).
5. Klikněte na **+** u příslušné session — přidá se do seznamu.
6. U každé přiřazené session zvolte roli: **Řečník** nebo **Moderátor**.
7. Uložte tlačítkem **Uložit změny**.

Přiřazení lze provést i z druhé strany — z panelu úprav session v **Obsah → Sessions** → záložka **Řečníci**.

### Role: Řečník vs Moderátor

- **Řečník** — osoba, která prezentuje obsah session.
- **Moderátor** — osoba, která session moderuje (například u panelové diskuse).

Rozdíl je vizuální — na detailu session jsou řečníci uvedeni pod nadpisem *Řečníci* a moderátoři pod nadpisem *Moderátoři*. Jeden řečník může být u různých sessions v různých rolích (u jedné jako řečník, u druhé jako moderátor).

### Řečník a účastník: dvě různé evidence

Řečník není role účastníka. Profil řečníka je **obsahový záznam** — jméno, firma, pracovní pozice, země, bio, fotografie — a popisuje toho, kdo vystupuje v programu. Nemá e-mail, nepatří k němu přihlášení do účastnické aplikace a s registrací člověka nijak nesouvisí. Účastníci jsou vedení jinde: kontakt ve **Správě kontaktů a skupin**, jeho přiřazení k události a dokončená registrace.

Obě evidence stojí vedle sebe a nepropojují se. V praxi to znamená tři věci:

- **Účastník, který už je zaregistrovaný a má vystoupit v programu** — vytvořte mu profil v *Obsah → Řečníci* (nebo ho naimportujte) a přiřaďte ho k jeho sessions. Profil vzniká **vedle** jeho registrace, ne místo ní — na účastnickém záznamu se nic nemění, takže není co opakovat ani přenastavovat.
- **Řečník, který zatím existuje jen jako profil** — do události ho profil nepřidá. Nepřijde mu pozvánka, QR vstupenku nedostane a v seznamu účastníků není. Pokud má mít i přístup do účastnické aplikace nebo se odbavit na místě, přiřaďte jeho kontakt k události a nechte ho dokončit registraci; samotné přiřazení registrace není. Postup je v článku [Ruční přidání účastníka do události](../02_nastaveni-eventu-a-registrace/15_rucni-pridani-ucastnika-do-udalosti.md).
- **Údaje se mezi evidencemi nezrcadlí.** Změna firmy nebo pracovní pozice u kontaktu se do profilu řečníka nepropíše a naopak; smazání profilu řečníka registraci nezruší.

### Kde jsou role a kde skupiny

Role **Řečník** a **Moderátor** patří k přiřazení profilu k session. Neurčují, co člověk uvidí, ani jestli je zaregistrovaný — přepínač, kterým byste ze zaregistrovaného účastníka udělali řečníka, v administraci není.

Když potřebujete řečníky rozlišit i na straně účastníků — poslat jim jinou pozvánku, zpřístupnit jim obsah navíc, filtrovat je ve statistikách — použijte **skupinu kontaktů** (typicky *Řečníci*). Skupina řídí viditelnost obsahových a engagement funkcí a cílení e-mailových kampaní — profily v modulu Řečníci ale nezakládá ani nemění. Detail v článku [Práce se skupinami a viditelností](../02_nastaveni-eventu-a-registrace/07_prace-se-skupinami-a-viditelnosti.md).

### Hromadné akce

V seznamu řečníků zaškrtněte víc řečníků najednou a použijte panel hromadných akcí:

- **Úroveň zobrazení** — hromadně změnit na *Základní / Vyšší / Nejvyšší*.
- **Stav** — hromadně změnit na *Publikováno / V programu / Skryto*.
- **Smazat řečníka** — smazání (nevratné!).

### Vícejazyčnost

Přepínačem jazyků můžete přeložit:

- Jméno a Příjmení
- Pracovní pozici
- Bio

Firma se typicky nepřekládá (název firmy je konzistentní), ale textové pole to umožní.

### Import

Řečníky lze naimportovat hromadně dvěma způsoby: **ze souboru** (XLS, XLSX nebo CSV — jméno, příjmení, firma, země, pracovní pozice, bio, úroveň zobrazení, stav) nebo **z jiné události**, kde vyberete konkrétní řečníky z existujícího modulu Speakers. Profilové fotografie se **ze souboru nenahrávají** — doplňte je ručně po importu; při importu z jiné události se naopak kopírují. Podrobný popis průvodce, šablony a kódů pro Úroveň zobrazení a Stav najdete v článku [Hromadný import řečníků](19_hromadny-import-recniku.md).

## Na co si dát pozor

### Řečník přidán, ale bez fotografie. Na microsite se zobrazí zástupný avatar s iniciálami — vypadá nedokončeně

Fotografie je volitelná, ale výrazně zlepšuje dojem. Pokud nemáte profesionální foto, použijte aspoň portrét v dobré kvalitě (800×800 px, JPG/PNG, max. 800 KB). Bez fotografie vypadá událost amatérsky.

### Všichni řečníci mají úroveň *Nejvyšší*. Hlavní stránka s řečníky je přetížená, keynote splývá s ostatními

Úroveň *Nejvyšší* používejte jen pro 1–3 nejvýraznější řečníky. Zbytek nastavte na *Vyšší* nebo *Základní*. Cílem je hierarchie.

### Automatické řazení vypadá jako trvalý režim — je to jednorázová akce

Kliknutí na možnost řečníky v úrovni seřadí jednou; systém pak pořadí sám neudržuje. Když později přidáte řečníky nebo se změní firmy či přiřazení k sessions, spusťte Automatické řazení znovu, případně pořadí dolaďte přetažením.

### Automatické řazení seřadilo jen část tabulky — řadí vždy jen jednu úroveň

Tlačítko Automatické řazení patří ke konkrétní úrovni zobrazení a seřadí jen řečníky v ní. Ostatní úrovně zůstanou beze změny — pokud chcete seřadit celou tabulku, spusťte řazení u každé úrovně zvlášť.

### Session vytvořena, řečník přiřazen — ale řečník má stav **Skryto**. Na detailu session se jeho jméno nezobrazuje

Pokud chcete řečníka vidět u session, musí mít stav **Publikováno** nebo **V programu**. Stav Skryto skrývá profil všude.

### Keynote řečník smazán omylem — ztratí se i jeho přiřazení k sessions

Smazání je **nevratné** a odebere přiřazení ke všem sessions. Samotné sessions zůstanou, ale bez řečníka. Pro dočasné odstranění použijte stav **Skryto** — profil ani přiřazení se neztratí.

### Řečník na detailu session chybí, přestože byl přiřazen — organizátor si myslí, že je chyba

Zkontrolujte stav řečníka. Pokud je **Skryto**, nezobrazuje se nikde. Pokud je **V programu**, zobrazuje se pouze u session, ne v seznamu řečníků na microsite ani na hlavní stránce aplikace.

### Import řečníků přes Excel očekává, že se nahrají i fotografie

Fotografie se přes import nenahrávají. Po importu projděte řečníky a doplňte fotografie ručně.

### Řečník má profil na microsite, ale nedostal pozvánku ani QR vstupenku

Profil v modulu Řečníci není registrace. Pokud má řečník dorazit i jako účastník — projít odbavením, otevřít účastnickou aplikaci — musí být zároveň kontaktem přiřazeným k události s dokončenou registrací. Samotné přiřazení k události potvrzovací e-mail s QR kódem nevystaví.

### Organizátor čeká, že se zaregistrovaný řečník objeví v seznamu řečníků sám

Registrační formulář profil řečníka nezaloží, ani když v něm člověk uvede, že vystupuje. Profil vytvoříte ručně nebo hromadným importem. Platí to i obráceně: kvůli profilu nikoho neposílejte registrovat znovu — profil vzniká v administraci, ne přes formulář.

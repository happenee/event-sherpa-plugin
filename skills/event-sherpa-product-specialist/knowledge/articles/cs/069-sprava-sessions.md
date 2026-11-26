# Správa sessions

> Vytváření, úprava a hromadná správa sessions na záložce Sessions: panel úprav, dědičnost nastavení z typu, stav, filtrování a hromadné akce.

- Článek v Help Centru: https://help.happenee.com/cs/articles/69-sprava-sessions
- English version: https://help.happenee.com/en/articles/69-managing-sessions
- Kolekce: Obsah a zkušenost účastníka
- Aktualizováno: 2026-09-16

---

> [!info] Krátce
> Session je základní stavební jednotka programu — konkrétní položka harmonogramu s názvem, časem, typem a dalšími údaji. Sessions vytváříte a upravujete na záložce **Sessions** v Programu: jednotlivě v panelu úprav, nebo hromadně nad vybranými sessions v seznamu. Každá session ve výchozím nastavení přebírá registraci, viditelnost a engagement z přiřazeného **typu**, ale tato nastavení lze u každé session samostatně přepsat.

## Jak začít

- Než vytvoříte první session, mějte připravené **typy** — typ určuje výchozí chování (registrace, viditelnost, engagement). Viz [Jak fungují typy sessions](https://help.happenee.com/cs/articles/27-jak-funguji-typy-sessions). Volitelně si dopředu připravte místa, štítky a registrační bloky.
- Novou session přidáte na záložce **Sessions** tlačítkem **+ Nová session**. Pokud už podobná session existuje, bývá rychlejší ji **zkopírovat** — viz *Kopírování session* níže.
- Vyplňte povinná pole: **Název session**, **Datum**, **Začátek**, **Konec** a **Typ**. Ostatní (místo, štítky, popis, řečníci, partneři) je volitelné.
- Uložte: **Uložit** session založí jako nepublikovanou, **Uložit a publikovat** ji rovnou zveřejní účastníkům.
- Čas se zadává v časovém pásmu události (viz [Vytvoření nové události](https://help.happenee.com/cs/articles/9-vytvoreni-nove-udalosti)).

## Detail

### Kde sessions najdete

V levém menu → **Obsah** → vyberte Program → záložka **Sessions**. Seznam zobrazuje všechny sessions daného Programu. Vedle jsou záložky **Typy**, **Bloky**, **Štítky**, **Místa**, **Moje agenda**, **Nastavení** a **Import**.

### Panel úprav session

Session se zakládá i upravuje ve výsuvném panelu (**Nová session** / **Upravit session**). Panel má záložky:

- **Informace** — základní údaje (datum, čas, typ, místo, štítky, poznámka; u registračních typů i blok a nastavení registrace).
- **Viditelnost** — kdo session uvidí.
- **Obsah** — popis, obrázek a engagement funkce.
- **Řečníci** — řečníci a moderátoři session.
- **Partneři** — sponzoři a vystavovatelé přiřazení k session.
- **Účastníci** — seznam registrovaných (jen při úpravě session typu Workshop nebo Časový slot).

U typu **Časový slot** přibývá ještě záložka **Sloty** — viz *Jak fungují časové sloty*.

### Záložka Informace

Tady jsou základní údaje session:

- **Datum**, **Začátek**, **Konec** — termín session v časovém pásmu události.
- **Typ** — zobrazuje se jako *vlastní název (základní chování)*, například *Keynote (Přednáška)* nebo *Workshop (Workshop)*. Typ rozhoduje o výchozím chování session.
- **Blok** — registrační blok (jen u typů Workshop a Časový slot; viz [Jak fungují registrační bloky, místa a štítky](https://help.happenee.com/cs/articles/31-jak-funguji-registracni-bloky-mista-a-stitky)).
- **Místo** — sál nebo stage, kde session probíhá (slouží i jako filtr v aplikaci).
- **Štítky** — tematické značky session.
- **Poznámka organizátora** — interní poznámka. Účastníkům se **nezobrazuje**, slouží jen organizátorům.

U typů s registrací (Workshop, Časový slot) je na této záložce navíc blok **Nastavení registrace** — viz níže.

### Dědičnost nastavení z typu

Toto je klíčová logika celého programu. Session **přebírá** tři skupiny nastavení z přiřazeného typu:

- **Nastavení registrace** (záložka Informace, u registračních typů),
- **Viditelnost** (záložka Viditelnost),
- **Engagement** (záložka Obsah).

U každé z nich je přepínač **Výchozí / Vlastní**:

- Dokud je v poloze **Výchozí**, session sdílí nastavení s typem — vidíte jen souhrn (například *Veřejné* nebo *Hodnocení, Otázky*) a změna na úrovni typu se promítne i sem.
- Přepnutím na **Vlastní** se nastavení **odpojí od typu** a rozbalí se jednotlivé volby, které teď platí jen pro tuto session. Pozdější změna typu už takovou session neovlivní.

Proč to takhle funguje: většinu sessions stejného typu nastavíte jednou na úrovni typu a nemusíte je řešit kus po kuse. *Vlastní* použijte jen tam, kde se konkrétní session od svého typu skutečně liší (jiná kapacita, jiná viditelnost). Detaily dědičnosti najdete v článku [Jak fungují typy sessions](https://help.happenee.com/cs/articles/27-jak-funguji-typy-sessions).

### Nastavení registrace u jednotlivé session

U typů Workshop a Časový slot lze po přepnutí na **Vlastní** nastavit:

- **Registrace pouze pro vybrané skupiny** — na session se přihlásí jen účastníci z vybraných skupin. Vybírat lze jen ze skupin, pro které je session viditelná (viz záložka **Viditelnost** níže).
- **Přiřadit účastníka do skupiny po registraci** — kdo se zaregistruje, automaticky se zařadí do zvolené skupiny (užitečné pro navazující cílení komunikace). Při odchodu ze session nebo po vypnutí přiřazování se skupina zase odebere — i účastníkovi, který ji má i z jiného zdroje.
- **Omezit počet registrací** — po zapnutí zadáte v krokovém poli **maximální počet účastníků** session.
- **Zobrazit počet dostupných míst** — účastníci uvidí, kolik míst ještě zbývá. Přepínač se objeví až po zapnutí **Omezit počet registrací**, protože bez limitu není z čeho volná místa počítat. Když limit později vypnete, vypne se i tento přepínač a po opětovném zapnutí limitu zůstane vypnutý, takže ho zapněte znovu.
- **Časové omezení registrace** — od kdy a do kdy se lze na session přihlásit. Hranice zadáte buď jako odstup od začátku session (*Dle začátku session*), nebo jako datum a čas (*Konkrétní datum*).
- **Odhlášení ze session** — do kdy si účastník může svou registraci zrušit sám. Stejné dva režimy.
- **Upozornění organizátorovi při změně registrace účastníka na session** — pošle e-mail, když se účastník sám zaregistruje nebo registraci zruší. Po zapnutí vyplníte adresy příjemců (víc adres oddělte čárkou); bez adresy nastavení neuložíte.
- **Upozornění účastníkovi při změně registrace na session** — pošle účastníkovi potvrzovací e-mail, když se sám zaregistruje nebo registraci zruší. Na změny, které uděláte vy, se nevztahuje; ty řídí přepínač na záložce **Účastníci**.
- **Odeslat ICS účastníkovi** — přiloží k potvrzovacímu e-mailu ICS soubor pro kalendář. Samo o sobě nic neposílá: bez zapnutého upozornění účastníkovi nepřijde ani ICS.

Tatáž pole se nastavují i jako výchozí na úrovni typu — viz [Nastavení workshopů a registrace na sessions](https://help.happenee.com/cs/articles/28-nastaveni-workshopu-a-registrace-na-sessions).

### Záložka Viditelnost

Po přepnutí na **Vlastní** zvolíte:

- **Veřejné** — session vidí všichni účastníci.
- **Pouze pro vybrané skupiny** — session uvidí jen vybrané skupiny, ostatním účastníkům bude skrytá. Po zvolení přibude pole **Vyberte skupiny**.

Volba *Pouze pro vybrané skupiny* zúží i nabídku u **Registrace pouze pro vybrané skupiny** na záložce Informace — k registraci pustíte jen skupinu, která session vidí. Nastavte proto viditelnost dřív než registraci.

Viditelnost (kdo session uvidí) je něco jiného než **stav** (zda je session vůbec publikovaná) — viz dále. Práci se skupinami popisuje [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti).

### Záložka Obsah

- **Popis** — text session v editoru (formátování, odkazy, obrázky v textu). Pozor na délku: na hlavní stránce microsite se standardně zobrazí **maximálně 400 znaků** popisu, pokud v *Microsite události → Obsah → Zobrazení* nezapnete **Zobrazit popis session v celé délce**. Podstatné napište do prvních dvou vět.
- **Obrázek** — náhledový obrázek session (JPG, PNG nebo GIF; doporučený rozměr 1200 × 600 px, poměr stran 2:1).
- **Engagement** — po přepnutí na **Vlastní** zapnete **Hodnocení session** (účastníci hodnotí session hvězdičkami) a **Otázky** (účastníci pokládají otázky v detailu session).

### Záložky Řečníci a Partneři

- **Řečníci** — přiřadíte řečníky a samostatně moderátory. Do pole **Hledejte řečníka** zadáte jméno a vyberete z profilů; přiřazeného řečníka lze **Odebrat**. Profily se spravují v obsahové funkci Řečníci (viz [Správa řečníků](https://help.happenee.com/cs/articles/23-sprava-recniku)) — přiřazení jde i z druhé strany, z panelu řečníka.
- **Partneři** — k session přiřadíte sponzory nebo vystavovatele přes pole **Hledat sponzory a vystavovatele**.

### Záložka Účastníci

U uložené session typu Workshop nebo Časový slot je k dispozici záložka **Účastníci** se seznamem registrovaných účastníků. Souhrn nad seznamem ukazuje obsazenost a odděluje registrace, které udělali účastníci sami, od těch, které jste udělali vy.

U workshopu tu účastníky spravujete i ručně: nového přidáte přes pole **Hledat účastníky**, stávajícího ze seznamu odeberete. Ručně přidaní jsou označeni **Přiřazen organizátorem**. Přidávat smíte i nad nastavený limit registrací, systém vás na překročení jen upozorní. U časového slotu spravujete účastníky po slotech v dialogu **Upravit účastníky** (viz [Jak fungují časové sloty](https://help.happenee.com/cs/articles/29-jak-funguji-casove-sloty)).

Na téže záložce je přepínač **Upozornění účastníkovi při manuálním přiřazení/odebrání**. Když je zapnutý, účastník dostane e-mail, jakmile ho ručně přidáte nebo odeberete. E-mail obsahuje název session, datum a čas a název události; k e-mailu o přidání se přiloží ICS soubor, pokud je zapnuté **Odeslat ICS účastníkovi**. Organizátorovi se o ručních změnách nic neposílá. Přepínač je ve výchozím stavu vypnutý a z typu session se nedědí, takže ho zapínáte u každé session zvlášť; časový slot ho má u každého slotu. Pokud se e-mail nepodaří odeslat, změna se přesto uloží a e-mail čeká na opakované odeslání. Stejný přepínač řídí i e-maily při rušení registrací kvůli skrytí nebo smazání session.

### Uložení, publikace a stav

Při **zakládání** session:

- **Uložit** — session se uloží jako nepublikovaná (zatím ji účastníci nevidí).
- **Uložit a publikovat** — session se uloží a rovnou zveřejní.
- Rozbalovací volby **Uložit a přidat další** / **Publikovat a přidat další** uloží session a hned otevřou prázdný panel pro další — užitečné při zakládání více sessions za sebou.

Při **úpravě** session uložíte tlačítkem **Uložit změny**. Vlevo dole je přepínač **stavu** a tlačítko **Smazat**.

**Stav** řídí, zda je session vidět účastníkům. Má dvě hodnoty:

- **Publikováno** — session je zveřejněná a účastníci ji vidí v programu na microsite i v aplikaci.
- **Skryto** — session není vidět nikde. Hodí se pro rozpracované sessions nebo pro dočasné stažení session, na kterou zatím nikdo není registrovaný. Skrytím session s registracemi o ně přijdete, viz další oddíl.

### Skrytí a smazání session s registracemi

Kdyby registrace na skrytou nebo smazanou session v systému zůstaly, účastník by session neviděl, ale registrace by mu dál mohla bránit v přihlášení na jinou session ve stejném čase. Happenee proto session s registrovanými účastníky neskryje ani nesmaže, dokud jejich registrace nezrušíte.

Když u publikované session přepnete stav na **Skryto** a uložíte, nebo když session smažete, zobrazí se potvrzovací dialog s počtem registrovaných účastníků. Stejně se chová hromadná změna stavu na *Skryto* a hromadné smazání. Tlačítkem **Odebrat účastníky a uložit** (u smazání **Odebrat účastníky a smazat**) systém registrace zruší a teprve potom session skryje nebo smaže. Účastníkům zároveň odebere skupiny, do kterých je zařadilo nastavení **Přiřadit účastníka do skupiny po registraci**. Když dialog zavřete, změna se neuloží a registrace zůstanou.

Jestli se účastníci o zrušení dozvědí e-mailem, řídí přepínač **Upozornění účastníkovi při manuálním přiřazení/odebrání** na záložce **Účastníci**. Dialog před potvrzením vypíše, kolika účastníkům e-mail odejde a kolika ne. Kdo e-mail nedostane, o zrušení neví, takže mu dejte vědět sami.

Zrušené registrace se po opětovném publikování session nevrátí. Stejný dialog se objeví i při skrytí typu, na jehož sessions jsou registrace (viz [Jak fungují typy sessions](https://help.happenee.com/cs/articles/27-jak-funguji-typy-sessions)), a při deaktivaci časového slotu (viz [Jak fungují časové sloty](https://help.happenee.com/cs/articles/29-jak-funguji-casove-sloty)).

### Vyhledávání a filtrování v seznamu

Seznam sessions má nad sebou pole **Hledat sessions** a sadu filtrů: **Den**, **Typ**, **Blok**, **Místo**, **Štítky** a **Stav**. Filtry lze kombinovat (například *Den 20. 03.* + *Typ Workshop*) a zobrazené výsledky tak zúžit. Aktivní filtry zrušíte tlačítkem **Vymazat filtry**.

Sloupce seznamu — **Den**, **Čas**, **Název session**, **Typ**, **Blok**, **Místo**, **Štítky**, **Viditelnost** a **Stav** — jsou řaditelné. Sloupec **Viditelnost** ukazuje, zda má session viditelnost převzatou z typu (*Výchozí*), nebo vlastní; sloupec **Stav** ukazuje *Publikováno*, nebo *Skryto*.

### Hromadné akce

V seznamu zaškrtněte víc sessions (nebo všechny přes zaškrtávátko v záhlaví) a použijte panel hromadných akcí:

- **Blok** — přiřadit nebo změnit registrační blok (volba *—* blok odebere).
- **Místo** — přiřadit nebo změnit místo.
- **Štítky** — přidat nebo odebrat štítky.
- **Stav** — hromadně změnit na *Publikováno*, nebo *Skryto*.
- **Smazat** — smazat vybrané sessions.

Hromadná akce mění **jen zvolený atribut**, ostatní nastavení sessions nechává beze změny. U změny i u smazání systém zobrazí potvrzovací dialog. Jsou-li na vybraných sessions registrace, dialog u změny stavu na *Skryto* i u smazání uvede jejich celkový počet a systém změnu provede až po jejich zrušení (viz *Skrytí a smazání session s registracemi*). Hromadné akce se hodí při přerovnání tracků, přesunu sessions mezi sály nebo když po změně nastavení typu potřebujete srovnat už existující sessions (změna typu se totiž do stávajících sessions sama nepropíše).

### Kopírování session

Existující session lze zkopírovat. Hodí se to, když se nová session od nějaké stávající liší jen v pár údajích — jiný čas, jiné místo, jiný řečník. Tlačítko **Kopírovat** je na dvou místech: v řádku session v seznamu a v panelu **Upravit session**.

Po kliknutí se otevře panel **Nová session** s předvyplněným nastavením původní session a s kurzorem rovnou v poli **Název session**. Název je předvyplněný ve tvaru **{Původní název} (Kopie)** — přepište ho hned, ať v programu nezůstane session se slovem *Kopie* v názvu.

Má-li původní session přiřazené řečníky, moderátory nebo partnery, zeptá se systém dialogem **Kopírovat řečníky a partnery?**, jestli je má přenést také. **Ano, zkopírovat** je do kopie přidá, **Ne, bez nich** vytvoří kopii bez nich. Ostatní nastavení se předvyplní bez ptaní.

Kopie je samostatná nová session — než ji uložíte, projděte si zejména **datum, začátek a konec**, aby vám v programu neležela přes původní session.

### Import

Sessions lze zakládat i hromadně z Excelu přes záložku **Import** v Programu. Import vytváří nové sessions, neupravuje existující — na hromadnou úpravu už založených sessions slouží hromadné akce výše. Podrobnosti v článku [Hromadný import sessions](https://help.happenee.com/cs/articles/68-hromadny-import-sessions).

## Na co si dát pozor

### Session je uložená, ale účastníci ji nevidí

Tlačítko **Uložit** session jen uloží, nezveřejní ji — zůstává nepublikovaná. Aby ji účastníci viděli, použijte **Uložit a publikovat**, nebo u uložené session přepněte stav na **Publikováno**. Zkontrolujte sloupec **Stav** v seznamu.

### Přepnutí na *Vlastní* odpojí session od typu

Jakmile u session přepnete registraci, viditelnost nebo engagement na **Vlastní**, přestane se na ni vztahovat nastavení typu. Pozdější změna na úrovni typu se do takové session **nepropíše**. Pokud chcete, aby session sledovala typ, nechte přepínač na **Výchozí**.

### Některá pole jsou po první registraci zamčená

Po registraci prvního účastníka na session typu Časový slot už nelze měnit typ, čas začátku a konce ani délku slotu; u registračních typů nejde přepínat ani **Výchozí / Vlastní** nastavení registrace. Tato rozhodnutí udělejte **před** spuštěním registrace. Viz [Jak fungují časové sloty](https://help.happenee.com/cs/articles/29-jak-funguji-casove-sloty).

### Hromadná změna místa nebo bloku přepíše stávající hodnoty

Hromadná akce nastaví zvolené místo nebo blok u **všech** vybraných sessions a přepíše to, co měly dosud. Před potvrzením zkontrolujte, které sessions máte zaškrtnuté.

### U kopírování platí volba o řečnících a partnerech pro všechny naráz

Dialog **Kopírovat řečníky a partnery?** je jeden dotaz za celou session — nevybíráte jednotlivé lidi. Když zvolíte **Ne, bez nich** a přiřazení přece jen potřebujete, doplňte ho v kopii ručně na záložkách **Řečníci** a **Partneři**.

### Smazání session je nevratné a skrytí registrace nezachrání

Smazání (jednotlivé i hromadné) sessions trvale odstraní. Stav **Skryto** přitom není způsob, jak registrace zachovat: u session s registrovanými účastníky vede ke stejnému potvrzovacímu dialogu a po potvrzení registrace zruší stejně jako smazání. Session bez registrací můžete skrýt a později znovu publikovat bez ztráty dat.

### „Zmizely mi sessions" — bývá to aktivní filtr

Pokud v seznamu nevidíte sessions, které tam mají být, zkontrolujte filtry nad seznamem. Aktivní filtr (například *Stav* nebo *Den*) zobrazuje jen část sessions — zrušíte ho tlačítkem **Vymazat filtry**.

### Popis vs Poznámka organizátora

**Popis** (záložka Obsah) se zobrazuje účastníkům v detailu session. **Poznámka organizátora** (záložka Informace) je interní a účastníci ji nevidí. Nepište veřejné informace do poznámky a naopak.

## Související články

- [Sestavení programu události — architektura](https://help.happenee.com/cs/articles/26-sestaveni-programu-udalosti-%E2%80%94-architektura)
- [Jak fungují typy sessions](https://help.happenee.com/cs/articles/27-jak-funguji-typy-sessions)
- [Nastavení workshopů a registrace na sessions](https://help.happenee.com/cs/articles/28-nastaveni-workshopu-a-registrace-na-sessions)
- [Jak fungují časové sloty](https://help.happenee.com/cs/articles/29-jak-funguji-casove-sloty)
- [Jak fungují registrační bloky, místa a štítky](https://help.happenee.com/cs/articles/31-jak-funguji-registracni-bloky-mista-a-stitky)
- [Správa řečníků](https://help.happenee.com/cs/articles/23-sprava-recniku)
- [Hromadný import sessions](https://help.happenee.com/cs/articles/68-hromadny-import-sessions)
- [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti)

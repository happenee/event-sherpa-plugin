# Vytvoření a odeslání e-mailové kampaně

> Modul pro hromadné e-mailové oslovení s cílením na skupiny a stavy, plánováním rozesílky a sledováním doručitelnosti.

- Článek v Help Centru: https://help.happenee.com/cs/articles/41-vytvoreni-a-odeslani-e-mailove-kampane
- English version: https://help.happenee.com/en/articles/41-creating-and-sending-an-e-mail-campaign
- Kolekce: Komunikace a pozvánky
- Aktualizováno: 2026-09-23

---

> [!info] Krátce
> E-mailová kampaň slouží pro **hromadné oslovení kontaktů a účastníků** přiřazených k události — remindery, follow-upy, segmentovaná sdělení, vstupenka v den události, zkrátka všechno kromě úvodního zvacího e-mailu. Na rozdíl od zvacího e-mailu umí cílit podle skupin a stavů, plánovat odeslání na konkrétní datum a čas a používat vlastní obrázek hlavičky. Jedna kampaň přitom není jedno odeslání — drží **historii jednotlivých rozesílek** a umí kampaň doposlat kontaktům, které k události přibyly později. Naplánovanou rozesílku můžete **zrušit** (kampaň i obsah zůstanou) a celou kampaň **smazat** (nevratně, včetně statistik rozesílky); odeslanou kampaň už ale vzít zpět nejde — opravuje se kopií.

## Jak začít

- Rozhodněte, **co chcete poslat a komu** — reminder všem, info jen pro VIP, dopozvánka těm bez reakce, ranní vstupenka v den události.
- Připravte obsah **ve všech jazycích události** — dokud některému jazyku chybí předmět nebo obsah, kampaň nepůjde odeslat ani naplánovat (viz níže).
- Rozhodněte, zda kampaň převezme **obrázek hlavičky podle nastavení události**, nebo dostane **vlastní obrázek hlavičky** jen pro sebe.
- Než kampaň odešlete, pošlete si **zkušební kampaň** — po odeslání se už obsah upravit nedá.
- Pokud kampaň míří na konkrétní termín, **naplánujte rozesílku** místo okamžitého odeslání.

## Detail

### Kde e-mailové kampaně najdete

V levém menu události → modul **E-mailové kampaně**. Modul má dvě záložky: **Kampaně** (seznam kampaní této události) a **Rozesílky** s číslem v odznaku — souhrn všech rozesílek napříč kampaněmi.

V seznamu kampaní je u každé vidět **Název kampaně**, **Předmět e-mailu**, **Cílení**, **Stav rozesílky** (*Nenaplánováno* u kampaně, která ještě nešla ven, *Naplánováno* u kampaně čekající na termín, *Odesláno* po rozeslání) a **Datum rozesílky**. Vpravo je tlačítko **Upravit**, vedle něj ikona **…**, která rozbaluje nabídku **Kopírovat**, **Zrušit rozesílku** a **Smazat kampaň**; u odeslané kampaně je navíc **E-maily**. Obě červené položky nabídky zasahují do rozesílky — rozdíl mezi nimi je popsaný níže v sekci *Zastavení, změna a smazání kampaně*.

### Založení nové kampaně

Tlačítkem **Nová kampaň** otevřete dialog, který se ptá na dvě povinné věci:

- **Název kampaně** — interní identifikátor pro orientaci v administraci. Účastník ho nikdy nevidí, takže ho pojmenujte tak, abyste kampaň za tři měsíce našli: *Reminder týden předem* je lepší než *Kampaň 3*.
- **Předmět e-mailu** — to, co adresát uvidí ve schránce.

Obojí jde později změnit — název na záložce **Nastavení**, předmět na záložce **Obsah**.

### Jak je detail kampaně poskládaný

Detail kampaně má čtyři záložky v tomto pořadí:

- **Obsah** — předmět, tělo e-mailu, registrační tlačítko, zástupné proměnné.
- **Nastavení** — název kampaně, obrázek hlavičky, přílohy, odesílatel a příjemce odpovědi.
- **Odeslání** — zkušební kampaň, cílení, plánování, samotné odeslání.
- **Rozesílky** — historie odeslaných rozesílek, doručitelnost a doposlání nově přiřazeným. Číslo v odznaku u názvu záložky říká, kolik rozesílek už kampaň má.

V hlavičce nad záložkami je vždy vidět **stav kampaně** (*Naplánováno*, *Odesláno*), datum a čas rozesílky a počet příjemců. U kampaně s naplánovanou rozesílkou je pod hlavičkou navíc oranžový pruh s ikonou zámku a textem *U této kampaně je naplánována rozesílka na …* — to je vysvětlení, proč jsou pole na záložce **Obsah** ztlumená a nejdou editovat.

### Obsah kampaně

- **Předmět e-mailu** — povinný.
- **Obsah e-mailu** — tělo e-mailu otevřete tlačítkem **Upravit**. Je to stejný editor jako u zvacího a potvrzovacího e-mailu.
- **Zástupné proměnné** — seznam proměnných, které systém při odeslání nahradí údaji konkrétního účastníka (jméno, název události, datum a čas, místo, QR kód pro vstup a další). Vkládají se do textu jako znaky typu `::UZIVATEL_JMENO::`. Fungují stejně napříč microsite, zvacím e-mailem, potvrzovacím e-mailem i kampaněmi — detail v článku *Jak funguje zvací e-mail*. Pod univerzálními proměnnými najdete navíc **zástupné proměnné k vlastním polím kontaktů** — ty se generují z vlastních polí, která máte ve svém workspace, takže v každém workspace vypadají jinak.

### Registrační tlačítko

U tlačítka volíte tři věci:

- **Text tlačítka** — povinný, formulujete si ho sami.
- **Pozice tlačítka** — *Nad obsahem*, *Pod obsahem*, *Nad i pod obsahem* nebo *Skrýt*. U dlouhého e-mailu dává smysl *Nad i pod obsahem*, aby účastník nemusel scrollovat zpět. U čistě informačního sdělení, kde se nikam neregistruje, zvolte *Skrýt*.
- **Kam má registrační tlačítko vést?** — *Osobní odkaz pro adresáta* (odkaz svázaný s konkrétním kontaktem), *Veřejný odkaz* (adresát zadá libovolný e-mail a pokračuje dál; odkaz lze veřejně sdílet), a u placené události navíc *Individuální vstup zdarma* (adresát se zaregistruje bez nákupu vstupenky).

**Guest list u placené události** dělá volba *Individuální vstup zdarma*: naimportujete 50 kontaktů, pošlete jim kampaň s touto volbou a oni se zaregistrují bez placeného nákupu. Osobní odkaz to neumí — ten u placené události vede na nákup vstupenky. Víc v článku *Osobní a veřejný odkaz: jaký je rozdíl*.

### Nastavení kampaně

- **Obrázek hlavičky** — volba *Podle nastavení události* použije stejnou hlavičku jako zvací e-mail, tedy úvodní obrázek události z **Nastavení události → Nastavení grafiky** (ikonu události s názvem a datem, nebo obrázek, který jste k události nahráli). Při volbě *Vlastní obrázek hlavičky* nahrajete obrázek jen pro tuto kampaň. Hodí se na VIP pozvánku nebo reminder s jiným vizuálem. Doporučená šířka je 1300 px v poměru stran 3:1, formát JPG do 500 kB.
- **Přílohy** — dva samostatné přepínače: **ICS soubor** (po kliknutí přidá událost do kalendáře) a **PDF vstupenka** (vstupenka s QR kódem). Typický scénář pro PDF vstupenku je ranní e-mail v den události.
- **Odesílatel kampaně a příjemce odpovědi** — **Jméno odesílatele**, **e-mail pro odpověď**, **Jméno pro odpověď** a **Společnost**. Toto nastavení je **unikátní pro konkrétní kampaň**, nepřepisuje tedy nastavení události ani workspace.

Úplně na konci záložky **Nastavení** je červeně orámovaná sekce **Smazat kampaň** — viz *Zastavení, změna a smazání kampaně* níže.

### Cílení a odeslání

Na záložce **Odeslání** jsou tři bloky.

**Test kampaně** — zadáte e-mailovou adresu, vyberete jazyk a odešlete si **zkušební kampaň**. Pokud v tomto jazyce chybí předmět nebo obsah, test se neodešle a dialog řekne, co doplnit. Jiný nevyplněný jazyk tento test neblokuje; otestujte proto každý jazyk zvlášť.

**Odeslání kampaně** — tady se rozhoduje, komu a kdy:

- **Cílení** — dropdown se skupinami. Můžete jich vybrat **víc naráz**; každá vybraná skupina se zobrazí jako odstranitelný štítek. Když nevyberete žádnou skupinu, kampaň jde *všem*.
- **Naplánovat** — buď *Rozeslat ihned*, nebo *Naplánovat rozesílku na pozdější datum*. Při plánování zadáváte datum i čas.
- **Odesílací tlačítka** — samotné odeslání spustíte tlačítkem podle stavu účastníků: **Všichni** · **Registrovaní** · **Nepozvaní** · **Bez reakce** · **Nepřečetli zvací e-mail** · **Účastníci na místě** · **Zobrazili webovou aplikaci** · **Nezobrazili webovou aplikaci**. Poslední dvě tlačítka rozlišují, zda si účastník už otevřel webovou aplikaci události, tedy účastnickou aplikaci v prohlížeči. Stav se kombinuje s cílením na skupiny — kliknutí na *Registrovaní* u vybrané skupiny VIP pošle kampaň jen registrovaným VIP.

Před odesláním se objeví potvrzovací dialog s počtem vybraných účastníků. Výsledný počet se od něj může mírně lišit — mezitím se stavy mohou změnit.

**Kontakty přiřazené k události** — přehled, kolik kontaktů spadá do kterého stavu, ještě než kliknete. Pod ním je rozpad **Výchozí jazyk uživatelů**, tedy kolik příjemců má jaký preferovaný jazyk. Je to nejrychlejší kontrola před rozesláním: pokud tu vidíte 40 anglických kontaktů a anglickou verzi jste nevyplnili, víte to včas. Odtud se také prokliknete do sekce **Správa kontaktů a skupin**.

Odesílání velkého množství e-mailů může trvat i několik hodin. Během té doby obsah kampaně neměňte.

### Jedna kampaň, víc rozesílek

Kampaň není jedno odeslání. Je to obálka, která drží **historii rozesílek** — každé spuštění (včetně doposlání nově přiřazeným) zakládá **novou rozesílku**. Najdete je na záložce **Rozesílky** v tabulce se sloupci **Datum rozesílky**, **Počet e-mailů**, **Stav odeslání** a **Akce** (ikona koše a odkaz **E-maily**).

Rozesílka prochází stavem *Probíhá odesílání* a končí jako *Odesláno*. Dokud běží, můžete ji smazat ikonou koše u řádku; po dokončení už ne. Přepínačem **Zobrazit testovací rozesílky** si do tabulky přimícháte i zkušební kampaně, které jste si posílali sami — ve výchozím stavu jsou skryté, aby historii nezaplevelily.

Praktický důsledek: nemusíte pro každou vlnu zakládat novou kampaň. Jedna kampaň „Reminder týden předem“ může mít tři rozesílky podle toho, jak postupně přibývají registrovaní — a všechny je uvidíte pohromadě.

### Doposlání nově přiřazeným

Na záložce **Rozesílky** je panel **Doposlat kampaň nově přiřazeným**. Ukazuje počet **nově přiřazených kontaktů** — tedy těch, které se k události nebo do skupiny dostaly **až po zahájení rozesílky**. Nezáleží na tom, jak přibyly: může je přiřadit organizátor ručně, nebo se zaregistrují sami, případně si koupí vstupenku.

Tlačítkem **Nově přiřazení** kampaň dopošlete jen jim. Původní adresáti ji nedostanou podruhé. Dokud není komu doposílat, zůstává tlačítko neaktivní.

Použití: kampaň odešlete 200 přihlášeným, o týden později se zaregistruje dalších 30 lidí, kliknete na *Nově přiřazení* a kampaň půjde jen těm novým. Zvací e-mail tuto logiku nemá.

### Zastavení, změna a smazání kampaně

Jakmile je kampaň naplánovaná nebo odeslaná, obsah **nejde editovat**. Je to pojistka proti tomu, abyste text měnili ve chvíli, kdy už mohla část rozesílky odejít. Další postup závisí na stavu kampaně:

- **Nenaplánováno** — kampaň ještě nikam nemíří, upravujte ji volně.
- **Naplánováno** — klikněte na **Zrušit rozesílku** (v hlavičce kampaně i v nabídce **…** u řádku v seznamu). Potvrzovací dialog *Zrušit naplánovanou rozesílku?* říká, že e-maily neodejdou a rozesílku můžete naplánovat znovu. Zruší se tedy **jen plánování, kampaň i obsah zůstanou**. Kampaň upravte a **naplánujte rozesílku znovu** — bez toho neodejde vůbec.
- **Probíhá odesílání** — rozesílku, která už běží, zastavíte **ikonou koše u jejího řádku** na záložce **Rozesílky**. Jakmile doběhne do stavu *Odesláno*, ikona zmizí.
- **Odesláno** — už se nedá vrátit. Použijte **Kopírovat kampaň** v hlavičce kampaně, nebo **Kopírovat** v nabídce **…** u řádku v seznamu kampaní. Obojí vytvoří novou kampaň se stejným obsahem a nastavením. Kopie se pojmenuje podle originálu s příponou *- copy* a založí se ve stavu *Nenaplánováno*. Přejmenujte ji, upravte a odešlete jako samostatnou kampaň.

Pozor na dva pojmy, které se snadno pletou: **kampaň** je obálka s obsahem a nastavením, **rozesílka** je jedno konkrétní spuštění. *Zrušit rozesílku* ruší plánování, ikona koše maže jednu rozesílku — a kampaň v obou případech zůstává.

### Smazání kampaně

Celou kampaň smažete dvěma cestami:

- na konci záložky **Nastavení** v červeně orámované sekci **Smazat kampaň**,
- nebo v nabídce **…** u řádku v seznamu kampaní.

Obě cesty vedou na potvrzovací dialog s volbami **Ponechat** a **Smazat kampaň**. Smazáním přijdete o **obsah kampaně, nastavení cílení i statistiky rozesílky** a naplánované e-maily neodejdou. **Akce je nevratná** — kampaň se nikam neodkládá a nejde obnovit.

Kdy má smazání smysl: u testovacích a omylem založených kampaní, u duplicit, které vznikly opakovaným kopírováním, a u kampaní, které jste připravili a nakonec se rozhodli neposílat. Jinými slovy tam, kde vám na obsahu ani na historii nezáleží.

**Kdy sáhnout po něčem jiném:**

- Chcete jen **zastavit odeslání** a kampaň zachovat → *Zrušit rozesílku*, ne mazání.
- Chcete **opravit už odeslanou kampaň** → zkopírujte ji a upravte kopii. Smazat jde i odeslaná kampaň, jenže mazání bere i **statistiky rozesílky** — přišli byste o kompletní historii doručitelnosti: kdo e-mail dostal, komu nedorazil a kdo si ho otevřel. Tato data jsou jediným dokladem o tom, co komu odešlo, a znovu je nezískáte.
- Chcete **uklidit v seznamu** a kampaň má za sebou rozesílky → nechte ji být. Historie odeslaných kampaní je součást reportingu události.

### Sledování doručitelnosti

Blok **Stav rozesílky** na záložce **Rozesílky** ukazuje prstencový graf s rozpadem na **K odeslání**, **Odesílá se**, **Doručeno a nepřečteno**, **Doručeno a přečteno** a **Nedoručeno**. To je první místo, kam se podívat, když si někdo stěžuje, že mu nic nepřišlo — hodnota *Nedoručeno* odliší problém na straně doručování od toho, že si e-mail jen nikdo nepřečetl.

Přes odkaz **E-maily** (u řádku rozesílky i v hlavičce kampaně) se dostanete na **detail po jednotlivých příjemcích** — u každé adresy je vidět, zda byl e-mail odeslán, doručen, otevřen a zda na tlačítko někdo klikl. Řádek se dá rozbalit a zobrazí **náhled e-mailu přesně tak, jak odešel** danému člověku. Tím se dá spolehlivě ověřit, že se proměnné doplnily a že odešla správná jazyková verze.

### Typické use cases

- **Remindery** — „Za týden začíná událost, tady máte program“.
- **Dopozvánka bez reakce** — reaktivace těch, kdo na zvací e-mail nereagovali.
- **Info pro VIP a řečníky** — cíleně jen na jejich skupinu; ostatní tato sdělení nedostanou.
- **Segmentované pozvánky** — kampaň česky pro české kontakty, anglicky pro zahraniční, každá s vlastním obrázkem hlavičky.
- **Ranní e-mail v den události** — vstupenka s QR kódem a krátký text; typicky se odesílá hodinu před otevřením.
- **Follow-up** — poděkování, odkaz na dotazník, fotky, záznam.

### Jazyky

Obsah kampaně vyplňujete v jednom jazyce. Pak přepnete **Jazyk obsahu** v pravém horním rohu na další jazyk události a vyplníte ho taky — předmět, tělo, případně text tlačítka. Každý příjemce dostane kampaň ve svém preferovaném jazyce. Kdo ho nemá vyplněný nebo má jazyk, který není mezi aktivními jazyky události, dostane primární jazyk události.

Kampaň odejde, až když má každý jazyk události vyplněný předmět i obsah. Pokud některý chybí, objeví se po kliknutí na odesílací tlačítko dialog *Kampaň není připravena k odeslání*. Uvede název každého dotčeného jazyka a zda mu chybí předmět e-mailu, obsah e-mailu, nebo obojí. V tu chvíli se nic neodešle ani nenaplánuje. Dialog zavřete tlačítkem **Zavřít**, na záložce **Obsah** chybějící pole doplníte a kampaň odešlete znovu. Stejně to platí pro naplánovanou rozesílku i pro doposlání nově přiřazeným.

Před rozesláním si pošlete zkušební kampaň v každém jazyce zvlášť. Uvidíte, jak e-mail v daném jazyce opravdu vypadá, včetně doplněných proměnných.

## Na co si dát pozor

### Organizátor klikne na odeslání a místo rozesílky se objeví *Kampaň není připravena k odeslání*

Některý jazyk události nemá vyplněný předmět nebo obsah; dialog vypíše jazyk i chybějící pole. Přepněte **Jazyk obsahu** na uvedený jazyk, doplňte chybějící pole a kampaň odešlete znovu. Doplnit je potřeba všechny jazyky události bez ohledu na cílení, tedy i u kampaně určené jen českým kontaktům. Kolika příjemců se který jazyk týká, zjistíte v přehledu **Kontakty přiřazené k události** v rozpadu *Výchozí jazyk uživatelů*.

### Organizátor chce upravit naplánovanou kampaň, ale pole na záložce Obsah jsou needitovatelná

Důvod je v oranžovém pruhu pod hlavičkou: *U této kampaně je naplánována rozesílka na …*. Naplánovanou kampaň **nejdřív odemkněte tlačítkem Zrušit rozesílku** (zruší se jen plánování, obsah zůstane), potom ji upravte. Pozor na druhou půlku: rozesílku je pak nutné **naplánovat znovu**, jinak kampaň neodejde vůbec.

### Organizátor chce zastavit odeslání a smaže celou kampaň

*Zrušit rozesílku* a *Smazat kampaň* jsou dvě různé věci, i když v nabídce **…** stojí hned pod sebou a obě jsou červené. **Zrušit rozesílku** zastaví jen odeslání a kampaň nechá být — text, cílení i nastavení zůstanou a rozesílku můžete naplánovat znovu. **Smazat kampaň** smaže obsah i cílení a nejde to vrátit zpět. Když chcete jen získat čas nebo opravit překlep, sáhněte po *Zrušit rozesílku*.

### Organizátor uklízí seznam kampaní a smaže i odeslané kampaně

**Smazat kampaň** funguje i u odeslané kampaně a nic vás nezastaví — smazání ale bere i **statistiky rozesílky**. U odeslané kampaně tím zmizí kompletní historie doručitelnosti: komu e-mail odešel, komu nedorazil a kdo ho otevřel. Nezískáte ji zpátky a přijdete o jediný doklad, kterým se dá dohledat, co komu odešlo. Odeslané kampaně nechte v seznamu; pokud vadí nepořádek, pomůže spíš důsledné pojmenovávání.

### Organizátor hledá mazání kampaně a v seznamu ho nevidí

V seznamu kampaní je schované pod ikonou **…** vedle tlačítka **Upravit**. Druhá cesta vede přes detail kampaně — úplně dole na záložce **Nastavení** je červeně orámovaná sekce **Smazat kampaň**.

### Organizátor našel překlep v už odeslané kampani a hledá, kde ji opravit

Odeslanou kampaň opravit nelze. Použijte **Kopírovat kampaň** v hlavičce kampaně (v seznamu kampaní je to **Kopírovat** v nabídce **…**), opravte kopii a odešlete ji jako novou kampaň. Cílení nastavte tak, aby opravu dostali jen ti, kterých se týká.

### Organizátor posílá kampaň se vstupenkou ráno v den události a účastníkům nechodí PDF

V nastavení kampaně zapněte přepínač **PDF vstupenka**. Samotný text e-mailu vstupenku sám od sebe nepřikládá.

### Po odeslání kampaně přibudou noví registrovaní a organizátor jim posílá celou kampaň znovu všem, takže ji podruhé dostanou i původní adresáti

Použijte panel **Doposlat kampaň nově přiřazeným** a tlačítko **Nově přiřazení**. Kampaň dostanou jen ti, kdo ji ještě nedostali.

### Organizátor zakládá pro každou vlnu novou kampaň a ztrácí přehled, komu už co odešlo

Jedna kampaň unese víc rozesílek. Historie je na záložce **Rozesílky** — u každé rozesílky vidíte datum, počet e-mailů a stav odeslání. Nová kampaň dává smysl při jiném obsahu, ne při stejném obsahu pro další lidi.

### Organizátor cílí jen stavem (například *Registrovaní*) a chybí mu cílení na skupinu (například jen VIP)

Vyberte skupinu v dropdownu **Cílení** a teprve pak klikněte na tlačítko stavu. Zvací e-mail filtr skupin nemá, proto se pro segmentovaná sdělení volí právě kampaň.

### Účastník tvrdí, že mu e-mail nepřišel, a organizátor nemá čím to ověřit

Otevřete **E-maily** u příslušné rozesílky a najděte adresu. Uvidíte, zda byl e-mail odeslán, doručen a otevřen, a můžete si zobrazit i jeho konkrétní podobu. Stav *Nedoručeno* v prstencovém grafu je jiný problém než nepřečtený e-mail a řeší se jinak.

## Související články

- [Jak funguje zvací e-mail](https://help.happenee.com/cs/articles/39-jak-funguje-zvaci-e-mail)
- [Jak funguje potvrzovací e-mail](https://help.happenee.com/cs/articles/40-jak-funguje-potvrzovaci-e-mail)
- [Kdy použít zvací e-mail a kdy e-mailovou kampaň](https://help.happenee.com/cs/articles/42-kdy-pouzit-zvaci-e-mail-a-kdy-e-mailovou-kampan)
- [Cílení komunikace podle skupin a stavů](https://help.happenee.com/cs/articles/43-cileni-komunikace-podle-skupin-a-stavu)
- [Osobní a veřejný odkaz: jaký je rozdíl](https://help.happenee.com/cs/articles/44-osobni-a-verejny-odkaz-jaky-je-rozdil)
- [Co dělat, když nepřišel e-mail](https://help.happenee.com/cs/articles/58-co-delat-kdyz-neprisel-e-mail)
- [Co dělat, když účastník ztratí registrační odkaz](https://help.happenee.com/cs/articles/59-co-delat-kdyz-ucastnik-ztrati-registracni-odkaz)
- [Interpretace statistik eventu](https://help.happenee.com/cs/articles/50-interpretace-statistik-eventu)
- [Používání oznámení v účastnické aplikaci](https://help.happenee.com/cs/articles/46-pouzivani-oznameni-v-ucastnicke-aplikaci)
- [Co dělat při problému na check-inu](https://help.happenee.com/cs/articles/62-co-delat-pri-problemu-na-check-inu)
- [Zvací e-mail jako save the date](https://help.happenee.com/cs/articles/63-zvaci-e-mail-jako-save-the-date)
- [Komunikační flow v den události](https://help.happenee.com/cs/articles/64-komunikacni-flow-v-den-udalosti)
- [Plánování follow-up komunikace po události](https://help.happenee.com/cs/articles/65-planovani-follow-up-komunikace-po-udalosti)
- [Jak fungují zástupné proměnné](https://help.happenee.com/cs/articles/78-jak-funguji-zastupne-promenne)
- [Sledování doručitelnosti e-mailů a kampaní](https://help.happenee.com/cs/articles/80-sledovani-dorucitelnosti-e-mailu-a-kampani)
- [Co dělat, když kampaň nejde odeslat nebo přišla v jiném jazyce](https://help.happenee.com/cs/articles/88-co-delat-kdyz-kampan-nejde-odeslat-nebo-prisla-v-jinem-jazyce)

# Správa kontaktů a skupin ve workspace

> Centrální databáze workspace pro kontakty a skupiny, sdílená napříč všemi vašimi událostmi.

- Článek v Help Centru: https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace
- English version: https://help.happenee.com/en/articles/11-managing-contacts-and-groups-in-your-workspace
- Kolekce: Nastavení eventu a registrace
- Aktualizováno: 2026-10-26

---

> [!info] Krátce
> Správa kontaktů a skupin je **centrální databáze** ve workspace, sdílená napříč všemi událostmi. Kontakty vkládáte ručně nebo importem z Excelu či CSV, skupiny slouží k cílení komunikace a řízení viditelnosti. Dobře naplánovaná struktura skupin ušetří hodiny práce — špatně naplánovaná znamená ruční přiřazování po stovkách účastníků.

## Jak začít

- Rozhodněte, kolik skupin budete potřebovat a podle jakého klíče. Typické klíče: typ účastníka (VIP, standardní, speaker, partner), zdroj registrace (kdo pozval), workshop/track, firemní příslušnost.
- Skupiny založte **před spuštěním registrace** — ne během ní.
- Kontakty můžete přidat ručně nebo hromadně importem z Excelu či CSV. Import rovnou zařadí kontakty do skupin, vyplní vlastní pole a preferovaný jazyk, případně je přiřadí k události, a před zápisem vám ukáže, co se stane.
- Přiřazení kontaktu k události je samostatný krok od jeho vytvoření ve workspace.

## Detail

### Kde se správa kontaktů a skupin nachází

V levém menu workspace (na úrovni celého účtu, ne uvnitř události) najdete položku **Kontakty a skupiny**. Uvnitř události je ve spodní části menu také odkaz na **Správu kontaktů a skupin** a na přehledu události je v **Nástrojích** tlačítko pro rychlý přístup.

Kontakty jsou **společné pro celý workspace** — stejný kontakt může být přiřazen k libovolnému počtu událostí. Údaje jako jméno, e-mail, telefon, firma, vlastní pole kontaktů a preferovaný jazyk jsou napříč událostmi sdílené.

### Přidání kontaktů

**Po jednom.** Klikněte na **+ Přidat kontakt** a vyplňte údaje. Vhodné při ad-hoc doplnění (například když účastník, který neprošel registrací, potřebuje být přidán ručně).

**Hromadný import ze souboru.** Import najdete na záložce **Import** ve Správě kontaktů a skupin. Průvodce má čtyři kroky: **Nahrání**, **Mapování**, **Kontrola** a **Import**. Do databáze se nic nezapíše, dokud v kroku Kontrola nekliknete na **Potvrdit a importovat**, takže si průchod můžete vyzkoušet nanečisto.

1. **Připravte soubor.** Tlačítkem **Stáhnout šablonu** získáte Excel se sloupci Jméno, Příjmení, Společnost, IČO, E-mail, Telefon, Pracovní pozice a Jazyk a s ukázkovým sloupcem skupiny a vlastního pole. Šablona ale není podmínkou: nahrát můžete i vlastní export z jiného systému (xls, xlsx nebo csv) a sloupce přiřadíte v kroku Mapování. Jediný povinný údaj je e-mail.
2. **Skupiny a vlastní pole zapište do hlavičky.** Sloupec s názvem `#VIP` zařadí do skupiny *VIP* každý kontakt, který má v tom sloupci cokoli vyplněného (třeba `ano`). Když máte skupiny v jednom sloupci jako text (`VIP, Speakers`), namapujete ho v dalším kroku na **Skupiny z hodnoty**; názvy oddělujte čárkou, středníkem nebo svislítkem. Vlastní pole kontaktu má sloupec `*Název pole`. Skupinu ani vlastní pole nemusíte zakládat předem, import je vytvoří.
3. **Nahrání.** Vyberte soubor a zvolte **Režim importu** (viz níže). **Volitelné přiřazení k události** přiřadí všechny importované kontakty k vybrané události, takže to nemusíte dělat zvlášť. **Výchozí jazyk nových účastníků** se použije u řádků, kde jazyk chybí nebo mu Happenee nerozumí. Pokračujte tlačítkem **Nahrát a načíst**.
4. **Mapování.** V tabulce vidíte každý sloupec souboru, ukázku hodnot a pole kontaktu, na které se má mapovat. Návrh vzniká podle názvů sloupců a rozumí českým i anglickým hlavičkám (*Příjmení* i *Last name*). Zkontrolujte ho, sloupce, které importovat nechcete, nechte na **Přeskočit**, a pokračujte tlačítkem **Zkontrolovat import**. Bez sloupce namapovaného na e-mail průvodce dál nepustí.
5. **Kontrola.** Happenee projde všechny řádky a ukáže souhrn: kolik řádků je v pořádku, kolik má chybu, kolik je duplicitních, kolik kontaktů vznikne nově a kolik jich už existuje, kolik přiřazení skupin, hodnot vlastních polí a přiřazení k události import provede. Pod souhrnem je seznam **Nově vytvořené skupiny** a tabulka **Problémové řádky** s číslem řádku, e-mailem, stavem a popisem problému. Tlačítko **Stáhnout report** dá CSV se stavem každého řádku. Pokud chcete soubor opravit, upravte ho a nahrajte znovu; rozpracovaný import nic nezapsal. Jinak potvrďte tlačítkem **Potvrdit a importovat**: řádky s chybou a duplicitní řádky se přeskočí, ostatní se importují.
6. **Import.** Sledujete průběh a výsledek: kolik kontaktů bylo vytvořeno, aktualizováno, přiřazeno k události, přeskočeno a u kolika import selhal. Report jde stáhnout i tady. Každý dokončený import se objeví v **Historii importů** pod průvodcem, včetně reportu.

**Režim importu** rozhoduje, co se stane s kontakty, které už ve workspace jsou (poznají se podle e-mailu):

- **Doplňujeme data** (výchozí) — existující kontakty nechá být, doplní jim jen chybějící preferovaný jazyk a prázdná vlastní pole. Nové kontakty založí.
- **Přepisujeme data neprázdnými hodnotami** — u existujících kontaktů přepíše jméno, společnost, telefon a další údaje hodnotami ze souboru. Prázdná buňka nic nemaže.

V obou režimech se skupiny jen přidávají; import kontakt ze žádné skupiny neodebere. E-mail se nikdy nepřepisuje, je to klíč, podle kterého se kontakty párují.

Kontrola označí jako **chybu** chybějící nebo neplatný e-mail, víc než 20 skupin v jedné buňce a název skupiny delší než 100 znaků. **Duplicita** je stejný e-mail podruhé v témže souboru; importuje se jen první řádek. Řádek bez jazyka projde, jen dostane výchozí jazyk. Soubor může mít nejvýš 20 000 řádků a 50 MB, hlavička s e-mailem musí být v prvních 100 řádcích a buňky se vzorci potřebují uloženou hodnotu (soubor uložte v Excelu, nebo vzorce nahraďte hodnotami).

Preferovaný jazyk je při importu důležitý, protože se podle něj řídí odesílání zvacího e-mailu a e-mailových kampaní. Vyplňte sloupec Jazyk dvoupísmenným kódem (`cs`, `en`); Happenee přijme i tvary jako *čeština* nebo *english*. Kde jazyk chybí, doplní se **Výchozí jazyk nových účastníků** z kroku Nahrání; už vyplněný jazyk existujícího kontaktu se tím nepřepíše.

### Tabulka kontaktů: vyhledávání, sloupce a filtry

Tabulku kontaktů si přizpůsobíte tomu, co zrovna řešíte:

- **Vyhledávání** — pole **Hledat kontakty** hledá podle jména, e-mailu, události nebo skupiny. Když zadáte název události, dostanete seznam kontaktů přiřazených k té události.
- **Sloupce** — tlačítkem **Sloupce** otevřete panel **Nastavení sloupců** a zaškrtnete, co chcete v tabulce vidět. **Příjmení a jméno** a **E-mail** jsou vždy zapnuté a nelze je vypnout; volitelně přidáte Události, Skupiny, Společnost, IČO, Telefon, Pozice a vaše vlastní pole kontaktů. Výběr potvrdíte tlačítkem **Použít**. Kliknutím na šipky v hlavičce sloupce řadíte.
- **Filtry** — nad tabulkou se zobrazí filtry odpovídající **zapnutým sloupcům**: jakmile přidáte sloupec Společnost, přibude i filtr podle společnosti. Filtry kombinujete a celý výběr zrušíte tlačítkem **Zrušit filtry**.

Sloupce a filtry jsou propojené záměrně — co si zobrazíte jako sloupec, podle toho můžete rovnou filtrovat. Hodí se to před hromadnou akcí: vyfiltrujete si přesně ty kontakty, kterých se má akce týkat (například podle skupiny nebo firmy), a teprve pak je označíte.

### Přiřazení kontaktu k události

Vytvořením kontaktu ve workspace ho ještě nepřiřadíte k události — to je samostatný krok. Přiřazení řešíte z tabulky kontaktů přes hromadné akce:

- **Označte jeden nebo více kontaktů** zaškrtnutím políčka v řádku — nad tabulkou se objeví lišta hromadných akcí.
- Klikněte na **Přiřazení k události**. Otevře se seznam událostí (dlouhý seznam profiltrujete polem **Filtrovat události**), kde upravíte, ke kterým událostem mají označené kontakty patřit. Volbu potvrdíte tlačítkem **Upravit přiřazení k událostem**.
- **Přes skupinu** — v sekci Skupiny označte skupinu a tlačítkem **Přiřazení k události** ji celou přiřadíte k události jedním krokem; přiřadí se tím všichni její členové.

Jedna akce **Přiřazení k události** tak řeší přidání i odebrání zároveň. Odebrání z události nesmaže kontakt z workspace — zůstává v centrální databázi a jen přestane být navázaný na danou událost.

### Úprava kontaktu

Konkrétní kontakt upravíte přes ikonu tužky v jeho řádku — otevře se **boční panel Upravit kontakt** se čtyřmi záložkami:

- **Základní údaje** — jméno, příjmení, e-mail, společnost, pozice, telefon, IČO, preferovaný jazyk a foto (čtvercové, poměr 1:1).
- **Vlastní pole** — hodnoty vašich vlastních polí kontaktů.
- **Události** — ke kterým událostem je kontakt přiřazen; přiřazení tady přidáte i odeberete.
- **Skupiny** — ve kterých skupinách kontakt je; členství upravíte zaškrtnutím.

Panel funguje jako kompletní karta jednoho kontaktu — údaje, události i skupiny spravujete na jednom místě, bez hromadných akcí. Změny uložíte tlačítkem **Uložit**.

### Smazání kontaktu

Kontakt smažete buď hromadně (označit v tabulce → **Smazat kontakt**), nebo z bočního panelu úprav. Smazat ale lze jen kontakt, který **nemá přiřazené žádné skupiny ani události** — dokud nějaké má, je tlačítko neaktivní a boční panel úprav vysvětlí proč. Nejdříve tedy kontakt odeberte ze všech skupin i událostí, teprve pak ho smažete.

Smazání je nevratné a odebere kontakt z celého workspace. Pokud ho chcete dostat jen z jedné události, nemažte ho — stačí ho z té události odebrat (viz výše).

### Správa skupin

Skupiny se vytvářejí v sekci **Skupiny** (záložka v rámci Kontaktů a skupin).

1. Klikněte na **+ Přidat skupinu** (nebo **Vytvořit novou skupinu**).
2. Zadejte název skupiny (například *VIP*, *Speakers*, *Brno*, *Partner Siemens*).
3. Uložte.

Skupiny jsou **globální pro workspace**. Lokální skupiny (unikátní pro jednu událost) dnes nejsou k dispozici.

### Jak kontakt do skupiny dostat

Tři cesty:

- **Při importu** — sloupcem `#Název skupiny`, nebo sloupcem se seznamem skupin namapovaným na **Skupiny z hodnoty**. Skupina, která ještě neexistuje, se založí.
- **Ručně v tabulce kontaktů** — označit kontakt(y) a použít hromadnou akci **Přidat nebo odebrat ze skupin**; stejnou akcí kontakt ze skupiny i odeberete. Členství u jednoho kontaktu upravíte také v bočním panelu úprav na záložce Skupiny.
- **Automaticky přes registrační formulář** — když účastník odpoví na otázku, přiřadí se podle odpovědi do skupiny. To se nastavuje v registračním formuláři (viz článek *Jak fungují podmíněné otázky v registračním formuláři*).

### K čemu skupiny slouží

Skupiny mají čtyři hlavní použití v Happenee:

- **Cílení komunikace** — e-mailové kampaně lze cílit jen na vybrané skupiny. Zvací e-mail cílení přes skupiny nepodporuje.
- **Řízení viditelnosti** — obsahové funkce (Program, Řečníci, Vlastní obsah) i engagement funkce (Oznámení, Hlasování, Dotazník) lze zobrazit jen vybraným skupinám.
- **Podmínky v registračním formuláři** — otázku i konkrétní odpověď lze zobrazit jen vybraným skupinám. Odpověď může účastníka do skupiny zařadit.
- **Reporting** — statistiky účastníků lze filtrovat podle skupin.

## Na co si dát pozor

### Skupiny se vytvářejí až v momentě, kdy už běží registrace. Organizátor zjistí, že chce cílit komunikaci, ale lidé jsou už ve formuláři zařazeni bez rozlišení

Strukturu skupin naplánujte **před** spuštěním registrace. Zamyslete se, koho budete chtít odlišit, a skupiny založte, aby je registrační formulář mohl automaticky přiřazovat. Ex post se dají skupiny přiřadit hromadně, ale je to ruční práce.

### Import přepsal údaje existujících kontaktů, protože organizátor zvolil **Přepisujeme data neprázdnými hodnotami**, i když chtěl jen doplnit chybějící

Nechte výchozí **Doplňujeme data**: existující kontakty nechá být a skupiny doplní stejně. Přepisování zvolte jen tehdy, když soubor nese novější údaje než workspace. V kroku Kontrola vidíte, kolik existujících kontaktů import zasáhne, a report u každého z nich uvádí upozornění, že bude aktualizován.

### Import založil novou skupinu vedle existující, protože se název lišil překlepem

Skupiny z importu vznikají automaticky a párují se podle názvu bez ohledu na velikost písmen. Překlep v hlavičce sloupce `#` nebo v buňce mapované na Skupiny z hodnoty založí novou skupinu. Před potvrzením projděte seznam **Nově vytvořené skupiny**; když v něm vidíte skupinu, kterou už máte, opravte soubor a nahrajte ho znovu.

### Kontakt uvedený na dvou řádcích skončil jen v části skupin

Stejný e-mail podruhé v souboru označí Kontrola jako duplicitu a druhý řádek přeskočí celý, i se skupinami a údaji, které měl navíc. Před nahráním sloučte řádky se stejným e-mailem do jednoho.

### Kontakt je vytvořen ve workspace, ale není přiřazen k události. Organizátor ho nevidí v registraci ani ho nemůže pozvat

Po vytvoření kontaktu ho vždy přiřaďte k události — jednotlivě, přes skupinu, nebo rovnou při importu volbou **Volitelné přiřazení k události**. Přiřazení je samostatný krok od přidání do workspace.

### Zahraniční hosté dostali českou pozvánku, protože soubor neměl sloupec Jazyk a výchozí jazyk zůstal na češtině

Import jazyk nikdy nenechá prázdný: kde chybí, dosadí **Výchozí jazyk nových účastníků** z kroku Nahrání. U smíšeného seznamu proto vyplňte sloupec Jazyk u každého řádku; u jednojazyčného seznamu stačí správně nastavit výchozí jazyk. Zvací e-mail a e-mailové kampaně se odesílají podle tohoto nastavení.

### Očekávání, že skupina z jedné události bude viditelná jen v ní. Skupiny jsou globální

Skupiny jsou dnes pouze na úrovni workspace. Pokud potřebujete odlišit skupiny pro různé události, pojmenujte je prefixem (*Konference25_VIP*, *Workshop25_Speakers*).

### Tlačítko Smazat kontakt je neaktivní

Kontakt nelze smazat, dokud má přiřazené nějaké skupiny nebo události — Happenee to blokuje, aby smazání nerozbilo data u běžící události. Odeberte kontakt ze všech skupin a událostí (hromadnou akcí, nebo v bočním panelu úprav na záložkách Skupiny a Události). V panelu změny uložte, teprve pak kontakt smažete. Když potřebujete kontakt dostat jen z jedné události, nemažte ho — odeberte ho z té události.

## Související články

- [Co je workspace a co je event](https://help.happenee.com/cs/articles/1-co-je-workspace-a-co-je-event)
- [Orientace v administraci Happenee](https://help.happenee.com/cs/articles/2-orientace-v-administraci-happenee)
- [Co nastavit jako první po vytvoření eventu](https://help.happenee.com/cs/articles/3-co-nastavit-jako-prvni-po-vytvoreni-eventu)
- [Vytvoření nové události](https://help.happenee.com/cs/articles/9-vytvoreni-nove-udalosti)
- [Nastavení primárního jazyka události](https://help.happenee.com/cs/articles/10-nastaveni-primarniho-jazyka-udalosti)
- [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti)
- [Nastavení registračního formuláře](https://help.happenee.com/cs/articles/13-nastaveni-registracniho-formulare)
- [Jak fungují podmíněné otázky v registračním formuláři](https://help.happenee.com/cs/articles/14-jak-funguji-podminene-otazky-v-registracnim-formulari)
- [Správa ubytování a výběru spolubydlícího](https://help.happenee.com/cs/articles/16-sprava-ubytovani-a-vyberu-spolubydliciho)
- [Jak fungují nominace a nominátoři](https://help.happenee.com/cs/articles/17-jak-funguji-nominace-a-nominatori)
- [Cílení komunikace podle skupin a stavů](https://help.happenee.com/cs/articles/43-cileni-komunikace-podle-skupin-a-stavu)
- [Jak funguje Networking](https://help.happenee.com/cs/articles/36-jak-funguje-networking)
- [Jak funguje zvací e-mail](https://help.happenee.com/cs/articles/39-jak-funguje-zvaci-e-mail)
- [Kdy použít zvací e-mail a kdy e-mailovou kampaň](https://help.happenee.com/cs/articles/42-kdy-pouzit-zvaci-e-mail-a-kdy-e-mailovou-kampan)
- [Jak funguje check-in a skenování QR kódů](https://help.happenee.com/cs/articles/47-jak-funguje-check-in-a-skenovani-qr-kodu)
- [Tisk jmenovek](https://help.happenee.com/cs/articles/48-tisk-jmenovek)
- [Příprava dat pro ubytovatele](https://help.happenee.com/cs/articles/49-priprava-dat-pro-ubytovatele)
- [Co dělat, když skupiny nebo viditelnost nefungují](https://help.happenee.com/cs/articles/61-co-delat-kdyz-skupiny-nebo-viditelnost-nefunguji)
- [Jak fungují vlastní pole kontaktů](https://help.happenee.com/cs/articles/76-jak-funguji-vlastni-pole-kontaktu)
- [Ruční přidání účastníka do události](https://help.happenee.com/cs/articles/77-rucni-pridani-ucastnika-do-udalosti)
- [Partnerské API klíče](https://help.happenee.com/cs/articles/95-partnerske-api-klice)
- [Nastavení placených vstupenek](https://help.happenee.com/cs/articles/18-nastaveni-placenych-vstupenek)

# Jak funguje check-in a skenování QR kódů

> Odbavení účastníků v servisní aplikaci (skenování QR i seznam podle jména a Kiosk režim) a ve webovém Check-inu (Prezenci).

- Článek v Help Centru: https://help.happenee.com/cs/articles/47-jak-funguje-check-in-a-skenovani-qr-kodu
- English version: https://help.happenee.com/en/articles/47-how-check-in-and-qr-code-scanning-work
- Kolekce: Den události a provoz na místě
- Aktualizováno: 2026-11-04

---

> [!info] Krátce
> **Check-in (odbavení na místě)** je okamžik, kdy účastník fyzicky dorazí a vy zaznamenáte jeho příchod. Happenee ho řeší dvěma cestami — mobilní **servisní aplikací (Happenee Service App)** na telefonu nebo tabletu a webovým nástrojem **Check-in (Prezence)** v administraci. Servisní aplikace má dva režimy: **Režim obsluhy** (personál skenuje QR kódy *nebo* odbavuje přímo ze **seznamu účastníků** podle jména) a **Kiosk režim** (samoobslužný check-in, účastník si naskenuje vstupenku sám). Odbavení trvá pod sekundu, umí přes Bluetooth tisknout jmenovky a sleduje příchody v reálném čase. Nastavení odbavení otevřete v levém menu administrace události pod **Odbavení na místě**, a to i bez aktivního modulu QR vstupenky. Skupiny zobrazované po skenu i v detailu účastníka vybíráte v nastavení odbavení; účastník je musí mít přiřazené.

## Jak začít

- Nastavení odbavení otevřete v levém menu administrace události přes **Odbavení na místě**. Položka je dostupná i bez aktivního modulu QR vstupenky, takže kvůli nastavení odbavení nemusíte účastníkům zapínat QR vstupenku v aplikaci.
- Rozhodněte, **kolik míst pro odbavení** budete mít (jeden vstup, víc vstupů, šatna, workshop, bus) a jaký **typ chování** má každé místo — viz *Typy míst pro odbavení* níže.
- Rozhodněte, **které skupiny** chcete při skenování zobrazit (VIP, řečník, typ vstupenky) a jestli se mají ukazovat všude, nebo jen na vybraných místech — nastavte je předem v sekci odbavení v administraci.
- Objednejte si u **customer success** účty pro personál, pokud bude mít obsluha vlastní přihlášení nad rámec administrátora — není to samoobslužné, domluvte je s předstihem.
- Stáhněte si **servisní aplikaci Happenee Service App** — pro iOS z [App Store](https://apps.apple.com/cz/app/happenee-service-app/id6499516161), pro Android z [Google Play](https://play.google.com/store/apps/details?id=com.happenee.serviceapp2&hl=cs). Přihlaste se a otestujte: vyberte událost, zvolte **Režim obsluhy** nebo **Kiosk režim**, **Místo check-inu** a spárujte tiskárnu (viz [Tisk jmenovek](https://help.happenee.com/cs/articles/48-tisk-jmenovek)).
- Pro účastníky bez QR kódu, kterým je potřeba znovu poslat vstupenku nebo zobrazit QR, mějte u vstupu připravený i webový **Check-in (Prezenci)** — viz níže.

## Detail

### Dvě prostředí pro odbavení

**Servisní aplikace (Happenee Service App)** — mobilní nástroj pro obsluhu na telefonu nebo tabletu. Skenuje QR kódy, odbavuje účastníky ze seznamu podle jména, tiskne jmenovky a zvládne i samoobslužný režim. Přihlašuje se pod administrátorským účtem; pro samostatné **účty pro personál** kontaktujte customer success.

**Check-in (Prezence)** — webový nástroj v administraci události (UI label *Check-in*). Otevřete ho z nástrojů události na počítači. Zvládá ruční odbavení a navíc dvě věci, které servisní aplikace zatím neumí: **znovu odeslat vstupenku e-mailem** a **zobrazit QR kód rovnou na obrazovce**. Proto má u vstupu pořád své místo (viz *Účastník bez QR kódu* níže).

### Spuštění servisní aplikace: režim, místo, tiskárna

Po přihlášení vyberete událost ze seznamu. U události zvolíte **režim** a **místo**:

- **Režim obsluhy** (*„Skenování QR kódů“*) — obsluhuje personál. Skenuje QR i odbavuje ze seznamu.
- **Kiosk režim** (*„Samoobslužný check-in“*) — bezobslužné stanoviště, účastník se odbaví sám.
- **Místo check-inu** — vyberete jedno z míst nastavených v administraci (každé má svůj typ chování, viz níže). Aplikace ukazuje názvy míst, ne jejich typy.
- **Tiskárna** — volitelně spárujete tiskárnu jmenovek (viz [Tisk jmenovek](https://help.happenee.com/cs/articles/48-tisk-jmenovek)). Bez ní check-in funguje, jen se netiskne.

Volbu potvrdíte tlačítkem **Pokračovat**. Režim i místo jdou kdykoli přepnout (přes přepnutí události v *Nastavení* nebo zpět na výběr).

### Režim obsluhy — záložka Sken

Spodní záložka **Sken** je klasický QR skener (*„Naskenujte QR kód účastníka“*). Skenuje QR z potvrzovacího e-mailu, z PDF vstupenky nebo z modulu **QR vstupenka** v účastnické aplikaci. Po každém skenu aplikace ukáže výsledek:

- **úspěšné odbavení** — a u připojené tiskárny rovnou nabídne tisk jmenovky,
- **upozornění, že účastník už dorazil** (duplicitní sken na místě typu *Příchod*) — s možností otevřít jeho detail,
- **neplatný kód** — s možností účastníka rovnou **zadat ručně**.

Nahoře běží počítadlo **Dnes odbaveno**, dole je historie **Poslední skeny** a stav tiskárny (*„Není připojená žádná tiskárna“*, dokud ji nespárujete).

### Režim obsluhy — záložka Účastníci (odbavení podle jména)

Spodní záložka **Účastníci** je **živý seznam** všech účastníků události — tady odbavíte i člověka, který nemá QR kód po ruce. Umí:

- **Hledat** podle jména nebo e-mailu a filtrovat rychlými přepínači **Vše / Odbaveno / Čeká** (plus řazení a filtr podle skupiny).
- **Swipnutím řádku** rovnou odbavíte (akce **Odbavit**) nebo vytisknete jmenovku (akce **Tisknout jmenovku**) — bez otevírání detailu.
- **Přidat účastníka** — hosta bez registrace, který v seznamu není, založíte přímo v aplikaci (e-mail, jméno, příjmení, firma, pozice, tagy). Po uložení ho lze odbavit a vytisknout mu jmenovku.
- Otevřít **Detail účastníka** s tlačítky **Odbavit** a **Tisk badge** (tisk jmenovky na vyžádání), s **Poznámkou** organizátora, sekcí **Detaily** (s úpravou přes **Upravit účastníka**), přehledem **Místa check-inu** (kde a kdy už byl odbaven, kým, a pořadovým číslem skenu) a historií **Scany v tomto eventu**.

U každého účastníka vidíte jeho **RSVP status** (*Zúčastní se* / *Bez odpovědi*) a **check-in status** (*Odbaveno* / *Nedorazil*).

### Typy míst pro odbavení

Jedno odbavení nemusí stačit. Na větší události skenujete na více místech — vstup do areálu, šatna, výdej občerstvení, kontrola u workshopu. Každé **místo** má v administraci přiřazený **typ** podle chování, které potřebujete:

- **Příchod** — klasický vstup. Po naskenování je účastník *Odbaven*. Druhý sken stejného QR ohlásí, že už dorazil. *(Hlavní vstup do areálu.)*
- **Odchod** — opuštění areálu nebo části události. Stav se přepne na *Odešel*, záznam o příchodu zůstává; přes *Příchod* lze znovu odbavit. *(Odchod z večírku, ukončení bloku.)*
- **Kontrola jednorázově** — jednorázové ověření; další pokus ohlásí, že kontrola už proběhla. *(Výdej voucheru, dárku.)*
- **Kontrola opakovaně** — opakované skenování bez omezení. *(Vstup do zóny, nástup do autobusu, docházka.)*

Typy lze na jedné události kombinovat. Obsluha v servisní aplikaci volí, **u jakého místa** zrovna stojí.

### Zobrazení skupiny při skenování

V administraci události otevřete **Odbavení na místě** a v nastavení **Zobrazení skupiny po naskenování účastníka** vyberte skupiny, které má obsluha vidět (například *VIP*, *Řečník*, *Standard*). Stejný výběr řídí zobrazení skupin po skenu i v **Detailu účastníka** v servisní aplikaci. Zobrazí se pouze vybrané skupiny, které má daný účastník přiřazené. Ostatní skupiny z workspace se automaticky nezobrazují; samotné vytvoření skupiny nebo její přiřazení kontaktu nestačí. Bez výběru skupin se žádné z těchto označení nezobrazí.

Při skenování můžete zobrazení skupiny omezit na vybraná **místa** (pole *Zobrazit na místech*). Prázdný výběr znamená všechna místa. V **Detailu účastníka** se toto omezení na místa neuplatňuje: zobrazí se všechny jeho skupiny vybrané k zobrazení, bez ohledu na aktuálně zvolené místo check-inu.

Omezení na místa využijete tam, kde obsluha nemá po skenu vidět všechno. U hlavního vstupu dává smysl *VIP* a *Řečník*, u dveří do sálu jen skupina, která na něj má nárok.

Skupiny se plní ručně (ve správě kontaktů, při importu) nebo automaticky (přiřazením ke vstupence, odpovědí ve formuláři, přihlášením na workshop, slevovým kódem). Detail v článku [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti).

### Kiosk režim — samoobslužný check-in

V **Kiosk režimu** se účastník odbaví sám. Režim je uzpůsobený pro **zobrazení na tabletu** umístěném na stojanu u vstupu: aplikace ukazuje výzvu, ať si účastník přiloží QR kód ke kameře; po úspěšném načtení potvrdí jeho jméno (a u placené události typ vstupenky a doprovod), automaticky vytiskne jmenovku a po pár sekundách se vrátí ke skeneru pro dalšího. Když sken neprojde, vyzve účastníka, ať se obrátí na obsluhu.

Hodí se tam, kde chcete snížit fronty u personálu. Vyžaduje spolehlivou tiskárnu, stabilní stojan na tablet a jednoduchou instrukci u stanoviště.

### Workshop nebo session — zatím přes skupiny

Samostatné odbavení **na konkrétní workshop** nebo **časový slot** Happenee přímo neumí — servisní aplikace odbavuje per *místo*, ne per session. Řešíte to přes **skupiny**: účastník přihlášený na workshop je automaticky ve skupině daného workshopu, tu nastavíte k zobrazení při skenování a omezíte ji jen na místo u dveří workshopu, kterému dáte typ *Kontrola opakovaně*; obsluha pak podle skupiny vidí, jestli má účastník přístup. Přímé odbavení workshopu s vlastním seznamem účastníků je v přípravě.

### Účastník bez QR kódu

Část lidí QR kód po ruce mít nebude (smazali e-mail, nestáhli aplikaci, registrovali se teď). Většinu z nich teď odbavíte **přímo v servisní aplikaci** — v záložce **Účastníci** je najdete podle jména a odbavíte, nebo přes **Přidat účastníka** založíte hosta bez registrace.

Webový **Check-in (Prezenci)** mějte u vstupu pro případy, které aplikace neumí: **znovu odeslat vstupenku e-mailem** a **zobrazit QR kód na obrazovce** (účastník nebo sousední stanoviště ho pak naskenuje). Detail postupu v článku [Co dělat, když účastník bez QR stojí ve frontě](https://help.happenee.com/cs/articles/66-co-delat-kdyz-ucastnik-bez-qr-stoji-ve-fronte).

### Export skenování

Z nastavení odbavení v administraci lze exportovat **seznam všech skenů** (kdo, kdy, na kterém místě) a **statistiky účastníka** (kdo dorazil, kdo ne, opakované skeny). Hodí se pro reporting po události a kontrolu provozu.

## Na co si dát pozor

### Na startu se vybere špatný režim nebo místo a odbavení se zapisuje jinam, než obsluha čeká

Před prvním účastníkem zkontrolujte, že máte zvolený správný **režim** (*Režim obsluhy* vs *Kiosk režim*) a hlavně správné **Místo check-inu** — sken se započítá k tomu místu, které je vybrané. U více vstupů přiřaďte každé obsluze její místo a typ (hlavní vstup = *Příchod*, opakovaná zóna = *Kontrola opakovaně*, jednorázový výdej = *Kontrola jednorázově*).

### Obsluha přijde na událost a nemůže se do servisní aplikace přihlásit pod vlastním účtem

Účty pro personál zapíná customer success, není to samoobslužné. Domluvte je **s předstihem** — minimálně týden. Jako nouzovku lze obsluhu přihlásit pod administrátorským účtem, ale pak nemáte oddělený audit, kdo koho odbavil.

### Organizátor čeká, že při skenování uvidí, kdo je ve které skupině, ale nezobrazí se nic

Ověřte, že má účastník skupinu přiřazenou a že je skupina vybraná k zobrazení v nastavení odbavení. Tento výběr platí i pro **Detail účastníka** v servisní aplikaci. Pokud skupina chybí pouze ve výsledku skenu, zkontrolujte také její omezení na místa; v detailu účastníka se omezení na místa neuplatňuje.

### Organizátor chce odbavovat konkrétní workshop podle jeho seznamu a hledá tu funkci

Dnes to není nativní funkce — řeší se přes skupiny (účastník je ve skupině workshopu, obsluha vidí příslušnost u dveří). Přímé odbavení workshopu je v přípravě.

### Účastník nemá QR a obsluha čeká, že mu v aplikaci znovu pošle vstupenku nebo zobrazí QR

Servisní aplikace umí účastníka **najít, přidat a odbavit**, ale **neumí** znovu odeslat vstupenku ani zobrazit QR na obrazovce. Tyto dvě věci řešíte ve webovém **Check-inu (Prezenci)** — mějte ho u vstupu otevřený na počítači.

### Čeká se na tisk jmenovky a tiskárna se zasekne

Mějte záložní tiskárnu a záložní roli jmenovek. Typická chyba je špatně nastavená velikost jmenovky — detail v článku [Tisk jmenovek](https://help.happenee.com/cs/articles/48-tisk-jmenovek).

## Související články

- [Tisk jmenovek](https://help.happenee.com/cs/articles/48-tisk-jmenovek)
- [Nastavení placených vstupenek](https://help.happenee.com/cs/articles/18-nastaveni-placenych-vstupenek)
- [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace)
- [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti)
- [Jak funguje Networking](https://help.happenee.com/cs/articles/36-jak-funguje-networking)
- [Jak funguje účastnická aplikace a její hlavní stránka](https://help.happenee.com/cs/articles/34-jak-funguje-ucastnicka-aplikace-a-jeji-hlavni-stranka)
- [Co dělat při problému na check-inu](https://help.happenee.com/cs/articles/62-co-delat-pri-problemu-na-check-inu)
- [Co dělat, když účastník bez QR stojí ve frontě](https://help.happenee.com/cs/articles/66-co-delat-kdyz-ucastnik-bez-qr-stoji-ve-fronte)
- [Práce s objednávkami a exporty](https://help.happenee.com/cs/articles/52-prace-s-objednavkami-a-exporty)
- [Interpretace statistik eventu](https://help.happenee.com/cs/articles/50-interpretace-statistik-eventu)
- [Interpretace statistik účastníků](https://help.happenee.com/cs/articles/51-interpretace-statistik-ucastniku)
- [Doporučený setup pro interní firemní event](https://help.happenee.com/cs/articles/53-doporuceny-setup-pro-interni-firemni-event)
- [Doporučený setup pro externí klientský event](https://help.happenee.com/cs/articles/54-doporuceny-setup-pro-externi-klientsky-event)
- [Doporučený setup pro konferenci](https://help.happenee.com/cs/articles/55-doporuceny-setup-pro-konferenci)
- [Doporučený setup pro expo / veletrh](https://help.happenee.com/cs/articles/56-doporuceny-setup-pro-expo-veletrh)
- [Komunikační flow v den události](https://help.happenee.com/cs/articles/64-komunikacni-flow-v-den-udalosti)
- [Ruční přidání účastníka do události](https://help.happenee.com/cs/articles/77-rucni-pridani-ucastnika-do-udalosti)
- [Příprava servisní aplikace před událostí](https://help.happenee.com/cs/articles/81-priprava-servisni-aplikace-pred-udalosti)
- [Co zkontrolovat v den události](https://help.happenee.com/cs/articles/83-co-zkontrolovat-v-den-udalosti)
- [Co dělat, když se účastník nedostane do aplikace](https://help.happenee.com/cs/articles/93-co-delat-kdyz-se-ucastnik-nedostane-do-aplikace)
- [Partnerské API klíče](https://help.happenee.com/cs/articles/95-partnerske-api-klice)
- [Nastavení engagement funkcí](https://help.happenee.com/cs/articles/97-nastaveni-engagement-funkci)
- [Doporučený setup pro testovací jízdy](https://help.happenee.com/cs/articles/98-doporuceny-setup-pro-testovaci-jizdy)

<!-- source: kb.cs.05.02 -->

---
title: "Tisk jmenovek"
description: "Tisk jmenovek v servisní aplikaci přes Bluetooth na Brother QL-820NWB. Nastavení velikosti, obsahu a většího písma pro velké jmenovky bez QR kódu."
modules: ["checkin_a_tisk_jmenovek"]
last_updated: "2026-10-15"
version: 5
---

> [!info] Krátce
> Jmenovku vytisknete v servisní aplikaci **po naskenování QR kódu**, kdy aplikace u připojené tiskárny nabídne tisk, nebo **ručně z detailu účastníka či seznamu**; automaticky se tiskne **jen v Kiosk režimu** po samoobslužném odbavení. Tisk probíhá na termotiskárně **Brother QL-820NWB** spárované přes Bluetooth a používá **kontaktní údaje ze správy kontaktů**. Pro standardní **velkou jmenovku 80 × 50 mm bez QR kódu** můžete v administraci události zvolit větší písmo; výchozí zůstává normální velikost. Pokud nemáte vlastní tiskárnu, domluvte si zapůjčení včas s customer success.

## Jak začít

- Rozhodněte, jakou **velikost jmenovky** použijete: velkou **80 × 50 mm** (umožňuje tisk QR) nebo malou **70 × 29 mm** (bez QR).
- Rozhodněte, **co bude na jmenovce** vedle jména a příjmení: firma, pracovní pozice, poznámka — nebo nic.
- Rozhodněte, zda na jmenovku **tisknout QR kód** — vyplatí se, pokud budete v účastnické aplikaci používat funkci **Účastníci** (skenování pro networking). Tisk QR si zapnete v nastavení tisku v modulu **Odbavení na místě**.
- U **velké jmenovky bez QR** rozhodněte také o velikosti písma — větší písmo využije uvolněné místo pro čitelnější jméno.
- Pokud si tiskárnu **půjčujete od Happenee**, domluvte s customer success termín doručení a platbu podle ceníku.
- **Den předem otestujte** — spárování přes Bluetooth, správně nastavenou velikost média v tiskárně a kvalitu tisku. Vedle **Vytisknout test badge** v *Nastavení* servisní aplikace vytiskněte z detailu účastníka i několik skutečných jmenovek, včetně nejdelších jmen a zvoleného doplňkového pole.

## Detail

### Kdy se jmenovka tiskne

- **Po naskenování QR** v Režimu obsluhy — obsluha naskenuje QR a aplikace u připojené tiskárny rovnou nabídne tisk.
- **Ručně z detailu účastníka** — tlačítko **Tisk badge**. Použijete, když chcete jmenovku vytisknout (nebo přetisknout) bez skenu.
- **Swipnutím řádku v seznamu** — akce **Tisknout jmenovku** vytiskne jmenovku rovnou ze seznamu **Účastníci**.
- **V Kiosk režimu** — jmenovka se vytiskne automaticky po samoobslužném odbavení účastníka.

Personál jmenovku odlepí a nalepí na visačku, kterou má účastník u sebe.

### Párování tiskárny

Tiskárnu spárujete přímo v aplikaci: v *Nastavení* otevřete **Připojit tiskárnu badge** (nebo na úvodní obrazovce události řádek **Tiskárna**), zapnete na tiskárně párovací režim a klepnete na **Spárovat novou tiskárnu**. Když se objeví v seznamu, vyberete ji a potvrdíte. Pokud párování nejde, aplikace odkáže na ruční cestu přes **Nastavení → Bluetooth** v systému.

Jedna tiskárna je spárovaná s jedním telefonem nebo tabletem. **Při přepnutí na jiné zařízení se párování ztratí** a je potřeba ho obnovit.

### Tiskárna Brother QL-820NWB

Standardně doporučovaný model. Tiskne termálně — nepotřebuje inkoust, jen roli jmenovek ve správné velikosti. Pokud nemáte vlastní, **Happenee tiskárnu zapůjčí** podle aktuálního ceníku. Dohoda a podrobnosti přes customer success — myslete na to **s předstihem** (doručení, kauce, vrácení).

### Velikosti jmenovek

Dvě standardní velikosti:

- **Velká jmenovka (80 × 50 mm)** — vejde se jméno, příjmení, další informace i **QR kód**. Používá se tam, kde chcete tisknout QR pro networking.
- **Malá jmenovka (70 × 29 mm)** — jen jméno, příjmení a případně jedno doplňkové pole. **QR kód se na ni netiskne** — technicky se nevejde.

Velikost jmenovek **musí být správně nastavená v tiskárně** — viz *Na co si dát pozor*.

### Zapnutí QR na jmenovce

Pokud máte oprávnění měnit nastavení tisku události, můžete v modulu **Odbavení na místě** sami zapnout nebo vypnout QR na jmenovce. QR je dostupné jen pro **velkou jmenovku 80 × 50 mm s normálním písmem**. Zapnutí QR automaticky nastaví normální velikost písma.

Při přepnutí na **malou jmenovku 70 × 29 mm** se QR vypne a písmo se vrátí na normální velikost. Volba QR zůstane viditelná, ale neaktivní, s vysvětlením omezení. Po návratu na velkou jmenovku zůstane QR vypnuté, dokud ho znovu nezapnete.

### Velikost písma u velké jmenovky bez QR

V administraci události v modulu **Odbavení na místě** najdete v nastavení tisku volbu **Velikost písma**. Zobrazí se jen pro **velkou jmenovku 80 × 50 mm (H50) bez QR kódu**:

- **Normální** — výchozí nastavení, které zachová původní rozložení jmenovky.
- **Větší** — volitelné rozložení, které využije místo bez QR pro větší jméno a příjmení.

Pokud přepnete na **malou jmenovku 70 × 29 mm (H29)** nebo se na jmenovku začne tisknout **QR kód**, nastavení se automaticky uloží jako **Normální** a volba velikosti písma se skryje. Po návratu na velkou jmenovku bez QR musíte **Větší** zvolit znovu.

### Dlouhá jména při větším písmu

Větší písmo přizpůsobí jméno i doplňkový text dostupnému místu: jméno může zabrat dva řádky a dlouhé křestní jméno se může zkrátit na iniciálu. Jméno a příjmení proto vyplňujte v kontaktních údajích do samostatných polí. Před událostí vytiskněte jmenovky s nejdelšími jmény a názvy firem a zkontrolujte, že jsou čitelné a úplné.

### Obsah jmenovky

Na jmenovce se vždy tiskne **jméno a příjmení** účastníka (povinné). Kromě toho si vyberete **jedno** z doplňkových polí:

- **Firma** — vhodné pro B2B události, klientské eventy, konference.
- **Pracovní pozice** — vhodné pro odborné konference, networkingové večery.
- **Poznámka** — volné pole z profilu účastníka (typicky dieta, role, dress code).
- **Bez doplňku** — jen jméno a příjmení.

Data se čerpají z **kontaktních údajů ve správě kontaktů**. Pokud účastník vyplnil *firmu*, ale vy nastavíte tisk *pracovní pozice*, zůstane pole prázdné. Ověřte si dopředu, že účastníci vyplnili to, co plánujete tisknout.

### Kdy na jmenovku tisknout QR kód

**Jen tehdy, když plánujete v účastnické aplikaci zapnout engagement funkci Účastníci** (Networking s QR skenováním). Účastníci si tam navzájem skenují QR ze jmenovek, aby si uložili kontakt. Pokud tuto funkci nepoužíváte, QR kód na jmenovce je zbytečný. QR **lze tisknout pouze na velkou jmenovku 80 × 50 mm s normální velikostí písma**. Detail v článku [Jak funguje Networking](../03_obsah-a-zkusenost-ucastnika/16_jak-funguje-networking.md).

### Tisk bez skenu — rychlé přidání účastníka

Když někdo dorazí bez registrace, založíte ho přímo v servisní aplikaci přes **Přidat účastníka** (v seznamu *Účastníci*) a pak mu vytisknete jmenovku tlačítkem **Tisk badge**. Totéž jde i ve webovém **Check-inu (Prezenci)**. Detail v článku [Jak funguje check-in a skenování QR kódů](01_jak-funguje-check-in-a-skenovani-qr-kodu.md).

## Na co si dát pozor

### Větší písmo zmizelo nebo se jmenovka tiskne jinak

Zkontrolujte, že máte **velkou jmenovku 80 × 50 mm** bez QR kódu a znovu zvolenou velikost **Větší**. Přepnutí na malou jmenovku nebo tisk QR vrací nastavení na **Normální**.

Pokud má vaše událost **jmenovku upravenou na míru**, větší písmo se na ni nepoužije. Podobu takové jmenovky řešte s customer success.

### Tisk nefunguje — jmenovky se nevytisknou, nebo vyjedou prázdné

Nejčastější příčina je **špatně nastavená velikost média v tiskárně**. Tiskárna má vlastní konfiguraci velikosti, která musí odpovídat vložené roli (80 × 50 nebo 70 × 29). Před událostí ručně otestujte — vložte roli, nastavte velikost, použijte **Vytisknout test badge** v *Nastavení* aplikace.

### Personál zapne tiskárnu, naskenuje QR, ale nic se netiskne

Zkontrolujte **Bluetooth spárování** mezi zařízením a tiskárnou. Při přepnutí mezi obsluhou (jiný telefon) se párování ztratí — obnovte ho přes **Spárovat novou tiskárnu**, případně přes **Nastavení → Bluetooth** v systému.

### Organizátor nastaví tisk firmy, ale na jmenovce jsou jen jména — firma chybí

Data se berou z kontaktů. Pokud účastníci firmu nevyplnili (nebyla jako pole v registračním formuláři), nemá systém co tisknout. Ověřte, že pole existuje ve formuláři a účastníci ho vyplnili.

### Organizátor chce tisknout QR kód na malou jmenovku

U malé jmenovky zůstává volba QR viditelná, ale neaktivní. Pro tisk QR vyberte **velkou jmenovku 80 × 50 mm** a QR znovu zapněte; použije se normální velikost písma.

### Na události dorazí jen jedna tiskárna a ta se zasekne

Mějte **záložní tiskárnu** a záložní roli jmenovek. U větších událostí se vyplatí dvě stanoviště pro tisk — redundance i vyšší propustnost.

### Organizátor si tiskárnu od Happenee objedná na poslední chvíli a nedoručí se včas

Půjčovna přes customer success není instantní — má logistiku, kauci, vrácení. Objednávejte **minimálně 10 dní předem**.

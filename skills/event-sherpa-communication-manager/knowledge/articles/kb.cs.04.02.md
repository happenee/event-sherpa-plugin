<!-- source: kb.cs.04.02 -->

---
title: "Jak funguje potvrzovací e-mail"
description: "Systémový e-mail, který se po dokončení registrace automaticky pošle účastníkovi s PDF vstupenkou a odkazem do aplikace."
modules: ["komunikace_a_pozvanky"]
last_updated: "2026-09-21"
version: 2
---

> [!info] Krátce
> Potvrzovací e-mail je systémová zpráva, která se **automaticky odešle účastníkovi po dokončení registrace**. Obvykle obsahuje PDF vstupenku s QR kódem a ICS soubor pro přidání do kalendáře. Funguje jako klíčový most z registrace do účastnické aplikace — z tohoto e-mailu účastník vstupuje dál. Pokud máte zapnuté **schvalování registrace**, systém pracuje se třemi variantami potvrzovacího e-mailu (čeká na schválení / schváleno / zamítnuto).

## Jak začít

- Vyplňte obsah potvrzovacího e-mailu **ve všech jazycích události**.
- V Nastavení události se rozhodněte, co připojíte jako přílohu: **ICS soubor**, **PDF vstupenku s QR kódem** (typicky ano), případně obojí.
- Pokud plánujete schvalování registrace, počítejte s tím, že nastavíte tři varianty potvrzovacího e-mailu.
- Otestujte celý tok: registrace → potvrzovací e-mail → odkaz do účastnické aplikace.

## Detail

### Kdy se potvrzovací e-mail odesílá

- Po dokončení registračního formuláře (typická cesta).
- Po dokončení platby u placené události s *automatickou registrací po nákupu*.
- Po vygenerování vstupenky u *registrace s doplněním informací* — až když účastník dokončí doplnění údajů.
- Po **ručním překlopení stavu** účastníka na *Zúčastním se* v administraci (viz níže).
- U schvalované registrace po **manuálním schválení** organizátorem.

### Obsah potvrzovacího e-mailu

V modulu **Potvrzovací e-mail** v levém menu události najdete:

- **Předmět e-mailu**.
- **Textový editor těla** — s proměnnými (merge tagy), které automaticky doplní jméno, název události, datum a další údaje.
- **HTML tlačítko** — pro vložení vlastního tlačítka (např. odkaz do účastnické aplikace, odkaz na FAQ).
- **Proměnné** dostupné ve všech e-mailových modulech (zvací, potvrzovací, kampaně) i na microsite v textu po odeslání registrace.

### Úvodní obrázek, přílohy a patička

Stejně jako u zvacího e-mailu se grafika a přílohy řídí centrálně z **Nastavení události**:

- **Úvodní obrázek** — v sekci Nastavení grafiky, sdílený s microsite a zvacím e-mailem.
- **ICS soubor** — v sekci Nastavení e-mailů. Přijde jako příloha, po otevření přidá událost do kalendáře. Některé e-mailové programy zobrazí vlastní banner s přidáním do kalendáře.
- **PDF vstupenka s QR kódem** — připojíte, aby si účastník mohl vstupenku vytisknout. QR kód v PDF funguje stejně jako QR kód v účastnické aplikaci.
- **Patička e-mailu** — výchozí text platformy, nebo vlastní.
- **Odesílatel a Příjemce odpovědi** — nastavuje se tamtéž.

### Schvalovaná registrace — tři e-maily místo jednoho

Schvalovaná registrace se zapíná v **Nastavení události** (jen u neplacených událostí — nelze ji kombinovat s placenými vstupenkami). Když je aktivní, potvrzovací e-mail má tři varianty:

- **Čeká na schválení registrace** — účastník dostane hned po odeslání formuláře. Říká, že registrace je přijatá a čeká na rozhodnutí organizátora.
- **Schváleno (potvrzení registrace)** — po manuálním schválení. Obsahuje PDF vstupenku a ICS. Toto je „hlavní“ potvrzovací e-mail v této situaci.
- **Zamítnuto** — po manuálním zamítnutí. Informuje účastníka, že se události nezúčastní.

Schvalovaná registrace se hodí, když chcete opravdu vybírat účastníky (například u veřejně sdíleného odkazu) nebo chcete sladit pozvání ve víc vlnách.

### Automatické odeslání při ručním přepnutí stavu

V administraci události můžete účastníkovi ručně překlopit stav na **Zúčastním se** (v Registraci). Typický případ: účastník napsal e-mailem, že přijde, ale neprošel formulářem. V tomto dialogu si **admin volí, zda se má odeslat potvrzovací e-mail** — typicky proto, aby přišla vstupenka.

### Test potvrzovacího e-mailu

Na rozdíl od zvacího e-mailu potvrzovací chodí automaticky, takže test je nepřímý — projděte si sami registraci (nebo si pomocí ručního překlopení stavu na *Zúčastním se* vyvolejte odeslání) a podívejte se, co reálně přijde. Vyzkoušejte to v obou jazycích.

### Vztah k účastnické aplikaci

Potvrzovací e-mail je **první kontaktní bod** s účastnickou aplikací. Obvykle obsahuje:

- PDF vstupenku s QR kódem (pro vstup na místě).
- ICS soubor pro kalendář.
- Odkaz (nebo text) vedoucí do účastnické aplikace — buď „Stáhněte si naši aplikaci“ (mobilní), nebo „Otevřít v prohlížeči“ (webová).

Přihlášení účastníka probíhá přes **Magic Link**, **PIN** nebo **QR kód** odeslaný na stejný e-mail. Proto je potvrzovací e-mail klíčový pro to, aby se účastník vůbec do aplikace dostal.

## Na co si dát pozor

### Organizátor vyplní potvrzovací e-mail jen v češtině a účastník registrovaný v angličtině nedostane potvrzení ve svém jazyce

Přepněte vlajku jazyků a vyplňte obsah i v druhém jazyce. Ověřte testovací registrací v obou jazycích.

### Organizátor zapne schvalovanou registraci, ale nepočítá s tím, že si musí připravit **tři** varianty potvrzovacího e-mailu. Účastníci tak dostávají zprávy bez textu organizátora

Pro schvalovanou registraci vyplňte všechny tři varianty — čeká na schválení, schváleno, zamítnuto — a to v každém jazyce. Varianta, kterou nevyplníte, odejde bez vašeho textu.

### Organizátor ručně přepne účastníka na *Zúčastním se*, ale odškrtne „odeslat potvrzovací e-mail“ a účastník tak nedostane vstupenku

Pokud má účastník dorazit, ponechte odesílání zapnuté, aby dostal PDF vstupenku s QR kódem a odkaz do aplikace. Znovu odeslat lze i později z detailu registrace.

### Organizátor připojí PDF vstupenku s QR kódem u placené události, kde se platí až po objednávce — a účastník ji dostane dřív, než zaplatil

Potvrzovací e-mail se vstupenkou chodí až po dokončení registrace (a u zálohových faktur po připsání platby / dokončení registrace). Proces nákupu vstupenky má vlastní e-maily (potvrzení objednávky, doplnění údajů).

### Úvodní obrázek, ICS nebo patičku hledá organizátor v modulu Potvrzovací e-mail a nemůže je najít

Všechno se nastavuje v **Nastavení události** (Grafika, E-maily, ICS, Patička). Modul Potvrzovací e-mail slouží primárně pro předmět a tělo.

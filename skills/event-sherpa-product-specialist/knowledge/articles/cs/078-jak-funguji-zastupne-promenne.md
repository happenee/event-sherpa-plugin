# Jak fungují zástupné proměnné

> Zástupné proměnné doplní do e-mailu, kampaně nebo na microsite individuální údaje účastníka — kompletní seznam univerzálních proměnných, proměnné k vlastním polím kontaktů a jak je testovat.

- Článek v Help Centru: https://help.happenee.com/cs/articles/78-jak-funguji-zastupne-promenne
- English version: https://help.happenee.com/en/articles/78-how-placeholder-variables-work
- Kolekce: Komunikace a pozvánky
- Aktualizováno: 2026-08-07

---

> [!info] Krátce
> **Zástupné proměnné** jsou znaky ve tvaru `::PROMENNA::`, které se při odeslání nahradí konkrétním údajem daného účastníka — jménem, názvem události, QR kódem. Vložíte je do textu zvacího e-mailu, potvrzovacího e-mailu, kampaně i do obsahu microsite a každý příjemce pak dostane text s vlastními hodnotami. Vedle univerzálních proměnných existují ještě proměnné navázané na **vlastní pole kontaktů**, které jsou pro každý workspace jiné.

## Jak začít

1. Otevřete text, který píšete (kampaň, zvací nebo potvrzovací e-mail), a najděte sekci **Zástupné proměnné**.
2. U každé proměnné je ikona kopírování — proměnnou zkopírujte a vložte do textového pole přesně tam, kde má hodnota být.
3. Zapište ji **včetně obou dvojteček na začátku i na konci**. `::UZIVATEL_JMENO::` funguje, `:UZIVATEL_JMENO:` ani `::UZIVATEL_JMENO` ne.
4. Před rozesláním pošlete **test kampaně** na svou adresu a zkontrolujte, že se proměnné opravdu nahradily.

## Detail

### Univerzální proměnné

Tyhle proměnné jsou k dispozici vždy, nezávisle na tom, jak máte workspace nastavený:

- **`::UZIVATEL_JMENO::`** — Křestní jméno účastníka
- **`::UZIVATEL_JMENO_PRIJMENI::`** — Jméno a příjmení
- **`::UZIVATEL_EMAIL::`** — E-mail účastníka
- **`::NAZEV_UDALOSTI::`** — Název události
- **`::KDY::`** — Datum a čas události
- **`::KDE::`** — Místo konání
- **`::KONTAKTNI_OSOBA::`** — Jméno kontaktní osoby
- **`::QRCODE::`** — QR kód pro vstup
- **`::VAR_SYMBOL::`** — Variabilní symbol
- **`::DATUM::`** — Aktuální datum
- **`::O_APLIKACI::`** — Blok s informacemi o aplikaci — obsah se řídí typem události (fyzická, virtuální, hybridní)
- **`::UDAJE_O_UZIVATELI::`** — Údaje, které účastník zadal při registraci
- **`::REGISTRACNI_FORMULAR::`** — Data zadaná v registračním formuláři
- **`::EVENT_CERTIFICATE_OFFLINE::`** — Odkaz pro stažení certifikátu u fyzické události

Některé z nich doplní **celý blok**, ne jedno slovo — typicky `::O_APLIKACI::`, `::UDAJE_O_UZIVATELI::` a `::REGISTRACNI_FORMULAR::`. Nepoužívejte je uprostřed věty; postavte je na vlastní řádek.

### Proměnné k vlastním polím kontaktů

Pokud máte ve workspace založená vlastní pole kontaktů, Happenee k nim vygeneruje samostatné proměnné ve tvaru `::CF####::`, kde číslice jsou interní identifikátor pole. Seznam najdete pod univerzálními proměnnými v podnadpisu **Zástupné proměnné k vlastním polím kontaktů**.

**Tyhle proměnné nejsou univerzální.** Čísla jsou přidělená v rámci vašeho workspace, takže proměnná, která u vás doplňuje oslovení, může v jiném workspace znamenat něco úplně jiného. Nikdy je nepřepisujte z návodu ani z jiné události — vždy je kopírujte ze seznamu ve své administraci.

### Vlastní tlačítko v HTML

Pod seznamem proměnných je připravený **HTML snippet pro vlastní tlačítko**. Zkopírujete ho do textu a upravíte v něm cílovou adresu a popisek. Hodí se, když potřebujete v kampani vlastní výzvu k akci (odkaz na program, dotazník, mapu) vedle standardního registračního tlačítka.

### Kde proměnné fungují

Zástupné proměnné se nahrazují v obsahu microsite, ve zvacím a potvrzovacím e-mailu i v e-mailových kampaních. Modul **Kontakt** se do e-mailů doplňuje automaticky, takže kontaktní osobu nemusíte psát ručně — stačí `::KONTAKTNI_OSOBA::`.

### Vícejazyčné texty

Proměnné se nepřekládají — `::UZIVATEL_JMENO::` je stejná v české i anglické verzi textu. Co se liší, je věta okolo ní. Když píšete dvojjazyčnou kampaň, zkontrolujte, že jste proměnnou vložili do **obou** jazykových verzí; chybějící proměnná v druhém jazyce je jeden z nejčastějších důvodů, proč část příjemců dostane neosobní e-mail.

## Na co si dát pozor

### Proměnná se odešle jako text

Když se v doručeném e-mailu objeví doslova `::UZIVATEL_JMENO::`, byla proměnná zapsaná špatně — nejčastěji chybí dvojtečky na konci, je v ní překlep nebo mezera. Proměnné proto kopírujte ikonou ze seznamu, nepište je z hlavy, a před ostrou rozesílkou pošlete test kampaně sami sobě.

### Prázdné jméno v oslovení

Proměnná doplní jen to, co je u kontaktu vyplněné. U lidí naimportovaných jen s e-mailem se z „Dobrý den, ::UZIVATEL_JMENO::," stane „Dobrý den, ,". Než rozešlete kampaň s osobním oslovením, zkontrolujte v tabulce kontaktů, kolik lidí nemá vyplněné jméno — a buď je doplňte, nebo zvolte neutrální oslovení.

### Proměnná k vlastnímu poli se zkopíruje z jiné události

Čísla v `::CF####::` platí pro váš workspace, ne obecně. Když proměnnou opíšete z cizího návodu nebo z e-mailu jiného pořadatele, buď se nedoplní nic, nebo se doplní hodnota úplně jiného pole. Berte je vždy ze seznamu ve své administraci.

### QR kód se vloží do kampaně pro nezaregistrované

`::QRCODE::` má smysl jen u lidí s dokončenou registrací — ostatním nemá systém co vykreslit. Když kampaň s QR kódem míří na segment, kde jsou i nezaregistrovaní, dostanou e-mail s prázdným místem. Cílení podle stavu účastníka je proto u takové kampaně důležitější než jinde.

## Související články
- [Jak funguje zvací e-mail](https://help.happenee.com/cs/articles/39-jak-funguje-zvaci-e-mail)
- [Jak funguje potvrzovací e-mail](https://help.happenee.com/cs/articles/40-jak-funguje-potvrzovaci-e-mail)
- [Vytvoření a odeslání e-mailové kampaně](https://help.happenee.com/cs/articles/41-vytvoreni-a-odeslani-e-mailove-kampane)
- [Jak fungují vlastní pole kontaktů](https://help.happenee.com/cs/articles/76-jak-funguji-vlastni-pole-kontaktu)

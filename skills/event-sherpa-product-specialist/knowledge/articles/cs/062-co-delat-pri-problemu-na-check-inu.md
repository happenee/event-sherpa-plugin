# Co dělat při problému na check-inu

> Postup pro typické check-in problémy: chybějící QR kód, duplicitní sken, host bez registrace.

- Článek v Help Centru: https://help.happenee.com/cs/articles/62-co-delat-pri-problemu-na-check-inu
- English version: https://help.happenee.com/en/articles/62-what-to-do-when-there-is-a-check-in-issue
- Kolekce: Řešení problémů
- Aktualizováno: 2026-11-04

---

> [!info] Krátce
> Na check-inu chybí QR kód, duplicitní sken, personálu chybí skupina po skenu či v detailu účastníka nebo přichází host bez registrace. Většinu situací vyřešíte přímo v **servisní aplikaci** (seznam **Účastníci** — najít podle jména, odbavit, přidat hosta bez registrace) a správnou volbou typu místa; znovu poslat vstupenku nebo zobrazit QR umí webový **Check-in (Prezence)** v administraci.

## Jak začít

U vstupu mějte obojí: **servisní aplikaci** na telefonu/tabletu (skenování + seznam účastníků) a otevřený webový **Check-in (Prezenci)** na počítači pro případy, které aplikace neumí.

## Detail

### Typické situace a řešení

**Účastník nemá QR kód.** V servisní aplikaci v záložce **Účastníci** ho najděte podle jména a odbavte (akce **Odbavit**), případně mu vytiskněte jmenovku. Pokud potřebuje vstupenku znovu poslat nebo zobrazit QR na obrazovce, použijte webový **Check-in (Prezenci)** — tyto dvě věci aplikace zatím nemá.

**Duplicitní sken (už odbaven).** Typ místa **Příchod** při druhém skenu vrátí upozornění *už dorazil*. Pokud má opakované skenování smysl (šatna, autobus, vstup do zóny), zvolte pro dané stanoviště typ **Kontrola opakovaně**. Pro jednorázovou kontrolu (voucher, dárek) použijte **Kontrola jednorázově**.

**V detailu účastníka nebo po skenu chybí skupina.** Ověřte, že má účastník skupinu přiřazenou. V administraci dané události otevřete **Odbavení na místě** a přidejte skupinu mezi zobrazované v nastavení **Zobrazení skupiny po naskenování účastníka**. Přestože název zmiňuje skenování, výběr platí také pro **Detail účastníka** v servisní aplikaci. Ostatní skupiny z workspace se automaticky nezobrazují.

**Skupina je v detailu vidět, ale po skenu chybí.** Zkontrolujte její nastavení *Zobrazit na místech* a místo vybrané v servisní aplikaci. Omezení na místa platí pouze při skenování; prázdný výběr znamená všechna místa. V detailu účastníka se toto omezení neuplatňuje.

**Host bez registrace na místě.** V servisní aplikaci použijte **Přidat účastníka** (e-mail, jméno, příjmení, firma, pozice) — po uložení ho rovnou odbavíte a vytisknete jmenovku. Totéž jde i ve webové Prezenci (**Rychle přidat účastníka**).

### Prevence

- **Hodinu před událostí** rozešlete e-mailovou kampaň s QR vstupenkou (připomenutí) — účastníci budou mít vstupenku v nejnovějším e-mailu a fronta se zkrátí.
- Zkontrolujte **nastavení typů míst** pro odbavení den předem, ne ráno před událostí.
- Zkontrolujte, že tiskárna (Brother QL-820NWB) je spárovaná se správným zařízením a že jsou vloženy **velké jmenovky 80 × 50 mm** (na malé 70 × 29 mm se QR netiskne).

## Na co si dát pozor

### Organizátor chce odbavovat konkrétní workshop nebo zónu — hledá *check-in na session*

Odbavení podle workshopu / zóny dnes není nativní funkce. Řeší se přes **skupiny** — přiřaďte účastníky do skupiny workshopu, nastavte tuto skupinu k zobrazení při skenování (klidně jen na místě u dveří workshopu) a u dveří použijte typ místa **Kontrola opakovaně**. Navázání check-inu přímo na session / časový slot je v plánu.

### Obsluha čeká, že v servisní aplikaci účastníkovi znovu pošle vstupenku nebo zobrazí QR

Servisní aplikace umí účastníka **najít, přidat a odbavit**, ale **neumí** znovu odeslat vstupenku ani zobrazit QR na obrazovce. Tyto dva kroky řešte ve webovém **Check-inu (Prezenci)** — mějte ho u vstupu otevřený.

### Jmenovka se vytiskla bez QR kódu

QR se tiskne pouze na **velké jmenovky (80 × 50 mm)**. Zkontrolujte formát role v tiskárně a nastavení velikosti.

## Související články

- [Jak funguje check-in a skenování QR kódů](https://help.happenee.com/cs/articles/47-jak-funguje-check-in-a-skenovani-qr-kodu)
- [Tisk jmenovek](https://help.happenee.com/cs/articles/48-tisk-jmenovek)
- [Vytvoření a odeslání e-mailové kampaně](https://help.happenee.com/cs/articles/41-vytvoreni-a-odeslani-e-mailove-kampane)
- [Jak funguje účastnická aplikace a její hlavní stránka](https://help.happenee.com/cs/articles/34-jak-funguje-ucastnicka-aplikace-a-jeji-hlavni-stranka)
- [Co dělat, když účastník bez QR stojí ve frontě](https://help.happenee.com/cs/articles/66-co-delat-kdyz-ucastnik-bez-qr-stoji-ve-fronte)

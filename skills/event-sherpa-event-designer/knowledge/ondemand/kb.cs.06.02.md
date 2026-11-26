<!-- source: kb.cs.06.02 -->

---
title: "Interpretace statistik účastníků"
description: "Stavy účastníků od pozvánky až po skutečnou účast a jak je číst při reportingu i cílení komunikace."
modules: ["reporting_a_statistiky"]
last_updated: "2026-10-22"
version: 6
---

> [!info] Krátce
> Statistiky s účastníky vám ukazují, kdo je v jakém stavu — od odeslání pozvánky přes registraci až po skutečnou účast na místě. Stavy účastníků jsou zároveň filtry pro e-mailové kampaně a Oznámení, takže reporting a cílení komunikace pracují s **týmiž daty**. Pokud rozumíte stavům, umíte zpětně pracovat s tím, kdo na co nereagoval a co s tím dál.

## Jak začít

Než začnete statistiky číst, ujasněte si, co vás reálně zajímá:

- **Před událostí** — kolik lidí reagovalo na pozvánku, kolik se zaregistrovalo, kolik má aplikaci.
- **V den události** — kdo přišel, kolik lidí chybí proti registraci, jestli účastníci používají aplikaci.
- **Po události** — kdo se zúčastnil, kolik lidí nedorazilo, případně kdo si stáhl aplikaci, ale nakonec nedorazil.

Podle toho otevřete správný pohled: **Statistiky → Statistiky s účastníky** v levém menu události, případně sekci **Registrace**, která je plochá tabulka se všemi stavy a filtry.

## Detail

### Klíčové stavy účastníka

- **Bez odpovědi** — Účastník má pozvánku nebo přístup, ale ještě nereagoval
- **Zúčastním se** — Dokončil registraci (nebo byl nastaven organizátorem)
- **Nezúčastním se** — Odmítl pozvánku
- **Čeká na schválení** — Jen u schvalované registrace — registrace je ve frontě, organizátor ji musí potvrdit
- **Odbaven** — Prošel check-inem na vstupu
- **Odešel** — Byl odbaven na místě typu *Odchod* (u událostí, kde se měří účast v průběhu)

Stavy se mění buď automaticky (registrací, check-inem), nebo ručně (organizátor v sekci *Registrace* může přepnout účastníka zpět do *Bez odpovědi* nebo ho z události úplně odebrat).

### Odpovědi na zvací e-mail

Pro pozvané kontakty sledujete čtyři hodnoty:

- **Odesláno** — e-mail odešel systémem
- **Zobrazeno** — účastník otevřel e-mail (záleží na tom, zda e-mailový klient umožňuje trackování)
- **Reagováno** — klikl na tlačítko nebo otevřel microsite
- **Registrováno** — dokončil formulář (už se překlápí do stavu *Zúčastním se*)

Tyhle hodnoty jsou zároveň **filtry pro e-mailovou kampaň** — například *„pošli druhou vlnu všem, kdo ještě nereagoval“*. Viz [Cílení komunikace podle skupin a stavů](../04_komunikace-a-pozvanky/05_cileni-komunikace-podle-skupin-a-stavu.md).

### Aktivita v účastnické aplikaci

Samostatný pohled (a samostatný export) pokrývá:

- **Kdo si stáhl mobilní aplikaci** — podle e-mailu, se kterým je účastník v aplikaci přihlášen
- **Aktivita uživatelů v aplikaci** — kteří účastníci si otevřeli příslušnou událost, jaké sekce aplikace otevřeli, kdy byli naposledy aktivní

Pro interní firemní událost to říká, kolik lidí reálně pracuje s aplikací. Pro konferenci to pomáhá vyhodnotit, jestli se vyplatí do aplikace tlačit víc obsahu.

### Filtrování v sekci Registrace

Sekce **Registrace** je plochá tabulka všech účastníků, ve které filtrujete podle stavu, skupiny, preferovaného jazyka, data registrace, vstupenky a dalších polí. Souhrnná čísla ve statistikách říkají *kolik*, filtr v Registraci říká *kdo*.

Filtr platí jen pro vaše aktuální zobrazení — je to pracovní nástroj, ne pohled, který byste kolegům předali. Když má s týmiž daty pracovat někdo další, pošlete mu **export** ze sekce **Statistiky → Exporty**.

### Rychlá ruční úprava

Ze stránky **Registrace** organizátor dokáže:

- Přepnout stav účastníka (například při telefonickém odhlášení ho ručně dát na *Nezúčastním se*)
- Zaregistrovat účastníka **místo něj** — přepne stav na *Zúčastním se* a volitelně mu pošle potvrzovací e-mail s vygenerovanou vstupenkou
- **Odebrat** účastníka z události úplně

Tyto operace jsou logovány a promítají se do statistik okamžitě.

### Sdílení s managementem

Statistiky s účastníky jsou vidět jen z administrace. Konkrétní pohled — *Zúčastním se* včetně doprovodu nebo *Odbaven* — odkazem sdílet nejde, stejně jako statistiky eventu. Kdo čísla potřebuje a do administrace nechodí, dostane je exportem ze sekce **Statistiky → Exporty**, nebo v podobě shrnutí, které mu připravíte. Viz [Interpretace statistik eventu](01_interpretace-statistik-eventu.md).

## Na co si dát pozor

### Zaměňujete *„Zobrazil event“* (ikona / náhled v aplikaci) s *„Zaregistroval se“*

Zobrazení eventu je jen signál zájmu, ne závazek. Registrace je formulář nebo potvrzovací klik. Pro reálné plánování počtů (catering, jmenovky) pracujte se stavem *Zúčastním se*.

### Po události děláte reporting podle počtu registrovaných, ne reálně přišlých

Pro skutečnou účast použijte stav **Odbaven** (v aplikaci nebo exportu skenování). Registrace = závazek; účast = realita. Většina událostí má rozdíl 10–30 %.

### Čekáte, až někdo *Bez odpovědi* zareaguje sám

Stav *Bez odpovědi* je podklad pro druhou vlnu komunikace. Pošlete e-mailovou kampaň cílenou přesně na ten stav — mnohem efektivnější než hromadná pozvánka všem.

### Díváte se jen na celková čísla, ne na skupiny

Segmentujte podle skupin (zaměstnanci / klienti / VIP) — dostanete se k otázkám typu *„kdo z VIP ještě nepotvrdil“*, které celkový pohled neukáže.

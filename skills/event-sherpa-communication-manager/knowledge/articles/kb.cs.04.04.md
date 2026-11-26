<!-- source: kb.cs.04.04 -->

---
title: "Kdy použít zvací e-mail a kdy e-mailovou kampaň"
description: "Zvací e-mail jako první vlnu pozvánek po importu kontaktů, kampaň na všechno ostatní."
modules: ["komunikace_a_pozvanky"]
last_updated: "2026-09-21"
version: 5
---

> [!info] Krátce
> V Happenee existují vedle sebe dva moduly pro odchozí e-maily — **Zvací e-mail** a **E-mailové kampaně**. Organizátoři si je často pletou. Zkrácené pravidlo: **zvací e-mail** pošlete jako **první vlnu pozvánek** po importu kontaktů. Na všechno ostatní (remindery, follow-upy, segmentovaná sdělení, dopozvánky novým kontaktům) použijte **kampaně**. Kampaně umí všechno, co zvací e-mail, a navíc cílení na skupiny, plánování a dorozesílání novým.

## Jak začít

- Pokud posíláte úplně první pozvánku přiřazeným kontaktům a stačí vám cílit podle stavu (nepozvaní), můžete použít **zvací e-mail**.
- Pokud potřebujete cílit jen na konkrétní skupinu (VIP, řečníci, jeden jazyk), plánovat rozesílku na datum, nebo mít jinou hlavičku než zbytek události — použijte **kampaň**.
- Ve většině větších událostí je jednodušší a přehlednější **vše řešit přes kampaně**, včetně první pozvánky.

## Detail

### Co zvací e-mail umí a neumí

Zvací e-mail je **legacy modul** v produktu — byl před kampaněmi. Má:

- Editor s proměnnými.
- Registrační tlačítko (osobní odkaz, veřejný odkaz, u placené události i individuální vstup zdarma).
- Individuální rozesílku (po jednom) a hromadnou rozesílku podle **stavů účastníků**:
  - *Nepozvaní* — komu zvací e-mail ještě nešel.
  - *Kdo si nepřečetl zvací e-mail*.
  - *Neregistrovaný (bez odpovědi)*.

Nemá:

- **Cílení podle skupin**.
- **Plánování rozesílky** na konkrétní datum.
- **Vlastní hlavičku** pro konkrétní rozesílku.
- **Dorozeslání novým** bez zásahu do historie.
- Napojení na reporty v takovém rozsahu jako kampaně.

### Co kampaně umí navíc

E-mailová kampaň obsáhne vše ze zvacího e-mailu a přidává:

- **Cílení podle skupin** (VIP, řečníci, jazyk, skupina ze slevového kódu atd.).
- **Plánovanou rozesílku** na konkrétní datum a čas.
- **Vlastní obrázek hlavičky** jen pro tuto kampaň.
- **Doposlat kampaň nově přiřazeným** — odešle jen těm, kdo k události přibyli až po zahájení rozesílky.
- **PDF vstupenku s QR kódem** jako přílohu (typicky ranní e-mail v den události).
- **Historii rozesílek** s doručitelností po jednotlivých příjemcích.

### Typický use case zvacího e-mailu

**První vlna pozvánek po importu.** Naimportujete seznam kontaktů, přiřadíte je k události, překontrolujete si text pozvánky a ve Zvacím e-mailu zvolíte rozesílku na „Nepozvané“. Všichni přiřazení tak dostanou první pozvánku v jednotné formě. Pro tento krok je zvací e-mail připravený a je to jeho historická role.

### Typické use cases kampaní

- **Reminder týden / 3 dny / 1 den před událostí** — naplánujete dopředu, odejde samo.
- **Guest list u placené události** — kampaň s volbou *Individuální vstup zdarma* na vybraný seznam importovaných kontaktů.
- **Dopozvánka bez reakce** — cílíte jen na stav *Bez reakce* s nenásilnějším tónem.
- **Info pro VIP nebo řečníky** — cílíte na skupinu, posíláte jim speciální info, které ostatní nedostanou.
- **Ranní e-mail v den události** — vstupenka s QR kódem a krátký text, cílení podle stavu *Registrovaní*.
- **Follow-up po události** — poděkování, fotky, odkaz na feedback.
- **Různé segmenty podle jazyka** — pokud chcete pro česky mluvící jiný text než pro anglicky.
- **Doposlání novým přihlášeným** — kampaň spustíte znovu funkcí *Doposlat kampaň nově přiřazeným*, aby ji dostali jen lidé, kteří přibyli.

### Proč to lidi pletou

Autor produktu mluví otevřeně: *„V e-mailech se trošku topěj v tom, že je nějakej zvací e-mail a e-mailový kampaně.“* Organizátoři si kladou otázku, proč jsou dva moduly, a nevědí, do kterého sáhnout.

Důvod je historický — zvací e-mail byl v produktu dřív. Kampaně přibyly, protože organizátoři potřebovali cílit podle skupin, plánovat a dorozesílat. Sjednocení do jednoho modulu je v plánu, ale teď jsou v produktu oba.

### Orientace do budoucna

Produkt dlouhodobě směřuje k tomu, aby **veškerá zvací komunikace šla přes kampaně**. Pokud pokrýváte opakovaně podobné eventy, zvykněte si používat kampaně i na první pozvánku — ušetříte si změnu návyku, až zvací e-mail splyne s kampaněmi.

### Rozhodovací pravidlo

- **První pozvánka, všem přiřazeným kontaktům, jeden text** — Zvací e-mail *(nebo kampaň — obojí OK)*
- **Pozvánka jen VIP / řečníkům / jedné skupině** — Kampaň
- **Reminder v konkrétní datum** — Kampaň (naplánovaná)
- **Dopozvánka těm bez odpovědi** — Zvací e-mail *(stavem)* nebo kampaň *(stav + skupina)*
- **Kampaň pro nové přihlášené** — Kampaň (*Doposlat kampaň nově přiřazeným*)
- **Guest list zdarma u placené události** — Kampaň *(Individuální vstup zdarma)*
- **Follow-up po události** — Kampaň
- **Ranní vstupenka v den události** — Kampaň (s PDF vstupenkou v příloze)
- **Vlastní hlavička pro jednu rozesílku** — Kampaň

### Pozor — potvrzovací e-mail je třetí věc

Zvací e-mail ≠ potvrzovací e-mail ≠ kampaň. Potvrzovací e-mail chodí **automaticky** po registraci a má vlastní modul. Zvací e-mail a kampaně jsou pro **aktivní oslovování** — rozhodujete o nich vy.

## Na co si dát pozor

### Organizátor chce poslat pozvánku jen VIP, ale dělá to přes zvací e-mail, kde cílení na skupinu není

Pro cílení na konkrétní skupinu použijte **kampaň**. Zvací e-mail cílí pouze podle stavů.

### Organizátor nastaví reminder týden před událostí ve zvacím e-mailu a čeká, až ho systém odešle

Zvací e-mail **neumí plánovanou rozesílku**. Pro timing v konkrétní datum použijte kampaň a zvolte *Naplánovat rozesílku*.

### Organizátor posílá tu samou pozvánku opakovaně všem, protože chce oslovit nové přihlášené — a ti staří ji dostanou podruhé

Použijte u odeslané kampaně panel **Doposlat kampaň nově přiřazeným** na záložce *Rozesílka* a tlačítko **Nově přiřazení**. Kampaň dostanou jen ti, kdo ji ještě nedostali.

### Organizátor nerozumí, proč vedle sebe existují dva moduly, a používá zvací e-mail pro všechno, čímž si zkomplikuje segmentaci

Pokud váš běžný scénář obsahuje remindery, dopozvání nebo cílení na skupiny, začněte používat **kampaně jako hlavní kanál**. Zvací e-mail nechte na první jednoduchou pozvánku, nebo ho úplně vynechte a první pozvánku pošlete také kampaní.

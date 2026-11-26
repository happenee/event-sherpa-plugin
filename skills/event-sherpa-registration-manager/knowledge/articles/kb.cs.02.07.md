<!-- source: kb.cs.02.07 -->

---
title: "Práce se skupinami a viditelností"
description: "Jak skupinami uvnitř události řídit viditelnost obsahu, cílení komunikace a omezení registrace."
modules: ["ucastnici_skupiny_a_viditelnost"]
last_updated: "2026-09-07"
version: 2
---

> [!info] Krátce
> Skupiny v Happenee slouží ke **kategorizaci účastníků** a k řízení toho, co kdo uvidí. Správa skupin je na úrovni workspace (viz *Správa kontaktů a skupin ve workspace*). Tento článek popisuje, jak skupiny použít **uvnitř události** — pro viditelnost obsahových a engagement funkcí, cílení komunikace, omezení registrace a filtrování statistik.

## Jak začít

- Ujasněte si, podle čeho chcete účastníky rozlišovat — typ (VIP / standardní), role (speaker / partner), zdroj registrace (nominátor), preferenci (stravování, workshop), firmu nebo tým.
- Skupiny založte **před** spuštěním registrace. Ex post přiřazování funguje, ale je ruční.
- Mechanizmy, jak se účastník do skupiny dostane, jsou popsané v článku *Správa kontaktů a skupin ve workspace* — nejrychlejší cesta je přes odpověď v registračním formuláři.
- Viditelnost zapínejte opatrně — prázdná funkce pro polovinu účastníků vytváří dojem rozbité aplikace.

## Detail

### Čtyři hlavní použití skupin

**1. Viditelnost obsahových a engagement funkcí.** U každé obsahové funkce (Program, Řečníci, Lokalita, Kontakt, Vlastní obsah, Sponzoři, Vystavovatelé) a u každé engagement funkce (QR vstupenka, Oznámení, Hlasování, Dotazník, Otázky, Účastníci, Registrační údaje, Online modul) lze nastavit, zda ji uvidí všichni, nebo pouze vybrané skupiny. (Funkce networkingu mezi účastníky se v UI jmenuje **Účastníci**; *Networking* je brand-term alias používaný v komunikaci.)

**2. Cílení e-mailových kampaní.** E-mailová kampaň se dá cílit na jednu nebo více skupin. Zvací e-mail cílení přes skupiny **nepodporuje** — pokud potřebujete segmentaci pro pozvánku, použijte e-mailovou kampaň.

**3. Viditelnost otázek a odpovědí v registračním formuláři.** U každé doplňující otázky a u každé konkrétní odpovědi lze nastavit, zda se zobrazí pouze vybraným skupinám.

**4. Reporting.** Ve statistikách účastníků lze filtrovat podle skupiny — například *kolik lidí z nominace obchodníka Nováka přišlo*.

### Jak se účastník do skupiny dostane

Shrnutí cest (detail v článku *Správa kontaktů a skupin ve workspace*):

- **Import** — při hromadném importu kontaktů ve sloupci skupin.
- **Ručně v tabulce kontaktů** — označit kontakty a použít akci **Přidat nebo odebrat ze skupin**.
- **Z registračního formuláře** — odpověď na otázku zařadí účastníka do skupiny (nastavuje se u konkrétní odpovědi, viz *Jak fungují podmíněné otázky v registračním formuláři*).
- **Od nominátora** — nominátor může mít nastavenou výchozí skupinu pro všechny své pozvané, případně ručně přiřazovat skupiny (viz *Jak fungují nominace a nominátoři*).
- **Po zakoupení vstupenky** — vstupenka může mít nastavenou skupinu, do které se účastník po registraci automaticky zařadí (viz *Nastavení placených vstupenek*).
- **Z odkazu** — individuální a hromadné registrační odkazy mohou mít přiřazenou skupinu, do které se registrovaný automaticky zařadí.
- **Po použití slevového kódu** — kód může mít přiřazenou skupinu.

### Jak nastavit viditelnost funkce

V administraci události v sekci **Obsah** nebo **Engagement funkce** otevřete detail konkrétní funkce. V panelu **Nastavení viditelnosti** (tooltip *Omezení viditelnosti pro skupiny*) najdete:

- **všichni účastníci** (výchozí) — funkci uvidí každý.
- **Pouze pro vybrané skupiny** — otevře se pole pro výběr skupin. Funkci uvidí jen účastníci ve vybraných skupinách.

U každé obsahové funkce lze současně nastavit, zda se zobrazí na **microsite**, v **účastnické aplikaci**, nebo na obou místech. Engagement funkce se zobrazují pouze v účastnické aplikaci. Viditelnost na skupiny platí pro všechny kanály, kde se funkce zobrazuje.

### Viditelnost otázek a odpovědí

V registračním formuláři na záložce **Doplňující otázky**:

- U celé **otázky** zapněte *Zobrazit otázku pouze vybraným skupinám* a vyberte, kterým.
- U konkrétní **odpovědi** v otázce typu 2 (výběr jedné) nebo podobné zapněte viditelnost a vyberte skupiny. Takto lze například odpověď *Ano, chci VIP přístup* skrýt pro všechny kromě skupiny VIP.

### Cílení e-mailové kampaně

V **E-mailových kampaních** při vytváření kampaně zvolíte příjemce. Lze vybrat:

- Všechny účastníky události.
- Účastníky v konkrétním stavu (*Zúčastním se*, *Nezúčastním se*, *Bez odpovědi*).
- Účastníky v jedné nebo více **skupinách**.

Kombinace filtrů umožňuje cílit velmi přesně — například *všichni z Brna, kteří jsou ve stavu Zúčastním se*.

### Systémové vs uživatelské skupiny

Všechny skupiny v Happenee jsou dnes **uživatelské** — vytváří je organizátor. Systémové skupiny (automaticky vytvářené, například *Potvrzení účastníci*, *Nepřihlášení*) dnes nejsou k dispozici, tuto funkci je potřeba řešit přes ruční skupiny nebo filtrování podle stavu účastníka.

### Globální vs lokální skupiny

Skupiny jsou **globální** pro celý workspace — neexistují skupiny, které by byly vázané na jednu konkrétní událost. Pokud chcete odlišit skupiny pro různé události, pojmenujte je jednoznačně (například *Konference25_VIP*, *Workshop25_Speakers*). Lokální skupiny vázané na událost dnes nejsou k dispozici.

## Na co si dát pozor

### Organizátor chce cílit komunikaci na VIP účastníky, ale nemá skupinu VIP — účastníci jsou rozdělení podle stavu přihlášení, ne podle typu

Typ účastníka definuje **skupina**, ne stav. Založte skupinu VIP a zařaďte do ní všechny, kterých se týká (import, registrační formulář s otázkou nebo ruční přiřazení).

### Funkce je nastavená jako viditelná jen pro vybranou skupinu, ale organizátor zapomněl do skupiny zařadit všechny, pro které je určena. Část účastníků funkci nevidí

Po nastavení viditelnosti ověřte v tabulce kontaktů, kolik lidí je ve skupině. Pokud vám toto číslo nesedí s očekáváním, doplňte účastníky (ručně nebo hromadně).

### Viditelnost zapnutá pro skupinu, která dosud nemá žádné členy, kteří by funkci potřebovali. Funkce se nikomu nezobrazuje

Viditelnost platí okamžitě — pokud ve skupině není nikdo, funkci nikdo nevidí. Nejprve zařaďte členy, pak zapněte viditelnost, nebo se spokojte s dočasným *Pouze pro skupinu organizátor* (testovací skupinu) a otevřete všem, až bude obsah hotový.

### Organizátor spoléhá na to, že přiřazení do skupiny přes odpověď ve formuláři funguje i pro odpovědi vybrané před tím, než ke konkrétní odpovědi skupinu přiřadil

Automatické zařazení do skupiny funguje jen u nových odpovědí. Existující odpovědi se do skupiny **zpětně nepropíšou** — pokud jste nastavení přidali po spuštění formuláře, doplňte skupiny ručně.

### Očekávání, že skupina z jedné události zůstane jen v té události. Skupiny jsou globální a zasahují do všech událostí

Pro jednorázové skupiny použijte pojmenování s prefixem události (například *ConfApril25_VIP*). Po události skupiny ukliďte, nebo aspoň přejmenujte.

### Zvací e-mail cílený přes skupinu — ale ta funkce neexistuje

Zvací e-mail cílení přes skupiny nepodporuje, pouze umožňuje rozdělit podle stavu (nepozvaní, bez odpovědi, nepřečetli). Pro segmentaci podle skupin použijte **E-mailovou kampaň**.

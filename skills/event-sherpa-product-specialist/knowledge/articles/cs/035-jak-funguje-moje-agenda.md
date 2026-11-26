# Jak funguje Moje agenda

> Osobní rozvrh účastníka z uložených a registrovaných sessions a nastavení bloku Moje agenda na záložce Programu.

- Článek v Help Centru: https://help.happenee.com/cs/articles/35-jak-funguje-moje-agenda
- English version: https://help.happenee.com/en/articles/35-how-my-agenda-works
- Kolekce: Obsah a zkušenost účastníka
- Aktualizováno: 2026-09-16

---

> [!info] Krátce
> Moje agenda je engagement funkce účastnické aplikace: osobní rozvrh, ve kterém účastník vidí jen sessions, které si uložil, a sessions, na které je zaregistrovaný. Obsah agendy tvoří účastník sám v Programu, vy ho v administraci nevyplňujete. V administraci na záložce **Moje agenda** v Programu nastavujete jen to, jestli se blok Moje agenda zobrazí na hlavní stránce účastnické aplikace a jak bude vypadat.

## Jak začít

1. V administraci události otevřete **Obsah**, vyberte Program a přejděte na záložku **Moje agenda**. Má-li událost víc Programů, nastavte blok jen v jednom z nich.
2. Zapněte **Zobrazit na detailu události**. Ve výchozím stavu je přepínač vypnutý a blok Moje agenda se ve webové aplikaci nezobrazí.
3. V části **Zobrazení na hlavní stránce účastnické aplikace** zvolte **Základní zobrazení**, nebo **Obrázek**. U obrázku nahrajte obě varianty, pro mobilní zobrazení i pro desktop, a každou potvrďte tlačítkem **Uložit**.

## Detail

### Co Moje agenda obsahuje

Agenda skládá dohromady dva druhy sessions ze všech Programů události:

- **Uložené** — účastník si session v Programu označí ikonou záložky. Jde to u jakékoli session, tedy i u Přednášky, na kterou se neregistruje. Uložení místo nerezervuje.
- **Registrované** — Workshopy a Časové sloty, na které se účastník zaregistroval. Do agendy se přidají samy. Po zrušení registrace z agendy zmizí, pokud si účastník session zároveň neuložil.

Každý účastník má svou agendu a vy ji nevyplňujete ani needitujete. Agendu vidí jen přihlášený účastník.

### Kde se Moje agenda nastavuje

V sekci **Engagement** Moje agenda není a přidat ji tam nejde. Nastavuje se na záložce **Moje agenda** v Programu (**Obsah** → Program), která má tři nastavení:

- **Zobrazit na detailu události** — jestli se blok Moje agenda ukáže na hlavní stránce účastnické aplikace. Ve výchozím stavu je vypnuté.
- **Zobrazení na hlavní stránce účastnické aplikace** — **Základní zobrazení** (nadpis Moje agenda s ikonou záložky), nebo **Obrázek** (vaše grafika místo nadpisu).
- **Obrázky** — po volbě **Obrázek** se objeví dvě pole: obrázek pro mobilní zobrazení (doporučený rozměr 800 × 300 px) a obrázek pro zobrazení na desktopu (1250 × 300 px). Doporučený formát je JPG do 500 KB. Obrázky jsou společné pro všechny jazyky události.

Blok nemá vlastní pořadí na hlavní stránce ani vlastní viditelnost pro skupiny. Ve webové aplikaci se zobrazí přímo nad dlaždicí toho Programu, ve kterém jste ho zapnuli, a posouvá se spolu s ní.

### Jak se nastavení ukládá

Přepínač i volba zobrazení se uloží hned po změně, tlačítko pro uložení u nich není. Když se uložení nepodaří, administrace vrátí předchozí hodnotu a zobrazí chybu.

Obrázek se výběrem souboru ještě neuloží. Po výběru uvidíte náhled a tlačítka **Uložit** a **Zrušit výběr**; na server se obrázek nahraje až po kliknutí na **Uložit**. Uložený obrázek vyměníte tlačítkem **Nahrát jiný obrázek**, i ten pak potvrdíte tlačítkem **Uložit**. Tlačítko **Odebrat** obrázek po potvrzení rovnou odstraní.

### Jak to vidí účastník

**Webová aplikace.** Pokud jste blok zapnuli, je na hlavní stránce účastnické aplikace nad dlaždicí Programu. Po kliknutí se otevře seznam uložených a registrovaných sessions rozdělený po dnech. Přímo v Programu má přihlášený účastník odkaz Moje agenda a u každé session ikonu záložky, takže se k agendě dostane i s vypnutým blokem.

**Mobilní aplikace.** Pokud má událost Program, je dlaždice Moje agenda vždy nad prvním z nich a ukazuje počet sessions v agendě. Položku Moje agenda účastník najde i v menu aplikace. Uvnitř přepíná mezi záložkami Vše, Uložené a Registrované. Nastavení ze záložky Moje agenda mobilní aplikace zatím nepoužívá, takže dlaždici tam nevypnete a vlastní obrázek se v ní neukáže.

Na detailu session může účastník session hodnotit nebo klást otázky, pokud jste u ní tyto engagement funkce zapnuli.

### ICS kalendářový soubor

Je-li u typu session nebo u konkrétní session zapnuté **Odeslat ICS účastníkovi** a zároveň *Upozornění účastníkovi při změně registrace na session*, přijde účastníkovi po registraci potvrzovací e-mail s ICS souborem. Ten si naimportuje do Google Kalendáře, Apple Kalendáře nebo Outlooku. Moje agenda v aplikaci a externí kalendář pak běží vedle sebe.

### Typické use cases

**Konference s paralelními tracky.** Účastník se zaregistruje na workshopy a zajímavé přednášky si uloží. V agendě pak místo celého programu konference vidí jen svůj rozvrh.

**Rezervace (testovací jízdy, doprovodný program).** Rezervace je registrace na Časový slot, takže se objeví v agendě i s časem a místem.

**Vícedenní události.** Agenda je rozdělená po dnech a účastník mezi nimi přepíná.

### Co Moje agenda neumí

- **Přidat vlastní položku** (osobní schůzku mimo Happenee) — zobrazuje jen sessions z Programů události.
- **Exportovat celou agendu jedním souborem** — do kalendáře jdou jen jednotlivé sessions přes ICS.
- **Sdílet agendu s ostatními** — je čistě osobní.
- **Nastavit blok na hlavní stránce zvlášť pro skupiny nebo mu dát vlastní pořadí** — řídí se dlaždicí Programu.

## Na co si dát pozor

### Blok Moje agenda na hlavní stránce chybí

Přepínač **Zobrazit na detailu události** je ve výchozím stavu vypnutý, takže dokud ho nezapnete, ve webové aplikaci blok nebude. Nepřihlášený návštěvník ho neuvidí vůbec. K agendě se přihlášený účastník dostane i bez bloku, přes odkaz Moje agenda v Programu.

### Moje agenda je na hlavní stránce dvakrát

Přepínač **Zobrazit na detailu události** se nastavuje v každém Programu zvlášť a blok se zobrazí u každého Programu, kde je zapnutý. Všechny bloky přitom otevřou stejnou agendu se sessions ze všech Programů. Pokud má událost víc Programů a nechcete, aby účastníci viděli blok Moje agenda víckrát, zapněte přepínač jen v jednom z nich.

### Vybraný obrázek se neuložil

Po výběru souboru se ukáže náhled, ale uložený obrázek ještě není. Když stránku zavřete nebo z ní odejdete bez kliknutí na **Uložit**, vybraný soubor se zahodí a musíte ho vybrat znovu.

### Místo obrázku se ukazuje základní zobrazení

Webová aplikace použije obrázek jen tehdy, když jsou nahrané oba, pro mobilní zobrazení i pro desktop. Když jeden chybí, blok se zobrazí v základním zobrazení. Nahrajte proto vždy oba.

### V mobilní aplikaci se nastavení neprojevilo

Mobilní aplikace nastavení ze záložky Moje agenda zatím nečte. Dlaždice Moje agenda je v ní vždy a v základní podobě, i když jste blok vypnuli nebo nahráli obrázek.

### Obrázek jste nahráli na jiné záložce

Obrázek dlaždice samotného Programu se nastavuje na záložce **Viditelnost**, obrázek bloku Moje agenda na záložce **Moje agenda**. Jsou to dva různé obrázky a jeden nenahrazuje druhý.

### Moje agenda je v aplikaci prázdná

Agenda se plní jen tím, co si účastník uloží nebo na co se zaregistruje, takže prázdná agenda chybou není. Zkontrolujte, že je účastník přihlášený a že sessions jsou publikované a viditelné pro jeho skupinu.

### Přednáška se do agendy nepřidala

Na Přednášky se účastníci neregistrují, a proto se do agendy samy nepřidají. Účastník si je tam přidá ikonou záložky v Programu.

### Účastník zruší registraci a čeká, že agenda zachová historii

Moje agenda ukazuje aktuální stav. Zrušená registrace z ní zmizí, pokud si účastník session zároveň neuložil. Historii registrací najdete v administraci session, u Časového slotu na záložce Sloty, nebo v exportech.

### Změna se v aplikaci neukázala hned

Agenda se aktualizuje okamžitě, ale mobilní aplikace může potřebovat obnovení obsahu stažením dolů nebo restart. Ve webové aplikaci stačí obnovit stránku.

## Související články

- [Sestavení programu události — architektura](https://help.happenee.com/cs/articles/26-sestaveni-programu-udalosti-%E2%80%94-architektura)
- [Jak funguje účastnická aplikace a její hlavní stránka](https://help.happenee.com/cs/articles/34-jak-funguje-ucastnicka-aplikace-a-jeji-hlavni-stranka)
- [Nastavení workshopů a registrace na sessions](https://help.happenee.com/cs/articles/28-nastaveni-workshopu-a-registrace-na-sessions)
- [Jak fungují časové sloty](https://help.happenee.com/cs/articles/29-jak-funguji-casove-sloty)
- [Nastavení rezervací v programu — auta, workshopy, doprovodný program](https://help.happenee.com/cs/articles/30-nastaveni-rezervaci-v-programu-%E2%80%94-auta-workshopy-doprovodny-program)

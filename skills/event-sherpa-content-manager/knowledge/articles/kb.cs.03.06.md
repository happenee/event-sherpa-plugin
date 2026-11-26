<!-- source: kb.cs.03.06 -->

---
title: "Sestavení programu události — architektura"
description: "Vrstvy programu (sessions, typy, registrační bloky, místa, štítky) a jak spolu souvisí."
modules: ["program_a_sessions"]
last_updated: "2026-09-16"
version: 9
---

> [!info] Krátce
> Program je **obsahová funkce**, která tvoří časový plán události. Základní stavební jednotkou je **session** — konkrétní položka programu s časem, místem, řečníky a obsahem. Sessions jsou přiřazeny k **typům**, které určují výchozí chování (viditelnost, registraci, engagement funkce). Pro sdružování sessions s registrací slouží **registrační bloky**; **místa** a **štítky** pomáhají účastníkům orientovat se ve větším programu. Tento článek popisuje architekturu — jak jednotlivé vrstvy spolu souvisí. Detail typů, workshopů a slotů najdete v navazujících článcích.

## Jak začít

- Než začnete vytvářet sessions, **rozhodněte o architektuře** — kolik sálů, kolik tracků, kolik dnů, jestli je program s registrací nebo bez.
- Vytvořte **Program** v **Obsahu** (pokud ho ještě nemáte).
- **Pořadí tvorby:** typy sessions → místa (pokud máte víc sálů) → štítky → sessions → registrační bloky (pokud jsou potřeba).
- Čas session se zadává v časovém pásmu události (viz *Vytvoření nové události*).

## Detail

### Přidání obsahové funkce Program

1. V levém menu → **Obsah** → **+ Přidat** → **Program**.
2. Obsahová funkce se přidá do seznamu obsahových funkcí v sekci Obsah a záložka **Sessions** se zpřístupní. Vedle ní se zobrazí záložky **Typy**, **Bloky**, **Štítky**, **Místa**, **Moje agenda**, **Nastavení**, **Viditelnost** a **Import**.

> Obsahovou funkci Program lze do události přidat **vícekrát**. Každá instance má vlastní sessions, typy, místa a štítky. Příklad: *Hlavní program*, *Workshopy*, *Doprovodný program* — tři samostatné Programy.

### Základní prvky architektury

**Sessions** — konkrétní položky programu. Každá session má:

- Název
- Datum, začátek, konec
- Typ (povinný — viz dále)
- Volitelně: místo, štítky, popis, řečníky, sponzory a vystavovatele

**Typy** — šablony výchozího chování. Každá session musí být přiřazena k typu. Happenee obsahuje **čtyři základní typy chování**:

- **Přednáška** — viditelná pro všechny, bez registrace. Keynote, prezentace.
- **Workshop** — účastníci se registrují na jednotlivé workshopy. K registraci jsou dostupné všechny, které jsou pro ně viditelné.
- **Časové sloty** — účastník si vybere jeden z nabízených slotů (rezervace konkrétního času).
- **Přestávka** — informativní položka bez detailu, registrace a engagementu.

Z těchto čtyř typů lze vytvořit vlastní typy (*Keynote*, *Panel*, *Masterclass*) — každý vychází z jednoho ze čtyř základních chování. Detail v článku *Jak fungují typy sessions*.

**Registrační bloky** — sdružují sessions s registrací (typy Workshop a Časové sloty) a určují, kolik sessions z bloku si účastník může zapsat. Příklad: blok *Dopolední workshopy* obsahuje tři workshopy, *Maximální počet sessions z bloku na účastníka* = 1 → účastník si zvolí jeden ze tří.

**Místa** — konkrétní prostory nebo stage. Přiřazují se k sessions a slouží jako filtr v aplikaci i na microsite.

**Štítky** — tematické značky (například *AI*, *Marketing*, *Leadership*). Slouží k filtrování a doporučování obsahu v aplikaci.

### Dědičnost nastavení

Typ session určuje výchozí chování pro **registraci**, **viditelnost** a **engagement funkce** (hodnocení, otázky, hlasování). Každá session tato nastavení **automaticky přebírá**, ale lze je u konkrétní session **přepsat**.

> ⚠️ Změna nastavení typu se promítne do všech sessions, které dané nastavení dědí (přepínač ve stavu **Výchozí**) — včetně už existujících. Sessions přepnuté na **Vlastní** jsou od typu odpojené a změnu nedostanou.

### Vytvoření nové session (přehled)

Panel úprav **Nová session** má pět záložek (u typu Časový slot šest):

- **Informace** — název, datum, čas, typ, blok, místo, štítky, poznámka organizátora.
- **Viditelnost** — převzít z typu, nebo nastavit vlastní (veřejné / pouze pro vybrané skupiny).
- **Obsah** — popis session, obrázek, odkaz na videohovor, engagement nastavení (hodnocení, otázky, hlasování).
- **Řečníci** — přiřazení řečníků a moderátorů (viz *Správa řečníků*).
- **Partneři** — přiřazení sponzorů a vystavovatelů k session.
- **Sloty** (pouze u typu Časový slot) — přehled vygenerovaných slotů a účastníků.

Detail vytváření sessions podle typu najdete v navazujících článcích.

Sessions lze také zakládat **hromadně z Excelu** přes záložku **Import** v Programu — viz *Hromadný import sessions*.

### Scénáře

**Program bez registrace** (přednáškový formát). Všechny sessions typu **Přednáška**. Registrační bloky ani místa nepotřebujete — stačí sessions a čas. Vhodné pro konferenci, meetup.

**Workshopy s volnou registrací.** Sessions typu **Workshop** bez registračních bloků. Účastník se přihlásí na libovolný počet workshopů. Nastavte kapacitu (**Omezit počet registrací**) a případně **Časové omezení registrace** a **Odhlášení ze session**.

**Workshopy s omezeným výběrem.** Sessions typu **Workshop** + **Registrační bloky**. Každý blok obsahuje 3–5 workshopů, maximální počet = 1. Účastník si musí vybrat jeden z nabídky. Typické pro vícekolový workshopový formát.

**Individuální schůzky a časové sloty.** Sessions typu **Časové sloty**. Session má definovanou délku (například 60 minut), která se rozdělí na 15minutové sloty. Účastník si vybere konkrétní slot. Vhodné pro one-to-one meetingy, testovací jízdy aut, rezervace (detail v *Nastavení rezervací v programu — auta, workshopy, doprovodný program*).

**Kombinovaný program.** Mix typů v jedné události. Keynote jako Přednáška, workshopy jako Workshop, individuální schůzky jako Časové sloty, pauzy jako Přestávka.

### Víceobrazovkový program

U velké konference s více sály a paralelními tracks:

1. Vytvořte **Místa** — jedno pro každý sál.
2. Vytvořte **typy sessions** nebo použijte **Štítky** pro rozlišení tracks (například *Business Track*, *Tech Track*).
3. Zapněte filtry **Místo** a **Štítky** v záložce **Nastavení** programu.
4. V nastavení programu u **Povolit souběžné registrace v rámci tohoto Programu** zvažte, zda má smysl — u konference ano, u workshopů obvykle ne.

### Souběžné registrace

Ve výchozím stavu se účastník **nemůže zaregistrovat na dvě sessions, jejichž časy se překrývají**. Platí to uvnitř jednoho Programu i napříč všemi Programy v události. Omezení uvolníte v záložce **Nastavení** programu dvěma nezávislými přepínači:

- **Povolit souběžné registrace v rámci tohoto Programu** — účastník se může přihlásit na překrývající se sessions, pokud jsou obě v tomto Programu.
- **Povolit souběžné registrace mezi Programy** — účastník se může ve stejný čas zaregistrovat na sessions z různých Programů. Přepínač musí být zapnutý **v obou Programech**; když ho má zapnutý jen jeden z nich, omezení mezi nimi dál platí.

Nad přepínači administrace vypíše, co aktuální kombinace pro účastníky znamená. Když zapnete druhý přepínač a zrušíte tím všechna omezení, systém se nejdřív zeptá, jestli to opravdu chcete. Vypnutí přepínače se uloží bez dotazu.

Jak systém překryv posuzuje:

- **Kolidují jen časy, které se skutečně protínají.** Sessions, které na sebe navazují (jedna končí v 11:00, další v 11:00 začíná), se nepřekrývají.
- **U časového slotu se počítá čas slotu**, ne celé session. Přepnutí na jiný slot téže session původní registrace neblokuje.
- **Počítají se jen platné registrace.** Zrušená registrace nic neblokuje.
- **Kontrola platí jen pro registraci, kterou udělá účastník sám.** Když účastníka přidáte ručně na záložce **Účastníci** nebo v dialogu **Upravit účastníky** u slotu, systém překryv nehlídá.
- **Změna nastavení se nepropisuje zpětně.** Když přepínač vypnete a omezení tím zase platí, registrace, které se už překrývají, zůstanou. Nic se neruší.

Účastník, kterého by registrace dostala do překryvu, uvidí tlačítko **Registrovat** neaktivní. V prohlížeči se po najetí myší ukáže důvod: *V tomto čase už máte registraci na jiné session.*

### Nastavení zobrazení

Záložka **Nastavení** programu obsahuje kromě souběžných registrací také sekci **Nastavení zobrazení** — přepínače, které řídí, jak se program zobrazuje účastníkům:

- **Zobrazit čas u session** — zobrazí začátek a konec vedle karty session v programu.
- **Zobrazit časové pásmo** — zobrazí informaci o časovém pásmu u termínu session. Užitečné u online a hybridních událostí s účastníky z více zemí.
- **Zobrazit datum v detailu session** — zobrazí datum konání v hlavičce detailu session. Hodí se u vícedenních událostí, kde samotný čas nestačí.
- **Rozbalit časové sloty v programu** — časové sloty se zobrazí přímo na kartě session v přehledu programu, takže účastník vybírá čas bez otevírání detailu (viz *Jak fungují časové sloty*).

> Zobrazení programu na microsite události se nastavuje samostatně v sekci **Microsite**.

### Ukládání záložky Nastavení

Záložka **Nastavení** nemá tlačítko **Uložit**. Každou změnu přepínače i nové pořadí filtrů systém uloží hned a potvrdí to hláškou. Když se uložení nepodaří, přepínač se vrátí do poslední uložené polohy a zobrazí se chyba. Stejně se ukládají přepínač a volba zobrazení na záložce **Moje agenda**. Tlačítko zůstalo na dvou místech: přejmenování filtru potvrzujete tlačítkem **Uložit** v bočním panelu a na záložce **Viditelnost** ukládáte název a skupiny tlačítkem **Uložit změny**.

### Viditelnost na microsite a v aplikaci

Všechny obsahové funkce (včetně Programu) mají samostatné přepínače zobrazení pro microsite a účastnickou aplikaci. Sessions se v aplikaci zobrazují v chronologickém pořadí; sessions se stejným časem začátku se řadí podle pořadí typů (viz [Jak fungují typy sessions](07_jak-funguji-typy-sessions.md)). Registrace na sessions typu **Workshop** a **Časový slot** je dostupná **pouze v účastnické aplikaci** — přes microsite se účastník nemůže na workshop přihlásit.

## Na co si dát pozor

### Organizátor vytvoří všechny sessions jako *Přednáška*, i když pro některé chtěl registraci. Účastníci nemají jak se přihlásit

Rozhodněte typ **před** vytvářením. Pro registraci volte **Workshop** (libovolný počet) nebo **Časové sloty** (konkrétní čas).

### Změna nastavení typu (například kapacity) se nepropíše do sessions přepnutých na *Vlastní*

Změna se promítne do sessions, které dané nastavení dědí (přepínač ve stavu **Výchozí**) — včetně existujících. Sessions, u kterých jste dané nastavení přepnuli na **Vlastní**, se od typu odpojily a změnu nedostanou; ty musíte srovnat samostatně u jednotlivých sessions — viz [Správa sessions](21_sprava-sessions.md).

### Program s paralelními sessions, ale bez míst. Účastník nerozumí, kde se co děje

U programu s paralelními tracks vždy vytvořte **Místa** a přiřaďte je k sessions. Účastník pak může filtrovat program podle sálu.

### Organizátor zapíná *Souběžné registrace* bez promyšlení — účastník se přihlásí na dvě sessions ve stejném čase a nezvládne obě

*Souběžné registrace* povolte jen tam, kde je to žádoucí (registrace na konferenci + poster session; workshop + doprovodný program). U klasických workshopů ponechte výchozí omezení.

### Souběžné registrace mezi Programy zapnete jen v jednom Programu a účastník se pořád nezaregistruje

Volba mezi Programy platí, jen když ji mají zapnutou oba Programy. Zkontrolujte **Nastavení** u obou.

### Omezení vrátíte až po otevření registrace a čekáte, že překryvy zmizí

Vypnutý přepínač hlídá jen nové registrace. Kdo se mezitím přihlásil na dvě sessions ve stejném čase, zůstane registrovaný na obou. Projděte registrované účastníky dotčených sessions a překryvy s nimi vyřešte, případně je z jedné session ručně odeberte.

### Sessions typu Časový slot vytvořeny, ale účastník nevidí sloty v aplikaci

Sloty se generují při uložení session z pole **Délka časového slotu** a **Délka přestávky**. Zkontrolujte tato pole. V záložce **Sloty** session vidíte vygenerované sloty a jejich obsazenost.

### Snaha změnit typ session po registraci prvního účastníka. Systém nedovolí

Po registraci prvního účastníka na session typu **Časový slot** **nelze** změnit typ, čas začátku a konce, délku slotu ani délku přestávky. Plánujte dopředu.

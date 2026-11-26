<!-- source: kb.cs.03.10 -->

---
title: "Nastavení rezervací v programu — auta, workshopy, doprovodný program"
description: "Jak přes časové sloty a workshopy řídit rezervační scénáře typu testovací jízdy nebo doprovodný program."
modules: ["program_a_sessions"]
last_updated: "2026-09-09"
version: 5
---

> [!info] Krátce
> Program v Happenee neslouží jen k přednáškám — přes **časové sloty** a **workshopy** lze řídit i **rezervační scénáře**: testovací jízdy aut, doprovodný program (let balonem, golfová akademie, relaxační zóna), půjčování vybavení nebo individuální schůzky s experty. Mechanika je vždy stejná — session typu Časový slot se rozdělí na sloty, účastník si jeden vybere. Tento článek ukazuje, **jak mapovat reálné use cases na strukturu programu**.

## Jak začít

- Vyjmenujte si, **co všechno chcete účastníkovi nabídnout k rezervaci** — konkrétní stroje/aktivity, dostupné časy, kapacity.
- Každá rezervovatelná aktivita = jedna **session typu Časový slot** (nebo několik).
- Pro větší nabídku (3 auta + 4 aktivity doprovodného programu) vytvořte **samostatné Programy** — *Testovací jízdy*, *Doprovodný program*. Program (obsahová funkce) lze přidat vícekrát.
- Každý zdroj (auto, instruktor, vybavení) obvykle = jedna session. Nemixujte je do jedné session s vyšší kapacitou — ztratíte kontrolu nad individuálním obsazením.

## Detail

### Proč Program pro rezervace

Happenee nemá samostatný rezervační modul. Místo toho používá **Program** a jeho mechaniku **časových slotů**. Výhody:

- Účastník vidí rezervace v **Moje agenda** jako součást svého programu.
- Stejné filtry (místo, štítky, typ) fungují i pro rezervace.
- Získává **potvrzovací e-mail** včetně ICS souboru (lze přidat do kalendáře).
- Rezervační sloty lze kombinovat s programovými sessions — účastník si vybírá z jednoho pohledu.

### Typické use cases

**Testovací jízdy aut (exteriérová událost automobilky).**
Každé auto = jedna session. Délka session = čas od–do, kdy lze auto rezervovat (například 9:00–17:00). Délka slotu = délka jedné jízdy + prostoru na výměnu (například 20 minut). Délka přestávky = čas na doplnění paliva / reset (5 minut).

Struktura: Program *Testovací jízdy* → sessions *Mercedes GLE*, *Mercedes EQS*, *Mercedes AMG GT*, každá se svými sloty.

**Doprovodný program na konferenci nebo firemní událost.**
Každá aktivita = jedna session. Let balonem (1 session, 3 sloty ráno), golfová akademie (1 session, sloty každou hodinu), vizážistka (1 session, 15min sloty), relaxační masáž (1 session, 30min sloty).

Struktura: Program *Doprovodný program* → sessions *Let balonem*, *Golfová akademie*, *Vizážistka*, *Masáž*, každá se svými sloty a kapacitou.

**Individuální konzultace (networking nebo odborný program).**
Každý konzultant = jedna session. Například *One-to-one s CFO*, *Konzultace s CMO*, *Mentoring s interním expertem*. 15–30min sloty.

**Půjčování vybavení (kolo, notebook, zážitkový kufr).**
Každý kus vybavení = jedna session. Délka slotu odpovídá délce půjčky. Kapacita = 1 (jedno vybavení nemůže mít víc lidí současně).

### Mapování reálných use cases na parametry

Pro každou aktivitu si určete:

- **Kolik kusů / instruktorů / zařízení máte?** — Počet sessions
- **V jakém čase je aktivita dostupná?** — Začátek a konec session
- **Jak dlouho trvá jedna rezervace?** — Délka časového slotu
- **Kolik času potřebujete mezi rezervacemi?** — Délka přestávky
- **Kolik lidí se vejde do jednoho slotu?** — Omezit počet registrací
- **Má se aktivita zobrazit jen někomu?** — Viditelnost (skupiny)

Příklad: testovací jízda v Mercedesu EQS, dostupný mezi 9:00 a 17:00, jedna jízda 20 minut, 10 minut na výměnu (včetně instruktáže), jeden řidič na jízdu, jen pro klienty:

- Session typu Časový slot, čas 9:00–17:00
- Délka slotu 20 min, přestávka 10 min
- Omezit počet registrací = 1
- Viditelnost: Pouze pro vybrané skupiny → *Klienti*

Systém vygeneruje přibližně **16 slotů** (9:00, 9:30, 10:00, …, 16:30).

### Organizační tip: místa a instruktoři jako Místa a Řečníci

Pokud se aktivity odehrávají **na různých místech**, využijte funkci **Místa** (záložka v Programu). Každé místo = sál, stan, parkoviště, plocha. Přiřaďte je k sessions — účastník pak vidí, kam má jít.

Pokud má aktivita **konkrétního instruktora nebo experta**, přidejte ho do **Řečníků** a přiřaďte k session. Účastník uvidí jméno a profil na detailu slotu.

### Seznam v aplikaci

V účastnické aplikaci se Program zobrazí jako seznam sessions v chronologickém pořadí; sessions se stejným časem začátku se řadí podle pořadí typů (viz [Jak fungují typy sessions](07_jak-funguji-typy-sessions.md)). Filtry (**Typ**, **Místo**, **Štítky**) pomáhají účastníkovi najít, co ho zajímá. Sessions typu Časový slot jsou vizuálně odlišeny — účastník vidí, že jde o rezervaci.

### Kombinace s engagement funkcemi

K sessions lze přiřadit:

- **Hodnocení session** (engagement funkce) — po rezervaci účastník hodnotí (jen pokud je zapnuté na úrovni typu nebo session).
- **Otázky** — před aktivitou si může klást dotazy (například *Mám si přivézt vlastní helmu?*).

### Exporty a reporting

Na úrovni session lze vyexportovat registrace do Excelu — kdo si rezervoval jaký slot. Po události vám to dá přehled, kdo co absolvoval.

## Na co si dát pozor

### Jedna session s kapacitou 3 pro „testovací jízdy“ — organizátor si myslí, že účastníci se rozdělí mezi 3 auta

Každý zdroj (auto, instruktor) = **samostatná session**. Kapacita 3 znamená, že 3 lidi přijdou ve stejný čas na stejné místo.

### Délka slotu nepočítá s časem na předání / reset. Lidé se překrývají, další čeká

Počítejte **realistickou délku + buffer**. Testovací jízda 15 min = slot 20 min. Masáž 30 min = slot 45 min (převlékání, dotazy). Délku slotu vybíráte z pevné nabídky (10, 15, 20, 30, 45, 50, 60, 90 nebo 120 minut), buffer proto zaokrouhlete nahoru na nejbližší nabízenou hodnotu. Detail v článku *Jak fungují časové sloty*.

### Doprovodný program v jednom Programu s hlavním programem konference. Účastník se ztrácí v seznamu

Pro jasnou separaci vytvořte **samostatný Program** *Doprovodný program*. Program je obsahová funkce, lze mít víc instancí. Každý Program má vlastní seznam, filtry a nastavení.

### Auto v servisu v polovině dne, ale slot zůstává rezervovatelný — účastník se přijde zaregistrovat a zjistí problém

V záložce **Sloty** u session přepněte konkrétní sloty na **Neaktivní**. Blokují registraci, ale zůstanou ve struktuře pro přehled.

### Kapacita otevřená všem, ale aktivity jsou exkluzivní pro VIP — běžní účastníci se zapisují a místo nezbyde

Nastavte **Viditelnost: Pouze pro vybrané skupiny** nebo **Registrace pouze pro vybrané skupiny** u celé session. Detail v článku *Nastavení workshopů a registrace na sessions*.

### Změna délky slotu po první rezervaci — systém nedovolí

Délka slotu, přestávky a čas session jsou po první registraci **zamčené**. Plánujte rozvrh pečlivě, otestujte na zkušebním účtu před spuštěním pro účastníky.

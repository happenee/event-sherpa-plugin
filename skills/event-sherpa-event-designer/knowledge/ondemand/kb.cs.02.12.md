<!-- source: kb.cs.02.12 -->

---
title: "Nastavení Seatingu"
description: "Placená pokročilá funkce pro přiřazování konkrétních sedadel ve vymodelovaném prostoru."
modules: ["registrace"]
last_updated: "2026-04-27"
version: 1
---

> [!info] Krátce
> Seating je **placená pokročilá funkce**, kterou zapíná **customer success**. Umožňuje přiřadit konkrétní sedadla konkrétním účastníkům ve vymodelovaném prostoru (O2 arena, Rudolfinum nebo libovolný prostor na míru). Důležitý princip: **účastník si sedadlo nevybírá sám** — po jeho registraci organizátor (nebo pověřené asistentky) sedadla přiřazují, a teprve poté se vygeneruje vstupenka s číslem sedadla.

## Jak začít

- Seating je **placená funkce přes zákaznickou podporu** / customer success. Pokud ji chcete použít, oslovte svůj CS kontakt s předstihem.
- Připravte si **půdorys prostoru** — Happenee má vymodelované O2 arénu a Rudolfinum, jiné prostory se modelují na zakázku.
- Rozhodněte, kdo bude přiřazovat sedadla — jeden organizátor, víc asistentek v zónách, nebo skriptové hromadné rozdělení.
- Nastavení seatingu není samoobslužné v administraci — Happenee tým připravuje prostor, zóny a přístupy.

## Detail

### Jak seating funguje v Happenee

Seating v Happenee je **obrácený proces** oproti veřejnému prodeji vstupenek s vlastním výběrem sedadla:

- Účastník se **nejdřív zaregistruje** (normálně, bez výběru sedadla).
- Po registraci organizátor nebo pověřená asistentka **přiřadí sedadlo** v administraci seatingu.
- Až po přiřazení se vygeneruje **finální vstupenka** s číslem sedadla.

Účastník tedy v procesu nákupu ani registrace sedadlo nevybírá. To je záměrné — Happenee se soustředí na korporátní událost, kde sedačkové uspořádání řídí organizátor (typicky podle interní logiky: obchodní tým sedí u svých klientů, management má VIP místa, atd.).

### Vymodelované prostory

V systému jsou hotové:

- **O2 arena** (Praha).
- **Rudolfinum** (Praha).

Další prostory může Happenee vymodelovat na zakázku. Oslovte customer success, pošlete půdorys (v rozumné přesnosti) a tým vytvoří digitální model prostoru včetně sekcí, řad a sedadel.

### Způsoby přiřazování sedadel

**Jedna osoba přiřazuje ručně.** Jednoduchý scénář — organizátor prochází seznamem účastníků a přetahuje je na sedadla v digitálním plánu prostoru. Vhodné pro menší události nebo událost s jasnou hierarchií.

**Hromadné rozdělení skriptem.** Pro velké události lze načíst seznam účastníků a systém je automaticky rozmístí. Používá se například u konferencí, kde pořadí nerozhoduje.

**Zónové rozdělení s více asistentkami.** Prostor se rozdělí na **zóny** (například *Sekce A*, *Sekce B*, *VIP sekce*) a každá asistentka má přístup pouze do své zóny. Každá pak rozmisťuje účastníky ze *svého* seznamu do svých sedadel. Vhodné pro velké korporátní události, kde různé týmy řeší různé části prostoru.

### Kdy se vygeneruje vstupenka se sedadlem

Vstupenka s konkrétním číslem sedadla se generuje **až po** přiřazení. Před tím má účastník běžnou vstupenku bez čísla (nebo vůbec žádnou, pokud tak nastavíte). Plán:

1. Účastník se zaregistruje → dostane běžný potvrzovací e-mail (bez čísla sedadla).
2. Organizátor nebo asistentka přiřadí sedadlo v seatingu.
3. Po přiřazení se vygeneruje vstupenka s **číslem sedadla, řady a sekce**.
4. Happenee odešle nový e-mail s touto vstupenkou, nebo ji účastník najde ve své účastnické aplikaci.

Časování odeslání vstupenek obvykle organizátor zvolí — často až těsně před událostí, aby se vyhnul přesunům, když někdo odpadne.

### Kombinace s placenými vstupenkami

Seating lze zapojit i do prodeje vstupenek, ale prodejní krok zůstává stejný jako u běžných placených událostí — účastník si **neurčuje místo**. Vstupenky se rozlišují typem (standard / VIP / partner), a podle typu je potom asistentka přiřadí do odpovídající zóny.

### Ceník a aktivace

Seating je **placená pokročilá funkce**. Není zahrnutá ve standardním plánu Happenee. Aktivace probíhá přes customer success:

1. Oslovte svůj customer success kontakt.
2. Pošlete základní informace o události — počet účastníků, prostor, termín.
3. Happenee tým zhodnotí požadavky, případně vymodeluje nový prostor.
4. Po aktivaci se seating objeví jako samostatná sekce v menu události.

## Na co si dát pozor

### Očekávání, že si účastník vybere sedadlo v nákupním procesu (jako v komerčním ticketingu typu Ticketportal)

Seating v Happenee je obrácený — účastník se zaregistruje, organizátor rozmístí. Pokud potřebujete volný výběr sedadla kupujícím, Happenee není správný nástroj.

### Snaha spustit seating v samoobslužné administraci bez oslovení customer success

Seating není samoobslužný. Dokud ho neaktivuje CS tým, v administraci události ho neuvidíte. Oslovte svůj kontakt s dostatečným předstihem (minimálně měsíc u vymodelovaných prostor, více u nových).

### Vytvoření vstupenek bez promyšlení typů. V rámci přiřazování sedadel pak asistentky nevědí, kdo má VIP, kdo standard

Typy vstupenek (standard / VIP / partner) definujte tak, aby byly jasně rozlišitelné. Pokud jdou vstupenky do různých zón, propojte typ vstupenky s typem zóny.

### Odeslání vstupenek se sedadly hned po přiřazení, ale před událostí se skladba účastníků mění a některá sedadla se musí měnit

Odesílání finálních vstupenek plánujte na **co nejpozdější termín** před událostí. Pokud pošlete brzo a pak přeorganizujete, účastník bude mít zmatek nebo dojde ke konfliktu u vchodu.

### Zónová distribuce bez jasných pravidel, kdo má do jaké zóny přístup. Asistentky rozmisťují do stejných míst, vzniká konflikt

Před spuštěním seatingu jasně rozdělte zóny mezi asistentky. Každá zóna = jedna odpovědná osoba. Při konfliktu (dva účastníci ve stejném sedadle) se systém obrátí na organizátora.

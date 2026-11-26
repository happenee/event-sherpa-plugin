<!-- source: kb.cs.05.04 -->

---
title: "Příprava servisní aplikace před událostí"
description: "Co zařídit dřív, než personál poprvé naskenuje QR kód — účty pro obsluhu, instalace aplikace, místa check-inu, párování tiskárny a zkušební sken."
modules: ["checkin_a_tisk_jmenovek"]
last_updated: "2026-11-04"
version: 2
---

> [!info] Krátce
> Servisní aplikace (Happenee Service) je nástroj, kterým obsluha na místě skenuje QR kódy a odbavuje účastníky. Většina problémů u vstupu nevzniká v den události, ale z toho, co se nestihlo předem — **účty pro personál**, **nastavená místa check-inu**, **spárovaná tiskárna** a **zkušební sken**. Tenhle článek shrnuje přípravu; samotné odbavení popisuje článek o check-inu.

## Jak začít

Přípravu rozdělte na dvě části podle toho, jak dlouho trvá:

**Nejméně týden předem** (potřebuje zákaznickou podporu nebo logistiku):

1. Objednejte **účty pro obsluhu** — zapíná je customer success, není to samoobslužné.
2. Pokud budete tisknout jmenovky, zajistěte **tiskárnu** — vlastní, nebo z půjčovny přes zákaznickou podporu (počítejte s lead time kolem deseti dnů).

**Dva až tři dny předem** (zvládnete sami):

3. Nastavte v administraci **místa check-inu** a jejich typy.
4. Nechte obsluhu **nainstalovat aplikaci** a přihlásit se — ne až ráno na místě.
5. Udělejte **zkušební sken** a **testovací tisk** jmenovky.

## Detail

### Účty pro obsluhu

Personál se do servisní aplikace přihlašuje vlastními účty. Ty zapíná customer success — domluvte je s předstihem, ideálně týden. Nouzově se dá obsluha přihlásit pod administrátorským účtem, ale pak v datech neuvidíte, kdo koho odbavil, a sdílíte přístup do celé administrace. Pro jednorázovou malou událost to projde, pro konferenci s několika stanovišti ne.

### Místa check-inu

Než obsluha aplikaci otevře, musí v administraci existovat **místa**, mezi kterými bude vybírat. Každé místo má typ, který určuje chování při skenování — **Příchod**, **Odchod**, **Kontrola jednorázově** a **Kontrola opakovaně**.

Připravte si je podle skutečného rozvržení události: hlavní vstup jako *Příchod*, výdej dárku jako *Kontrola jednorázově*, vstup do sálu nebo nástup do autobusu jako *Kontrola opakovaně*. Aplikace pak obsluze nabízí názvy míst, ne typy — pojmenujte je tak, aby personál poznal, kde stojí (*Hlavní vstup*, *Šatna*, *Autobus 1*).

### Zobrazení skupin při skenování

V administraci události otevřete **Odbavení na místě** a v nastavení **Zobrazení skupiny po naskenování účastníka** vyberte skupiny, které má obsluha vidět, například VIP nebo řečníky. Tento výběr platí **po skenu i v detailu účastníka** v servisní aplikaci. Účastník musí mít skupinu také přiřazenou; ostatní skupiny z workspace se automaticky nezobrazují.

Při zkušebním skenu ověřte i případné omezení skupiny na konkrétní místa. Prázdný výběr míst znamená všechna místa. Otevřete také detail účastníka: tam se omezení na místa neuplatňuje a uvidíte všechny jeho skupiny vybrané k zobrazení.

### Instalace a přihlášení

Aplikaci nechte obsluhu nainstalovat a přihlásit se **před dnem události**. Ráno u vstupu se řeší stahování aplikace, zapomenutá hesla a slabá wi-fi nejhůř. Zároveň si ověříte, že účty opravdu fungují — což je informace, kterou chcete mít několik dní předem, ne deset minut před příchodem prvních hostů.

Při spuštění obsluha vybere událost, **režim** (*Režim obsluhy* pro skenování personálem, *Kiosk režim* pro samoobslužné stanoviště) a **místo check-inu**, případně spáruje tiskárnu.

### Párování tiskárny

Tiskárnu jmenovek spárujete přímo v aplikaci přes Bluetooth. Bez ní check-in normálně funguje, jen se netiskne. Párování a velikosti štítků popisuje článek [Tisk jmenovek](02_tisk-jmenovek.md).

Vytiskněte si **testovací jmenovku** ještě před událostí. Ověříte tím nejen tiskárnu, ale i to, že se na štítek vejde nejdelší jméno a název firmy, které v datech máte.

### Zkušební sken

Poslední krok přípravy: zaregistrujte sami sebe (nebo kolegu) a projděte celou cestu — potvrzovací e-mail, QR kód, sken v aplikaci, tisk jmenovky. Zabere to pět minut a odhalí většinu problémů, které by jinak vyšly najevo před frontou lidí.

## Na co si dát pozor

### Účty pro personál se řeší den před událostí

Zapínají se přes customer success, ne v administraci — a když napíšete v pátek odpoledne na sobotní událost, nemusí to vyjít. Objednejte je ve stejnou chvíli, kdy domlouváte tiskárnu, tedy zhruba týden předem.

### Aplikace se instaluje až na místě

Obsluha přijde hodinu před otevřením, stahuje aplikaci přes přetíženou wi-fi a zjišťuje, že si nepamatuje heslo. Instalaci i první přihlášení nechte proběhnout doma, klidně o pár dní dřív.

### Místa se pojmenují podle typu, ne podle reality

Když se místo jmenuje *Kontrola opakovaně*, personál u šatny neví, jestli je to ono. Názvy volte podle fyzického místa — *Hlavní vstup*, *Šatna*, *Recepce B* — typ chování je věc nastavení, ne názvu.

### Testovací sken se přeskočí

Bez zkušebního průchodu se první chyba objeví ve chvíli, kdy před vámi stojí dvacet lidí. Projděte si celou cestu od registrace po tisk jmenovky, ideálně na stejném zařízení, které bude na místě.

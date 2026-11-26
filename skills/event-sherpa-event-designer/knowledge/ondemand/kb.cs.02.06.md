<!-- source: kb.cs.02.06 -->

---
title: "Jak fungují podmíněné otázky v registračním formuláři"
description: "Podmíněné otázky se zobrazí jen po vybrané odpovědi, takže formulář zůstává krátký."
modules: ["registrace"]
last_updated: "2026-04-27"
version: 1
---

> [!info] Krátce
> Podmíněné otázky umožňují zobrazit další otázku až v okamžiku, kdy účastník zvolí konkrétní odpověď. Formulář tak zůstává krátký pro ty, kterých se další otázka netýká, a ptá se jen tam, kde to dává smysl. Podmíněné otázky jsou jedna z nejčastějších oblastí, kde organizátoři dělají chyby — hlavně v kombinaci s viditelností na skupiny.

## Jak začít

- Vyjmenujte si, které otázky mají smysl pro všechny a které jen pro část účastníků. Typický příklad: když někdo přijede autem, netýkají se ho otázky o autobusu.
- Podmíněné otázky se přidávají **pod konkrétní odpověď** nadřazené otázky, ne jako samostatná otázka.
- Pracují jen u otázky typu **2** (výběr jedné), **3** (výběr jedné nebo vlastní text) a jiných typů, které mají diskrétní odpovědi.
- Před nastavením zkontrolujte, zda nemáte čekat, až bude na scéně daná otázka — podmínky navazují na konkrétní odpověď, kterou musíte už mít v seznamu.

## Detail

### Dvě odlišné věci, které se snadno zamění

V Happenee se v registračním formuláři potkávají dva mechanismy, které vypadají podobně, ale fungují jinak:

- **Podmíněné otázky** — otázka se zobrazí účastníkovi až poté, co vybere konkrétní odpověď u nadřazené otázky. Kontrola je okamžitá, v samotném formuláři.
- **Viditelnost otázek pro skupiny** — otázka se zobrazí pouze účastníkům zařazeným do vybraných skupin. Kontrola proběhne na začátku (účastník je/není ve skupině), než formulář začne.

Podmíněné otázky reagují na **aktuální chování účastníka ve formuláři**. Viditelnost na skupiny reaguje na **to, kdo účastník je** (jeho zařazení ve workspace nebo po registraci).

### Jak přidat podmíněnou otázku

1. V záložce **Doplňující otázky** otevřete otázku, pod kterou chcete podmínku přidat (typicky otázka typu 2 — výběr jedné).
2. V seznamu odpovědí najděte **konkrétní odpověď**, na kterou chcete navázat.
3. U této odpovědi je sekce **Podmínky** / **Při zvolení této odpovědi se zobrazí další otázka**.
4. Přidejte novou otázku — vyberte typ, nazvěte ji, případně přidejte další odpovědi.

Podmíněná otázka je vnořená pod odpověď. Pokud účastník vybere jinou odpověď, podmíněná otázka se mu nezobrazí.

### Jak to vidí účastník

Účastník otevře formulář a vidí jen první (nadřazenou) otázku. Jakmile vybere odpověď, pod ní se **dynamicky objeví** další otázka(y). Pokud vybere jinou odpověď, otázky pod ní zmizí a místo nich se ukážou ty navázané na novou odpověď.

### Praktický příklad

**Nadřazená otázka (typ 2):** *Odkud přijedete?*
- *Praha* — žádná podmíněná otázka.
- *Brno* — podmíněná otázka: *Dorazíte společným autobusem?* (typ 2, odpovědi *Ano / Ne*).
  - *Ano* — podmíněná otázka: *Který autobus?* (typ 6 s limitem kapacity).
  - *Ne* — žádná další otázka.
- *Jiné* — podmíněná otázka: *Upřesněte místo odjezdu* (typ 1, volný text).

Účastník z Prahy vidí jen první otázku. Účastník z Brna vidí první + případně autobus. Podmínky se mohou řetězit do více úrovní.

### Viditelnost jednotlivých odpovědí

U otázky typu 2 (a dalších s diskrétními odpověďmi) lze **konkrétní odpověď** ukázat jen některým skupinám. Příklad: otázka *Chcete přístup do VIP loungu?* s odpovědí *Ano* viditelnou jen pro skupinu **VIP**. Ostatní účastníci odpověď *Ano* ani nevidí.

Rozdíl oproti viditelnosti celé otázky: skryjete jen jednu odpověď, ne celou otázku.

### Přiřazení do skupiny podle odpovědi

Každá odpověď u otázky typu 2 může mít nastavené **Zařadit do skupiny**. Když účastník zvolí tuto odpověď, systém ho automaticky přidá do uvedené skupiny. Skupinu přitom musíte předem vytvořit v **Kontaktech a skupinách**.

Příklad: odpověď *Brno* → zařadí do skupiny **Brno**. Potom můžete cílit e-mailovou kampaň *Informace pro cestující z Brna* jen na tuto skupinu.

Tohle je také nejefektivnější cesta, jak kategorizovat účastníky podle jejich odpovědí, aniž byste to museli řešit ručně po registraci.

### Náhled a struktura

V administraci formuláře je tlačítko **Náhled formuláře** (formulář jako účastník) a **Struktura otázek** (přehled všech otázek a jejich podmínek ve stromové formě). Před spuštěním registrace projděte strukturu a náhled — zkontrolujete, zda se podmínky zobrazují tak, jak jste je zamýšleli.

## Na co si dát pozor

### Podmíněná otázka je přidaná jako samostatná otázka v seznamu. Organizátor ji pak nastavuje „Zobrazit otázku pouze skupinám“ a čeká, že se zobrazí při vybrané odpovědi — ale skupiny fungují jinak než odpovědi

Podmínka se přidává **pod konkrétní odpověď** nadřazené otázky, ne jako samostatná položka. Otevřete nadřazenou otázku, najděte odpověď a tam přidejte navázanou otázku.

### Viditelnost na skupinu a podmíněná otázka zkombinované bez promyšlení. Otázka se nezobrazí, i když účastník zvolil správnou odpověď, protože není ve správné skupině

Pokud jde o větvení podle odpovědi (aktuální akce ve formuláři), použijte **podmíněnou otázku**. Pokud jde o větvení podle typu účastníka (VIP, standardní, speaker), použijte **viditelnost na skupinu**. Nekombinujte bez jasného důvodu.

### Účastník vybere jednu odpověď, odpoví na podmíněnou otázku, pak změní odpověď. Organizátor čeká, že první odpověď zůstane v datech

Změna nadřazené odpovědi **odebere** předchozí podmíněnou otázku i s odpovědí. V datech zůstane jen finální stav formuláře.

### Podmíněné otázky jsou vnořené do třetí, čtvrté úrovně. Formulář se stává nepřehledným, účastník se ztrácí

Dvě úrovně podmínek (otázka → podotázka → podpodotázka) jsou maximum, které má smysl. Pokud potřebujete víc, rozdělte formulář na dvě fáze nebo otevřete rozhovor přes e-mail až po registraci.

### Skupina pro zařazení podle odpovědi neexistuje, protože organizátor ji založil až po zveřejnění formuláře. Účastníci, kteří se zaregistrovali před vytvořením skupiny, zůstanou bez zařazení

Skupinu založte **před** zveřejněním formuláře. Pokud to stihnete i na poslední chvíli, ex post doplnění skupiny k existující odpovědi **nepropíše zařazení zpětně** — musíte provést ručně hromadné přiřazení v Kontaktech a skupinách.

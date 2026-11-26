<!-- source: kb.cs.03.23 -->

---
title: "Hromadný import vystavovatelů"
description: "Nahrání vystavovatelů z Excelu přes 5krokový průvodce — šablona, mapování sloupců, přiřazení kategorií a míst, validace a CSV report."
modules: ["sponzori_a_vystavovatele"]
last_updated: "2026-08-07"
version: 2
---

> [!info] Krátce
> Hromadný import umožňuje vytvořit více vystavovatelů najednou z Excelu místo zakládání po jednom. Hodí se, když máte seznam stánků připravený v tabulce — typicky deset a více. Průvodce má pět kroků (nahrání souboru, mapování sloupců, přiřazení kategorií a míst, náhled, výsledek) a před zápisem zkontroluje validitu dat. Naimportují se textová pole, číslo stánku, kategorie a místo; **loga, zástupci ani štítky se přes import nenastaví** — loga ale po importu doplníte hromadnou akcí **Najít loga**.

## Jak začít

- Rozhodněte, **do které instance Vystavovatelů** importujete. Obsahovou funkci lze do události přidat víckrát a záložka **Import** je samostatná pro každou instanci — vystavovatelé se naimportují do té, ve které právě jste.
- Připravte si data v Excelu. Můžete stáhnout **šablonu** přímo z administrace, nebo použít **vlastní soubor** — sloupce ručně namapujete ve druhém kroku průvodce.
- **Vyplňte v souboru webové stránky.** Import loga nenahraje, ale hromadná akce **Najít loga** je po importu umí dohledat z webů vystavovatelů — bez vyplněné URL skončí vystavovatel se stavem *Chybí web* a logo doplníte ručně.
- Srovnejte si **názvy kategorií a míst**. Průvodce má na jejich kontrolu vlastní krok: hodnoty ze souboru přiřadíte k existujícím kategoriím a místům, nebo necháte vytvořit nové.
- **Zástupce** (pracovníky na stánku) přes import nezaložíte — musí být účastníky události a k vystavovatelům je přiřadíte ručně po importu.

## Detail

### Kde Import najdete

V administraci přejděte na **Obsah** a otevřete instanci **Vystavovatelé**, do které chcete importovat. V hlavičce sekce je šest záložek: **Vystavovatelé**, **Kategorie**, **Místa**, **Štítky**, **Nastavení** a **Import**. Otevřete záložku **Import**.

### Šablona, nebo vlastní soubor

V prvním kroku průvodce máte dvě cesty:

- **Stáhnout šablonu** a vyplnit ji. Šablona je XLSX s jedním listem *Exhibitors*, hlavičkovým řádkem a jedním ukázkovým řádkem s fiktivními daty (*Example Company s.r.o.*, stánek *A-01*) — ten před importem smažte, viz pozor níže.
- **Nahrát vlastní Excel** s vlastními názvy sloupců. Mapování na pole vystavovatele nastavíte ručně ve druhém kroku, takže na názvech sloupců nezáleží.

Hlavičky šablony se stahují **v jazyce administrace** (česká administrace *Název*, *Webové stránky*…, anglická *Name*, *Website*…); sloupec pro popis je vázaný na **jazyk obsahu události** (u události s anglickým obsahem *Description - EN*). Obě varianty mají stejné sloupce ve stejném pořadí, takže na jazyce šablony nezáleží.

V obou případech pak kliknete na **Nahrát a zpracovat** a průvodce přejde na mapování.

### Pole, která lze naimportovat

- **Název** *(povinné)* — Jediné povinné pole. Zároveň slouží jako klíč pro rozpoznání duplicity.
- **Webové stránky** *(volitelné)* — URL musí začínat `https://`. Zdroj pro hromadné dohledání log po importu.
- **E-mail** *(volitelné)*
- **Telefon** *(volitelné)*
- **Popis - EN** *(volitelné)* — Vázaný na jazyk obsahu události.
- **Číslo stánku** *(volitelné)* — V panelu vystavovatele se totéž pole jmenuje **Číslo vystavovatele** — používá ho řazení *Podle čísla*.
- **Kategorie** *(volitelné)* — Na rozdíl od sponzorů **není povinná**. Hodnoty se přiřazují ve 3. kroku průvodce.
- **Místo** *(volitelné)* — Stánek nebo sektor (například *Hall A*). Hodnoty se přiřazují ve 3. kroku průvodce.
- **LinkedIn, Twitter / X, Instagram, Facebook, YouTube** *(volitelné)* — Odkazy na sociální sítě vystavovatele.

Povinný je jen **Název** — poznáte ho podle hvězdičky u cílového pole v mapování. Sloupce, kterým necháte mapování prázdné, se přeskočí.

Šablona **nemá sloupec pro štítky, logo, zástupce ani stav** — nic z toho import nenastaví (viz *Co import neumí*).

### Průvodce importem (5 kroků)

V horní části obrazovky je krokový indikátor: **Nahrát → Mapování → Kategorie → Náhled → Výsledek**. Mezi kroky se lze vracet zpět. Oproti importu řečníků a sponzorů je třetí krok jiný — místo *Vazeb* má vlastní obrazovku pro kategorie a místa.

**1. Nahrát.** Stáhněte šablonu (volitelně), nebo rovnou nahrajte svůj Excel přes výběr souboru. Klikněte na **Nahrát a zpracovat**.

**2. Mapování.** Průvodce načte hlavičky vašeho souboru a zobrazí je v tabulce *Sloupec v Excelu — Ukázkové hodnoty — Mapovat na pole*, spolu s počtem nalezených řádků. U každého sloupce vyberte cílové pole. Mapování **se nikam neukládá** — při každém importu ho nastavujete znovu od začátku.

**3. Kategorie.** Obrazovka **Přiřazení kategorií a míst**. Průvodce vypíše všechny unikátní hodnoty ze sloupců Kategorie a Místo — každou s počtem výskytů a rozbalovací nabídkou **Přiřadit k**. Hodnotu buď přiřadíte k existující kategorii či místu (i když se v souboru jmenuje jinak), nebo necháte vytvořit novou. Právě tady zachytíte překlepy a odchylky v názvech — viz pozor níže. Klikněte na **Ověřit a zobrazit náhled** (případně **← Zpět na mapování**).

**4. Náhled.** Průvodce zobrazí souhrn: **Celkem / Validní / Varování / Chyby / Duplicity**. Pod souhrnem je tabulka s každým řádkem souboru a jeho stavem — validní řádek je označený zeleně, u duplicitního je ikona duplicity a hláška *Vystavovatel s tímto názvem již existuje.* Čísla řádků odpovídají číslům v Excelu (první datový řádek je `2`). **Žádná data se ještě nezapsala** — je to poslední možnost se vrátit a soubor opravit. Pokud souhrn vyhovuje, klikněte na **Importovat**.

**5. Výsledek.** Po dokončení importu se zobrazí výsledná čísla: **Vytvořeno / Přeskočeno / Chyby**. Z této obrazovky můžete přejít na seznam vystavovatelů (**Pokračovat na seznam**), nebo si stáhnout detailní CSV report o každém řádku (**Stáhnout report (CSV)**).

### Jak průvodce pozná duplicitu

Duplicita se určuje podle **názvu vystavovatele** — stejné pravidlo jako u sponzorů. Řádek je duplicitní, pokud vystavovatel se stejným názvem **už v události existuje**, nebo se stejný název **opakuje v souboru**. Duplicitní řádky se **nezaimportují**; z opakujících se řádků se zaimportuje první výskyt. Import tedy **nepřepisuje existující vystavovatele** — na hromadné změny použijte hromadné akce v záložce Vystavovatelé.

### Co import neumí

- **Nahrát loga.** Šablona ani mapování pole pro logo nemají. Po importu ale nemusíte loga sbírat ručně — označte vystavovatele a spusťte hromadnou akci **Najít loga**, která je zkusí dohledat z vyplněných webových stránek.
- **Založit zástupce.** Zástupci jsou účastníci události — z Excelu vystavovatelů je nevytvoříte. Přiřaďte je po importu v panelu vystavovatele na záložce **Zástupci**.
- **Přiřadit štítky.** Šablona sloupec pro štítky nemá a krok *Kategorie* přiřazuje jen kategorie a místa. Štítky doplňte po importu — nejrychleji hromadnou akcí **Štítky** v seznamu vystavovatelů.
- **Nastavit stav.** Publikováno / Skryto se importem neurčí — po importu stav zkontrolujte v seznamu.
- **Aktualizovat existující vystavovatele.** Duplicitní řádky se přeskakují.

## Na co si dát pozor

### Šablona obsahuje ukázkový řádek (Example Company s.r.o.) — pokud ho nesmažete, naimportuje se

Stažená šablona má první datový řádek vyplněný fiktivní ukázkou včetně stánku *A-01*, kategorie *Services* a místa *Hall A*. V *Náhledu* projde jako validní. Před vyplněním vlastních dat ho smažte — jinak vám v seznamu zůstane smyšlený vystavovatel a k němu založená kategorie i místo.

### V kroku *Kategorie* nezaložte překlep jako novou kategorii

Krok *Přiřazení kategorií a míst* je pojistka proti překlepům — ale jen když ji použijete. Pokud soubor obsahuje *Zdravotnictvi* a v události už máte *Zdravotnictví*, přiřaďte hodnotu k existující kategorii z nabídky **Přiřadit k**; když ji bez kontroly necháte vytvořit novou, skončíte se dvěma skoro stejnými kategoriemi a rozpadnutým filtrováním. Totéž platí pro místa.

### Jediné povinné pole je Název — vystavovatel bez kategorie a místa se ale špatně hledá

Import vás nedonutí kategorie ani místa vyplnit. Kategorie, místa a štítky přitom fungují v aplikaci i na microsite jako filtry — vystavovatel bez nich se v delším seznamu ztratí. Sloupce Kategorie a Místo v souboru vyplňte, štítky doplňte po importu hromadnou akcí.

### Bez webových stránek nedohledáte loga hromadně

Hromadná akce **Najít loga** vychází z pole **Webové stránky** — vystavovatelé bez URL skončí se stavem *Chybí web* a jejich loga doplníte ručně. Pokud weby máte, vyplňte je už v importním souboru; u 50 stánků to je rozdíl mezi jedním dialogem a odpolednem ruční práce.

### Opakovaný import stejného souboru nevytvoří nic — všechny řádky spadnou do Duplicit

Řádky se porovnávají s už existujícími vystavovateli v dané instanci, takže druhý import téhož souboru skončí s *Validní 0* a *Duplicity* rovnými počtu řádků. Vyšší počet duplicit, než čekáte, znamená, že část vystavovatelů už v události je — import je znovu nevytvoří ani nepřepíše.

### Dva vystavovatelé se stejným názvem — druhý se nenaimportuje

Duplicita se pozná jen podle názvu, ne podle čísla stánku nebo e-mailu. Dvě pobočky stejné firmy pod identickým názvem projdou jako jedna — odlište je v názvu (například městem), jinak vám jedna vypadne.

### Mapování sloupců musíte nastavit při každém importu znovu

Průvodce si namapování nepamatuje — po každém nahrání souboru ho zadáváte od začátku. Pokud importujete opakovaně, držte ve svém souboru **stejné názvy a pořadí sloupců jako ve stažené šabloně**.

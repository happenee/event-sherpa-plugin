# Hromadný import sponzorů

> Nahrání sponzorů z Excelu — mapování sloupců, přiřazení kategorií v kroku Vazby, náhled a CSV report.

- Článek v Help Centru: https://help.happenee.com/cs/articles/71-hromadny-import-sponzoru
- English version: https://help.happenee.com/en/articles/71-bulk-import-of-sponsors
- Kolekce: Obsah a zkušenost účastníka
- Aktualizováno: 2026-09-29

---

> [!info] Krátce
> Hromadný import umožňuje vytvořit více sponzorů najednou z Excelu místo zakládání po jednom. Hodí se, když máte partnery připravené v tabulce — typicky deset a více. Průvodce před zápisem zkontroluje validitu dat. V kroku **Vazby** můžete hodnoty kategorií ze souboru přiřadit k existujícím kategoriím nebo vytvořit nové. Naimportují se textová pole, zařazení do kategorie a volitelně stav; **loga se přes import nahrát nedají** a doplňujete je ručně po importu.

## Jak začít

- Rozhodněte, **do které instance Sponzorů** importujete. Obsahovou funkci Sponzoři lze do události přidat víckrát (například *Partneři konference* a *Mediální partneři*) a záložka **Import** je samostatná pro každou z nich — sponzoři se naimportují do té instance, ve které právě jste.
- Připravte si data v Excelu. Můžete stáhnout **šablonu** přímo z administrace, nebo použít **vlastní soubor** — sloupce ručně namapujete ve druhém kroku průvodce, takže na jejich názvech nezáleží.
- Projděte si **názvy kategorií**. Kategorie je u sponzora povinná. V kroku **Vazby** přiřadíte hodnoty ze souboru k existujícím kategoriím nebo zvolíte vytvoření nových; překlep tak můžete opravit před importem.
- Připravte si **loga zvlášť**. Import je neumí — po importu je doplníte ručně v panelu úprav každého sponzora.
- Rozhodněte, **co se stane po kliknutí na logo** (externí web, profil sponzora, nebo nic). Hodnota se do souboru zapisuje slovem a musí odpovídat tomu, co máte v dalších sloupcích vyplněné.

## Detail

### Kde Import najdete

V administraci přejděte na **Obsah** a otevřete instanci **Sponzoři**, do které chcete importovat (název instance je v přepínači vedle nadpisu *Obsah*). V hlavičce sekce jsou čtyři záložky: **Sponzoři**, **Kategorie**, **Nastavení** a **Import**. Otevřete záložku **Import**.

### Šablona, nebo vlastní soubor

V prvním kroku průvodce máte dvě cesty:

- **Stáhnout šablonu** a vyplnit ji. Šablona je XLSX s jedním listem *Sponsors*, hlavičkovým řádkem a jedním ukázkovým řádkem s fiktivními daty (*Example Sponsor s.r.o.*) — ten před importem smažte, viz pozor níže. Název souboru obsahuje název události, ze které jste šablonu stáhli.
- **Nahrát vlastní Excel** s vlastními názvy sloupců. Mapování na pole sponzora nastavíte ručně ve druhém kroku.

Hlavičky šablony se stahují **v jazyce administrace** — z české administrace dostanete *Název*, *Kategorie*, *Webové stránky*, z anglické *Name*, *Category*, *Website*. Na obsah to vliv nemá: obě varianty mají stejné sloupce ve stejném pořadí a stejný ukázkový řádek, a mapování ve druhém kroku funguje bez ohledu na to, v jakém jazyce hlavičky jsou.

Sloupec pro popis je naopak vázaný na **jazyk obsahu události** — u události s anglickým obsahem se jmenuje *Description - EN*.

V obou případech pak kliknete na **Nahrát a zpracovat** a průvodce přejde na mapování.

### Pole, která lze naimportovat

- **Název** *(povinné)* — Název sponzora. Zároveň slouží jako klíč pro rozpoznání duplicity.
- **Kategorie** *(povinné)* — Hodnotu ze souboru přiřadíte v kroku **Vazby** k existující kategorii nebo zvolíte založení nové.
- **Webové stránky** *(volitelné)* — URL musí začínat `https://`.
- **Akce po kliknutí na logo (website/profile/none)** *(volitelné)* — Hodnota se zapisuje slovem: `website`, `profile`, nebo `none`.
- **Popis - EN** *(volitelné)* — Vázaný na jazyk obsahu události.
- **E-mail** *(volitelné)*
- **Telefon** *(volitelné)*
- **LinkedIn, Twitter / X, Instagram, Facebook, YouTube** *(volitelné)* — Odkazy na sociální sítě sponzora.
- **Stav** *(volitelné)* — Hodnota se zapisuje slovem: `published` (Publikováno), nebo `hidden` (Skryto). Ve stažené šabloně tento sloupec není, takže pokud chcete stav nastavit importem, přidejte si ho do souboru sami. Když ho nenamapujete, zkontrolujte stav nových sponzorů po importu v seznamu sponzorů.

Povinné jsou jen **Název** a **Kategorie** — poznáte je podle hvězdičky u názvu cílového pole v mapování. Sloupce, kterým necháte mapování prázdné, se přeskočí.

Logo ani pořadí sponzora v kategorii mezi cílovými poli nejsou, takže je import nenastaví.

### Akce po kliknutí na logo se zapisuje slovem

Na rozdíl od importu řečníků, kde se **Úroveň zobrazení** a **Stav** zadávají číselnými kódy, u sponzorů se zapisuje **text**. Povolené hodnoty jsou přímo v názvu sloupce:

- **`website`** — kliknutí na logo otevře externí web sponzora. Vyplňte k tomu sloupec *Webové stránky*, URL s `https://`.
- **`profile`** — kliknutí otevře profil sponzora uvnitř platformy. Vyplňte k tomu popis, případně kontakty a sociální sítě.
- **`none`** — kliknutí na logo neprovede nic, logo je čistě vizuální. Nic dalšího vyplňovat nemusíte.

### Průvodce importem

Průvodce vás provede obrazovkami **Nahrát**, **Mapování**, **Vazby**, **Náhled** a **Výsledek**. Mezi kroky se lze vracet zpět.

**Nahrát.** Stáhněte šablonu (volitelně), nebo rovnou nahrajte svůj Excel přes výběr souboru. Klikněte na **Nahrát a zpracovat**.

**Mapování.** Průvodce načte hlavičky vašeho souboru a zobrazí je v tabulce *Sloupec v Excelu — Ukázkové hodnoty — Mapovat na pole*, spolu s počtem nalezených řádků. U každého sloupce vyberte z rozbalovacího menu, kam se má hodnota uložit. Sloupce bez přiřazení se přeskočí. Mapování **se nikam neukládá** — při každém importu ho nastavujete znovu od začátku. Klikněte na **Ověřit a zobrazit náhled** a průvodce zobrazí přiřazení vazeb.

**Vazby.** U každé hodnoty kategorie nalezené v souboru vyberte existující kategorii nebo **+ Vytvořit novou**. Kategorii se stejným názvem průvodce předvybere, i když se liší velikostí písmen; hodnotu s překlepem můžete přiřadit ke správné existující kategorii. Nová kategorie vznikne až po potvrzení importu. Klikněte na **Ověřit a zobrazit náhled** a zkontrolujte přiřazení v Náhledu.

**Náhled.** Průvodce zobrazí souhrn: **Celkem / Validní / Varování / Chyby / Duplicity**. Pod souhrnem je tabulka s každým řádkem souboru a jeho stavem — validní řádek je označený zeleně, u duplicitního je ikona duplicity a hláška, že sponzor s tímto názvem už existuje. Čísla řádků odpovídají číslům v Excelu, takže první datový řádek je `2` (jednička je hlavička). **Žádná data se ještě nezapsala** — je to poslední možnost se vrátit a soubor opravit. Pokud souhrn vyhovuje, klikněte na **Importovat**.

**Výsledek.** Po dokončení importu se zobrazí výsledná čísla: **Vytvořeno / Přeskočeno / Chyby**. Z této obrazovky můžete přejít na seznam sponzorů (**Pokračovat na seznam**), nebo si stáhnout detailní CSV report o každém řádku (**Stáhnout report (CSV)**) — hodí se, když chcete dohledat, který řádek se nenaimportoval a proč.

### Kategorie: import ji založí, ale nezobrazí na hlavní stránce

Kategorie je u sponzora povinná. Pokud v kroku **Vazby** zvolíte **+ Vytvořit novou**, import kategorii založí a sponzory do ní zařadí. Jestliže hodnotu přiřadíte k existující kategorii, nová nevznikne.

Nově založená kategorie se ale **sama nezobrazí na hlavní stránce** microsite ani účastnické aplikace. Pokud tam kategorii chcete mít, zapněte jí po importu v záložce **Kategorie** přepínač **Zobrazení na homepage microsite a účastnické aplikace**. Ve stejném kroku zkontrolujte i **Úroveň zobrazení** (hodnoty **1**, **2**, **4**) — určuje pořadí kategorií a počet log v jednom řádku.

### Jak průvodce pozná duplicitu

Duplicita se u sponzorů určuje podle **samotného názvu**. Řádek je duplicitní, pokud:

- sponzor se stejným názvem **už v události existuje**, nebo
- stejný název se **opakuje v souboru** na více řádcích.

Duplicitní řádky se **nezaimportují** — průvodce je přeskočí a z opakujících se řádků zaimportuje **první výskyt**. V kroku *Náhled* uvidíte počet duplicit dopředu; ve *Výsledku* se přeskočené řádky započítají do **Přeskočeno**.

Import tedy **nepřepisuje existující sponzory**. Pokud chcete hromadně změnit sponzory, kteří už v události jsou, použijte hromadné akce v záložce Sponzoři (změna kategorie, stavu, smazání).

### Co import neumí

- **Nahrát loga.** Šablona ani mapování nemají sloupec pro logo ani jeho URL. Loga doplníte po importu ručně v panelu úprav sponzora.
- **Určit pořadí v kategorii.** Pořadí sponzorů uvnitř kategorie se nastavuje přetažením v seznamu, ne sloupcem v Excelu.
- **Aktualizovat existující sponzory.** Duplicitní řádky se přeskakují; hromadné změny řešte hromadnými akcemi v seznamu sponzorů.

## Na co si dát pozor

### Šablona obsahuje ukázkový řádek (Example Sponsor s.r.o.) — pokud ho nesmažete, naimportuje se

Stažená šablona má první datový řádek vyplněný fiktivní ukázkou včetně kategorie *Main sponsors*, webu *example.com* a telefonu s předvolbou. V *Náhledu* se objeví jako validní řádek. Před vyplněním vlastních dat ho smažte — jinak vám v seznamu zůstane smyšlený sponzor a podle volby v kroku **Vazby** může vzniknout také kategorie *Main sponsors*.

### Překlep v názvu kategorie opravte v kroku Vazby

Překlep není chyba, kterou by *Náhled* automaticky odmítl. Například hodnotu *Zlatý sponzoři* ze souboru můžete v kroku **Vazby** přiřadit ke kategorii *Zlatí sponzoři*. Pokud místo toho ponecháte **+ Vytvořit novou**, po importu vznikne další kategorie. Před kliknutím na **Importovat** zkontrolujte zvolenou kategorii u každého řádku v Náhledu.

### Nová kategorie z importu se na hlavní stránce neobjeví sama

Kategorie založená importem má sponzory správně zařazené, ale zobrazení na hlavní stránce microsite a účastnické aplikace je potřeba zapnout ručně v záložce **Kategorie**. Pokud po importu sponzory na hlavní stránce nevidíte, tohle je první místo ke kontrole — spolu se stavem sponzora i kategorie (viditelní jsou jen tehdy, když jsou **oba** ve stavu **Publikováno**).

### Opakovaný import stejného souboru nevytvoří nic — všechny řádky spadnou do Duplicit

Řádky se porovnávají s už existujícími sponzory v dané instanci, takže druhý import téhož souboru skončí tak, že se všechny řádky vyhodnotí jako duplicitní a přeskočí (v *Náhledu* uvidíte *Validní 0* a *Duplicity* rovné počtu řádků). Před kliknutím na **Importovat** proto vždy zkontrolujte počet duplicit — vyšší číslo, než čekáte, znamená, že část sponzorů už v události je. Import je znovu nevytvoří ani nepřepíše.

### Dva sponzoři se stejným názvem — druhý se nenaimportuje

Duplicita se u sponzorů pozná jen podle názvu, ne podle webu nebo e-mailu (u řečníků se přitom porovnává jméno a příjmení dohromady). Pokud máte dvě pobočky nebo dvě divize stejné firmy zapsané pod identickým názvem, projde jen první. Odlište je v názvu (například dodatkem o zemi nebo divizi), jinak vám jedna vypadne.

### Loga se přes import nenahrají — počítejte s ruční prací po importu

Hromadný import řeší jen textová pole, zařazení do kategorie a stav. U dvaceti partnerů to znamená dvacet panelů úprav, ve kterých po importu doplníte logo (PNG, JPEG nebo GIF, poměr 16:9, max. 500 KB). Naplánujte si na to čas — a připravte si loga předem v jednotném formátu.

### Mapování sloupců musíte nastavit při každém importu znovu

Průvodce si namapování sloupců nepamatuje — po každém nahrání souboru ho zadáváte od začátku. Pokud importujete opakovaně (partneři přibývají průběžně), držte ve svém souboru **stejné názvy a pořadí sloupců jako ve stažené šabloně**. Mapování pak zabere pár vteřin a nepřehlédnete žádné pole.

## Související články

- [Správa sponzorů](https://help.happenee.com/cs/articles/32-sprava-sponzoru)
- [Hromadný import řečníků](https://help.happenee.com/cs/articles/67-hromadny-import-recniku)
- [Hromadný import sessions](https://help.happenee.com/cs/articles/68-hromadny-import-sessions)
- [Hromadný import vystavovatelů](https://help.happenee.com/cs/articles/72-hromadny-import-vystavovatelu)

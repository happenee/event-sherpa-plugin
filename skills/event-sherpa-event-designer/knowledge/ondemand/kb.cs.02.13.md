<!-- source: kb.cs.02.13 -->

---
title: "Kopírování události"
description: "Založení nové události z existující v průvodci: co se dá převzít, co se nikdy nekopíruje a na co si po kopírování dát pozor."
modules: ["nastaveni_udalosti", "registrace", "vstupenky_a_objednavky"]
last_updated: "2026-11-04"
version: 5
---

> [!info] Krátce
> Kopírování události založí novou událost z existující. V průvodci zadáte název a termín nové události a vyberete, co se z původní události převezme: registrace a registrační formulář, zapnutí placených vstupenek, microsite, e-maily, obsah kampaní, jednotlivé obsahové a engagement funkce (s jejich obsahem, nebo bez něj) a případně i stejné účastníky. Odpovědi účastníků, objednávky, vstupenky, check-in ani statistiky se nekopírují nikdy. Použijete ho u opakující se události nebo série, kdy chcete znovu využít hotový setup. Najdete ho v **Nastavení události** na záložce **Danger zone** pod tlačítkem **Kopírovat událost**.

## Jak začít

- Rozhodněte, jestli je kopie správný nástroj. Hodí se, když má nová událost podobný formát a stačí upravit termín a obsah. Pro úplně jiný typ události je čistší založit novou od začátku.
- Připravte si název a termín nové události. Pokud chcete převzaté účastníky rovnou zařadit do skupiny, založte ji předem v **Kontaktech a skupinách**; průvodce nabízí jen existující skupiny.
- Otevřete **Nastavení události → Danger zone** a klikněte na **Kopírovat událost**. Průvodce má dva kroky: v prvním nastavíte novou událost, ve druhém vyberete, co se zkopíruje. Kopii založíte tlačítkem **Vytvořit kopii**; administrace vás potom přepne do nastavení nové události.

## Detail

### Krok 1: nová událost

- **Název nové události** je předvyplněný ve tvaru *Kopie {datum} - {název původní události}*. Přepište ho na skutečný název, protože z něj vznikne i adresa microsite.
- **Začátek a konec** (datum a čas). Konec se předvyplní podle délky původní události a můžete ho změnit. Pod poli vidíte pro kontrolu termín původní události.
- **Posun programu.** Sessions se posunou o stejný počet dní, o kolik posunete začátek; jejich časy zůstávají. Sessions, které by po posunu nespadly do nového termínu, se nezkopírují vůbec, včetně svých vazeb. Průvodce na to upozorní ještě před vytvořením kopie.
- **Nastavení události** — **Časové pásmo**, **Popis události** a **Grafika události**. Zaškrtnuté se převezme z původní události, odškrtnuté zadáte nově: vyberete jiné časové pásmo (časy programu zůstanou stejné v novém pásmu), napíšete nový popis nebo ho necháte prázdný a doplníte později.
- **Účastníci nové události** — volba **Přiřadit stejné účastníky** přidá do kopie účastníky původní události (bez administrátorů). Přiřadí se čistě: bez pozvání, odpovědí, potvrzení účasti a check-inu. Pokud má nová událost zapnuté schvalování registrací, čekají přiřazení účastníci na schválení. Volitelně je můžete **Zařadit do skupiny**; zařazení se jen přidá k jejich dosavadním skupinám.

Kopírování samo nic neodesílá. Přiřazeným účastníkům nepřijde žádný e-mail, dokud jim pozvánku nebo kampaň v nové události nepošlete vy.

### Krok 2: co zkopírovat

Základ události (název, termín, základní údaje a jazyky) se kopíruje vždy, časové pásmo podle volby v kroku 1. Ostatní volíte zaškrtnutím ve třech skupinách.

**Moduly**:

- **Registrace** — nastavení registrace, pole a otázky, ubytování a pravidla schvalování.
- **Registrační formulář** — funkce registračního formuláře z levého menu.
- **Placené vstupenky** — převezme se jen zapnutí modulu Placené vstupenky. Samotné vstupenky, slevové kódy ani objednávky se nekopírují. Volba je dostupná jen tehdy, když má původní událost placené vstupenky zapnuté.
- **Microsite** — texty a nastavení microsite.
- **Zvací e-mail** a **Potvrzovací a schvalovací e-maily** — texty, předmět, odesílatel a přílohy těchto e-mailů.
- **Obsah kampaní** — všechny e-mailové kampaně původní události, i už odeslané, se zkopírují s obsahem jako nové neodeslané kampaně. Bez příjemců, data a času rozesílky, plánování a historie. Tahle volba je ve výchozím stavu vypnutá.

**Obsahové funkce** a **Engagement funkce** — seznam funkcí události tak, jak je máte pojmenované v levém menu. U každé zvolíte, jestli se zkopíruje. U Programu, Řečníků, Sponzorů, Vystavovatelů, Hlasování, Dotazníku, Lokality, Kontaktu a Vlastního obsahu navíc rozhodnete volbou **Obsah**, jestli se zkopírují i jejich položky (sessions, řečníci, otázky hlasování…), nebo jen prázdná funkce. U ostatních funkcí se kopíruje nastavení; historie a interakce účastníků ne.

Tlačítka **Vybrat vše** a **Odebrat vše** nastaví všechny volby najednou. Vpravo průběžně vidíte **Souhrn kopie** se seznamem toho, co se zkopíruje a co ne.

Průvodce si pamatuje váš poslední úspěšný výběr a příště ho nabídne znovu. Název, termín a skupinu zadáváte pokaždé nově. Funkce, které při minulém kopírování nebyly k dispozici, zůstanou vypnuté a průvodce vás upozorní, ať výběr zkontrolujete.

### Co se nikdy nekopíruje

- Odpovědi a historická data účastníků: odpovědi z registračního formuláře, hlasy, dotazy, chaty, schůzky a check-in.
- Vstupenky, slevové kódy, objednávky a statistiky vstupenek a také nastavení plateb a konec prodeje. Z **Placených vstupenek** se převezme nanejvýš jejich zapnutí.
- Push notifikace, oznámení a rozesílky kampaní.
- Nastavení **Online modulu**. V průvodci ho nelze vybrat, v kopii ho nastavte znovu.
- Podmíněné otázky a automatické zařazení do skupin v registračním formuláři a pokoje u ubytování. Otázky samotné se zkopírují, podmínky a pokoje nastavte znovu.

Jde o data konkrétního běhu události, ne o setup. Nová událost proto začíná bez historie prodeje a bez odeslaných zpráv.

## Na co si dát pozor

### Výchozí název obsahuje „Kopie“ a datum

Pokud předvyplněný název v průvodci nepřepíšete, nová událost se bude jmenovat *Kopie {datum} - {název}* a stejný tvar bude mít i adresa microsite. Ve druhém jazyce události dostane název tento tvar vždy. Po vytvoření kopie proto zkontrolujte název ve všech jazycích a případně i adresu microsite, dřív než pošlete první pozvánku. Jak adresu změnit, popisuje [Jak funguje microsite události](../03_obsah-a-zkusenost-ucastnika/01_jak-funguje-microsite-udalosti.md).

### Kratší termín vynechá část programu

Když novou událost zkrátíte, sessions mimo nový termín se nezkopírují a s nimi ani jejich vazby na řečníky nebo sponzory. Průvodce zobrazí, kolik položek vypadne. Pokud je chcete zachovat, nastavte konec dost pozdě a program upravte až v kopii.

### Vazby mezi obsahy potřebují obě funkce

Vazba řečníka nebo sponzora na session se zkopíruje jen tehdy, když vyberete obě funkce včetně obsahu. Jinak se vynechá a administrace po vytvoření kopie upozorní, že některé vazby mezi obsahy chybí.

### Placené vstupenky se v kopii zakládají znovu

I když volbu **Placené vstupenky** necháte zaškrtnutou, převezme se jen zapnutí modulu. Typy vstupenek, platební nastavení ani slevové kódy v kopii nejsou a konec prodeje se vrátí na konec události. Před otevřením registrace proto vstupenky v nové události nastavte znovu, jinak nebude co prodávat.

### Soukromé zprávy a schůzky v Networkingu jsou vypnuté

I když Networking zkopírujete, jeho volby **Zapnout soukromé zprávy** a **Zapnout rezervační systém schůzek** jsou v nové události vypnuté. Pokud je chcete používat, zapněte je v nastavení Networkingu znovu.

### Původní Program se nekopíruje

Pokud událost používá původní Program (starší obsahovou funkci pro časový plán, kterou nové události už nenabízejí), je v průvodci nedostupný a průvodce to vysvětlí. Ostatní vybrané položky se zkopírují normálně. V nové události přidejte aktuální Program a sessions v něm vytvořte znovu; postup je v článku *Sestavení programu události — architektura*.

### Kopírování je v Danger zone hned vedle nevratného smazání

Na stejné záložce je i **Smazat událost**, které událost odstraní **nenávratně**. **Kopírovat událost** je bezpečná akce (jen otevře průvodce a založí novou událost), smazání ne. Před kliknutím se ujistěte, které tlačítko mačkáte.

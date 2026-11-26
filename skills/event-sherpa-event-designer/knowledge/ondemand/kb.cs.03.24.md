<!-- source: kb.cs.03.24 -->

---
title: "Nastavení engagement funkcí"
description: "Hlasování, Otázky, Dotazník a Registrační údaje v administraci události — kde se zapínají, kdy se hodí který a jak se čtou výsledky."
modules: ["ucastnicka_aplikace"]
last_updated: "2026-09-08"
version: 2
---

> [!info] Krátce
> **Engagement** je sekce v levém menu události, kde zapínáte funkce pro aktivní zapojení účastníka v účastnické aplikaci. Tento článek popisuje čtyři z nich: **Hlasování** (interaktivní ankety a soutěže), **Otázky** (otázky z publika), **Dotazník** (zpětná vazba, názory, doplňující otázky) a **Registrační údaje** (údaje účastníka zadané při registraci). Sekce jich nabízí devět; zbylých pět je popsaných jinde a rozcestník na ně je hned v Detailu. Engagement funkce se zobrazují v účastnické aplikaci, ne na microsite.

## Jak začít

- Funkci přidáte v sekci **Engagement** tlačítkem **+ Přidat** a výběrem z nabídky.
- Každou z těchto čtyř funkcí lze do jedné události přidat **jen jednou**. Vícekrát jde přidat pouze Online modul.
- Rozhodněte nejdřív, **na jaké úrovni se ptáte**. Hlasování a otázky ke konkrétní přednášce nastavujete v programu u dané session, ne tady — podrobněji níže v sekci *Tři místa, kde se stejné názvy potkávají*.
- Určete, **kdo funkci během události obsluhuje** — kdo publikuje hlasování, kdo moderuje otázky, kdo v pravou chvíli pošle Oznámení s odkazem na dotazník. Bez toho funkce v aplikaci visí prázdná.
- Počítejte s tím, že Hlasování i Dotazník jsou v aplikaci vidět **až po doplnění odpovědí a publikaci**. Připravit si je můžete dopředu a nechat nepublikované.

## Detail

### Devět funkcí v nabídce a kde je najdete

Tlačítko **+ Přidat** nabízí devět engagement funkcí. Čtyři z nich popisuje tenhle článek, zbylých pět má vlastní:

- **QR vstupenka** — *Odbavení účastníků a tisk štítků*. Účastník má vstupenku v aplikaci; odkaz na kartě vede rovnou do *Odbavení na místě*. Viz [Jak funguje check-in a skenování QR kódů](../05_den-akce-a-provoz/01_jak-funguje-check-in-a-skenovani-qr-kodu.md).
- **QR doprovod** — *QR pro doprovod zvolený v registračním formuláři*. Zobrazí se jen tehdy, když formulář otázku na doprovod obsahuje; nastavuje se v [Nastavení registračního formuláře](../02_nastaveni-eventu-a-registrace/05_nastaveni-registracniho-formulare.md).
- **Oznámení** — *Oznámení v účastnické aplikaci a push notifikace*. Viz [Používání oznámení v účastnické aplikaci](../04_komunikace-a-pozvanky/08_pouzivani-oznameni-v-ucastnicke-aplikaci.md).
- **Hlasování** — *Interaktivní ankety a soutěže*. Níže v tomhle článku.
- **Otázky** — *Otázky z publika*. Níže v tomhle článku.
- **Dotazník** — *Zpětná vazba, názory, doplňující otázky*. Níže v tomhle článku.
- **Účastníci** — *Networking a schůzky*. Viz [Jak funguje Networking](16_jak-funguje-networking.md).
- **Registrační údaje** — *Údaje účastníků zadané při registraci*. Níže v tomhle článku.
- **Online modul** — *Livestream, video, 3D, social wall, hry*. Viz [Použití Online modulu](18_pouziti-online-modulu.md).

### Tři místa, kde se stejné názvy potkávají

*Hlasování* a *Otázky* najdete v administraci na třech různých místech. Nejde o tutéž věc zobrazenou třikrát — jsou to samostatné objekty s vlastním nastavením a vlastní sadou odpovědí:

- **Engagement funkce na úrovni události** (tento článek) — jedno hlasování nebo jedna fronta otázek za celou událost. Nevztahuje se ke konkrétní session ani k místu. Hodí se pro jednoduché a online události, kde je jeden sál a jeden proud programu.
- **Engagement u session** — u typu session a u konkrétní session zapínáte *Hodnocení session*, *Otázky*, *Anonymní otázky* a *Hlasování* na záložce **Engagement**. Účastník se ptá přímo k přednášce, kterou sleduje, a najde to na detailu session v Programu nebo v Moje agendě. U konference s paralelními sály je tohle správná cesta.
- **Interaktivní záložky uvnitř Online modulu** — každá instance Online modulu má vlastní chat, otázky, anonymní otázky a hlasování vedle livestreamu. Patří ke sledování streamu, ne k události jako celku.

Když si nejste jistí, ptejte se, čeho se otázka týká: celé události, jedné přednášky nebo jednoho streamu.

### Hlasování

Hlasování je rychlá anketa během programu — jedna otázka, sada odpovědí, výsledek během pár desítek sekund. Používá se k rozproudění sálu, k orientačnímu průzkumu („kolik z vás už tohle nasazuje?“) a k soutěžím.

V dialogu **Nové hlasování** vyplníte **Otázku nebo název hlasování** a vyberete šablonu odpovědí:

- **Vlastní odpovědi** — napíšete si vlastní varianty.
- **Odpovědi Ano / Ne** — dvě předvyplněné možnosti.
- **Hodnocení 1 až 5** — škála, kterou nemusíte psát ručně.

Volitelně přidáte **Doplňující popis**, když samotná otázka nestačí.

Hlasování má stav publikace — dokud ho nepublikujete, účastník ho v aplikaci nevidí. Připravená, ale nepublikovaná hlasování jsou běžný způsob, jak si celý blok nachystat den předem. Stavy jde měnit i **hromadně** přes *Hromadně změnit stav*.

**Výsledky** otevřete u konkrétního hlasování tlačítkem *Výsledky*. Uvidíte grafy a můžete je otevřít v nové kartě — to je pohled, který se dává na projekci v sále. Celou sadu odpovědí stáhnete tlačítkem *Výsledky (Excel)* a přes *Upravit výsledky* zasáhnete do odpovědí, třeba doplníte hlas za účastníka, který hlasoval na papíře.

**Účastník výsledky nevidí, dokud je nezveřejníte.** Je to záměr: dokud hlasování běží, nemá průběžný stav ovlivňovat, jak lidé hlasují.

### Dotazník

Dotazník je delší forma než Hlasování — víc otázek, různé typy odpovědí, sbíráte je v průběhu události i po jejím skončení. Dvě typická použití: evaluace na závěr a doplnění informací, které od lidí potřebujete a nezískali jste je při registraci (dietní požadavky, zájem o navazující workshop, velikost trička).

U každé otázky (**+ Nová otázka dotazníku**) vybíráte v poli **Vyberte odpověď uživatele** jeden z pěti typů:

- **Odpoví vlastními slovy** — volný text.
- **Vybere pouze jednu** — právě jedna z nabídnutých odpovědí.
- **Vybere pouze jednu nebo vlastní text** — jedna odpověď, nebo si účastník napíše svou.
- **Může vybrat více** — libovolný počet nabídnutých odpovědí.
- **Může vybrat více a vlastní text** — několik odpovědí plus vlastní doplnění.

K otázce lze přidat **Doplňující popis**, když samotné znění nestačí. Pole **Odpověď** rozhoduje, jestli se účastník může k odpovědi vrátit: **Lze měnit**, nebo **Nelze měnit**.

Dotazník má tři stavy — **Nepublikováno**, **Publikováno** a **Uzavřeno**. Uzavřený dotazník účastník vidí, ale už do něj nemůže odpovídat; to je čistší konec sběru než smazání. Stavy jde měnit i **hromadně** přes *Hromadně změnit stav*.

**Výsledky** se zobrazují jako grafy, otevřete si je v nové kartě, celou sadu stáhnete přes *Výsledky (Excel)* a přes *Upravit výsledky* můžete odpovědi doplnit nebo opravit za konkrétního účastníka. Pokud jste dotazník omezili na skupinu, uvidíte ve výsledcích jen tu část.

**Kdy Hlasování a kdy Dotazník:** Hlasování je jedna otázka v reálném čase s výsledkem na projekci. Dotazník je sada otázek, kterou účastník vyplní ve svém čase a jejíž výsledky čtete až po skončení události.

### Otázky

Karta se v sekci Engagement jmenuje **Otázky** a sbírá dotazy na řečníka nebo panel za celou událost. Hodí se u online událostí a u jednodušších formátů s jedním sálem. Máte-li paralelní program, jsou správnou volbou otázky u jednotlivých sessions.

Funkce má dvě záložky: **Otázky** se samotnou frontou a **Nastavení** se třemi přepínači.

**Moderace.** Fronta je rozdělená na **Aktivní**, **K moderaci** a **Archivované** a u každé záložky vidíte počet. S jednotlivou otázkou pracujete přímo v seznamu — archivujete ji, smažete, nebo označíte jako hlavní; tlačítko *Archivovat všechny* uklidí frontu najednou. Otázky lze přidávat i z administrace přes **+ Nová otázka**, což je praktické, když dotaz přijde mimo aplikaci. Přepínač **Schvalování otázek před veřejným zobrazením** rozhoduje, jestli otázka jde rovnou ven, nebo napřed do fronty k moderaci.

**Možnost zasílat otázky anonymně.** Samostatný přepínač na úrovni celé funkce. Anonymita zvyšuje ochotu ptát se na nepříjemné věci, ale u takto poslaných otázek neuvidíte, kdo se ptal.

**Umožnit přidávat otázky ve webové aplikaci bez přihlášení.** Účastník položí dotaz bez přihlášení do účastnické aplikace přes odkaz zobrazený na projekci a **kód**, který si tady nastavíte. Užitečné pro hosty, kteří v seznamu účastníků nejsou.

**Možnosti zobrazení** nabízejí čtyři pohledy pro různé lidi u různých obrazovek:

- **Zobrazit k projekci** — pohled pro produkci události: pokládat otázky, řadit je do fronty, označovat jako zodpovězené, hodnotit lajky a archivovat.
- **Zobrazit k projekci se streamy** — totéž, ale otázky jsou ve formátu vhodném pro projekci se streamem.
- **Zobrazit hlavní dotaz k projekci** — zobrazí jen jednu otázku označenou jako hlavní.
- **Zobrazit frontu dotazů** — pohled pro řečníka; obsahuje otázky přidané do fronty ze zobrazení se streamy.

Otázky stáhnete přes *Výsledky (Excel)*.

### Registrační údaje

Registrační údaje jsou proti zbylým třem funkcím jiný typ věci: **nic nesbírají**. Zpřístupní účastníkovi v aplikaci přehled toho, co sám vyplnil při registraci — na jednom místě, kam se může kdykoli podívat. Odpadají tím dotazy typu „přihlásil jsem se na ten workshop, nebo ne?“.

Celé nastavení je jedno pole: popis modulu, který se účastníkovi ukáže na hlavní stránce události. Výchozí text zní *Vaše údaje zadané při registraci* a dá se přepsat.

Registrační údaje nemají výsledky ani vlastní export — jsou jen pohledem na data, která už v události jsou. Odpovědi z registrace exportujete ze sekce *Registrace* a z reportingu, ne odsud.

### Co platí pro všechny engagement funkce

- **Viditelnost pro skupiny** se nastavuje u konkrétní funkce, ne centrálně; na kartě funkce ji rovnou vidíte. Dotazník viditelný jen pro skupinu *Produkce* je běžný způsob, jak sbírat interní zpětnou vazbu odděleně od účastníků.
- **Pořadí a publikaci v aplikaci** řešíte v levém menu v sekci **Účastnická aplikace**, ne v Engagementu. Tam také rozhodnete, jestli se funkce na hlavní stránce zobrazí jako textový blok, nebo obrázek.
- **Změnit název a smazat.** Na kartě funkce jsou dvě tlačítka. *Změnit název* přepíše výchozí označení — *Hlasování* na *Hlasujte o nejlepší přednášce*, *Dotazník* na *Evaluace konference* — a nový název se propíše na hlavní stránku aplikace.
- **Prázdná funkce působí hůř než vypnutá.** Pokud pro Hlasování nemáte otázku a pro soutěž cenu, nezapínejte je a přidejte je později.

## Na co si dát pozor

### Funkce je přidaná, ale účastník ji v aplikaci nevidí

Hlasování a Dotazník jsou viditelné až po doplnění odpovědí a publikaci. Zkontrolujte stav publikace a pak sekci **Účastnická aplikace** — funkce může být připravená a přitom v aplikaci nepublikovaná. Třetí častou příčinou je omezení viditelnosti na skupinu, do které konkrétní účastník nepatří.

### Organizátor čeká, že účastníci uvidí výsledky hlasování hned po odeslání

Neuvidí. Výsledky se účastníkovi zobrazí, až když je zveřejníte — typicky promítnutím v sále přes *Výsledky* a otevření v nové kartě. Pokud chcete, aby lidé viděli, jak sál hlasoval, musí to někdo na pódiu udělat; samo se to nestane.

### Otázky z publika běží bez moderátora

Fronta bez obsluhy je horší než vypnutá funkce — lidé se ptají a nikdo neodpovídá. Než otázky zapnete, určete, kdo je během programu sleduje, a domluvte s moderátorem, odkud si otázky bere. U větších událostí zapněte schvalování před veřejným zobrazením, ať se do sálu nedostane všechno.

### Hlasování založené na úrovni události, i když otázka patří k jedné přednášce

Engagement funkce na úrovni události se nevztahuje ke konkrétní session. Pokud se ptáte na obsah jedné přednášky, patří otázka k té session — jinak ji uvidí i lidé, kteří byli v jiném sále, a výsledek nic neřekne.

### Anonymní otázky zapnuté a pak je potřeba dohledat, kdo se ptal

Přepínač platí pro celou funkci a u anonymně poslaných otázek se k autorovi zpětně nedostanete. Rozmyslete si předem, jestli je pro danou událost důležitější otevřenost, nebo možnost se k dotazu vrátit.

### U otázky dotazníku zůstane výchozí *Lze měnit*, i když jde o soutěž nebo závaznou volbu

Výchozí nastavení dovolí účastníkovi odpověď kdykoli přepsat. U evaluace to nevadí; u soutěžní otázky nebo u volby, podle které něco objednáváte, přepněte na *Nelze měnit*.

### Dotazník míří i na lidi, kteří na události nebyli

Dotazník v aplikaci uvidí ten, kdo aplikaci otevře. Pokud chcete zpětnou vazbu od těch, kdo dorazili, omezte viditelnost na skupinu podle stavu účasti a upozorněte na dotazník Oznámením — jinak sbíráte hodnocení i od lidí, kteří událost nezažili.

### Dotazník nemá vlastní úvodní text

V administraci není pole, kam napsat odstavec před otázkami; dotazník začne rovnou první otázkou. Kontext, proč ho vyplnit, nesete jinudy: názvem funkce přes *Změnit název* (*Dotazník* na *Evaluace konference*), **Doplňujícím popisem** u první otázky a Oznámením, které na dotazník odkáže.

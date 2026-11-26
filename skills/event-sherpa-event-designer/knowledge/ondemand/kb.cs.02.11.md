<!-- source: kb.cs.02.11 -->

---
title: "Správa objednávek a faktur"
description: "Kde u placené události najdete všechny objednávky a co s nimi v detailu uděláte — faktury, fakturační údaje, refundace, exporty."
modules: ["vstupenky_a_objednavky"]
last_updated: "2026-10-26"
version: 11
---

> [!info] Krátce
> **Objednávky** jsou nákupní strana placené události — kdo co koupil, jestli zaplatil, jaká faktura mu vznikla a jestli se ke vstupence někdo zaregistroval. V detailu objednávky opravíte fakturační údaje i údaje účastníka u vstupenky, stáhnete fakturu i PDF vstupenku, pošlete upozornění tomu, kdo nedokončil registraci nebo zatím nezaplatil zálohovou fakturu, u zaplacené objednávky bez evidované vrácené částky podáte žádost o refundaci a nezaplacenou objednávku zrušíte nebo smažete. V žádosti o refundaci zvolíte, kolik kupující dostane zpět a kdo zaplatí platební poplatek. Určíte také, komu přijde e-mail o dokončení.

## Jak začít

- Objednávky existují jen u události se zapnutými **Placenými vstupenkami**. U neplacené události žádné nevznikají.
- Otevřete je z nabídky **Nástroje** ve spodní části levého menu, dlaždicí *Objednávky* v sekci **Nástroje** na **Přehledu** události, nebo tlačítkem *Objednávky* vpravo nahoře na stránce *Placené vstupenky*.
- U **registrace s doplněním informací** vzniká objednávka dřív než registrace: kupující zaplatí a účastník se teprve registruje. Počítejte s tím, že seznam objednávek a seznam registrací se nikdy nepotkají jedna ku jedné.
- Rozmyslete si dopředu, jak budete řešit odstoupení: u zaplacené objednávky bez evidované vrácené částky podáte **žádost o refundaci**, nezaplacenou **zrušíte** nebo **smažete**.
- Faktury nelze ručně mazat ani přečíslovávat. Oprava fakturačních údajů přepíše údaje na stávajících fakturách, nová verze dokladu nevzniká.

## Detail

### Co v seznamu objednávek vidíte

Tabulka objednávek má sloupce **Objednávající** (jméno a e-mail kupujícího — může to být někdo jiný než účastník), **Objednáno**, **Stav objednávky**, **Celkem**, **Měna**, **Zaplaceno** (skutečně uhrazená částka), **Vstupenek** a **Registrováno**. Podle většiny z nich lze řadit.

Stav objednávky je jedna ze čtyř hodnot:

- **Zaplaceno** — u chipu je i datum úhrady.
- **Nezaplaceno** — vystavená zálohová faktura čeká na peníze.
- **Zrušeno** — u chipu je datum zrušení.
- **Zdarma** — objednávka s nulovou částkou (vstupenka zdarma nebo stoprocentní slevový kód). Vzniká normální objednávka včetně dokladu.

Nad tabulkou je **vyhledávání podle jména, e-mailu nebo firmy** a sada filtrů:

- **Chipy s počty** — *Vše*, *Zaplacené*, *Nezaplacené*, *Neregistrované*, *Zrušené*. Čísla u chipů ukazují, kolik objednávek do které skupiny spadá, takže hned vidíte, kde je práce.
- **Měna** — u události, která prodává ve víc měnách.
- **Registrace** — volby *Registrovaní* / *Neregistrovaní*, potvrzuje se tlačítkem *Použít filtr*.
- **Upozornění k registraci** — volby *Dosud neupozornění* / *Již upozornění*. Zúží seznam na objednávky s nedokončenou registrací podle toho, jestli jste účastníkovi upozornění už poslali.
- **Upomínka platby** — stejné dvě volby pro nezaplacené objednávky: komu upomínka už odešla a komu ještě ne.

Chip *Neregistrované* zúží seznam na objednávky, kde registrace ještě nedoběhla. Kolik vstupenek z konkrétní objednávky je doregistrovaných, přečtete ze sloupce *Registrováno* a přesně pak z tabulky vstupenek v detailu.

### Detail objednávky

Objednávka se rozbalí **přímo v řádku** (šipka na konci řádku), nechodí se na samostatnou stránku. V hlavičce detailu je **Způsob platby** (karta, zálohová faktura, nebo *Zdarma*), **Variabilní symbol** a datum, kdy bylo **Zaplaceno**.

Nezaplacená objednávka se zálohovou fakturou má v hlavičce navíc **Upomínka platby** s tlačítkem **Upozornit**. Pošle kupujícímu stejný e-mail jako hromadná položka **Nezaplaceným**, jen této jedné objednávce. Dokud upomínka čeká na odeslání, je u ní stav **Čeká ve frontě** a tlačítko je neaktivní. Po odeslání se zobrazí **Odesláno** s datem a časem a tlačítko se změní na **Odeslat znovu**.

Pod hlavičkou je tabulka **Vstupenky** se sloupci *Název*, *E-mail*, *Cena vstupenky*, *Cena po slevě*, *Vstupenka*, *Slevový kód* a *Registrace*. U každé vstupenky jsou akce:

- **Vstupenka** — stáhne PDF vstupenku s QR kódem. Je k dispozici u vstupenky s dokončenou registrací.
- **Upozornit** — u vstupenky bez dokončené registrace pošle e-mail s odkazem pro registraci. Po odeslání se u vstupenky zobrazí stav **Odesláno** s datem a časem a tlačítko se změní na **Odeslat znovu**; pět minut po každém odeslání odkazu zůstává neaktivní, aby nevznikl duplicitní e-mail.
- **Ikona tužky** — otevře úpravu údajů účastníka u dané vstupenky (popis níže).

### Faktury

Jakou fakturu si stáhnete, závisí na způsobu platby:

- **Platba kartou** — rovnou **konečná faktura** (daňový doklad).
- **Bankovní převod** — **zálohová faktura** před úhradou, **konečná faktura** po připsání peněz.

Jednotlivý doklad stáhnete tlačítkem **Stáhnout fakturu** v detailu objednávky. Všechny faktury najednou stáhnete přes **Exporty → Export PDF faktur**.

### Úprava fakturačních údajů

Tlačítko **Upravit fakturační údaje** otevře formulář **Fakturační údaje** s poli *Společnost*, *Adresa*, *Město*, *PSČ*, *Země*, *IČO*, *DIČ* a *Poznámka*, předvyplněnými aktuálními fakturačními údaji objednávky.

Po uložení se opravené údaje propíšou do objednávky a do všech jejích faktur. **Nová faktura nevzniká:** doklady si ponechají svá čísla a po stažení tlačítkem **Stáhnout fakturu** už nesou opravené údaje.

Úprava nemění položky, ceny, DPH ani číslo faktury a neovlivní stav platby ani údaje účastníků. Fakturu, kterou kupující už dostal e-mailem, systém znovu neposílá.

### Úprava údajů účastníka

Ikona tužky u vstupenky otevře boční panel s poli *Jméno*, *Příjmení*, *E-mail*, *Společnost*, *Pozice* a *Telefon*. Údaje upravíte, dokud se ke vstupence nikdo nezaregistroval. Typicky opravujete překlep v e-mailu, kvůli kterému registrační odkaz nedorazil, nebo vstupenku předáváte jiné osobě.

- **Uložení nic neodešle.** Registrační odkaz novému účastníkovi pošlete tlačítkem **Upozornit** u vstupenky.
- **Odkaz se úpravou nemění.** Při otevření vždy nabídne aktuální údaje vstupenky, takže i odkaz, který dřív odešel na původní adresu, povede k registraci nového účastníka.
- **Smazat data** po potvrzení vymaže všechna pole včetně e-mailu. Hodí se jen tehdy, když nový účastník zatím není známý (proč, viz *Na co si dát pozor*). Vstupenka bez e-mailu tlačítko **Upozornit** nemá; odkaz pošlete, až e-mail znovu doplníte.
- **Po dokončení registrace** se panel otevře jen pro čtení. Údaje zaregistrovaného účastníka změníte v sekci **Registrace**.

Původní údaje se po úpravě nikde neuchovávají. Pokud je budete potřebovat, poznamenejte si je předem.

### Refundace, zrušení a smazání objednávky

Které akce máte v detailu k dispozici, se řídí stavem objednávky.

**U zaplacené objednávky** se tlačítko **Refundace objednávky** nabízí pouze tehdy, pokud u ní dosud není evidovaná žádná vrácená částka a splňuje ostatní podmínky refundace. Otevře okno s žádostí o refundaci. Žádost není okamžitý převod peněz: peníze se kupujícímu vrátí až po jejím zpracování, které dokončuje Happenee.

Pod nadpisem okna je částka **Zaplaceno a zatím nevráceno**, tedy kolik z objednávky můžete vrátit. Pod otázkou **Kolik kupující dostane zpět** vyberete jednu ze tří možností. U každé okno rovnou ukazuje, kolik **Kupující dostane**, a v popisu, kdo zaplatí platební poplatek a v jaké výši:

- **Zaplacenou částku sníženou o poplatek** — předvybraná možnost. Poplatek zaplatí kupující: systém ho z vracené částky odečte a kupující dostane zbytek.
- **Celou zaplacenou částku** — kupující dostane zpět celou částku a poplatek zaplatí organizátor.
- **Jinou částku** — do pole přímo v této možnosti zadáte, kolik kupující dostane zpět; nápověda pod polem ukazuje nejvyšší možnou částku. Poplatek zaplatí organizátor. Jen u této možnosti je povinná **Interní poznámka** s důvodem (nejvýše 200 znaků), u ostatních je nepovinná.

Když sazba platebního poplatku není k dispozici, první možnost nejde vybrat, předvybraná je *Celou zaplacenou částku* a okno to pod možnostmi vysvětlí. První možnost je nedostupná i tehdy, když by kupujícímu po odečtení poplatku nic nezbylo.

Přepínači **Informovat kupujícího o dokončení refundace** a **Informovat organizátora o dokončení refundace** určíte, komu přijde e-mail s opravným daňovým dokladem. Odejde až po dokončení refundace. Při otevření okna je zapnutý organizátor a vypnutý kupující; informovat můžete jednoho, oba nebo nikoho. Zapnutý přepínač ukáže pole pro adresu; u kupujícího je předvyplněná adresa z objednávky a můžete ji přepsat. Do každého pole lze zadat až deset adres oddělených čárkou.

Žádost odešlete tlačítkem **Odeslat žádost** dole v okně. Před odesláním ještě potvrdíte dialog, který zopakuje, kolik kupující dostane zpět a kdo zaplatí poplatek. Zároveň vypíše, na které adresy výsledek přijde, nebo upozorní, že e-mailem nebude informován nikdo.

Jakmile je u objednávky evidovaná jakákoli vrácená částka, hlavní tlačítko refundace se v rozbaleném detailu seznamu objednávek už nezobrazí. Platí to i pro částečnou refundaci a refundaci sníženou o poplatek. Rozdíl mezi zaplacenou a vrácenou částkou sám o sobě neznamená, že se tlačítko nabídne znovu. Stav refundace a dostupné doklady zůstávají viditelné.

**U nezaplacené objednávky** jsou místo refundace tlačítka **Zrušit objednávku** a **Smazat objednávku**. Zrušení nechá objednávku v seznamu se stavem *Zrušeno* i s datem, smazání ji odstraní včetně dokladu a uvolní obsazený kus ve statistikách vstupenek.

### Hromadné upozornění e-mailem

Vpravo nahoře nad seznamem je rozbalovací nabídka **Upozornit e-mailem** se dvěma položkami. Číslo u položky říká, kolika příjemcům upozornění právě teď odejde: u **Nezaplaceným** jsou to objednávky, u **Neregistrovaným** jednotliví účastníci. Od chipu *Neregistrované*, který počítá objednávky, se proto může lišit.

Nabídka se řídí stejným výběrem jako seznam. Když seznam zúžíte hledáním, chipem nebo filtrem, čísla se přepočítají a upozornění odejde jen tomuto výběru. Bez filtrů osloví všechny, kterých se v události týká.

- **Nezaplaceným** — pošle kupujícím upozornění, že objednávka zatím není uhrazená. E-mail má vlastní text v češtině, angličtině nebo slovenštině podle jazyka objednávky, v příloze nese zálohovou fakturu a u registrace s doplněním informací dodává, že odkaz na registraci přijde po zaplacení. Odejde jen objednávkám, ke kterým zálohová faktura existuje, tedy platbám bankovním převodem; přerušená platba kartou zálohovou fakturu nemá a upozornění nedostane. Zrušené, refundované a smazané objednávky a objednávky bez platného e-mailu kupujícího systém vynechá.
- **Neregistrovaným** — znovu pošle registrační odkaz účastníkům zaplacených objednávek a objednávek zdarma, kteří registraci nedokončili. Typicky těsně před událostí, když zjistíte, že část lidí zaplatila, ale nedokončila registraci, a nechcete rozesílat odkazy po jednom.

Obě položky potvrzujete v dialogu. Upozornění neodcházejí v okamžiku kliknutí: administrace je zařadí do fronty a systém je odesílá postupně, po jednotlivých událostech. Objednávka nebo vstupenka, která ve frontě ještě čeká, se dalším kliknutím nezařadí podruhé, takže opakované kliknutí duplicitní e-maily nevytvoří.

Upozornění můžete poslat opakovaně. Jakmile fronta doběhne, další kliknutí na **Nezaplaceným** osloví znovu všechny objednávky z aktuálního výběru, které jsou stále nezaplacené. Kdo už upomínku dostal, toho vynecháte filtrem **Upomínka platby** → *Dosud neupozornění*. U registračních odkazů platí navíc pauza: účastník, kterému odkaz odešel v posledních pěti minutách, ho znovu nedostane.

### Exporty

Tlačítko **Exporty** vpravo nahoře nabízí tři soubory:

- **Objednávky (Excel)** — řádek za objednávku: kupující, částky, stav, fakturační údaje. Podklad pro účetní.
- **Objednávky po vstupenkách (Excel)** — řádek za vstupenku, tedy rozpad objednávek na jednotlivé kusy a účastníky.
- **Export PDF faktur** — všechny faktury události najednou, bez stahování po jedné.

## Na co si dát pozor

### Objednávky se hledají mezi hlavními položkami levého menu

V hlavním seznamu nejsou. Vedou k nim tři cesty: nabídka **Nástroje** ve spodní části levého menu, dlaždice *Objednávky* v sekci *Nástroje* na **Přehledu** události a tlačítko *Objednávky* vpravo nahoře na stránce *Placené vstupenky*. U neplacené události objednávky nevzniknou vůbec.

### Po opravě fakturačních údajů čekáte, že kupující dostane novou fakturu

Oprava přepíše údaje na stávající faktuře pod stejným číslem a nic dalšího neudělá: novou fakturu nevystaví a e-mailem ji znovu neodešle. Kupující má dál PDF s původními údaji. Opravenou fakturu stáhněte tlačítkem **Stáhnout fakturu** a pošlete mu ji sami s tím, že původní už nemá používat.

### Zaplacená objednávka se maže v domnění, že se tím vrátí peníze

U zaplacené objednávky je **Refundace objednávky**, ne mazání. *Zrušit* a *Smazat* patří k nezaplaceným objednávkám — samy o sobě žádné peníze nevracejí.

### Necháte předvybranou možnost, i když má kupující dostat zpět všechno

Okno při otevření předvybere **Zaplacenou částku sníženou o poplatek**, takže když nic nezměníte, kupujícímu se platební poplatek odečte. Výši poplatku i částku, kterou kupující dostane, vidíte přímo v této možnosti. Pokud má kupující dostat zpět všechno, například protože událost rušíte vy, vyberte **Celou zaplacenou částku**. Poplatek pak zaplatí organizátor.

### Kupující zaplatil, ale ve statistikách vstupenek je pořád rozdíl mezi prodanými a zaregistrovanými

U registrace s doplněním informací je mezi *prodáno* a *zaregistrováno* logický rozdíl. Prodáno znamená zaplacenou objednávku, zaregistrováno znamená, že účastník prošel registračním formulářem. Rozdíl je normální a klesá, jak lidé registrace doplňují.

### Hromadné upozornění dostanou i lidé, kteří na událost nedorazí

*Upozornit e-mailem* osloví všechny, kdo odpovídají aktuálnímu výběru; bez filtrů je to celá událost. Před odesláním proto seznam zužte a zkontrolujte číslo u položky. Když víte, že část kupujících už odřekla, pošlete upozornění jednotlivě z detailu objednávky: registrační odkaz tlačítkem **Upozornit** u vstupenky, upomínku platby tlačítkem **Upozornit** u údaje **Upomínka platby**. Objednávku kupujícího, který odřekl, rovnou zrušte, další upozornění pak nedostane.

### Upozornění nezaplaceným nedorazí kupujícímu, který nedokončil platbu kartou

Položka **Nezaplaceným** pošle upozornění jen objednávkám, ke kterým existuje zálohová faktura, tedy platbám bankovním převodem. Přerušená platba kartou zálohovou fakturu nemá, a systém ji proto vynechá. Takového kupujícího oslovte jinou cestou, nebo objednávku zrušte.

### Stejný stav se jmenuje jinak v Objednávkách a ve Statistikách vstupenek

V *Objednávkách* je chip **Zrušené** (stav *Zrušeno*), ve *Statistikách vstupenek* stejná skupina figuruje jako **Stornované**. Jde o totéž, jen jinak pojmenované — při odsouhlasování čísel s účetní o to nezakopněte.

### Vstupenka se předává jiné osobě smazáním údajů

Po **Smazat data** nemá vstupenka e-mail a registrační formulář pak přijme jakoukoli adresu. Registraci tak může dokončit kdokoli, kdo odkaz má, včetně původního adresáta, kterému jste ho poslali dřív. Když nového účastníka znáte, údaje rovnou přepište a pošlete mu odkaz tlačítkem **Upozornit**. Starý odkaz pak nabídne už jeho údaje.

### Celou účastnickou kartu hledáte v objednávce

Objednávka drží nákupní stranu — kupujícího, částky, doklad a údaje u jednotlivých vstupenek. Odpovědi z registračního formuláře, skupiny a stav účasti najdete v sekci **Registrace**. Toto rozdělení je záměrné: objednávka je o nákupu, registrace o účastníkovi.

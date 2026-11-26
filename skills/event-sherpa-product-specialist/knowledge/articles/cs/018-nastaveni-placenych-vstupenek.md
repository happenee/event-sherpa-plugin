# Nastavení placených vstupenek

> Jak zapnout a nastavit placené vstupenky včetně online plateb, faktur a slevových kódů.

- Článek v Help Centru: https://help.happenee.com/cs/articles/18-nastaveni-placenych-vstupenek
- English version: https://help.happenee.com/en/articles/18-setting-up-tickets
- Kolekce: Nastavení eventu a registrace
- Aktualizováno: 2026-10-26

---

> [!info] Krátce
> Placené vstupenky zapnete v **Nastavení události** přepínačem **Placené vstupenky**. Systém umí online platby kartou (včetně Apple Pay a Google Pay), zálohové faktury, slevové kódy a skupiny vstupenek. Prodej vstupenek ve výchozím stavu sám skončí s koncem události, takže vstupenku na proběhlou událost už nikdo nekoupí; jiný termín nebo prodej bez společného konce nastavíte v části **Ukončení prodeje**. Jednotlivou vstupenku spravujete v bočním panelu se záložkami **Detaily**, **Údaje o účastníkovi** a **Nastavení vstupenky**.

## Jak začít

- Ujasněte si **cenový model** — jeden typ vstupenky, víc typů (early bird / standard / VIP), balíčky, individuální pozvánky zdarma.
- Rozhodněte, zda chcete **registraci s doplněním informací** (účastník po zaplacení ještě projde formulářem), nebo **automatickou registraci po nákupu vstupenky** (vstupenka přijde ihned, bez formuláře). Detail v článku *Nastavení typu registrace a doplňujících otázek*.
- Připravte si fakturační údaje a položky na faktuře, sazby DPH (chybějící sazbu přidá zákaznická podpora) a měnu.
- Placené vstupenky **nelze** kombinovat se schvalovanou registrací a povinná kontaktní pole řídí nastavení registračního formuláře.
- Pro GTM měřicí kódy kontaktujte **zákaznickou podporu**.
- Rozmyslete, **kdy má prodej skončit**. Ve výchozím stavu skončí s koncem události; jiný termín nastavíte v části **Ukončení prodeje** na záložce **Nastavení vstupenek**.

## Detail

### Aktivace placených vstupenek

V menu události otevřete **Nastavení události** → sekci **Placené vstupenky** a zapněte přepínač. Objeví se nové pole **Placené vstupenky** v levém menu a následné povinné kroky:

1. Zvolte **měnu** — CZK nebo EUR (další měny lze doplnit na vyžádání).
2. Zvolte **typ registrace po nákupu** — *Automatická registrace po nákupu vstupenky*, nebo *Registrace s doplněním informací*.
3. Pokud používáte registraci s doplněním informací, systém vás upozorní, abyste v **Registračním formuláři** nastavili povinná kontaktní pole.

> Pokud jsou aktivní placené vstupenky, je **nutné vytvořit alespoň jednu vstupenku**. Jinak bude registrace na událost uzavřena.

### Vytvoření a editace vstupenky

Novou vstupenku přidáte na záložce **Vstupenky** tlačítkem **+ Nová vstupenka**, existující otevřete ikonou úprav v jejím řádku. Otevře se boční panel se třemi záložkami — **Detaily**, **Údaje o účastníkovi** a **Nastavení vstupenky**. Pole **Název vstupenky** je nad záložkami společné a je povinné — je to název, který uvidí účastník (například *Standard*, *VIP*, *Early Bird*). Změny uložíte tlačítkem **Uložit**.

### Záložka Detaily

Na záložce **Detaily** nastavíte cenu a podobu vstupenky:

- **Odlišný název vstupenky na faktuře** — ve výchozím stavu se na faktuře použije název vstupenky. Když přepínač zapnete, objeví se pole **Položka na faktuře** pro jiné označení v daňovém dokladu (hodí se, když má účetnictví používat jiný název než ten marketingový).
- **DPH** — sazba daně. Pokud potřebná sazba DPH chybí, přidá ji zákaznická podpora (kontaktujte ji). Tlačítko **DPH kalkulačka** pomůže přepočítat částku mezi cenou s daní a bez daně.
- **Cena bez DPH** — částka bez daně v měně události (pole nese měnu, například *Cena bez DPH CZK*).
- **Popis vstupenky** — volitelný text, který účastník uvidí u vstupenky v nákupním prostředí.

### Stav vstupenky

Poslední volba na záložce **Detaily** určuje viditelnost vstupenky:

- **Publikováno** — vstupenka je veřejně zobrazená v přehledu vstupenek a je dostupná k nákupu.
- **Neveřejné** — vstupenka se nezobrazuje v přehledu, ale je dostupná k nákupu přes samostatný odkaz nebo ve **Skupině vstupenek**. Hodí se pro partnerské nebo VIP vstupenky, které nechcete ukazovat všem.
- **Nepublikováno** — vstupenka není nikde na platformě viditelná ani dostupná k nákupu, a to ani přes odkaz na vstupenku, ani ve **Skupině vstupenek**.

Vstupenku **nelze smazat**, pokud už byla použita. Nepoužitou vstupenku smazat lze.

### Záložka Údaje o účastníkovi

Na záložce **Údaje o účastníkovi** určujete, která kontaktní pole účastník vyplní a která jsou povinná. K dispozici jsou pole **Jméno**, **Příjmení**, **Společnost**, **Pracovní pozice** a **Telefon** s volbami **Povinné**, **Nepovinné** a **Skrýt**; **E-mail** je vždy povinný. Pod nimi jsou **Vlastní pole kontaktu** se stejnými volbami — ta se zakládají a spravují v Nastavení workspace, tady jen rozhodnete o jejich použití u této vstupenky.

Chování polí závisí na zvoleném typu registrace po nákupu (viz *Aktivace placených vstupenek*):

- **Registrace s doplněním informací** — účastník po zaplacení projde registračním formulářem, takže povinnost polí se řídí nastavením kontaktních údajů v **Registračním formuláři**. Pole, která formulář označuje jako povinná, jsou tady zamčená na **Povinné** (sjednoceno s formulářem); u ostatních polí nastavíte **Povinné**, **Nepovinné** nebo **Skrýt** podle potřeby této vstupenky.
- **Automatická registrace po nákupu vstupenky** — registrační formulář se nevyužívá a vstupenka přijde hned po nákupu. Která pole jsou povinná, proto nastavujete přímo zde u vstupenky a objednávající je vyplní při nákupu.

### Opakovaný nákup a e-mail účastníka

E-mail objednávajícího slouží jako kontakt k objednávce: stejná osoba může nakupovat opakovaně, třeba pro různé kolegy. Kontrola stejného e-mailu se týká až **účastníka uvedeného u vstupenky** v téže události. Vyplní-li objednávající svůj e-mail i jako účastník, platí pro něj pravidla účastníka.

- Při **automatické registraci po nákupu** nelze dokončit další objednávku pro účastníka, jehož e-mail už je na platné dokončené objednávce této události. Platí to i tehdy, když původní objednávka čeká na platbu nebo na automatické provedení registrace. Samotný rozpracovaný košík jiné osoby nákup neblokuje.
- Při **registraci s doplněním informací** nákupní stránka na předchozí nákup nebo registraci upozorní, ale kupující může v nákupu pokračovat.

Pokud původní objednávka není zaplacená, kupující ji může dokončit. Když ji kupující využít nechce, zrušte ji v detailu objednávky tlačítkem **Zrušit objednávku**, případně **Smazat objednávku** (viz *Správa objednávek a faktur*). Zrušená, smazaná nebo plně refundovaná objednávka sama o sobě další nákup neblokuje. Při automatické registraci ale nákup zablokuje i existující registrace účastníka na událost, a to nezávisle na stavu původní objednávky. V jedné objednávce nelze zadat stejný účastnický e-mail na více vstupenek.

### Záložka Nastavení vstupenky

Na záložce **Nastavení vstupenky** zapínáte volitelná pravidla prodeje. Každé je přepínač (**Aktivní** / **Neaktivní**); po zapnutí se objeví jeho pole:

- **Možnost koupit vstupenku bez uvedení údajů o účastníkovi** — objednávající koupí vstupenku, aniž by vyplnil e-mail účastníka. Vstupenka se vygeneruje později — buď jakmile objednávající údaje doplní, nebo když se účastník přes zaslaný odkaz zaregistruje sám. Užitečné, když firma kupuje vstupenky dopředu a zatím neví, kdo přesně přijde.
- **Omezit maximální počet vstupenek** — pole **Počet vstupenek** nastaví celkový počet k prodeji. Po vyprodání vidí účastník v nákupním prostředí hlášku *Vyprodáno*.
- **Omezit období prodeje** — pole **Začátek prodeje** a **Konec prodeje** vymezí prodej jednotlivé vstupenky. Začátek platí od půlnoci a konec do konce vybraného dne v časovém pásmu události. Pokud dřív nastane společný konec prodeje celé události (viz *Ukončení prodeje pro celou událost*), platí ten.
- **Nákup vstupenky v balíčku** — minimální odběr v násobcích. Při kroku 5 si objednávající může koupit jen 5, 10, 15 vstupenek atd. Hodí se pro hromadné partnery nebo slevové balíčky.
- **Přiřadit do skupiny** — po registraci účastníka (ne po zaplacení objednávky) se účastník automaticky přidá do vybrané skupiny. Skupinu využijete pro cílenou komunikaci, viditelnost obsahových a engagement funkcí nebo push notifikace v účastnické aplikaci. **Přiřazení platí jen dopředu:** kdo se zaregistroval dřív, než jste volbu zapnuli, do skupiny nespadne a systém ho tam zpětně nedoplní.

### Co systém ze vstupenky pozná a co ne

Název a popis vstupenky jsou pro systém jen text. Když vstupenku pojmenujete *Jednodenní* nebo *Dvoudenní*, systém s tím dál nepracuje — nerozlišuje délku vstupu, nehlídá, na které dny účastník přijde, a do kalendáře přidá vždy celý rozsah události. Rozdíl mezi typy vstupenek existuje jen v tom, co si přečte člověk.

Účastník název vstupenky uvidí v potvrzovacím e-mailu a na faktuře — nebo tam uvidí **Položku na faktuře**, pokud jste ji nastavili odlišně. Obsluha při odbavení ale název vstupenky nevidí. Po naskenování QR kódu se jí zobrazí jméno, příjmení, společnost a skupiny účastníka, nic dalšího.

Praktický důsledek: pokud potřebujete na místě rozlišit typy vstupenek, zapněte u vstupenky **Přiřadit do skupiny** a tutéž skupinu pak vyberte k zobrazení při skenování v nastavení odbavení. Skupinu i její přiřazení připravte před spuštěním prodeje.

### Ukončení prodeje pro celou událost

Prodej vstupenek ve výchozím stavu sám skončí s koncem události, aby nikdo omylem nekoupil vstupenku na událost, která už proběhla. Pravidlo najdete nahoře na záložce **Nastavení vstupenek** (platí pro celou událost) v části **Ukončení prodeje**. V poli **Kdy ukončit prodej** vyberete jednu z možností:

- **Podle konce události** — výchozí volba. Prodej skončí v okamžiku, kdy skončí událost, a když termín události posunete, posune se i konec prodeje. Pokud událost nemá vyplněnou hodinu konce, prodej skončí o půlnoci po jejím posledním dni.
- **Vlastní datum a čas** — prodej skončí v termínu, který zadáte, dřív i později než událost. Datum a čas upravíte každé zvlášť ikonou úprav a úpravu potvrdíte přímo u pole.
- **Neomezeně** — společný konec se nepoužije a prodej omezují jen data u jednotlivých vstupenek. Vstupenka, která nemá vyplněný vlastní **Konec prodeje**, se pak dá koupit i po skončení události.

Zvolená možnost se uloží hned, bez dalšího potvrzení. Pod polem vidíte údaje **Časové pásmo** a **Společný konec prodeje**, tedy okamžik, kdy prodej skutečně skončí. Rozhoduje časové pásmo události včetně přechodu mezi letním a zimním časem, ne pásmo vašeho počítače. Čas, který při změně letního času neexistuje nebo nastává dvakrát, uložit nejde; zvolte jiný.

Když prodej skončí, uvidíte tu i důvod: *Prodej je ukončen, protože událost již skončila.*, nebo u vlastního termínu *Prodej je ukončen podle nastaveného data a času.*

Společný konec a **Omezit období prodeje** u jednotlivé vstupenky platí současně a rozhoduje ten konec, který nastane dřív. Vstupenku, jejíž prodej začíná až po společném konci, nepůjde koupit vůbec. Pokud chcete vědomě prodávat i po skončení události, zvolte **Vlastní datum a čas** s pozdějším termínem a zkontrolujte **Konec prodeje** u jednotlivých vstupenek.










### Co vidí kupující po skončení prodeje

Vstupenka, jejíž prodej skončil, z nabídky zmizí a ostatní vstupenky se prodávají dál. Když skončí prodej všech vstupenek události, nákup nahradí stránka **Prodej vstupenek byl ukončen.** s vysvětlením, že už vytvořené objednávky zůstávají platné. Stránka se neukáže, pokud prodej některé vstupenky teprve začne. Neukáže se ani jen proto, že je nabídka prázdná nebo že jsou vstupenky nepublikované či vyprodané.

Konec prodeje platí stejně pro veřejnou nabídku, přímý odkaz na neveřejnou vstupenku i **Skupiny vstupenek**. Výjimkou není ani košík otevřený před koncem prodeje: objednávku se vstupenkou, jejíž prodej skončil, kupující nedokončí. Ukončení prodeje neruší objednávky, registrace ani platby, které už vznikly.



### Nastavení vstupenek (platby na úrovni události)

Na záložce **Nastavení vstupenek** (platí pro celou událost, ne pro jednu vstupenku) nastavíte platby:

- **Možnosti platby** — **Platba kartou i bankovním převodem**, **Jen platba kartou**, nebo **Jen bankovním převodem**. U platby kartou (včetně Apple Pay a Google Pay) dostane objednávající daňový doklad ihned; u převodu systém vystaví zálohovou fakturu a daňový doklad přijde po zaplacení.
- **Zobrazení ceny** — přepínač **Zobrazit hlavní cenu s DPH** určuje, zda se hlavní cena u vstupenky a ve shrnutí objednávky na microsite ukazuje s DPH, nebo bez.
- **Nastavení plateb bankovním převodem (zálohové faktury)** — **Doba splatnosti zálohové faktury** s volbami **3, 7, 14 nebo 30 dní od vystavení** (vlastní počet dní zadat nelze).
- **Měřící kódy** — pro nastavení GTM měřicích kódů kontaktujte zákaznickou podporu.

> Maximální datum splatnosti je vždy **nejpozději dva dny před začátkem události**. Pokud by zvolená splatnost vycházela později, automaticky se zkrátí. Pokud už do události zbývá méně než dva dny, splatnost se nastaví na den vystavení faktury.

### Předvýběr vstupenky z microsite

Vstupenky na microsite mají tlačítko **Koupit**. Tlačítko zavede účastníka do nákupního prostředí a do prázdného košíku rovnou přidá vstupenku, u které klikl; nic k tomu nenastavujete. U běžné vstupenky se přidá jeden kus. Při nákupu v balíčku se množství řídí nastaveným krokem balíčku, stejně jako při použití tlačítka plus.

Pokud už má účastník v košíku některou vstupenku, další kliknutí na **Koupit** jeho výběr nepřepíše ani nenavýší. Jinou vstupenku nebo množství upraví přímo v nákupním prostředí. Předvýběr neobchází dostupnost vstupenky ani období prodeje.

Po otevření nákupu se údaj o předvýběru odstraní z adresy. Obnovení stránky proto vstupenku znovu nepřidá. Nové kliknutí na **Koupit** po vyprázdnění košíku naopak předvýběr umožní. Když si tlačítko testujete a po kliknutí u jiné vstupenky se v košíku nic nezmění, není to chyba: košík z předchozího pokusu ještě není prázdný. Vyzkoušejte proto prázdný i již naplněný košík.

### Slevové kódy

V sekci **Slevové kódy** klikněte na **+ Nový slevový kód**. Nastavujete:

- **Typ slevy** — procento, nebo hodnota.
- **Výše slevy.**
- **Platnost kódu** — datum od–do.
- **Maximální počet použití** — pokud necháte neomezeně, kód platí bez limitu.
- **Omezit platnost vstupenky** — kód se může aplikovat na všechny vstupenky, nebo jen na vybrané.
- **Přiřadit skupinu po použití kódu** — účastník, který projde s kódem, se automaticky přidá do skupiny.

Kódy můžete sdílet s partnery, vybranými účastníky nebo v marketingových kampaních.

### Individuální a hromadné registrační odkazy

**Individuální registrační odkaz** — jednorázový odkaz, který umožňuje vstup zdarma pro jednoho konkrétního člověka. Účastník projde registračním formulářem, nemusí nic platit. Použití: guest list, redakční pozvánky, VIP hosté.

**Hromadný registrační odkaz** — totéž, ale jeden odkaz pro víc lidí. Při zakládání vyplníte název a **Počet použití** od 1 do 500; hromadný odkaz bez limitu založit nejde. Použití: partnerské pozvánky s limitem (partner má 6 pozvánek zdarma, dostane odkaz a sdílí ho, jak uzná za vhodné).

U obou typů odkazů lze nastavit **přiřazení do skupiny** po registraci.

Přehled všech odkazů stáhnete jako jeden soubor: na stránce **Placené vstupenky** otevřete vpravo nahoře **Exporty** a zvolte **Export registračních odkazů**. Soubor v Excelu má řádek za každý odkaz, nahoře individuální odkazy, pod nimi hromadné. U každého najdete e-mail adresáta (jen u individuálního odkazu), název, nastavený limit, kolikrát už byl odkaz použit, stav a celou adresu odkazu. Stav má čtyři hodnoty: **Nepoužit**, **Použito částečně**, **Vyčerpán** a **Použit**. *Vyčerpán* znamená hromadný odkaz s naplněným limitem, *Použit* individuální odkaz, přes který se už někdo zaregistroval.

Export se hodí pro reporting partnerům (kolik z jejich pozvánek zdarma se už využilo) a pro rozeslání odkazů vlastní cestou. Ukazuje ale jen počty: jména lidí, kteří přišli přes hromadný odkaz, ani skupinu, do které odkaz zařazuje, v něm nenajdete.

### Skupiny vstupenek

Skupiny vstupenek slouží k vytvoření sady vstupenek viditelných pouze pro určitý typ nákupu. Vytvoříte skupinu, přidáte do ní vybrané vstupenky a skupinu sdílíte přes **unikátní odkaz**. Účastník přes tento odkaz vidí pouze vstupenky ze skupiny, a to jen ty ve stavu **Publikováno** nebo **Neveřejné**. Vstupenku ve stavu **Nepublikováno** do skupiny přidat jde, přes odkaz skupiny se ale nenabídne. Pro vstupenky, které se mají prodávat jen přes skupinu, proto volte stav **Neveřejné**.

Použití: partnerské ceny, speciální nabídky, VIP balíčky s vlastní sestavou vstupenek.

### Hromadný import (Import)

Na záložce **Import** hromadně nahrajete data přes Excel šablonu. Import je dostupný pro **E-mailové odkazy** (individuální registrační odkazy), **Hromadné odkazy** a **Slevové kódy**. U každého typu si stáhnete šablonu (**Stáhnout šablonu**), vyplníte ji, nahrajete (**Nahrát vyplněnou šablonu**) a spustíte **Importovat**. Po importu uvidíte souhrn **Vytvořeno / Přeskočeno / Chyby** s popisem případných chyb po řádcích.

Šablony pracují se skupinami podle názvu. Pokud řádek odkazuje na skupinu, která ve workspace neexistuje, nenaimportuje se a skončí chybou. Skupiny si proto připravte předem.

### Statistiky vstupenek

Poslední záložka na stránce **Placené vstupenky** se jmenuje **Statistiky** (dostanete se na ni i tlačítkem **Statistiky** vpravo nahoře — vede na tutéž záložku). Jsou na ní dvě tabulky: **Statistiky vstupenek** a pod nimi **Měsíční přehled**.

Tabulka **Statistiky vstupenek** má řádek pro každou vstupenku a souhrnný řádek **Celkem**. Nad sloupci s částkami je uvedená měna události (například *CZK*). Každá částka je zobrazená **s DPH** a pod ní je v závorce tatáž částka **bez DPH**:

- **Prodané** (Počet / Částka) — všechny prodané vstupenky bez ohledu na to, zda už jsou zaplacené.
- **Zaplacené** (Počet / Částka) — objednávky s připsanou platbou.
- **Nezaplacené** (Počet / Částka) — vystavené, ale zatím neuhrazené. Typicky zálohové faktury čekající na převod.
- **Zdarma** (Počet) — vstupenky pořízené za nulovou cenu, typicky přes individuální a hromadné registrační odkazy.
- **Stornované** (Počet) — zrušené objednávky.
- **Registrovaní** (Počet / Částka) — kolik kupujících už dokončilo registraci. Má smysl jen u *registrace s doplněním informací*; rozdíl proti **Prodaným** ukazuje, kolik lidí zaplatilo a formulářem ještě neprošlo.

**Měsíční přehled** ukazuje tatáž čísla v rozpadu po měsících, se dvěma rozdíly: u **Stornovaných** přibývá **Vráceno** (kolik peněz z nich reálně odešlo zpět, tedy refundace) a **Registrovaní** mají jen **Počet**. Je to nejrychlejší pohled na to, kdy se co prodalo — vyhodnocení prodejních vln a dopadu jednotlivých kampaní.

Data vyexportujete tlačítkem **Exporty** vpravo nahoře — v Excelu po objednávkách nebo po vstupenkách. Třetí položka téže nabídky, **Export registračních odkazů**, stáhne přehled odkazů zdarma; popisuje ho část *Individuální a hromadné registrační odkazy* výše v tomto článku.

## Na co si dát pozor

### Placené vstupenky zapnuté, ale žádná vstupenka vytvořená. Registrace je uzavřena, účastníci se stěžují

Po zapnutí placených vstupenek okamžitě vytvořte alespoň jednu. Do té doby registrace nefunguje.

### Automatická registrace zvolena u placené události, přestože potřebujete doplňující data nebo rozšířené souhlasy

Automatická registrace u placených událostí **nevyužívá** registrační formulář ani rozšířené souhlasy. Volte *Registrace s doplněním informací*. Detail v článku *Výběr správného typu registrace*.

### Splatnost zálohové faktury nastavená na 14 dnů, ale událost je za 10 dnů. Účastník dostane fakturu se splatností za hranou termínu

Systém automaticky zkrátí splatnost tak, aby vycházela nejpozději 2 dny před začátkem události. Ověřte v nastavení, jak vysokou splatnost skutečně nastavíte u blízkých událostí.

### Vstupenka ve stavu *Neveřejné* — organizátor ji nevidí v nákupním prostředí a myslí si, že je rozbitá

Neveřejná vstupenka se v přehledu nákupu nezobrazuje záměrně. Přímý odkaz na ni získáte ikonou **Odkaz na vstupenku** v jejím řádku v seznamu vstupenek; přes tento odkaz — nebo zařazením do Skupiny vstupenek — ji lze koupit.

### Nepublikovaná vstupenka ve Skupině vstupenek. Partner otevře odkaz skupiny a vstupenku nevidí

Přes odkaz skupiny se nabízejí jen vstupenky ve stavu **Publikováno** nebo **Neveřejné**. Stav **Nepublikováno** vstupenku skryje všude, i když je ve skupině. Změňte stav na **Neveřejné**: v běžném přehledu vstupenek zůstane skrytá a přes odkaz skupiny ji půjde koupit.

### Po skončení události chcete vstupenky dál prodávat, ale z nabídky zmizely

Společný konec prodeje se týká všech událostí, i těch založených dřív, a výchozí volba je **Podle konce události**. Pokud má prodej po skončení události pokračovat, nastavte v části **Ukončení prodeje** volbu **Vlastní datum a čas** s pozdějším termínem. Zkontrolujte také, že prodej neukončuje dřívější **Konec prodeje** u samotné vstupenky.

### Volba *Neomezeně* u proběhlé události. Vstupenky na starý ročník jdou koupit dál

Volba **Neomezeně** vypne společný konec prodeje a vstupenka, která nemá vyplněný **Konec prodeje**, zůstane v nabídce i po skončení události. Kupující, který hledá aktuální ročník, pak může omylem koupit vstupenku na ten proběhlý. Volbu **Neomezeně** používejte, jen když má každá vstupenka zapnuté **Omezit období prodeje** a vyplněný **Konec prodeje**; jinak nechte **Podle konce události**.

### Slevový kód 100 % místo individuálního registračního odkazu. Účastník musí projít celým nákupním procesem, aby dostal vstupenku zdarma

Pokud jde jen o jednorázovou pozvánku zdarma, použijte **Individuální registrační odkaz** — účastník projde registrací bez nákupního procesu. Slevový kód 100 % má smysl pro marketingové kampaně, kde chcete evidovat, kolik lidí kód uplatnilo.

### Balíček vstupenek (krok 5) nastavený, ale organizátor očekává, že si účastník může koupit i jinou velikost. Zákazník se diví, proč nemůže koupit 3 vstupenky

Nastavení balíčku vynucuje **násobky** — krok 5 povoluje pouze 5, 10, 15 atd. Pokud chcete flexibilnější nabídku, vytvořte dvě vstupenky: základní *Standard* (bez balíčku) a *Standard — balíček po 5* (s balíčkem a slevou).

### *Přiřadit do skupiny* zapnuté až v průběhu prodeje. Dřívější kupující ve skupině chybí a cílená komunikace je mine

Přiřazení do skupiny u vstupenky se **nepropisuje zpětně**. Zapnete-li volbu ve chvíli, kdy už máte prodáno padesát vstupenek, skupinu dostanou jen ti, kdo se zaregistrují potom. Padesát dřívějších účastníků zůstane mimo, a pokud podle skupiny cílíte kampaň, viditelnost obsahu nebo zobrazení při skenování, tihle lidé z cílení vypadnou.

Pozor na to, že u přiřazování skupin na sessions to funguje opačně: tam se zapnutí i vypnutí promítne i na účastníky, kteří už jsou registrovaní. Zkušenost z jednoho místa produktu se sem tedy přenést nedá.

Když se to stane, doplňte členství ručně: buď po jednom v **bočním panelu Upravit kontakt** na záložce *Skupiny*, nebo u větších počtů znovu naimportujte tytéž kontakty s volbou **Doplnit skupiny u všech**, která existujícím kontaktům skupiny přidá a nic nepřepíše. Obojí popisuje článek [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace). Spolehlivější je ale skupinu i její přiřazení nastavit **před spuštěním prodeje**.

### Hromadný import skončí chybou, protože skupina ve workspace ještě neexistuje

Šablony importu (E-mailové odkazy, Hromadné odkazy, Slevové kódy) odkazují na skupiny podle názvu. Pokud skupina neexistuje, řádek se nenaimportuje a skončí chybou (například *Unknown group: VIP*). Skupiny vytvořte před importem a názvy v šabloně s nimi sjednoťte.

### Snaha nabídnout ke vstupence doplněk — tričko, oběd, workshop — jako další položku v košíku

Nákupní proces není modulární, účastník si objednávku neskládá z víc položek. Každá další položka je samostatná vstupenka, a protože e-mail účastníka lze v objednávce použít jen jednou, druhá položka na tutéž osobu neprojde.

Řešením je samostatná vstupenka pro každou kombinaci: *Vstup na konferenci*, *Vstup na konferenci + workshop*, *Vstup na konferenci + tričko*. Účastník si vybere jednu a má v ceně všechno. Rozlišení pro vás i pro odbavení na místě zajistíte přes **Přiřadit do skupiny** u každé varianty.

Nezaměňujte s přepínačem **Nákup vstupenky v balíčku** — ten řídí minimální odběr v násobcích (5, 10, 15 kusů téže vstupenky), ne obsah vstupenky.

### Objednávající i účastník dostanou odkaz na dokončení registrace a vyplní ho oba

Když firma kupuje víc vstupenek, dostane objednávající odkazy na registraci všech účastníků a každý účastník zároveň dostane svůj vlastní. Registraci tak může dokončit kterýkoli z nich. Kdo na odkaz klikne jako druhý, uvidí, že účastník už je zaregistrovaný. Pokud vám záleží na tom, kdo údaje vyplní, napište to do doprovodné komunikace — systém to neřídí.

## Související články

- [Výběr správného typu registrace](https://help.happenee.com/cs/articles/4-vyber-spravneho-typu-registrace)
- [Nastavení typu registrace a doplňujících otázek](https://help.happenee.com/cs/articles/12-nastaveni-typu-registrace-a-doplnujicich-otazek)
- [Správa objednávek a faktur](https://help.happenee.com/cs/articles/19-sprava-objednavek-a-faktur)
- [Nastavení registračního formuláře](https://help.happenee.com/cs/articles/13-nastaveni-registracniho-formulare)
- [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti)
- [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace)
- [Jak fungují nominace a nominátoři](https://help.happenee.com/cs/articles/17-jak-funguji-nominace-a-nominatori)
- [Nastavení Seatingu](https://help.happenee.com/cs/articles/20-nastaveni-seatingu)
- [Osobní a veřejný odkaz: jaký je rozdíl](https://help.happenee.com/cs/articles/44-osobni-a-verejny-odkaz-jaky-je-rozdil)
- [Práce s objednávkami a exporty](https://help.happenee.com/cs/articles/52-prace-s-objednavkami-a-exporty)
- [Jak funguje check-in a skenování QR kódů](https://help.happenee.com/cs/articles/47-jak-funguje-check-in-a-skenovani-qr-kodu)
- [Doporučený setup pro konferenci](https://help.happenee.com/cs/articles/55-doporuceny-setup-pro-konferenci)
- [Doporučený setup pro expo / veletrh](https://help.happenee.com/cs/articles/56-doporuceny-setup-pro-expo-veletrh)
- [Co dělat, když účastník ztratí registrační odkaz](https://help.happenee.com/cs/articles/59-co-delat-kdyz-ucastnik-ztrati-registracni-odkaz)
- [Oprava chybné faktury](https://help.happenee.com/cs/articles/60-oprava-chybne-faktury)
- [Interpretace statistik vstupenek](https://help.happenee.com/cs/articles/84-interpretace-statistik-vstupenek)
- [Jak poznat, že byl zvolen špatný typ registrace](https://help.happenee.com/cs/articles/92-jak-poznat-ze-byl-zvolen-spatny-typ-registrace)

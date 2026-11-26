# Jak funguje microsite události

> Microsite je veřejná stránka události, na kterou vedou všechny odkazy z e-mailů.

- Článek v Help Centru: https://help.happenee.com/cs/articles/21-jak-funguje-microsite-udalosti
- English version: https://help.happenee.com/en/articles/21-how-the-event-microsite-works
- Kolekce: Obsah a zkušenost účastníka
- Aktualizováno: 2026-11-04

---

> [!info] Krátce
> Microsite události je **veřejná webová stránka události**, na kterou vedou všechny odkazy z e-mailů a kampaní; je to vstupní bod k registraci a k výkladu, o co na události jde. Vzniká automaticky při vytvoření události a obsah se plní z **obsahových funkcí** (Program, Řečníci, Lokalita, Kontakt, Vlastní obsah, Sponzoři, Vystavovatelé); u každé rozhodujete, jestli se na microsite zobrazí a v jakém pořadí. U placené události v téže tabulce určujete i místo, kde bude nabídka vstupenek. Adresa microsite má tvar `https://www.happenee.com/events/<slug>` a její koncovou část (slug) můžete změnit v **Microsite události → Nastavení** — dřív sdílené odkazy včetně těch v rozeslaných pozvánkách ale po změně přestanou fungovat. Workspace s white label nastavením má microsite na vlastní doméně. Pokud má microsite vlastní obrázek hlavičky, můžete v **Microsite události → Nastavení** zapnout, aby se pod ním zobrazil i název události, termín, místo a tlačítko pro přidání události do kalendáře.

## Jak začít

- Rozhodněte, **jak podrobnou microsite chcete** — jednoduchá vizitka (kdy, kde, kontakt), nebo plnohodnotná stránka s programem, řečníky, partnery a FAQ.
- Microsite se plní **obsahovými funkcemi**, které zapínáte v **Obsahu**. Bez obsahu bude microsite prázdná.
- Úvodní obrázek, text a pozici registračního tlačítka nastavíte v **Microsite události** v levém menu.
- Zkontrolujte **adresu microsite** dřív, než ji poprvé sdílíte. Výchozí slug vzniká z čísla události a jejího názvu (např. `4690_event-ops-summit-2026`); změnit ho jde kdykoli, ale staré odkazy pak přestanou platit.
- Pokud budete sdílet odkaz veřejně, kontrolujte *Omezení registrace* v Nastavení události — kdo všechno se smí přihlásit (viz článek o typu registrace).

## Detail

### Kde microsite nastavujete

V administraci události v levém menu klikněte na **Microsite události**. Na úvodu nastavujete:

- **Úvodní text** — rich text editor; zobrazuje se pod hlavičkou microsite.
- **Pozice registračního tlačítka** — nahoře, uprostřed, dole nebo automaticky.
- **Text na obrazovce po vyplnění a odeslání registračního formuláře** — děkovná stránka. Podporuje zástupné proměnné (jméno účastníka, název události).

### Záložky a obsahové funkce

Pod úvodem je tabulka **záložek** microsite. Běžné záložky odpovídají **obsahovým funkcím**, které jste přidali v sekci **Obsah**. Když má událost zapnuté **Placené vstupenky**, je v tabulce navíc řádek **Vstupenky** (viz *Pořadí vstupenek* níže). Typické obsahové záložky:

- **Program** (obsahová funkce)
- **Řečníci** (obsahová funkce)
- **Lokalita** (obsahová funkce)
- **Kontakt** (obsahová funkce)
- **Vlastní obsah** (obsahová funkce, FAQ, mapa, informační blok)
- **Sponzoři** (obsahová funkce)
- **Vystavovatelé** (obsahová funkce)

Tabulka má sloupce **Název**, **Typ** a **Publikace na microsite**. U běžných obsahových záložek volíte:

- **Publikace na microsite** — přepínač v pravém sloupci. Vypnutá záložka na microsite není, obsah v administraci zůstává.
- **Pořadí** — přetažením za úchyt se šesti tečkami vlevo od názvu.
- **Zobrazení** — tlačítko uprostřed řádku. **Není u všech záložek**; mají ho typy **Sessions** a **Řečníci**, u vlastního obsahu chybí. Otevře dialog s variantami, jak se obsah vypíše na hlavní stránce.

### Pořadí vstupenek

Když má událost zapnuté **Placené vstupenky**, je v tabulce záložek řádek **Vstupenky**. Určuje, kde na hlavní stránce microsite bude nabídka vstupenek. Řádek přidá Happenee samo, jakmile placené vstupenky zapnete. Pokud je událost měla zapnuté už dřív, přibude řádek při prvním otevření **Microsite události** (stránka se přitom jednou sama obnoví). Na začátku stojí na prvním místě, takže microsite vypadá stejně jako dosud a vstupenky jsou nad ostatním obsahem.

Pokud má účastník nejdřív vidět třeba program nebo řečníky, přetáhněte řádek **Vstupenky** za úchyt vlevo od názvu na požadované místo. Nabídka vstupenek se na hlavní stránce přesune mezi ostatní obsah a odkaz **Vstupenky** v menu microsite se posune na stejné místo. Výsledek zkontrolujte na veřejné microsite.

Řádek slouží jen k řazení. Nemá přepínač **Publikace na microsite** ani tlačítko **Zobrazení**. Přesunem tedy nabídku vstupenek nezapnete ani neskryjete; jestli ji účastník uvidí, řídí nastavení placených vstupenek.

Když **Placené vstupenky** vypnete, řádek z tabulky zmizí. Po jejich opětovném zapnutí se vrátí na místo, kam jste ho naposledy přesunuli. Znovu ho přidávat ani zakládat další obsahovou funkci nemusíte.

### Zobrazení řečníků na hlavní stránce

U záložky **Řečníci** otevře tlačítko **Zobrazení** dialog **Zobrazení řečníků** se dvěma volbami:

- **Náhled prvních 3 řádků řečníků** — na hlavní stránce se vypíše jen začátek seznamu a pod ním tlačítko na podstránku se všemi řečníky.
- **Výpis všech řečníků** — na hlavní stránce je celý seznam; jednotlivé karty jsou prokliknutelné na detail řečníka.

Volbu potvrdíte tlačítkem **Uložit**.

Rozhodujte podle toho, **kolik řečníků máte a jak moc na nich stavíte program**. U konference s třiceti jmény zabere výpis všech na hlavní stránce tolik místa, že program a registrace spadnou pod ohyb — tam volte náhled. U události se čtyřmi keynote řečníky je naopak proklik na podstránku krok navíc a lidi na ni nedojdou; tam dává smysl výpis všech.

Pozor na slovo **řádky**: kolik řečníků se na řádek vejde, závisí na šířce obrazovky a na úrovni zobrazení, takže „řádky" a „řečníci" nejsou totéž. Kolik jich náhled reálně ukáže, si po nastavení otevřete tlačítkem **Microsite** vpravo nahoře.

Podobu výpisu řečníků tedy **neřídí nastavení konkrétního řečníka**, ale tahle volba u záložky. Detail profilů je v článku [Správa řečníků](https://help.happenee.com/cs/articles/23-sprava-recniku).

### Zobrazení programu na hlavní stránce

U záložky typu **Sessions** otevře tlačítko **Zobrazení** dialog **Zobrazení programu**. Má tři části.

**Na hlavní stránce microsite** — volba mezi dvěma variantami:

- **Náhled prvních 6 sessions s proklikem na celý program** — na hlavní stránce je nejvýš šest sessions vybraného dne a pod nimi tlačítko na podstránku s celým programem.
- **Výpis všech sessions** — celý program je rovnou na hlavní stránce.

**Quick filtry na hlavní stránce** — rozbalovací pole pod volbou zobrazení. Rozhoduje, jestli se u programu na hlavní stránce objeví řada filtračních tlačítek, kterými účastník jedním klikem přepne výpis — typicky na konkrétní sál. Nabídku skládá Happenee podle nastavení programu: kromě volby **Nezobrazovat** (výchozí stav, žádná tlačítka) jsou v ní jen filtry, které mají v *Obsah → (program) → Nastavení* zapnutý přepínač **Zobrazit filtr** — pod názvy, které jste jim tam dali, a ve stejném pořadí. Filtr bez vlastního názvu se v nabídce objeví pod výchozím označením svého typu (*Typ*, *Místo*, *Štítky*). Když nemá *Zobrazit filtr* zapnutý žádný filtr, zbude v nabídce jediná volba — *Nezobrazovat*. Podrobnosti níže v části *Quick filtry u programu*.

**Zobrazení session** — čtyři přepínače, které řídí, kolik se u každé session ukáže:

- **Zobrazit popis session v celé délce** — bez zaškrtnutí se popis zkrátí; **standardně se zobrazí maximálně 400 znaků**.
- **Proklik na detail session** — název session se stane odkazem na její detailovou stránku.
- **Zobrazit řečníky** — u session se vypíšou přiřazení řečníci.
- **Proklik na profil řečníka** — jméno řečníka u session se stane odkazem na jeho profil.

Poslední dva přepínače jsou provázané: bez zaškrtnutého *Zobrazit řečníky* se **Proklik na profil řečníka** sám odškrtne a zešedne, takže ho nejde zapnout samostatně. Odkaz na profil totiž nemá na co navázat, když se řečníci u session nevypisují.

Volbu potvrdíte tlačítkem **Uložit**.

Tady se vyplatí přemýšlet o **délce stránky**. Program s třiceti sessions, u každé plný popis, řečníci a jejich profily, udělá z hlavní stránky několikametrový sloupec, ve kterém účastník přestane hledat. Kombinace, která funguje skoro vždy: **náhled prvních 6 sessions** plus **proklik na detail** a **zobrazení řečníků** — na hlavní stránce je vidět, o čem událost je, a kdo chce víc, proklikne se.

Těch **400 znaků** je dobré držet v hlavě už při psaní programu: pokud popisy sessions píšete delší a checkbox nezapnete, uvidí účastník na hlavní stránce jen jejich začátek. Detail psaní popisů je v článku [Správa sessions](https://help.happenee.com/cs/articles/69-sprava-sessions).

### Quick filtry u programu

Když v dialogu *Zobrazení programu* vyberete typ filtru, objeví se u programu na hlavní stránce **řada tlačítek s hodnotami toho filtru** — u *Místa* například *Main Stage*, *Stage B*, *Workshop Room 1*. Účastník tak vidí členění programu hned po otevření microsite a nemusí kvůli němu přecházet na podstránku s celým programem.

Jak se tlačítka chovají:

- **Výchozí stav je bez filtru** — účastník vidí celý program v časovém pořadí.
- **Klik zúží výpis** na jednu hodnotu. Aktivní může být vždy **jen jedna** — klik na jiné tlačítko přepne, klik na totéž tlačítko filtr zruší a vrátí celý program. Tlačítko *Vše* v řadě není.
- **Řada se drží vybraného dne.** U vícedenní události, kde jsou nad programem záložky dnů, nabízí jen hodnoty, které na ten den skutečně připadají — sál, kde se v daný den nic nekoná, v ní není. Přepnutí dne zároveň zruší vybraný filtr.
- **Fungují v obou variantách zobrazení.** U *Náhledu* se filtr vztáhne na celý vybraný den a z odpovídajících sessions se vypíše nejvýš šest — účastník tak najde i session, která by se do nefiltrované šestice nevešla; tlačítko na celý program zůstává. U *Výpisu všech sessions* filtrují celý výpis.
- **Nastavení je samostatné pro každou záložku typu Sessions.** Microsite se dvěma programy může mít quick filtry u jednoho zapnuté a u druhého ne.
- U štítků tlačítka přebírají **barvu štítku**, takže řada vypadá stejně jako štítky na kartách sessions.

**Nabídku i uložený výběr hlídá nastavení programu.** Jestli se filtr vůbec dostane do nabídky, rozhoduje přepínač **Zobrazit filtr** u daného filtru v *Obsah → (program) → Nastavení*. Když ho vypnete u filtru, který je zrovna vybraný jako quick filtr, vrátí Happenee volbu rovnou na *Nezobrazovat* — neuloží se stav, ve kterém je vybraný filtr, který se na hlavní stránce nemá jak projevit. Odebrání jedné hodnoty (jednoho sálu, jednoho štítku) je něco jiného: volba zůstane a řada tlačítek jen přijde o tuhle hodnotu. Souvislosti filtrů popisuje [Jak fungují registrační bloky, místa a štítky](https://help.happenee.com/cs/articles/31-jak-funguji-registracni-bloky-mista-a-stitky).

Quick filtry mají smysl tam, kde program běží ve více paralelních stopách — více sálů, více tematických tracků. Účastník hned na hlavní stránce vidí, kolik stop událost má, a přepne se do jedné kliknutím. U jednodenního programu v jednom sále nechte **Nezobrazovat**: řada s jediným tlačítkem nikomu nepomůže a jen přidá prvek nad program.

### Hlavní stránka microsite události

**Hlavní stránka microsite události** je první obrazovka, kterou účastník vidí po otevření odkazu. Kromě záložek obsahuje:

- Úvodní obrázek (centrální obrázek celé události).
- Úvodní text.
- **Registrační tlačítko** (nebo tlačítko nákupu vstupenek u placené události).
- **Nabídka vstupenek** u placené události, na místě, které určuje řádek **Vstupenky** v tabulce záložek.
- Náhled vybraných obsahových funkcí, pokud jsou v **Zobrazení** nastavené na náhled či výpis (např. kategorie sponzorů, první sessions z programu, výchozí vystavovatelé).

### Úvodní obrázek a grafika

Úvodní obrázek microsite je společný napříč microsite, zvacím e-mailem, potvrzovacím e-mailem a účastnickou aplikací. Nastavuje se v **Nastavení události → Nastavení grafiky** (ne přímo v Microsite události). Máte dvě volby:

- **Ikona události s názvem a datem** — generovaný obrázek.
- **Obrázek hlavičky** — vlastní nahraný obrázek v doporučených rozměrech.

Vedle úvodního obrázku je v **Nastavení grafiky** volitelné pole **Nastavení hlavičky pro účastnickou aplikaci**. Obrázek z něj se zobrazí jen v účastnické aplikaci, mobilní i webové; microsite ani e-maily ho nepoužívají. Když ho nenahrajete, aplikace převezme obrázek z volby **Obrázek hlavičky**, tedy stejnou hlavičku jako e-maily a microsite. Když nemáte nahraný ani ten, použije se všude ikona události s názvem a datem.

### Informace pod vlastním obrázkem

V **Microsite události → Nastavení** v části s úvodním obrázkem, hned pod odkazem **Nastavení události**, můžete zapnout přepínač **Zobrazit informace o události pod obrázkem**. Pod vlastním obrázkem hlavičky pak návštěvník uvidí název události, termín, místo (pokud je vyplněné) a tlačítko pro přidání události do kalendáře (Outlook, Google nebo iCal). Hodí se to, když chcete ponechat vlastní banner a zároveň mít termín a místo na stránce jako text, který si návštěvník přečte i bez zvětšování obrázku.

Přepínač je **ve výchozím stavu vypnutý** a změna se uloží hned po přepnutí; výsledek zkontrolujte obnovením veřejné microsite. Mění jen zobrazení microsite: obrázek ani obsah e-mailů zůstávají stejné. Přepínač jde zapnout, až když má microsite nastavený vlastní úvodní obrázek. Do té doby je neaktivní a pod ním uvidíte upozornění, že je potřeba obrázek nejdřív nastavit; informace o události se v hlavičce bez vlastního obrázku zobrazují jako dosud. U hlavičky upravené na zakázku pro konkrétního zákazníka se přepínač neprojeví.

### Adresa microsite a její změna

Microsite má adresu ve tvaru `https://www.happenee.com/events/<slug>`. Slug je koncová část adresy; Happenee ho vytvoří při založení události z **čísla události a jejího názvu**, například `4690_event-ops-summit-2026`. Pozdější přejmenování události slug nemění. Tentýž slug je součástí všech registračních odkazů: osobní i veřejný odkaz ve zvacím e-mailu, odkazy v kampaních a odkaz pro doplnění registrace u placených vstupenek vedou přes něj.

Adresu vidíte a měníte v **Microsite události → Nastavení**, v sekci s veřejným odkazem. Pevná část `https://www.happenee.com/events/` se změnit nedá. Slug ano: klikněte na něj, v dialogu **Opravdu chcete změnit URL adresu microsite?** potvrďte tlačítkem **Změnit odkaz** (nebo couvněte přes **Ponechat původní**) a zapište nový tvar. Vedle adresy je tlačítko, které celý odkaz zkopíruje do schránky — použijte ho po každé změně, ať sdílíte přesně to, co je uložené.

Co se s novým slugem stane:

- **Happenee ho upraví do bezpečného tvaru.** Malá písmena, bez diakritiky, mezery nahradí pomlčkou; zůstanou jen písmena a–z, číslice, pomlčka a podtržítko, ostatní znaky se vypustí. Z „Konference Jaro 2027“ vznikne `konference-jaro-2027`.
- **Musí být jedinečný v celém Happenee**, ne jen ve vašem workspace. Pokud ho už používá jiná událost, Happenee přidá příponu `_1`, `_2`… a uloží tuto upravenou podobu bez upozornění. Uloženou adresu proto po změně zkontrolujte.
- **Stará adresa přestane fungovat okamžitě.** Přesměrování neexistuje: kdo klikne na dřív sdílený odkaz (v už odeslaném zvacím e-mailu, v kampani, na sociálních sítích nebo na vašem webu), se na microsite nedostane.

Slug proto měňte dřív, než odkaz poprvé rozešlete: u čerstvě založené události, které chcete dát čitelnou adresu na pozvánku nebo tištěné materiály, a u kopie události, pokud jste v průvodci kopírováním ponechali předvyplněný název: slug pak obsahuje slovo *kopie* a datum kopírování. Po rozeslání pozvánek znamená změna adresy nové rozeslání všeho, co odkaz obsahovalo.

### White label: microsite na vlastní doméně

Pokud má váš workspace **white label** nastavení (vlastní doména, logo, účastnická aplikace pod vlastním jménem), microsite neběží na `www.happenee.com`, ale na vaší doméně. Tvar adresy zůstává stejný, jen s jinou doménou: `https://<vaše doména>/events/<slug>`, a pro slug platí stejná pravidla včetně jedinečnosti napříč celým Happenee. Doménu si v administraci nenastavíte — white label zajišťuje **zákaznická podpora** a počítejte s přípravou v řádu týdnů. Jak white label ovlivňuje e-maily a účastnickou aplikaci, popisuje [Cesta účastníka z microsite do účastnické aplikace](https://help.happenee.com/cs/articles/45-cesta-ucastnika-z-microsite-do-ucastnicke-aplikace).

### Sdílení a veřejnost

**Veřejný odkaz** na microsite najdete tamtéž, v **Microsite události → Nastavení**. Odkaz lze sdílet e-mailem, na sociálních sítích, na vlastním webu, ve zvacím e-mailu nebo e-mailových kampaních.

- Kdo přijde z veřejně sdíleného odkazu, je ve statistikách veden jako registrovaný z **otevřené registrace**.
- U *invitation only* událostí používejte místo veřejného odkazu **zvací e-mail** nebo **e-mailovou kampaň** — tam dostane účastník personalizovaný odkaz s předvyplněnými údaji.

### Viditelnost pro skupiny

U každé obsahové funkce (ne u microsite jako celku) můžete nastavit, aby byla viditelná pouze **vybraným skupinám účastníků**. Kontrola ale proběhne až **po registraci a přihlášení do účastnické aplikace** — microsite sama je vždy veřejně přístupná všem, kdo mají odkaz.

### Patička a měřicí kódy

- **Patička microsite** — buď výchozí text platformy Happenee, nebo vlastní text (volba v **Microsite události → Nastavení**).
- **GTM měřicí kódy** (Google Tag Manager) — pro jejich nastavení kontaktujte **zákaznickou podporu**. V samoobsluze se neřeší.

### Změny v průběhu

Obsah microsite lze kdykoli měnit — publikace je okamžitá. Pokud účastníci mají microsite otevřenou v prohlížeči, změnu uvidí po obnovení stránky.

## Na co si dát pozor

### Organizátor sdílí odkaz na microsite, ale ještě nemá naplněný obsah. Účastníci vidí prázdnou stránku s názvem a datem

Základní obsahové funkce (alespoň Lokalita a Kontakt) vyplňte **před** sdílením odkazu. Ideálně i Program a úvodní text.

### Úvodní obrázek v nízkém rozlišení nebo špatném poměru — na microsite působí rozmazaně

Respektujte doporučené rozměry obrázku v **Nastavení grafiky**. Microsite zobrazuje na počítači i na telefonu stejný úvodní obrázek; obrázek v poli **Nastavení hlavičky pro účastnickou aplikaci** se na microsite neprojeví.

### V dialogu *Zobrazení programu* je najednou *Nezobrazovat*, ačkoli quick filtry byly nastavené

Někdo mezitím vypnul přepínač **Zobrazit filtr** u filtru, podle kterého byly quick filtry nastavené. Happenee volbu vrátí na *Nezobrazovat* samo a bez upozornění, aby na hlavní stránce nezůstal výběr, který se nemá jak vykreslit. Zapněte *Zobrazit filtr* zpátky v *Obsah → (program) → Nastavení* a quick filtry v dialogu vyberte znovu.

### Organizátor čeká, že quick filtry rozdělí program do sekcí po sálech

Nerozdělí. Výchozí zobrazení zůstává celý program v časovém pořadí a sál si účastník zvolí kliknutím na tlačítko. Pokud potřebujete program opravdu členěný po sálech už při příchodu na stránku, quick filtry to neřeší.

### Quick filtry jsou zapnuté u jednoho programu a u druhého ne — vypadá to jako chyba

Nastavení patří k záložce, ne k události. Každá záložka typu **Sessions** má vlastní dialog *Zobrazení programu* a vlastní volbu quick filtrů. Projděte záložky jednu po druhé.

### Vstupenky jsou na microsite pořád nahoře, i když má být první program

Nabídka vstupenek stojí na prvním místě, dokud ji nepřesunete. V **Microsite události** přetáhněte v tabulce záložek řádek **Vstupenky** pod záložky, které mají být výš. Pokud řádek v tabulce nevidíte, nemá událost zapnuté **Placené vstupenky**.

### Všechny záložky mají v Zobrazení nastavený plný výpis — hlavní stránka je přetížená a účastník se v ní ztrácí

Když u každé záložky zvolíte výpis všeho, hlavní stránka naroste do několika obrazovek a registrační tlačítko spadne hluboko pod ohyb. Plný výpis nechte u **2–4 nejdůležitějších záložek** (typicky Program, Řečníci, Sponzoři), u zbytku volte náhled s proklikem na podstránku.

### Veřejný odkaz sdílen bez omezení registrace. Registrují se lidé z ulice, událost je „invitation only“

V **Nastavení události → Omezení registrace** zvolte *Pouze pro přiřazené kontakty*. Odkaz sice zůstane veřejný, ale registrovat se smí jen kontakty, které máte ve správě.

### Organizátor změní adresu microsite po rozeslání pozvánek. Účastníci klikají na odkaz v e-mailu a na microsite se nedostanou

Stará adresa po změně slugu nepřesměrovává a platí to i pro osobní registrační odkazy ve zvacím e-mailu a v kampaních. Buď slug vraťte na původní tvar (po změně je zase volný), nebo rozešlete pozvánky znovu a opravte odkaz všude, kde jste ho sdíleli — na webu, na sociálních sítích, v tištěných materiálech.

### Uložený slug vypadá jinak, než organizátor zapsal — má příponu `_1`, chybí diakritika nebo mezery

Happenee slug upravuje do bezpečného tvaru a při shodě s jinou událostí kdekoli v Happenee přidá číselnou příponu, obojí bez upozornění. Zvolte konkrétnější tvar (s rokem nebo zkratkou firmy) a uloženou adresu po každé změně zkontrolujte — zkopírujte ji tlačítkem vedle adresy nebo otevřete microsite tlačítkem **Microsite** vpravo nahoře.

### Text microsite vyplněný jen v jednom jazyce, zahraniční účastník vidí jen prázdno nebo český obsah

Přepněte vlajku jazyka v pravém horním rohu a vyplňte úvodní text ve všech jazycích, které událost podporuje. Pokud jazyk nevyplníte, použije se primární jazyk (viz *Nastavení primárního jazyka události*).

### Účastník registrovaný z veřejného odkazu se nezobrazuje v seznamu pozvaných — organizátor si myslí, že něco nefunguje

Účastníci, kteří přišli z veřejně sdíleného odkazu, jsou ve statistikách vedení jako registrovaní z otevřené registrace. Zkontrolujte je ve **Statistikách s účastníky**. Pro plnou kontrolu nad pozváními použijte **zvací e-mail** místo veřejného odkazu.

## Související články

- [Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka](https://help.happenee.com/cs/articles/5-microsite-vs-ucastnicka-aplikace-jak-premyslet-nad-flow-ucastnika)
- [Nastavení lokality a místa konání](https://help.happenee.com/cs/articles/22-nastaveni-lokality-a-mista-konani)
- [Správa řečníků](https://help.happenee.com/cs/articles/23-sprava-recniku)
- [Kopírování události](https://help.happenee.com/cs/articles/70-kopirovani-udalosti)
- [Přidání kontaktní osoby organizátora](https://help.happenee.com/cs/articles/24-pridani-kontaktni-osoby-organizatora)
- [Použití vlastního obsahu (FAQ, mapa, informační bloky)](https://help.happenee.com/cs/articles/25-pouziti-vlastniho-obsahu-faq-mapa-informacni-bloky)
- [Správa sponzorů](https://help.happenee.com/cs/articles/32-sprava-sponzoru)
- [Správa vystavovatelů](https://help.happenee.com/cs/articles/33-sprava-vystavovatelu)
- [Sestavení programu události — architektura](https://help.happenee.com/cs/articles/26-sestaveni-programu-udalosti-%E2%80%94-architektura)
- [Jak funguje účastnická aplikace a její hlavní stránka](https://help.happenee.com/cs/articles/34-jak-funguje-ucastnicka-aplikace-a-jeji-hlavni-stranka)
- [Osobní a veřejný odkaz: jaký je rozdíl](https://help.happenee.com/cs/articles/44-osobni-a-verejny-odkaz-jaky-je-rozdil)
- [Cesta účastníka z microsite do účastnické aplikace](https://help.happenee.com/cs/articles/45-cesta-ucastnika-z-microsite-do-ucastnicke-aplikace)

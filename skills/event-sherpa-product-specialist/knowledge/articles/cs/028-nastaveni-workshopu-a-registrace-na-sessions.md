# Nastavení workshopů a registrace na sessions

> Workshop je session s povinnou registrací, kapacitou, časovým oknem registrace a termínem odhlášení; registrace probíhá v účastnické aplikaci.

- Článek v Help Centru: https://help.happenee.com/cs/articles/28-nastaveni-workshopu-a-registrace-na-sessions
- English version: https://help.happenee.com/en/articles/28-setting-up-workshops-and-session-registration
- Kolekce: Obsah a zkušenost účastníka
- Aktualizováno: 2026-09-16

---

> [!info] Krátce
> Workshop je typ session, který **vyžaduje registraci účastníka**. Každý workshop má vlastní kapacitu a volitelně časové okno registrace, termín odhlášení a omezení na vybrané skupiny. Registrace probíhá **v účastnické aplikaci**. Tento článek popisuje nastavení registračních pravidel; sdružování workshopů do balíků (účastník si vybere 1 ze 3) je v článku *Jak fungují registrační bloky, místa a štítky*.

## Jak začít

- Rozhodněte, zda se má účastník **přihlašovat na jednotlivé workshopy samostatně**, nebo si zvolit **jeden workshop z nabídky** (registrační blok).
- Plánujte **kapacity** podle prostoru a obsahu workshopu. Systém kapacitu hlídá automaticky.
- Pokud chcete **cílit komunikaci** na lidi registrované na workshop, nastavte **Přiřadit do skupiny po registraci**.
- Má-li se registrace na workshopy otevřít jindy než registrace na událost, nastavte **Časové omezení registrace**. Session kvůli tomu nemusíte držet skrytou a v den spuštění publikovat.
- Chystáte-li se workshop omezit na skupiny, rozhodněte **nejdřív viditelnost, teprve pak registraci**.

## Detail

### Kde se registrace nastavuje

Registrační pravidla workshopu se nastavují na **dvou úrovních**:

- **Na úrovni typu session** — výchozí hodnoty pro všechny sessions daného typu. Nastavíte jednou, všechny workshopy je dědí.
- **Na úrovni konkrétní session** — individuální přepsání výchozího nastavení.

U obou úrovní máte stejná pole registračního nastavení.

### Registrační nastavení workshopu

**Přiřadit účastníka do skupiny po registraci.**
Po registraci na workshop systém účastníka automaticky přidá do vybrané skupiny. Skupinu musíte předem vytvořit v **Kontaktech a skupinách**. Přiřazení funguje i tehdy, když účastníka na session přihlásí ručně organizátor — chová se stejně jako registrace v aplikaci.

Přiřazení je **obousměrné a průběžné**. Když účastník ze session odejde — zruší si registraci nebo ho odebere organizátor — skupina se mu zase odebere. Když přiřazování na session nebo na jejím typu **zapnete nebo vypnete**, propíše se to i na účastníky, kteří už jsou registrovaní: zapnutím se skupina doplní, vypnutím odebere. Na úrovni typu to platí pro všechny sessions daného typu naráz.

Použití: cílení komunikace jen na účastníky konkrétního workshopu (personalizovaný e-mail, push notifikace, speciální obsah v aplikaci viditelný jen této skupině).

**Registrace pouze pro vybrané skupiny.**
Registrace na workshop je omezená jen na účastníky v určených skupinách. Ostatní workshop vidí (pokud není i viditelnost omezená), ale nemohou se na něj přihlásit.

Skupiny, které tady vyberete, jsou vždy **podmnožinou toho, kdo workshop vidí**. Když je viditelnost nastavená na *Pouze pro vybrané skupiny*, nabídne výběr u registrace **jen skupiny, pro které je session viditelná** — jinou vybrat nelze. Vychází to z logiky funkce: skupina, která workshop v programu nevidí, by se na něj stejně nepřihlásila. Při viditelnosti *Veřejné* vybíráte z celého seznamu skupin.

Použití: VIP workshopy pro platící účastníky, uzavřené workshopy pro konkrétní firemní tým.

**Omezit počet registrací.**
Maximální počet účastníků workshopu. Po naplnění se workshop v aplikaci označí jako *Plně obsazen* a další registrace jsou blokovány.

**Zobrazit počet dostupných míst.**
Pokud je kapacita omezená, můžete účastníkům v aplikaci ukázat zbývající kapacitu. Transparentní pro účastníka, ale může vyvolat tlak („rychle, už tam je jen pár míst“).

**Časové omezení registrace.**
Určuje, od kdy a do kdy se lze na workshop přihlásit. Po zapnutí volíte jeden ze dvou režimů:

- **Dle začátku session** — obě hranice se počítají zpětně od začátku workshopu. Vybíráte z pevné nabídky odstupů (*15 min*, *30 min*, *1 h*, *3 h*, *1 day*, *2 days*, *7 days*; delší jsou zatím anglicky), nebo zvolíte **Neomezeně**.
- **Konkrétní datum** — u každé hranice zadáte datum a čas, nebo ji přepínačem **Neomezeně** vypnete.

Režim *Konkrétní datum* pokrývá nejčastější zadání: prodej vstupenek běží od června, registrace na workshopy se má otevřít 1. srpna. Do pole **Možnost registrace od** zadáte 1. 8. a čas, u pole **Možnost registrace do** necháte zapnutý přepínač **Neomezeně**. Workshop je přitom celou dobu publikovaný a účastníci ho v programu vidí; jen se na něj do prvního srpna nepřihlásí.

Časy se řídí časovým pásmem události. Obě hranice jsou včetně — v okamžiku otevření i v okamžiku uzavření registrace ještě projde.

**Odhlášení ze session.**
Určuje, do kdy si účastník může svou registraci zrušit sám. Stejné dva režimy: **Dle začátku session** s týmiž odstupy (tady bez volby *Neomezeně*), nebo **Konkrétní datum** s datem a časem. Po termínu tlačítko *Zrušit registraci* zmizí a účastník se musí obrátit na vás.

Nastavení termín **přidává**, možnost odhlášení neruší. S vypnutým *Odhlášením ze session* může účastník registraci zrušit kdykoli.

Použití: workshop s objednaným cateringem nebo tištěnými materiály, kde potřebujete znát počty dva dny předem.

**Upozornění organizátorovi při změně registrace účastníka na session.**
E-mail organizátorovi, když se účastník sám zaregistruje nebo registraci zruší. Po zapnutí vyplníte adresy příjemců (víc adres oddělte čárkou); bez adresy nastavení neuložíte. Vhodné pro workshopy s asistentem, který plánuje kapacitu (catering, materiály).

**Upozornění účastníkovi při změně registrace na session.**
Potvrzovací e-mail účastníkovi, když se sám zaregistruje nebo registraci zruší. Na ruční přidání a odebrání účastníka organizátorem se nevztahuje. To řídí samostatný přepínač **Upozornění účastníkovi při manuálním přiřazení/odebrání**, který není mezi registračními poli: najdete ho jen u konkrétní session na záložce **Účastníci** a z typu se nedědí (viz [Správa sessions](https://help.happenee.com/cs/articles/69-sprava-sessions)).

**Odeslat ICS účastníkovi.**
Přiloží k potvrzovacímu e-mailu ICS soubor, kterým si účastník session přidá do kalendáře. Samostatný e-mail neposílá: když je *Upozornění účastníkovi při změně registrace na session* vypnuté, účastník po registraci nedostane nic, ani ICS. Přikládá se také k e-mailu o ručním přidání účastníka.

### Flow registrace v aplikaci

1. Účastník otevře **účastnickou aplikaci** (mobilní nebo webovou) a najde session v Programu.
2. Na detailu session vidí tlačítko **Registrovat** (pokud není obsazeno a splňuje podmínky viditelnosti).
3. Po kliknutí se automaticky registruje. Pokud je nastavené, dostane e-mail s potvrzením a ICS.
4. Session se mu zobrazí v **Moje agenda**.

Mimo nastavené okno tlačítko **Registrovat** není k dispozici. Místo něj je v detailu session zpráva *Registrace bude otevřena od* s datem a časem, nebo *Registrace skončila*. U session, na které účastník registrovaný je, se po termínu odhlášení objeví *Možnost odhlášení skončila*. Účastník tak vidí důvod a nemusí se ptát vás.

### Kapacita a wait list

Happenee dnes nepodporuje **wait list** (čekací seznam). Po naplnění kapacity se workshop označí jako obsazený a další registrace jsou odmítnuty. Pokud někdo zruší, místo se uvolní a další účastník se může přihlásit (ale ne automaticky z wait listu — musí aktivně kliknout Registrovat).

### Viditelnost workshopu

Na záložce **Viditelnost** panelu session:

- **Veřejné** — workshop vidí všichni účastníci.
- **Pouze pro vybrané skupiny** — workshop vidí jen účastníci z vybraných skupin. Ostatní ho v programu vůbec neuvidí.

Rozdíl proti *Registrace pouze pro vybrané skupiny*: omezení viditelnosti = účastník workshop nevidí vůbec; omezení registrace = vidí ho, ale nemůže se přihlásit.

Obě omezení jdou kombinovat, ale ne libovolně — **viditelnost je nadřazená registraci**. Jakmile viditelnost omezíte na skupiny, zúží se tím i výběr u *Registrace pouze pro vybrané skupiny* na tytéž skupiny. Nastavujte proto nejdřív viditelnost a až potom registraci; obráceným postupem vám skupina, kterou chcete pustit k registraci, v nabídce chybí.

### Workshop bez registračního bloku vs s blokem

Bez bloku: účastník se může registrovat na **libovolný počet workshopů**. Vhodné pro dobrovolné workshopy nebo tréninkové programy s více paralelními streamy, kde si účastník skládá vlastní itinerář.

S blokem: účastník si vybírá **1–N workshopů ze sady**. Vhodné pro formát „ráno si vyberete jeden ze tří workshopů, odpoledne další ze tří“. Detail v článku *Jak fungují registrační bloky, místa a štítky*.

## Na co si dát pozor

### Workshop s kapacitou bez *Omezit počet registrací*. Registruje se víc účastníků, než se vejde

Kapacitu vždy nastavte — systém registrace zablokuje po naplnění. Bez nastavení je kapacita neomezená.

### Účastník se nemůže přihlásit na session přes microsite. Organizátor si myslí, že je rozbitá

Registrace na workshopy je **jen v účastnické aplikaci**. Na microsite účastník workshop vidí, ale pro registraci musí do aplikace.

### Skupina pro přiřazení po registraci není vytvořena. Účastník se zaregistruje, ale skupina zůstává prázdná

**Založte skupinu předem** v Kontaktech a skupinách, teprve pak ji přiřaďte k workshopu.

### Stejnou skupinu používáte pro workshop i pro trvalý segment. Po odebrání ze session o ni účastník přijde úplně

Odebrání skupiny po registraci je **bezpodmínečné**. Když účastníka ze session odeberete nebo na ní vypnete přiřazování, skupina se mu sebere i v případě, že ji má přiřazenou zároveň odjinud — z registračního odkazu, slevového kódu, vstupenky, jiné session nebo z ručního přiřazení. Systém nekontroluje, jestli účastníka ve skupině drží ještě jiný důvod. Pro přiřazení po registraci na session proto používejte **vyhrazenou skupinu**. Nesdílejte ji s trvalým segmentem — například se skupinou „Partner XY“, do které partnery řadí jejich hromadný registrační odkaz a na které stojí cílení kampaní nebo viditelnost obsahu. Když pak takového partnera odeberete z workshopu, o skupinu přijde a segmentace se tiše rozbije.

### Snaha změnit kapacitu workshopu po registracích. Někteří účastníci jsou už přihlášení, další čekají

Kapacitu **zvýšit** lze kdykoli. **Snížit** pod aktuální počet registrovaných nelze — systém nedovolí. Pro snížení musíte nejdřív zrušit registraci účastníkům ručně.

### Skupina, kterou chcete pustit k registraci, není ve výběru u *Registrace pouze pro vybrané skupiny*

Nabídka je omezená na skupiny, pro které je session viditelná. Pokud skupinu ve výběru nevidíte, doplňte ji nejdřív na záložce **Viditelnost** k volbě *Pouze pro vybrané skupiny*, nebo viditelnost přepněte na *Veřejné* — pak vybíráte z celého seznamu skupin.

### Obě hranice okna registrace nastavené na *Neomezeně*. Nastavení nejde uložit

Časové omezení musí omezovat aspoň jednu stranu. Když nechcete registraci uzavírat, nechte *Neomezeně* jen u **Možnost registrace do**; když ji nechcete odkládat, jen u **Možnost registrace od**. Obojí naráz systém odmítne.

### Registrace se má otevřít později, než se zavírá. Systém hlásí chybu

Hláška zní *Začátek registrace musí být dříve než její konec*. V režimu *Konkrétní datum* je chyba vidět na první pohled. V režimu *Dle začátku session* se plete snadno, protože obě čísla jsou odstupy **před** začátkem workshopu — otevření proto musí být větší odstup než uzavření. Platné je „otevřít 7 dní předem, uzavřít 1 den předem"; kombinace „otevřít 15 minut předem, uzavřít den předem" je neplatná.

### Workshop se drží ve stavu *Skryto*, aby se na něj nešlo přihlásit dřív

Obvyklá obcházka: session se předpřipraví skrytá a v den spuštění se publikuje. Není potřeba a má nevýhodu — skrytou session účastník v programu nevidí, takže si dopředu nenaplánuje, na co půjde. Nechte session publikovanou a čas otevření řešte **Časovým omezením registrace**.

### Je zapnuté *Odeslat ICS účastníkovi*, ale účastníkovi po registraci nic nepřišlo

ICS se jen přikládá k potvrzovacímu e-mailu. Zapněte i **Upozornění účastníkovi při změně registrace na session**.

### Účastníka jste ručně přidali nebo odebrali a e-mail mu nepřišel

*Upozornění účastníkovi při změně registrace na session* ruční změny nepokrývá. E-mail pošle jen přepínač **Upozornění účastníkovi při manuálním přiřazení/odebrání** na záložce **Účastníci**, který je ve výchozím stavu vypnutý a nastavuje se u každé session zvlášť (u časového slotu u každého slotu). Zapněte ho dřív, než změnu uložíte; na už uložené změny se e-mail dodatečně nepošle.

### Účastník v kampani dostane upozornění na workshop, ale v aplikaci jej nevidí

Zkontrolujte, zda má účastník **viditelnost** na daný workshop (skupiny) a zda je **stav session** Publikováno. Třetí možnost: účastník není registrovaný na event (musí být přihlášen do aplikace se stavem *Zúčastním se*).

## Související články

- [Sestavení programu události — architektura](https://help.happenee.com/cs/articles/26-sestaveni-programu-udalosti-%E2%80%94-architektura)
- [Jak fungují typy sessions](https://help.happenee.com/cs/articles/27-jak-funguji-typy-sessions)
- [Správa sessions](https://help.happenee.com/cs/articles/69-sprava-sessions)
- [Jak fungují časové sloty](https://help.happenee.com/cs/articles/29-jak-funguji-casove-sloty)
- [Jak fungují registrační bloky, místa a štítky](https://help.happenee.com/cs/articles/31-jak-funguji-registracni-bloky-mista-a-stitky)
- [Správa řečníků](https://help.happenee.com/cs/articles/23-sprava-recniku)
- [Nastavení rezervací v programu — auta, workshopy, doprovodný program](https://help.happenee.com/cs/articles/30-nastaveni-rezervaci-v-programu-%E2%80%94-auta-workshopy-doprovodny-program)
- [Jak funguje Moje agenda](https://help.happenee.com/cs/articles/35-jak-funguje-moje-agenda)
- [Nastavení typu registrace a doplňujících otázek](https://help.happenee.com/cs/articles/12-nastaveni-typu-registrace-a-doplnujicich-otazek)
- [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti)
- [Doporučený setup pro konferenci](https://help.happenee.com/cs/articles/55-doporuceny-setup-pro-konferenci)
- [Co dělat, když nefunguje registrace na workshop nebo session](https://help.happenee.com/cs/articles/90-co-delat-kdyz-nefunguje-registrace-na-workshop-nebo-session)
- [Co dělat, když je workshop plný](https://help.happenee.com/cs/articles/91-co-delat-kdyz-je-workshop-plny)
- [Doporučený setup pro testovací jízdy](https://help.happenee.com/cs/articles/98-doporuceny-setup-pro-testovaci-jizdy)

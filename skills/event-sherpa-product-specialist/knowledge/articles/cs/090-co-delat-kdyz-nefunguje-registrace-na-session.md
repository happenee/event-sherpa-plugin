# Co dělat, když nefunguje registrace na workshop nebo session

> Účastník nevidí tlačítko pro registraci na session, nebo se mu registrace nedaří dokončit. Nastavení a situace, které to nejčastěji způsobují.

- Článek v Help Centru: https://help.happenee.com/cs/articles/90-co-delat-kdyz-nefunguje-registrace-na-workshop-nebo-session
- English version: https://help.happenee.com/en/articles/90-what-to-do-when-workshop-or-session-registration-does-not-work
- Kolekce: Řešení problémů
- Aktualizováno: 2026-09-16

---

> [!info] Krátce
> Účastník tvrdí, že se na workshop nemůže přihlásit — buď nevidí tlačítko, nebo mu systém registraci nedovolí. Příčina je skoro vždy ve viditelnosti session, zapnuté registraci, časovém omezení registrace, vyčerpané kapacitě, limitu registračního bloku nebo v časovém překryvu s jinou registrací.

## Jak začít

Zeptejte se účastníka, **co přesně vidí**: chybí tlačítko, nebo se registrace nedokončí? Tahle jedna odpověď rozdělí příčiny na dvě skupiny a ušetří polovinu hledání.

## Detail

### Tlačítko pro registraci vůbec není vidět

- **Session není viditelná pro skupinu**, do které účastník patří. Zkontrolujte viditelnost session i jejího typu — nastavení může být na obou úrovních.
- **Registrace na session není zapnutá.** Bez ní je session jen položkou v programu; účastník si ji může uložit do Mojí agendy, ale nepřihlásí se na ni.
- **Session je skrytá.** Stav *Skryto* znamená, že ji účastník nevidí vůbec.
- **Registrace ještě nezačala, nebo už skončila.** Když má session zapnuté **Časové omezení registrace**, je místo tlačítka zpráva *Registrace bude otevřena od* s datem a časem, nebo *Registrace skončila*. Okno zkontrolujte na session i na jejím typu — nastavení může být na obou úrovních.

### Registrace se nedokončí

- **Kapacita je vyčerpaná.** Čekací seznam v Happenee neexistuje, takže po naplnění se přihlásit nelze.
- **Limit registračního bloku.** Blok omezuje, na kolik sessions z dané skupiny se účastník může přihlásit. Když limit vyčerpal jinde, na další session už ho systém nepustí — i když v ní je místo.
- **Časový překryv s jinou registrací.** Ve výchozím stavu se účastník nemůže registrovat na session, která se časově překrývá s jinou, na kterou už je registrovaný, ani když je v jiném Programu. Tlačítko **Registrovat** vidí neaktivní a v prohlížeči po najetí myší důvod *V tomto čase už máte registraci na jiné session.* Zjistěte, kde je v tu dobu registrovaný, a zkontrolujte **Nastavení** programu. U sessions z různých Programů musí být **Povolit souběžné registrace mezi Programy** zapnuté v obou.
- **Nedokončená registrace na událost.** Kdo nemá dokončenou registraci na události, nemá se kam přihlašovat.

### Účastník se nemůže odhlásit

Po termínu **Odhlášení ze session** tlačítko *Zrušit registraci* zmizí a účastník vidí zprávu *Možnost odhlášení skončila*. Registraci pak zruší jen organizátor v administraci. Když je *Odhlášení ze session* vypnuté, žádný termín neplatí a účastník se odhlásí kdykoli.

### Jak to ověřit rychle

Nejrychlejší cesta je otevřít si program v účastnické aplikaci pod testovacím účtem zařazeným do stejné skupiny jako stěžující si účastník. Uvidíte přesně to, co on.

## Na co si dát pozor

### Viditelnost se kontroluje jen na session

Session dědí nastavení od svého typu. Když je přepnutá na vlastní hodnoty, platí ty; když ne, platí typ. Při hledání příčiny se dívejte na obě úrovně, ne jen na jednu.

### Účastník tlačítko vidí, ale registrace neprojde

Časové okno se vyhodnocuje na serveru. Když měl účastník aplikaci otevřenou přes okamžik uzavření registrace, tlačítko mu na obrazovce zůstalo, ale server registraci odmítne a stránka se obnoví. Není to chyba — ověřte, kdy okno končí.

### Kapacita se plete s limitem bloku

Obojí zabrání registraci, ale řeší se jinak. U vyčerpané kapacity můžete kapacitu zvýšit; u limitu bloku musíte účastníka nejdřív odhlásit z jiné session. V administraci proto vždy ověřte, které z obou opravdu brání.

### Účastník se přihlásí, ale organizátor ho v seznamu nevidí

Zkontrolujte, jestli se nedíváte na jinou session se stejným názvem — u vícedenních událostí se běžně opakují. Ručně přidaní lidé jsou navíc označení jako **Přiřazen organizátorem**, takže je poznáte od těch, kteří se přihlásili sami.

## Související články
- [Nastavení workshopů a registrace na sessions](https://help.happenee.com/cs/articles/28-nastaveni-workshopu-a-registrace-na-sessions)
- [Jak fungují registrační bloky, místa a štítky](https://help.happenee.com/cs/articles/31-jak-funguji-registracni-bloky-mista-a-stitky)
- [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti)

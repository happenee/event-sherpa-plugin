# Sledování doručitelnosti e-mailů a kampaní

> Jak číst graf Stav rozesílky, co znamená Nedoručeno a jak se liší od nepřečteného, a kde najdete doručení a otevření u jednotlivého příjemce.

- Článek v Help Centru: https://help.happenee.com/cs/articles/80-sledovani-dorucitelnosti-e-mailu-a-kampani
- English version: https://help.happenee.com/en/articles/80-tracking-e-mail-and-campaign-deliverability
- Kolekce: Komunikace a pozvánky
- Aktualizováno: 2026-09-21

---

> [!info] Krátce
> Po odeslání kampaně zjistíte na záložce **Rozesílka**, jak dopadla — prstencový graf **Stav rozesílky** ukazuje rozpad na doručené, přečtené a nedoručené e-maily a tabulka pod ním vypíše jednotlivé rozesílky. Přes odkaz **E-maily** se dostanete až na úroveň konkrétního příjemce a uvidíte, jestli mu zpráva došla, jestli ji otevřel a jestli klikl. Tahle data jsou první místo, kam se podívat, když někdo tvrdí, že mu nic nepřišlo.

## Jak začít

Otevřete kampaň a přepněte na záložku **Rozesílka**. Číslo v odznaku u názvu záložky říká, kolik rozesílek kampaň zatím měla — doposlání nově přiřazeným zakládá další rozesílku, takže jich může být víc než jedna.

Postupujte odshora dolů: nejdřív graf pro celkový obrázek, pak tabulka rozesílek, teprve nakonec detail konkrétního příjemce.

## Detail

### Graf Stav rozesílky

Prstencový graf rozdělí e-maily do pěti kategorií:

- **K odeslání** — Zpráva čeká ve frontě, ještě neodešla.
- **Odesílá se** — Rozesílka právě probíhá.
- **Doručeno a nepřečteno** — E-mail dorazil do schránky, příjemce ho zatím neotevřel.
- **Doručeno a přečteno** — E-mail dorazil a byl otevřen.
- **Nedoručeno** — Zpráva se nedostala do schránky — neexistující adresa, plná schránka, odmítnutí serverem příjemce.

Zásadní je rozdíl mezi **Nedoručeno** a **Doručeno a nepřečteno**. *Nedoručeno* je technický problém na straně adresy a řeší se opravou kontaktu. *Doručeno a nepřečteno* znamená, že e-mail v pořádku dorazil a jde jen o to, že ho příjemce ještě neotevřel — s tím nic technického neuděláte, pomůže leda připomínka.

### Tabulka rozesílek

Pod grafem je seznam jednotlivých rozesílek dané kampaně, novější nahoře. U každé vidíte **datum a čas**, **počet e-mailů** a **stav odeslání** (*Probíhá odesílání* → *Odesláno*). Přepínačem **Zobrazit testovací rozesílky** si zobrazíte i testy, které jste si poslali na vlastní adresu — ve výchozím stavu se nezapočítávají.

Běžící rozesílku lze smazat ikonou koše. U dokončené rozesílky už ikona není — odeslané e-maily zpět nevezmete.

### Detail příjemců

Odkaz **E-maily** u rozesílky (nebo tlačítko v hlavičce kampaně) otevře seznam všech příjemců se sloupci **Mailgun**, **Odesláno**, **Doručeno**, **Otevřený** a **Kliknuto**. Seznam se dá prohledávat podle e-mailu.

Každý řádek jde rozbalit a zobrazí se **náhled konkrétního e-mailu tak, jak ho příjemce dostal** — včetně hlavičkového obrázku, registračního tlačítka a záložního textového odkazu pro případ, že tlačítko nefunguje. To je nejrychlejší způsob, jak ověřit, co komu skutečně odešlo, když si stěžuje na obsah nebo na nefunkční odkaz.

### Doposlání nově přiřazeným

Blok **Doposlat kampaň nově přiřazeným** ukazuje počet kontaktů, které se k události nebo do skupiny dostaly až po zahájení rozesílky — ať už je přiřadil organizátor, nebo přibyly registrací či nákupem vstupenky. Tlačítkem **Nově přiřazení** jim kampaň dopošlete.

Doposlání **zakládá novou rozesílku**, ne pokračování té původní. V tabulce proto přibude další řádek a odznak u záložky se zvýší. Když sledujete čísla, počítejte s tím, že jedna kampaň může mít několik rozesílek s různým počtem příjemců.

### Zvací e-mail

Zvací e-mail nemá vlastní prstencový graf doručitelnosti. To, jak lidé reagovali, čtete přes **stavy účastníků** — kdo nereagoval, kdo se registroval, kdo účast odmítl. Reporting stavů je popsaný v článku o statistikách účastníků; pro sledování technické doručitelnosti je vhodnější nástroj kampaň.

## Na co si dát pozor

### Nedoručeno se plete s nepřečteno

Nejčastější chyba při čtení grafu. Když organizátor hlásí „polovina e-mailů nedorazila", obvykle se dívá na *Doručeno a nepřečteno*. Ty e-maily dorazily. Skutečný problém je jen segment **Nedoručeno** — a ten se řeší kontrolou adres, ne opakovaným rozesíláním.

### Vysoké Nedoručeno se bere jako chyba Happenee

Vysoký počet nedoručených obvykle znamená vadná data: překlepy v adresách z ručního přepisu, staré kontakty po odchodu zaměstnanců, firemní adresy zrušené při reorganizaci. Projděte si konkrétní adresy v detailu příjemců — vzorec bývá vidět na první pohled a opravit je potřeba kontakty, ne kampaň.

### Čísla se čtou hned po odeslání

Doručování i otevírání má zpoždění. Pár minut po rozeslání uvidíte většinu e-mailů ve stavu *K odeslání* nebo *Odesílá se* a téměř nulovou otevřenost. Rozumný odečet je za několik hodin, u ranní rozesílky nejdřív odpoledne.

### Test se počítá do statistik

Testovací rozesílky jsou ve výchozím zobrazení skryté právě proto, aby čísla nekazily. Když si přepínač **Zobrazit testovací rozesílky** zapnete a zapomenete na to, budou vám počty příjemců sedět o vaše vlastní testy.

## Související články
- [Vytvoření a odeslání e-mailové kampaně](https://help.happenee.com/cs/articles/41-vytvoreni-a-odeslani-e-mailove-kampane)
- [Cílení komunikace podle skupin a stavů](https://help.happenee.com/cs/articles/43-cileni-komunikace-podle-skupin-a-stavu)
- [Co dělat, když nepřišel e-mail](https://help.happenee.com/cs/articles/58-co-delat-kdyz-neprisel-e-mail)

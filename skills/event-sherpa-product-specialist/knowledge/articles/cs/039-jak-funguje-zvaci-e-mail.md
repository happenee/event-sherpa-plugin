# Jak funguje zvací e-mail

> Zvací e-mail je první vlna pozvánek pro přiřazené kontakty.

- Článek v Help Centru: https://help.happenee.com/cs/articles/39-jak-funguje-zvaci-e-mail
- English version: https://help.happenee.com/en/articles/39-how-the-invitation-e-mail-works
- Kolekce: Komunikace a pozvánky
- Aktualizováno: 2026-09-21

---

> [!info] Krátce
> Zvací e-mail je systémová zpráva, kterou rozešlete kontaktům přiřazeným k události, aby se dostali na microsite a zaregistrovali. Obsahuje předmět, tělo (s proměnnými), registrační tlačítko, případně ICS soubor a patičku. Hodí se jako **první vlna pozvánek** — typicky po importu kontaktů. Pokud ale potřebujete cílit na různé skupiny nebo plánovat rozesílku, použijte místo něj **e-mailovou kampaň**.

## Jak začít

- Nejprve přiřaďte kontakty k události (ve správě kontaktů a skupin). Bez přiřazených kontaktů není koho pozvat.
- Vyplňte obsah zvacího e-mailu **ve všech jazycích události** — systém rozesílá variantu podle *preferovaného jazyka* kontaktu.
- Než spustíte hromadnou rozesílku, odešlete si zkušební zvací e-mail a ověřte vzhled i funkčnost tlačítka.
- Pokud budete potřebovat cílit na různé skupiny nebo odeslat follow-up, připravte si vedle zvacího e-mailu i e-mailové kampaně.

## Detail

### Kde zvací e-mail najdete

V levém menu události → modul **Zvací e-mail**. V modulu je editor těla e-mailu, předmět, registrační tlačítko, nastavení, odeslání a statistiky.

### Editor a proměnné

Text e-mailu píšete v textovém editoru. Dole najdete **zástupné proměnné** (merge tagy), které systém automaticky nahradí údaji účastníka — jménem, názvem události, datem a dalšími. Stejné proměnné fungují v potvrzovacím e-mailu i v kampaních.

Editor zvládá základní formátování. Pokročilejší WYSIWYG je v produktu rozpracovaný; v běžných scénářích si vystačíte se současným editorem.

### Registrační tlačítko — kam má vést

V sekci **Kam má registrační tlačítko vést?** vybíráte cíl tlačítka. Nabídka se liší podle typu události:

- **Osobní odkaz pro adresáta** — odkaz je svázaný s konkrétním kontaktem. U neplacené události nelze e-mail pro registraci změnit a adresát může účast potvrdit, nebo odmítnout. U placené události odkaz personalizuje microsite a adresát pokračuje na nákup vstupenky, kde smí uvést jiný e-mail.
- **Veřejný odkaz** — po kliknutí se zobrazí microsite, kde zájemce zadá libovolný e-mail a pokračuje dál. Odkaz lze veřejně šířit.
- **Individuální vstup zdarma** — jen u placené události. Adresát se zaregistruje bez nutnosti koupit vstupenku — to je nástroj na guest list zdarma.

Který typ kdy použít je popsané v článku *Osobní a veřejný odkaz: jaký je rozdíl*.

### Úvodní obrázek, ICS a patička

Grafické a technické prvky se sdílejí s potvrzovacím e-mailem a microsite, proto se nastavují centrálně v **Nastavení události**:

- **Úvodní obrázek** — v sekci Nastavení grafiky. Společný pro zvací e-mail, potvrzovací e-mail, microsite a účastnickou aplikaci.
- **Příloha ICS** — v sekci Nastavení e-mailů / ICS souboru. Po rozbalení nabídne účastníkovi přidání události do kalendáře.
- **Patička e-mailu** — v sekci Nastavení e-mailů. Buď výchozí text platformy, nebo vlastní.
- **Odesílatel a Příjemce odpovědi** — rovněž v Nastavení e-mailů.

### Odeslání — individuální a hromadné

V sekci **Odeslání** máte dvě cesty:

- **Individuální odeslání zvacího e-mailu** — vyberete konkrétní kontakt a odešlete jen jemu. Hodí se pro zkušební rozesílku (odeslat si ho sám sobě) nebo pro ruční dopozvání jednoho člověka.
- **Hromadné odeslání zvacího e-mailu** — rozesíláte na některý z následujících stavů:
  - **Nepozvaní** — kontakty přiřazené k události, kterým zvací e-mail ještě nebyl odeslán.
  - **Kdo si nepřečetl zvací e-mail** — pro druhou vlnu, když na první nereagovali.
  - **Kdo je neregistrovaný (bez odpovědi)** — dostali pozvánku, ale ještě nevyplnili registrační formulář.

Systém u toho ukazuje, **kolik kontaktů je k události přiřazeno** a v jakých jazycích — například „43 česky, 13 anglicky, 2 bez nastaveného jazyka“.

### Jazykový fallback podle kontaktu

Zvací e-mail se rozesílá podle **preferovaného jazyka** kontaktu ve správě kontaktů a skupin. Proto:

- Při importu kontaktů vyplňujte sloupec s jazykem. Pokud jazyk není nastaven, systém použije primární jazyk události.
- Preferovaný jazyk se automaticky přednastaví i při registraci z microsite — podle jazyka, v jakém si účastník otevřel microsite.
- Máte-li kontakty bez jazyka, doplňte ho před rozesláním, nebo počítejte s tím, že dostanou variantu v primárním jazyce.

### Test zvacího e-mailu

Individuální odeslání je zároveň nástroj pro zkoušku — odešlete si zvací e-mail sám sobě (nebo na testovací adresu) a ověřte vzhled, proměnné a funkčnost tlačítka. Vždycky otestujte ještě **druhý jazyk**, nejen primární.

### Statistiky a reporting

Pod odesláním najdete přehled stavu zvacího e-mailu — komu byl odeslán, kdo ho otevřel, kdo na něj reagoval registrací. Tyto stavy zároveň slouží jako cílení pro další rozesílky („kdo si nepřečetl“, „bez odpovědi“).

### Legacy status a směřování k e-mailovým kampaním

Zvací e-mail je historicky daný modul — byl v produktu dřív než e-mailové kampaně. Nemá napojení na reporty v takovém rozsahu jako kampaně a **neumí cílit podle skupin**, jen podle stavů účastníků. Pokud potřebujete flexibilněji cílit, plánovat rozesílku nebo dorozesílat nově přiřazeným kontaktům, použijte kampaň.

Produkt v této oblasti postupně směřuje k tomu, aby veškerá zvací komunikace šla přes kampaně. Zvací e-mail jako takový zatím běží dál a je plně funkční.

## Na co si dát pozor

### Organizátor vyplní zvací e-mail jen v primárním jazyce a kontakty s druhým jazykem nedostanou pozvánku ve svém jazyce

Po přepnutí vlajky v pravém horním rohu vyplňte tělo i předmět i v sekundárním jazyce. Před rozesláním si pošlete testovací zvací e-mail v obou jazycích.

### Organizátor importuje kontakty bez sloupce s preferovaným jazykem a následně se diví, proč angličtí účastníci dostali pozvánku česky

Při importu vyplňujte sloupec s jazykem. Pokud chybí, ve správě kontaktů ho doplňte jednotlivě nebo hromadnou úpravou — a teprve pak spusťte rozesílku.

### Organizátor chce pozvat jen konkrétní skupinu (například VIP), ale přes zvací e-mail to nejde

Zvací e-mail cílí pouze podle stavů, ne podle skupin. Pro cílení na skupiny použijte **e-mailovou kampaň**.

### Organizátor očekává, že zvací e-mail půjde i kontaktům, které ještě nepřiřadil k události

Přiřaďte kontakty k události ve správě kontaktů a skupin — teprve pak se objeví v rozesílce.

### Organizátor zapomene, že úvodní obrázek a patička nejsou v modulu Zvací e-mail, a hledá je uvnitř editoru

Grafika a příloha ICS se řídí z **Nastavení události** (sekce Grafika a E-maily). V modulu Zvací e-mail editujete hlavně tělo a předmět.

## Související články

- [Jak funguje potvrzovací e-mail](https://help.happenee.com/cs/articles/40-jak-funguje-potvrzovaci-e-mail)
- [Kdy použít zvací e-mail a kdy e-mailovou kampaň](https://help.happenee.com/cs/articles/42-kdy-pouzit-zvaci-e-mail-a-kdy-e-mailovou-kampan)
- [Vytvoření a odeslání e-mailové kampaně](https://help.happenee.com/cs/articles/41-vytvoreni-a-odeslani-e-mailove-kampane)
- [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace)
- [Osobní a veřejný odkaz: jaký je rozdíl](https://help.happenee.com/cs/articles/44-osobni-a-verejny-odkaz-jaky-je-rozdil)
- [Co dělat, když nepřišel e-mail](https://help.happenee.com/cs/articles/58-co-delat-kdyz-neprisel-e-mail)
- [Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka](https://help.happenee.com/cs/articles/5-microsite-vs-ucastnicka-aplikace-jak-premyslet-nad-flow-ucastnika)
- [Cílení komunikace podle skupin a stavů](https://help.happenee.com/cs/articles/43-cileni-komunikace-podle-skupin-a-stavu)
- [Doporučený setup pro interní firemní event](https://help.happenee.com/cs/articles/53-doporuceny-setup-pro-interni-firemni-event)
- [Doporučený setup pro externí klientský event](https://help.happenee.com/cs/articles/54-doporuceny-setup-pro-externi-klientsky-event)
- [Zvací e-mail jako save the date](https://help.happenee.com/cs/articles/63-zvaci-e-mail-jako-save-the-date)
- [Jak fungují zástupné proměnné](https://help.happenee.com/cs/articles/78-jak-funguji-zastupne-promenne)

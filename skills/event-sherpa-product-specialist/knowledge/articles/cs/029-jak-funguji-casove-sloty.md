# Jak fungují časové sloty

> Session, kde si účastník rezervuje konkrétní čas z nabídky (testovací jízdy, konzultace, schůzky).

- Článek v Help Centru: https://help.happenee.com/cs/articles/29-jak-funguji-casove-sloty
- English version: https://help.happenee.com/en/articles/29-how-time-slots-work
- Kolekce: Obsah a zkušenost účastníka
- Aktualizováno: 2026-09-16

---

> [!info] Krátce
> Časový slot je typ session, kde účastník **rezervuje konkrétní čas** z nabídky. Session má definovanou délku (například hodinu), kterou systém rozdělí na **jednotlivé sloty** (například 15minutové s 5minutovou přestávkou mezi sloty). Účastník si vybere jeden slot podle své preference. Typické použití: testovací jízdy, individuální konzultace, one-to-one meetingy, doprovodný program (detail v *Nastavení rezervací v programu — auta, workshopy, doprovodný program*).

## Jak začít

- Rozhodněte **délku jednoho slotu** podle toho, kolik času potřebujete na interakci. Na výběr je 10, 15, 20, 30, 45, 50, 60, 90 nebo 120 minut; výchozí hodnota je 15 minut. Jinou délku (například 5 nebo 25 minut) nastavit nelze.
- Rozhodněte **délku přestávky** mezi sloty (pauza na předání, reset). Na výběr je 0, 5, 10 nebo 15 minut; výchozí je 0 minut, sloty tedy jdou hned za sebou. Přestávka je samostatné nastavení a do délky slotu se nezapočítává.
- **Maximální počet účastníků na jeden slot** je obvykle 1 (individuální konzultace), ale lze povolit víc (skupinové sloty).
- Časový slot je session, takže má místo, řečníky (instruktory / odborníky) a další atributy jako běžná session.

## Detail

### Jak se časový slot vytvoří

Session typu **Časový slot** má v panelu úprav kromě běžných záložek navíc záložku **Sloty**. Při vytváření:

1. Vytvořte session typu **Časový slot** (nebo vlastní typ s tímto základem).
2. Zadejte **datum, začátek, konec** — to určuje celkovou délku session (například 9:00–12:00 = 180 minut).
3. V sekci **Nastavení registrace** zadejte:
   - **Délka časového slotu** — jedna z hodnot 10, 15, 20, 30, 45, 50, 60, 90 nebo 120 minut. Výchozí hodnota v nabídce je 15 min.
   - **Délka přestávky** — pauza mezi sloty: 0, 5, 10 nebo 15 minut (výchozí 0 min).
   - **Omezit počet registrací** — počet účastníků na jeden slot (výchozí 1).
4. Uložte. Systém vygeneruje sloty.

Pro délku 180 minut, slot 15 min, přestávka 5 min systém vygeneruje **9 slotů** (9:00, 9:20, 9:40, 10:00, 10:20, 10:40, 11:00, 11:20, 11:40). Zbytek na konci session, který je kratší než jeden slot, systém jako slot nevytvoří.

### Záložka Sloty

Záložka **Sloty** je dostupná pouze u sessions typu Časový slot. Zobrazuje všechny vygenerované sloty — každý slot s časovým rozsahem, kapacitou a počtem registrovaných účastníků. Přestávky mezi sloty jsou zobrazeny jako samostatné řádky.

U každého slotu lze:

- **Přepnout toggle Aktivní / Neaktivní** — neaktivní slot není dostupný pro registraci (typicky pokud odpadne instruktor a slot se zruší). Má-li slot registrované účastníky, zobrazí se při uložení potvrzovací dialog s jejich počtem. Tlačítkem **Odebrat účastníky a uložit** registrace zrušíte a slot deaktivujete; když dialog zavřete, změna se neuloží.
- Kliknutím na tlačítko **Účastníci** otevřít dialog **Upravit účastníky** — vidíte seznam registrovaných účastníků, limit, kapacitu. Organizátor může:
  - **Odebrat** účastníka ze slotu.
  - **Přidat účastníka ručně** (vyhledat v poli a přidat). Ručně přiřazení účastníci jsou označeni jako **Přiřazen organizátorem**.
  - Zapnout **Upozornění účastníkovi při manuálním přiřazení/odebrání** — účastník pak dostane e-mail, když ho do slotu přidáte nebo z něj odeberete; k e-mailu o přidání se přiloží ICS, pokud je zapnuté **Odeslat ICS účastníkovi**. Přepínač platí jen pro daný slot a ve výchozím stavu je vypnutý.

### Flow účastníka

1. Účastník otevře session v účastnické aplikaci.
2. Vidí **seznam dostupných slotů** s obsazeností (pokud je zapnuté zobrazování zbývajících míst).
3. Klikne na konkrétní slot → zaregistruje se.
4. Slot se mu zobrazí v **Moje agenda**.

### Zobrazení slotů přímo v přehledu programu

Ve výchozím stavu účastník vidí sloty až po otevření detailu session. Pokud v záložce **Nastavení** programu zapnete **Rozbalit časové sloty v programu**, zobrazí se sloty přímo na kartě session v přehledu programu — účastník vybírá čas bez otevírání detailu. Hodí se, když jsou sloty jádrem programu (například testovací jízdy nebo konzultace).

### Registrační nastavení (stejné jako u Workshopu)

Časový slot má stejnou sadu registračních nastavení jako Workshop:

- Přiřadit účastníka do skupiny po registraci
- Registrace pouze pro vybrané skupiny
- Omezit počet registrací (na **jeden slot**, ne na session jako celek)
- Zobrazit počet dostupných míst
- Časové omezení registrace (**Možnost registrace od** / **do**)
- Odhlášení ze session (**Možnost odhlášení do**)
- Upozornění organizátorovi / účastníkovi
- Odeslat ICS účastníkovi

Detail viz článek *Nastavení workshopů a registrace na sessions*.

### Kapacita na slot

Výchozí hodnota **Omezit počet registrací** u časového slotu je **1** (individuální schůzka). Lze ji zvýšit — například u skupinové konzultace 3 na slot. Všichni registrovaní v jednom slotu tam přijdou ve stejný čas.

### Zrušení registrace a uvolnění slotu

Když účastník zruší registraci:

- Slot se uvolní.
- Místo je znovu dostupné pro jiného účastníka.
- Happenee nemá automatický wait list — místo se neautomaticky přidělí dalšímu.

Pokud jste u session nastavili **Odhlášení ze session**, platí termín i tady: po něm už účastník registraci nezruší **ani nepřepne na jiný slot**. Změnu času za něj musíte udělat vy. Termín proto nastavujte s ohledem na to, jak dlouho chcete přehazování slotů dovolit.

### Víc sessions typu Časový slot

Můžete mít **více sessions typu Časový slot** v programu najednou (například *Konzultace s CFO* a *Konzultace s CTO*). Každá session má vlastní sloty. Účastník se může registrovat na sloty z různých sessions, ve výchozím stavu ale ne na dva sloty, jejichž časy se překrývají. To dovolí až povolené souběžné registrace v nastavení programu (viz *Sestavení programu události — architektura*). Sloty, které na sebe jen navazují, se nepřekrývají.

### Zamčená pole po první registraci

> ⚠️ Po registraci prvního účastníka na session typu Časový slot **nelze změnit**:
> - Typ session
> - Čas začátku a konce
> - Délku časového slotu
> - Délku přestávky

Plánujte tyto parametry dopředu. Přidat další čas (například 12:00–14:00 jako druhá session) lze — ale upravovat existující po registraci ne.

### Přiřazení řečníka k session (ne ke slotu)

Řečník se přiřazuje k session jako celku, ne ke konkrétnímu slotu. Všichni účastníci ve všech slotech vidí stejného řečníka / instruktora. Pokud potřebujete rozdělit sloty mezi víc řečníků, vytvořte víc sessions (jedna per řečník).

## Na co si dát pozor

### Délka slotu 10 minut bez přestávky. Systém vygeneruje mnoho slotů, ale účastník nestihne přijít, pozdravit a začít

Nejkratší nabízená délka slotu je 10 minut. Reálná délka slotu musí odpovídat reálné interakci: pro individuální konzultaci obvykle 15–30 minut a k tomu krátká přestávka (5 minut) na předání.

### Organizátor mění čas session po první registraci — systém nedovolí

Čas začátku/konce slotu je zamčený po první registraci. Plánujte finální rozvrh **před** otevřením registrace. Pokud musíte změnit, zrušte registraci všem ručně, pak upravte, pak otevřete.

### Session typu Časový slot vytvořen, ale účastník nevidí sloty — jen jednu položku v programu

Zkontrolujte, že session má typ se základem Časový slot a vyplněné pole **Délka časového slotu**. Přestávka může být 0 minut, sloty se generují i bez ní. Záložka **Sloty** ukáže, co systém vygeneroval.

### Kapacita slotu 1, účastník čeká, že se zapíše skupina tří lidí

Zvyšte **Omezit počet registrací** na 3. Pozor — všichni registrovaní přijdou ve stejný čas na stejný slot. Pokud chcete více skupin, vytvořte víc sessions nebo rozdělte čas jinak.

### Účastník zruší registraci, organizátor čeká, že systém pošle upozornění dalšímu na wait listu

Happenee dnes wait list nemá. Uvolněné místo je dostupné všem — první, kdo klikne Registrovat, ho získá.

### Neaktivní slot znovu zaktivněn, ale organizátor zapomněl zrušeného účastníka znovu přidat

Deaktivace slotu registraci zrušila, takže po opětovné aktivaci účastník ve slotu není a sám se nevrátí. Musíte ho ručně vyhledat a přidat přes dialog **Upravit účastníky**. Pokud se o přidání má dozvědět e-mailem, zapněte předtím u slotu **Upozornění účastníkovi při manuálním přiřazení/odebrání**.

## Související články

- [Sestavení programu události — architektura](https://help.happenee.com/cs/articles/26-sestaveni-programu-udalosti-%E2%80%94-architektura)
- [Jak fungují typy sessions](https://help.happenee.com/cs/articles/27-jak-funguji-typy-sessions)
- [Správa sessions](https://help.happenee.com/cs/articles/69-sprava-sessions)
- [Nastavení workshopů a registrace na sessions](https://help.happenee.com/cs/articles/28-nastaveni-workshopu-a-registrace-na-sessions)
- [Nastavení rezervací v programu — auta, workshopy, doprovodný program](https://help.happenee.com/cs/articles/30-nastaveni-rezervaci-v-programu-%E2%80%94-auta-workshopy-doprovodny-program)
- [Jak fungují registrační bloky, místa a štítky](https://help.happenee.com/cs/articles/31-jak-funguji-registracni-bloky-mista-a-stitky)
- [Správa řečníků](https://help.happenee.com/cs/articles/23-sprava-recniku)
- [Jak funguje Moje agenda](https://help.happenee.com/cs/articles/35-jak-funguje-moje-agenda)
- [Doporučený setup pro konferenci](https://help.happenee.com/cs/articles/55-doporuceny-setup-pro-konferenci)
- [Co dělat, když je workshop plný](https://help.happenee.com/cs/articles/91-co-delat-kdyz-je-workshop-plny)
- [Doporučený setup pro testovací jízdy](https://help.happenee.com/cs/articles/98-doporuceny-setup-pro-testovaci-jizdy)

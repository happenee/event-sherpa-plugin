# Jak fungují typy sessions

> Šablona výchozího chování sessions: registrace, viditelnost a engagement funkce.

- Článek v Help Centru: https://help.happenee.com/cs/articles/27-jak-funguji-typy-sessions
- English version: https://help.happenee.com/en/articles/27-how-session-types-work
- Kolekce: Obsah a zkušenost účastníka
- Aktualizováno: 2026-09-16

---

> [!info] Krátce
> Typ session je **šablona výchozího chování** — určuje registraci, viditelnost a engagement funkce pro všechny sessions daného typu. Každá session musí být přiřazena k typu. Happenee obsahuje čtyři základní typy chování (**Přednáška**, **Workshop**, **Časové sloty**, **Přestávka**), z nichž můžete vytvářet vlastní pojmenované typy (*Keynote*, *Panel*, *Masterclass*). Dědičnost jde z typu na session, ale u konkrétní session ji lze přepsat.

## Jak začít

- Před vytvářením sessions **rozhodněte typy**, které budete potřebovat. Pojmenování pomáhá orientaci — například *Keynote*, *Panel*, *Workshop*, *Prezentace partnera*.
- Každý vlastní typ **vychází z jednoho ze čtyř základních chování** — nelze vytvořit typ, který by chování mixoval.
- Výchozí chování nastavíte jednou na úrovni typu a všechny sessions jej **automaticky přebírají**.
- Pokud máte jen pár sessions, vystačíte si se čtyřmi předvytvořenými typy.

## Detail

### Čtyři základní chování

**Přednáška.** Session je viditelná pro všechny účastníky a nevyžaduje registraci. Typické použití: keynote, plenární přednáška, celofiremní prezentace. Zobrazí se v programu, účastník na ni chodí bez přihlášení.

**Workshop.** Účastníci se **registrují na jednotlivé sessions**. K registraci jsou dostupné všechny workshopy, které jsou pro ně viditelné. Každý workshop má vlastní kapacitu. Typické použití: workshopové konference, odborné semináře, školení.

**Časové sloty.** Session má definovanou délku (například hodinu), která se rozdělí na **sloty** (například 15 minut s 5minutovou přestávkou). Účastník si **vybere jeden slot**. Typické použití: testovací jízdy aut, individuální konzultace, rezervace konkrétního času u experta. Detail v článku *Jak fungují časové sloty*.

**Přestávka.** Informativní položka **bez detailu, registrace a engagement funkcí**. V programu se zobrazí jako prostý časový blok (*Oběd*, *Coffee break*). Vyplnit lze pouze **Místo**, **Štítky** a **Poznámku organizátora**.

### Výchozí typy po vytvoření programu

Když přidáte Program, systém automaticky vytvoří **čtyři výchozí typy**: *Přednáška*, *Workshop*, *Časové sloty*, *Přestávka*. Lze je:

- **Přejmenovat** (*Přednáška* → *Keynote*).
- **Smazat** — ale pouze pokud k nim nejsou přiřazeny sessions.
- **Skrýt** — ale to skryje i všechny sessions daného typu. Jsou-li na nich registrovaní účastníci, typ skryjete až po zrušení jejich registrací.

### Vlastní typy

Vlastní typy vycházejí z jednoho ze čtyř základních chování. Rozdíl je v **pojmenování** a v **předvyplněném nastavení** — lze mít dva vlastní typy vycházející ze stejného základu, ale s jinými výchozími hodnotami.

Příklady:

- *Keynote* (základ Přednáška) — viditelné všem, prominentně v programu.
- *Panel* (základ Přednáška) — viditelné všem, ale jiná vizuální značka ve filtru.
- *Malý workshop* (základ Workshop) — kapacita 15 lidí.
- *Velký workshop* (základ Workshop) — kapacita 100 lidí.

### Vytvoření nového typu

1. Přejděte na záložku **Typy** v Programu.
2. Klikněte na **+ Nový typ**.
3. Zadejte **Název typu** (povinné).
4. Na záložce **Nastavení**:
   - **Viditelnost** — *Veřejné*, nebo *Pouze pro vybrané skupiny*.
   - **Typ** — vyberte základní chování: *Přednáška*, *Workshop*, *Časové sloty*, *Přestávka*. Po výběru se zobrazí sekce **Registrace** (u Workshopu a Časových slotů).
5. V sekci **Registrace** (zobrazuje se pro Workshop a Časové sloty) nastavte výchozí:
   - **Přiřadit účastníka do skupiny po registraci.**
   - **Registrace pouze pro vybrané skupiny.**
   - **Omezit počet registrací.**
   - **Zobrazit počet dostupných míst.**
   - **Časové omezení registrace** — od kdy a do kdy se lze přihlásit.
   - **Odhlášení ze session** — do kdy si účastník může registraci zrušit.
   - **Upozornění organizátorovi** a **účastníkovi** při změně registrace.
   - **Odeslat ICS účastníkovi.**
6. Pro **Časové sloty** navíc: **Délka časového slotu**, **Délka přestávky**.
7. Na záložce **Engagement** nastavte výchozí: **Hodnocení session**, **Otázky**, **Anonymní otázky**, **Hlasování**.
8. Uložte tlačítkem **Uložit** nebo **Uložit a publikovat**.

Pořadí kroků 4 a 5 není náhodné. Pokud u **Viditelnosti** zvolíte *Pouze pro vybrané skupiny*, nabídne **Registrace pouze pro vybrané skupiny** jen tytéž skupiny — k registraci pustíte jen někoho, kdo sessions daného typu vůbec vidí. Viditelnost proto nastavte dřív než registraci; detail v článku [Nastavení workshopů a registrace na sessions](https://help.happenee.com/cs/articles/28-nastaveni-workshopu-a-registrace-na-sessions).

### Dědičnost a přepsání

Každá nová session daného typu **automaticky dědí** všechna nastavení. U konkrétní session lze dědění **přepsat**:

1. Otevřete panel úprav session.
2. Na záložce **Informace** v sekci **Nastavení registrace** přepněte toggle z *Výchozí* na *Vlastní*.
3. Upravte pole, která se teď nastavují individuálně.

> ⚠️ **Přepnutí mezi Výchozí a Vlastní nastavením registrace není možné**, pokud je na session registrován alespoň jeden účastník. Plánujte dopředu.

Obdobně funguje přepnutí u záložky **Viditelnost** (toggle **Výchozí nastavení viditelnosti podle typu**) a u sekce **Engagement** na záložce **Obsah** session.

### Pořadí typů a jeho dopad na program

Řádky v záložce **Typy** můžete **přetažením** (za úchyt vlevo u řádku) ručně seřadit. Pořadí typů není jen kosmetické — promítne se na dvě místa, která vidí účastník:

- **Filtr Typ.** V programu na microsite, v mobilní i webové účastnické aplikaci se hodnoty filtru **Typ** zobrazují v tom pořadí, v jakém typy seřadíte v tabulce. Klíčové typy (například *Keynote*) tak dostanete na začátek filtru.
- **Sessions ve stejný čas.** Když dvě sessions začínají ve stejný čas, program je seřadí podle pořadí jejich typů — typ výš v tabulce se v programu zobrazí dřív.

Stejný princip „pořadí určíte přetažením" platí i pro **Místa** a **Štítky** a jejich filtry — viz [Jak fungují registrační bloky, místa a štítky](https://help.happenee.com/cs/articles/31-jak-funguji-registracni-bloky-mista-a-stitky).

### Změna typu session

Typ session lze **změnit** v panelu úprav session na záložce **Informace**. Pokud přecházíte na typ s jiným registračním chováním (např. z *Přednáška* na *Workshop*), nastavení registrace se změní podle výchozích hodnot nového typu. Stávající registrace účastníků tím nejsou dotčeny.

### Skrytí typu

Skrytím typu se **skryjí všechny sessions** k němu přiřazené. Sessions se nezobrazí účastníkům v aplikaci ani na microsite, dokud typ nebude opět zviditelněn.

Jsou-li na sessions daného typu registrovaní účastníci, zobrazí se při skrytí typu potvrzovací dialog s jejich počtem, a to i při hromadné změně stavu více typů. Tlačítkem **Odebrat účastníky a uložit** registrace zrušíte a typ skryjete; když dialog zavřete, změna se neuloží a registrace zůstanou. Zrušené registrace se po opětovném zveřejnění typu nevrátí. Proč to tak je a kdy účastníkům odejde e-mail, popisuje článek [Správa sessions](https://help.happenee.com/cs/articles/69-sprava-sessions).

### Smazání typu

Typ nelze smazat, pokud k němu jsou přiřazeny sessions. Nejprve přesuňte všechny sessions k jinému typu.

## Na co si dát pozor

### Změna nastavení typu se nepropíše do sessions přepnutých na *Vlastní* — organizátor očekává, že se srovnají i ty

Změna na úrovni typu se promítne do všech sessions, které dané nastavení dědí — mají u něj přepínač ve stavu **Výchozí** (včetně existujících). Sessions, u kterých jste dané nastavení přepnuli na **Vlastní**, se od typu odpojily a změnu nedostanou; ty srovnáte samostatně u jednotlivých sessions — přepnutím zpět na **Výchozí**, nebo úpravou jejich vlastních hodnot (viz [Správa sessions](https://help.happenee.com/cs/articles/69-sprava-sessions)).

### Vlastní typ vytvořen bez rozhodnutí o základním chování. Organizátor pak zjistí, že Workshop nemůže změnit na Časové sloty

Základní chování (*Přednáška* / *Workshop* / *Časové sloty* / *Přestávka*) je vlastnost typu. Pokud potřebujete jiné chování, vytvořte nový typ a sessions převeďte.

### Skrytí typu jako dočasná úschova — organizátor zjistí, že s nimi zmizely i sessions

Skrytí typu = skrytí všech sessions. Pokud chcete skrýt jen typ, ale sessions zachovat viditelné, převeďte sessions k jinému typu nebo upravte viditelnost u každé session individuálně. Pokud se na sessions daného typu už někdo zaregistroval, přijdete skrytím typu navíc o registrace.

### Vlastní typ *Keynote* vytvořen s chováním *Přednáška*, ale organizátor čeká, že bude vyžadovat registraci

Chování určuje registraci — *Přednáška* nikdy registraci nevyžaduje. Pokud chcete registraci, volte základ *Workshop* nebo *Časové sloty*. Pojmenování *Keynote* je jen interní.

### Přepínání *Výchozí ↔ Vlastní* u session s registrovanými účastníky — systém nedovolí

Pokud je potřeba změnit nastavení session, **udělejte to před spuštěním registrace**. Po registraci účastníků jsou některá nastavení zamčená.

### Pořadí typů necháno bez rozmyslu — filtr i program řadí sessions nečekaně

Pořadí typů v záložce **Typy** řídí pořadí hodnot ve filtru **Typ** i to, jak se seřadí sessions se stejným časem začátku. Pokud chcete mít nahoře klíčové typy, přetáhněte je v tabulce nahoru dřív, než program zveřejníte.

## Související články

- [Sestavení programu události — architektura](https://help.happenee.com/cs/articles/26-sestaveni-programu-udalosti-%E2%80%94-architektura)
- [Správa sessions](https://help.happenee.com/cs/articles/69-sprava-sessions)
- [Nastavení workshopů a registrace na sessions](https://help.happenee.com/cs/articles/28-nastaveni-workshopu-a-registrace-na-sessions)
- [Jak fungují časové sloty](https://help.happenee.com/cs/articles/29-jak-funguji-casove-sloty)
- [Jak fungují registrační bloky, místa a štítky](https://help.happenee.com/cs/articles/31-jak-funguji-registracni-bloky-mista-a-stitky)
- [Správa řečníků](https://help.happenee.com/cs/articles/23-sprava-recniku)
- [Nastavení rezervací v programu — auta, workshopy, doprovodný program](https://help.happenee.com/cs/articles/30-nastaveni-rezervaci-v-programu-%E2%80%94-auta-workshopy-doprovodny-program)
- [Hromadný import sessions](https://help.happenee.com/cs/articles/68-hromadny-import-sessions)
- [Nastavení engagement funkcí](https://help.happenee.com/cs/articles/97-nastaveni-engagement-funkci)

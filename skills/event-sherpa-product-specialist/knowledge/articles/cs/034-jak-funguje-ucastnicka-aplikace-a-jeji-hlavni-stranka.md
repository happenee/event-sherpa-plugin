# Jak funguje účastnická aplikace a její hlavní stránka

> Prostředí, ve kterém účastník během události žije, a jak je uspořádaná hlavní stránka aplikace.

- Článek v Help Centru: https://help.happenee.com/cs/articles/34-jak-funguje-ucastnicka-aplikace-a-jeji-hlavni-stranka
- English version: https://help.happenee.com/en/articles/34-how-the-attendee-app-and-its-home-screen-work
- Kolekce: Obsah a zkušenost účastníka
- Aktualizováno: 2026-09-16

---

> [!info] Krátce
> Účastnická aplikace je prostředí, ve kterém **účastník během události žije** — vidí program, dostává oznámení, komunikuje s ostatními, skenuje vstupenku na vstupu. Je dostupná ve třech variantách: **mobilní aplikace iOS**, **mobilní aplikace Android**, **webová aplikace** (v prohlížeči). Obsah je napříč všemi variantami stejný, jen se liší forma zobrazení. **Hlavní stránka účastnické aplikace** je úvodní obrazovka, kterou účastník vidí po otevření události — obsahuje dlaždice nejdůležitějších modulů a funkcí (Program, QR vstupenka, Moje agenda, Networking, Sponzoři, Vystavovatelé a další).

## Jak začít

- Rozhodněte, **jestli chcete účastníkovi nabídnout aplikaci** (doporučeno u středních a větších událostí) — kolekce 01 *Microsite vs účastnická aplikace*.
- Obsah hlavní stránky **se skládá z obsahových a engagement funkcí**, které jste zapnuli v události. Čím víc funkcí, tím bohatší hlavní stránka — ale i riziko přetížení.
- Pořadí obsahových a engagement funkcí na hlavní stránce nastavujete v levém menu → **Účastnická aplikace** → přetažením.
- Zobrazení konkrétní funkce na hlavní stránce lze upravit — **textový blok** vs **obrázek**.

## Detail

### Tři varianty aplikace

**Mobilní aplikace iOS / Android.** Nativní aplikace, kterou si účastník stáhne z App Store nebo Google Play. Happenee standardně publikuje pod **hlavním Happenee brandem** nebo pod **white label** brandem zákazníka (enterprise). Push notifikace fungují.

**Webová aplikace.** Otevírá se v prohlížeči — účastník nemusí nic instalovat. Odkaz dostane v e-mailu nebo najde na microsite. Push notifikace fungují omezeně (podpora browser notifikací).

> U **fyzických** událostí je dostupná mobilní + webová aplikace. U **virtuálních** pouze webová. U **hybridních** obě. Nastavuje se při vytvoření události (*Typ události*).

### Hlavní stránka účastnické aplikace

Hlavní stránka je úvodní obrazovka, kterou účastník vidí po otevření konkrétní události v aplikaci. Obsahuje **seznam funkcí — dlaždic** s náhledem každé obsahové a engagement funkce. Typicky:

- **QR vstupenka** (engagement) — QR kód pro check-in.
- **Program** (obsahová) — nejbližší sessions.
- **Moje agenda** (engagement) — sessions, které si účastník uložil nebo na které je registrovaný. Ve webové aplikaci se zobrazí nad dlaždicí Programu, jen když ji zapnete na záložce **Moje agenda** v Programu; v mobilní aplikaci je nad prvním Programem vždy.
- **Networking / Účastníci** (engagement) — seznam ostatních účastníků.
- **Sponzoři / Vystavovatelé** (obsahové) — loga a filtry.
- **Oznámení** (engagement) — novinky a push zprávy.
- **Lokalita** (obsahová) — adresa a mapa.
- **Kontakt** (obsahová) — kontakt na organizátora.
- **Vlastní obsah** (obsahová) — FAQ, parkování, dress code.
- **Leaderboard**, **Online modul** (pokud aktivní).

### Dvě vrstvy konfigurace hlavní stránky

**Vrstva 1 — co na hlavní stránce je.** Zapnuté obsahové a engagement funkce se automaticky objeví na hlavní stránce. Co není zapnuté, se nezobrazí.

**Vrstva 2 — jak konkrétní funkce vypadá.** U každé funkce (obsahové i engagement) lze zvolit zobrazení na hlavní stránce:

- **Textový blok** — nadpis + krátký úvodní text. Například *„Vlastní obsah: Parkování a doprava“*.
- **Obrázek** — nahradí textový náhled obrázkem. Nahraje se samostatně pro **mobilní** a **web** zobrazení (rozměry se liší).

Obrázek je silnější vizuál, ale vyžaduje kvalitní grafiku. Pokud nemáte, nechte textový blok.

### Pořadí modulů a funkcí

V **Účastnická aplikace** (levé menu události) je seznam zapnutých funkcí. Přetáhněte za ikonu vlevo a uspořádejte. Účastník uvidí funkce v nastaveném pořadí.

**Doporučené pořadí pro většinu událostí:**

1. QR vstupenka (rychlý přístup pro check-in)
2. Program (hlavní obsah; blok Moje agenda nemá vlastní pořadí a zobrazuje se nad ním)
3. Oznámení (aktuality)
4. Networking (interakce)
5. Lokalita (praktické info)
6. Sponzoři / Vystavovatelé
7. Další

### Viditelnost pro skupiny

Viditelnost jednotlivých funkcí pro skupiny se nastavuje na úrovni **každé obsahové a engagement funkce** (viz *Práce se skupinami a viditelností*), ne v sekci Účastnická aplikace. V sekci Účastnická aplikace nastavujete jen **pořadí** a **publikaci** (zapnuto/vypnuto v aplikaci).

### Co účastník potřebuje pro přístup

1. **Stav registrace: Zúčastním se** (nebo přiřazení k události bez registrace, pokud je *Bez nutnosti registračního formuláře*).
2. **Přihlášení** v aplikaci — e-mailem a kódem nebo Magic Linkem.
3. **Staženou aplikaci** (mobilní) nebo otevřenou webovou verzi.

Pokud účastník nemá staženou nativní mobilní aplikaci, nabídněte odkaz na webovou — někdy účastníci nativní aplikaci nestahují.

### White label aplikace

Enterprise zákazníci mohou mít vlastní mobilní aplikaci v App Store a Google Play pod jménem své organizace. Obsahově je stejná, ale vizuálně brandovaná. Nastavuje se při setupu enterprise účtu, ne v běžné administraci události.

### Rozdíl oproti microsite

- **Microsite** — veřejná stránka pro **před-registrační fázi** a marketingové sdílení. Účastník ji otevře z e-mailu nebo odkazu, vidí program, řečníky, sponzory, registrační tlačítko.
- **Účastnická aplikace** — prostředí pro **účastníky po registraci**. Hlavní stránka účastnické aplikace obsahuje personalizovaný pohled (Moje agenda, vstupenka), který microsite nemá.

Obsah mezi microsite a aplikací je v Happenee **sdílený** — obsahové funkce vyplňujete jednou, pak rozhodujete, kde se zobrazí. Detail v článku *Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka*.

### Přejmenování funkcí

V detailu obsahové nebo engagement funkce lze funkci **přejmenovat** — výchozí název *Vlastní obsah*, *Sponzoři* atd. změnit na cokoliv. Název se propíše do hlavní stránky.

## Na co si dát pozor

### Hlavní stránka přeplněná 15 funkcemi. Účastník se v ní neorientuje

Zapínejte jen funkce, které naplňujete obsahem. Pro střední události stačí 6–8 funkcí. Prázdné dlaždice působí nedokončeně.

### Obrázek pro hlavní stránku nahrán jen pro desktop. Mobilní aplikace zobrazí prázdnou dlaždici nebo defaultní pohled

Obrázek nahrajte pro **obě varianty** — mobilní (menší rozměr) a desktop / web. Pokud jen jeden, druhý zůstane v defaultu.

### Účastník se nemůže přihlásit do aplikace. Zkouší e-mail, ale systém ho nenajde

Zkontrolujte, zda je účastník ve stavu **Zúčastním se** u dané události. Pokud je ve stavu *Bez odpovědi* nebo *Nezúčastním se*, nemá přístup do aplikace. U otevřených událostí ověřte, zda je ve správě kontaktů.

### Organizátor změní pořadí funkcí v průběhu události. Účastníci zmatení

Pořadí funkcí nastavte před spuštěním události a neměňte v jejím průběhu. Výjimka: pokud je změna nutná (funkce přestala mít smysl), komunikujte ji v Oznámení.

### Snaha dostat do aplikace obsah, který v Happenee není obsahovou ani engagement funkcí (například externí stránka s materiály)

Použijte **Vlastní obsah** s externím odkazem — na hlavní stránce se zobrazí dlaždice, po kliknutí se otevře externí URL. Pro soubory (PDF) lze použít centrální úložiště **Soubory** v Nastavení workspace.

### White label aplikace v App Store, ale účastník stahuje hlavní Happenee aplikaci — nevidí brand

U enterprise událostí komunikujte přesný odkaz na white label aplikaci (obvykle pod specifickým jménem v App Store). V e-mailech a na microsite odkazujte přímo na ni.

## Související články

- [Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka](https://help.happenee.com/cs/articles/5-microsite-vs-ucastnicka-aplikace-jak-premyslet-nad-flow-ucastnika)
- [Jak funguje microsite události](https://help.happenee.com/cs/articles/21-jak-funguje-microsite-udalosti)
- [Použití vlastního obsahu (FAQ, mapa, informační bloky)](https://help.happenee.com/cs/articles/25-pouziti-vlastniho-obsahu-faq-mapa-informacni-bloky)
- [Správa sponzorů](https://help.happenee.com/cs/articles/32-sprava-sponzoru)
- [Správa vystavovatelů](https://help.happenee.com/cs/articles/33-sprava-vystavovatelu)
- [Jak funguje Moje agenda](https://help.happenee.com/cs/articles/35-jak-funguje-moje-agenda)
- [Jak funguje Networking](https://help.happenee.com/cs/articles/36-jak-funguje-networking)
- [Jak funguje Leaderboard](https://help.happenee.com/cs/articles/37-jak-funguje-leaderboard)
- [Použití Online modulu](https://help.happenee.com/cs/articles/38-pouziti-online-modulu)
- [Cesta účastníka z microsite do účastnické aplikace](https://help.happenee.com/cs/articles/45-cesta-ucastnika-z-microsite-do-ucastnicke-aplikace)
- [Používání oznámení v účastnické aplikaci](https://help.happenee.com/cs/articles/46-pouzivani-oznameni-v-ucastnicke-aplikaci)
- [Jak funguje check-in a skenování QR kódů](https://help.happenee.com/cs/articles/47-jak-funguje-check-in-a-skenovani-qr-kodu)
- [Doporučený setup pro interní firemní event](https://help.happenee.com/cs/articles/53-doporuceny-setup-pro-interni-firemni-event)
- [Doporučený setup pro externí klientský event](https://help.happenee.com/cs/articles/54-doporuceny-setup-pro-externi-klientsky-event)
- [Doporučený setup pro konferenci](https://help.happenee.com/cs/articles/55-doporuceny-setup-pro-konferenci)
- [Doporučený setup pro expo / veletrh](https://help.happenee.com/cs/articles/56-doporuceny-setup-pro-expo-veletrh)
- [Doporučený setup pro incentive / itinerář](https://help.happenee.com/cs/articles/57-doporuceny-setup-pro-incentive-itinerar)
- [Co dělat při problému na check-inu](https://help.happenee.com/cs/articles/62-co-delat-pri-problemu-na-check-inu)
- [Co dělat, když se účastník nedostane do aplikace](https://help.happenee.com/cs/articles/93-co-delat-kdyz-se-ucastnik-nedostane-do-aplikace)
- [Nastavení engagement funkcí](https://help.happenee.com/cs/articles/97-nastaveni-engagement-funkci)

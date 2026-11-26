# Co nastavit jako první po vytvoření eventu

> Doporučené pořadí prvních kroků po vytvoření eventu, hlavně rozhodnutí, která už nepřepíšete.

- Článek v Help Centru: https://help.happenee.com/cs/articles/3-co-nastavit-jako-prvni-po-vytvoreni-eventu
- English version: https://help.happenee.com/en/articles/3-what-to-set-up-first-after-creating-an-event
- Kolekce: Začínáme s Happenee
- Aktualizováno: 2026-09-09

---

> [!info] Krátce
> Po vytvoření nového eventu vás čeká řada rozhodnutí, která ovlivní zbytek práce. Některá z nich ex post nelze změnit — typicky primární jazyk — jiná se dají upravovat, ale stojí tím zpětnou práci. Tento článek vás provede doporučeným pořadím prvních kroků, abyste měli jistotu, že se později nebudete vracet k základům.

## Jak začít

- Vyplňte základní informace eventu (název, čas, typ, jazyky) při jeho vytváření.
- Hned potvrďte primární jazyk — ex post se nemění bez založení nové události.
- Rozhodněte o typu registrace a viditelnosti události, než do ní zveřejníte odkaz.
- Naplánujte skupiny a kategorie účastníků dopředu, ne až při problémech.
- Teprve potom vyplňujte obsahové a engagement funkce.

## Detail

### 1. Základní informace eventu

Při zakládání eventu vyplňujete:

- **Název události** a ikonu (lze doplnit později).
- **Časové pásmo** — nastaví se automaticky podle prohlížeče, ale ověřte ho.
- **Začátek a konec události.**
- **Typ události** — Fyzická / Virtuální / Hybridní. Fyzický event umožňuje účastníkovi přístup do mobilní i webové aplikace, virtuální jen do webové, hybridní do obou.
- **Primární jazyk.**

### 2. Primární jazyk

Primární jazyk je záložní jazyk eventu. Když účastník otevře microsite nebo aplikaci s nastavením zařízení v jazyce, který event nemá explicitně přidaný, zobrazí se obsah v primárním jazyce.

Pokud máte například dva obsahové jazyky — češtinu a angličtinu — a očekáváte zahraniční hosty s nastavením zařízení v němčině, španělštině nebo jiných jazycích, primární jazyk by měl být **angličtina**. Jinak se jim zobrazí čeština. Pokud má událost zahraniční účastníky, prakticky vždy doporučujeme nastavit jako primární angličtinu.

> Primární jazyk se nastavuje při zakládání eventu a nelze ho později změnit bez založení nové události. Jde o jedno z mála rozhodnutí v Happenee, které je skutečně nevratné. Věnujte mu pozornost.

### 3. Rozhodnutí o typu registrace

Ještě než otevřete registraci, rozhodněte:

- **Veřejná vs uzavřená registrace** — budete sdílet veřejný odkaz, nebo pozvete účastníky osobním odkazem? Veřejný odkaz se může šířit k cizím lidem, osobní drží kontrolu.
- **Omezení na doménu** — chcete povolit registraci jen lidem z konkrétní firemní domény? Nastavení povolených nebo zakázaných domén vyžaduje zákaznickou podporu.
- **Nominace** — chcete, aby registrace šly přes nominátory (například obchodní tým, který zve své klienty)?
- **Schvalování** — potřebujete registrace manuálně schvalovat, než se účastník dostane do eventu? **Pozor:** schvalování lze nastavit pouze u neplacených událostí.
- **Automatická registrace po nákupu vs Registrace s doplněním informací** — potvrdí se registrace ihned, nebo potřebujete od účastníka doplnit informace ve formuláři?

Každá z těchto voleb ovlivňuje flow i správu registrací. Rozhodnout je před spuštěním je mnohem jednodušší než opravovat později.

### 4. Viditelnost a přístup do události v aplikaci

Kromě typu registrace má event dvě důležitá nastavení, která rozhodují, co uvidí účastník v účastnické aplikaci:

- **Viditelnost události v aplikaci** — buď pouze pro přizvané kontakty (výchozí), nebo pro všechny kontakty ve workspace. Druhá varianta se hodí u interních firemních událostí, kde chcete, aby všichni kolegové viděli nabídku událostí, i kdyby je organizátor explicitně nepozval.
- **Přístup do události v aplikaci** — buď pouze po vyplnění registračního formuláře (výchozí), nebo bez nutnosti formuláře (klik na událost = rovnou stav Zúčastním se). Druhá varianta je užitečná u interních událostí, kde nechcete nutit kolegy vyplňovat cokoliv.

Kombinace těchto dvou nastavení s omezením registrace dává flexibilitu pro různé typy událostí — od přísně invitation-only po zcela otevřené firemní události.

### 5. Omezení registrace

V nastavení přístupu a registrace lze zvolit:

- **Bez omezení** — registrovat se může kdokoli s odkazem.
- **Pouze pro přiřazené kontakty** — i když máte veřejný odkaz na microsite, registrovat se smějí jen kontakty předem přiřazené k události.
- **Pouze povolené domény** — registrace jen z vybraných firemních domén (nastavuje zákaznická podpora).
- **Blokovat registraci ze specifických domén** — naopak blokuje registrace z vybraných domén (nastavuje zákaznická podpora).
- **Výchozí nastavení účtu (workspace)** — globální omezení platné pro všechny eventy workspace (nastavuje zákaznická podpora).

Lze také nastavit maximální počet účastníků, deadline pro registraci i možnost odhlášení.

### 6. Skupiny a kategorizace účastníků

Skupiny jsou jeden z nejpodceňovanějších nástrojů v Happenee. Slouží k:

- **Cílení komunikace** — rozlišení, komu pošlete který e-mail.
- **Řízení viditelnosti** — která skupina uvidí kterou obsahovou nebo engagement funkci.
- **Podmíněným otázkám v registračním formuláři** — například otázka o stravování se zobrazí jen VIP účastníkům.
- **Reportování** — filtrování statistik podle skupiny (například „kolik lidí z nominace kolegy Nováka přišlo“).

Platí jednoduché pravidlo: **skupiny, které chcete využít, je potřeba naplánovat dopředu**. Když účastník prochází registrací, jeho zařazení do skupiny se řídí tím, co zvolí ve formuláři — a to musí být nastavené. Ex post přiřazování skupin funguje hromadně, ale je to ruční práce navíc.

### 7. Obsahové funkce

Obsahové funkce najdete v sekci **Obsah**. Tvoří informační základ události a zobrazují se jak na microsite, tak v účastnické aplikaci (kde je to relevantní):

- Program
- Řečníci
- Lokalita
- Kontakt
- Vlastní obsah (libovolný text, obrázky, FAQ, mapa, informační blok)
- Sponzoři
- Vystavovatelé

Přidáte je tlačítkem **+ Přidat** a postupně vyplníte. U každé obsahové funkce rozhodujete, zda se zobrazí na microsite, v aplikaci, nebo na obou místech.

### 8. Engagement funkce

Engagement funkce slouží k aktivnímu zapojení účastníka v aplikaci:

- QR vstupenka (engagement funkce; modulová role je **Placené vstupenky**)
- Oznámení (push notifikace a novinky v news feedu)
- Hlasování (interaktivní ankety a soutěže)
- Otázky z publika
- Dotazník (zpětná vazba)
- Networking a schůzky mezi účastníky
- Registrační údaje (přehled toho, co účastník vyplnil v registračním formuláři)
- Online modul (živé přenosy, 3D prostředí, doplňkový obsah)

Ne každý event potřebuje všechny engagement funkce. Zapínejte jen ty, které dává smysl využít. Zapnuté a prázdné funkce působí hůř než jejich absence.

### 9. Microsite a aplikace — kde se co zobrazí

Každá obsahová nebo engagement funkce má vlastní přepínače zobrazení. Typicky lze nastavit:

- Zobrazit v aplikaci ano/ne
- Zobrazit na microsite ano/ne
- Zobrazit pouze vybraným skupinám (viditelnost)

To znamená, že obsah vyplňujete jednou a jeho cílení řídíte odděleně.

## Na co si dát pozor

### Primární jazyk se nastaví bez rozmyslu, teprve v průběhu přípravy si organizátor uvědomí, že tam budou zahraniční hosté

Pokud má událost zahraniční účastníky, primární jazyk = angličtina. Tohle rozhodnutí udělejte při zakládání, ne až se zveřejňuje registrace — ex post to nejde změnit.

### Skupiny se vytvářejí až v momentě, kdy už běží registrace a organizátor zjistí, že chce cílit komunikaci

Naplánujte strukturu skupin před spuštěním registrace. Zamyslete se, koho budete chtít odlišit (VIP, standardní, speakeři, partneři, klientské skupiny) a skupiny založte předem — ať je může registrační formulář automaticky přiřazovat.

### Zapnutí všech obsahových a engagement funkcí „pro jistotu“, i když v nich nejsou data

Prázdné funkce působí nedokončeně. Zapínejte jen ty, které budete naplňovat. U menších událostí je méně vždy lepší.

### Vytvoření eventu bez rozhodnutí o typu registrace, se spoléháním, že „to později upravíme“

Typ registrace (veřejná, uzavřená, nominovaná, schvalovaná) určete předtím, než zveřejníte jakýkoli odkaz. Změny v běhu vytvářejí chaos v datech účastníků.

## Související články

- [Co je workspace a co je event](https://help.happenee.com/cs/articles/1-co-je-workspace-a-co-je-event)
- [Orientace v administraci Happenee](https://help.happenee.com/cs/articles/2-orientace-v-administraci-happenee)
- [Vytvoření nové události](https://help.happenee.com/cs/articles/9-vytvoreni-nove-udalosti)
- [Nastavení primárního jazyka události](https://help.happenee.com/cs/articles/10-nastaveni-primarniho-jazyka-udalosti)
- [Výběr správného typu registrace](https://help.happenee.com/cs/articles/4-vyber-spravneho-typu-registrace)
- [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti)
- [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace)
- [Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka](https://help.happenee.com/cs/articles/5-microsite-vs-ucastnicka-aplikace-jak-premyslet-nad-flow-ucastnika)
- [Must-have, optional a advanced funkce a moduly podle typu události](https://help.happenee.com/cs/articles/6-must-have-optional-a-advanced-funkce-a-moduly-podle-typu-udalosti)
- [Doporučené pořadí setupu eventu krok za krokem](https://help.happenee.com/cs/articles/8-doporucene-poradi-setupu-eventu-krok-za-krokem)
- [Doporučený setup pro interní firemní event](https://help.happenee.com/cs/articles/53-doporuceny-setup-pro-interni-firemni-event)

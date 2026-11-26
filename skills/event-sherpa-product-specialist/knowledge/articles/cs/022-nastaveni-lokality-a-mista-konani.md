# Nastavení lokality a místa konání

> Obsahová funkce, která účastníkům ukazuje, kde se událost koná, s mapou a navigací.

- Článek v Help Centru: https://help.happenee.com/cs/articles/22-nastaveni-lokality-a-mista-konani
- English version: https://help.happenee.com/en/articles/22-setting-up-venue-and-the-event-location
- Kolekce: Obsah a zkušenost účastníka
- Aktualizováno: 2026-09-18

---

> [!info] Krátce
> Lokalita je **obsahová funkce**, která účastníkům ukazuje, **kde se událost koná**. Obsahuje název místa, adresu, mapu a volitelně obrázek a popis. Zobrazuje se na microsite události i v účastnické aplikaci; v mobilní aplikaci účastník spustí navigaci tlačítkem **Navigovat** na dlaždici Lokality. Nepleťte si Lokalitu s **Místy** uvnitř programu — Místa jsou jednotlivé sály a stánky, Lokalita je adresa celé události.

## Jak začít

- Připravte si **přesnou adresu** místa konání (ne jen název areálu).
- Pokud má událost víc budov nebo hal, zvažte, zda o nich informovat v Lokalitě (textově), nebo využít **Místa v programu** (pro sessions).
- Připravte si kontaktní údaje k místu (telefon na recepci, web) — jsou volitelné, ale pomáhají účastníkům.
- Obrázek lokality je volitelný, ale zlepšuje orientaci.

## Detail

### Kde se Lokalita nastavuje

1. V levém menu klikněte na **Obsah**.
2. Pokud tam Lokalitu ještě nemáte, přidejte ji tlačítkem **+ Přidat** → **Lokalita**.
3. Klikněte na záložku **Lokalita** a vyplňte pole:

- **Název místa** — například *Kongresové centrum Praha*, *O2 arena*, *Hotel Corinthia*.
- **Telefon** (volitelný) — kontakt na recepci místa.
- **Webové stránky** (volitelné) — odkaz na web místa.
- **Adresa** — zadejte a **vyhledejte**. Happenee převede adresu na souřadnice a zobrazí mapu.
- **Obrázek lokality** (volitelný).
- **Popis lokality** — text v rich text editoru. Dopravní informace, parkování, jak se dostat, zvláštní upozornění.

### Jak to účastník vidí

**Na microsite události** — záložka Lokalita obsahuje adresu, mapu (Google Maps embed) a popis. Kliknutím na adresu nebo mapu se účastníkovi otevře navigace v mapové aplikaci.

**V mobilní účastnické aplikaci** — klepnutím na dlaždici Lokality na hlavní stránce, včetně adresy nebo náhledu mapy, účastník otevře detail lokality. Tlačítkem **Navigovat** otevře externí mapovou aplikaci s trasou na místo konání. Tlačítko je na dlaždici i v detailu lokality.

Pokud dlaždice zobrazuje mapu a aplikace má k dispozici polohu účastníka, náhled zahrne účastníka i místo konání, případně dostupnou trasu. Čím dál účastník od místa je, tím větší oblast mapa ukazuje. Bez dostupné polohy zobrazí okolí místa konání.

Čas a vzdálenost se zobrazují jen při dostupném výpočtu trasy. Pokud aplikace polohu zná, ale trasu nezíská, mapa ukáže oba body bez trasy a odhadu cesty. Samotné povolení přístupu k poloze proto nezaručuje, že se trasa zobrazí. Náhled neslouží k průběžné navigaci; tu účastník spustí tlačítkem **Navigovat**.

Má-li Lokalita nastavený vlastní obrázek pro hlavní stránku, dlaždice zobrazí jen tento obrázek — bez adresy, mapy a tlačítka **Navigovat**. Klepnutím na obrázek účastník otevře detail lokality a navigaci spustí až tam.

### Vícejazyčnost

Přepínačem jazyků (vlajky v pravém horním rohu) můžete přeložit:

- Název místa
- Popis lokality

Adresa jako taková se nepřekládá — je jedna pro všechny jazyky. Pokud je potřeba přidat překlad pro jiný zápis (například česky/anglicky u zahraničního místa), doplňte ho do **popisu**.

### Rozdíl mezi Lokalitou a Místy v programu

- **Lokalita** (obsahová funkce) = adresa celé události. Jedna na událost. Zobrazuje se jako samostatná záložka na microsite i v aplikaci.
- **Místa v programu** (nastavení uvnitř Programu) = jednotlivé sály, stage nebo stánky, ke kterým se přiřazují konkrétní sessions. Slouží jako filtr. Detail v článku *Jak fungují registrační bloky, místa a štítky*.

U jednodenní události v jednom sále stačí Lokalita. U konference s více paralelními sessions ve více sálech používejte **obojí** — Lokalita = adresa kongresového centra, Místa = jednotlivé sály.

### Viditelnost

Lokalitu lze:

- **Zobrazit všem účastníkům** (výchozí).
- **Zobrazit pouze vybraným skupinám** — např. když část účastníků má jiné místo konání (VIP galavečer na jiné adrese). V takovém případě je ale obvykle lepší vytvořit samostatnou událost.

### Kdy Lokalitu nepotřebujete

- **Virtuální události** — místo konání neexistuje. Lokalitu jednoduše nepřidávejte.
- **Incentive / itinerář s více stanovišti** — událost prochází víc lokalitami. Použijte místo toho **Vlastní obsah** s vlastnoručně vyrobeným přehledem stanovišť, nebo Program jako itinerář.

## Na co si dát pozor

### Zadán jen název areálu bez adresy. Účastníkovi se v mapové aplikaci zobrazí jiné místo s podobným názvem, nebo se nic nenajde

Vždy vyplňte přesnou adresu včetně ulice a čísla popisného. Po zadání klikněte na **Vyhledat** a zkontrolujte, zda systém našel správné místo.

### Organizátor nahraje obrázek areálu z webu místa v nízkém rozlišení — na microsite vypadá špatně

Obrázek lokality by měl být minimálně 1200×600 px, formát JPG nebo PNG. Pokud nemáte vlastní, raději nechte prázdné.

### Popis lokality obsahuje aktuální informace (parkování, rozvoz), které se změní týden před událostí — pak už je pozdě aktualizovat

Informace, které se mění, zveřejňujte přes **Oznámení** v účastnické aplikaci, ne ve statickém popisu lokality.

### Více budov v areálu, popis lokality obsahuje jen adresu hlavní budovy. Účastníci se ztrácejí

V popisu lokality uveďte, **kam přesně jít** (vchod A, budova 3, přízemí). Pro konferenci s více sály používejte navíc **Místa** v programu.

### Organizátor nastavuje lokalitu pro virtuální událost. Účastníkům se zobrazuje nesmyslná adresa

U virtuálních událostí obsahovou funkci Lokalita **vůbec nepřidávejte**. Odkaz na livestream nebo online místo dejte do **Vlastního obsahu** nebo do **Online modulu**.

## Související články

- [Jak funguje microsite události](https://help.happenee.com/cs/articles/21-jak-funguje-microsite-udalosti)
- [Přidání kontaktní osoby organizátora](https://help.happenee.com/cs/articles/24-pridani-kontaktni-osoby-organizatora)
- [Použití vlastního obsahu (FAQ, mapa, informační bloky)](https://help.happenee.com/cs/articles/25-pouziti-vlastniho-obsahu-faq-mapa-informacni-bloky)
- [Sestavení programu události — architektura](https://help.happenee.com/cs/articles/26-sestaveni-programu-udalosti-%E2%80%94-architektura)
- [Jak fungují registrační bloky, místa a štítky](https://help.happenee.com/cs/articles/31-jak-funguji-registracni-bloky-mista-a-stitky)
- [Doporučený setup pro incentive / itinerář](https://help.happenee.com/cs/articles/57-doporuceny-setup-pro-incentive-itinerar)

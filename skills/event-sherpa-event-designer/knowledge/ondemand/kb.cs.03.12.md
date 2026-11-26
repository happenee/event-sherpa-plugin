<!-- source: kb.cs.03.12 -->

---
title: "Správa sponzorů"
description: "Obsahová funkce pro zobrazení partnerů události s jejich logy v kategoriích podle prominence."
modules: ["sponzori_a_vystavovatele"]
last_updated: "2026-09-02"
version: 3
---

> [!info] Krátce
> Sponzoři je **obsahová funkce**, která zobrazí partnery události s jejich logy na microsite i v účastnické aplikaci. Každý sponzor patří do **kategorie** (Generální sponzor, Zlatý, Stříbrný) — kategorie určuje prominenci a kolik log se zobrazí v jednom řádku. Po kliknutí na logo lze otevřít **externí web sponzora**, **profil sponzora** (popis, kontakty, sociální sítě), nebo **nic**. Sponzory lze navíc přiřadit k sessions v programu.

## Jak začít

- Zmapujte si **strukturu sponzorství** — jaké máte úrovně (Generální / Zlatý / Stříbrný / Mediální) a jaké benefity každá úroveň má (počet log v řadě, prominence, přiřazení k sessions).
- Připravte si **loga sponzorů** v jednotném formátu (PNG / JPEG / GIF, poměr 16:9, max. 500 KB).
- Rozhodněte o **události po kliknutí** — externí web, profil v aplikaci, nebo bez události.
- Rozhodněte, kde se kategorie zobrazí — **na hlavní stránce microsite / účastnické aplikace**, nebo jen v sekci Sponzoři.

## Detail

### Přidání obsahové funkce Sponzoři

1. V levém menu → **Obsah** → **+ Přidat** → **Sponzoři**.
2. Obsahová funkce se přidá a zpřístupní se záložky **Sponzoři**, **Kategorie**, **Nastavení** a **Import**.

> Obsahovou funkci Sponzoři lze přidat **vícekrát**. Každá instance má vlastní sponzory, kategorie a nastavení. Vhodné pro separátní sekce: *Partneři konference* vs *Mediální partneři*.

### Kategorie jsou povinné

Každý sponzor **musí patřit do kategorie**. Bez kategorie ho nelze uložit. Při prvním otevření záložky **Kategorie** jsou **předvyplněny čtyři výchozí kategorie**: *Generální sponzor*, *Zlatí sponzoři*, *Stříbrní sponzoři*, *Mediální sponzoři*. Lze je upravit, skrýt nebo smazat (pokud neobsahují sponzory).

### Vytvoření kategorie

1. Na záložce **Kategorie** klikněte na **Nová kategorie**.
2. Zadejte **Název kategorie**.
3. V poli **Úroveň zobrazení** vyberte **1**, **2** nebo **4** — počet log v jednom řádku. Kategorie s úrovní 1 má nejvyšší prominenci (jedno velké logo), kategorie s úrovní 4 menší loga.
4. Přepínačem **Zobrazení na homepage microsite a účastnické aplikace** nastavte, zda se kategorie zobrazí na hlavní stránce, nebo pouze v sekci Sponzoři.
5. Uložte.

**Řazení kategorií:** pořadí je dáno hodnotou **Úroveň zobrazení**. Úroveň 1 = první v pořadí, úroveň 4 = poslední. Pro jemnější kontrolu pořadí musíte kategorie pojmenovat tak, aby se mezi sebou rozlišovaly úrovní.

### Vytvoření sponzora

1. Na záložce **Sponzoři** klikněte na **Nový sponzor**.
2. Zadejte **Název sponzora**.
3. Vyberte **Kategorii** (povinné).
4. V sekci **Akce po kliknutí na logo** vyberte:
   - **Webové stránky sponzora** — po kliknutí účastník přejde na externí web. Zobrazí se pole **Webové stránky** (URL musí začínat `https://`).
   - **Profil sponzora** — otevře profil uvnitř platformy. Vyplňte **Popis sponzora**, **Webové stránky**, **E-mail**, **Telefon**, volitelně sociální sítě (**LinkedIn**, **Twitter/X**, **Instagram**, **Facebook**, **YouTube**).
   - **Bez události** — kliknutí na logo neprovede nic (čistě vizuální zobrazení).
5. Volitelně nahrajte **Logo** (PNG, JPEG nebo GIF, poměr stran 16:9, max. 500 KB).
6. Uložte.

### Stavy

**Sponzor:**
- **Publikováno** — zobrazí se v seznamu sponzorů.
- **Skryto** — nezobrazí se nikde.

**Kategorie:**
- **Publikováno** — sponzoři v ní jsou viditelní.
- **Skryto** — všichni sponzoři v kategorii jsou skryti.

> Sponzor se zobrazí účastníkům pouze tehdy, pokud jsou **oba** — sponzor i jeho kategorie — ve stavu **Publikováno**.

### Přiřazení k sessions

Ke každému sponzorovi lze přiřadit sessions, u nichž se zobrazí jeho logo s titulkem (výchozí: *Sponzoruje*; lze změnit v **Nastavení → Titulek u loga sponzora**).

1. Otevřete úpravu sponzora, záložka **Sessions**.
2. Do pole **Hledat sessions** zadejte název.
3. Klikněte na **+** u požadované session.
4. Uložte.

> Záložka Sessions je dostupná jen tehdy, pokud je v události aktivní obsahová funkce **Program** (Sessions je její záložka).

### Nastavení zobrazení

Na záložce **Nastavení** lze nastavit:

- **Zobrazení sponzorů v programu** — titulek u loga (výchozí: *Sponzoruje*).
- **Zobrazení na hlavní stránce účastnické aplikace** — *Základní zobrazení* (loga v mřížce), nebo *Obrázek* (JPG banner, 1250×300 web / 800×300 mobil, max. 500 KB). **Zarovnání log**: vlevo / na střed.
- **Zobrazení na hlavní stránce microsite** — *Základní zobrazení*, nebo *Zobrazení z hlavní stránky účastnické aplikace* (převezme nastavení z aplikace). **Zarovnání log**: vlevo / na střed.
- **Zobrazení v detailu** — zarovnání log na detailu stránky sponzora: vlevo / na střed.

### Hromadné akce

Na záložce Sponzoři vyberte víc sponzorů a použijte:

- **Kategorie** — hromadná změna kategorie.
- **Stav** — hromadné publikování nebo skrytí.
- **Smazat sponzora** — hromadné smazání.

### Filtrování v administraci vs. v aplikaci

V administraci Sponzorů lze seznam filtrovat pomocí rozbalovacích nabídek **Kategorie** a **Stav** — ale **pouze pro interní správu**. V účastnické aplikaci a na microsite **sponzoři filtrovatelní nejsou** (na rozdíl od Vystavovatelů, kde kategorie, místa a štítky slouží jako filtry pro účastníky). Účastník vidí sponzory seřazené podle kategorií v pořadí daném jejich *Úrovní zobrazení*.

### Vícejazyčnost

Přepínačem jazyků lze přeložit:

- Popis sponzora (v profilu)
- Název kategorie
- Titulek u loga sponzora

Název sponzora typicky nepřekládáme (jde o název firmy).

## Na co si dát pozor

### Sponzor přidán bez kategorie — systém neuloží

Nejprve vytvořte kategorii (nebo použijte některou z výchozích), pak sponzora přidejte.

### Sponzor má stav Publikováno, ale kategorie je skrytá. V aplikaci se nezobrazuje

Pro zobrazení musí být **oba** ve stavu Publikováno. Zkontrolujte stav kategorie.

### URL bez `https://` prefixu — odkaz v aplikaci nefunguje

Vždy začínejte `https://`. Bez prefixu systém nepřesměruje.

### Logo v nízkém rozlišení — na velkém displeji vypadá rozmazaně

Nahrajte logo alespoň v rozměru 800×450 px (poměr 16:9). U log s plochými barvami a textem zvolte PNG — JPEG přidává na hranách kompresní artefakty.

### Všechny kategorie zapnuté na *Zobrazení na homepage* — hlavní stránka je přeplněná logy

Na hlavní stránce mějte **jen nejvyšší 1–2 kategorie** (Generální, Zlatý). Ostatní nechte dostupné v sekci Sponzoři přes kliknutí.

### Záložka Sessions u sponzora chybí — sekce Sessions/Program ještě není aktivní

Přidejte obsahovou funkci **Program** do události a vytvořte alespoň jednu session. Záložka se zpřístupní.

### Pořadí sponzorů v rámci kategorie není takové, jaké organizátor chce — systém řadí ručně nastaveným pořadím

Na záložce Sponzoři přetáhněte sponzory za ikonu vlevo do správného pořadí. Pořadí se respektuje v aplikaci i na microsite.

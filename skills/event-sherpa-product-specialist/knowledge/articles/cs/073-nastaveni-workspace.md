# Nastavení workspace

> Co všechno se nastavuje na úrovni workspace — účet a dvoufázové ověření, informace o společnosti, patička e-mailu a microsite, vlastní pole kontaktů, GDPR, soubory, integrace a faktury.

- Článek v Help Centru: https://help.happenee.com/cs/articles/73-nastaveni-workspace
- English version: https://help.happenee.com/en/articles/73-setting-up-the-workspace
- Kolekce: Začínáme s Happenee
- Aktualizováno: 2026-08-16

---

> [!info] Krátce
> **Nastavení workspace** je jediné místo, kde se nastavují věci platné pro **všechny vaše události najednou** — váš uživatelský účet, informace o společnosti, výchozí patička e-mailu a microsite, vlastní pole kontaktů, ochrana osobních údajů a napojení na externí systémy; sdílené **Soubory** a přehled **Faktur** mají v levém menu vlastní položky. Nastavíte je jednou před první událostí a pak se k nim vracíte jen výjimečně. Část z nich ale nemůžete změnit sami — mění je zákaznická podpora, takže s nimi počítejte s předstihem.

## Jak začít

Do nastavení se dostanete z levého menu na úrovni workspace, kde je pět položek: **Události**, **Správa kontaktů a skupin**, **Nastavení workspace**, **Soubory** a **Faktury**. Samotné Nastavení workspace má čtyři záložky: **Uživatelský účet**, **Vlastní pole kontaktů**, **Ochrana osobních údajů** a **Integrace**.

Doporučené pořadí, než založíte první událost:

1. **Uživatelský účet** — zkontrolujte jméno, jazyk administrace a zapněte dvoufázové ověření.
2. **Informace o společnosti** — pokud nesedí, napište zákaznické podpoře; sami je nezměníte.
3. **Patička e-mailu a microsite** — výchozí text, který se propíše do všech událostí.
4. **Vlastní pole kontaktů** — jestli budete u kontaktů evidovat něco navíc, založte pole teď. Později se dají doplnit, ale už nasbíraná data v nich chybět budou.
5. **Ochrana osobních údajů** — bez ní nesmíte spustit registraci.

Body 4 a 5 mají největší dopad, když se na ně zapomene. Zbytek se dá dohnat kdykoli.

## Detail

### Workspace versus událost

Workspace je prostředí vaší organizace — drží kontakty, skupiny a všechny události. Nastavení workspace platí napříč událostmi, nastavení události jen pro tu jednu. Rozdělení je stabilní: GDPR, vlastní pole kontaktů, sdílené soubory a databáze kontaktů jsou **workspace**; program, registrační formulář, řečníci a sponzoři jsou **událost**.

### Uživatelský účet

Záložka **Uživatelský účet** obsahuje vaše jméno a příjmení, **jazyk administrace** (v jakém jazyce vidíte samotné rozhraní — nesouvisí s jazyky obsahu události) a **Dvoufázové ověření (2FA)**. Jazyk administrace má dvě hodnoty, češtinu a angličtinu.

Dvoufázové ověření je ve výchozím stavu **Vypnuto**; zapnete ho odkazem **Povolit dvoufaktorové ověření** vedle stavu. Potvrzuje se **ověřovací aplikací** typu Google Authenticator: administrace zobrazí QR kód, ten načtete v aplikaci a zapnutí dokončíte tlačítkem **Kód jsem si přidal - Zapnout**. Při každém dalším přihlášení pak kromě hesla zadáte časově omezený kód z aplikace. Ověření přes SMS ani záložní kódy Happenee nenabízí, takže **potřebujete telefon s ověřovací aplikací** — počítejte s tím, než ověření zapnete.

U workspace, přes který jde registrace zaměstnanců nebo klientů, ověření doporučujeme zapnout — administrátorský účet vidí kontaktní údaje všech účastníků napříč událostmi.

**Heslo se nemění tady.** Volbu **Změna hesla** najdete v menu, které se rozbalí kliknutím na jméno vašeho účtu úplně dole v levém sloupci, vedle odhlášení.

Dnes má workspace **jeden administrátorský účet**. Rozpad na víc uživatelů s vlastními přístupovými právy je v přípravě, takže zatím počítejte s tím, že přihlašovací údaje sdílí celý tým, který do administrace potřebuje.

### Informace o společnosti

Sekce **Informace o společnosti** drží fakturační a identifikační údaje vaší organizace a **Kód** — interní identifikátor workspace, který jen čtete. Kromě názvu společnosti sem patří **jméno odesílatele**, **jméno a e-mail příjemce odpovědi** a dvojice polí pro **ICS soubor** (kalendářovou pozvánku), tedy hodnoty, se kterými odcházejí e-maily účastníkům. Ze stejných údajů se plní i šablona ochrany osobních údajů, kde vystupujete jako správce.

Informace o společnosti **nastavuje zákaznická podpora**. Když se změní název firmy nebo adresa, napište jim; v administraci pole neupravíte. Pro jednotlivou událost je ale můžete přepsat v jejím nastavení.

Ve spodní části záložky **Uživatelský účet** najdete ještě kartu **Odkazy na brandovanou účastnickou aplikaci** — odkazy na iOS aplikaci, Android aplikaci a webovou aplikaci pod vaší značkou. Samotný vzhled aplikace (white label) tady nenastavíte — zapíná ho zákaznická podpora.

### Patička e-mailu a microsite

Výchozí text patičky se propisuje do e-mailů i na microsite všech událostí ve workspace. Jsou to dvě pole — **Patička microsite** a **Patička e-mailu** — a vyplňují se zvlášť pro každý jazyk obsahu; prázdné pole ukazuje **Nenastaveno**.

Stejně jako informace o společnosti mění **výchozí hodnoty** zákaznická podpora. Na úrovni jednotlivé události pak patičku můžete přepsat — pokud tedy potřebujete jinou patičku jen pro jednu událost, řešte to v nastavení té události, ne tady.

### Vlastní pole kontaktů

Textová pole, kterými si rozšíříte kontaktní údaje nad rámec standardní sady. Definují se ve workspace a jsou sdílená se všemi událostmi — použijete je v registračním formuláři, při nákupu vstupenky i jako sloupce v tabulce kontaktů. Vyplňují se ve všech jazycích, které používáte. Detail v článku [Jak fungují vlastní pole kontaktů](https://help.happenee.com/cs/articles/76-jak-funguji-vlastni-pole-kontaktu).

### Ochrana osobních údajů

Podmínky zpracování osobních údajů, které účastník bere na vědomí při registraci i při nákupu vstupenky, a **souhlasy nad rámec** (marketing, fotografie, nabídky třetích stran). Bez nastavené ochrany osobních údajů nemá smysl spouštět registraci. Detail v článku [Nastavení ochrany osobních údajů](https://help.happenee.com/cs/articles/74-nastaveni-ochrany-osobnich-udaju).

### Soubory

Samostatná položka levého menu (ne záložka nastavení): centrální úložiště dokumentů pro celý workspace. Nahrajete sem PDF nebo obrázek a dostanete odkaz, kterým se na soubor odkážete z obsahu události nebo z e-mailu. Detail v článku [Práce se soubory ve workspace](https://help.happenee.com/cs/articles/75-prace-se-soubory-ve-workspace).

### Integrace

Záložka **Integrace** spravuje napojení workspace na externí systémy. Dnes na ní vydáváte **Partner API klíče** — přístupové klíče, kterými se váš druhý systém (CRM, registrační nástroj, prodejní kanál) autorizuje proti Happenee. Ke každému klíči nastavujete oprávnění zvlášť, takže integrace dostane jen to, co potřebuje. Detail v článku [Partnerské API klíče](https://help.happenee.com/cs/articles/95-partnerske-api-klice).

### Faktury

Položka **Faktury** v levém menu ukazuje **všechny faktury napříč událostmi** ve workspace — má smysl jen tehdy, když někde prodáváte placené vstupenky. Je to běžná stránka administrace s levým menu.

Seznam filtrujete podle roku, měsíce, typu faktury a události, případně fulltextovým polem **Filtr**; u každého záznamu vidíte číslo faktury, typ, data vystavení a zdanitelného plnění, variabilní symbol, událost, částku s DPH a odběratele a stáhnete doklad v PDF. Pro účetnictví je nad tabulkou hromadné **Stáhnutí ISDOC**; u jednotlivého řádku se ISDOC nabízí jen u některých typů dokladu, takže se na něj u zálohových faktur nespoléhejte.

Nepleťte si to s objednávkami uvnitř události: tam řešíte konkrétní objednávku, fakturační údaje a refundace. Faktury ve workspace slouží k tomu, abyste si na konci měsíce stáhli doklady za všechny události na jednom místě.

### Export kontaktů

Celou databázi kontaktů vyexportujete tlačítkem **Kontakty (Excel)**. Nehledejte ho v Nastavení workspace — je **vpravo nahoře na stránce Správa kontaktů a skupin**. Hodí se před migrací, pro zálohu nebo pro předání dat do CRM.

## Na co si dát pozor

### Organizátor hledá GDPR nebo vlastní pole kontaktů v nastavení události a nenajde je

Obojí je **workspace-level**. V události najdete jen přepínače, které rozhodují, jestli se souhlasy nad rámec a vlastní pole zobrazí v registračním formuláři — samotný text podmínek ani definici polí tam nezaložíte. Když něco z toho nemůžete najít, zkontrolujte nejdřív, na které úrovni administrace stojíte.

### Změna informací o společnosti nebo výchozí patičky se plánuje na poslední chvíli

Obojí mění zákaznická podpora, ne vy. Když firma mění název nebo se sjednocuje branding, napište podpoře **dřív**, než rozešlete pozvánky — přepsat patičku ve všech už odeslaných e-mailech nejde.

### Heslo a export kontaktů se hledají v Nastavení workspace

Ani jedno tam není. **Změna hesla** je v menu pod jménem vašeho účtu dole v levém sloupci, export **Kontakty (Excel)** vpravo nahoře na stránce **Správa kontaktů a skupin**. Záložka *Uživatelský účet* mění jen jméno, jazyk administrace a dvoufázové ověření.

### Jazyk administrace se plete s jazyky obsahu události

Jazyk administrace určuje, v jakém jazyce vidíte samotné rozhraní Happenee. S tím, v jakých jazycích vidí obsah účastník, nemá nic společného — jazyky obsahu se nastavují u události a přepínají vlajkami vpravo nahoře. Klidně můžete mít administraci česky a událost jen v angličtině.

### Vlastní pole kontaktů se zakládá až po prvních registracích

Pole můžete přidat kdykoli, ale zpětně se samo nevyplní. Lidem, kteří se zaregistrovali před jeho založením, bude hodnota chybět a doplníte ji jen ručně nebo importem. Rozmyslete si proto ještě před spuštěním registrace, co budete o kontaktech potřebovat vědět.

## Související články
- [Orientace v administraci Happenee](https://help.happenee.com/cs/articles/2-orientace-v-administraci-happenee)
- [Nastavení ochrany osobních údajů](https://help.happenee.com/cs/articles/74-nastaveni-ochrany-osobnich-udaju)
- [Práce se soubory ve workspace](https://help.happenee.com/cs/articles/75-prace-se-soubory-ve-workspace)
- [Partnerské API klíče](https://help.happenee.com/cs/articles/95-partnerske-api-klice)
- [Jak fungují vlastní pole kontaktů](https://help.happenee.com/cs/articles/76-jak-funguji-vlastni-pole-kontaktu)

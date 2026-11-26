# Nastavení primárního jazyka události

> Primární jazyk je záložní jazyk pro účastníky mimo přidané jazyky a po vytvoření události se nedá změnit.

- Článek v Help Centru: https://help.happenee.com/cs/articles/10-nastaveni-primarniho-jazyka-udalosti
- English version: https://help.happenee.com/en/articles/10-setting-the-primary-language-of-an-event
- Kolekce: Nastavení eventu a registrace
- Aktualizováno: 2026-04-27

---

> [!info] Krátce
> Primární jazyk události je **záložní jazyk**, který se zobrazí účastníkovi, jehož jazyk zařízení nepatří mezi jazyky, které jste k události explicitně přidali. Volba primárního jazyka je nevratná — po vytvoření události ji nelze změnit bez založení jiné události. Pro událost se zahraničními účastníky je doporučený primární jazyk **angličtina**.

## Jak začít

- Před založením události si vyjasněte, zda budete očekávat zahraniční účastníky.
- Pokud ano, primární jazyk nastavte na **angličtinu**, i kdyby byl hlavní obsahový jazyk čeština.
- Přidejte sekundární jazyky (čeština, slovenština, další) podle toho, v jakých jazycích chcete mít obsah.
- Toto rozhodnutí udělejte při vytváření události — později ho nezměníte.

## Detail

### Jak funguje volba jazyka pro účastníka

Účastník přichází na microsite nebo do účastnické aplikace s nějakým jazykovým nastavením zařízení. Happenee zkontroluje, zda má událost obsah v tomto jazyce:

- **Ano** — zobrazí se obsah v daném jazyce.
- **Ne** — zobrazí se obsah v **primárním jazyce** události.

Primární jazyk tedy nerozhoduje, v jakém jazyce obsah vyplňujete — obsah vyplňujete v každém přidaném jazyce zvlášť. Primární jazyk rozhoduje, co vidí účastník, jehož jazyk jste nepřidali.

### Praktický příklad

Máte konferenci v Praze se zahraničními hosty. Obsah chcete vytvářet v **češtině** a **angličtině**. Očekáváte, že přijdou i účastníci s nastavením telefonu v němčině, španělštině nebo italštině.

- **Primární jazyk = čeština** (chyba): Účastníci s nastavením v němčině, španělštině nebo italštině uvidí český obsah. Pro ně nepoužitelné.
- **Primární jazyk = angličtina** (správně): Tito účastníci uvidí anglický obsah, kterému rozumí.

Pravidlo: **pokud má událost zahraniční účastníky, primární jazyk nastavte na angličtinu**. Češtinu přidejte jako sekundární. Česky mluvící účastníci uvidí češtinu, všichni ostatní angličtinu.

### Proč je rozhodnutí nevratné

Primární jazyk je základem datové struktury události. Obsahové funkce, registrační formulář, e-maily, microsite — všechno se vytváří s referencí na primární jazyk. Happenee nedovolí ho změnit zpětně, protože by to znamenalo rozbít integritu obsahu.

> Primární jazyk se nastavuje při zakládání události a **později ho nelze upravit**. Pokud zjistíte, že jste zvolili špatně, musíte založit novou událost.

### Kde se primární jazyk liší od sekundárních

Při úpravě obsahu v administraci přepínáte mezi jazyky pomocí **dvou vlajek** v pravém horním rohu. Sekundární jazyky lze libovolně přidávat a odebírat v **Nastavení události → Nastavení jazyka**. Primární jazyk v tomto nastavení vidíte označený jako **„Primární jazyk — nelze upravit“** a zůstane tam natrvalo.

Pokud nevyplníte obsah v sekundárním jazyce, systém použije pro daný obsah primární jazyk. To je také důvod, proč má smysl primární jazyk volit co nejširší (typicky angličtinu) — chrání vás před tím, že účastníkovi zobrazíte prázdný obsah.

## Na co si dát pozor

### Primární jazyk = čeština u události, na kterou přijdou zahraniční hosté. Německý host otevře microsite a vidí český obsah, i když událost má anglickou verzi

U událostí se zahraničními účastníky volte **primární jazyk = angličtina**. Češtinu přidejte jako sekundární. Platí i pro slovenské události — pokud mohou přijít hosté z jiných zemí, primární jazyk by měl být angličtina.

### Organizátor si uvědomí chybně nastavený primární jazyk, když už je zveřejněn registrační odkaz

Primární jazyk nelze změnit. Jediná možnost je založit novou událost a staré registrované účastníky do ní převést. Rozhodnutí udělejte při zakládání události.

### Obsah vyplněný jen v primárním jazyce, ale účastníci s tímto jazykem nastaveným v zařízení jsou v menšině

Primární jazyk neznamená „hlavní obsahový jazyk“ — znamená „fallback pro všechny neznámé jazyky“. Obsah vyplňte ve všech jazycích, které chcete nabídnout. Pro přepnutí jazyka při úpravě použijte vlajku v pravém horním rohu administrace události.

## Související články

- [Vytvoření nové události](https://help.happenee.com/cs/articles/9-vytvoreni-nove-udalosti)
- [Co nastavit jako první po vytvoření eventu](https://help.happenee.com/cs/articles/3-co-nastavit-jako-prvni-po-vytvoreni-eventu)
- [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace)
- [Co dělat, když kampaň nejde odeslat nebo přišla v jiném jazyce](https://help.happenee.com/cs/articles/88-co-delat-kdyz-kampan-nejde-odeslat-nebo-prisla-v-jinem-jazyce)

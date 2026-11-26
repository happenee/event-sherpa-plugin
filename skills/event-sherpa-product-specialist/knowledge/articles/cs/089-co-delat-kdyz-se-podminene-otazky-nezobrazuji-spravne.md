# Co dělat, když se podmíněné otázky nezobrazují správně

> Navazující otázka se účastníkovi neukáže, nebo se ukáže všem. Kde hledat příčinu a proč zpětné úpravy nefungují na už odeslané odpovědi.

- Článek v Help Centru: https://help.happenee.com/cs/articles/89-co-delat-kdyz-se-podminene-otazky-nezobrazuji-spravne
- English version: https://help.happenee.com/en/articles/89-what-to-do-when-conditional-questions-do-not-display-correctly
- Kolekce: Řešení problémů
- Aktualizováno: 2026-08-07

---

> [!info] Krátce
> Navazující otázka se účastníkovi buď neukáže vůbec, nebo naopak vyskočí všem. Za obojím stojí nastavení vazby mezi konkrétní **odpovědí** a navazující otázkou — ne chyba formuláře jako celku.

## Jak začít

Otevřete formulář v náhledu a projděte ho jako účastník: vyberte tu odpověď, která má navazující otázku spustit. Náhled ukáže reálné chování rychleji než kontrola nastavení.

## Detail

### Otázka se nezobrazí

Nejčastější příčiny v pořadí, v jakém je má smysl kontrolovat:

1. **Vazba je na jinou odpověď, než si myslíte.** Podmínka se váže na konkrétní odpověď, ne na otázku. Když jste odpovědi po nastavení přejmenovali nebo přidali novou, vazba může ukazovat jinam.
2. **Navazující otázka je skrytá.** Zkontrolujte její viditelnost — skrytá otázka se nezobrazí, ani když se podmínka splní.
3. **Otázka je omezená na skupinu**, do které účastník nepatří. Viditelnost podle skupin a podmínka podle odpovědi se sčítají: musí platit obě.
4. **Chybí druhá jazyková verze.** Otázka bez textu ve druhém jazyce se účastníkovi s tímto jazykem prakticky nezobrazí.

### Otázka se zobrazí všem

Znamená to, že podmínka není nastavená, nebo se ztratila při úpravě odpovědí. Otevřete navazující otázku a ověřte, že má vazbu na konkrétní odpověď — bez ní je to běžná otázka pro všechny.

### Zpětné úpravy nefungují na existující odpovědi

Když podmínku nebo zařazení do skupiny doplníte až po spuštění formuláře, na už odeslané odpovědi se to **nepropíše**. Lidé, kteří se zaregistrovali dřív, zůstanou bez navazující otázky a bez skupiny. Doplnit to musíte ručně — hromadným přiřazením ve Správě kontaktů a skupin.

## Na co si dát pozor

### Formulář se testuje z administrace, ne z pohledu účastníka

V administraci vidíte všechny otázky včetně skrytých a podmíněných. Chování, které uvidí účastník, ověříte jen v náhledu nebo skutečným průchodem registrací. Testujte vždy obě jazykové verze.

### Podmíněné otázky se řetězí do hloubky

Otázka podmíněná odpovědí, která je sama podmíněná jinou odpovědí, se ladí špatně a účastníka mate. Když potřebujete víc než dvě úrovně, obvykle je čistší rozdělit publikum skupinami a mít dva jednodušší formuláře.

### Povinná podmíněná otázka blokuje odeslání

Pokud je navazující otázka povinná a z nějakého důvodu se nezobrazí správně, účastník formulář neodešle a nepochopí proč. U podmíněných otázek zvažte, jestli musí být povinné.

## Související články
- [Jak fungují podmíněné otázky v registračním formuláři](https://help.happenee.com/cs/articles/14-jak-funguji-podminene-otazky-v-registracnim-formulari)
- [Nastavení registračního formuláře](https://help.happenee.com/cs/articles/13-nastaveni-registracniho-formulare)
- [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti)

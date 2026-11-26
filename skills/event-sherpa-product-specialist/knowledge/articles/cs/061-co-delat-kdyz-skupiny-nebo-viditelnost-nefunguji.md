# Co dělat, když skupiny nebo viditelnost nefungují

> Postup, když účastníci nevidí obsah, který mají vidět, nebo naopak vidí, co neměli.

- Článek v Help Centru: https://help.happenee.com/cs/articles/61-co-delat-kdyz-skupiny-nebo-viditelnost-nefunguji
- English version: https://help.happenee.com/en/articles/61-what-to-do-when-groups-or-visibility-are-not-working
- Kolekce: Řešení problémů
- Aktualizováno: 2026-08-04

---

> [!info] Krátce
> Účastníci nevidí obsah, který mají vidět, nebo naopak vidí něco, co vidět neměli. Nejčastější příčina je, že struktura skupin nebyla promyšlená před spuštěním registrace — a ex post se to dohání ručně. *Když to neuděláte na začátku, ex post už to vlastně nejde* platí pro Happenee poměrně přesně.

## Jak začít

Otevřete správu kontaktů a skupin a podívejte se, kolik lidí ve *skupině, na kterou cílíte*, skutečně je. Pokud je číslo nižší, než čekáte, problém je v přiřazení — ne v nastavení viditelnosti.

## Detail

### Typické příčiny

- **Skupina nebyla vytvořena před spuštěním registrace.** Automatické přiřazení (přes odpověď ve formuláři, vstupenku, slevový kód, nominátora) funguje jen dopředu — existující registrace se do nově vytvořené skupiny samy nepřidají.
- **Viditelnost modulu je nastavená na skupinu, ve které účastník chybí.** Funkce se tím pro něj „schová“ a organizátor si myslí, že je aplikace rozbitá.
- **Očekávání automatických systémových skupin** (například *Potvrzení účastníci*, *Nepřihlášení*). Dnes jsou k dispozici **pouze Globální skupiny**, Systémové i Lokální skupiny jsou plánované. Pro rozlišení podle stavu použijte filtr ve statistikách účastníků nebo v cílení kampaně.
- **Očekávání Lokálních skupin vázaných na jednu událost.** Všechny skupiny jsou dnes **Globální pro workspace** — neexistují skupiny, které by patřily jen jedné události. Lokální skupiny jsou plánované.

### Jak to opravit

- **Ručně přiřaďte účastníky** do správné skupiny ve správě kontaktů a skupin (akce *Přidat nebo odebrat ze skupin*).
- **Zkontrolujte nastavení viditelnosti** u dané obsahové nebo engagement funkce — buď ji otevřete všem, nebo ověřte, že cílová skupina má správné členy.
- **Znovu odešlete kampaň / zvací e-mail** s aktualizovaným cílením — u již odeslané kampaně použijte na záložce **Rozesílky** panel **Doposlat kampaň nově přiřazeným** a tlačítko **Nově přiřazení**.
- **U funkce, která má pro organizátora smysl jen pro některé**, zvažte, zda místo viditelnosti podle skupiny nestačí nechat funkci vypnutou a zapnout ji, až budete mít skupinu naplněnou.

### Prevence

- Než zapnete registraci, projděte si seznam skupin, které budete potřebovat — pro cílení komunikace, viditelnost obsahu, filtrování reportingu.
- U jednorázových skupin použijte pojmenování s prefixem události (například `Konference25_VIP`), aby se skupiny z různých událostí nemíchaly.
- Detailní logika skupin a viditelnosti je popsána v článku *Práce se skupinami a viditelností*.

## Na co si dát pozor

### Organizátor očekává, že se po registraci vytvoří automaticky skupina *Potvrzení účastníci*

Systémové skupiny dnes nejsou k dispozici (funkce je plánovaná). Místo skupiny použijte filtr podle stavu přihlášení — ve statistikách účastníků i v cílení kampaně.

### Skupina byla vytvořena až po spuštění registrace. Organizátor čeká, že se stávající účastníci do ní zařadí zpětně

Automatické zařazení přes odpověď ve formuláři, vstupenku, slevový kód nebo nominátora platí jen pro nové registrace / odpovědi. Stávající členy doplňte ručně ve správě kontaktů a skupin. **Výjimka je přiřazení skupiny na session nebo jejím typu** (nastavení *Přiřadit účastníka do skupiny po registraci*): tam se skupina po zapnutí doplní i účastníkům, kteří už jsou registrovaní, a po vypnutí se zase odebere — včetně těch, kdo ji mají přiřazenou i z jiného zdroje.

### Zvací e-mail cílený na skupinu — a nejde to nastavit

Zvací e-mail nepodporuje cílení přes skupiny (jen podle stavu: *Nepozvaní*, *Bez odpovědi*, *Kdo si nepřečetl zvací e-mail*). Pro cílení na skupinu použijte **E-mailovou kampaň**.

## Související články

- [Práce se skupinami a viditelností](https://help.happenee.com/cs/articles/15-prace-se-skupinami-a-viditelnosti)
- [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace)
- [Jak fungují podmíněné otázky v registračním formuláři](https://help.happenee.com/cs/articles/14-jak-funguji-podminene-otazky-v-registracnim-formulari)

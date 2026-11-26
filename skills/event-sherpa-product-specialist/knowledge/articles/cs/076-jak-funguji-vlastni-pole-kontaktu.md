# Jak fungují vlastní pole kontaktů

> Workspace-level pole, kterými rozšíříte kontaktní údaje nad standardní sadu — kde se definují, kde všude se projeví a proč je má smysl založit před spuštěním registrace.

- Článek v Help Centru: https://help.happenee.com/cs/articles/76-jak-funguji-vlastni-pole-kontaktu
- English version: https://help.happenee.com/en/articles/76-how-custom-contact-fields-work
- Kolekce: Nastavení eventu a registrace
- Aktualizováno: 2026-08-07

---

> [!info] Krátce
> **Vlastní pole kontaktů** jsou textová pole, kterými si rozšíříte kontaktní údaje nad rámec standardní sady (jméno, e-mail, telefon, společnost, pozice a další). Definujete je jednou v **Nastavení workspace** a jsou pak **sdílená napříč všemi událostmi** — použijete je v registračním formuláři, u nákupu vstupenky, jako sloupec v tabulce kontaktů i jako zástupnou proměnnou v e-mailu. Založte je dřív, než spustíte první registraci; zpětně se nevyplní.

## Jak začít

1. Sepište si, co o lidech potřebujete vědět **napříč událostmi**, ne jen na jedné. Typicky oslovení, oddělení, interní ID zaměstnance, středisko pro přeúčtování nákladů.
2. Ověřte, že to už není standardní pole. **Společnost** a **IČO** standardní pole jsou — zakládat je znovu jako vlastní pole je častý omyl.
3. Pole založte v **Nastavení workspace** na záložce **Vlastní pole kontaktů** a vyplňte název **ve všech jazycích**, které používáte.
4. Teprve pak v registračním formuláři konkrétní události rozhodněte, jestli se pole zobrazí a jestli bude povinné.

## Detail

### Workspace, ne událost

Definice pole žije ve workspace, ne v události. To znamená, že pole založené kvůli jedné konferenci je od té chvíle k dispozici i všem ostatním událostem — a hodnota, kterou u kontaktu vyplníte, se drží u kontaktu napříč událostmi. Když stejný člověk přijde na tři vaše události, jeho oddělení nebo interní ID zadáváte jednou.

To je zároveň důvod, proč nemá smysl zakládat pole pro jednorázovou informaci vázanou na jednu událost (*preferovaný termín workshopu*, *velikost trička*). Takové věci patří mezi **doplňující otázky** registračního formuláře — ty jsou vázané na událost a odpověď zůstane u té události.

### Kde se pole projeví

- **Registrační formulář** — vlastní pole jsou v něm samostatná sekce pod standardními kontaktními poli, se stejnou trojicí voleb *Povinné / Nepovinné / Skrýt*.
- **Nákup vstupenky** — pole lze zobrazit i v údajích, které vyplňuje kupující.
- **Tabulka kontaktů** — vlastní pole si zapnete jako sloupec přes tlačítko **Sloupce**, takže podle něj můžete filtrovat a řadit.
- **Import kontaktů** — vlastní pole má svůj sloupec v importní šabloně, takže se dají naplnit hromadně z Excelu.
- **E-maily a kampaně** — na vlastní pole existuje zástupná proměnná, kterou vložíte do textu zprávy.

### Vlastní pole versus doplňující otázky

Rozhodovací pravidlo je jednoduché:

- **údaj, který o člověku platí dlouhodobě a napříč událostmi** — **vlastní pole kontaktů** (workspace)
- **odpověď platnou jen pro tuhle událost** — **doplňující otázku** v registračním formuláři (událost)
- **větvení formuláře podle odpovědi nebo zařazení do skupiny** — **doplňující otázku** — vlastní pole tohle neumí

Vlastní pole jsou textová. Když potřebujete výběr z možností, souhlas, datum nebo podmíněnou logiku, jste v doplňujících otázkách.

### Vyplnění ve více jazycích

Název pole se zadává pro každý jazyk zvlášť. Pokud událost běží česky i anglicky a název vyplníte jen v jednom jazyce, uvidí druhá jazyková skupina prázdný nebo nepřeložený popisek. Po založení pole vždy přepněte jazyk a doplňte druhou verzi.

## Na co si dát pozor

### Jako vlastní pole se založí Společnost nebo IČO

Obojí je **standardní** kontaktní pole registračního formuláře. Když je založíte znovu jako vlastní pole, budete mít v tabulce kontaktů dva sloupce s firmou, dvě různě vyplněné hodnoty a v exportu nepořádek. Než pole založíte, projděte si standardní sadu: E-mail, Jméno, Příjmení, Telefon, Pracovní pozice, Společnost, IČO, Země, Twitter (X), LinkedIn.

### Pole vznikne až po prvních registracích

Vlastní pole můžete přidat kdykoli, ale zpětně se samo nevyplní. Lidem, kteří se zaregistrovali dřív, bude hodnota chybět a doplníte ji jen ručně u jednotlivých kontaktů nebo importem z Excelu. U větší události to znamená hodiny práce navíc — proto pole zakládejte v přípravné fázi, ne až vám bude chybět v reportu.

### Pole se použije pro jednorázovou informaci k jedné události

Velikost trička, výběr menu nebo preferovaný workshop nejsou vlastnosti kontaktu — jsou to odpovědi k jedné události. Když je zadáte jako vlastní pole, budou viset u kontaktu i u všech dalších událostí a při příští události vám budou matoucí. Patří do doplňujících otázek registračního formuláře.

### Organizátor hledá definici pole v události

V nastavení události najdete jen přepínač, jestli se vlastní pole ve formuláři zobrazí. Samotné pole zakládáte a přejmenováváte v **Nastavení workspace**. Pokud tam pole nevidíte, není založené — ne skryté.

## Související články
- [Nastavení workspace](https://help.happenee.com/cs/articles/73-nastaveni-workspace)
- [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace)
- [Nastavení registračního formuláře](https://help.happenee.com/cs/articles/13-nastaveni-registracniho-formulare)
- [Jak fungují zástupné proměnné](https://help.happenee.com/cs/articles/78-jak-funguji-zastupne-promenne)

# Co je workspace a co je event

> Workspace je centrální prostor vaší organizace, event je konkrétní události uvnitř něj.

- Článek v Help Centru: https://help.happenee.com/cs/articles/1-co-je-workspace-a-co-je-event
- English version: https://help.happenee.com/en/articles/1-what-is-a-workspace-and-what-is-an-event
- Kolekce: Začínáme s Happenee
- Aktualizováno: 2026-09-01

---

> [!info] Krátce
> V Happenee jsou dva klíčové pojmy, které musíte pochopit hned na začátku: **workspace** a **event**. Workspace je centrální prostor vaší organizace — jeden účet, ve kterém se hromadí všechny události a všichni účastníci. Event je konkrétní událost uvnitř workspace — má svůj program, svoji registraci, svoji komunikaci. Pochopení, co patří na úroveň workspace a co na úroveň eventu, vám ušetří práci napříč všemi budoucími událostmi.

## Jak začít

- Ujasněte si, že pod jedním workspace běží všechny vaše události — minulé i připravované.
- Rozhodněte, co má smysl nastavovat jednou na úrovni workspace (GDPR, patička e-mailů, vlastní pole kontaktů), a co naopak patří do nastavení konkrétního eventu (registrace, program, obsah).
- Teprve pak vytvořte první event.

## Detail

### Workspace — jeden prostor pro celou organizaci

Workspace je administrátorský účet, pod kterým běží celá vaše práce v Happenee. Typicky ho má jedna organizace — společnost, agentura, oddělení. Jeden workspace má v současnosti jednoho administrátora (jeden přístupový e-mail).

V rámci workspace se sdílí:

- **Databáze kontaktů** — všichni lidé, které jste kdy do Happenee naimportovali, existují jako kontakty ve workspace. Nejsou „navěšeni“ na konkrétní event. Když založíte nový event, prostě je k němu přiřadíte.
- **Skupiny** — skupiny (VIP, speakeři, klientské segmenty) žijí na úrovni workspace a můžete je používat napříč eventy.
- **Vlastní pole kontaktů** — rozšíření standardních kontaktních údajů. Jednou založené pole se propisuje do všech eventů.
- **Výchozí nastavení GDPR a podmínek** — šablona zpracování osobních údajů, souhlasy nad rámec (marketing, publikace fotek atd.) platí napříč všemi eventy.
- **Soubory** — centrální úložiště dokumentů, na které lze odkazovat z libovolného eventu.
- **Faktury** — přehled všech vystavených faktur pro workspace, pokud používáte placené vstupenky.
- **Patička e-mailu a microsite** — výchozí texty, které se propisují do všech eventů.

### Event — konkrétní událost

Event je jednotlivá událost, kterou organizujete — konference, firemní setkání, workshop, galavečer. Patří do workspace a dědí z něj výše zmíněné sdílené prvky. Zároveň má vlastní nastavení, která platí jen pro něj:

- **Základní informace** — název, datum, čas, časové pásmo, Typ události (Fyzická / Virtuální / Hybridní), primární jazyk.
- **Registrační formulář a doplňující otázky** — ty se ukládají k danému eventu. To, jakou otázku přidáte do formuláře konference v březnu, nijak neovlivní formulář workshopu v září.
- **Program, Řečníci, Lokalita, Sponzoři, Vystavovatelé** — veškerý obsah je specifický pro event.
- **Microsite a účastnická aplikace** — každý event má vlastní microsite a vlastní data v aplikaci.
- **Komunikace** — zvací a potvrzovací e-maily, e-mailové kampaně, oznámení.
- **Přiřazení účastníci** — kontakty z workspace jsou k eventu přiřazeny, samotné kontakty ale zůstávají ve workspace.

### Jak workspace a event spolupracují

Nejlepší způsob, jak si vztah představit: workspace je **firemní adresář a pravidla**, event je **konkrétní projekt**.

Příklad z praxe:

- V lednu pořádáte konferenci. Naimportujete si 2 000 kontaktů do workspace a 600 z nich přiřadíte ke konferenci.
- V květnu pořádáte klientský workshop. Kontakty už máte — jen vyberete 120 z nich a přiřadíte k workshopu.
- V září máte firemní setkání. Přiřadíte třeba 80 lidí, kteří byli v lednu na konferenci.

Žádný z těchto účastníků jste nemuseli importovat třikrát. A jejich data (vyplněná při registraci na konferenci) ve workspace zůstávají — rozšiřují profil kontaktu napříč všemi událostmi.

### Co z toho plyne pro nastavení

Některé věci řešte **jednou na úrovni workspace**, abyste se k nim nevraceli u každého eventu:

- GDPR šablona
- Souhlasy nad rámec (marketing, fotky, třetí strany)
- Patička e-mailu
- Vlastní pole kontaktů
- Import standardní databáze kontaktů a skupin

Ostatní věci řešte **uvnitř eventu**:

- Registrační formulář a doplňující otázky (každý event má jiné)
- Obsah (program, řečníci, sponzoři)
- Komunikaci a kampaně

## Na co si dát pozor

### Import kontaktů zvlášť pro každý event, jako by šlo o samostatné databáze

Importujte kontakty jednou do workspace a dál je jen přiřazujte k jednotlivým eventům. Happenee je navržené na tento způsob práce.

### Vlastní pole kontaktů vytvořená uvnitř eventu v domnění, že jsou specifická pro danou událost

Vlastní pole kontaktů patří do workspace. Fungují napříč všemi eventy — to je jejich smysl. Informace specifické pro jednu událost patří do doplňujících otázek registračního formuláře, ne do vlastních polí kontaktů.

### GDPR šablona a souhlasy se nastavují zvlášť u každého eventu, přestože jsou společné pro celou organizaci

GDPR nastavujete jednou na úrovni workspace. U jednotlivých eventů jen ověřujete, že se správně propisuje.

## Související články

- [Orientace v administraci Happenee](https://help.happenee.com/cs/articles/2-orientace-v-administraci-happenee)
- [Co nastavit jako první po vytvoření eventu](https://help.happenee.com/cs/articles/3-co-nastavit-jako-prvni-po-vytvoreni-eventu)
- [Microsite vs účastnická aplikace: jak přemýšlet nad flow účastníka](https://help.happenee.com/cs/articles/5-microsite-vs-ucastnicka-aplikace-jak-premyslet-nad-flow-ucastnika)
- [Vytvoření nové události](https://help.happenee.com/cs/articles/9-vytvoreni-nove-udalosti)
- [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace)
- [Dokumentace Happenee ve vašem AI asistentovi](https://help.happenee.com/cs/articles/96-dokumentace-happenee-ve-vasem-ai-asistentovi)

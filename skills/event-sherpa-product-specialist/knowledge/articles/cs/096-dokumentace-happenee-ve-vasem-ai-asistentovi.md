# Dokumentace Happenee ve vašem AI asistentovi

> Jak dát ChatGPT, Claude nebo jinému AI asistentovi přístup k aktuální dokumentaci Happenee: instrukce ke zkopírování a na co si dát pozor.

- Článek v Help Centru: https://help.happenee.com/cs/articles/96-dokumentace-happenee-ve-vasem-ai-asistentovi
- English version: https://help.happenee.com/en/articles/96-using-the-happenee-documentation-in-your-ai-assistant
- Kolekce: Event Sherpa
- Aktualizováno: 2026-09-01

---

> [!info] Krátce
> Pokud svůj event plánujete v ChatGPT, Claude nebo jiném AI asistentovi, můžete mu dát přístup k aktuální dokumentaci Happenee. Stačí do projektu vložit krátkou instrukci z tohoto článku — asistent si pak při otázkách o Happenee načte odpovídající články nápovědy a spojí je s tím, co ví o vašem eventu. Pro rychlé dotazy při práci v administraci je nejkratší cestou Event Sherpa; vlastní AI asistent se hodí na plánování v širším kontextu eventu. Nic se neinstaluje; instrukce funguje v každém AI nástroji, který umí načítat webové stránky.

## Jak začít

- Otevřete AI nástroj, ve kterém svůj event řešíte — typicky projekt v ChatGPT nebo Claude, kde už máte brief, program nebo rozpočet.
- Vložte instrukci ze sekce Detail do instrukcí projektu (v ChatGPT a Claude je najdete v nastavení projektu; v jiných nástrojích patří do systémových instrukcí).
- Ověřte, že asistent smí načítat webové stránky. Bez přístupu na web instrukce nefunguje.
- Položte zkušební otázku — například „Jak v Happenee nastavím registraci pro VIP a běžné hosty?" — a zkontrolujte, že odpověď odkazuje na články z help.happenee.com.

## Detail

### Event Sherpa, nebo vlastní AI asistent?

Event Sherpa je AI asistent přímo v administraci Happenee. Zná tuto dokumentaci, je po ruce u konkrétního nastavení a na otázky typu „jak nastavím registraci" nebo „kde najdu exporty" odpoví okamžitě — poradí vám postup, samotné kroky v administraci ale děláte vy. Vlastní AI asistent přidává druhý úhel pohledu: zná kontext vašeho eventu, takže se hodí při plánování a rozhodování.

- **Event Sherpa** — dotazy při práci v administraci: jak něco nastavit, kde co najít, proč se něco chová jinak, než čekáte. Odpovídá okamžitě, bez jakékoli přípravy.
- **Vlastní AI asistent** — plánování a rozhodování v kontextu celého eventu: kombinuje dokumentaci Happenee s vaším briefem, programem a rozpočtem.

Oba čerpají ze stejné dokumentace, odpovědi si proto neprotiřečí — vyberte si podle toho, kde právě pracujete.

### Instrukce ke zkopírování

Zkopírujte celý obsah rámečku (sedm bodů včetně adres) a vložte ho do instrukcí svého AI projektu:

```
1. Kdykoli se konverzace týká Happenee (nastavení eventu, registrace, microsite, e-maily, program, check-in, reporting), neodpovídej z paměti. Dokumentace na help.happenee.com se průběžně mění a tvoje interní znalosti mohou být zastaralé. Při rozporu platí načtený obsah.
2. Podle tématu otázky načti stránku kolekce se seznamem článků:
   - Začínáme s Happenee: https://help.happenee.com/cs/collections/1-zaciname-s-happenee
   - Nastavení eventu a registrace: https://help.happenee.com/cs/collections/4-nastaveni-eventu-a-registrace
   - Obsah a zkušenost účastníka (microsite, program, aplikace): https://help.happenee.com/cs/collections/9-obsah-a-zkusenost-ucastnika
   - Komunikace a pozvánky (e-maily, kampaně): https://help.happenee.com/cs/collections/13-komunikace-a-pozvanky
   - Den události a provoz na místě (check-in): https://help.happenee.com/cs/collections/17-den-udalosti-a-provoz-na-miste
   - Reporting a práce po události: https://help.happenee.com/cs/collections/20-reporting-a-prace-po-udalosti
   - Event Sherpa (doporučené setupy podle typu události): https://help.happenee.com/cs/collections/23-event-sherpa
   - Řešení problémů: https://help.happenee.com/cs/collections/27-reseni-problemu
3. Ze seznamu vyber jeden až tři relevantní články a načti je celé. Teprve potom odpovídej.
4. Odpověď postav na dvou zdrojích: fakta o Happenee ber výhradně z načtených článků, specifika eventu (cílové skupiny, program, rozpočet) z kontextu tohoto projektu.
5. U použitých článků uveď v odpovědi jejich plné adresy, aby si je organizátor mohl otevřít.
6. Když dokumentace téma nepokrývá, řekni to výslovně a doporuč zeptat se Event Sherpy přímo v administraci Happenee. Nikdy nepopisuj funkce, které v načtené dokumentaci nejsou.
7. Pokud webové stránky načítat nemůžeš, řekni to a označ odpověď jako potenciálně neaktuální.
```

### Jak instrukce funguje

Instrukce vede asistenta stejnou cestou, jakou byste v nápovědě šli sami: nejdřív přehled článků v kolekci, pak jeden až tři konkrétní články, teprve potom odpověď. Smyslem je aktuálnost — dokumentace se mění spolu s produktem, zatímco AI modely si pamatují stav ke dni svého tréninku. Asistent, který si článek načte, pracuje s přesnými pojmy, aktuálním postupem i upozorněními na časté chyby a umí je vztáhnout ke konkrétnímu eventu, který s ním plánujete.

## Na co si dát pozor

### Asistent bez přístupu na web odpovídá z paměti

Pokud má váš AI nástroj načítání webu vypnuté, instrukce nemá jak fungovat a asistent odpoví ze svých tréninkových dat — ta bývají i mnoho měsíců stará. Poznáte to podle chybějících odkazů na help.happenee.com v odpovědi.

### Načtení dokumentace není zaručené pokaždé

I s vloženou instrukcí může model občas odpovědět rovnou z paměti. Pokud odpověď nevypadá aktuálně nebo neodkazuje na nápovědu, požádejte: „Ověř to v dokumentaci Happenee." Asistent si články načte a odpověď opraví nebo potvrdí.

### Asistent nevidí do vaší administrace

Dokumentace popisuje, jak Happenee funguje — asistent z ní nezjistí stav vašeho eventu, počet registrovaných ani obsah administrace. Odpověď na otázky typu „kolik lidí se už registrovalo" najdete v administraci události, ne v dokumentaci.

### Osobní údaje účastníků do externí AI nepatří

Pro práci s dokumentací asistent žádné osobní údaje nepotřebuje. Jména, e-maily ani exporty registrací do externího AI nástroje nevkládejte — jejich sdílení s třetí stranou podléhá vašim povinnostem podle GDPR.

## Související články

- [Co je workspace a co je event](https://help.happenee.com/cs/articles/1-co-je-workspace-a-co-je-event)
- [Doporučené pořadí setupu eventu krok za krokem](https://help.happenee.com/cs/articles/8-doporucene-poradi-setupu-eventu-krok-za-krokem)

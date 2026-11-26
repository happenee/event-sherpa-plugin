<!-- source: kb.cs.07.09 -->

---
title: "Doporučený setup pro testovací jízdy"
description: "Jak připravit rezervace testovacích jízd podle skutečné dostupnosti vozů, instruktorů a provozu na místě."
collection: "Event Sherpa"
subcollection: "pro-specializovane"
modules: ["prurezovy"]
slug: "doporuceny-setup-pro-testovaci-jizdy"
lang: "cs"
status: "published"
docId: 98
last_updated: "2026-09-21"
version: 2
tags: [testovaci-jizdy, rezervace, casove-sloty, automobily, event-sherpa]
source_images_consulted: false
related:
  - "Nastavení rezervací v programu — auta, workshopy, doprovodný program"
  - "Jak fungují časové sloty"
  - "Sestavení programu události — architektura"
  - "Nastavení workshopů a registrace na sessions"
  - "Jak funguje check-in a skenování QR kódů"
---

> [!info] Krátce
> Testovací jízdu postavte kolem skutečného provozního oběhu: příchod hosta, ověření podmínek, instruktáž, předání vozu, jízda, návrat a příprava pro dalšího hosta. V Happenee nabídnete rezervace pomocí sessions typu Časový slot a dáte hostovi program, instrukce a kontakt v účastnické aplikaci. Happenee ale automaticky nekoordinuje současnou dostupnost auta, instruktora, trasy a stanoviště a neeviduje, zda host jízdu skutečně absolvoval.

## Jak začít

Nejdřív si odpovězte na pět otázek:

- **Co si host rezervuje a co má z jízdy mít?** Konkrétní vůz, model, nebo jen návštěvu s ručním přidělením auta? A co si má odnést host a co potřebujete vykázat vy jako pořadatel? Podle čeho úspěch poznáte, si dohodněte dřív, než otevřete rezervace.
- **Co omezuje počet souběžných jízd?** Počet vozů, instruktorů, stanovišť, bezpečná trasa, nebo jejich kombinace?
- **Jak dlouho trvá celý oběh?** Započítejte ověření podmínek, instruktáž, předání, návrat, kontrolu a provozní rezervu, ne jen čas za volantem.
- **Kdo smí jet a kdo to ověří?** Podmínky, oprávnění a potřebné dokumenty určuje a kontroluje provozovatel.
- **Kdo rozhodne při zpoždění, zrušení nebo nedostupném voze?** Určete odpovědnou osobu i náhradní postup dřív, než otevřete rezervace.

Pokud skutečnou délku oběhu neznáte, proveďte jednu fyzickou zkušební jízdu. Teoretický počet slotů neberte jako potvrzenou kapacitu.

## Detail

### Zvolte model rezervací podle zdrojů

Pro rezervace použijte samostatný Program a sessions typu Časový slot. Happenee nemá samostatný rezervační modul; rezervace je registrace na konkrétní slot a host ji vidí v Moje agenda.

- **Konkrétní vůz nebo specialista:** jedna session představuje jeden zdroj. Host ví, co rezervuje, ale organizátor musí mimo systém sladit další potřebné zdroje.
- **Zaměnitelné vozy stejného modelu:** kapacita jednoho slotu může odpovídat počtu jízd, které obsluha skutečně zvládne. Tuto variantu použijte jen tehdy, když obsluha umí přidělit konkrétní vůz na místě a odpovídá tomu i počet instruktorů a stanovišť. Počítejte s tím, že všichni hosté z jednoho slotu přijdou ve stejný čas a že v evidenci neuvidíte, kdo jel kterým vozem.
- **Příchod bez rezervace:** zveřejněte návštěvní okno a řiďte frontu ručně. Host musí vědět, že nemá zaručený čas jízdy. Happenee nemá automatický čekací seznam.
- **Více modelů během jedné návštěvy:** mezi rezervacemi ponechte čas na přesun a instruktáž. Výchozí omezení souběžných registrací brání hostovi rezervovat dva sloty ve stejný čas, ale neověřuje, zda je pro obě jízdy volný instruktor nebo vůz.

Nenastavujte dvě souběžné řady jízd jen proto, že máte dvě auta, pokud obě potřebují stejného instruktora. Jeden sdílený zdroj může být skutečným limitem celé kapacity.

### Nastavte časové sloty podle celého oběhu

U každé session nastavte datum, začátek a konec a pole **Délka časového slotu**, **Délka přestávky** a **Omezit počet registrací** (kapacita jednoho slotu). Délka slotu se vybírá z pevné nabídky od 10 do 120 minut, přestávka může být 0, 5, 10 nebo 15 minut. Vše ověřte před první rezervací: po registraci prvního hosta jsou typ session, čas začátku a konce, délka slotu i délka přestávky zamčené.

Příklad: samotná jízda trvá 20 minut a předání s přípravou dalších 10 minut, tedy slot 20 minut a přestávka 10 minut. Celý oběh je 30 minut. Pokud máte jediného instruktora a ten musí sedět v každém voze, zvládne během tří hodin nejvýše šest teoretických jízd bez provozní rezervy. Dvě auta tento limit nezdvojnásobí. Bezpečnější první rozpis nabídne pět slotů a jeden blok ponechá na zpoždění nebo přípravu: v záložce **Sloty** přepněte jeden slot na **Neaktivní**. Konkrétní plán potvrďte fyzickou zkouškou.

U typů Workshop a Časový slot můžete nastavit **Časové omezení registrace** (od kdy a do kdy lze rezervovat) a **Odhlášení ze session** (do kdy může host rezervaci sám zrušit). Odhlášení ze session termín přidává, zrušení nezakazuje: bez nastaveného termínu může host rezervaci zrušit kdykoli. Po termínu už host rezervaci nezruší ani nepřepne na jiný slot; změnu za něj uděláte vy.

### Propojte rezervaci s cestou hosta

Microsite může hostovi představit modely a podmínky ještě před registrací. V účastnické aplikaci host najde Program, svou rezervaci v Moje agenda, místo, instrukce a kontakt. Webová aplikace běží v prohlížeči bez instalace; kvůli ní nemusíte událost zakládat jako hybridní: u fyzické události je dostupná webová i mobilní aplikace.

I pro malý počet hostů doporučujeme účastnickou aplikaci nabídnout jako součást celého ekosystému Happenee, ne ji každému vnucovat. Po jízdě se host může ve stejném prostředí vrátit k materiálům, kontaktu nebo dalším termínům série, podle přístupu a licence. U série testovacích dnů je tento návrat součástí hodnoty: nejde jen o jednu rezervaci. Rozsah obsahu a navazující komunikace přizpůsobte skutečnému zájmu hosta a souhlasům, které od něj máte.

Pokud účastnickou aplikaci nepoužijete, předejte čas, místo, podmínky a kontakt pro změny jiným domluveným kanálem. PDF není samoobslužný rezervační systém; změny musí převzít konkrétní člověk.

U session zapněte **Upozornění účastníkovi při změně registrace**, aby host dostal e-mail při rezervaci i při jejím zrušení, a případně **Odeslat ICS účastníkovi**. Provozní změnu (jiný čas, jiný vůz, zrušená jízda) ale hostovi vždy předejte sami. Úprava v administraci sama o sobě neznamená, že se o ní host dozvěděl.

### Oddělte příchod, jízdu a další krok

Při příjezdu obsluha hosta odbaví v servisní aplikaci naskenováním QR kódu nebo ze seznamu podle jména. Check-in eviduje příchod na místo, ne konkrétní rezervovanou jízdu: nepotvrzuje, že host jízdu absolvoval ani že vrátil vůz. Předání a návrat vozu můžete zaznamenat jako další **místa check-inu** typu **Kontrola opakovaně** (například *Předání vozu* a *Návrat vozu*): obsluha naskenuje hosta při předání a znovu při návratu a export skenů vám dá čas obou úkonů. Záznam patří k hostovi a místu, ne k vozu ani ke slotu; stav vozu ani oprávnění hosta tím neověříte. Pokud vám to nestačí, veďte domluvený provozní záznam.

Po události vykazujte odděleně:

- rezervované sloty (export registrací u session);
- příchozí hosty (check-in);
- skutečně absolvované jízdy (sken při návratu nebo provozní záznam);
- zpětnou vazbu;
- další krok, o který host požádal.

Rezervace není absolvovaná jízda a check-in není obchodní výsledek. Do CRM nebo obchodnímu týmu předávejte jen kontakty a další kroky, ke kterým máte souhlas hosta a domluvený postup.

## Na co si dát pozor

### Kapacita odpovídá počtu aut, ne sdílenému instruktorovi

Happenee není automatický plánovač všech potřebných zdrojů. Rozpis sestavte podle nejužšího skutečného omezení a otestujte ho s provozovatelem.

### Slot počítá jen čas samotné jízdy

Přidejte ověření, instruktáž, předání, návrat, kontrolu, údržbu nebo nabíjení a přestávky obsluhy. Přestávka mezi sloty je samostatné nastavení s maximem 15 minut; delší rezervu započítejte do délky slotu. Jinak se zpoždění přenese do všech dalších rezervací.

### Nedostupný vůz zůstane rezervovatelný

Známou nedostupnost promítněte do slotů před otevřením registrace: v záložce **Sloty** přepněte dotčené sloty na **Neaktivní**. Když vůz vypadne až po rezervaci, nejdřív se s hostem domluvte na náhradě, teprve potom rezervaci upravte (v dialogu **Upravit účastníky** hosta z původního slotu odeberete a ve stejném dialogu nového slotu ho přidáte) a ověřte, že host změnu dostal.

### Rezervace se zaměňuje za bezpečnostní kontrolu

Oprávnění k jízdě, dokumenty, stav vozu a bezpečnostní podmínky ověřuje odpovědný člověk. Platná rezervace tuto kontrolu nenahrazuje.

## Související články

- [Nastavení rezervací v programu — auta, workshopy, doprovodný program](../03_obsah-a-zkusenost-ucastnika/10_nastaveni-rezervaci-v-programu.md)
- [Jak fungují časové sloty](../03_obsah-a-zkusenost-ucastnika/09_jak-funguji-casove-sloty.md)
- [Sestavení programu události — architektura](../03_obsah-a-zkusenost-ucastnika/06_sestaveni-programu-udalosti-architektura.md)
- [Nastavení workshopů a registrace na sessions](../03_obsah-a-zkusenost-ucastnika/08_nastaveni-workshopu-a-registrace-na-sessions.md)
- [Jak funguje check-in a skenování QR kódů](../05_den-akce-a-provoz/01_jak-funguje-check-in-a-skenovani-qr-kodu.md)

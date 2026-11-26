<!-- source: kb.cs.02.15 -->

---
title: "Ruční přidání účastníka do události"
description: "Všechny cesty, jak dostat člověka do události mimo registrační formulář — přiřazení kontaktu nebo skupiny, import, host bez registrace na místě — a co která udělá se stavem účastníka."
modules: ["ucastnici_skupiny_a_viditelnost", "registrace"]
last_updated: "2026-10-26"
version: 3
---

> [!info] Krátce
> Účastník se do události nemusí dostat jen registračním formulářem — můžete ho přidat sami. Cest je několik: **přiřazení existujícího kontaktu**, **přiřazení celé skupiny**, **hromadný import z Excelu** a na místě **založení hosta bez registrace v servisní aplikaci**. Zásadní je rozdíl mezi **přiřazením** a **registrací**: přiřazením dostanete člověka do seznamu události, ale zaregistrovaný tím není a e-maily závislé na registraci mu nepřijdou.

## Jak začít

Než někoho přidáte, rozhodněte, co má nastat:

- **Má se teprve rozhodnout, jestli přijde?** Přiřaďte kontakt k události a pošlete mu zvací e-mail. Registraci dokončí sám.
- **Už víte, že přijde, a nepotřebujete od něj data?** Přiřaďte ho k události a počítejte s tím, že zůstane ve stavu bez odpovědi, dokud formulář někdo nevyplní.
- **Stojí před vámi na místě?** Založte ho rovnou v servisní aplikaci jako hosta bez registrace a odbavte.

## Detail

### Přiřazení jednoho kontaktu

Ve **Správě kontaktů a skupin** buď najdete existující kontakt, nebo založíte nový tlačítkem **Přidat kontakt** (minimálně e-mail, dále jméno, příjmení, telefon, firma, preferovaný jazyk). Kontakt pak označíte a hromadnou akcí **Přiřazení k události** ho přidáte ke konkrétní události. Stejnou cestou ho můžete od události zase odřadit.

Kontakty jsou společné pro celý workspace — jeden kontakt může být přiřazený k libovolnému počtu událostí a jeho údaje se drží napříč nimi.

### Přiřazení celé skupiny

Rychlejší cesta u větších sad lidí: v záložce **Skupiny** kliknete na skupinu a přiřadíte ji celou k události. Přidají se všichni, kdo ve skupině jsou. Hodí se pro opakující se publikum (*vedení*, *partneři*, *interní tým*), které zvete znovu a znovu.

Pozor na to, že přiřazení je jednorázová akce, ne živá vazba. Když do skupiny přidáte člověka **po** přiřazení skupiny k události, do události se sám nepropíše.

### Hromadný import z Excelu

U desítek a stovek lidí použijte import ve **Správě kontaktů a skupin**. V šabloně můžete rovnou uvést skupinu (s prefixem `#`) a preferovaný jazyk. Po importu přiřadíte skupinu k události a máte hotovo. Detailní postup je v článku [Správa kontaktů a skupin ve workspace](03_sprava-kontaktu-a-skupin-ve-workspace.md).

### Host bez registrace na místě

Když někdo dorazí bez registrace, nemusíte ho zakládat v administraci. V servisní aplikaci v **Režimu obsluhy** je v záložce **Účastníci** tlačítko **Přidat účastníka** — zadáte e-mail, jméno, příjmení, firmu a pozici, uložíte, odbavíte a případně vytisknete jmenovku. Detail v článku [Jak funguje check-in a skenování QR kódů](../05_den-akce-a-provoz/01_jak-funguje-check-in-a-skenovani-qr-kodu.md).

### Ruční přidání na session nebo do časového slotu

Přidání do události a přidání na konkrétní session jsou dvě různé věci. U sessions s registrací a u časových slotů může organizátor účastníka doplnit ručně — v seznamu registrovaných ho vyhledá a přidá. Takto přidaní lidé jsou označení jako **Přiřazen organizátorem**, takže poznáte, kdo se přihlásil sám a koho jste tam dali vy.

### Co se stavem účastníka

Přiřazení kontaktu k události **není registrace**. Člověk se objeví v seznamu ve stavu bez odpovědi a teprve vyplněním formuláře (nebo nákupem vstupenky) se posune dál. To má dva praktické důsledky:

- **Potvrzovací e-mail s PDF vstupenkou a QR kódem mu nepřijde**, protože je navázaný na dokončenou registraci. Pokud potřebuje QR kód, pošlete mu ho z webového nástroje **Check-in (Prezence)** nebo ho odbavte podle jména.
- **V statistikách se počítá mezi pozvané, ne mezi registrované.** Čísla vám nebudou sedět, pokud tenhle rozdíl nedržíte.

Stavy jde v sekci **Registrace** upravit i ručně — například přepnout někoho na *Nezúčastním se*, když se odhlásí telefonicky.

## Na co si dát pozor

### Administrátora nebo autora události nelze odebrat v Registraci

Když v sekci **Registrace** odebíráte účastníka z události, systém odmítne odebrat kontakt, který je administrátorem nebo autorem této události. Hláška vysvětlí konkrétní důvod a kontakt zůstane přiřazený. Odebrání účastníka nemění vlastnictví události ani přístupy; potřebnou změnu řešte s osobou oprávněnou spravovat přístupy.

### Přiřazení se plete s registrací

Nejčastější omyl. Organizátor přiřadí 200 kontaktů, uvidí je v seznamu události a považuje událost za naplněnou — ale registrovaní nejsou, vstupenky nedostali a na check-inu nemají co skenovat. Přiřazení je pozvání, ne účast.

### Skupina se doplní až po přiřazení k události

Když přiřadíte skupinu k události a teprve pak do ní přidáte další lidi, noví členové v události nebudou. Po každém doplnění skupiny přiřazení zopakujte, nebo přidejte konkrétní kontakty jednotlivě.

### Ručně přidaný člověk nemá preferovaný jazyk

U kontaktu založeného narychlo se snadno vynechá jazyk — a zvací e-mail pak odejde ve výchozím jazyce workspace, i když má událost dvě jazykové verze. Při zakládání kontaktu jazyk vyplňte, ať už jednotlivě, nebo ve sloupci importní šablony.

### Host bez registrace založený na místě zůstane bez dalších údajů

Servisní aplikace sbírá jen základní údaje, aby odbavení bylo rychlé. Když od účastníka potřebujete odpovědi z registračního formuláře (dietní omezení, workshop, souhlasy), nedostanete je — host bez registrace formulářem neprošel. Počítejte s tím při reportu i při zpracování souhlasů.

<!-- source: kb.cs.06.04 -->

---
title: "Interpretace statistik vstupenek"
description: "Jak číst Statistiky vstupenek — prodané, zaplacené, nezaplacené, zdarma a stornované kusy, měsíční přehled, vztah k registracím a co z toho dostanete exportem."
modules: ["vstupenky_a_objednavky", "reporting_a_statistiky"]
last_updated: "2026-09-17"
version: 3
---

> [!info] Krátce
> **Statistiky vstupenek** ukazují prodej po jednotlivých typech vstupenek — kolik kusů se prodalo, kolik je zaplacených, nezaplacených, zdarma a stornovaných, a kolik lidí z nich má dokončenou registraci. Vedle toho je k dispozici měsíční přehled, takže vidíte, jak prodej nabíhal v čase. Je to samostatný pohled od statistik účastníků: ty počítají lidi a jejich stavy, tyhle počítají vstupenky a peníze.

## Jak začít

Statistiky vstupenek najdete u události mezi statistikami a reportingem; má smysl je otevírat jen tehdy, když máte zapnuté placené vstupenky.

Dřív než se začnete dívat na čísla, ujasněte si, na co se ptáte:

- **Kolik jsme prodali?** → počty po typech vstupenek.
- **Kolik z toho máme na účtu?** → rozdíl mezi zaplacenými a nezaplacenými.
- **Kolik lidí opravdu dorazí?** → počet registrovaných, ne prodaných.
- **Jak se prodej vyvíjel?** → měsíční přehled.

## Detail

### Jednotlivé kategorie

U každého typu vstupenky vidíte rozpad:

- **Prodané** — Celkový počet vydaných vstupenek daného typu.
- **Zaplacené** — Vstupenky s dokončenou platbou.
- **Nezaplacené** — Objednávka vznikla, peníze nedorazily — typicky zálohová faktura po splatnosti.
- **Zdarma** — Vstupenky vydané bez platby, například přes stoprocentní slevový kód nebo registrační odkaz.
- **Stornované** — Zrušené objednávky. Do prodeje se nepočítají, ale zůstávají v záznamu.
- **Registrovaní** — Kolik z těchhle vstupenek má dokončenou registraci účastníka.

Částky se zobrazují v měně, ve které se prodávalo — v korunách nebo v eurech podle nastavení vstupenky.

### Prodané versus registrovaní

Nejdůležitější dvojice čísel na celé obrazovce. U **registrace s doplněním informací** vzniká objednávka dřív než registrace: někdo koupí vstupenky pro pět kolegů, ale ti se teprve musí zaregistrovat. Dokud to neudělají, mají vstupenku, ale nemají QR kód ani odpovědi z formuláře.

Rozdíl mezi prodanými a registrovanými proto čtěte jako **frontu práce, ne jako chybu**. Čím blíž k události, tím naléhavější — nezaregistrovaní lidé se na check-inu řeší ručně. Konkrétní kupující s nedokončenou registrací najdete v sekci objednávek a jde je hromadně upozornit e-mailem.

### Nezaplacené vstupenky

Vysoký počet nezaplacených obvykle neznamená neplatiče, ale zálohové faktury, u kterých ještě běží splatnost. Podívejte se na data vystavení: pokud jsou čerstvá, je to normální stav. Pokud jsou po splatnosti a událost se blíží, je čas na připomínku (v **Objednávkách** nabídka **Upozornit e-mailem → Nezaplaceným** pošle kupujícím e-mail se zálohovou fakturou v příloze), nebo na rozhodnutí, jestli místo uvolníte.

### Měsíční přehled

Ukazuje, jak prodej nabíhal v čase. Používejte ho hlavně srovnávacím způsobem — proti minulému ročníku nebo proti očekávané křivce. Typický vzorec u konferencí jsou dvě vlny: jedna po spuštění prodeje a druhá v posledních dvou týdnech. Pokud vám druhá vlna nepřichází, je to signál pro poslední připomínkovou kampaň.

### Jak dostat čísla ven

Z administrace vedou dvě cesty exportu do Excelu: **po objednávkách** a **po vstupenkách**. První se hodí pro účetnictví (jedna objednávka = jeden doklad), druhá pro provoz (jedna vstupenka = jeden člověk u vstupu).

Veřejný ani sdílitelný odkaz na statistiky **neexistuje** — nikdo bez přístupu do administrace se na ně nepodívá. Když čísla potřebuje management, pošlete export nebo z něj udělejte shrnutí.

## Na co si dát pozor

### Prodané vstupenky se berou jako počet účastníků

Prodaná vstupenka neznamená zaregistrovaného člověka. U registrace s doplněním informací může jeden kupující držet pět vstupenek, u kterých ještě nikdo nevyplnil, kdo přijde. Pro kapacitu sálu počítejte s prodanými, pro přípravu jmenovek a check-inu s registrovanými.

### Stornované vstupenky se počítají do prodeje

Storno zůstává v záznamu, aby byla dohledatelná historie, ale do reálného prodeje nepatří. Když sestavujete výsledek události, ověřte, jestli s ním číslo, ze kterého vycházíte, počítá — a jestli počítá i s vratkami.

### Statistiky se zamění se statistikami účastníků

Dva různé pohledy na tutéž událost. Statistiky vstupenek počítají kusy a peníze, statistiky účastníků lidi a jejich stavy (pozvaný, registrovaný, odbavený). U placené události potřebujete oba a nikdy si nebudou sedět jedna ku jedné.

### Managementu se slíbí odkaz na živá čísla

Odkaz na statistiky, který by fungoval bez přístupu do administrace, v Happenee není. Domluvte se raději na pravidelném exportu — třeba jednou týdně — než abyste slibovali něco, co pak musíte vysvětlovat.

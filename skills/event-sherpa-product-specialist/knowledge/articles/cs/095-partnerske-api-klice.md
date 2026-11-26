# Partnerské API klíče

> Vydání klíče pro Partner API na záložce Integrace — sandboxový a produkční klíč, sedm oprávnění, zrušení klíče a kdy má napojení smysl místo importu.

- Článek v Help Centru: https://help.happenee.com/cs/articles/95-partnerske-api-klice
- English version: https://help.happenee.com/en/articles/95-setting-up-partner-api-keys
- Kolekce: Začínáme s Happenee
- Aktualizováno: 2026-08-07

---

> [!info] Krátce
> **Partner API klíče** jsou přístupové klíče, kterými se váš druhý systém — CRM, prodejní kanál, registrační nástroj — autorizuje proti Happenee. Vydáváte je v **Nastavení workspace** na záložce **Integrace** a ke každému zvlášť nastavujete **oprávnění**, takže integrace dostane přesně ten rozsah dat, který potřebuje. Typický důvod: účastníky a prodané vstupenky máte jinde a chcete je odbavit v Happenee, aniž byste je pokaždé importovali ručně.

## Jak začít

Než klíč vydáte, rozhodněte tři věci:

1. **Co má integrace umět.** Jen číst účastníky pro synchronizaci do CRM, nebo je i zakládat? Rozsah se promítne do oprávnění a ta se dají kdykoli zúžit.
2. **Sandbox, nebo produkce.** Sandboxový klíč slouží k vývoji a testům, produkční pro ostrý provoz. **Typ se po vytvoření nemění**, takže s tím počítejte dopředu — jinak budete zakládat klíč znovu.
3. **Kdo klíč dostane.** Klíč je přístup k datům účastníků. Patří vývojáři nebo dodavateli, který integraci staví, ne do sdíleného chatu.

Samotné vydání je krátké: na záložce **Integrace** kliknete na **Nový API klíč**, pojmenujete ho (název je jen pro vás — hodí se popsat, co se napojuje, třeba *CRM integrace*), vyberete typ, zaškrtnete oprávnění a potvrdíte tlačítkem **Vygenerovat klíč**.

Technický popis rozhraní — endpointy, formát požadavků, chybové stavy — najde váš vývojář v **dokumentaci Partner API**, na kterou vede odkaz přímo z info lišty záložky.

## Detail

### Kde záložka je a co spravuje

**Nastavení workspace → Integrace.** Je to workspace-level nastavení, takže klíč platí napříč všemi vašimi událostmi, ne jen pro jednu. Tomu odpovídá i rozsah oprávnění: když integraci pustíte ke čtení účastníků, vidí účastníky všech událostí ve workspace.

### Sandbox a produkce

U každého klíče volíte **Typ**:

- **Sandbox** — pro vývoj a testování napojení.
- **Produkce** — pro ostrý provoz.

Oddělení má praktický smysl: dodavatel může na integraci pracovat se sandboxovým klíčem, a produkční klíč dostane až ve chvíli, kdy je napojení hotové. Typ **v editaci klíče chybí** — po vytvoření se nemění, takže přechod z testu do provozu znamená vydat nový klíč.

### Sedm oprávnění

Oprávnění se zaškrtávají jednotlivě a ve výchozím stavu jsou při zakládání zapnutá všechna. Zúžení je na vás:

- **Události čtení** — seznam a detaily událostí ve workspace.
- **Účastníci čtení** — čtení účastnických záznamů.
- **Účastníci zápis** — zakládání a úpravy účastníků.
- **Program čtení** — čtení programu, tedy sessions.
- **Program zápis** — zápis do programu.
- **Certifikáty čtení** — čtení certifikátů.
- **Uživatelé čtení** — čtení uživatelských záznamů.

Zápis se nabízí jen u účastníků a programu; události, certifikáty a uživatelé jsou **jen pro čtení**. Rozdělení na čtení a zápis využijte — integrace, která má jen doplňovat data do vašeho CRM, nepotřebuje nic zapisovat zpět.

*(Anglická administrace používá u programu jiný termín: **Program čtení / zápis** je v ní **Sessions read / write**. Je to totéž oprávnění.)*

### Přehled vydaných klíčů

Tabulka na záložce ukazuje u každého klíče **Název**, **Typ**, **Klíč**, **Oprávnění**, **Stav** a datum vytvoření. Samotná hodnota klíče je maskovaná — vidíte jen poslední čtyři znaky, podle kterých klíč poznáte. **Celou hodnotu si proto uložte hned po vygenerování**, do správce hesel nebo rovnou do konfigurace systému, který se napojuje.

Stav je **Aktivní**, nebo **Zrušený**. Zrušený klíč z přehledu nezmizí, takže zůstává dohledatelné, co kdy existovalo.

### Úprava a zrušení klíče

U každého řádku jsou dvě akce. **Upravit API klíč** otevře panel, kde změníte název a oprávnění — hodí se, když integrace časem potřebuje víc nebo míň, než se čekalo. Druhá akce klíč **zruší**; klíč se nemaže, přepne se do stavu *Zrušený*.

Oprávnění zužujte průběžně. Když se změní rozsah integrace, je snazší upravit existující klíč než řešit, proč má dodavatel přístup k datům, která už nepotřebuje.

### Kdy API a kdy import

API má smysl, když data mezi systémy tečou **opakovaně a bez lidského zásahu** — průběžná synchronizace registrací, odbavení účastníků, kteří si koupili vstupenku jinde, aktualizace programu z externího nástroje.

Pro jednorázový přenos je import jednodušší a rychlejší: seznam kontaktů nahrajete z Excelu v **Správě kontaktů a skupin** a nepotřebujete vývojáře. Když si nejste jistí, začněte importem a k API sáhněte, teprve když se ukáže, že ho děláte pořád dokola.

## Na co si dát pozor

### Klíč se vygeneruje a nikam neuloží

V přehledu se pak ukazují jen poslední čtyři znaky. Zkopírujte si celou hodnotu okamžitě a předejte ji bezpečnou cestou — správcem hesel, ne e-mailem ani chatem. Když se hodnota ztratí, cesta ven je vydat nový klíč a starý zrušit.

### Typ se vybere „zatím na zkoušku" a pak se má měnit

Sandbox a produkce se po vytvoření nepřepínají. Když víte, že integrace půjde do ostrého provozu, počítejte s tím, že produkční klíč je samostatný záznam — a nechte ten sandboxový aktivní, dokud napojení nedoběhne.

### Klíč dostane všechna oprávnění, protože „ať to funguje"

Při zakládání jsou zaškrtnutá všechna, takže je snadné je tam nechat. Klíč ale platí pro celý workspace, tedy pro všechny události a všechny účastníky. Zaškrtněte jen to, co integrace opravdu dělá — a když si nejste jistí zápisem, začněte jen se čtením a doplňte ho, až se ukáže, že je potřeba.

### Klíč koluje v týmu

Klíč nemá vlastníka ani jméno člověka, takže po odchodu dodavatele není z čeho poznat, kdo ho má. Vydávejte proto samostatný klíč pro každé napojení a pojmenujte ho podle systému, ne podle člověka. Když spolupráce skončí, klíč zrušte.

## Související články
- [Nastavení workspace](https://help.happenee.com/cs/articles/73-nastaveni-workspace)
- [Správa kontaktů a skupin ve workspace](https://help.happenee.com/cs/articles/11-sprava-kontaktu-a-skupin-ve-workspace)
- [Jak funguje check-in a skenování QR kódů](https://help.happenee.com/cs/articles/47-jak-funguje-check-in-a-skenovani-qr-kodu)

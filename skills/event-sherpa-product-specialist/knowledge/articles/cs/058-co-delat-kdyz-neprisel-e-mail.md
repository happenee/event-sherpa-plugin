# Co dělat, když nepřišel e-mail

> Postup, když účastník hlásí nedoručený zvací, potvrzovací e-mail nebo kampaň.

- Článek v Help Centru: https://help.happenee.com/cs/articles/58-co-delat-kdyz-neprisel-e-mail
- English version: https://help.happenee.com/en/articles/58-what-to-do-when-an-e-mail-does-not-arrive
- Kolekce: Řešení problémů
- Aktualizováno: 2026-09-21

---

> [!info] Krátce
> Účastník hlásí, že mu nedorazil zvací e-mail, potvrzovací e-mail nebo e-mailová kampaň. Většinou nejde o výpadek systému — e-mail se buď nedostal ke správné adrese, šel do spamu, nebo nebyl vůbec odeslán (chybějící jazyková varianta, nepřiřazený kontakt, špatný stav účastníka).

## Jak začít

Otevřete **Prezenci** nebo **Registraci** a najděte účastníka. Zkontrolujte jeho e-mail, stav přihlášení a preferovaný jazyk — tím zúžíte příčinu.

## Detail

### Typické příčiny

- **Špatný e-mail na účastníkovi** — překlep, zastaralá firemní adresa.
- **Spam nebo záložka Hromadné / Promoce** — e-maily jsou odesílány z domény `invitation.happenee.com`; účastník to nemusí znát.
- **Kampaň neodešla kvůli chybějící jazykové verzi** — pokud se při odeslání objevil dialog *Kampaň není připravena k odeslání*, rozesílka nevznikla a na záložce **Rozesílky** ji nenajdete. Dialog vypisuje jazyky, kterým chybí předmět nebo obsah.
- **Zvací e-mail ještě nebyl odeslán** — zvací e-mail není automatický, musí se poslat ručně (individuálně nebo hromadně).
- **Účastník není přiřazen k události** — zvací e-maily a kampaně chodí jen přiřazeným kontaktům.
- **Stav účastníka je *Nezúčastním se* nebo odhlášen** — potvrzovací e-mail se neodesílá.
- **U placených vstupenek** — kupující zaplatil, ale účastník ještě neprošel registračním formulářem; vstupenka s QR kódem se generuje teprve po dokončení registrace.

### Jak to opravit

- **Potvrzovací e-mail po chybě** — v **Prezenci** najděte účastníka, opravte e-mail, přepněte stav na *Zúčastním se* a znovu mu odešlete potvrzovací e-mail (zaškrtávátko při změně stavu).
- **Nedokončená registrace u placené vstupenky** — v **Objednávkách** rozbalte konkrétní objednávku a použijte **Upozornit** u vstupenky. Hromadně: nabídka **Upozornit e-mailem → Neregistrovaným** vpravo nahoře nad seznamem objednávek. Odkaz, který odešel v posledních pěti minutách, se znovu nepošle.
- **Kampaň** — u odeslané kampaně otevřete záložku **Rozesílky**, panel **Doposlat kampaň nově přiřazeným** a tlačítkem **Nově přiřazení** oslovte účastníky, kteří v době rozesílky u události ani ve skupině ještě nebyli.
- **Ověření konkrétní adresy** — na záložce **Rozesílky** otevřete u dané rozesílky **E-maily**. U každého příjemce je vidět, zda byl e-mail odeslán, doručen a otevřen. Stav *Nedoručeno* v grafu **Stav rozesílky** znamená problém s doručením (překlep v adrese, plná nebo zrušená schránka, blokace na straně příjemce) — ten doposláním nevyřešíte, nejdřív opravte adresu.
- **Kampaň zastavená kvůli chybějícímu jazyku** — přepněte **Jazyk obsahu** na jazyky, které dialog vypsal, doplňte předmět a obsah a kampaň odešlete znovu.

### Prevence

- Vyplňujte obsah e-mailů a kampaní **vždy ve všech aktivních jazycích**, i když si myslíte, že všichni účastníci čtou jeden konkrétní jazyk.
- U placených událostí kontrolujte v **Objednávkách** rozdíl mezi *prodáno* a *zaregistrováno* — rozdíl = ti, kdo nedokončili registraci, kterým stačí doposlat odkaz.
- Před hromadnou rozesílkou vždy použijte **test kampaně** / **zkušební zvací e-mail** na vlastní adresu.
- Odbavení jménem v účastnické aplikaci dnes není — v den události je praktické poslat kampaní *připomenutí s QR kódem* hodinu před začátkem, aby měli účastníci vstupenku po ruce i bez přístupu do aplikace.

## Na co si dát pozor

### Účastník říká *nic mi nepřišlo*, organizátor znovu posílá — přijde druhá kopie, ale původní e-mail se mezitím našel ve spamu

Nejdřív se účastníka zeptejte na složku *Hromadné* / *Promoce* / *Spam* a na doménu `invitation.happenee.com`. Teprve potom opakujte odeslání.

### U placených vstupenek organizátor čeká, že po zaplacení má účastník automaticky vstupenku. Platba proběhla, ale vstupenka nedošla

U *registrace s doplněním informací* je vstupenka vygenerována až po dokončení registračního formuláře. Zkontrolujte stav v **Objednávkách** a případně znovu odešlete odkaz.

## Související články

- [Jak funguje zvací e-mail](https://help.happenee.com/cs/articles/39-jak-funguje-zvaci-e-mail)
- [Jak funguje potvrzovací e-mail](https://help.happenee.com/cs/articles/40-jak-funguje-potvrzovaci-e-mail)
- [Vytvoření a odeslání e-mailové kampaně](https://help.happenee.com/cs/articles/41-vytvoreni-a-odeslani-e-mailove-kampane)
- [Správa objednávek a faktur](https://help.happenee.com/cs/articles/19-sprava-objednavek-a-faktur)
- [Sledování doručitelnosti e-mailů a kampaní](https://help.happenee.com/cs/articles/80-sledovani-dorucitelnosti-e-mailu-a-kampani)

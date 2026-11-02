# Planning

Met de planning laat de gebruiker gebeurtenissen volgens een tijdschema plaatsvinden. Een fabriek start bijvoorbeeld op werkdagen om 8:00 de machines en stopt ze om 18:00.

Klik op “Planning” in de “standaardlijst”; het dialoogvenster van de planning verschijnt, zoals hieronder.

<img src="../../setting/schedule.files/schedule706.png" width="728" />

 Afbeelding 7-49 Dialoogvenster planning

Klik op de knop “Nieuw”; een nieuw dialoogvenster verschijnt, zoals hieronder. Eerst wordt de pagina “Algemeen” getoond.

<img src="../../setting/schedule.files/schedule984.png" width="694" />

  Afbeelding 7-50 Dialoogvenster nieuwe planning

• Beschrijving:

Voer hier een tekst in die de functie van deze planning verduidelijkt.

• Start-/eindactie uitvoeren bij inschakelen:

Wordt de voeding (HMI) na de starttijd ingeschakeld, dan wordt de start-/eindactie uitgevoerd.

• Doeladres:

Voer het type en het doeladres in; de waarde wordt op het start-/eindtijdstip naar dit adres geschreven.

• Schrijfbewerking:

Type “Constante” of “Adres”. Bij “Constante” hoort de waarde die naar het doeladres wordt geschreven; bij “Adres” hoort een adresveld waarvan de waarde op het start-/eindtijdstip naar het doeladres wordt geschreven.

• Eindbewerking gebruiken:

Is deze optie aangevinkt, dan wordt op het eindtijdstip de waarde van de schrijfbewerking naar het doeladres geschreven.

 Klik na de pagina “Algemeen” op de pagina “Tijdslimiet”, zoals hieronder.

<img src="../../setting/schedule.files/schedule2016.png" width="694" />

  Afbeelding 7-51 Pagina “Tijdslimiet”

• Constante: vink het start-/eindtijdstip aan; op dat tijdstip wordt de bijbehorende schrijfbewerking uitgevoerd.

• Adres: een reeks adressen bestuurt de start- en eindtijd van de planning, zoals hieronder.

 <img src="../../setting/schedule.files/schedule2396.png" width="693" />

 Afbeelding 7-52 Besturing via adres

Is het adres bijvoorbeeld LW0, dan worden LW0~LW10 voor de planning gebruikt.

LW0: besturingsadres. Bij LW0 == 1 worden de plantijden in de HMI geladen en begint het planningselement te werken. Na het laden wordt LW0 op 0 gezet;

LW1: planningsstatus. Zijn de plantijden geladen (LW0==0), dan wordt LW1 op 1 gezet.

LW2: actiemodus. Bij LW2 = 1 wordt de schrijfactie uitgevoerd als de huidige tijd na de starttijd ligt. Bij LW2 = 0 wordt de start-/eindactie uitgevoerd als de huidige tijd gelijk is aan de start-/eindtijd.

LW3: de dag van de starttijd; de waarde is 2^(nummer van de weekdag), LW3 = (0,1,4,8,16,32,64)

LW4~LW6: uren, minuten en seconden van de starttijd.

LW7: de dag van de eindtijd; de waarde is 2^(nummer van de weekdag), LW3 = (0,1,4,8,16,32,64)

LW8~LW10: uren, minuten en seconden van de eindtijd.

Evenzo worden, als LWn het besturingsadres is, LWn~LWn+10 voor de planning gebruikt, zoals hierboven.

**Tip:** bij “Adres” moet u na het instellen van start- en eindtijd het besturingsadres op 1 zetten om de planning te laden; anders werkt ze niet.

Pagina “Blokkering”, zoals hieronder:

<img src="../../setting/schedule.files/schedule3691.png" width="694" />

 Afbeelding 7-53 Pagina “Blokkering”

Is “Blokkering gebruiken” aangevinkt, dan werkt de planning alleen als het bitadres aan de voorwaarde (0 of 1) voldoet.

Klik na het instellen van de parameters op “OK” om een planningselement aan te maken, zoals hieronder.

<img src="../../setting/schedule.files/schedule4054.png" width="732" />

  Afbeelding 7-50 Aangemaakte planning

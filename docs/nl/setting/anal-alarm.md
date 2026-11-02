# Analoge alarmregistratie

Open het dialoogvenster met de analoge alarminstellingen, zoals in afbeelding 7-28:

Er zijn twee typen: numerieke waarde en numerieke vergelijking.

<img src="../../setting/anal-alarm.files/image002.jpg" width="145" />

Het alarm met numerieke vergelijking ziet er zo uit:

<img src="../../setting/anal-alarm.files/image007.jpg" width="599" />

Afbeelding 7-28    Dialoogvenster analoge alarmregistratie

Om een analoog alarm te gebruiken, gaat u als volgt te werk:

• Voer eerst het te bewaken adres in bij “Leesadres”. Hier wordt het interne adres LW1 gebruikt.

• Kies bij “Aantal” het totale aantal alarmen, dus het totale aantal adressen; het gegevenstype bepaalt hoe de adressen worden gelezen. Standaard is elk adres een opeenvolgend 16-bits gegeven, maar het gegevenstype kan worden gewijzigd. In afbeelding 7-28 is LW1 een 32-bits positief geheel getal en zijn LW3 en LW4 16-bits positieve gehele getallen. Bij 32-bits gegevens is het volgende adres dus het vorige plus 2, bij 16-bits gegevens het vorige plus 1.

• De gebruiker kan de “Scantijd” van het alarm instellen, dus de scanfrequentie.

• Klik op elk item om een waarde in te voeren in het veld “Grens” rechts, en voer daarna de tekst (alarminhoud) in het veld “Tekst” in. Hier wordt aangenomen dat de berichten zijn zoals in afbeelding 7-28: elke adreswaarde valt in een van vier bereiken: Laag, Laag-laag, Hoog, Hoog-hoog.

Zoals in afbeelding 7-29:

<img src="../../setting/anal-alarm.files/image004.jpg" width="566" />

Afbeelding 7-29    De vier bereiken voor het adres LW1

• Laag-laag: is de waarde kleiner dan deze grens en is “Gebruiken” aangevinkt, dan verschijnt de alarminformatie in de “alarmweergave” of de “dynamische alarmbalk”;

• Laag: is de waarde niet kleiner dan de grens “Laag-laag” maar kleiner dan de grens “Laag” en is “Gebruiken” aangevinkt, dan verschijnt de alarminformatie in de “alarmweergave” of de “dynamische alarmbalk”;

• Hoog: is de waarde groter dan de grens “Hoog” maar niet groter dan de grens “Hoog-hoog” en is “Gebruiken” aangevinkt, dan verschijnt de alarminformatie in de “alarmweergave” of de “dynamische alarmbalk”.

• Hoog-hoog: is de waarde groter dan deze grens en is “Gebruiken” aangevinkt, dan verschijnt de alarminformatie in de “alarmweergave” of de “dynamische alarmbalk”.

• U-export: exporteert de alarminstellingen

• U-import: importeert de alarminstellingen

Zie voor “Gebruiken” de “Digitale alarmregistratie”.

Een alarm met numerieke waarde treedt op als de waarde de ingestelde grens bereikt.

De instellingen zijn als volgt: het alarm wordt geactiveerd als de waarde 1, 12, 30 en 40 bereikt.

<img src="../../setting/anal-alarm.files/image006.jpg" width="130" />

Opmerking: de HMI's van de HM-serie ondersteunen maximaal 10 analoge alarmen.

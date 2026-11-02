# Meerstandenknop

De meerstandenknop en de meerstandenlamp werken vrijwel gelijk; het enige verschil is dat de meerstandenknop ook waarden kan invoeren, naast de weergave. Werkwijze:

Klik op het pictogram<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button271.png" width="31" /> in de werkbalk om het dialoogvenster van afbeelding 4-87 te openen.

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button336.png" width="663" />

Afbeelding 4-87 Dialoogvenster Meerstandenknop

• Status: de gebruiker kan per status de statuswaarde, randkleur, voorgrondkleur, achtergrondkleur en het patroon van het object wijzigen

• Statustype: (aangenomen dat de ingevoerde waarde n is)

• Waarde: de geschreven waarde ligt tussen nul en het totale aantal statussen.

• Registerbit: de geschreven waarde is 2 tot de macht n.

E.g:

Kies “Waarde” als statustype, “Toetsenbordinvoer” als modus en LW3 als schrijfadres, vink “Bewakingsadres gelijk aan schrijfadres” aan en zet het totale aantal statussen op 8. Klik op “OK” om het object aan het scherm toe te voegen en sla het project op.

Klik in de simulatie of op het scherm op het object; er verschijnt een toetsenbord om een statuswaarde in te voeren. Voert u 3 in, dan wordt 2 tot de macht 3 naar LW3 geschreven en wordt de tekst van status 3 getoond (ingesteld op de pagina “Tekst”). Omgekeerd: is LW3 gelijk aan 8, dan toont het object de tekst van status 3. Is LW3 gelijk aan 5, dan toont het object geen status.

• Aangepaste statuswaarden: met deze optie verschijnt een knop “Statuswaarden definiëren...”, zoals in afbeelding 4-88:

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button1611.png" width="662" />

Afbeelding 4-88 Meerstandenknop met aangepaste statuswaarden

Klik op “Statuswaarden definiëren...”; het venster “Aangepaste statuswaarden” verschijnt, zoals in afbeelding 4-89:

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button1799.png" width="333" />

Afbeelding 4-89 Dialoogvenster Statuswaarden definiëren

In dit venster is de kolom “S #” de statuskolom. Na het kiezen van een rij is de waarde bij “S#” de waarde van die status; dubbelklik om de waarde in te voeren.

Kies bijvoorbeeld “Aangepaste statuswaarden” als statustype, “Toetsenbordinvoer” als modus en LW3 als schrijfadres, vink “Bewakingsadres gelijk aan schrijfadres” aan en zet het totale aantal statussen op 8. Klik op “OK” om het object aan het scherm toe te voegen en sla het project op. Klik in de simulatie of op het scherm op het object; er verschijnt een toetsenbord om een statuswaarde in te voeren. Voert u 1 in, dan wordt 22 naar LW3 geschreven en wordt de tekst van status 1 getoond (ingesteld op de pagina “Tekst”). Omgekeerd: is LW3 gelijk aan 33, dan toont het object de tekst van status 2. Is LW3 gelijk aan 2, dan toont het object geen status.

• Modus: zes opties: “Toetsenbordinvoer”, “Constante”, “Verhogen”, “Verlagen”, “Cyclisch verhogen” en “Cyclisch verlagen”.

• Toetsenbordinvoer: alle drie opties van “Statustype” zijn mogelijk. In de simulatie of op het scherm verschijnt bij een klik op het object een toetsenbord om de waarde in te voeren, zoals in afbeelding 4-90:

![](../../../configuration-guide/basic-control/multiple-button.files/001.png)

Afbeelding 4-90 Toetsenbord

• Constante: van de drie opties van “Statustype” is alleen “Waarde” mogelijk. Er verschijnt een veld “Constante” om de waarde in te stellen. In de simulatie of op het scherm wordt bij een klik op het object deze constante geschreven

• Verhogen: van de drie opties van “Statustype” is alleen “Waarde” mogelijk. In de simulatie of op het scherm verhoogt elke klik de status met 1; bij het bereiken van het totale aantal statussen stopt het verhogen.

• Verlagen: van de drie opties van “Statustype” is alleen “Waarde” mogelijk. In de simulatie of op het scherm verlaagt elke klik de status met 1; bij de grens stopt het verlagen.

• Cyclisch verhogen: van de drie opties van “Statustype” is alleen “Waarde” mogelijk. In de simulatie of op het scherm verhoogt elke klik de status met 1; na het totale aantal statussen keert hij terug naar status 0.

• Cyclisch verlagen: van de drie opties van “Statustype” is alleen “Waarde” mogelijk. In de simulatie of op het scherm verlaagt elke klik de status met 1; voorbij de grens keert hij terug naar de hoogste status.

• Gegevenstype: gegevenstype van het schrijf- en bewakingsadres (lezen)

• Bewakingsadres: leesadres waarvan de waarde de getoonde status van het object bepaalt.

• Totaal aantal statussen: maximaal aantal statussen

• Script gebruiken: indien aangevinkt wordt bij een klik op het object in de simulatie of op het scherm het gekozen script uitgevoerd.

<img src="../../../configuration-guide/basic-control/multiple-button.files/multiple-button5026.png" width="130" />

Opmerking: zie voor vorm, randkleur, voorgrondkleur, achtergrondkleur en patroon het object “Bit-knop”.

Opmerking: zie voor de pagina's “Tekst” en “Afbeelding” het object “Meerstandenlamp”.

Opmerking: zie voor de pagina's “Geavanceerd” en “Zichtbaarheid” het object “Bit-knop”; zie voor sneltoetsen de bit-knop.

Klik na de instellingen op “OK” om het object aan het werkgebied (het scherm) toe te voegen

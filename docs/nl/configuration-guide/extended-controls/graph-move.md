# Grafische beweging

Met het object grafische beweging beweegt een galerijelement of afbeeldingsbestand in een bepaalde richting over het scherm, afhankelijk van de waarde van de gekoppelde variabelen. Zo ontstaan animaties op het scherm.

Het object grafische beweging toevoegen en de eigenschappen wijzigen:

Kies de knop Grafische beweging<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move351.png" width="35" /> in de werkbalk, stel de eigenschappen in het dialoogvenster in en klik op “OK”, zoals in afbeelding 4-61:

<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move459.png" width="662" />

Afbeelding 4-61 Dialoogvenster Grafische beweging

• Afbeeldingskeuze:

Kies op de pagina “Afbeeldingen” de afbeelding die beweegt; die kan ook aangepast zijn.

• Bewakingsadres:

Het bewakingsadres van de beweging neemt drie adressen in: totaal aantal statussen, waarde van de X-as en waarde van de Y-as. Met intern adres LW1 en gegevenstype 16 bits besturen LW1, LW2 en LW3 direct het totale aantal statussen, de X-beweging en de Y-beweging; bij 32 bits staat het totale aantal statussen in LW1, de X-coördinaat in LW3 en de Y-coördinaat in LW5.

• Methode: in de volgende voorbeelden is het bewakingsadres het interne adres LW1 met gegevenstype 16 bits. De bewegingssoorten:

• Horizontaal langs de X-as: het element beweegt alleen horizontaal, niet verticaal, en niet buiten de onder- en bovengrens van de X-as. Het totale aantal statussen is de waarde van LW1 en LW2 is de X-coördinaat.

• Verticaal langs de Y-as: het element beweegt alleen verticaal, niet horizontaal, en niet buiten de onder- en bovengrens van de Y-as. Het totale aantal statussen is de waarde van LW1 en LW2 is de Y-coördinaat.

• Tegelijk horizontaal en verticaal: het element beweegt tegelijk horizontaal en verticaal, binnen de grenzen van de X- en Y-as. Het totale aantal statussen is de waarde van LW1, LW2 is de X-coördinaat en LW3 de Y-coördinaat.

• Proportioneel horizontaal langs de X-as: het element beweegt alleen horizontaal, niet verticaal, en niet buiten de onder- en bovengrens van de X-as. Het totale aantal statussen is de waarde van LW1 en LW2 is de X-coördinaat.

• Proportioneel verticaal langs de Y-as: het element beweegt alleen verticaal, niet horizontaal, en niet buiten de onder- en bovengrens van de Y-as. Het totale aantal statussen is de waarde van LW1 en LW2 is de coördinaat.

• Omgekeerd proportioneel horizontaal langs de X-as: het element beweegt alleen horizontaal, niet verticaal, en niet buiten de onder- en bovengrens van de X-as. Het totale aantal statussen is de waarde van LW1 en LW2 is de X-coördinaat.

• Omgekeerd proportioneel verticaal langs de Y-as: het element beweegt alleen verticaal, niet horizontaal, en niet buiten de onder- en bovengrens van de Y-as. Het totale aantal statussen is de waarde van LW1 en LW2 is de coördinaat.

<img src="../../../configuration-guide/extended-controls/graph-move.files/graph-move3614.png" width="130" />

• Zie voor de pagina's “Tekst” en “Afbeelding” het object “Meerstandenlamp”.

• Zie voor de pagina “Zichtbaarheid” het object “Bit-knop”.

• De waarden van de laatste twee bewakingsadressen bepalen de positie van het element.

• De maximale coördinaat van de X- / Y-as is de maximale schermgrootte.

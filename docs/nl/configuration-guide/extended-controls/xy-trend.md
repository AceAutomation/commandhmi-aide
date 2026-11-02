# XY-trendgrafiek

**Inleiding XY-trendgrafiek:**

Toont dynamisch en continu de waarden van variabelen.

Tekent meerdere referentiecurves, met de waarden van twee opeenvolgende registers als horizontale en verticale coördinaat, om hun verband nauwkeurig en intuïtief te volgen.

Er kunnen tot 8 polylijnen (curves) worden getoond.

De XY-trendgrafiek wordt toegevoegd en ingesteld zoals de trendgrafiek; zie de pagina “Trendgrafiek”. Pictogram:<img src="../../../configuration-guide/extended-controls/xy-trend.files/image002.jpg" width="36" />

Open het eigenschappenvenster van de XY-trend; zie de instellingen van de “Trendgrafiek”. Verschil: in de trendgrafiek staat elke curve voor de waarde van opeenvolgende adressen vanaf het schrijfadres; in de XY-grafiek staat elke curve voor de waarden van twee opeenvolgende adressen.

**Gebruik van de XY-trendgrafiek:**

Kleur: kleur van de detectielijn (referentielijn).

Detectieadres: de waarde van de huidige detectielijn wordt naar dit adres geschreven.

Bij gegevenstype 16 bits en 4 gegevensgroepen worden, als het ingevoerde adres LW3 is, 8 opeenvolgende waarden gelezen:

LW3: curve 1, waarde X-as

LW4: curve 1, waarde Y-as

LW5: curve 2, waarde X-as

LW6: curve 2, waarde Y-as

LW7: curve 3, waarde X-as

LW8: curve 3, waarde Y-as

LW9: curve 4, waarde X-as

LW10: curve 4, waarde Y-as

Gelezen worden LW3-LW10, dus 8 adressen. Met 16-bits gegevens en N groepen worden dus 2 \* N opeenvolgende adressen gelezen volgens de adresregels van de PLC.

Bij gegevenstype 32 bits en 3 groepen worden, als het ingevoerde adres LW3 is, de volgende waarden gelezen:

LW3: curve 1, waarde X-as

LW5: curve 1, waarde Y-as

LW7: curve 2, waarde X-as

LW9: curve 2, waarde Y-as

LW11: curve 3, waarde X-as

LW13: curve 3, waarde Y-as

Gelezen worden LW3-LW14, dus 12 adressen. Met 32-bits gegevens en N groepen worden dus 2 \* N waarden gelezen door het adres telkens met 2 te verhogen volgens de adresregels van de PLC.

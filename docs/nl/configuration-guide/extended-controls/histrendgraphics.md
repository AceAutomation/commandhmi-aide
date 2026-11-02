# Historische trendgrafiek

• Inleiding: deze trendgrafiek wordt gebruikt samen met de “[Historische gegevensverzamelaar](../../setting/history-data.md)” in de projectbeheerder; hij toont de waarden van de gegevens in de verzamelaar.

• Inleiding XY-trendgrafiek:

Toont dynamisch en continu de waarden van variabelen.

Toont meerdere referentiecurves, met de tijd op de X-as en de adreswaarde op de Y-as, om het verloop van een waarde over een periode nauwkeurig en intuïtief te beoordelen.

Er kunnen tot 8 polylijnen (curves) worden getoond.

• De trendgrafiek toevoegen en de eigenschappen wijzigen:

1. Kies het trendpictogram<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image002.jpg" width="34" /> in de werkbalk; het eigenschappenvenster van de historische trend verschijnt, zoals in afbeelding 4-53:

Afbeelding 4-53    Pagina “Algemeen” van de historische trend

• Achtergrondkleur: wijzigt de achtergrondkleur van de grafiek. De wijziging is niet direct zichtbaar; klik op “OK” om ze toe te passen.

• Transparantie: wijzigt de transparantie van de achtergrondkleur.

• Gegevensverzameling: standaard de “Historische gegevensverzamelaar” in de projectbeheerder. CommandHMI ondersteunt meerdere groepen historische gegevens; met deze optie kiest de ontwerper welke groep wordt gebruikt. Zoals hieronder:

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image004.jpg" width="774" />

• Aantal curves: aantal getoonde curves; maximaal 8.

• Kleur: kleur van het spoor van de curve.

• Besturingsadres gebruiken: bepaalt of een besturingsadres wordt gebruikt. Het neemt 28 offsets in en bestuurt de weergave van elke curve, maximum en minimum, eindtijd, periode (minuten), maximum en minimum bij alleen de Y-as, of de Y-as wordt getoond en de terugkeer naar de beginstatus.

|                |                                                                                                         |
|----------------|---------------------------------------------------------------------------------------------------------|
| Adresoffset | Door het besturingsregister bestuurd element                                                           |
| 0              | Totaal aantal getoonde curves                                                                 |
| 1              | <span id="OLE_LINK534"></span><span id="OLE_LINK533"></span>Curve 1 tonen                        |
| 2              | Curve 2 tonen                                                                                    |
| 3              | Curve 3 tonen                                                                                    |
| 4              | Curve 4 tonen                                                                                    |
| 5              | Curve 5 tonen                                                                                    |
| 6              | Curve 6 tonen                                                                                    |
| 7              | Curve 7 tonen                                                                                    |
| 8              | Curve 8 tonen                                                                                    |
| 9              | Maximale waarde op de Y-as                                                                                 |
| 10             |                                                                                                         |
| 11             | Minimale waarde op de Y-as                                                                              |
| 12             |                                                                                                         |
| 13             | 0: standaard maximum en minimum; 1: ingestelde boven- en ondergrens gebruiken |
| 14             | Begintijd van de zoekopdracht                                                                                        |
| 15             |                                                                                                         |
| 16             |                                                                                                         |
| 17             |                                                                                                         |
| 18             |                                                                                                         |
| 19             |                                                                                                         |
| 20             | Eindtijd van de zoekopdracht                                                                                          |
| 21             |                                                                                                         |
| 22             |                                                                                                         |
| 23             |                                                                                                         |
| 24             |                                                                                                         |
| 25             |                                                                                                         |
| 26             | Bij 1 wordt de zoekopdracht uitgevoerd; keert automatisch terug naar 0                                 |
| 27             | Bij 1 terug naar de actuele status; keert automatisch terug naar 0                             |

Besturingsadres tonen:

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/2020-03-23_091355.jpg" width="774" />

**Detectielijn**

• Activeren: geeft aan of de detectielijn (referentielijn) actief is.

• Kleur: kleur van de detectielijn (referentielijn).

• Detectieadres: de waarde bij de huidige detectielijn wordt naar dit register geschreven.

• Detectietijd tonen: de tijd van de huidige positie van de detectielijn wordt naar dit register geschreven; weergave met een ASCII-weergaveobject van in totaal 19 woorden.

• Tijdsverschil van het detectiepunt: het verschil tussen de tijd van de huidige positie van de detectielijn en de begintijd wordt naar dit adres geschreven; weergave met een numeriek weergaveobject, 16-bits geheel getal, in seconden.

2\. De pagina “Curves” van de historische trendgrafiek staat in afbeelding 4-54.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image005.jpg" width="774" />

Afbeelding 4-54    Tabblad “Curves” van de historische trend

Hier stelt u maximum, minimum, stijl en kleur van elke curve in. De gegevensbron is de “[Historische gegevensverzamelaar](../../setting/history-data.md)” in de projectbeheerder. Elke curve kan een andere bron hebben.

3\. De pagina “XY-assen” van de historische trendgrafiek staat in afbeelding 4-55.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image006.jpg" width="774" />

Afbeelding 4-55    Tabblad “XY-assen” van de historische trend

**X-as**

• Schaal tonen: of de schaal van de X-as wordt getoond.

• Y-raster tonen: of het raster van de Y-as wordt getoond.

• Kleur as / schaal: wijzigt de kleur van de X-as / schaal.

• Rasterkleur: wijzigt de kleur van het raster van de X-as.

• Hoofdverdelingen: hoofdverdelingen van de X-as.

• Subverdelingen: subverdelingen van de X-as.

• Tijd tonen: formaat en lettergrootte van de tijd.

• Tijdbereik: getoond tijdsinterval in de grafiek.

**Y-as**

• Schaal tonen: of de schaal van de Y-as wordt getoond.

• X-raster tonen: of het raster van de X-as wordt getoond.

• Kleur as / schaal: wijzigt de kleur van de Y-as / schaal.

• Rasterkleur: wijzigt de kleur van het raster van de Y-as.

• Hoofdverdelingen: aantal hoofdverdelingen van de Y-as.

• Subverdelingen: aantal subverdelingen van de Y-as.

• Markeringen tonen: of de markeringen van de Y-schaal worden getoond.

• Lettergrootte: wijzigt de lettergrootte van de Y-schaal.

• Minimum: minimale waarde van de Y-schaal.

• Maximum: maximale waarde van de Y-schaal.

• Totaal: maximaal aantal cijfers van de gegevens.

• Decimalen: maximaal aantal cijfers na de komma.

• Meerdere assen tonen: of meerdere assen worden getoond.

<img src="../../../configuration-guide/extended-controls/histrendgraphics.files/image007.jpg" width="130" />

Zie voor de pagina “Zichtbaarheid” het object “Bit-knop”.

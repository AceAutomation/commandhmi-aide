# Trendgrafiek

**Inleiding trendgrafiek:**

<span id="OLE_LINK525"></span><span id="OLE_LINK526"></span>Toont dynamisch en continu de waarden van variabelen.

Tekent referentiecurves van meerdere gegevens, met de tijd op de horizontale en de waarde op de verticale as, om het verloop van een waarde over een periode nauwkeurig en intuïtief te beoordelen.

Er kunnen tot 8 polylijnen (curves) worden getoond.

Eigenschappen van de trendgrafiek:

1. Kies het pictogram trendgrafiek<img src="../../../configuration-guide/extended-controls/trend.files/image002.jpg" width="35" /> in de werkbalk; het eigenschappenvenster verschijnt, zoals in afbeelding 4-50

Afbeelding 4-50    Algemeen dialoogvenster trendgrafiek

• Achtergrondkleur: wijzigt de achtergrondkleur van de grafiek. Het effect is pas zichtbaar na een klik op “OK”.

• Gegevenstype: er zijn 7 gegevenstypen beschikbaar.

• Leestriggerbit: de curve loopt alleen als het “adres van de leestriggerbit” 1 is.

• Aantal curves: aantal curves, maximaal 8.

• Leestriggerbit automatisch resetten: is het leesadres 1, dan wordt het op 0 gezet.

• Punten per groep: <span id="OLE_LINK492"></span><span id="OLE_LINK493"></span>aantal gegevens op de <span id="OLE_LINK494"></span><span id="OLE_LINK495"></span>X-as.

• Bemonsteringstijd: bemonsteringsfrequentie.

• Leesadres: de waarde is de waarde van elke curve op de Y-as. Afhankelijk van het aantal groepen en het gegevenstype worden de adressen aaneengesloten (16-bits gegevens) of met tussenruimte (32-bits gegevens) gelezen.

• Variabel aantal punten: de “punten per groep” worden dynamisch bepaald door de waarde van een adres. Met deze optie is de standaardwaarde van het adres de beginwaarde van de punten per groep.

**Detectielijn**

• Activeren: geeft aan of de detectielijn (referentielijn) actief is.

• Kleur: kleur van de detectielijn (referentielijn).

<span id="OLE_LINK527"></span><span id="OLE_LINK528"></span><span id="OLE_LINK543"></span>• Detectieadres: de waarde van de huidige detectielijn (referentielijn) wordt naar dit adres geschreven.

• Besturingsadres gebruiken: bepaalt dynamisch minimum en maximum van de Y-as volgens de waarde van het besturingsadres. Dit adres neemt vijf opeenvolgende offsets in: het wijzigt minimum en maximum van de Y-schaal en bepaalt of de beginstatus wordt hersteld.

|                |                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Adresoffset | Door het besturingsregister bestuurd element                                                                                                                            |
| 0              | Lage 16 bits van het minimum                                                                                                                                |
| 1              | Hoge 16 bits van het minimum                                                                                                                                |
| 2              | Lage 16 bits van het maximum                                                                                                                                |
| 3              | Hoge 16 bits van het maximum                                                                                                                                |
| 4              | Oorspronkelijk maximum en minimum herstellen. 1 betekent dynamische wijziging; anders wordt de beginwaarde hersteld |

<img src="../../../configuration-guide/extended-controls/trend.files/image004.jpg" width="130" />

Het besturingsadres kan alleen een intern adres zijn; minimum en maximum nemen elk twee opeenvolgende woorden in.

E.g.:

Bij gegevenstype 16 bits en 8 gegevensgroepen worden, als het ingevoerde adres LW3 is, 8 opeenvolgende adressen gelezen:

LW3: waarde van curve 1

LW4: <span id="OLE_LINK513"></span><span id="OLE_LINK514"></span>waarde van curve 2

LW5: <span id="OLE_LINK515"></span><span id="OLE_LINK516"></span>waarde van curve 3

LW6: waarde van curve 4

LW7: waarde van curve 5

LW8: waarde van curve 6

LW9: waarde van curve 7

LW10: waarde van curve 8

Met 16-bits gegevens en N groepen worden dus N opeenvolgende adressen gelezen volgens de adresregels van de PLC.

Bij gegevenstype 32 bits en 5 groepen worden, als het ingevoerde adres LW3 is, 5 opeenvolgende waarden gelezen.

LW3: <span id="OLE_LINK517"></span><span id="OLE_LINK518"></span>waarde van curve 1

LW5: waarde van curve 2

LW7: waarde van curve 3

LW9: waarde van curve 4

LW11: waarde van curve 5

Met 32-bits gegevens en N groepen worden dus N waarden gelezen door het adres telkens met 2 te verhogen volgens de adresregels van de PLC.

• Richting:

• Van links naar rechts: de curve loopt vanaf links.

• Van rechts naar links: de curve loopt vanaf rechts.

• Kleur: kleur van de curve

• Wistriggerbit: wist de huidige toestand van alle curves als het adres van 0 naar 1 gaat (stijgende flank). Gaat het van 1 naar 0 (dalende flank) of verandert het niet, dan blijven de curves ongewijzigd.

De pagina “Curves” van de trendgrafiek staat in afbeelding 4-51: hier stelt u maximum, minimum, stijl en kleur van elke curve in.

<img src="../../../configuration-guide/extended-controls/trend.files/image005.jpg" width="774" />

Afbeelding 4-51    Dialoogvenster curves van de trendgrafiek

Het gegevenstype op de pagina “Algemeen” bepaalt dat van maximum en minimum.

Is maximum of minimum bijvoorbeeld een drijvendekommagetal, dan moet u eerst “32-bits drijvende komma” kiezen als gegevenstype op de pagina “Algemeen”. Anders volgt een fout bij een klik op “OK”.

3\. De pagina “XY-assen” van de trendgrafiek staat in afbeelding 4-52:

<img src="../../../configuration-guide/extended-controls/trend.files/image006.jpg" width="774" />

Afbeelding 4-52    Dialoogvenster XY-assen van de trendgrafiek

• X-as

• Schaal tonen: of de schaal van de X-as wordt getoond.

• Y-raster tonen: of het raster van de Y-as wordt getoond.

• Kleur as / schaal: wijzigt de kleur van de X-as / schaal.

• Rasterkleur: wijzigt de kleur van het raster van de X-as.

• Hoofdverdelingen: hoofdverdelingen van de X-as.

• Subverdelingen: subverdelingen van de X-as.

Schaal tonen: of de schaal van de X-as wordt getoond.

• Y-as

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

<img src="../../../configuration-guide/extended-controls/trend.files/image004.jpg" width="130" />

Zie voor de pagina “Zichtbaarheid” het object “Bit-knop”.

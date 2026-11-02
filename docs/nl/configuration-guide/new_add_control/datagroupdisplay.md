# Weergave gegevensgroepen

Weergave gegevensgroepen: een gegevensgroep (of blok) bestaat uit gegevens op opeenvolgende adressen, zoals LW12, LW13, LW14, LW15 enz. Dit object kan de inhoud van meerdere gegevensgroepen tegelijk tonen, bijvoorbeeld LW12 tot LW15 en RWI12 tot RWI15, zodat de gebruiker de gegevens van elk register kan bekijken en vergelijken. Het kan ook referentiecurves van meerdere gegevensreeksen tekenen, met het aantal punten op de horizontale en de waarde van elk adres op de verticale as, om het verloop van een waarde over een periode nauwkeurig en intuïtief te beoordelen. Er kunnen tot 8 polylijnen (curves) worden getoond.

Het pictogram in de werkbalk is: <img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay756.png" width="31" />; klik erop om het dialoogvenster van afbeelding 4-122 te openen:

<img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay838.png" width="741" />

Afbeelding 4-122 Algemeen dialoogvenster weergave gegevensgroepen

• Achtergrondkleur: achtergrondkleur van de grafiek.

• Gegevenstype: er zijn 7 gegevenstypen beschikbaar.

• Leestriggerbit: de curve loopt alleen als het “adres van de leestriggerbit” 1 is.

• Automatisch resetten: is het “adres van de leestriggerbit” 1, dan wordt het na het loslaten van de muisknop automatisch op 0 gezet.

• Aantal kanalen: aantal gegevensreeksen, en dus het aantal curves.

• Huidig kanaal: kies een kanaal om zijn \[Besturingsadres\] in te stellen.

• Besturingsadres: leesadres. Elk kanaal heeft een eigen besturingsadres.

Per kanaal kan een ander beginadres worden ingesteld; lengte van het adres = Len \* aantal weergavepunten (bij 16-bits gegevens is Len = 1, bij 32 bits Len = 2).

Is het beginadres van kanaal 1 bijvoorbeeld LW1, het gegevenstype 32-bits geheel getal en het aantal weergavepunten 4, dan gebruikt kanaal 1 de adressen LW1 LW3 LW5 LW7;

• Weergavepunten: aantal te lezen besturingsadressen per kanaal.

• Detectie

• Activeren: geeft aan of de detectielijn (referentielijn) actief is.

• Kleur: kleur van de detectielijn (referentielijn).

• Detectieadres: de waarde bij de huidige detectielijn wordt naar dit register geschreven.

• Voorbeeld

16 bits, 4 kanalen, 10 weergavepunten, LW1 als \[Besturingsadres\] van kanaal 1; LW100 voor kanaal 2; LW200 voor kanaal 3; RWI1 voor kanaal 4. Dan:

Curve 1: LW1 tot LW10

Curve 2: LW100 tot LW109

Curve 3: LW200 tot LW209

Curve 4: RWI1 tot RWI10

Bij 32-bits gegevens en verder dezelfde instellingen:

Curve 1: LW1 tot LW20

Curve 2: LW100 tot LW119

Curve 3: LW200 tot LW219

Curve 4: RWI1 tot RWI20

Met 32-bits gegevens en N groepen worden de adreswaarden dus gelezen door het adres telkens met 2 te verhogen, volgens de adresregels van het PLC-model.

• Achtergrondkleur: kleur van het gebied waarin de curves bewegen.

• Wistriggerbit: wist de huidige toestand van alle curves als het adres van 0 naar 1 gaat (stijgende flank). Gaat het van 1 naar 0 (dalende flank) of verandert het niet, dan blijven de curves ongewijzigd.

• Gegevenspunten markeren: elke curve bestaat uit punten

• Lijnen tekenen: elke curve bestaat uit lijnen.

<img src="../../../configuration-guide/new_add_control/datagroupdisplay.files/datagroupdisplay3263.png" width="130" />

Zie voor de pagina “Zichtbaarheid” de “Bit-knop”.

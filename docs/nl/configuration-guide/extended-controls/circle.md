# Dynamische cirkel

De dynamische cirkel is een grafisch element op het scherm dat zich langs een baan beweegt en van grootte verandert. Beweging en grootte hangen af van de waarde van het bewakingsadres. Het object toevoegen en de eigenschappen wijzigen:

Kies het pictogram dynamische cirkel<img src="../../../configuration-guide/extended-controls/circle.files/image002.jpg" width="32" /> in de werkbalk, zoals in afbeelding 4-56:

Afbeelding 4-56    Dialoogvenster Dynamische cirkel

De dynamische cirkel leest drie adresgroepen, die de x- en y-coördinaat van het middelpunt en de straal van de cirkel voorstellen. Hoe ze worden gelezen, hangt af van het gekozen gegevenstype.

• Besturing:

• Middelpunt: de cirkel verplaatst zich volgens de positie van het middelpunt; de straal verandert niet.

• Straal: alleen de straal verandert; de positie niet.

• Middelpunt en straal: de straal verandert met het adres voor de straal, en het middelpunt met de adressen voor de x- en y-coördinaat.

• Transparantie: wijzigt de transparantie van de achtergrondkleur van de dynamische cirkel.

<span id="OLE_LINK564"></span><span id="OLE_LINK565"></span>• Gevuld:

Is “Gevuld” niet aangevinkt, dan is de cirkel leeg (zonder achtergrondkleur). Indien aangevinkt is de cirkel gevuld en kan de achtergrondkleur met de bijbehorende optie worden gewijzigd.

• Rand

Is deze optie niet aangevinkt, dan heeft de cirkel geen randlijn en kan de randkleur niet worden gewijzigd. Indien aangevinkt heeft de cirkel een rand, waarvan de kleur met de optie “Randkleur” kan worden gewijzigd.

Voorbeeld:

Bij gegevenstype “16-bits geheel getal” worden drie opeenvolgende gegevens gelezen volgens het adresformaat van de PLC: x-coördinaat, y-coördinaat van het middelpunt en straal. Met bewakingsadres LW1 <span id="OLE_LINK548"></span><span id="OLE_LINK549"></span>worden LW1, LW2 en LW3 gelezen, met deze betekenis:

LW1 is de x-coördinaat van het middelpunt.

<span id="OLE_LINK552"></span><span id="OLE_LINK553"></span>         LW2 is de y-coördinaat van het middelpunt.

LW3 is de straal van de cirkel.

<img src="../../../configuration-guide/extended-controls/circle.files/image004.jpg" width="130" />

Of nu “Middelpunt” of “Straal” is gekozen, de HMI leest altijd de drie adresgroepen, met dezelfde betekenis. Kiest u bijvoorbeeld “Straal” met bewakingsadres LW1, dan bestuurt alleen LW3 de straal.

Bij gegevenstype “32-bits geheel getal” en bewakingsadres LW1 worden de adressen als volgt gelezen:

<span id="OLE_LINK550"></span><span id="OLE_LINK551"></span>LW1 is de x-coördinaat van het middelpunt.

LW3 is de y-coördinaat van het middelpunt.

LW5 is de straal van de cirkel.

Bij “32-bits geheel getal” wordt het bewakingsadres volgens het adresformaat van de PLC telkens met 2 verhoogd om de drie gegevens te krijgen: x-coördinaat, y-coördinaat van het middelpunt en straal.

<img src="../../../configuration-guide/extended-controls/circle.files/image004.jpg" width="130" />

Zie voor de pagina “Zichtbaarheid” het object “Bit-knop”.

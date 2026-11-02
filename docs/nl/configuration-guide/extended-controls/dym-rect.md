# Dynamische rechthoek

De dynamische rechthoek werkt zoals de dynamische cirkel: beide tonen realtime de waarde van het bewakingsadres door positie of grootte van het element te veranderen.

Kies het pictogram dynamische rechthoek<img src="../../../configuration-guide/extended-controls/dym-rect.files/image002.jpg" width="34" /> in de werkbalk om het dialoogvenster van afbeelding 4-57 te openen.

Afbeelding 4-57    Dialoogvenster Dynamische rechthoek

De dynamische rechthoek leest vier adresgroepen: x-coördinaat, y-coördinaat, breedte en hoogte van de rechthoek. Hoe ze worden gelezen, hangt af van het gekozen gegevenstype.

• Lijndikte: wijzigt de lijndikte

• Type: rechte, afgeschuinde of afgeronde hoek.

• Opmerking: het type werkt alleen bij een lijndikte groter dan 1.

Voorbeeld:

Bij gegevenstype “16-bits geheel getal” en bewakingsadres LW1 worden LW1, LW2, LW3 en LW4 gelezen, met deze betekenis:

LW1 is de x-coördinaat <span id="OLE_LINK558"></span><span id="OLE_LINK559"></span>van de rechthoek;

LW2 is de y-coördinaat van de rechthoek;

LW3 is de breedte van de rechthoek;

LW4 is de hoogte van de rechthoek.

Bij gegevenstype “16-bits geheel getal” worden vier opeenvolgende gegevens gelezen volgens het adresformaat van de PLC: x-coördinaat, y-coördinaat, breedte en hoogte van de rechthoek.

Bij gegevenstype “32-bits geheel getal” en bewakingsadres LW1 worden LW1, LW3, LW5 en LW7 gelezen.

LW1 is de x-coördinaat van de rechthoek;

LW3 is de y-coördinaat van de rechthoek;

LW5 is de breedte van de rechthoek;

LW7 is de hoogte van de rechthoek;

Bij “32-bits geheel getal” wordt het bewakingsadres volgens het adresformaat van de PLC telkens met 2 verhoogd om de vier gegevens te krijgen: x-coördinaat, y-coördinaat, breedte en hoogte van de rechthoek.

**Besturing:**

• Positie: hoogte en breedte van de rechthoek veranderen niet; de positie verandert met de adressen voor de x- en y-coördinaat.

• Grootte: hoogte en breedte veranderen vanuit een van de vier volgende vaste punten; de positie verandert niet.

• Linksboven: <span id="OLE_LINK562"></span><span id="OLE_LINK563"></span>het vaste punt is de linkerbovenhoek en de rechthoek groeit naar rechtsonder.

• Rechtsboven: het vaste punt is de rechterbovenhoek en de rechthoek groeit naar linksonder.

• Linksonder: het vaste punt is de linkeronderhoek en de rechthoek groeit naar rechtsboven.

• Rechtsonder: het vaste punt is de rechteronderhoek en de rechthoek groeit naar linksboven.

**Gevuld:**

Is “Gevuld” niet aangevinkt, dan is de rechthoek leeg (zonder achtergrondkleur). Indien aangevinkt is hij gevuld en kan de achtergrondkleur met de bijbehorende optie worden gewijzigd.

**Rand:**

Is deze optie niet aangevinkt, dan heeft de rechthoek geen randlijn en kan de randkleur niet worden gewijzigd. Indien aangevinkt heeft de rechthoek een rand, waarvan de kleur met de optie “Randkleur” kan worden gewijzigd.

Transparantie: wijzigt de transparantie van de achtergrondkleur van de dynamische rechthoek.

<span id="OLE_LINK570"></span><span id="OLE_LINK571"></span><img src="../../../configuration-guide/extended-controls/dym-rect.files/image004.jpg" width="130" />

Zie voor de pagina “Zichtbaarheid” het object “Bit-knop”.

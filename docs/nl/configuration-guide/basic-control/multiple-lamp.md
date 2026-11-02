# Meerstandenlamp

De meerstandenlamp toont verschillende statussen afhankelijk van de waarde van het bewakingsadres. Er kunnen tot 32 statussen worden getoond.

Klik op het pictogram meerstandenlamp<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image002.jpg" width="28" /> in de werkbalk om het dialoogvenster van afbeelding 4-83 te openen.

Afbeelding 4-83    Dialoogvenster Meerstandenlamp

1\. Algemeen:

• Status: de gebruiker kan de statuswaarde wijzigen om per status randkleur, voorgrondkleur, achtergrondkleur en patroon van het object aan te passen

• Statustype: (aangenomen dat de ingevoerde waarde n is)

• Waarde: de geschreven waarde ligt tussen nul en het totale aantal statussen min 1.

• Registerbit: de geschreven waarde is 2 tot de macht n.

E.g.:

<span id="OLE_LINK657"></span><span id="OLE_LINK511"></span><span id="OLE_LINK510"></span>Het bewakingsadres (lezen) is LW3 en het totale aantal statussen is 8. Klik op “OK” om het object aan het scherm toe te voegen, voeg daarna een numerieke invoer toe met LW3 als schrijf- en bewakingsadres en sla het project op.

In de simulatie of op het scherm klikt de gebruiker op de numerieke invoer en voert met het toetsenbord een statuswaarde in. Voert hij 2 in, dan is de waarde van het bewakingsadres (lezen) 1 en toont het object de tekst van status 1 (ingesteld op de pagina “Tekst”); is LW3 gelijk aan 8, dan toont het object de tekst van status 3. Wordt 3 in LW3 ingevoerd, dan gaat de meerstandenlamp naar geen enkele status.

• Aangepaste statuswaarden: met deze optie verschijnt een knop “Statuswaarden definiëren”. Klik erop om het venster “Aangepaste statuswaarden” te openen, zoals in afbeelding 4-84:

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image004.jpg" width="333" />

Afbeelding 4-84    Dialoogvenster door gebruiker gedefinieerde statuswaarden

In dit venster is de kolom “S \#” de statuskolom: de gekozen waarde geeft de huidige status aan; dubbelklik op een waarde om de waarde van die status in te voeren.

Bijvoorbeeld: het bewakingsadres (lezen) is LW3 en het totale aantal statussen is 8. Klik op “OK” om het object aan het scherm toe te voegen, voeg daarna een numerieke invoer toe met LW3 als schrijf- en bewakingsadres en sla het project op.

In de simulatie of op het scherm klikt de gebruiker op de numerieke invoer en voert met het toetsenbord een statuswaarde in. Voert hij 1 in, dan is de waarde van het bewakingsadres (lezen) 1 en toont het object de tekst van status 1 (ingesteld op de pagina “Tekst”); is LW3 gelijk aan 33, dan toont het object de tekst van status 2. Wordt 2 in LW3 ingevoerd, dan gaat de meerstandenlamp naar geen enkele status.

• Gegevenstype: gegevenstype van het schrijf- en bewakingsadres (lezen)

• Bewakingsadres: leesadres waarvan de statuswaarde bepaalt welke status het object toont.

• Totaal aantal statussen: de gebruiker stelt het totale aantal statussen in naar behoefte, tot 32 statussen (status 0 tot 31).

Bijvoorbeeld: met gegevenstype positief geheel getal van 16 bits en 32 statussen: is het bewakingsadres 0, dan toont de meerstandenlamp tekst en afbeelding van status 0; is het 5, die van status 5. Is het 60, dan toont hij nog steeds status 31, omdat het maximum 32 statussen is.

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image005.jpg" width="130" />

Opmerking: zie voor vorm, randkleur, voorgrondkleur, achtergrondkleur en patroon het object “Bit-knop”.

Opmerking: gebruikt de meerstandenlamp een 32-bits gegevenstype, dan neemt het adres 2 woorden in. <span id="OLE_LINK673"></span><span id="OLE_LINK672"></span>Wordt bijvoorbeeld naar het dataregister V10 van een SIEMENS-PLC geschreven, dan worden V10 en V11 bezet; bewaakt een ander object ook V11, dan ontstaat een fout. Let op bij 32-bits gegevenstypen om gegevens- en adresfouten te voorkomen.

Opmerking: het gegevenstype moet overeenkomen met de te tonen gegevens.

2\. Tekst:

Klik op het tabblad “Tekst” van de eigenschappen van de meerstandenlamp om de tekstinstellingen te tonen, zoals in afbeelding 4-85:

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image006.jpg" width="675" />

Afbeelding 4-85 Pagina “Tekst” van de meerstandenlamp

Alle talen gebruiken de tekst van de eerste taal: optie voor meertalige projecten, dus als onder “Taal” in de projectbeheerder meer dan één taal is ingesteld; de tekst van het object verandert dan niet bij het wisselen van taal.

<span id="OLE_LINK737"></span><span id="OLE_LINK736"></span>• Taal: optie voor meertalige projecten. Kies een taal om per status andere teksten in te voeren en zo meertaligheid te bereiken. (Kies in de functieknop “Taal wisselen” en de doeltaal; in de simulatie of op het scherm schakelen bij een druk op de knop alle objecten met tekst naar die taal.) Tekst, lettertype en lettergrootte kunnen per taal verschillen; kleur, tekenafstand en positie zijn gemeenschappelijk.

• Lettertype: lettertype van de tekst; kan per status en per taal verschillen.

• Lettergrootte: grootte van de tekst; kan per status en per taal verschillen.

• Kleur, tekenafstand, positie: kleur, tekenafstand en uitlijning van de geselecteerde tekst. Kiest u op de pagina “Tekst” een andere taal dan taal 1 terwijl het project meer dan één taal heeft, dan hebben deze drie opties geen effect, omdat ze gelijk zijn aan die van taal 1.

3\. Afbeelding:

Klik op het tabblad “Afbeelding” van de eigenschappen van de meerstandenlamp om de instellingen te tonen, zoals in afbeelding 4-86.

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image007.jpg" width="675" />

Afbeelding 4-86 Pagina “Afbeelding” van de meerstandenlamp

Op deze pagina worden per status afbeeldingen geladen. Standaard is de afbeelding van elke status leeg; dit kan naar wens worden gewijzigd.

• Werkwijze: kies in de lijst het element waarvan u de afbeelding wilt wijzigen en kies een afbeelding uit de systeembibliotheek of via een pad in Windows. Bij een klik op een status wordt de bijbehorende afbeelding hieronder geladen. De gebruiker bepaalt ook of de afbeelding aan het object wordt aangepast: zo niet, dan kunnen marge en positie worden gewijzigd voor een mooier resultaat.

• Aanpassen aan object: indien aangevinkt krijgt de afbeelding de grootte van het object op de pagina “Algemeen” en worden marge en positie verborgen; zo niet, dan verschijnen ze.

Importeert u een afbeelding uit een extern bestand, dan verschijnt de optie “Transparant”, waarmee een bepaalde kleur transparant wordt

<img src="../../../configuration-guide/basic-control/multiple-lamp.files/image005.jpg" width="130" />

Opmerking: zie voor de pagina “Zichtbaarheid” het object “Bit-knop”.

Klik na het instellen van alle eigenschappen op “OK” en voeg het object toe aan het scherm

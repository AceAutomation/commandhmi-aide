# Staafdiagram

Het staafdiagram toont het realtime verloop van numerieke waarden als staven, zodat de gebruiker het verloop visueler ziet. Het kan het verloop van dataregisters van de PLC of andere apparaten tonen, en van alle analoge grootheden in het proces. Zie de afbeelding hieronder.

<img src="../../../configuration-guide/basic-control/bar.files/image006.jpg" width="535" alt="2018_11_20_14_27_19.jpg" />

Afbeelding 4-101   Staafdiagram

Een staafdiagram toevoegen en de eigenschappen wijzigen:

1\. Kies het pictogram staafdiagram <img src="../../../configuration-guide/basic-control/samdra8.gif" width="20" /> in de werkbalk of het menu “Gereedschap”. Het dialoogvenster van afbeelding 4-102 verschijnt.

2\. Stel de eigenschappen van het staafdiagram in en klik op “OK”:

• Achtergrondkleur: achtergrondkleur van het staafdiagram

• Randkleur: randkleur van de staaf. In afbeelding 4-102 heeft de randkleur geen effect; kies een andere “vorm” om het verschil te zien.

• Transparant: achtergrond van de staaf transparant

• Richting: vulrichting van de staaf, in vier richtingen: omhoog, omlaag, naar links en naar rechts.

• Omhoog: als de waarde van het bewakingsadres stijgt, vult de staaf zich van onder naar boven

• Omlaag: als de waarde van het bewakingsadres stijgt, vult de staaf zich van boven naar onder

• Naar links: als de waarde van het bewakingsadres stijgt, vult de staaf zich van rechts naar links

• Naar rechts: als de waarde van het bewakingsadres stijgt, vult de staaf zich van links naar rechts

• Gegevenstype: type van de gelezen waarde, dus woordadres of dubbelwoordadres.

• Bewakingsadres: adres van het dataregister dat in de staaf wordt getoond, dus het leesadres

• Maximum: maximale waarde van het bewakingsadres (lezen). Is de waarde hoger, dan is de staaf vol en verandert niet meer

• Minimum: minimale waarde van het bewakingsadres (lezen). Is de waarde lager, dan is de staaf leeg en verandert niet meer

• Variabel bereik: maximum en minimum veranderen dynamisch volgens het door de gebruiker opgegeven adres; het gegevenstype van dat adres is het ingestelde “Gegevenstype”

• Bipolaire staaf: de staaf kan aan beide zijden worden getoond, afhankelijk van de waarde van het dataregister.

• Middelpunt: middelpunt van de bipolaire staaf.

<img src="../../../configuration-guide/basic-control/bar.files/image002.jpg" width="675" />

Afbeelding 4-102   Dialoogvenster Staafdiagram

Bijvoorbeeld: met maximum 100, minimum 10 en vullen naar boven, bipolaire staaf aangevinkt en “Middelpunt” 70, wordt de waarde van het bewakingsadres die vanaf 0 stijgt getoond zoals in afbeelding 4-103.

<img src="../../../configuration-guide/basic-control/samdra10.gif" width="534" />

Afbeelding 4-103 Bipolair staafdiagram

3\. Staafdiagram wijzigen: klik erop; er verschijnen acht groene puntjes waarmee u met de muis de grootte kunt aanpassen.

Pagina “Bereik”:

Op deze pagina wordt de waarde van het bewakingsadres binnen het opgegeven bereik met andere voorgrond- en achtergrondkleuren getoond. De eigenschappen staan in afbeelding 4-104:

Afbeelding 4-104   Pagina “Bereik” van het staafdiagram

• Bereik tonen: indien aangevinkt stelt de gebruiker de onder- en bovengrens en de achtergrondkleuren voor laag en hoog in. De bewaakte (gelezen) waarde wordt binnen deze grenzen met verschillende kleuren weergegeven.

• Variabel bereik: de waarden “Ondergrens” en “Bovengrens” veranderen dynamisch volgens het door de gebruiker opgegeven adres

• Ondergrens: ondergrens van de weergave. Is de waarde lager, dan krijgt de achtergrond de kleur van “Achtergrondkleur laag”.

• Bovengrens: bovengrens van de weergave. Is de waarde hoger, dan krijgt de achtergrond de kleur van “Achtergrondkleur hoog”.

<span id="OLE_LINK727"></span><span id="OLE_LINK726"></span>Klik na de instellingen op “OK” om het object aan het werkgebied (het scherm) toe te voegen

<img src="../../../configuration-guide/basic-control/bar.files/image004.jpg" width="130" />

Opmerking: ligt de waarde van het bewakingsadres tussen maximum en minimum, dan zijn voorgrond- en achtergrondkleur die van de pagina “Algemeen”.

Opmerking: zie voor de “Zichtbaarheid” de “Bit-knop”.

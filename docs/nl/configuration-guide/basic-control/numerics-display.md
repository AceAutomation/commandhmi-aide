# Numerieke weergave

De numerieke weergave is een veelgebruikt object dat waarden toont uit dataregisters van de PLC of andere aangesloten apparaten, zoals snelheid, stroom, druk enz.

Kies het pictogram weergave<img src="../../../configuration-guide/basic-control/numerics-display.files/image002.jpg" width="30" /> in de werkbalk; er verschijnt een dialoogvenster, zoals in afbeelding 4-91:

Afbeelding 4-91 Dialoogvenster Numerieke weergave

Hier stelt u de weergave in van de waarde in het dataregister van de PLC of een ander apparaat: aantal cijfers, decimalen, lettergrootte, kleur, uitlijning en opmaak van de tekst.

• Gegevenstype: de gebruiker kiest het gegevenstype naar de waarde van het bewaakte adres.

• Weergavetype: de gebruiker kiest het weergavetype naar de behoeften van het project.

• Bewakingsadres: leesadres. Het adres van het dataregister in de PLC of een ander apparaat met de te tonen gegevens.

• Decimalen: aantal getoonde decimalen.

• Lettertype: gewoon of digitaal lettertype.

• Lettergrootte: grootte van het getoonde lettertype.

• Uitlijning: standaard gecentreerd.

• Links: de waarde wordt links in het weergavegebied getoond.

• Midden: de waarde wordt in het midden van het weergavegebied getoond.

• Rechts: de waarde wordt rechts in het weergavegebied getoond.

• Opvulling: standaard nulonderdrukking.

• Nulonderdrukking: nullen vóór de significante cijfers worden verborgen. <span id="OLE_LINK668"></span><span id="OLE_LINK669"></span>Is de waarde van het bewakingsadres 00123 (positief geheel getal van 16 bits), dan wordt 123 getoond.

• Voorloopnullen: voorloopnullen worden getoond. Is de waarde van het bewakingsadres 00123 (positief geheel getal van 16 bits), dan wordt 00123 getoond.

• Voorloopspaties: spaties in plaats van voorloopnullen. Is de waarde van het bewakingsadres 00123 (positief geheel getal van 16 bits), dan wordt   123 getoond.

• Tekstkleur: kleur van de getoonde gegevens;

<img src="../../../configuration-guide/basic-control/numerics-display.files/image004.jpg" width="130" />

Opmerking: zie voor vorm, randkleur, voorgrondkleur, achtergrondkleur en stijl het object “Bit-knop”.

Opmerking: <span id="OLE_LINK678"></span><span id="OLE_LINK679"></span>dubbelklik op het weergaveveld om inhoud en eigenschappen te wijzigen. Werkt het object in de HMI, dan verschijnt een schermtoetsenbord waarmee de gebruiker gegevens kan invoeren.

Opmerking: <span id="OLE_LINK684"></span><span id="OLE_LINK685"></span>het aantal decimalen beïnvloedt de weergave. Bij de typen positief geheel getal of geheel getal van 16/32 bits wordt de getoonde waarde verkregen door de komma van de teruggegeven waarde het ingestelde aantal posities te verschuiven. Wordt 212 teruggegeven met 2 decimalen, dan wordt 2.12 getoond. Bij het type drijvende komma van 32 bits wordt de waarde niet verschoven; alleen de ingestelde decimalen worden getoond. Wordt 2.123 teruggegeven met 2 decimalen, dan wordt 2.12 getoond.

Opmerking: het totale aantal cijfers is de som van het gehele en het decimale deel. Is het gehele deel van de waarde langer dan ingesteld, dan wordt het met zijn werkelijke lengte getoond. Voor de waarde 2123 met lengte 2 en 1 decimaal wordt bijvoorbeeld 212.3 getoond.

De pagina “Geavanceerd” van de numerieke weergave biedt krachtige functies, zoals schaling en bereikweergave, zie afbeelding 4-92:

<img src="../../../configuration-guide/basic-control/numerics-display.files/image005.jpg" width="675" />

Afbeelding 4-92    Pagina “Geavanceerd” van de numerieke weergave

• Schaling: indien aangevinkt is de getoonde waarde: waarde van het bewakingsadres (lezen) × versterking + offset

<span id="OLE_LINK696"></span><span id="OLE_LINK697"></span>• Bereik tonen: indien aangevinkt stelt de gebruiker de onder- en bovengrens en de achtergrondkleuren voor laag en hoog in. De bewaakte (gelezen) waarde wordt binnen deze grenzen met verschillende kleuren weergegeven.

• Variabel bereik: de waarden “Ondergrens” en “Bovengrens” veranderen dynamisch volgens het door de gebruiker opgegeven adres

• Ondergrens: ondergrens van de weergave. Is de waarde lager, dan krijgt de achtergrond de kleur van “Achtergrondkleur laag”.

• Bovengrens: bovengrens van de weergave. Is de waarde hoger, dan krijgt de achtergrond de kleur van “Achtergrondkleur hoog”.

Stelt u bijvoorbeeld op de pagina “Algemeen” de achtergrond- en tekstkleur in en kiest u de bereikkleuren zoals in afbeelding 4-93:

<img src="../../../configuration-guide/basic-control/numerics-display.files/image006.jpg" width="673" />

<img src="../../../configuration-guide/basic-control/numerics-display.files/image007.jpg" width="349" />

Afbeelding 4-93 Instellingen bereikweergave

Verandert de waarde van het bewaakte adres, dan veranderen tekst en achtergrond van de numerieke weergave mee, zoals in afbeelding 4-94:

<img src="../../../configuration-guide/basic-control/samdra93.gif" width="508" />

Afbeelding 4-94    Voorbeeld van een numerieke weergave

<img src="../../../configuration-guide/basic-control/numerics-display.files/image004.jpg" width="130" />

Opmerking: zie voor de pagina “Zichtbaarheid” het object “Bit-knop”.

Opmerking: <span id="OLE_LINK682"></span><span id="OLE_LINK683"></span>bij een 32-bits gegevenstype neemt het adres 2 woorden in. Wordt bijvoorbeeld naar het dataregister V10 van een SIEMENS-PLC geschreven, dan worden V10 en V11 bezet; bewaakt een ander object ook V11, dan ontstaat een fout. Let op bij 32-bits gegevenstypen om gegevens- en adresfouten te voorkomen.

Klik na de instellingen op “OK” om het object aan het werkgebied (het scherm) toe te voegen

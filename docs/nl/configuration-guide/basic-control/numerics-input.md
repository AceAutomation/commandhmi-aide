# Numerieke invoer

De numerieke invoer is het meest gebruikte object en vrijwel onmisbaar bij procesbesturing. Hiermee worden waarden in dataregisters van de PLC of andere apparaten ingevoerd, getoond en opgeslagen, zoals snelheid, stroom, druk enz.

Numerieke invoer en numerieke weergave werken vrijwel gelijk; het enige verschil is dat de numerieke invoer ook waarden naar dataregisters van de PLC of andere apparaten kan schrijven, naast ze tonen.

Een numerieke invoer aanmaken:

Kies het pictogram numerieke invoer<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input596.png" width="31" /> in de werkbalk; er verschijnt een dialoogvenster, zoals in afbeelding 4-95.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input665.png" width="662" />

Afbeelding 4-95 Dialoogvenster Numerieke invoer

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input705.png" width="130" />

Opmerking: zie voor vorm, randkleur, voorgrondkleur, achtergrondkleur en patroon het object “Bit-knop”.

Opmerking: zie voor “Uitlijning”, “Opvulling”, “Decimalen” en “Totaal aantal cijfers” het object “Numerieke weergave”.

Opmerking: dubbelklik op het weergaveveld om inhoud en eigenschappen te wijzigen. Werkt het object in de HMI, dan verschijnt een schermtoetsenbord waarmee de gebruiker gegevens kan invoeren, zoals in afbeelding 4-96.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input1192.png" width="693" />

Afbeelding 4-96 Numeriek toetsenbord

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input1228.png" width="130" />

Opmerking: bij een 32-bits gegevenstype neemt het adres 2 woorden in. Wordt bijvoorbeeld naar het dataregister V10 van een SIEMENS-PLC geschreven, dan worden V10 en V11 bezet; bewaakt een ander object ook V11, dan ontstaat een fout. Let op bij 32-bits gegevenstypen om gegevens- en adresfouten te voorkomen.

Opmerking: het aantal decimalen beïnvloedt de weergave. Bij de typen positief geheel getal of geheel getal van 16/32 bits wordt de getoonde waarde verkregen door de komma van de teruggegeven waarde het ingestelde aantal posities te verschuiven. Wordt 212 teruggegeven met 2 decimalen, dan wordt 2.12 getoond. Bij het type drijvende komma van 32 bits wordt de waarde niet verschoven; alleen de ingestelde decimalen worden getoond. Wordt 2.123 teruggegeven met 2 decimalen, dan wordt 2.12 getoond.

Opmerking: het totale aantal cijfers is de som van het gehele en het decimale deel. Is het gehele deel van de waarde langer dan ingesteld, dan wordt het met zijn werkelijke lengte getoond. Voor de waarde 2123 met lengte 2 en 1 decimaal wordt bijvoorbeeld 212.3 getoond.

• Wachtwoordinvoer: de door de gebruiker ingevoerde tekens worden tijdens invoer en weergave als “\*” getoond.

• Script gebruiken: vink “Script gebruiken” aan om de lijst met scripts te tonen. De gebruiker kiest een script dat bij het indrukken van de numerieke invoer wordt uitgevoerd. Alleen gecompileerde scripts staan in de lijst.

• Totaal aantal cijfers: som van de gehele en decimale cijfers. Begrenst de grootte van de getoonde en ingevoerde waarden. Met 4 cijfers in totaal en 1 decimaal is de maximale waarde 999.9, het maximum voor invoer en weergave. Een grotere invoer geeft een fout; bij een grotere weergave worden de overtollige cijfers genegeerd en alleen het ingestelde aantal getoond. Bijvoorbeeld: 4 cijfers, 1 decimaal, werkelijke waarde 12345: het object toont 234.5.

Pagina “Geavanceerd”: voor versterking, offset en bereikcontrole van de ingevoerde gegevens (controle of de waarde buiten het ingestelde bereik valt). Daarnaast zijn er de opties “Aanraakbaarheid” en “Melding”, die werken zoals bij het object “Bit-knop”.

Klik op het tabblad “Geavanceerd”, zoals in afbeelding 4-97:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input3958.png" width="675" />

Afbeelding 4-97 Pagina “Geavanceerd” van de numerieke invoer

• Bitgestuurd: indien aangevinkt is het object alleen onder bepaalde voorwaarden beschikbaar. Is de “Geldige status” 1, dan reageert het object alleen als het “Stuurbit” 1 is. Is de “Geldige status” 0, dan reageert het alleen als het “Stuurbit” 0 is. In alle andere gevallen werkt het niet.

• Gestuurd door gebruikersniveau: de gebruiker kan meerdere opties aanvinken. In de simulatie of op de HMI wordt gecontroleerd of de huidige gebruiker die bevoegdheid heeft.

• Sneltoetsen gebruiken: zie de Bit-knop.

• Waarde tonen: indien aangevinkt toont het invoertoetsenbord de huidige waarde van het object. Is de getoonde waarde bijvoorbeeld 389, dan toont het invoerveld na een klik op de numerieke invoer 389; zo niet, dan is het leeg, zoals hieronder:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input4972.png" width="93" />

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input4974.png" width="630" />

Bijvoorbeeld: zijn op de pagina “Geavanceerd” van het object de opties 2 en 3 van de niveaubesturing aangevinkt, en zijn de gebruikerswachtwoorden in de touchscreenparameters zoals in afbeelding 4-98:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input5185.png" width="605" />

Afbeelding 4-98 Gebruikerswachtwoorden in de touchscreenparameters

Is het standaard gebruikersniveau NULL, dan reageert het object niet; met de functie “Gebruikersniveau wijzigen” van een functieknop kunt u het niveau wijzigen. Voert de gebruiker bijvoorbeeld 6666 in (niveau 6), dat alleen optie 1 heeft en niet 2 of 3, dan meldt het systeem dat het wachtwoord onjuist is; voert hij 2222 of 3333 in, dan hebben beide gebruikers optie 2, die overeenkomt met 2 of 3: het wachtwoord is geldig en het object reageert. Is het standaardniveau gebruiker 2 of 3, dan hebben beide optie 2 en reageert het object vanaf het begin in de simulatie of op het scherm; is het gebruiker 3 zonder overeenkomst, dan reageert het object niet. De standaardinstellingen staan in de afbeelding hieronder:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input6241.png" width="266" />

Is “Gebruikersniveau wijzigen indien onvoldoende” aangevinkt, dan verschijnt bij een niet-passend niveau een aanmeldvenster om een passend niveau te kiezen en opnieuw aan te melden, zoals hieronder:

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input6435.png" width="268" />

• Melding: reageert het object, dan wordt in de simulatie of op het scherm na een klik erop en invoer van een waarde via het pop-uptoetsenbord de ingestelde status (1 of 0) naar het adres van het “Meldingsbit” geschreven.

• Schaling: indien aangevinkt is de naar het adres geschreven waarde = (door de gebruiker via het toetsenbord ingevoerde waarde - offset) / versterking; de getoonde waarde (waarde van het bewakingsadres) = waarde van het bewakingsadres × versterking + offset

• Bereik tonen: indien aangevinkt stelt de gebruiker de onder- en bovengrens en de achtergrondkleuren voor laag en hoog in. De bewaakte (gelezen) waarde wordt binnen deze grenzen met verschillende kleuren weergegeven.

• Variabel bereik: de waarden “Ondergrens” en “Bovengrens” veranderen dynamisch volgens het door de gebruiker opgegeven adres

• Ondergrens: ondergrens van de weergave. Is de waarde lager, dan krijgt de achtergrond de kleur van “Achtergrondkleur laag”.

• Bovengrens: bovengrens van de weergave. Is de waarde hoger, dan krijgt de achtergrond de kleur van “Achtergrondkleur hoog”.

• Bereikcontrole: controleert of de ingevoerde waarde het ingestelde maximum of minimum overschrijdt.

Klik na de instellingen op “OK” om het object aan het werkgebied (het scherm) toe te voegen

• Met de pagina “Algemeen” zoals hieronder wordt het getal binair getoond en decimaal ingevoerd. Bij een ander weergavetype is het invoertype gelijk aan het weergavetype.

<img src="../../../configuration-guide/basic-control/numerics-input.files/numerics-input8099.png" width="663" />

• Klik na het instellen van de eigenschappen op “OK”; de muisaanwijzer wordt een kruis. Teken met de muis een rechthoek op het scherm om het object toe te voegen.

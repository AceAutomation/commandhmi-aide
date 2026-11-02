# Gegevensoverdracht

Voor gegevensoverdracht tussen PLC en HMI of tussen twee PLC's. Klik in de projectbeheerder op “Gegevensoverdracht” om de lijst met overdrachten te tonen.

<img src="../../../configuration-guide/extended-controls/transmission.files/image005.jpg" width="564" />

Afbeelding 7-36

De lijst toont alle huidige overdrachten in detail. De gebruiker kan ze aanmaken, verwijderen en wijzigen. De software CommandHMI ondersteunt tot 512 gegevensoverdrachten.

Om een overdracht aan te maken of te wijzigen, opent u de eigenschappenpagina:

<img src="../../../configuration-guide/extended-controls/transmission.files/image006.jpg" width="339" />

Afbeelding 7-37

**1. Eigenschappen**

Periodiek / trigger: activeringswijze van de overdracht.

Periodiek: de overdracht gebeurt met het ingestelde interval.

Trigger: de overdracht wordt door een adres bestuurd; ze wordt uitgevoerd als het adres 1 is.

Automatisch resetten: is het triggeradres 1, dan wordt het automatisch op 0 gezet.

Adrestype: type van het overgedragen adres: bit / woord / dubbelwoord.

Woorden / bits: lengte van de over te dragen gegevens, van 1 tot 64.

**2. Adres**

Bronadres: bronadres van de gegevens, <span id="OLE_LINK497"></span><span id="OLE_LINK498"></span>van hetzelfde type als ingesteld onder “Eigenschappen”.

Doeladres: doeladres van de gegevens, van hetzelfde type als ingesteld onder “Eigenschappen”.

<img src="../../../configuration-guide/extended-controls/transmission.files/image004.jpg" width="130" />

Bron- en doeladres kunnen niet in dezelfde PLC liggen.

# Het project downloaden

<img src="../../start-new-project/download-project.files/image012.jpg" width="368" />

Afbeelding 3-11    Melding compileerfout

U kunt het project aanpassen aan de hand van de foutmelding in het uitvoervenster, of dubbelklikken op de fout: CommandHMI zoekt en selecteert dan automatisch het foute object. Dubbelklik op het object om de eigenschappen te bekijken, de oorzaak van de fout te vinden en die te corrigeren. Klik daarna op “Opslaan” en compileer opnieuw. Zijn er geen fouten, dan verschijnt na enige tijd een venster dat het compileren is gelukt. Klik op “OK” om af te ronden, zoals in afbeelding 3-12:

<img src="../../start-new-project/download-project.files/image013.jpg" width="364" />

Afbeelding 3-12    Uitvoervenster

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

Vóór het downloaden moet worden gecompileerd en vóór het compileren opgeslagen; anders mislukt het compileren, zoals in afbeelding 3-11. Na een wijziging na het compileren moet opnieuw worden gecompileerd.

<img src="../../start-new-project/download-project.files/image014.jpg" width="425" />

Afbeelding 3-13    Herinnering compileren

Kies ten slotte de opdracht “USB” in het menu “Downloaden” om via de USB-kabel te downloaden; u kunt ook direct “Compileren + downloaden” kiezen. Daarna verschijnt het dialoogvenster van afbeelding 3-14:

<img src="../../start-new-project/download-project.files/image015.jpg" width="716" />

Afbeelding 3-14    Dialoogvenster downloaden

Klik op “Downloaden”; de voortgangsbalk in het midden toont de voortgang. Na afloop meldt een venster dat de USB-download is voltooid. Klik op “OK” om af te ronden, zoals in afbeelding 3-15:

<img src="../../start-new-project/download-project.files/image005.jpg" width="720" alt="2018_11_20_09_02_42.jpg" />

Afbeelding 3-15    Downloaden voltooid

Daarna wordt de PLC aangesloten om te controleren of het project correct op de HMI werkt.

De aansluiting van HMI op PLC of pc staat onder “Bedrading” in de hardwarehandleiding.

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

Schakel tijdens de overdracht de voeding van HMI of pc niet uit, trek de USB-kabel niet los en voer geen andere bewerkingen uit; anders mislukt de overdracht.

Installeer vóór het downloaden het USB-stuurprogramma; anders maakt de pc geen verbinding met de HMI en kan het downloaden niet worden voltooid.

<img src="../../start-new-project/download-project.files/image017.jpg" width="716" />

Afbeelding 3-16    Melding USB-stuurprogramma

<img src="../../start-new-project/download-project.files/image006.jpg" width="130" />

Het venster van afbeelding 3-16 betekent dat de pc de HMI niet herkent. Controleer dan of het USB-stuurprogramma is geïnstalleerd: verbind de pc, schakel de HMI in en zoek “CommandHMI HMI Tech Corp USB drive” in Windows onder “Deze computer” - “Eigenschappen” - “Hardware” - “Apparaatbeheer” - “USB-controllers” (trek eventueel de USB-kabel los en sluit hem weer aan om te zien of de pc de HMI herkent):

**Project downloaden via Ethernet**

• Netwerkparameters van de HMI instellen

Zet DIP-schakelaars 1 en 3 samen aan; stel het IP-adres in (hier 192.168.1.100), de gateway, het subnet en de poort. De poort is vast 12345.

• Het project compileren

Bij downloaden via Ethernet moeten IP-adres en poortnummer in het invoerveld worden ingevoerd. Het IP-adres is dat van de doel-HMI, hier zoals hierboven 192.168.1.100, en de poort is vast 12345. Klik daarna op herstarten en downloaden, zoals in afbeelding 3-18:

![](../../start-new-project/download-project.files/001.png)

Afbeelding 3-18 Project downloaden via Ethernet

U kunt ook op de knop “Scannen” klikken om IP-adressen te zoeken

![](../../start-new-project/download-project.files/002.png)

U kunt het gevonden IP-adres aanvinken en wijzigen in het wijzigingsveld hieronder

![](../../start-new-project/download-project.files/003.png)

Klik op de knop rechts om de schermgegevens te wijzigen; na afloop verschijnt een pop-upvenster.

![](../../start-new-project/download-project.files/004.png)

Klik dan op “Opnieuw scannen”: het gewijzigde resultaat staat in de lijst.

![](../../start-new-project/download-project.files/005.png)

Vink het gewenste IP-adres aan en klik op “Selecteren” om het doel-IP te kiezen; de IP-gegevens worden overgenomen in het downloadvenster.

**Let op!**

Voor de IP-scanfunctie moet aan deze drie voorwaarden worden voldaan:

1. Touchscreens die vóór 30 december 2024 zijn geproduceerd, hebben een handmatig te installeren IP-scanpatch nodig; vindt u het bestand “hmi.patch” niet in de installatiemap, vraag het dan aan de technische dienst.
     2. De versie van de configuratiesoftware moet minimaal HMITOOLV7.1_022 zijn
     3. De firmwareversie moet minimaal Simulator 8.1.0.10 zijn.

![](../../start-new-project/download-project.files/006.png)

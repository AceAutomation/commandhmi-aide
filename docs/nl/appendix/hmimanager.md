# Gebruik van HMIManager

Ga naar de pagina met downloadhulpmiddelen

![](../../appendix/hmimanageer.files/002.png)

Pagina “Download”:

Communicatie-instellingen:
USB: de pc is via USB met de HMI verbonden
WAN: de pc is via Ethernet met de HMI verbonden

U kunt ook op de knop “Scannen” klikken om IP-adressen te zoeken

![](../../appendix/hmimanageer.files/a1.png)

U kunt het gevonden IP-adres aanvinken en wijzigen in het wijzigingsveld hieronder

![](../../appendix/hmimanageer.files/a2.png)

Klik op de knop rechts om de schermgegevens te wijzigen; na afloop verschijnt een pop-upvenster.

![](../../appendix/hmimanageer.files/a3.png)

Klik dan op “Opnieuw scannen”: het gewijzigde resultaat staat in de lijst.

![](../../appendix/hmimanageer.files/a4.png)

Vink het gewenste IP-adres aan en klik op “Selecteren” om het doel-IP te kiezen; de IP-gegevens worden overgenomen in het downloadvenster.

**Let op!**

Voor de IP-scanfunctie moet aan deze drie voorwaarden worden voldaan:

1. Touchscreens die vóór 30 december 2024 zijn geproduceerd, hebben een handmatig te installeren IP-scanpatch nodig; vindt u het bestand “hmi.patch” niet in de installatiemap, vraag het dan aan de technische dienst.
     2. De versie van de configuratiesoftware moet minimaal HMITOOLV7.1_022 zijn
     3. De firmwareversie moet minimaal Simulator 8.1.0.10 zijn.

Downloadkeuze:
Configuratie downloaden: maak het projectbestand u-disk-prj.bin aan; kies in de configuratiesoftware Download-&gt;Extract Project Save As-&gt;u-disk-prj.bin aanmaken, klik op “Bladeren” om het bestand te kiezen en daarna op “Start” om het te downloaden en de configuratie in de HMI bij te werken.
Recept downloaden: compileer het bewerkte HMI-project; in de map compile van de installatiemap worden de bestanden recipe60.bin en recipe62.bin aangemaakt; kies voor versie 6.0 of lager recipe60.bin en voor hoger dan 6.0 recipe62.bin. Klik op “Bladeren” om het bestand te kiezen en daarna op “Download starten”.

![](../../appendix/hmimanageer.files/003.png)

Pagina “Upload”:

Communicatie-instellingen:
Zoals bij het downloaden.

Uploadkeuze:
Keuzegebied: de configuratie kan alleen worden geüpload als de touchscreenparameters dat toestaan; recepten, historische gegevens en historische alarmen alleen als ze in het HMI-programma bestaan.
Historische gegevens uploaden: klik op “Bladeren” om locatie en bestandsnaam te kiezen en op “Upload starten” om het zip-bestand en het .csv-bestand met historische gegevens te uploaden; zie “Bestanden met historische gegevens uploaden”.
Configuratie uploaden: klik op “Bladeren” om locatie en bestandsnaam te kiezen en op “Upload starten” om het zip-bestand van de configuratie te uploaden; pak het daarna uit om het project normaal te bekijken en te bewerken; zie “Configuratieprogramma uploaden”.
Recept uploaden: klik op “Bladeren” om locatie en bestandsnaam te kiezen en op “Upload starten” om het receptbestand van de HMI te uploaden.
Historische alarmen uploaden: klik op “Bladeren” om locatie en bestandsnaam te kiezen en op “Upload starten” om het alarmbestand van de HMI te uploaden.

![](../../appendix/hmimanageer.files/004.png)

Pagina “Versie”:

Communicatie-instellingen:
Zoals bij het downloaden.

Versie-informatie: versie van de aangesloten HMI.

![](../../appendix/hmimanageer.files/005.png)

Pagina “Firmware”:

Communicatie-instellingen:
Zoals bij het downloaden.

Firmware-informatie
Firmware: klik op “Bladeren” om de bij te werken firmware te kiezen en daarna op “Bijwerken”

![](../../appendix/hmimanageer.files/006.png)

Pagina “Simulatie”:

Kies het projectbestand .vpm om de online- of offlinesimulatie uit te voeren.

![](../../appendix/hmimanageer.files/007.png)

Pagina “Adres”:

Service: kies de fabrikant van het apparaat.
Model: kies het apparaatmodel
Toont alle adresgegevens van het gekozen apparaat.

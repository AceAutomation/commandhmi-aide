# Modbus TCP/IP

Via MODBUS TCP kan de HMI op afstand worden aangesproken en bestuurd.

**Instellingen** met de HMI als master:

Dubbelklik na het aanmaken van een project op “Verbinding 1”, zoals hieronder:

<img src="../../multpoint/modbustcpip.files/modbustcpip209.png" width="248" />

Het dialoogvenster “Eigenschappen communicatiepoort” verschijnt (zie hieronder).

<img src="../../multpoint/modbustcpip.files/modbustcpip286.png" width="590" />

Klik in het venster “Eigenschappen poort” op “Parameters” en stel in het volgende venster het IP-adres en het poortnummer in (die van het bewaakte apparaat). Kies de standaardadresmodus en klik op “OK”.

<img src="../../multpoint/modbustcpip.files/modbustcpip544.png" width="588" />

Kiest u “Uitgebreide modus” als adresmodus, dan gelden de IP-adres- en poortinstellingen hier niet; ze kunnen dan worden ingesteld met de functieknop “IP-configuratie slave-apparaten” in de configuratie.

Klik tijdens de werking op de knop om het venster voor het stationsnummer te openen; voer het stationsnummer in en u komt in het venster voor IP-adres en poortnummer van de slave, zoals in de afbeelding hieronder:

<img src="../../multpoint/modbustcpip.files/modbustcpip985.png" width="445" />

Download na deze instellingen het project naar de HMI en verbind master en slave direct of via een router om te bewaken en te besturen.

**Instellingen van de slave:**

**1. IP-adres instellen**

Stel eerst het IP-adres van de HMI in met DIP-schakelaars 1 en 3; voer in het IP-instellingenvenster het IP-adres in. In dit voorbeeld is het IP-adres van de slave 192.168.1.31. 2.

**2. Verbinding instellen**

Dubbelklik na het aanmaken van het project op “Verbinding 1”, zoals hieronder:

<img src="../../multpoint/modbustcpip.files/modbustcpip1527.png" width="229" />

Het dialoogvenster “Eigenschappen communicatiepoort” verschijnt (zie hieronder).

<img src="../../multpoint/modbustcpip.files/modbustcpip1604.png" width="588" />

Stel in het dialoogvenster hierboven het volgende in:

\* Verbindingspoort: “Ethernet” (zie afbeelding).

<img src="../../multpoint/modbustcpip.files/modbustcpip1711.png" width="543" />

\* HMI-locatie: kies “Lokaal” (zie afbeelding).

<img src="../../multpoint/modbustcpip.files/modbustcpip1752.png" width="163" />

\* Verbindingsdienst: kies “Modbus” - “Modbus Slave TCP / IP” (zie afbeelding).

<img src="../../multpoint/modbustcpip.files/modbustcpip1830.png" width="531" />

Klik in het venster “Eigenschappen poort” op “Parameters” en stel in het volgende venster het IP-adres (van de slave) en het poortnummer in. Klik op “OK”.

<img src="../../multpoint/modbustcpip.files/modbustcpip2039.png" width="589" />

Download het project naar de HMI en verbind master en slave direct of via een router om te bewaken en te besturen.

<img src="../../multpoint/modbustcpip.files/modbustcpip2198.png" width="130" />

Als de HMI slave is, zijn de adressen de interne adressen.

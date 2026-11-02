# Stuurprogramma Siemens

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Met dit stuurprogramma lezen en schrijven HMI's van de HM-serie gegevens of statussen van registers van PLC's uit de serie Siemens S7-200/300/1200. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik van dit stuurprogramma dit hoofdstuk en de technische documentatie van de PLC aandachtig.</p></td>
</tr>
<tr class="even">
<td><p> Verbinding maken met een PLC uit de serie Siemens S7-200/300/1200tcp</p>
<p><strong>1. 1 Hardwareaansluiting</strong></p>
<p>Verbindingskabel:</p>
<p>RS485-Siemens S7-200<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI HM-serie COM1/COM2</strong></p></td>
<td colspan="2"><p>Serie Siemens S7-200</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>8</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>3</p></td>
<td><p>TX+</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/siemens.files/image002.gif" width="130" /><img src="../../drivers/siemens.files/image003.gif" width="290" /><img src="../../drivers/siemens.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

  RS232-Siemens S7-300

|                             |     |                           |     |
|-----------------------------|-----|---------------------------|-----|
| **HMI HM-serie COM1/COM2** |     | **Serie Siemens S7-300** |     |
| **2**                       | RX  | 3                         | TX  |
| **3**                       | TX  | 2                         | RX  |
| **5**                       | GND | 5                         | GND |

|     |                                                      |     |                                                      |
|-----|------------------------------------------------------|-----|------------------------------------------------------|
|     |                                                      |     |                                                      |
|     | <img src="../../drivers/siemens.files/image005.gif" width="408" /> |     | <img src="../../drivers/siemens.files/image006.gif" width="129" /> |

De aansluiting van de HMI is DB9F, die van de MPI-poort van de Siemens S7-300-serie DB9M.

Verbinding maken met PLC's van de Siemens S7-200/300/1200-serie

**1. 2 Hardwareaansluiting**

Verbindingskabel:

  RJ45-kabel;

  Pintoewijzing RJ45:

**<img src="../../drivers/siemens.files/image014.jpg" width="343" />**

1. IP-adres en poortnummer instellen

Kies op de pagina “Algemeen” van de eigenschappen van de communicatiepoort “Ethernetpoort” als verbindingsinterface en bij de verbindingsdiensten “SIEMENS”, “Siemens S7-200(TCP/IP)/Siemens S7-300(TCP/IP)/Siemens S7-1200(TCP)”;

Stel op de pagina “Parameters” van de eigenschappen van de communicatiepoort het IP-adres en poortnummer in.

Opmerking:

De adressen van PLC en HMI moeten in hetzelfde subnet liggen; stel het subnetmasker dus in op 255.255.255.0.

2. Controleer in de instellingen van de Siemens 1200-PLC of de verbindingsbeveiliging actief is; vink zo nodig de betreffende optie aan, compileer opnieuw en download naar de PLC.

Upload het PLC-programma of maak een nieuw Siemens 1200-project aan in TIA Portal; klik met de rechtermuisknop op het item, kies “Eigenschappen” en vink onder “Beveiliging” de optie “Toegang via PUT/GET-communicatie door remote partner (PLC, HMI, OPC...) toestaan” aan, zoals in de afbeelding hieronder:

**<img src="../../drivers/siemens.files/image015.jpg" width="1152" />**

**2. Software-instellingen**

Kies SIEMENS bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Siemens S7-200/300-serie

Standaardverbindingsparameters van de HMI HM-serie

|                             |                         |                                    |                                              |
|-----------------------------|-------------------------|------------------------------------|----------------------------------------------|
| **Instelling**            | Standaardwaarde |                                    | Instelbereik                                |
| **PLC-type**                | S7-200(PPI)             |                                    | S7-200(PPI)/ S7-300(MPI)                     |
| **Poorttype** | RS485                   |                                    | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                   |                                    | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 8                       |                                    | 7/8                                          |
| **Pariteit**              | EVEN                    |                                    | EVEN/ODD/NONE                                |
| **Stopbits**         | 1                       |                                    | 1/2                                          |
| **Stationsnummer PLC**      | 2                       |                                    | 1 tot 255                                     |
| **Stationsnummer HMI**      | 0                       |                                    | 0 tot 255                                     |
| **Functie**     |                         | **Ondersteund**        |                                              |
| **Offlinesimulatie**     |                         | Ja                                |                                              |
| **Onlinesimulatie**      |                         | Ja                                |                                              |
| **Uitgebreide modus**           |                         | Yes: S7-200(PPI)/ No.: S7-300(MPI) |                                              |
|                             |                         |                                    |                                              |

**3. Bruikbare registers en adresbereik**

Siemens S7-200

|                   |                    |                 |                                                                                                    |
|-------------------|--------------------|-----------------|----------------------------------------------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                                                                        |
| **I**             | dd.o               | 0.0 tot 4095.7   | Bit: Ingangsbeeld, alleen lezen                                                              |
| **Q**             | dd.o               | 0.0 tot 4095.7   | Bit: Uitgangsbeeld                                                                        |
| **M**             | dd.o               | 0.0 tot 4095.7   | Bit: Bitgeheugen (merkers)                                                                                    |
| **S**             | dd.o               | 0.0 tot 4095.7   | Bit: Volgordebesturingsrelais                                                                        |
| **SM**            | ddd.o              | 0.0 tot 4095.7   | Bit: Speciaal bitgeheugen, SM0.0-SM29.7 alleen lezen                                                    |
| **T**             | ddd                | 0 tot 255        | Bit: Timerstatus: alleen lezen                                                                        |
| **C**             | ddd                | 0 tot 255        | Bit: Tellerstatus: alleen lezen                                                                      |
| **VB_Bit**        | ddddd.o            | 0.0 tot 10239.7  | Bit: Bit van het variabelengeheugen                                                                           |
| **IW**            | dd                 | 0 tot 4095       | Woord: Ingangsbeeld, alleen lezen, 8-bits register, elk woord neemt twee adressen in         |
| **QW**            | dd                 | 0 tot 4095       | Woord: Uitgangsbeeld, 8-bits register, elk woord neemt twee adressen in                   |
| **MW**            | dd                 | 0 tot 4095       | Woord: Bitgeheugen (merkers), 8-bits register, elk woord neemt twee adressen in                               |
| **SW**            | dd                 | 0 tot 4095       | Woord: Volgordebesturingsrelais, 8-bits register, elk woord neemt twee adressen in                   |
| **SMW**           | ddd                | 0 tot 4095       | Woord: Speciaal bitgeheugen, SMW0-SMW29 alleen lezen, 8-bits register, elk woord neemt twee adressen in |
| **VB**            | ddddd              | 0 tot 10239      | Woord: Variabelengeheugen, 8-bits register                                                            |
| **VW**            | ddddd              | 0 tot 10238      | Woord: Variabelengeheugen, 8-bits register, elk woord neemt twee adressen in                          |
| **VD**            | ddddd              | 0 tot 10236      | Dubbelwoord: Variabelengeheugen, 8-bits register, elk dubbelwoord neemt vier adressen in           |
| **TV**            | ddd                | 0 tot 255        | Woord: Actuele waarde van de timer                                                                   |
| **CV**            | ddd                | 0 tot 255        | Woord: Actuele waarde van de teller                                                                 |
| **AIW**           | dd                 | 0 tot 62         | Woord: Analoge ingang, alleen lezen, 8-bits register, elk woord neemt twee adressen in                  |
| **AQW**           | dd                 | 0 tot 62         | Woord: Analoge uitgang, alleen schrijven, 8-bits register, elk woord neemt twee adressen in                |

Siemens S7-300 / Siemens S7-300(MPI) / Siemens S7-300tcp

|                   |                    |                     |                                                                                                                                                            |
|-------------------|--------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik**     | **Opmerkingen**                                                                                                                                                |
| **I**             | dddd.o             | 0.0 tot 4095.7       | Bit: Ingangsbeeld                                                                                                                                 |
| **Q**             | dddd.o             | 0.0 tot 4095.7       | Bit: Uitgangsbeeld                                                                                                                                |
| **M**             | dddd.o             | 0.0 tot 4095.7       | Bit: Bitgeheugen (merkers)                                                                                                                                            |
| **DB_Bit**        | DDD:dddd.o         | 0:0.0 tot 255:8192.7 | Bit: Bit van een woord in het DB-bouwsteengebied, bouwsteennummer DD 0 tot 255, woord per bouwsteen dddd 0 tot 8192, bit per woord o 0 tot 7                          |
| **IW**            | dddd               | 0 tot 4095           | Woord: Ingangsbeeld, 8-bits register, elk woord neemt twee adressen in                                                                            |
| **QW**            | dddd               | 0 tot 4095           | Woord: Uitgangsbeeld, 8-bits register, elk woord neemt twee adressen in                                                                           |
| **MW**            | dddd               | 0 tot 4095           | Woord: Bitgeheugen (merkers), 8-bits register, elk woord neemt twee adressen in                                                                                       |
| **DBW**           | DDD:dddd           | 0:0 tot 255:8192     | Woord: DB-bouwsteengebied, bouwsteennummer DD 0 tot 255, woord dddd 0 tot 8192, 8-bits register, elk woord neemt twee adressen in                |
| **DBD**           | DDD:dddd           | 0:0 tot 255:8192     | Dubbelwoord: DB-bouwsteengebied, bouwsteennummer DD 0 tot 255, woord dddd 0 tot 8192, 8-bits register, elk dubbelwoord neemt vier adressen in |

Siemens S7-1200tcp

|                   |                    |                  |                                                                                                                                                            |
|-------------------|--------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik**  | **Opmerkingen**                                                                                                                             |
| **I**             | dddd.o             | 0.0~1024.7       | Bit: Ingangsbeeld                                                                                                                                 |
| **Q**             | dddd.o             | 0.0~1024.7       | Bit: Uitgangsbeeld                                                                                                                                |
| **M**             | dddd.o             | 0.0~8191.7       | Bit: Bitgeheugen (merkers)                                                                                                                                            |
| **DB_Bit**        | DDD:dddd.o         | 0:0.0~255:8192.7 | Bit: Bit van een woord in het DB-bouwsteengebied, bouwsteennummer DD 0 tot 255, woord per bouwsteen dddd 0 tot 8192, bit per woord o 0 tot 7                          |
| **IW**            | dddd               | 0~1024           | Woord: Ingangsbeeld, 8-bits register, elk woord neemt twee adressen in                                                                            |
| **QW**            | dddd               | 0~1024           | Woord: Uitgangsbeeld, 8-bits register, elk woord neemt twee adressen in                                                                           |
| **MW**            | dddd               | 0~8191           | Woord: Bitgeheugen (merkers), 8-bits register, elk woord neemt twee adressen in                                                                                       |
| **DBW**           | DDD:dddd           | 0:0~255:8192     | Woord: DB-bouwsteengebied, bouwsteennummer DD 0 tot 255, woord dddd 0 tot 8192, 8-bits register, elk woord neemt twee adressen in                |
| **DBD**           | DDD:dddd           | 0:0~255:8192     | Dubbelwoord: DB-bouwsteengebied, bouwsteennummer DD 0 tot 255, woord dddd 0 tot 8192, 8-bits register, elk dubbelwoord neemt vier adressen in |

LOGO_TCP

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen** |
| **I**             | dd                 | 1~64            | Bit: Ingangsbeeld     |
| **Q**             | dd                 | 1~64            | Bit: Uitgangsbeeld    |
| **M**             | ddd                | 1~112           | Bit: Bitgeheugen (merkers)                |
| **VB**            | dddd.o             | 0.0~1023.7      | Bit                            |
| **AI**            | dd                 | 1~16            | Woord: Ingangsbeeld    |
| **AQ**            | dd                 | 1~16            | Woord: Uitgangsbeeld   |
| **AM**            | dd                 | 1~64            | Woord: Bitgeheugen (merkers)               |
| **VW**            | dddd               | 0~511           | Word                           |

<img src="../../drivers/siemens.files/image007.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

o: octaal, invoerbereik 0-7;

DDD: bloknummer, invoerbereik 0-255;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Dubbelwoord in de opmerkingen: het gegevenstype van het register moet in de configuratie 32 bits zijn;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/siemens.files/image008.gif" width="595" />

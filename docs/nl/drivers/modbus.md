# Stuurprogramma Modbus

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Met dit stuurprogramma lezen en schrijven HMI's van de HM-serie gegevens of statussen van de <span id="OLE_LINK37"></span><span id="OLE_LINK38"></span>MODBUS-apparaten. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van het MODBUS-apparaat. Lees vóór gebruik van dit stuurprogramma dit hoofdstuk en de technische documentatie van het MODBUS-apparaat aandachtig.</p></td>
</tr>
<tr class="even">
<td><p>Verbinding maken met een MODBUS-apparaat</p>
<p><strong>1.</strong> <strong>Hardwareaansluiting</strong></p>
<p>Verbindingskabel:</p>
<p>RS232<span id="OLE_LINK24"></span><span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK62"></span><span id="OLE_LINK63"></span><span id="OLE_LINK64"></span><strong>HMI HM-serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Modbus-apparaat</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>Door gebruiker gedefinieerde pin</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>Door gebruiker gedefinieerde pin</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>Door gebruiker gedefinieerde pin</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/modbus.files/image002.gif" width="157" /><img src="../../drivers/modbus.files/image003.gif" width="130" />

De aansluiting van de HMI is DB9F. De pintoewijzing van het Modbus-apparaat hangt af van het apparaat.

**RS422**

|                                                                                                                    |     |                   |     |
|--------------------------------------------------------------------------------------------------------------------|-----|-------------------|-----|
| **HMI HM-serie COM1/COM2** |     | **Modbus device** |     |
| 6                                                                                                                  | RX- | Door gebruiker gedefinieerde pin | TX- |
| 7                                                                                                                  | RX+ | Door gebruiker gedefinieerde pin | TX+ |
| 8                                                                                                                  | TX- | Door gebruiker gedefinieerde pin | RX- |
| 9                                                                                                                  | TX+ | Door gebruiker gedefinieerde pin | RX+ |

<img src="../../drivers/modbus.files/image004.gif" width="157" /><img src="../../drivers/modbus.files/image005.gif" width="130" />

De aansluiting van de HMI is DB9F. De pintoewijzing van het Modbus-apparaat hangt af van het apparaat.

**RS485**

|                                                                                       |     |                   |     |
|---------------------------------------------------------------------------------------|-----|-------------------|-----|
| **HMI HM-serie COM1/COM2** |     | **Modbus device** |     |
| 8                                                                                     | D-  | Door gebruiker gedefinieerde pin | B   |
| 9                                                                                     | D+  | Door gebruiker gedefinieerde pin | A   |

<img src="../../drivers/modbus.files/image006.gif" width="157" /><img src="../../drivers/modbus.files/image007.gif" width="130" />

De aansluiting van de HMI is een 9-polige Sub-D-bus. De pintoewijzing van het Modbus-apparaat hangt af van het apparaat.

**TCP/IP (directe RJ45-verbinding)**

|                                                                                                                    |      |                   |      |
|--------------------------------------------------------------------------------------------------------------------|------|-------------------|------|
| **HMI HM-serie COM1/COM2** |      | **Modbus device** |      |
| 1                                                                                                                  | TX+  | 3                 | RX+  |
| 2                                                                                                                  | TX-  | 6                 | RX-  |
| 3                                                                                                                  | RX+  | 1                 | TX+  |
| 4                                                                                                                  | BD4+ | 4                 | BD4+ |
| 5                                                                                                                  | BD4- | 5                 | BD4- |
| 6                                                                                                                  | RX-  | 2                 | TX-  |
| 7                                                                                                                  | BD3+ | 7                 | BD3+ |
| 8                                                                                                                  | BD3- | 8                 | BD3- |

|     |                                                    |     |                                                     |     |                                                    |
|-----|----------------------------------------------------|-----|-----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                    |     |                                                     |     |                                                    |
|     | <img src="../../drivers/modbus.files/image008.gif" width="95" /> |     |                                                     |     |                                                    |
|     |                                                    |     |                                                     |     | <img src="../../drivers/modbus.files/image009.gif" width="95" /> |
|     |                                                    |     | <img src="../../drivers/modbus.files/image010.gif" width="267" /> |     |                                                    |
|     |                                                    |     |                                                     |     |                                                    |
|     |                                                    |     |                                                     |     |                                                    |

<span id="OLE_LINK68"></span><span id="OLE_LINK69"></span><span id="OLE_LINK70"></span>

De aansluiting van de HMI is RJ45, die van het Modbus-apparaat RJ45.

**TCP/IP (RJ45-verbinding via router)**

|                       |      |               |      |
|-----------------------|------|---------------|------|
| **HM-HMI COM1/COM2** |      | Modbus device |      |
| 1                     | TX+  | 3             | RX+  |
| 2                     | TX-  | 6             | RX-  |
| 3                     | RX+  | 1             | TX+  |
| 4                     | BD4+ | 4             | BD4+ |
| 5                     | BD4- | 5             | BD4- |
| 6                     | RX-  | 2             | TX-  |
| 7                     | BD3+ | 7             | BD3+ |
| 8                     | BD3- | 8             | BD3- |

<img src="../../drivers/modbus.files/image011.gif" width="95" />

|     |                                                     |     |                                                    |
|-----|-----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                     |     |                                                    |
|     |                                                     |     | <img src="../../drivers/modbus.files/image012.gif" width="95" /> |
|     | <img src="../../drivers/modbus.files/image013.gif" width="267" /> |     |                                                    |
|     |                                                     |     |                                                    |

De aansluiting van de HMI is RJ45, die van het Modbus-apparaat RJ45.

**2. Software-instellingen**

Kies Modbus bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van het apparaat de technische documentatie van het Modbus-apparaat.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | RTU Master                  | RTU/RTU_S/ASCII/ASCII_S Master               |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 8                           | 7/8                                          |
| **Pariteit**              | NONE                        | EVEN/ODD/NONE                                |
| **Stopbits**         | 1                           | 1/2                                          |
| **Stationsnummer PLC**      | 1                           | 0~255                                        |
| **Stationsnummer HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Functie** | **Ondersteund** |
| **Offlinesimulatie** | Ja                         |
| **Onlinesimulatie**  | Ja                         |
| **Uitgebreide modus**       | Ja                         |

<img src="../../drivers/modbus.files/image014.gif" width="595" />

Opmerking: RTU_S en ASCII_S schrijven gegevens met functiecode 0x10 (ongeacht de lengte van de geschreven gegevens);

·Is het stationsnummer van de PLC 0, dan werkt het systeem in broadcastmodus.

**3. Bruikbare registers en adresbereik**

|                   |                    |                 |                                                                                                  |
|-------------------|--------------------|-----------------|--------------------------------------------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                                                                      |
| 0x                | ddddd              | 0~65535         | Bit: Ingangsspoel                                                                                  |
| 1x                | ddddd              | 0~65536         | Bit: Ingangsspoel, alleen lezen                                                                       |
| 3x_Bit            | ddddd.DD           | 0.00~65535.15   | Bit: Bit van een 16-bits ingangsregister, alleen lezen                       |
| 4x_Bit            | ddddd.DD           | 0.00~65535.15   | Bit: Bit van een 16-bits uitgangsregister                                                               |
| 3x                | ddddd              | 0~65535         | Woord: 16-bits ingangsregister, alleen lezen                                                           |
| 4x                | ddddd              | 0~65535         | Woord: 16-bits uitgangsregister                                                                     |
| 3x_D              | ddddd              | 0~65535         | Dubbelwoord: Ingangsregister, hoge en lage 16 bits van het 3x-dubbelwoord verwisseld, alleen lezen |
| 4x_D              | ddddd              | 0~65535         | Dubbelwoord: Uitgangsregister, hoge en lage 16 bits van het 4x-dubbelwoord verwisseld           |

Modbus Slave

|                       |                             |                 |                                                                |
|-----------------------|-----------------------------|-----------------|----------------------------------------------------------------|
| **Intern register** | **Ondersteunde functiecode** | **Invoerbereik** | **Opmerking**                                                     |
| LB                    | 01/02/05/15                 | 0~59999         | Bit：Intern adres van het touchscreen lezen en schrijven (LB) |
| LW                    | 03/04/06/16                 | 0~59999         | Woord：Intern adres van het touchscreen lezen en schrijven  |

<img src="../../drivers/modbus.files/image015.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

DD: 16 bits, invoerbereik 0-15;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Dubbelwoord in de opmerkingen: het gegevenstype van het register moet in de configuratie 32 bits zijn;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/modbus.files/image016.gif" width="595" />

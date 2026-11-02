# Stuurprogramma AIBUS-apparaten

Met dit stuurprogramma leest en schrijft de HMI van de HM-serie gegevens of statussen van AIBUS-apparaten via het AIBUS-protocol. De seriële verbinding loopt tussen de seriële poort van de HMI en die van het AIBUS-apparaat. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van het AIBUS-apparaat.

**1.  Hardwareaansluiting**

Verbindingskabel:

RS232 (seriële poort, protocol RS232)

|                             |     |                   |     |
|-----------------------------|-----|-------------------|-----|
| **HMI HM-serie COM1/COM2** |     | **AIBUS-apparaat**  |     |
| 2                           | RX  | Door gebruiker gedefinieerde pin | TX  |
| 3                           | TX  | Door gebruiker gedefinieerde pin | RX  |
| 5                           | GND | Door gebruiker gedefinieerde pin | GND |

<img src="../../drivers/aibus.files/image002.gif" width="157" /><img src="../../drivers/aibus.files/image003.gif" width="130" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>De poort van het touchscreen is een 9-polige Sub-D-bus. De pintoewijzing van het AIBUS-apparaat hangt af van het apparaat.</p>
<p><strong>RS422 (seriële poort, protocol RS422)</strong></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI HM-serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>AIBUS-apparaat</strong></p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>RX-</p></td>
<td><p>Door gebruiker gedefinieerde pin</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>RX+</p></td>
<td><p>Door gebruiker gedefinieerde pin</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>Door gebruiker gedefinieerde pin</p></td>
<td><p>RX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>Door gebruiker gedefinieerde pin</p></td>
<td><p>RX+</p></td>
</tr>
</tbody>
</table>
<table>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><img src="../../drivers/aibus.files/image004.gif" width="280" /></td>
</tr>
</tbody>
</table>
 &#10;<br />
&#10;<p>De poort van het touchscreen is een 9-polige Sub-D-bus. De pintoewijzing van het AIBUS-apparaat hangt af van het apparaat.</p>
<p><strong>RS485 (seriële poort, protocol RS485)</strong></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>Touchscreen COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>AIBUS-apparaat</strong></p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>D-</p></td>
<td><p>Door gebruiker gedefinieerde pin</p></td>
<td><p>B</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>D+</p></td>
<td><p>Door gebruiker gedefinieerde pin</p></td>
<td><p>A</p></td>
</tr>
</tbody>
</table>
<p>De poort van het touchscreen is een 9-polige Sub-D-bus. De pintoewijzing van het AIBUS-apparaat hangt af van het apparaat.</p></td>
</tr>
</tbody>
</table>

**2. Software-instellingen**

ü Kies AIBUS Protocol bij het aangesloten apparaat.

ü Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

ü Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van het AIBUS-apparaat.

ü Zie voor de instellingen van het AIBUS-apparaat de technische documentatie ervan.

Standaardverbindingsparameters van het touchscreen

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | AIBUS Protocol              | AIBUS Protocol                               |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 8                           | 7/8                                          |
| **Pariteit**              | NONE                        | EVEN/ODD/NONE                                |
| **Stopbits**         | 1                           | 1/2                                          |
| **Stationsnummer PLC**      | 1                           | 1~255                                        |
| **Stationsnummer HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Functie** | **Ondersteund** |
| **Offlinesimulatie** | Ja                         |
| **Onlinesimulatie**  | Ja                         |
| **Uitgebreide modus**       | Ja                         |

**3. Bruikbare registers en adresbereik**

|                   |                    |                 |                      |
|-------------------|--------------------|-----------------|----------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**          |
| **Parameter**     | ddd                | 0~255           | Woord: parameter |
| **PV**            | d                  | 0               | Woord: uitgangswaarde   |
| **SV**            | d                  | 0               | Woord: setpoint      |
| **MV**            | d                  | 0               | Woord: statuswaarde    |
| **Status**        | d                  | 0               | Woord: statuswaarde    |

<img src="../../drivers/aibus.files/image005.gif" width="595" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Opmerking: </p>
<p>• ·d: decimaal, invoerbereik 0-9;</p>
<p>• ·“Woord” in de opmerkingen: het register kan alleen als woord worden gebruikt;</p>
<p>• Namen en bereiken van de registers kunnen per apparaatmodel verschillen.</p>
<p>Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat.</p></td>
</tr>
</tbody>
</table>

<img src="../../drivers/aibus.files/image006.gif" width="595" />

# Stuurprogramma Hitachi

Met dit stuurprogramma leest en schrijft de HMI van de HM-serie gegevens of statussen van de registers van PLC's Hitachi E/EH-serie. De seriële verbinding loopt tussen de seriële poort van de HMI en die van de PLC. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van de PLC.

**1. Hardwareaansluiting**

Verbindingskabel:

RS232 (seriële poort, protocol RS232)

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI HM-serie COM1/COM2</strong></p></td>
<td colspan="3"><p><strong>Serie Hitachi E/EH</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td colspan="2"><p>SD</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>6</p></td>
<td colspan="2"><p>RD</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>1</p></td>
<td colspan="2"><p>SG</p></td>
</tr>
<tr class="odd">
<td colspan="2" rowspan="2"></td>
<td><p>4</p></td>
<td><p>PHL</p></td>
<td rowspan="2"><p>4-7</p>
<p>Kortsluiting</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p>DR</p></td>
</tr>
</tbody>
</table>

|     |                                                      |     |                                                      |     |                                                     |
|-----|------------------------------------------------------|-----|------------------------------------------------------|-----|-----------------------------------------------------|
|     |                                                      |     |                                                      |     |                                                     |
|     |                                                      |     |                                                      |     | <img src="../../drivers/hitachi.files/image002.gif" width="91" /> |
|     | <img src="../../drivers/hitachi.files/image003.gif" width="130" /> |     |                                                      |     |                                                     |
|     |                                                      |     | <img src="../../drivers/hitachi.files/image004.gif" width="278" /> |     |                                                     |
|     |                                                      |     |                                                      |     |                                                     |
|     |                                                      |     |                                                      |     |                                                     |

De aansluiting van de HMI HM-serie is DB9F, die van het apparaat RJ45.

**2. Software-instellingen**

Kies Hitachi Industrial bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Hitachi E/EH-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Serie Hitachi E/EH         | Serie Hitachi E/EH                          |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 7                           | 7/8                                          |
| **Pariteit**              | EVEN                        | EVEN/ODD/NONE                                |
| **Stopbits**         | 1                           | 1/2                                          |
| **Stationsnummer PLC**      | 0                           | 0~255                                        |
| **Stationsnummer HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Functie** | **Ondersteund** |
| **Offlinesimulatie** | Ja                         |
| **Onlinesimulatie**  | Ja                         |
| **Uitgebreide modus**       | Ja                         |

**3. Bruikbare registers en adresbereik**

|                   |                    |                 |                                                                    |
|-------------------|--------------------|-----------------|--------------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                                        |
| **X**             | hhhh               | 0~ffff          | Bit: Externe digitale ingang, alleen lezen                     |
| **Y**             | hhhh               | 0~ffff          | Bit: Externe digitale uitgang |
| **M**             | hhhh               | 0~ffff          | Bit: Intern relais (merker)                                                |
| **R**             | hhhh               | 0~ffff          | Bit: Intern register                                             |
| **T**             | hhhh               | 0~ffff          | Bit: Timerstatus                                               |
| **L**             | hhhh               | 0~ffff          | Bit: Linkrelais                                                    |
| **WX**            | hhhh               | 0~ffff          | Woord: Externe digitale ingang                               |
| **WY**            | hhhh               | 0~ffff          | Woord: Externe digitale uitgang                              |
| **WM**            | hhhh               | 0~ffff          | Woord: Intern relais (merker)                                               |
| **WR**            | hhhh               | 0~ffff          | Woord: Intern register                                            |
| **WL**            | hhhh               | 0~ffff          | Woord: Linkrelais                                                   |
| **TC**            | hhhh               | 0~ffff          | Woord: Actuele waarde van timer/teller                               |

<img src="../../drivers/hitachi.files/image005.gif" width="595" />

Opmerking:

h: hexadecimaal, invoerbereik 0-9, a-f;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat.

<img src="../../drivers/hitachi.files/image006.gif" width="595" />

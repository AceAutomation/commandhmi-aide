# Stuurprogramma Yokogawa

Met dit stuurprogramma leest en schrijft de HMI van de HM-serie gegevens of statussen van de registers van PLC's Yokogawa FA-M3-serie. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van de PLC.

Verbinding maken met PLC's van de Yokogawa FA-M3-serie

**1. Hardwareaansluiting**

Verbindingskabel:

RS232 <span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>

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
<td colspan="2"><p>HM-serie COM1/COM2</p></td>
<td colspan="3"><p><strong>Serie Yokogawa FA-M3</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>5</strong></p></td>
<td><p>GND</p></td>
<td><p>5</p></td>
<td><p>SG</p></td>
<td rowspan="2"><p>4-5 doorverbonden</p>
<p>Weerstand van 220 Ω in serie</p></td>
</tr>
<tr class="odd">
<td><p><strong>6</strong></p></td>
<td><p>RX-</p></td>
<td><p>4</p></td>
<td><p>SDB</p></td>
</tr>
<tr class="even">
<td><p><strong>7</strong></p></td>
<td><p>RX+</p></td>
<td><p>3</p></td>
<td><p>SDA</p></td>
<td rowspan="2"><p>2-3 doorverbonden</p>
<p>Weerstand van 220 Ω in serie</p></td>
</tr>
<tr class="odd">
<td><p><strong>8</strong></p></td>
<td><p>TX-</p></td>
<td><p>2</p></td>
<td><p>RDB</p></td>
</tr>
<tr class="even">
<td><p><strong>9</strong></p></td>
<td><p>TX+</p></td>
<td><p>1</p></td>
<td colspan="2"><p>RDA</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>6</p></td>
<td><p>CSA</p></td>
<td rowspan="2"><p>6-7 doorverbonden</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>7</p></td>
<td><p>ERA</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>8</p></td>
<td><p>CSB</p></td>
<td rowspan="2"><p>8-9 doorverbonden</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>9</p></td>
<td><p>ERB</p></td>
</tr>
</tbody>
</table>

De aansluiting van de HMI is DB9F, die van de Yokogawa FA-M3-serie SIO.

**2. Software-instellingen**

Kies Yokogawa Electric Corp. bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Yokogawa FA-M3-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Yokogawa FA-M3              | Yokogawa FA-M3                               |
| **Poorttype** | RS422                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 8                           | 7/8                                          |
| **Pariteit**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Stopbits**         | 1                           | 1/2                                          |
| **Stationsnummer PLC**      | 1                           | 0 tot 255                                     |
| **Stationsnummer HMI**      | 0                           | 0 tot 255                                     |

|                         |                             |
|-------------------------|-----------------------------|
| **Functie** | **Ondersteund** |
| **Offlinesimulatie**  | Ja                         |
| **Onlinesimulatie**   | Ja                         |
| **Uitgebreide modus**       | Nee                          |

**3. Bruikbare registers en adresbereik**

|                   |                    |                 |                                                           |
|-------------------|--------------------|-----------------|-----------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                               |
| **X**             | ddddd              | 0 tot 71664      | Bit: Ingang, niet aaneengesloten, afhankelijk van het slotnummer  |
| **Y**             | ddddd              | 0 tot 71664      | Bit: Uitgang, niet aaneengesloten, afhankelijk van het slotnummer |
| **M**             | ddddd              | 0 tot 16384      | Bit: Speciaal relais                                        |
| **I**             | ddddd              | 0 tot 71024      | Bit: Intern relais (merker)                                       |
| **L**             | ddddd              | 0 tot 9984       | Bit: Linkrelais, niet aaneengesloten                            |
| **D**             | ddddd              | 0 tot 8192       | Woord: Dataregister                                       |
| **B**             | ddddd              | 0 tot 32768      | Woord: Bestandsregister                                       |
| **V**             | ddddd              | 0 tot 64         | Woord: Externe digitale uitgang                     |
| **W**             | ddddd              | 0 tot 71024      | Woord: Linkregister, niet aaneengesloten                        |
| **Z**             | ddddd              | 0 tot 512        | Woord: Speciaal register                                    |

<img src="../../drivers/yokogawa.files/image002.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/yokogawa.files/image002.gif" width="595" />

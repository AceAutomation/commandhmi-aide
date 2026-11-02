# Stuurprogramma Vigor

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Met dit stuurprogramma lezen en schrijven HMI's van de HM-serie gegevens of statussen van registers van PLC's uit de serie Vigor V/VH/VB/M. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik van dit stuurprogramma dit hoofdstuk en de technische documentatie van de PLC aandachtig.</p></td>
</tr>
<tr class="even">
<td><p>Verbinding maken met een PLC uit de serie Vigor V/VH/VB/M</p>
<p><strong>1.  Hardwareaansluiting</strong></p>
<p>Verbindingskabel:</p>
<p>RS232 <span id="OLE_LINK3"></span><span id="OLE_LINK2"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI HM-serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Serie Vigor V/VH/VB/M</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>3</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>2</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>4</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/vigor.files/image002.gif" width="63" /><img src="../../drivers/vigor.files/image003.gif" width="318" /><img src="../../drivers/vigor.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

De aansluiting van de HMI is DB9F, die van de Vigor V/VH/VB/M-serie DB9M.

**2. Software-instellingen**

Kies Vigor Electric Corp. bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Vigor V/VH/VB/M-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Serie V/VH/VB/M            | Serie V/VH/VB/M                             |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 7                           | 7/8                                          |
| **Pariteit**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Stopbits**         | 1                           | 1/2                                          |
| **Stationsnummer PLC**      | 0                           | 0 tot 255                                     |
| **Stationsnummer HMI**      | 0                           | 0 tot 255                                     |

|                         |                             |
|-------------------------|-----------------------------|
| **Functie** | **Ondersteund** |
| **Offlinesimulatie**  | Ja                         |
| **Onlinesimulatie**   | Ja                         |
| **Uitgebreide modus**       | Nee                          |

**3. Bruikbare registers en adresbereik**

|                   |                    |                 |                                       |
|-------------------|--------------------|-----------------|---------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                           |
| **X**             | ooo                | 0 tot 777        | Bit: Ingangscontact                    |
| **Y**             | ooo                | 0 tot 777        | Bit: Uitgangscontact                   |
| **M**             | dddd               | 0 tot 8999       | Bit: Intern relais (merker)                   |
| **SM**            | dddd               | 9000 tot 9255    | Bit: Speciaal intern relais           |
| **S**             | dddd               | 0 tot 999        | Bit: Staprelais                   |
| **T**             | ddd                | 0 tot 255        | Bit: Timerstatus                      |
| **C**             | ddd                | 0 tot 255        | Bit: Tellerstatus                    |
| **D**             | dddd               | 0 tot 8999       | Woord: Dataregister                   |
| **SD**            | dddd               | 9000 tot 9255    | Woord: Speciaal dataregister           |
| **TV**            | ddd                | 0 tot 255        | Woord: Actuele waarde van de timer      |
| **CV**            | ddd                | 0 tot 199        | Woord: Actuele waarde van de teller    |
| **CV32**          | ddd                | 200 tot 255      | Woord: Actuele waarde van de 32-bits teller |

<img src="../../drivers/vigor.files/image005.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

o: octaal, invoerbereik 0-7;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Dubbelwoord in de opmerkingen: het gegevenstype van het register moet in de configuratie 32 bits zijn;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen;

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat.

<img src="../../drivers/vigor.files/image005.gif" width="595" />

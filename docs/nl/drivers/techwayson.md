# Stuurprogramma Techwayson

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Met dit stuurprogramma lezen en schrijven HMI's van de HM-serie gegevens of statussen van registers van PLC's uit de serie TaiLing DX. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik van dit stuurprogramma dit hoofdstuk en de technische documentatie van de PLC aandachtig.</p></td>
</tr>
<tr class="even">
<td><p>Verbinding maken met een PLC uit de serie TaiLing DX</p>
<p><strong>1.  Hardwareaansluiting</strong></p>
<p>Verbindingskabel:</p>
<p>RS232 <span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>(seriële poort, protocol RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI HM-serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Serie TaiLing DX</strong></p></td>
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
<td><p>5</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/techwayson.files/image002.gif" width="130" /><img src="../../drivers/techwayson.files/image003.gif" width="290" /><img src="../../drivers/techwayson.files/image004.gif" width="129" /></p></td>
</tr>
</tbody>
</table>

De aansluiting van de HMI is DB9F, die van de PLC MD8M.

**2. Software-instellingen**

Kies TaiLing Electric bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de TaiLing DX-serie.

Standaardverbindingsparameters van de HMI HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Serie Techwayson V80       | Serie Techwayson V80                        |
| **Poorttype** | RS232                       | RS232                                        |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 8                           | 7/8                                          |
| **Pariteit**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Stopbits**         | 1                           | 1/2                                          |
| **Stationsnummer PLC**      | 1                           | 0~255                                        |
| **Stationsnummer HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Functie** | **Ondersteund** |
| **Offlinesimulatie**  | Ja                         |
| **Onlinesimulatie**   | Ja                         |
| **Uitgebreide modus**       | Ja                         |

**3. Bruikbare registers en adresbereik**

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                  |
| **X**             | oooo               | 0 tot 377        | Bit: Ingangsspoel, alleen lezen                   |
| **Y**             | oooo               | 0 tot 377        | Bit: Uitgangsspoel                             |
| **M**             | dddd               | 0 tot 7999       | Bit: Tussenrelais (merker)                      |
| **SM**            | dddd               | 8000 tot 8999    | Bit: Speciaal tussenrelais              |
| **S**             | dddd               | 0 tot 999        | Bit: Statusbit                               |
| **T**             | dddd               | 0 tot 256        | Bit: Timerstatus                             |
| **C**             | dddd               | 0 tot 256        | Bit: Tellerstatus                           |
| **D**             | dddd               | 0 tot 7999       | Woord: Register                               |
| **SD**            | dddd               | 8000 tot 8999    | Woord: Speciaal register                       |
| **TV**            | dddd               | 0 tot 255        | Woord: Actuele waarde van de timer             |
| **CV**            | dddd               | 0 tot 199        | Woord: Actuele waarde van de teller           |
| **CV32**          | dddd               | 200 tot 255      | Dubbelwoord: Actuele waarde van de 32-bits teller |

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                            |
| **0x**            | dddd               | 1~9984          | Bit: Uitgangsspoel                       |
| **1x**            | dddd               | 1~2048          | Bit: Ingangsspoel, alleen lezen             |
| **3x**            | dddd               | 1~512           | Woord: 16-bits ingangsregister, alleen lezen |
| **4x**            | dddd               | 1~9999          | Woord: 16-bits holdingregister          |

<img src="../../drivers/techwayson.files/image005.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

o: octaal, invoerbereik 0-7;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Dubbelwoord in de opmerkingen: het gegevenstype van het register moet in de configuratie 32 bits zijn;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/techwayson.files/image006.gif" width="595" />

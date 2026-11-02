# Stuurprogramma Inovance

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Met dit stuurprogramma lezen en schrijven HMI's van de HM-serie gegevens of statussen van registers van PLC's uit de serie Inovance H1u/H2u. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik van dit stuurprogramma dit hoofdstuk en de technische documentatie van de PLC aandachtig.</p></td>
</tr>
<tr class="even">
<td><p>Verbinding maken met een PLC uit de serie Inovance H1u/H2u</p>
<p><strong>1.  Hardwareaansluiting</strong></p>
<p>Verbindingskabel:</p>
<p>RS232 (seriële poort, protocol RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HM-HMI COM1/COM2</p></td>
<td colspan="2"><p>Serie Inovance H1u/H2u</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>RX-</p></td>
<td><p>4</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>RX+</p></td>
<td><p>7</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>1</p></td>
<td><p>RX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>2</p></td>
<td><p>RX+</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/inovance.files/image002.gif" width="281" /><img src="../../drivers/inovance.files/image003.gif" width="130" /><img src="../../drivers/inovance.files/image004.gif" width="145" />

De aansluiting van de HMI is DB9F, die van de Inovance H1u/H2u-serie DB9M.

**2. Software-instellingen**

Kies Inovance Technology Corp. bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Inovance H1u/H2u-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | H1u/H2u                     | H1u/H2u                                      |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
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
| **Uitgebreide modus**       | Nee                          |

**3. Bruikbare registers en adresbereik**

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                  |
| **X**             | oooo               | 0~377           | Bit: Ingangsspoel, alleen lezen                   |
| **Y**             | oooo               | 0~377           | Bit: Uitgangsspoel                             |
| **M**             | dddd               | 0~7999          | Bit: Tussenrelais (merker)                      |
| **SM**            | dddd               | 8000~8999       | Bit: Speciaal tussenrelais              |
| **S**             | dddd               | 0~999           | Bit: Statusbit                              |
| **T**             | dddd               | 0~256           | Bit: Timerstatus                         |
| **C**             | dddd               | 0~256           | Bit: Tellerstatus                       |
| **D**             | dddd               | 0~7999          | Woord: Register                               |
| **SD**            | dddd               | 8000~8999       | Woord: Speciaal register                       |
| **TV**            | dddd               | 0~255           | Woord: Actuele waarde van de timer                 |
| **CV**            | dddd               | 0~199           | Woord: Actuele waarde van de teller               |
| **CV32**          | dddd               | 200~255         | Dubbelwoord: Actuele waarde van de 32-bits teller |

<img src="../../drivers/inovance.files/image005.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

o: octaal, invoerbereik 0-7;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Dubbelwoord in de opmerkingen: het gegevenstype van het register moet in de configuratie 32 bits zijn;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/inovance.files/image006.gif" width="595" />

# Stuurprogramma Delta

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Met dit stuurprogramma lezen en schrijven HMI's van de HM-serie gegevens of statussen van de <span id="OLE_LINK42"></span><span id="OLE_LINK43"></span>Registers van PLC's uit de serie Delta DVP. De seriële verbinding loopt tussen de seriële poort van de HMI en die van de PLC. Lees vóór gebruik van dit stuurprogramma dit hoofdstuk en de technische documentatie van de PLC aandachtig.</p></td>
</tr>
<tr class="even">
<td><p>Verbinding maken met een PLC uit de serie Delta DVP</p>
<p><strong>1.  Hardwareaansluiting</strong></p>
<p>Verbindingskabel:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK53"></span><span id="OLE_LINK2"></span> (seriële poort, protocol RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HMI HM-serie COM1/COM2</p></td>
<td colspan="2"><p>Serie Delta DVP</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>4</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/delta.files/image008.gif" width="281" /><img src="../../drivers/delta.files/image009.gif" width="146" /><img src="../../drivers/delta.files/image010.gif" width="130" />  </p>
<p><span id="OLE_LINK54"></span>De aansluiting van de HMI uit de HM-serie is DB9F, die van de Delta DVP-PLC MD8M.</p>
<p>RS485 (seriële poort, protocol RS485)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HMI HM-serie COM1/COM2</p></td>
<td><p>Serie Delta DVP</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>B</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>A</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/delta.files/image011.gif" width="130" /><img src="../../drivers/delta.files/image012.gif" width="156" /></p>
<p>De aansluiting van de HM-serie is DB9F, die van de Delta DVP-PLC een tweedraadsklem.</p></td>
</tr>
</tbody>
</table>

**2. Software-instellingen**

ü Kies Delta Corporation bij het aangesloten apparaat.

ü Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

ü Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

ü Zie voor de instellingen van de PLC de technische documentatie van de Delta DVP-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Delta DVP Series            | Delta DVP Series                             |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
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

**3. Bruikbare registers en adresbereik**

|                   |                    |                 |                                               |
|-------------------|--------------------|-----------------|-----------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                   |
| **X**             | ooo                | 0~377           | Bit: Ingang, alleen lezen        |
| **Y**             | ooo                | 0~377           | Bit: Uitgang                  |
| **M**             | dddd               | 0~4095          | Bit: Hulprelais (merker)                          |
| **S**             | dddd               | 0~1023          | Bit: Intern relais (merker)                           |
| **T**             | ddd                | 0~255           | Bit: Timerstatus                             |
| **C**             | ddd                | 0~255           | Bit: Tellerstatus                           |
| **D**             | dddd               | 0~9999          | Woord: Tijdelijk datageheugen                  |
| **TV**            | ddd                | 0~255           | Woord: Actuele waarde van de timer                  |
| **CV**            | ddd                | 0~199           | Woord: Actuele waarde van de teller                |
| **CV32**          | ddd                | 200~255         | Dubbelwoord: Actuele waarde van de 32-bits teller |

<img src="../../drivers/delta.files/image013.gif" width="595" />

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p>Opmerking:</p>
<p>d: decimaal, invoerbereik 0-9;</p>
<p>o: octaal, invoerbereik 0-7;</p>
<p>Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;</p>
<p>Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;</p>
<p>Dubbelwoord in de opmerkingen: het gegevenstype van het register moet in het project 32 bits zijn;</p>
<p>Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;</p>
<p>Namen en bereiken van de registers kunnen per apparaatmodel verschillen.</p>
<p>Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat.</p></td>
</tr>
</tbody>
</table>

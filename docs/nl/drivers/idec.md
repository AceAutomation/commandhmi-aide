# Stuurprogramma IDEC

Met dit stuurprogramma leest en schrijft de HMI van de HM-serie gegevens of statussen van de registers van PLC's MicroSmart FC4A/FC5A/FC6A-serie. De seriële verbinding loopt tussen de seriële poort van de HMI en die van de PLC. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van de PLC.

**Verbinding maken met de MicroSmart FC4A/FC5A-serie**

1\. Hardwareaansluiting

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
<td colspan="3"><p><strong>Macro Smart FC4A/FC5A</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>3</p></td>
<td colspan="2"><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>4</p></td>
<td colspan="2"><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>6</p></td>
<td><p>GND</p></td>
<td rowspan="2"><p>6-7</p>
<p>Kortsluiting</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>7</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>

|     |                                                   |     |                                                   |     |                                                   |
|-----|---------------------------------------------------|-----|---------------------------------------------------|-----|---------------------------------------------------|
|     |                                                   |     |                                                   |     |                                                   |
|     |                                                   |     |                                                   |     | <img src="../../drivers/idec.files/image002.gif" width="146" /> |
|     | <img src="../../drivers/idec.files/image003.gif" width="129" /> |     |                                                   |     |                                                   |
|     |                                                   |     | <img src="../../drivers/idec.files/image004.gif" width="280" /> |     |                                                   |
|     |                                                   |     |                                                   |     |                                                   |
|     |                                                   |     |                                                   |     |                                                   |

De aansluiting van de HMI is DB9F, die van de MicroSmart FC4A/FC5A-serie MD8M.

**2. Software-instellingen**

Kies Allen-Bradley bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de MicroSmart FC4A/FC5A/FC6A-serie.

Standaardverbindingsparameters van de HMI HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Macro Smart FC4A            | Macro Smart FC4A/ Macro Smart FC5A           |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 7                           | 7/8                                          |
| **Pariteit**              | EVEN                        | EVEN/ODD/NONE                                |
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

Macro Smart FC4A

|                   |                    |                 |                                                |
|-------------------|--------------------|-----------------|------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                    |
| **I**             | ddd                | 0~255           | Bit: Externe digitale ingang, alleen lezen |
| **Q**             | ddd                | 0~255           | Bit: Externe digitale uitgang           |
| **M**             | dddd               | 0~1023          | Bit: Intern relais (merker)                            |
| **SM**            | ddd                | 0~215           | Bit: Intern register                         |
| **R**             | ddd                | 0~255           | Woord: Schuifregister                           |
| **D**             | ddd                | 0~1299          | Woord: Dataregister                            |
| **TV**            | ddd                | 0~127           | Woord: Actuele waarde van de timer                   |
| **CV**            | ddd                | 0~127           | Woord: Actuele waarde van de teller                 |

Macro Smart FC5A

|                   |                    |                 |                                                |
|-------------------|--------------------|-----------------|------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                    |
| **I**             | ddd                | 0~255           | Bit: Externe digitale ingang, alleen lezen |
| **Q**             | ddd                | 0~255           | Bit: Externe digitale uitgang           |
| **M**             | dddd               | 0~2047          | Bit: Intern relais (merker)                            |
| **SM**            | ddd                | 0~215           | Bit: Intern register                         |
| **R**             | ddd                | 0~255           | Woord: Schuifregister                           |
| **D**             | ddd                | 0~42000         | Woord: Dataregister                            |
| **TV**            | ddd                | 0~255           | Woord: Actuele waarde van de timer                   |
| **CV**            | ddd                | 0~255           | Woord: Actuele waarde van de teller                 |

Macro Smart FC6A Tcp/IP

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Registernaam</strong></p></td>
<td><p><strong>Adresformaat</strong></p></td>
<td><p><strong>Invoerbereik</strong></p></td>
<td><p><strong>Opmerkingen</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>I</strong></p></td>
<td><p>Ddo</p></td>
<td><p>0~627</p></td>
<td><p>Bit: externe digitale ingang, alleen lezen</p></td>
</tr>
<tr class="odd">
<td><p><strong>Q</strong></p></td>
<td><p>Ddo</p></td>
<td><p>0~627</p></td>
<td><p>Bit：Bit: externe digitale uitgang</p></td>
</tr>
<tr class="even">
<td><p><strong>M</strong></p></td>
<td><p>Dddo</p></td>
<td><p>0~7997</p>
<p>8000~8317</p>
<p>10000~17497</p></td>
<td><p>Bit：intern relais (merker)</p></td>
</tr>
<tr class="odd">
<td><p><strong>R</strong></p></td>
<td><p>Ddd</p></td>
<td><p>0~255</p></td>
<td><p>Bit：schuifregister</p></td>
</tr>
<tr class="even">
<td><p><strong>T</strong></p></td>
<td><p>Dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Bit: timerstatus (alleen lezen)</p></td>
</tr>
<tr class="odd">
<td><p><strong>C</strong></p></td>
<td><p>Dddd</p></td>
<td><p>0~511</p></td>
<td><p>Bit: tellerstatus (alleen lezen)</p></td>
</tr>
<tr class="even">
<td><p><strong>D</strong></p></td>
<td><p>ddddd</p></td>
<td><p>0~8499</p>
<p>10000~55999</p></td>
<td><p>Woord: register</p></td>
</tr>
<tr class="odd">
<td><p><strong>TV</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Woord: actuele waarde van de timer (alleen lezen)</p></td>
</tr>
<tr class="even">
<td><p><strong>CV</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~511</p></td>
<td><p>Woord: actuele waarde van de teller (alleen lezen)</p></td>
</tr>
<tr class="odd">
<td><p><strong>TS</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>• Woord: instelwaarde van de timer (alleen lezen)</p></td>
</tr>
<tr class="even">
<td><p><strong>CS</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~511</p></td>
<td><p>Woord: instelwaarde van de teller (alleen lezen)</p></td>
</tr>
</tbody>
</table>

<img src="../../drivers/idec.files/image009.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat.

<img src="../../drivers/idec.files/image010.gif" width="595" />

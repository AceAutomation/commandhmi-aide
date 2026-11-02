# Apparaat Invt

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Met dit stuurprogramma lezen en schrijven HMI's van de HM-serie gegevens of statussen van de <span id="OLE_LINK121"></span>Registers van PLC's uit de serie Invt. De seriële verbinding loopt tussen de seriële poort van de HMI en die van de PLC. Lees vóór gebruik van dit stuurprogramma dit hoofdstuk en de technische documentatie van de PLC aandachtig.</p></td>
</tr>
<tr class="even">
<td><p>Verbinding maken met een PLC uit de serie Invt</p>
<p>1.  Hardwareaansluiting</p>
<p>Verbindingskabel:</p>
<p>RS232</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI HM-serie COM1/COM2</strong></p></td>
<td colspan="2"><p>Invt</p></td>
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
<td><p>3</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/invt.files/image005.gif" width="145" /><img src="../../drivers/invt.files/image006.gif" width="281" /><img src="../../drivers/invt.files/image007.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

De aansluiting van de HMI is DB9F, die van de Invt-serie MD8M.

**2. Software-instellingen**

Kies Invt Network Power bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Invt-serie.

Standaardverbindingsparameters van het touchscreen

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC type**                | IVC1,IVC1L,IVCIS,IVC2L,IVC3 | IVC1,IVC1L,IVCIS,IVC2L,IVC3                  |
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

**3. (IVC1,IVC1L,IVCIS,IVC2L,IVC3,IVC3 TCP) Bruikbare registers en adresbereik**

|                   |                    |                 |                                             |
|-------------------|--------------------|-----------------|---------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                 |
| X                 | ooo                | 0~377           | Bit: Ingang, alleen lezen      |
| Y                 | ooo                | 0~377           | Bit: Uitgang                |
| M                 | dddd               | 0~7999          | Bit: Intern relais (merker)                         |
| SM                | ddd                | 0~255           | Bit: Speciaal intern relais                 |
| S                 | ddd                | 0~999           | Bit: Staprelais                         |
| T                 | ddd                | 0~255           | Bit: Timerstatus                           |
| C                 | ddd                | 0~255           | Bit: Tellerstatus                         |
| D                 | dddd               | 0~7999          | Woord: Tijdelijk datageheugen                |
| SD                | ddd                | 0~255           | Woord: Speciaal tijdelijk datageheugen        |
| TV                | ddd                | 0~255           | Woord: Actuele waarde van de timer                |
| CV                | ddd                | 0~255           | Woord: Actuele waarde van de teller              |
| Z                 | dd                 | 0~15            | Woord: Register voor geïndexeerde adressering           |
| D_Double          | dddd               | 0~7999          | Dubbelwoord: Tijdelijk datageheugen         |
| CV_Double         | ddd                | 0~255           | Dubbelwoord: Actuele waarde van de teller       |
| SD_Double         | ddd                | 0~255           | Dubbelwoord: Speciaal tijdelijk datageheugen |
| R                 | ddd                | 0~32767         | Woord: 16-bits register                       |
| RD                | ddd                | 32766           | Dubbelwoord: 32-bits R-register              |
|                   |                    |                 |                                             |
| D_Bit             | dddd.dd            | 0.0~7999.15     | Bit:D-bitregister                        |
| SD_Bit            | ddd.dd             | 0.0~255.15      | Bit:SD-bitregister                       |
| Z_Bit             | dd.dd              | 0.0~15.15       | Bit:Z-bitregister                        |
| R_Bit             | dddd.dd            | 0.0~32767.15    | Bit:R-bitregister                        |

AX70 RTU/AX70 TCP

|                   |                    |                 |                                                            |
|-------------------|--------------------|-----------------|------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                                |
| **IX**            | ddd.o              | 0.0~511.7       | Bit：Bitweergave van het I-gebied (alleen lezen)                 |
| **QX**            | ddd.o              | 0.0~511.7       | Bit：Bitweergave van het Q-gebied                             |
| **MX**            | ddd.o              | 0.0~7566.7      | Bit：Bitweergave van het M-gebied                             |
| **IB**            | ddd                | 0~511           | Byte：Byteweergave van het I-gebied (alleen lezen)              |
| **QB**            | ddd                | 0~511           | Byte：Byteweergave van het Q-gebied                          |
| **MB**            | dddd               | 0~7566          | Byte：Byteweergave van het M-gebied                          |
| **IW**            | ddd                | 0~511           | Woord：Woordweergave van het I-gebied (alleen lezen)              |
| **QW**            | ddd                | 0~511           | Woord：Woordweergave van het Q-gebied                           |
| **MW**            | dddd               | 0~3783          | Woord：Woordweergave van het M-gebied                           |
| **ID**            | ddd                | 0~127           | Dubbelwoord：Dubbelwoordweergave van het I-gebied (alleen lezen) |
| **QD**            | ddd                | 0~127           | Dubbelwoord：Dubbelwoordweergave van het Q-gebied             |
| **MD**            | dddd               | 0~1891          | Dubbelwoord：Dubbelwoordweergave van het M-gebied             |

<img src="../../drivers/invt.files/image004.gif" width="600" />

Opmerking:

d: decimaal, invoerbereik 0-9;

o: octaal, invoerbereik 0-7;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Dubbelwoord in de opmerkingen: het gegevenstype van het register moet in de configuratie 32 bits zijn;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat.

<img src="../../drivers/invt.files/image004.gif" width="600" />

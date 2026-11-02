# Stuurprogramma Keyence

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Met dit stuurprogramma lezen en schrijven HMI's van de HM-serie gegevens of statussen van registers van PLC's uit de serie Keyence KV/VisualKV. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik van dit stuurprogramma dit hoofdstuk en de technische documentatie van de PLC aandachtig.</p></td>
</tr>
<tr class="even">
<td><p>Verbinding maken met een PLC uit de serie Keyence KV/VisualKV</p>
<p><strong>1. Hardwareaansluiting</strong></p>
<p>Verbindingskabel:</p>
<p>RS232 (seriële poort, protocol RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI HM-serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Serie Keyence KV/VisualKV</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>2</p></td>
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
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/keyence.files/image002.gif" width="130" /><img src="../../drivers/keyence.files/image003.gif" width="90" /><img src="../../drivers/keyence.files/image004.gif" width="278" />

De aansluiting van de HMI is DB9F, die van de Keyence KV/VisualKV-serie een 6-polige modulaire aansluiting.

**2. Software-instellingen**

Kies Keyence Corporation bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Keyence KV/VisualKV-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | KV-1000/700 KV-L20(R)       | KV-1000/700 KV-L20(R)/ KV-/40 KV-P16         |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 8                           | 7/8                                          |
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

l  KV-1000/700 KV-L20(R)

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                    |
| **R**             | dddDD              | 0~99915         | Bit: In-/uitgangsrelais        |
| **MR**            | dddDD              | 0~3915          | Bit: Interne hulpmerker  |
| **LR**            | dddDD              | 0~3999          | Bit: Vergrendelrelais            |
| **CR**            | ddDD               | 0~3999          | Bit: Besturingsrelais             |
| **T**             | dddd               | 0~65534         | Bit: Timer                     |
| **C**             | dddd               | 0~65534         | Bit: Teller                   |
| **DM**            | ddddd              | 0~32766         | Woord: Datageheugen             |
| **EM**            | ddddd              | 0~511           | Woord: Uitgebreid datageheugen    |
| **FM**            | ddddd              | 0~11998         | Woord: Bestandsregister            |
| **TM**            | ddd                | 0~3999          | Woord: Tijdelijk datageheugen   |
| **CM**            | ddddd              | 0~3999          | Woord: Besturingsgeheugen          |
| **TV**            | dddd               | 0~99915         | Woord: Actuele waarde van de timer   |
| **CV**            | dddd               | 0~3915          | Woord: Actuele waarde van de teller |

l  KV-10/16/24/40 KV-P16

|                   |                    |                 |                                           |
|-------------------|--------------------|-----------------|-------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                               |
| RLY               | dddDD              | 0~99915         | Bit: Relais                                |
| T                 | dddd               | 0~999           | Bit: Timer                                |
| C                 | dddd               | 0~999           | Bit: Teller                              |
| DM                | ddddd              | 0~9999          | Woord: Datageheugen                        |
| TM                | ddd                | 0~99            | Woord: Tijdelijk datageheugen              |
| TV_c              | dddd               | 0~999           | Woord: Actuele waarde van de timer              |
| TV_p              | dddd               | 0~999           | Woord: Voorinstelwaarde van de timer               |
| CV_c              | dddd               | 0~999           | Woord: Actuele waarde van de teller            |
| CV_p              | dddd               | 0~999           | Woord: Voorinstelwaarde van de teller             |
| CTH               | dddd               | 0~9             | Woord: Actuele waarde van de snelle teller |

l  KV-Nano

|                   |                    |                 |                                      |
|-------------------|--------------------|-----------------|--------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                          |
| **R**             | ddddd              | 0~59915         | Bit: Relais                      |
| **B**             | DDDD               | 0~1FFF          | Linkrelais                           |
| **MR**            | ddddd              | 0~59915         | Interne hulpmerker             |
| **LR**            | ddddd              | 0~19915         | Vergrendelrelais                       |
| **CR**            | dddd               | 0~8915          | Besturingsrelais                        |
| **VB**            | DDDD               | 0~1FFF          | Werkrelais                        |
| **T**             | ddd                | 0~511           | Bit: timer                            |
| **C**             | ddd                | 0~255           | Bit: Teller                         |
| **DM**            | dddd               | 0~32767         | Datageheugen                          |
| **W**             | DDDD               | 0~3FFF          | Linkregister                        |
| **TM**            | dddd               | 0~511           | Tijdelijk datageheugen               |
| **Z**             | dddd               | 1~12            | Indexregister                       |
| **TC**            | dddd               | 0~511           | Dubbelwoord: Timer (actuele waarde)   |
| **TS**            | dddd               | 0~511           | Dubbelwoord: Timer (instelwaarde)       |
| **CC**            | ddd                | 0~255           | Dubbelwoord: Teller (actuele waarde) |
| **CS**            | ddd                | 0~255           | Dubbelwoord: Teller (instelwaarde)     |
| **CTH**           | d                  | 0~3             | Snelle teller                   |
| **CTC**           | d                  | 0~7             | Dubbelwoord: Snelle comparator   |
| **CM**            | dddd               | 0~8999          | Besturingsgeheugen                       |
| **VM**            | dddd               | 0~9999          | Werkgeheugen                       |

<img src="../../drivers/keyence.files/image005.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

DD: 16 bits, invoerbereik 0-15;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat.

<img src="../../drivers/keyence.files/image005.gif" width="595" />

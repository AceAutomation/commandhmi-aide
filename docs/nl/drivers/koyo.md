# Stuurprogramma Koyo

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Met dit stuurprogramma lezen en schrijven HMI's van de HM-serie gegevens of statussen van registers van PLC's uit de serie Koyo SN. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik van dit stuurprogramma dit hoofdstuk en de technische documentatie van de PLC aandachtig.</p></td>
</tr>
<tr class="even">
<td><p> Verbinding maken met een PLC uit de serie Koyo SN</p>
<p><strong>1.</strong> <strong>Hardwareaansluiting</strong></p>
<p>Verbindingskabel:</p>
<p>RS232 (seriële poort, protocol RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HM-HMI COM1/COM2</p></td>
<td colspan="2"><p>Serie Koyo SN</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>4</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>3</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/koyo.files/image006.gif" width="278" /><img src="../../drivers/koyo.files/image007.gif" width="130" /><img src="../../drivers/koyo.files/image008.gif" width="90" />

De aansluiting van de HMI is DB9F, die van de Koyo SN-serie een 6-polige modulaire aansluiting.

**2. Software-instellingen**

Kies Koyo Electronics bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Koyo SN-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Serie Koyo SN              | Serie Koyo SN                               |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 8                           | 7/8                                          |
| **Pariteit**              | ODD                         | EVEN/ODD/NONE                                |
| **Stopbits**         | 1                           | 1/2                                          |
| **Stationsnummer PLC**      | 1                           | 0~255                                        |
| **Stationsnummer HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Functie** | **Ondersteund** |
| **Offlinesimulatie** | Ja                         |
| **Onlinesimulatie**  | Ja                         |
| **Uitgebreide modus**       | Ja                         |

**3. Koyo SN-serie**

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                    |
| **I**             | ooo                | 0~377           | Bit: Ingangsrelais, alleen lezen    |
| **O**             | ooo                | 0~377           | Bit: Uitgangsrelais              |
| **M**             | oooo               | 0~1177          | Bit: Hulprelais (merker)           |
| **SP**            | ooo                | 0~777           | Bit: Speciaal hulprelais   |
| **S**             | ooo                | 0~177           | Bit: Staprelais            |
| **T**             | ooo                | 0~177           | Bit: Timer                     |
| **C**             | ooo                | 0~177           | Bit: Teller                   |
| **R**             | ooooo              | 0~13777         | Woord: Dataregister            |
| **TR**            | ooooo              | 0~13777         | Woord: Actuele waarde van de timer   |
| **CR**            | ooooo              | 0~13777         | Woord: Actuele waarde van de teller |
| **SR**            | ooooo              | 0~13777         | Woord: Speciaal dataregister    |

**4. Koyo DIRECT-serie**

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                    |
| **X**             | ooo                | 0~3777          | Bit: Ingangsrelais, alleen lezen    |
| **Y**             | ooo                | 0~3777          | Bit: Uitgangsrelais              |
| **GX**            | oooo               | 0~7777          | Bit: Ingangsrelais, alleen lezen    |
| **GY**            | oooo               | 0~7777          | Bit: Uitgangsrelais              |
| **C**             | oooo               | 0~7777          | Bit: Teller                   |
| **S**             | oooo               | 0~1777          | Bit: Staprelais            |
| **SP**            | oooo               | 0~1777          | Bit: Speciaal hulprelais   |
| **CT**            | ooo                | 0~777           | Bit: Teller                   |
| **T**             | ooo                | 0~777           | Bit: Timer                     |
| **V**             | oooo               | 0~77777         | Woord: Speciaal dataregister    |
| **TV**            | ooo                | 0~777           | Woord: Actuele waarde van de timer   |
| **CV**            | ooo                | 0~777           | Woord: Actuele waarde van de teller |

KV-Nano

|                |              |              |                                            |
|----------------|--------------|--------------|--------------------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                                   |
| **R**          | ddddd        | 0~59915      | Bit: Relais                            |
| **B**          | DDDD         | 0~1FFF       | Bit: Linkrelais                       |
| **MR**         | ddddd        | 0~59915      | Bit：Interne hulpmerker         |
| **LR**         | ddddd        | 0~19915      | Bit: Vergrendelrelais                   |
| **CR**         | dddd         | 0~8915       | Bit: Besturingsrelais                    |
| **VB**         | DDDD         | 0~1FFF       | Bit: Werkrelais                       |
| **T**          | ddd          | 0~511        | Bit: Timer                            |
| **C**          | ddd          | 0~255        | Bit: Teller                          |
| **DM**         | dddd         | 0~32767      | Woord：Datageheugen                         |
| **W**          | DDDD         | 0~3FFF       | Woord：Linkregister                        |
| **TM**         | dddd         | 0~511        | Woord：Tijdelijk datageheugen               |
| **Z**          | dddd         | 1~12         | Woord：Indexregister                       |
| **TC**         | dddd         | 0~511        | Dubbelwoord：Timer (actuele waarde)         |
| **TS**         | dddd         | 0~511        | Dubbelwoord：Timer (instelwaarde)         |
| **CC**         | ddd          | 0~255        | Dubbelwoord：Teller (actuele waarde)       |
| **CS**         | ddd          | 0~255        | Dubbelwoord：Teller (instelwaarde)       |
| **CTH**        | d            | 0~3          | Dubbelwoord：Snelle teller            |
| **CTC**        | d            | 0~7          | Dubbelwoord：Comparator van de snelle teller |
| **CM**         | dddd         | 0~8999       | Woord：Besturingsgeheugen                      |
| **VM**         | dddd         | 0~9999       | Woord：Werkgeheugen                       |

<img src="../../drivers/koyo.files/image009.gif" width="595" />

Opmerking:

o: octaal, invoerbereik 0-7;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Dubbelwoord in de opmerkingen: het gegevenstype van het register moet in de configuratie 32 bits zijn;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/koyo.files/image010.gif" width="595" />

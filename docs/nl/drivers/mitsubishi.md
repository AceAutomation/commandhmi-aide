# Stuurprogramma Mitsubishi

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Met dit stuurprogramma lezen en schrijven HMI's van de HM-serie gegevens of statussen van registers van PLC's uit de serie Melsec FXxn/Q00J/C24N. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik van dit stuurprogramma dit hoofdstuk en de technische documentatie van de PLC aandachtig.</p></td>
</tr>
<tr class="even">
<td><p>Verbinding maken met een PLC uit de serie Melsec FXxn/Q00J/Q00U/C24N</p>
<p><strong>1.  Hardwareaansluiting</strong></p>
<p>Verbindingskabel:</p>
<p>RS422- Melsec-FXxn/FX3U/3G<span id="OLE_LINK1"></span><span id="OLE_LINK3"></span><span id="OLE_LINK2"></span> <span id="OLE_LINK24"></span><span id="OLE_LINK26"></span><span id="OLE_LINK25"></span>(seriële poort, protocol RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK30"></span><span id="OLE_LINK27"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span><strong>HMI HM-serie COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Melsec-FXxn</strong></p></td>
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

<img src="../../drivers/mitsubishi.files/image002.gif" width="145" /><img src="../../drivers/mitsubishi.files/image003.gif" width="280" /><img src="../../drivers/mitsubishi.files/image004.gif" width="130" />

De aansluiting van het touchscreen is DB9F, die van de Melsec FXxn-serie MD8M.

**RS232 - Melsec-Q00J/Q00U**

|                                                                                       |     |              |     |
|---------------------------------------------------------------------------------------|-----|--------------|-----|
| **HMI HM-serie COM1/COM2** |     | **Q00J CPU** |     |
| **2**                                                                                 | RX  | 2            | TX  |
| **3**                                                                                 | TX  | 1            | RX  |
| **5**                                                                                 | GND | 3            | GND |

<img src="../../drivers/mitsubishi.files/image005.gif" width="146" /><img src="../../drivers/mitsubishi.files/image006.gif" width="280" /><img src="../../drivers/mitsubishi.files/image007.gif" width="130" />

De aansluiting van het touchscreen is DB9F, die van de Melsec FXxn-serie MD8M.

Opmerking: aansluitinstructies Q00U

Q00U: pinnen 5 en 6 van de 6-polige aansluiting kortsluiten

MITSUBISHI-programmeersoftware: parameters -&gt; PLC-parameters -&gt; instellingen seriële communicatie

Vink het gebruik van de seriële communicatie aan, kies baudrate 115200, vink de controle aan en vink “Schrijven tijdens RUN” aan

Met de MITSUBISHI-communicatiekabel, direct aangesloten op de HMI

**RS232 - Melsec-QC24N-module**

|                             |     |              |     |
|-----------------------------|-----|--------------|-----|
| **HMI HM-serie COM1/COM2** |     | **Q00J CPU** |     |
| **2**                       | RX  | 3            | TX  |
| **3**                       | TX  | 2            | RX  |
| **5**                       | GND | 5            | GND |

<img src="../../drivers/mitsubishi.files/image008.gif" width="130" /><img src="../../drivers/mitsubishi.files/image009.gif" width="290" /><img src="../../drivers/mitsubishi.files/image010.gif" width="130" />

De aansluiting van het touchscreen is DB9F, die van de Melsec QC24N-module MB9M.

**2. Software-instellingen**

Kies MITSUBISHI bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Melsec FXxn/Q00J/C24N-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Melsec-FX2N                 | Melsec-FX/ FX2N/ FX3U/3G /Q_C24N Q00J        |
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

Melsec-FXxn/FX3U/3G/ FX3U-Ethernet

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                  |
| **X**             | oooo               | 0~377           | Bit: Ingangsspoel, alleen lezen                   |
| **Y**             | oooo               | 0~377           | Bit: Uitgangsspoel                             |
| **M**             | dddd               | 0~7999          | Bit: Tussenrelais (merker)                      |
| **SM**            | dddd               | 8000~8999       | Bit: Speciaal tussenrelais              |
| **S**             | dddd               | 0~999           | Bit: Statusbit                              |
| **T**             | dddd               | 0~256           | Bit: Timerstatus                         |
| **C**             | dddd               | 0~256           | Bit: Timerstatus                         |
| **D_Bit**         | dddd.dd            | 0.00~7999.15    | Bit: Bit van een 16-bits register                  |
| **D**             | dddd               | 0~7999          | Woord: Register                               |
| **SD**            | dddd               | 8000~8999       | Woord: Speciaal register                       |
| **TV**            | dddd               | 0~255           | Woord: Actuele waarde van de timer                 |
| **CV**            | dddd               | 0~199           | Woord: Actuele waarde van de teller               |
| **CV32**          | dddd               | 200~255         | Dubbelwoord: Actuele waarde van de 32-bits teller |

FX5U/FX5U-Ethernet

|                   |                    |                               |                                         |
|-------------------|--------------------|-------------------------------|-----------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik**               | **Opmerkingen**                             |
| **X**             | oooo               | 0~1777                        | Bit: Ingangsspoel, alleen lezen              |
| **Y**             | oooo               | 0~1777                        | Bit: Uitgangsspoel                        |
| **M**             | dddd               | 0~7679                        | Bit: Intern relais (merker)                     |
| **L**             | dddd               | 0~7679                        | Bit: Vergrendelrelais                     |
| **F**             | ddd                | 0~127                         | Bit: Alarmrelais                        |
| **TS**            | ddd                | 0~511                         | Bit: Timercontact                      |
| **CS**            | ddd                | 0~255                         | Bit: Tellercontact                    |
| **S**             | dddd               | 0~4095                        | Bit: Staprelais                     |
| **SM**            | dddd               | 0~9999                        | Bit: Speciaal relais                      |
| **B**             | hh                 | 0-ff (hexadecimaal)  | Bit: Bit: linkrelais                     |
| **D_Bit**         | dddd.dd            | 0.0~7999.15                   | Bit: Bit van een 16-bits register             |
| **D**             | dddd               | 0~7999                        | Woord: Register                          |
| **R**             | ddddd              | 0~32767                       | Woord: Cumulatieve actuele waarde van de timer |
| **W**             | hhh                | 0-1ff (hexadecimaal) | Woord: Linkregister                     |
| **CN**            | ddd                | 0~255                         | Woord: Actuele waarde van het register         |
| **TN**            | ddd                | 0~511                         | Woord: Actuele waarde van de timer            |
| **SD**            | ddddd              | 0~11999                       | Woord: Speciaal register                  |

  Melsec-Q00J/QC24N

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                    |
| **X**             | hhh                | 0~7ff           | Bit: Ingangsrelais, alleen lezen    |
| **Y**             | hhh                | 0~7ff           | Bit: Uitgangsrelais              |
| **M**             | dddd               | 0~8191          | Bit: Intern relais (merker)            |
| **L**             | dddd               | 0~2047          | Bit: Vergrendelrelais            |
| **F**             | dddd               | 0~2047          | Bit: Alarm                     |
| **V**             | dddd               | 0~2047          | Bit: Indexrelais            |
| **S**             | dddd               | 0~2047          | Bit: Staprelais            |
| **B**             | hhh                | 0~7ff           | Bit: Conversierelais          |
| **SB**            | hhh                | 0~3ff           | Bit: Speciaal linkrelais        |
| **T**             | ddd                | 0~511           | Bit: Timerstatus           |
| **C**             | ddd                | 0~511           | Bit: Tellerstatus         |
| **D**             | ddddd              | 0~11135         | Woord: Dataregister            |
| **W**             | hhh                | 0~7ff           | Woord: Conversieregister      |
| **SW**            | hhh                | 0~3ff           | Woord: Speciaal linkregister    |
| Z                 | d                  | 0~9             | Woord: Indexregister           |
| TV                | ddd                | 0~511           | Woord: Actuele waarde van de timer   |
| CV                | ddd                | 0~511           | Woord: Actuele waarde van de teller |

Q00U

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                    |
| **X**             | hhhh               | 0~1fff          | Bit: Ingangsrelais, alleen lezen    |
| **Y**             | hhhh               | 0~1fff          | Bit: Uitgangsrelais              |
| **M**             | dddd               | 0~8191          | Bit: Intern relais (merker)            |
| **L**             | dddd               | 0~8191          | Bit: Vergrendelrelais            |
| **F**             | dddd               | 0~2047          | Bit: Alarmrelais               |
| **V**             | dddd               | 0~2047          | Bit: Indexrelais            |
| **B**             | ffff               | 0~1fff          | Bit: Conversierelais          |
| **T**             | ddd                | 0~2047          | Bit: Timerstatus           |
| **C**             | dddd               | 0~1023          | Bit: Tellerstatus         |
| **SB**            | hhh                | 0~7ff           | Bit: Speciaal linkrelais        |
| **SM**            | ddd                | 0~2047          | Bit: Speciaal relais             |
| **D_Bit**         | Dddd.h             | 0.0~12287.f     | Bit: Bit van een 16-bits register    |
| **D**             | Dddd               | 0~12287         | Woord: Dataregister            |
| **W**             | Hhhh               | 0~1fff          | Woord: Conversieregister      |
| **TV**            | Dddd               | 0~2047          | Woord: Actuele waarde van de timer   |
| **CV**            | Dddd               | 0~1023          | Woord: Actuele waarde van de teller |
| **SW**            | Hhh                | 0~7ff           | Woord: Speciaal linkregister    |
| **SD**            | Dddd               | 0~2047          | Woord: Speciaal register         |
| **Z**             | Dd                 | 0~19            | Woord: Indexregister           |

Melsec-E71

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                    |
| **X**             | hhhh               | 0~1fff          | Bit: Ingangsrelais, alleen lezen    |
| **Y**             | hhhh               | 0~1fff          | Bit: Uitgangsrelais              |
| **M**             | dddd               | 0~8191          | Bit: Intern relais (merker)            |
| **L**             | dddd               | 0~8191          | Bit: Vergrendelrelais            |
| **F**             | dddd               | 0~2047          | Bit: Alarmrelais               |
| **V**             | dddd               | 0~2047          | Bit: Indexrelais            |
| **S**             | dddd               | 0~8191          | Bit: Staprelais            |
| **B**             | ffff               | 0~1fff          | Bit: Conversierelais          |
| **T**             | ddd                | 0~2047          | Bit: Timerstatus           |
| **C**             | dddd               | 0~1023          | Bit: Tellerstatus         |
| **SB**            | hhh                | 0~7ff           | Bit: Speciaal linkrelais        |
| **SM**            | ddd                | 0~2047          | Bit: Speciaal relais             |
| **D_Bit**         | Dddd.h             | 0.0~12287.f     | Bit: Bit van een 16-bits register    |
| **D**             | Dddd               | 0~12287         | Woord: Dataregister            |
| **W**             | Hhhh               | 0~1fff          | Woord: Conversieregister      |
| **TV**            | Dddd               | 0~2047          | Woord: Actuele waarde van de timer   |
| **CV**            | Dddd               | 0~1023          | Woord: Actuele waarde van de teller |
| **SW**            | Hhh                | 0~7ff           | Woord: Speciaal linkregister    |
| **SD**            | Dddd               | 0~2047          | Woord: Speciaal register         |
| **Z**             | Dd                 | 0~19            | Woord: Indexregister           |

Melsec-LCPU

|                |              |              |                                |
|----------------|--------------|--------------|--------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                       |
| **X**          | hhhh         | 0~1fff       | Bit: Ingangsrelais, alleen lezen    |
| **Y**          | hhhh         | 0~1fff       | Bit: Uitgangsrelais              |
| **M**          | dddd         | 0~8191       | Bit: Intern relais (merker)            |
| **L**          | dddd         | 0~8191       | Bit: Vergrendelrelais            |
| **F**          | dddd         | 0~2047       | Bit: Alarmrelais               |
| **V**          | dddd         | 0~2047       | Bit: Indexrelais            |
| **S**          | dddd         | 0~8191       | Bit: Staprelais            |
| **B**          | hhhh         | 0~1fff       | Bit: Conversierelais          |
| **SB**         | hhh          | 0~7ff        | Bit: Speciaal linkrelais        |
| **T**          | dddd         | 0~2047       | Bit: Timerstatus           |
| **C**          | dddd         | 0~1023       | Bit: Tellerstatus         |
| **D-bit**      | ddddd.dd     | 0~45055.15   | Bit: Bit van een 16-bits register    |
| **D**          | ddddd        | 0~45055      | Woord: Dataregister            |
| **TV**         | dddd         | 0~2047       | Woord: Actuele waarde van de timer   |
| **CV**         | dddd         | 0~1023       | Woord: Actuele waarde van de teller |
| **W**          | hhhh         | 0~1fff       | Woord: Conversieregister      |
| **SW**         | hhh          | 0~7ff        | Woord: Speciaal linkregister    |
| **SD**         | hhhh         | 0~2047       | Woord: Speciaal register         |
| **Z**          | hh           | 0~19         | Woord: Indexregister           |

<img src="../../drivers/mitsubishi.files/image011.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

o: octaal, invoerbereik 0-7;

h: hexadecimaal, invoerbereik 0-9, a-f;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Dubbelwoord in de opmerkingen: het gegevenstype van het register moet in de configuratie 32 bits zijn;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/mitsubishi.files/image011.gif" width="595" />

**4. Verbinding tussen de HMI HM-serie en de FX5U-PLC van Mitsubishi**

Open GX Works3 - Nieuw bestand - Serie FX5CPU - Type FX5U

<img src="../../drivers/mitsubishi.files/image012.gif" width="384" />

Navigatie - Parameter - Moduleparameter - Ethernet

<img src="../../drivers/mitsubishi.files/image013.gif" width="1092" />

Objectkoppeling - Specifieke instelling

<img src="../../drivers/mitsubishi.files/image014.gif" width="1024" />

Software CommandHMI: Algemeen

<img src="../../drivers/mitsubishi.files/image015.gif" width="532" />

Koppeling - Parameter

<img src="../../drivers/mitsubishi.files/image016.gif" width="532" />

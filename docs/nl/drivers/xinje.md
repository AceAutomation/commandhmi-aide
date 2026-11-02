# Stuurprogramma Xinje

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Met dit stuurprogramma lezen en schrijven HMI's van de HM-serie gegevens of statussen van registers van PLC's uit de serie Thinget XC/XCM/XD. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik van dit stuurprogramma dit hoofdstuk en de technische documentatie van de PLC aandachtig.</p></td>
</tr>
<tr class="even">
<td><p>Verbinding maken met een PLC uit de serie Thinget XC/XCM/XD</p>
<p><strong>1.  Hardwareaansluiting</strong></p>
<p>Verbindingskabel:</p>
<p>RS232 <span id="OLE_LINK3"></span><span id="OLE_LINK2"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>Touchscreen COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Serie Thinget XC/XCM/XD</strong></p></td>
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
<p><img src="../../drivers/xinje.files/image006.gif" width="130" /><img src="../../drivers/xinje.files/image007.gif" width="280" /><img src="../../drivers/xinje.files/image008.gif" width="146" /></p></td>
</tr>
</tbody>
</table>

De aansluiting van de HMI is DB9F, die van de Thinget XC/XCM/XD-serie MD8M.

**2. Software-instellingen**

Kies Xinje Electronic bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Thinget XC/XCM/XD-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Serie Thinget XC           | Serie Thinget XC/XCM/XD                     |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
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
| **Uitgebreide modus**       | Ja                         |

**3. Bruikbare registers en adresbereik**

Thinget XC/XCM-serie

|                   |                    |                 |                                    |
|-------------------|--------------------|-----------------|------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                        |
| **X**             | dddd               | 0 tot 1037       | Bit: Ingangsspoel                    |
| **Y**             | dddd               | 0 tot 1037       | Bit: Uitgangsspoel                   |
| **M**             | dddd               | 0 tot 8767       | Bit: Interne spoel                 |
| **S**             | dddd               | 0 tot 1023       | Bit: Processtap                       |
| **T**             | ddd                | 0 tot 639        | Bit: Timerstatus                   |
| **C**             | ddd                | 0 tot 639        | Bit: Tellerstatus                 |
| **D**             | dddd               | 0 tot 9023       | Woord: Dataregister                |
| **TD**            | ddd                | 0 tot 639        | Woord: Actuele waarde van de timer   |
| **CD**            | ddd                | 0 tot 639        | Woord: Actuele waarde van de teller |
| **FD**            | dddd               | 0 tot 9023       | Woord: FlashROM-register            |
| **ED**            | ddddd              | 0 tot 16383      | Woord: Uitgebreid intern register   |

Thinget XD2-serie

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
<td><p><strong>X</strong></p></td>
<td><p>o</p></td>
<td><p>0~7</p></td>
<td><p>Ingangsspoel</p></td>
</tr>
<tr class="odd">
<td><p><strong>Y</strong></p></td>
<td><p>o</p></td>
<td><p>0~7</p></td>
<td><p>Uitgangsspoel</p></td>
</tr>
<tr class="even">
<td><p><strong>M</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~7999</p></td>
<td><p>Intern relais (merker)</p></td>
</tr>
<tr class="odd">
<td><p><strong>HM</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~959</p></td>
<td><p>Intern relais (merker)</p></td>
</tr>
<tr class="even">
<td><p><strong>SM</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~2047</p></td>
<td><p>Speciaal intern relais</p></td>
</tr>
<tr class="odd">
<td><p><strong>S</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Processtap</p></td>
</tr>
<tr class="even">
<td><p><strong>HS</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~127</p></td>
<td><p>Processtap</p></td>
</tr>
<tr class="odd">
<td><p><strong>T</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Timer</p></td>
</tr>
<tr class="even">
<td><p><strong>TD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Actuele waarde van de timer</p></td>
</tr>
<tr class="odd">
<td><p><strong>HT</strong></p></td>
<td><p>dd</p></td>
<td><p>0~95</p></td>
<td><p>Timer</p></td>
</tr>
<tr class="even">
<td><p><strong>ET</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Precisietimer</p></td>
</tr>
<tr class="odd">
<td><p><strong>ETD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~31</p></td>
<td><p>Uitgebreid intern register</p></td>
</tr>
<tr class="even">
<td><p><strong>C</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Teller</p></td>
</tr>
<tr class="odd">
<td><p><strong>CD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Actuele waarde van de teller</p></td>
</tr>
<tr class="even">
<td><p><strong>HC</strong></p></td>
<td><p>dd</p></td>
<td><p>0~95</p></td>
<td><p>Teller</p></td>
</tr>
<tr class="odd">
<td><p><strong> HSC</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Snelle teller</p></td>
</tr>
<tr class="even">
<td><p><strong>D</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~7999</p></td>
<td><p>Dataregister</p></td>
</tr>
<tr class="odd">
<td><p><strong>HD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~999</p></td>
<td><p>Dataregister</p></td>
</tr>
<tr class="even">
<td><p><strong>SD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~2047</p></td>
<td><p>Speciaal dataregister</p></td>
</tr>
<tr class="odd">
<td><p><strong>HSD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~499</p></td>
<td><p>Speciaal dataregister</p></td>
</tr>
<tr class="even">
<td><p><strong>FD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~4095</p></td>
<td><p>FlashROM-register</p></td>
</tr>
<tr class="odd">
<td><p><strong>SFD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1999</p></td>
<td><p>FlashROM-register</p></td>
</tr>
<tr class="even">
<td><p><strong>FS</strong></p></td>
<td><p>dd</p></td>
<td><p>0~47</p></td>
<td><p>Speciaal beveiligingsregister</p></td>
</tr>
<tr class="odd">
<td><p><strong>SEM</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Sequentieel functieblok WAIT<br />
Commandospoel</p></td>
</tr>
</tbody>
</table>

Thinget XD3-serie

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                                                                                      |
| **X**             | ooooo              | 0~20077         | Ingangsspoel (X10000~X11177 horen bij de uitbreidingsmodule) (X20000~X20277 bij de BD-uitbreidingsmodule)              |
| **Y**             | ooooo              | 0~20077         | Uitgangsspoel (Y10000~Y11177 horen bij de uitbreidingsmodule) (Y20000~Y20277 bij de BD-uitbreidingsmodule) |
| **M**             | dddd               | 0~7999          | Intern relais (merker)                                                                                                   |
| **HM**            | ddd                | 0~959           | Intern relais (merker)                                                                                                   |
| **SM**            | dddd               | 0~2047          | Speciaal intern relais                                                                                           |
| **S**             | dddd               | 0~1023          | Processtap                                                                                            |
| **HS**            | ddd                | 0~127           | Processtap                                                                                            |
| **T**             | ddd                | 0~575           | Timer                                                                                                            |
| **TD**            | ddd                | 0~575           | Actuele waarde van de timer                                                                                              |
| **HT**            | dd                 | 0~95            | Timer                                                                                                            |
| **ET**            | dd                 | 0~31            | Precisietimer                                                                                                  |
| **ETD**           | ddd                | 0~31            | Uitgebreid intern register                                                                                       |
| **C**             | ddd                | 0~575           | Teller                                                                                                          |
| **CD**            | ddd                | 0~575           | Actuele waarde van de teller                                                                                            |
| **HC**            | dd                 | 0~95            | Teller                                                                                                          |
| **HSC**          | dd                 | 0~31            | Snelle teller                                                                                               |
| **D**             | dddd               | 0~7999          | Dataregister                                                                                                    |
| **HD**            | ddd                | 0~999           | Dataregister                                                                                                    |
| **SD**            | dddd               | 0~2047          | Speciaal dataregister                                                                                            |
| **HSD**           | ddd                | 0~499           | Speciaal dataregister                                                                                            |
| **FD**            | dddd               | 0~4095          | FlashROM-register                                                                                                |
| **SFD**           | dddd               | 0~1999          | FlashROM-register                                                                                                |
| **FS**            | dd                 | 0~47            | Speciaal beveiligingsregister                                                                                        |
| **ID**            | ddddd              | 0~20099         | Basiseenheid (ID10000~ID10999 horen bij de uitbreidingsmodule) (ID20000~20099 bij de BD-uitbreidingsmodule)              |
| **QD**            | ddddd              | 0~20099         | Basiseenheid (QD10000~QD10999 horen bij de uitbreidingsmodule) (QD20000~QD20099 bij de BD-uitbreidingsmodule)            |
| **SEM**           | dd                 | 0~31            | Sequentieel functieblok WAIT, commandospoel                                                                      |

Thinget XD5/XDM-serie

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                                                                                      |
| **X**             | ooooo              | 0~20077         | Ingangsspoel (X10000~X11177 horen bij de uitbreidingsmodule) (X20000~X20277 bij de BD-uitbreidingsmodule)              |
| **Y**             | ooooo              | 0~20077         | Uitgangsspoel (Y10000~Y11177 horen bij de uitbreidingsmodule) (Y20000~Y20277 bij de BD-uitbreidingsmodule) |
| **M**             | ddddd              | 0~20479         | Intern relais (merker)                                                                                                   |
| **HM**            | ddddd              | 0~11999         | Intern relais (merker)                                                                                                   |
| **SM**            | dddd               | 0~4095          | Speciaal intern relais                                                                                           |
| **S**             | dddd               | 0~7999          | Processtap                                                                                            |
| **HS**            | ddd                | 0~999           | Processtap                                                                                            |
| **T**             | dddd               | 0~4095          | Timer                                                                                                            |
| **TD**            | ddd                | 0~575           | Actuele waarde van de timer                                                                                              |
| **HT**            | dddd               | 0~1023          | Timer                                                                                                            |
| **ET**            | dd                 | 0~39            | Precisietimer                                                                                                  |
| **ETD**           | ddd                | 0~39            | Uitgebreid intern register                                                                                       |
| **C**             | dddd               | 0~4095          | Teller                                                                                                          |
| **CD**            | ddd                | 0~4095          | Actuele waarde van de teller                                                                                            |
| **HC**            | dddd               | 0~1023          | Teller                                                                                                          |
| **HSC**          | dd                 | 0~36            | Snelle teller                                                                                               |
| **D**             | ddddd              | 0~20479         | Dataregister                                                                                                    |
| **HD**            | ddddd              | 0~6143          | Dataregister                                                                                                    |
| **SD**            | dddd               | 0~4095          | Speciaal dataregister                                                                                            |
| **HSD**           | dddd               | 0~1023          | Speciaal dataregister                                                                                            |
| **FD**            | dddd               | 0~4095          | FlashROM-register                                                                                                |
| **SFD**           | dddd               | 0~5999          | FlashROM-register                                                                                                |
| **FS**            | dd                 | 0~47            | Speciaal beveiligingsregister                                                                                        |
| **ID**            | ddddd              | 0~20099         | Basiseenheid (ID10000~ID10999 horen bij de uitbreidingsmodule) (ID20000~20099 bij de BD-uitbreidingsmodule)              |
| **QD**            | ddddd              | 0~20099         | Basiseenheid (QD10000~QD10999 horen bij de uitbreidingsmodule) (QD20000~QD20099 bij de BD-uitbreidingsmodule)            |
| **SEM**           | ddd                | 0~127           | Sequentieel functieblok WAIT, commandospoel                                                                      |

<img src="../../drivers/xinje.files/image009.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

o: octaal, invoerbereik 0-7;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/xinje.files/image011.gif" width="595" />

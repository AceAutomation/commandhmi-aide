# Stuurprogramma Omron

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Met dit stuurprogramma lezen en schrijven HMI's van de HM-serie gegevens of statussen van registers van PLC's uit de serie SYSMAC C/CPM/CS/CJ. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik van dit stuurprogramma dit hoofdstuk en de technische documentatie van de PLC aandachtig.</p></td>
</tr>
<tr class="even">
<td><p>Verbinding maken met een PLC uit de serie SYSMAC C/CPM/CS/CJ</p>
<p>1.  Hardwareaansluiting</p>
<p>Verbindingskabel:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> <span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span><span id="OLE_LINK30"></span><strong>Touchscreen COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>SYSMAC CS/CJ</strong></p></td>
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
<td><p>3</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>9</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/omron.files/image002.gif" width="130" /><img src="../../drivers/omron.files/image003.gif" width="290" /><img src="../../drivers/omron.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

De aansluiting van de HMI is DB9F, die van de SYSMAC C/CPM/CS/CJ-serie DB9M.

**2. Software-instellingen**

Kies OMRON bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de SYSMAC C/CPM/CS/CJ-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Serie SYSMAC C/CPM         | Serie SYSMAC C/CPM/CS/CJ                    |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 7                           | 7/8                                          |
| **Pariteit**              | EVEN                        | EVEN/ODD/NONE                                |
| **Stopbits**         | 2                           | 1/2                                          |
| **Stationsnummer PLC**      | 0                           | 0~255                                        |
| **Stationsnummer HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Functie** | **Ondersteund** |
| **Offlinesimulatie** | Ja                         |
| **Onlinesimulatie**  | Ja                         |
| **Uitgebreide modus**       | Nee                          |

**3. Bruikbare registers en adresbereik**

SYSMAC C/CPM-serie

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                                                                                      |
| **IR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit: In-/uitgangsrelais                                                                                          |
| **HR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit: Houdrelais                                                                                                  |
| **LR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit: Linkrelais                                                                                                  |
| **AR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit: Hulpmerker                                                                                      |
| **T**             | ddd                | 0~255           | Bit: Timerstatus                                                                                             |
| **C**             | ddd                | 0~255           | Bit: Tellerstatus                                                                                           |
| **IR**            | dddd               | 0~4095          | Woord: In-/uitgangsrelais                                                                                         |
| **HR**            | dddd               | 0~4095          | Woord: Houdrelais                                                                                                 |
| **LR**            | dddd               | 0~4095          | Woord: Linkrelais                                                                                                 |
| **AR**            | dddd               | 0~4095          | Woord: Hulpmerker                                                                                     |
| **TC**            | ddd                | 0~255           | Woord: Waarde van de timer                                                               |
| **DM**            | dddd               | 0~9999          | Woord: Gemeenschappelijk datagebied |

SYSMAC CS/CJ-serie

|                   |                    |                 |                                                                                         |
|-------------------|--------------------|-----------------|-----------------------------------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                                                             |
| **CIO_Bit**       | dddd.DD            | 0.0~3189.15     | Bit: Kern-I/O-gebied                                        |
| **W_Bit**         | dddd.DD            | 0.0~6143.15     | Bit: Werkgebied                                            |
| **H_Bit**         | dddd.DD            | 0.0~511.15      | Bit: Houdgebied                                         |
| **A_Bit**         | dddd.DD            | 0.0~959.15      | Bit: Hulpgebied, alleen lezen: 7.168 bits: A00000～A447.15 |
| **D_Bit**         | dddd.DD            | 0.0~32767.15    | Bit: Gemeenschappelijk datagebied                                     |
| **T**             | dddd               | 0~4095          | Bit: Timerstatus                                                                    |
| **C**             | dddd               | 0~4095          | Bit: Tellerstatus                                                                  |
| **CIO**           | dddd               | 0~3189          | Woord: Kern-I/O-gebied                                                                     |
| **W**             | dddd               | 0~6143          | Woord: Werkgebied                                                                         |
| **H**             | dddd               | 0~511           | Woord: Houdgebied                                                                      |
| **A**             | dddd               | 0~959           | Woord: Hulpgebied, alleen lezen: 448 woorden: A000～A447                                    |
| **D**             | dddd               | 0~32767         | Woord: Gemeenschappelijk datagebied                                                                  |
| **TV**            | dddd               | 0~4095          | Woord: Actuele waarde van de timer                                                            |
| **CV**            | dddd               | 0~4095          | Woord: Actuele waarde van de teller                                                          |

CP1L Tcp/Ip       / Fins-udp

|                   |                    |                 |                                                           |
|-------------------|--------------------|-----------------|-----------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                               |
| **CIO_Bit**       | dddd.DD            | 0.0~3189.15     | Bit: Kern-I/O-gebied                                        |
| **W_Bit**         | dddd.DD            | 0.0~6143.15     | Bit: Werkgebied                                            |
| **H_Bit**         | dddd.DD            | 0.0~511.15      | Bit: Houdgebied                                         |
| **A_Bit**         | dddd.DD            | 0.0~959.15      | Bit: Hulpgebied, alleen lezen: 7.168 bits: A00000～A447.15 |
| **D_Bit**         | dddd.DD            | 0.0~32767.15    | Bit: Gemeenschappelijk datagebied                                     |
| **T**             | dddd               | 0~4095          | Bit: Timerstatus                                      |
| **C**             | dddd               | 0~4095          | Bit: Tellerstatus                                    |
| **CIO**           | dddd               | 0~3189          | Woord: Kern-I/O-gebied                                       |
| **W**             | dddd               | 0~6143          | Woord: Werkgebied                                           |
| **H**             | dddd               | 0~511           | Woord: Houdgebied                                        |
| **A**             | dddd               | 0~959           | Woord: Hulpgebied, alleen lezen: 448 woorden: A000～A447      |
| **D**             | dddd               | 0~32767         | Woord: Gemeenschappelijk datagebied                                    |
| **TV**            | dddd               | 0~4095          | Woord: Actuele waarde van de timer                              |
| **CV**            | dddd               | 0~4095          | Woord: Actuele waarde van de teller                            |

<img src="../../drivers/omron.files/image010.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

DD: 16 bits, invoerbereik 0-15;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/omron.files/image011.gif" width="595" />

 Instellingen voor de CP1L-verbinding via TCP/IP

Ingebouwd Ethernet -&gt; IP-adres en poortnummer instellen. Opmerking:

Gebruik bij voorkeur FINS-UDP: dan kunnen meerdere touchscreens met dezelfde PLC verbinden; vóór de normale communicatie is een handshake nodig, wat enige tijd vergt

Instructies voor de FINS-UDP-verbinding:

Ingebouwd Ethernet -&gt; IP-adres en poortnummer instellen

Het knooppuntnummer in de FINS-UDP-configuratie moet overeenkomen met het knooppuntnummer in de Ethernet-instellingen van Omron

<img src="../../drivers/omron.files/image008.jpg" width="500" alt="image009.jpg" />

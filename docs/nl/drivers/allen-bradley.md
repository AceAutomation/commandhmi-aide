# Stuurprogramma Allen-Bradley

Met dit stuurprogramma leest en schrijft de HMI van de HM-serie gegevens of statussen van AIBUS-apparaten via het AIBUS-protocol. De seriële verbinding loopt tussen de seriële poort van de HMI en die van het AIBUS-apparaat. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van het AIBUS-apparaat.

**Verbinding maken met het AIBUS-apparaat**

**1. Hardwareaansluiting**

Verbindingskabel:

RS232 (seriële poort, protocol RS232)

|                             |     |                   |     |
|-----------------------------|-----|-------------------|-----|
| **HMI HM-serie COM1/COM2** |     | **AIBUS-apparaat**  |     |
| 2                           | RX  | Door gebruiker gedefinieerde pin | TX  |
| 3                           | TX  | Door gebruiker gedefinieerde pin | RX  |
| 5                           | GND | Door gebruiker gedefinieerde pin | GND |

<img src="../../drivers/allen-bradley.files/image002.gif" width="130" /><img src="../../drivers/allen-bradley.files/image003.gif" width="280" /><img src="../../drivers/allen-bradley.files/image004.gif" width="145" />

ControlLogix/CompactLogix:

|                             |     |                         |     |
|-----------------------------|-----|-------------------------|-----|
| **HMI HM-serie COM1/COM2** |     | **Allen-Bradley (AB)** |     |
| 2                           | RX  | 3                       | TX  |
| 3                           | TX  | 2                       | RX  |
| 5                           | GND | 5                       | GND |

<img src="../../drivers/allen-bradley.files/image005.gif" width="129" /><img src="../../drivers/allen-bradley.files/image006.gif" width="290" /><img src="../../drivers/allen-bradley.files/image007.gif" width="130" />

De poort van de HMI HM-serie is DB9F, die van het AB-apparaat MD8M.

**2. Software-instellingen**

ü Kies Allen-Bradley bij het aangesloten apparaat.

ü Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

ü Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

ü Zie voor de instellingen van de PLC de technische documentatie van de Allen-Bradley-PLC.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | MicroLogix DF1_CRC          | MicroLogix DF1_CRC/MicroLogix DF1_BCC        |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 8                           | 7/8                                          |
| **Pariteit**              | NONE                        | EVEN/ODD/NONE                                |
| **Stopbits**         | 1                           | 1/2                                          |
| **Stationsnummer PLC**      | 1                           | 1~31                                         |
| **Stationsnummer HMI**      | 0                           | 0~255                                        |
| **Controle**                   | CRC                         | BCC                                          |

|                         |                             |
|-------------------------|-----------------------------|
| **Functie** | **Ondersteund** |
| **Offlinesimulatie** | Ja                         |
| **Onlinesimulatie**  | Ja                         |
| **Uitgebreide modus**       | Nee                          |

**3. Bruikbare registers en adresbereik**

SLC-serie/MicroLogix:

|                   |                    |                        |                                |
|-------------------|--------------------|------------------------|--------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik**        | **Opmerkingen**                    |
| **I**             | 1:ddd/o            | 1:0/0~1:255/15         | Bit: Ingangsbeeld     |
| **O**             | 0:ddd/o            | 0:0/0~0:255/15         | Bit: Uitgangsbeeld    |
| **B**             | ddd:ddd/o          | 3:0/0~255:255/15       | Bit: Bitgeheugen (merkers)                |
| **S_Bit**         | 2:ddd/o            | 2:0/0~2:255/15         | Bit: systeemstatusbit          |
| **N_Bit**         | ddd:ddd/o          | 7:0、10:0/0~255:255/15 | Bit: bit van een gegevensregisterwoord |
| **S**             | 2:ddd              | 2:0~2:255              | Woord: systeemstatuswoord        |
| **ST**            | ddd:ddd.dd         | 0:0.0~255:255.40       | Woord: systeemstatuswoord        |
| **N**             | ddd:ddd            | 7:0、10:0~255:255      | Woord: Dataregister            |
| **F**             | ddd:ddd            | 8:0~255:255            | Woord: drijvendekommaregister |
| **T_ACC**         | ddd:ddd            | 4:0~255:255            | Woord: ACC-waarde timer          |
| **T_PRE**         | ddd:ddd            | 4:0~255:255            | Woord: PRE-waarde timer          |
| **C_ACC**         | ddd:ddd            | 5:0~255:255            | Woord: ACC-waarde teller        |
| **C_PRE**         | ddd:ddd            | 5:0~255:255            | Woord: PRE-waarde teller        |

ControlLogix/CompactLogix:

|                   |                    |                  |                                |
|-------------------|--------------------|------------------|--------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik**  | **Opmerkingen**                    |
| **B-Bit**         | ddd:ddd/dd         | 3~225:0~255/0~15 | Bit: bit van een gegevensregisterwoord |
| **N_Bit**         | ddd:ddd/dd         | 7~225:0~255/0~15 | Bit: bit van een gegevensregisterwoord |
| **N_Bit**         | ddd:ddd/o          | 7:0/0~255:255/7  | Bit: bit van een gegevensregisterwoord |
| **S**             | 2:ddd              | 2:0~2:255        | Woord: systeemstatuswoord        |
| **N**             | ddd:ddd            | 7:0~255:255      | Woord: Dataregister            |
| **F**             | ddd:ddd            | 8:0~255:255      | Woord: drijvendekommaregister |

CompactLogix_L16ER_TCP (poortnummer: 44818)

|               |                    |                 |                                        |
|---------------|--------------------|-----------------|----------------------------------------|
| Registernaam | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                            |
| **B**         | ddd.ddd            | 0.0~255.255     | Bit: adres van het type bool                 |
| **I**         | Ddd.ddd            | 0.0~255.255     | Woord: 16-bits int-register              |
| **F**         | ddd.ddd            | 0.0~255.99      | Dubbelwoord: 32-bits float-register |

MicroLogix DF1_TCP            (poortnummer: 44818)

|               |                    |                  |                                                    |
|---------------|--------------------|------------------|----------------------------------------------------|
| Registernaam | **Adresformaat** | **Invoerbereik**  | **Opmerkingen**                                        |
| **I**         | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: ingangsbeeldregister, alleen lezen             |
| **O**         | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: Uitgangsbeeld                         |
| **B**         | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: bitgeheugen                                   |
| **T**         | ddd.ddd            | 0.0~255.255      | Bit: Timerstatus                                   |
| **C**         | ddd.ddd            | 0.0~255.255      | Bit: Tellerstatus                                 |
| **S_Bit**     | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: bit van het systeemregister                |
| **N_Bit**     | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: bits van een gegevensregister                      |
| **S**         | ddd.ddd            | 0.0~255.255      | Woord: Systeemregister                              |
| **N**         | ddd.ddd            | 0.0~255.255      | Woord: 16-bits integerregister                      |
| **F**         | ddd.ddd            | 0.0~255.255      | Dubbelwoord: 32-bits drijvendekommaregister |
| **TV**        | ddd.ddd            | 0.0~255.255      | Woord: Actuele waarde van de timer                       |
| **CV**        | ddd.ddd            | 0.0~255.255      | Woord: Actuele waarde van de teller                        |
| **TS**        | ddd.ddd            | 0.0~255.255      | Woord: instelwaarde timer                          |
| **CS**        | ddd.ddd            | 0.0~255.255      | Woord: instelwaarde teller                            |

**4. Verbinding tussen de HMI HM-serie en PLC's van de series ControlLogix en CompactLogix van Allen-Bradley**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p>Open RSLinx en stel het communicatiestuurprogramma van de PLC in</p>
<p><img src="../../drivers/allen-bradley.files/image008.gif" width="349" /></p>
<p>Maak een stuurprogramma aan; kies seriële verbinding en RS-232 DF1-apparaten</p>
<p><img src="../../drivers/allen-bradley.files/image009.gif" width="425" /></p>
<p>Is er een kabel tussen pc en PLC aangesloten, dan verschijnt de PLC na de instelling in RSLinx</p>
<p><img src="../../drivers/allen-bradley.files/image010.gif" width="430" /></p>
<p>Open de PLC-programmeersoftware RSLogix 5000 en maak uw project en nieuwe tags aan</p>
<p><img src="../../drivers/allen-bradley.files/image011.gif" width="282" /></p>
<p>Maak de tags B003, N007 en F008 aan</p>
<p><img src="../../drivers/allen-bradley.files/image012.gif" width="390" /></p>
<p>Taglijst na het aanmaken:</p>
<p><img src="../../drivers/allen-bradley.files/image013.gif" width="633" /></p>
<p>Maak de <a href="javascript:;">adrestoewijzing</a> aan</p>
<p><img src="../../drivers/allen-bradley.files/image014.gif" width="428" /><strong></strong></p>
<p><img src="../../drivers/allen-bradley.files/image015.gif" width="410" /><strong></strong></p>
<p><strong>PLC-parameters instellen</strong></p>
<p><img src="../../drivers/allen-bradley.files/image016.gif" width="807" /><strong></strong></p>
<p><img src="../../drivers/allen-bradley.files/image017.gif" width="552" /><strong></strong></p>
<p>·d: decimaal, invoerbereik 0-9;</p>
<p>·o: octaal, invoerbereik 0-7;</p>
<p>·Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;</p>
<p>·Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;</p>
<p>·Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;</p>
<p>·Namen en bereiken van de registers kunnen per apparaatmodel verschillen.</p>
<p>Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat </p></td>
</tr>
</tbody>
</table>

Aansluiting van een CompactLogix-PLC uit de 1769-serie

Nieuwe adrestags in de PLC

Overeenkomst adressen en tags

Register        type tag     arraygrootte

B                          bool             255

I                           int                 255

F                          real               100

De tag moet uit 3 tekens bestaan, zoals B003, I004 en F005

<img src="../../drivers/allen-bradley.files/image018.jpg" width="314" alt="ab_guanli.jpg" />

<img src="../../drivers/allen-bradley.files/image019.jpg" width="390" alt="ab_guanli2.jpg" />

Aansluiting van een MicroLogix DF1_TCP uit de 1766-serie

Behalve voor de I/O-registers, waarvan de grootte niet kan worden ingesteld, is de arraygrootte van alle registers 256. Het eerste getal in het adresinvoerformaat is het bestandsnummer: dat van F8 is bijvoorbeeld 8, dat van I1 is 1, enz.

# Stuurprogramma HaiWell

|                                                                                                                                                                                                                                                                                                                                                                                                                                                     |     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| Met dit stuurprogramma leest en schrijft de HMI van de HM-serie gegevens of statussen van de registers van PLC's Haiwell E/S/H-serie. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van de PLC. |     |

<span id="OLE_LINK217"></span><span id="OLE_LINK218"></span><span id="OLE_LINK219"></span>Verbinding maken met HAIWELL-apparaten<span id="OLE_LINK221"></span>

<span id="OLE_LINK222"></span><span id="OLE_LINK223"></span><span id="OLE_LINK224"></span>**1. Hardwareaansluiting**

<span id="OLE_LINK225"></span><span id="OLE_LINK226"></span><span id="OLE_LINK227"></span>Verbindingskabel:

RS232 (seriële poort, protocol RS232)

|                                                                                                                       |     |                          |     |
|-----------------------------------------------------------------------------------------------------------------------|-----|--------------------------|-----|
| **HMI HM-serie COM1/COM2** |     | **Serie HaiWell E/S/H** |     |
| 2                                                                                                                     | RX  | 2                        | TX  |
| 3                                                                                                                     | TX  | 1                        | RX  |
| 5                                                                                                                     | GND | 3                        | GND |

|     |                                                      |     |                                                      |     |                                                      |
|-----|------------------------------------------------------|-----|------------------------------------------------------|-----|------------------------------------------------------|
|     |                                                      |     |                                                      |     |                                                      |
|     | <img src="../../drivers/haiwell.files/image002.gif" width="129" /> |     |                                                      |     |                                                      |
|     |                                                      |     |                                                      |     | <img src="../../drivers/haiwell.files/image003.gif" width="140" /> |
|     |                                                      |     | <img src="../../drivers/haiwell.files/image004.gif" width="280" /> |     |                                                      |
|     |                                                      |     |                                                      |     |                                                      |
|     |                                                      |     |                                                      |     |                                                      |

<span id="OLE_LINK231"></span>De aansluiting van de HMI HM-serie is DB9F, die van de Haiwell E/S/H-serie MD4M.

<span id="OLE_LINK237"></span>**2. Software-instellingen**

Kies Haiwell Technology Corp. bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Haiwell E/S/H-serie.

<span id="OLE_LINK242"></span>Standaardverbindingsparameters van het touchscreen

|                             |                             |                             |                                              |     |
|-----------------------------|-----------------------------|-----------------------------|----------------------------------------------|-----|
| **Instelling**            | **Standaardwaarde** |                             | **Instelbereik**                            |     |
| **Poorttype** | RS232                       |                             | RS232/RS422/RS485                            |     |
| **Baudrate**               | 19200                       |                             | 1200/2400/4800/9600/19200/38400/57600/115200 |     |
| **Databits**         | 8                           |                             | 7/8                                          |     |
| **Pariteit**              | NONE                        |                             | EVEN/ODD/NONE                                |     |
| **Stopbits**         | 2                           |                             | 1/2                                          |     |
| **Stationsnummer PLC**      | 1                           |                             | 1~31                                         |     |
| **Stationsnummer HMI**      | 0                           |                             | 0~255                                        |     |
| **Functie**     |                             | **Ondersteund** |                                              |     |
| **Offlinesimulatie**     |                             | Ja                         |                                              |     |
| **Onlinesimulatie**      |                             | Ja                         |                                              |     |
| **Uitgebreide modus**           |                             | Ja                         |                                              |     |
|                             |                             |                             |                                              |     |

3\. **Bruikbare registers en adresbereik**

|                   |                    |                 |                                                            |
|-------------------|--------------------|-----------------|------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                                |
| X                 | ddd                | 0~1023          | Bit: Externe digitale ingang                                 |
| Y                 | ddd                | 0~1023          | Bit: Externe digitale uitgang                                |
| M                 | ddd                | 0~12287         | Bit: Intern relais (merker)                                        |
| SM                | ddd                | 0~215           | Bit: Systeemstatus           |
| S                 | ddd                | 0~2047          | Bit: Stapstatus                                           |
| T                 | ddd                | 0~1023          | Bit: Timerstatus                                          |
| C                 | ddd                | 0~255           | Bit: Tellerstatus                                        |
| AI                | ddd                | 0~255           | Woord: Analoog ingangsregister                                |
| AQ                | ddd                | 0~255           | Woord: Analoog uitgangsregister                               |
| V                 | ddd                | 0~14847         | Woord: Intern register                                    |
| TCV               | ddd                | 0~1023          | Woord: Actuele waarde van de timer |
| CCV               | ddd                | 0~47, 80~255    | Woord: Actuele waarde van de teller                             |
| SV                | ddd                | 0~154           | Woord: Systeemregister                                      |
| CCV32             | ddd                | 0~31            | Dubbelwoord: Actuele waarde van de teller                      |

<img src="../../drivers/haiwell.files/image010.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat.

<img src="../../drivers/haiwell.files/image011.gif" width="595" />

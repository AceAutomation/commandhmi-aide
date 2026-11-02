# Stuurprogramma Fatek

Met dit stuurprogramma leest en schrijft de HMI van de HM-serie gegevens of statussen van de registers van PLC's <span id="OLE_LINK158"></span><span id="OLE_LINK159"></span>Fatek FB-serie. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van de PLC.

**Verbinding maken met Fatek-apparaten**

**1. Hardwareaansluiting**

Verbindingskabel:

RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span> (seriële poort, protocol RS232)

|                         |     |                 |     |
|-------------------------|-----|-----------------|-----|
| HMI HM-serie COM1/COM2 |     | Serie Fatek FB |     |
| 2                       | RX  | 1               | TX  |
| 3                       | TX  | 2               | RX  |
| 5                       | GND | 4               | GND |

|     |                                                    |     |                                                    |     |                                                    |
|-----|----------------------------------------------------|-----|----------------------------------------------------|-----|----------------------------------------------------|
|     |                                                    |     |                                                    |     |                                                    |
|     |                                                    |     |                                                    |     | <img src="../../drivers/fatek.files/image006.gif" width="146" /> |
|     | <img src="../../drivers/fatek.files/image007.gif" width="129" /> |     |                                                    |     |                                                    |
|     |                                                    |     | <img src="../../drivers/fatek.files/image008.gif" width="280" /> |     |                                                    |
|     |                                                    |     |                                                    |     |                                                    |
|     |                                                    |     |                                                    |     |                                                    |

De aansluiting van de HMI HM-serie is DB9F, die van de Fatek FB-serie MD4M.

**2. Software-instellingen**

Kies Fatek Automation Corp. bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Fatek FB-serie.

Standaardverbindingsparameters van het touchscreen

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Serie Fatek FB             | Serie Fatek FB                              |
| **Poorttype** | RS232                       | RS232                                        |
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

|                   |                    |                 |                                                   |
|-------------------|--------------------|-----------------|---------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                       |
| X                 | dddd               | 0~9999          | Bit: Ingang, alleen lezen            |
| Y                 | dddd               | 0~9999          | Bit: Uitgangsrelais                                 |
| M                 | dddd               | 0~9999          | Bit: Intern relais (merker)                               |
| S                 | dddd               | 0~9999          | Bit: Staprelais                               |
| T                 | dddd               | 0~9999          | Bit: Timerstatus                                 |
| C                 | dddd               | 0~9999          | Bit: Tellerstatus                               |
| R                 | dddd               | 0~9999          | Woord: Dataregister |
| D                 | dddd               | 0~9999          | Woord: Dataregister                               |
| TR                | dddd               | 0~9999          | Woord: Actuele waarde van de timer                      |
| CR                | dddd               | 0~9999          | Woord: Actuele waarde van de teller                    |
| F                 | dddd               | 0~9999          | Woord: Bestandsregister                               |
| DRC               | ddd                | 200~255         | Dubbelwoord: Actuele waarde van de 32-bits teller      |

<img src="../../drivers/fatek.files/image009.gif" width="600" />

Opmerking:

d: decimaal, invoerbereik 0-9;

o: octaal, invoerbereik 0-7;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Dubbelwoord in de opmerkingen: het gegevenstype van het register moet in de configuratie 32 bits zijn;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/fatek.files/image009.gif" width="600" />

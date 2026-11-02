# Stuurprogramma Matsushita

Met dit stuurprogramma leest en schrijft de HMI van de HM-serie gegevens of statussen van de registers van PLC's Matsushita FP-serie. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van de PLC.

Verbinding maken met PLC's van de Matsushita FP-serie

**1.  Hardwareaansluiting**

Verbindingskabel:

RS232-FP0/FP2/FP2SH/FPM

|                                                                                                                                                 |     |                          |     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----|--------------------------|-----|
| **HMI HM-serie COM1/COM2** |     | **Serie Matsushita FP** |     |
| 2                                                                                                                                               | RX  | 3                        | TX  |
| 3                                                                                                                                               | TX  | 2                        | RX  |
| 5                                                                                                                                               | GND | 1                        | GND |

<img src="../../drivers/matsushita.files/image002.gif" width="280" /><img src="../../drivers/matsushita.files/image003.gif" width="129" /><img src="../../drivers/matsushita.files/image004.gif" width="145" />

De aansluiting van de HMI is DB9F, die van de Matsushita FP-serie MD5M.

RS422-FP1

|                             |     |                      |     |
|-----------------------------|-----|----------------------|-----|
| **HMI HM-serie COM1/COM2** |     | Serie Matsushita FP |     |
| 6                           | RX- | 2                    | TX- |
| 7                           | RX+ | 5                    | TX+ |
| 8                           | TX- | 3                    | RX- |
| 9                           | TX+ | 6                    | RX+ |

<img src="../../drivers/matsushita.files/image005.gif" width="140" /><img src="../../drivers/matsushita.files/image006.gif" width="129" /><img src="../../drivers/matsushita.files/image007.gif" width="280" />

De aansluiting van de HMI is DB9F, die van de Matsushita FP-serie MD8M.

**2. Software-instellingen**

Kies MATSUSHITA bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Matsushita FP-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Serie FP                   | Serie FP                                    |
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
| **Uitgebreide modus**       | Nee                          |

**3. Bruikbare registers en adresbereik**

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                            |
| **X**             | ddddh              | 0~9999f         | Bit: Externe ingang, alleen lezen         |
| **Y**             | ddddh              | 0~9999f         | Bit: Externe uitgang                   |
| **R**             | ddddh              | 0~9999f         | Bit: Intern relais (merker)                    |
| **L**             | ddddh              | 0~9999f         | Bit: Linkrelais                        |
| **T**             | dddd               | 0~9999          | Bit: Timerstatus, alleen lezen        |
| **C**             | dddd               | 0~9999          | Bit: Tellerstatus, alleen lezen      |
| **WX**            | dddd               | 0~9999          | Woord: Externe ingang, alleen lezen        |
| **WY**            | dddd               | 0~9999          | Woord: Externe uitgang                  |
| **WR**            | dddd               | 0~9999          | Woord: Intern relais (merker)                   |
| **WL**            | dddd               | 0~9999          | Woord: Linkrelais                       |
| **DT**            | ddddd              | 0~99999         | Woord: Dataregister                    |
| **LD**            | ddddd              | 0~99999         | Woord: Linkregister                    |
| **FL**            | ddddd              | 0~99999         | Woord: Bestandsregister                    |
| **SV**            | dddd               | 0~9999          | Woord: Gebied instelwaarden timer/teller     |
| **EV**            | dddd               | 0~9999          | Woord: Gebied actuele waarden timer/teller |

<img src="../../drivers/matsushita.files/image008.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

h: hexadecimaal, invoerbereik 0-9, a-f;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/matsushita.files/image009.gif" width="595" />

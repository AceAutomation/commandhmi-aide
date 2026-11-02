# Stuurprogramma GE

Met dit stuurprogramma leest en schrijft de HMI van de HM-serie gegevens of statussen van de registers van PLC's GE Fanuc. De seriële verbinding loopt tussen de seriële poort van de HMI en die van de PLC. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van de PLC.

**1. Hardwareaansluiting**

Verbindingskabel:

RS232 (seriële poort, protocol RS232)

|                             |     |                     |     |
|-----------------------------|-----|---------------------|-----|
| **HMI HM-serie COM1/COM2** |     | **Serie GE Fanuc** |     |
| 2                           | RX  | 4                   | TX  |
| 3                           | TX  | 3                   | RX  |
| 5                           | GND | 8                   | GND |

|     |                                                 |     |                                                 |     |                                                |
|-----|-------------------------------------------------|-----|-------------------------------------------------|-----|------------------------------------------------|
|     |                                                 |     |                                                 |     |                                                |
|     |                                                 |     |                                                 |     | <img src="../../drivers/ge.files/image002.gif" width="97" /> |
|     | <img src="../../drivers/ge.files/image003.gif" width="130" /> |     |                                                 |     |                                                |
|     |                                                 |     | <img src="../../drivers/ge.files/image004.gif" width="278" /> |     |                                                |
|     |                                                 |     |                                                 |     |                                                |
|     |                                                 |     |                                                 |     |                                                |

De aansluiting van de HMI HM-serie is DB9F, die van de GE Fanuc-PLC RJ45.

**2. Software-instellingen**

Kies GE Corporation bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de GE Fanuc-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | GE Fanuc SNP-X              | GE Fanuc SNP-X/ GE Fanuc CCM                 |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 8                           | 7/8                                          |
| **Pariteit**              | ODD                         | EVEN/ODD/NONE                                |
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

|                   |                    |                 |                            |
|-------------------|--------------------|-----------------|----------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                |
| **%I**            | ddddd              | 1~10000         | Bit: Digitale ingang        |
| **%Q**            | ddddd              | 1~10000         | Bit: Digitale uitgang       |
| **%M**            | ddddd              | 1~10000         | Bit: Intern gebruik          |
| **%S**            | ddd                | 1~128           | Bit: Systeemgebruik, alleen lezen |
| **%SA**           | ddd                | 1~128           | Bit: Systeemgebruik, alleen lezen |
| **%SB**           | ddd                | 1~128           | Bit: Systeemgebruik, alleen lezen |
| **%SC**           | ddd                | 1~128           | Bit: Systeemgebruik, alleen lezen |
| **%T**            | ddd                | 1~256           | Bit: Tijdelijke status      |
| **%G**            | dddd               | 1~7680          | Bit: Genius Global        |
| **%AI**           | ddddd              | 1~10000         | Woord: Analoge ingang         |
| **%AQ**           | ddddd              | 1~10000         | Woord: Analoge uitgang        |
| **%R**            | ddddd              | 1~32640         | Woord: Registergeheugen      |

 <img src="../../drivers/ge.files/image005.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

o: octaal, invoerbereik 0-7;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat.

<img src="../../drivers/ge.files/image005.gif" width="595" />

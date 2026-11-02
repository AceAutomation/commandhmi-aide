# Stuurprogramma ZhengHang

Met dit stuurprogramma leest en schrijft de HMI van de HM-serie gegevens of statussen van de registers van PLC's ZhengHang A5-serie. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van de PLC.

Verbinding maken met PLC's van de ZhengHang A5-serie

**1. Hardwareaansluiting**

Verbindingskabel:

RS232 <span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>

|                           |     |                    |     |
|---------------------------|-----|--------------------|-----|
| **HM-HMI COM1/COM2** |     | **ZhengHang A5　** |     |
| 2                         | RX  | 2                  | TX  |
| 3                         | TX  | 3                  | RX  |
| 5                         | GND | 5                  | GND |

<img src="../../drivers/zhenghang.files/image002.gif" width="130" /><img src="../../drivers/zhenghang.files/image003.gif" width="290" /><img src="../../drivers/zhenghang.files/image004.gif" width="130" />

De aansluiting van de HMI is DB9F, die van de ZhengHang A5-serie DB9M.

**2. Software-instellingen**

Kies ZhengHang Electronics bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de ZhengHang A5-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Serie A5                   | Serie A5                                    |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 8                           | 7/8                                          |
| **Pariteit**                  | NONE                        | EVEN/ODD/NONE                                |
| **Stopbits**         | 1                           | 1/2                                          |
| **Stationsnummer PLC**      | 1                           | 0~255                                        |
| **Stationsnummer HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Functie** | **Ondersteund** |
| **Offlinesimulatie**  | Ja                         |
| **Onlinesimulatie**   | Ja                         |
| **Uitgebreide modus**       | Ja                         |

**3. Bruikbare registers en adresbereik**

|                   |                    |                 |                                                                           |
|-------------------|--------------------|-----------------|---------------------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                                               |
| **I**             | dd.o               | 0.0 tot 15.7     | Bit: Ingangsbeeld, alleen lezen                                      |
| **Q**             | dd.o               | 0.0 tot 15.7     | Bit: Uitgangsbeeld                                                |
| **M**             | dddd.o             | 0.0 tot 4095.7   | Bit: Bitgeheugen (merkers)                                                           |
| **VW**            | dddd               | 0 tot 1998       | Woord: Variabelengeheugen, 8-bits register, elk woord neemt twee adressen in |
| **AIW**           | d                  | 0 tot 9          | Woord: Analoge ingang, alleen lezen                                             |
| **AQW**           | d                  | 0 tot 9          | Woord: Analoge uitgang, alleen schrijven                                           |

<img src="../../drivers/zhenghang.files/image005.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

o: octaal, invoerbereik 0-7;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/zhenghang.files/image005.gif" width="595" />

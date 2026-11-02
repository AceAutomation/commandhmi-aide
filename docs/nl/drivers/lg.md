# Stuurprogramma LG

Met dit stuurprogramma leest en schrijft de HMI van de HM-serie gegevens of statussen van de registers van PLC's LG Master-K-serie. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van de PLC.

Verbinding maken met PLC's van de LG Master-K-serie

**1. Hardwareaansluiting**

Verbindingskabel:

RS232 met CNet-protocol<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> (seriële poort, protocol RS232)

|                                                                                                                    |     |                 |     |
|--------------------------------------------------------------------------------------------------------------------|-----|-----------------|-----|
| **HMI HM-serie COM1/COM2** |     | **LG Master-K** |     |
| 2                                                                                                                  | RX  | 7               | TX  |
| 3                                                                                                                  | TX  | 4               | RX  |
| 5                                                                                                                  | GND | 5               | GND |

<img src="../../drivers/lg.files/image002.gif" width="130" /><img src="../../drivers/lg.files/image003.gif" width="291" /><img src="../../drivers/lg.files/image004.gif" width="130" />

De aansluiting van de HMI is DB9F, die van de LG Master-K-serie DB9M.

RS232 met KLoader-protocol

|                                                                                       |     |                 |     |
|---------------------------------------------------------------------------------------|-----|-----------------|-----|
| **HMI HM-serie COM1/COM2** |     | **LG Master-K** |     |
| 2                                                                                     | RX  | 3               | TX  |
| 3                                                                                     | TX  | 2               | RX  |
| 5                                                                                     | GND | 5               | GND |

<img src="../../drivers/lg.files/image005.gif" width="291" /><img src="../../drivers/lg.files/image006.gif" width="130" /><img src="../../drivers/lg.files/image007.gif" width="130" />

De aansluiting van de HMI is DB9F, die van de LG Master-K-serie DB9M.

RS<span id="OLE_LINK51"></span><span id="OLE_LINK52"></span>485

|                                                          |     |                 |
|----------------------------------------------------------|-----|-----------------|
| **HMI HM-serie COM1/COM2** |     | **LG Master-K** |
| 8                                                        | D-  | B               |
| 9                                                        | D+  | A               |

 <img src="../../drivers/lg.files/image008.gif" width="157" /><img src="../../drivers/lg.files/image009.gif" width="130" />

De aansluiting van de HMI is DB9F, die van de LG Master-K-serie een tweedraadsklem.

RS232-K10S1

|                             |     |                 |     |
|-----------------------------|-----|-----------------|-----|
| **HMI HM-serie COM1/COM2** |     | **LG Master-K** |     |
| 2                           | RX  | 4               | TX  |
| 3                           | TX  | 1               | RX  |
| 5                           | GND | 6               | GND |

De aansluiting van de HMI is DB9F, die van de LG Master-K-serie MD6M.

|     |                                                 |     |                                                 |
|-----|-------------------------------------------------|-----|-------------------------------------------------|
|     |                                                 |     |                                                 |
|     |                                                 |     | <img src="../../drivers/lg.files/image010.gif" width="146" /> |
|     | <img src="../../drivers/lg.files/image011.gif" width="401" /> |     |                                                 |
|     |                                                 |     |                                                 |

**2. Software-instellingen**

Kies LG Industrial Systems bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de LG Master-K-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | LG Master-K Cnet            | LG Master-K Cnet/K Loader/K10s1              |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 8                           | 7/8                                          |
| **Pariteit**              | NONE                        | EVEN/ODD/NONE                                |
| **Stopbits**         | 1                           | 1/2                                          |
| **Stationsnummer PLC**      | 0                           | 0~255                                        |
| **Stationsnummer HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Functie** | **Ondersteund** |
| **Offlinesimulatie** | Ja                         |
| **Onlinesimulatie**  | Ja                         |
| **Uitgebreide modus**       | Ja                         |

**3. Bruikbare registers en adresbereik**

Bruikbaar adresbereik van PLC's van de Kxxx-serie:

|               |                |             |                                |
|---------------|----------------|-------------|--------------------------------|
| Registernaam | Adresformaat | Invoerbereik | Opmerkingen                        |
| P_Bit         | dddh           | 0~255f      | Bit: In-/uitganggebied         |
| M_Bit         | dddh           | 0~255f      | Bit: Hulprelais (merker)           |
| K_Bit         | dddh           | 0~255f      | Bit: Beschermingsrelais (remanent)          |
| L_Bit         | dddh           | 0~255f      | Bit: Linkrelais                |
| F_Bit         | dddh           | 0~255f      | Bit: Speciaal relais             |
| P             | dddh           | 0~255f      | Woord: In-/uitganggebied        |
| M             | dddh           | 0~255f      | Woord: Hulprelais (merker)          |
| K             | dddh           | 0~255f      | Woord: Beschermingsrelais (remanent)         |
| L             | dddh           | 0~255f      | Woord: Linkrelais               |
| F             | dddh           | 0~255f      | Woord: Speciaal relais            |
| T             | ddd            | 0~255       | Bit: Timerrelais               |
| C             | ddd            | 0~255       | Bit: Tellerrelais             |
| S             | dddd           | 0~9999      | Woord: Stapregister        |
| D             | dddd           | 0~9999      | Woord: Dataregister            |
| TV            | ddd            | 0~255       | Woord: Actuele waarde van de timer   |
| CV            | ddd            | 0~255       | Woord: Actuele waarde van de teller |

Bruikbaar adresbereik van PLC's van de XGB CPU-serie (via de RS232-downloadpoort van de PLC):

|                |              |              |                                   |
|----------------|--------------|--------------|-----------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                          |
| P_Bit          | ddddh        | 0-1023f      | Bit: In-/uitganggebied            |
| M_Bit          | ddddh        | 0-1023f      | Bit: Hulprelais (merker)              |
| F_Bit          | ddddh        | 0-1023f      | Bit: Speciaal relais                |
| L_Bit          | ddddh        | 0-2047f      | Bit: Linkrelais                   |
| K_Bit          | ddddh        | 0-4095f      | Bit: Beschermingsrelais (remanent)             |
| D_Bit          | ddddh        | 0-10239f     |                                   |
| T              | dddd         | 0-1023       | Bit: Timerrelais                  |
| C              | dddd         | 0-1023       | Bit: Tellerrelais                |
| TV             | dddd         | 0-1023       | Woord: Actuele waarde van de timer      |
| CV             | dddd         | 0-1023       | Woord: Actuele waarde van de teller    |
| P              | dddd         | 0-1023       | Woord: In-/uitganggebied           |
| M              | dddd         | 0-1023       | Woord: Hulprelais (merker)             |
| F              | dddd         | 0-1023       | Woord: Speciaal relais (alleen lezen) |
| L              | dddd         | 0-2047       | Woord: Linkrelais                  |
| K              | dddd         | 0-4095       | Woord: Beschermingsrelais (remanent)            |
| D              | dddd         | 0-10239      | Woord: Dataregister               |
| R              | dddd         | 0-10239      | Woord: Stapregister           |
| ZR             | dddd         | 0-10239      | Woord:                             |
| S              | ddd          | 0-127        | Woord: Stapregister           |
| Z              | ddd          | 0-127        | Woord:                             |
| U              | dd.dd        | 0.0-10.31    | Woord：(alleen lezen)               |

Bruikbaar adresbereik van PLC's van de XGB CNET-serie:

|               |                |             |                         |
|---------------|----------------|-------------|-------------------------|
| Registernaam | Adresformaat | Invoerbereik | Opmerkingen                 |
| P             | dddh           | 0~127f      | Woord: In-/uitganggebied |
| M             | dddh           | 0~255f      | Woord: Hulprelais (merker)   |
| K             | dddh           | 0~2559f     | Woord: Beschermingsrelais (remanent)  |
| L             | dddh           | 0~1279f     | Woord: Linkrelais        |
| F             | dddh           | 0~255f      | Woord: Speciaal relais     |
| T             | ddd            | 0~255       | Bit: Timerrelais        |
| C             | ddd            | 0~255       | Bit: Tellerrelais      |
| S             | ddd            | 0~127.99    | Woord: Stapregister |
| D             | dddd           | 0~5119      | Woord: Dataregister     |
| N             | dddd           | 0~3935      |                         |
| Z             | ddd            | 0~127       |                         |
| ZR            | dddd           | 0~1023      |                         |
| U             | d              | 0~7.31      |                         |

XGB TCP/IP

|                |              |              |                                   |
|----------------|--------------|--------------|-----------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                          |
| P_Bit          | ddddh        | 0-2047f      | Bit: In-/uitganggebied            |
| M_Bit          | ddddh        | 0-2047f      | Bit: Hulprelais (merker)              |
| F_Bit          | ddddh        | 0-2047f      | Bit: Speciaal relais                |
| L_Bit          | ddddh        | 0-4095f      | Bit: Linkrelais                   |
| K_Bit          | ddddh        | 0-8191f      | Bit: Beschermingsrelais (remanent)             |
| T              | dddd         | 0-2047       | Bit: Timerrelais                  |
| C              | dddd         | 0-2047       | Bit: Tellerrelais                |
| TV             | dddd         | 0-2047       | Woord: Actuele waarde van de timer      |
| CV             | dddd         | 0-2047       | Woord: Actuele waarde van de teller    |
| P              | dddd         | 0-2047       | Woord: In-/uitganggebied           |
| M              | dddd         | 0-2047       | Woord: Hulprelais (merker)             |
| F              | dddd         | 0-2047       | Woord: Speciaal relais (alleen lezen) |
| L              | dddd         | 0-4095       | Woord: Linkrelais                  |
| K              | dddd         | 0-8191       | Woord: Beschermingsrelais (remanent)            |
| D              | ddddd        | 0-19999      | Woord: Dataregister               |
| R              | ddddd        | 0-16383      |                                   |
| S              | ddd          | 0-127        | Woord: Stapregister           |
| Z              | ddd          | 0-127        |                                   |
| U              | dd.dd        | 0.0-11.31    |                                   |
| N              | ddddd        | 0-10239      | Woord：(alleen lezen)               |

<img src="../../drivers/lg.files/image012.gif" width="595" />

Opmerking:

d: decimaal, invoerbereik 0-9;

h: hexadecimaal, invoerbereik 0-9, a-f;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/lg.files/image013.gif" width="595" />

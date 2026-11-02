# Stuurprogramma Fuji

Met dit stuurprogramma leest en schrijft de HMI van de HM-serie gegevens of statussen van de registers van PLC's Fuji NB-serie. De seriële verbinding loopt tussen de seriële poort van de HMI en die van de PLC. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van de PLC.

**Verbinding maken met Fuji-apparaten**

**1. Hardwareaansluiting**

Verbindingskabel:

RS422<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span> (seriële poort, protocol RS422)

|                         |     |                |     |
|-------------------------|-----|----------------|-----|
| HMI HM-serie COM1/COM2 |     | Serie Fuji NB |     |
| 6                       | RX- | 4              | TX- |
| 7                       | RX+ | 3              | TX+ |
| 8                       | TX- | 6              | RX- |
| 9                       | TX+ | 5              | RX+ |

|     |                                                   |     |                                                   |     |                                                  |
|-----|---------------------------------------------------|-----|---------------------------------------------------|-----|--------------------------------------------------|
|     |                                                   |     |                                                   |     |                                                  |
|     |                                                   |     |                                                   |     | <img src="../../drivers/fuji.files/image002.gif" width="95" /> |
|     | <img src="../../drivers/fuji.files/image003.gif" width="130" /> |     |                                                   |     |                                                  |
|     |                                                   |     | <img src="../../drivers/fuji.files/image004.gif" width="278" /> |     |                                                  |
|     |                                                   |     |                                                   |     |                                                  |
|     |                                                   |     |                                                   |     |                                                  |

De aansluiting van de HMI HM-serie is DB9F, die van de Fuji NB-serie RJ45.

**2. Software-instellingen**

Kies Fuji Electric Corporation bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de Fuji NB-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Serie Fuji NB              | Serie Fuji NB                               |
| **Poorttype** | RS422                       | RS422                                        |
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
| **Uitgebreide modus**       | Ja                         |

**3. Bruikbare registers en adresbereik**

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                            |
| **X**             | hhh                | 0~7ff           | Bit: Ingang, alleen lezen |
| **Y**             | hhh                | 0~7ff           | Bit: Uitgang           |
| **M**             | hhhh               | 0~7fff          | Bit: Intern relais (merker)                    |
| **SM**            | hhhh               | 8000~81ff       | Bit: Intern relais (merker)                    |
| **L**             | hhh                | 0~5ff           | Bit: Blokkeerrelais                     |
| **S**             | hh                 | 0~ff            | Bit: Staprelais                    |
| **T**             | hhh                | 0~1ff           | Bit: Timerstatus                   |
| **C**             | hh                 | 0~ff            | Bit: Tellerstatus                 |
| **D**             | hhhh               | 0~7fff          | Woord: Tijdelijk datageheugen           |
| **SD**            | hhhh               | 8000~80ff       | Woord: Tijdelijk datageheugen           |
| **TV**            | hhh                | 0~1ff           | Woord: Actuele waarde van de timer           |
| **CV**            | hh                 | 0~ff            | Woord: Actuele waarde van de teller         |

<img src="../../drivers/fuji.files/image005.gif" width="595" />

Opmerking:

h: hexadecimaal, invoerbereik 0-9, a-f;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat.

<img src="../../drivers/fuji.files/image005.gif" width="595" />

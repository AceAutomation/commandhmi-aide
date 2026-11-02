# Stuurprogramma HollySys

Met dit stuurprogramma leest en schrijft het touchscreen gegevens of statussen van de registers van PLC's HollySys LM-serie. De seriële verbinding loopt tussen de seriële poort van het touchscreen en die van de PLC. Lees vóór gebruik aandachtig dit hoofdstuk en de technische documentatie van de PLC.

**Verbinding maken met PLC's van de HOLLYSYS-serie**

**1.  Hardwareaansluiting**

Verbindingskabel:

RS232 (seriële poort, protocol RS232)

|                             |     |                        |     |
|-----------------------------|-----|------------------------|-----|
| **HMI HM-serie COM1/COM2** |     | **Serie HollySys LM** |     |
| 2                           | RX  | 3                      | TX  |
| 3                           | TX  | 2                      | RX  |
| 5                           | GND | 5                      | GND |

<img src="../../drivers/hollysys.files/image002.gif" width="130" /><img src="../../drivers/hollysys.files/image003.gif" width="290" /><img src="../../drivers/hollysys.files/image004.gif" width="130" />

De aansluiting van de HMI HM-serie is DB9F, die van de HollySys LM-serie DB9M.

**2. Software-instellingen**

Kies HollySys Group bij het aangesloten apparaat.

Kies bij het aangesloten apparaat het item dat overeenkomt met het PLC-model of het ondersteunde protocol.

Zorg dat de communicatieparameters van het touchscreen en het stationsnummer van de PLC overeenkomen met die van de aangesloten PLC.

Zie voor de instellingen van de PLC de technische documentatie van de HollySys LM-serie.

Standaardverbindingsparameters van de HMI HM-serie

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Instelling**            | **Standaardwaarde** | **Instelbereik**                            |
| **PLC-type**                | Serie HollySys LM          | Serie HollySys LM                           |
| **Poorttype** | RS232                       | RS232/RS422/RS485                            |
| **Baudrate**               | 38400                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Databits**         | 8                           | 7/8                                          |
| **Pariteit**              | NONE                        | EVEN/ODD/NONE                                |
| **Stopbits**         | 1                           | 1/2                                          |
| **Stationsnummer PLC**      | 51                          | 0~255                                        |
| **Stationsnummer HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Functie** | **Ondersteund** |
| **Offlinesimulatie** | Ja                         |
| **Onlinesimulatie**  | Ja                         |
| **Uitgebreide modus**       | Nee                          |

**3. Bruikbare registers en adresbereik**

|                   |                    |                 |                                                                                                       |
|-------------------|--------------------|-----------------|-------------------------------------------------------------------------------------------------------|
| **Registernaam** | **Adresformaat** | **Invoerbereik** | **Opmerkingen**                                                                                           |
| **IX**            | ddd.o              | 0.0~511.7       | Bit: I-geheugengebied, alleen lezen                                                                        |
| **QX**            | ddd.o              | 0.0~511.7       | Bit: Q-geheugengebied                                                                                   |
| **MX**            | dddd.o             | 0.0~7816.7      | Bit: M-geheugengebied                                                                                   |
| **IW**            | ddd                | 0~510           | Woord: I-geheugengebied, 8-bits register, elk woord neemt twee adressen in |
| **QW**            | ddd                | 0~510           | Woord: Q-geheugengebied, 8-bits register, elk woord neemt twee adressen in |
| **MW**            | dddd               | 0~8190          | Woord: M-geheugengebied, 8-bits register, elk woord neemt twee adressen in                               |

<img src="../../drivers/hollysys.files/image005.gif" width="600" />

Opmerking:

d: decimaal, invoerbereik 0-9;

o: octaal, invoerbereik 0-7;

Woord in de opmerkingen: het register kan alleen als woord worden gebruikt;

Bit in de opmerkingen: het register kan alleen als bit worden gebruikt;

8-bits register in de opmerkingen: de adresafstand tussen twee aangrenzende woorden van het register is 2;

Alleen lezen in de opmerkingen: het register kan worden gelezen maar niet beschreven;

Namen en bereiken van de registers kunnen per apparaatmodel verschillen.

Raadpleeg voor de exacte namen en bereiken de technische documentatie van het aangesloten apparaat

<img src="../../drivers/hollysys.files/image005.gif" width="600" />

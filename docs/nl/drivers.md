# Apparaatstuurprogramma's

Dit hoofdstuk beschrijft de apparaten die compatibel zijn met de HMI's van de HM-serie van ACE AUTOMATION.

Het instellen van de I/O van het apparaatstuurprogramma is belangrijk voor de configuratie. De HMI's van de HM-serie communiceren met PLC's, microcontrollers, frequentieregelaars en andere industriële apparatuur, waaronder de overgrote meerderheid van de PLC's: CommandHMI, MITSUBISHI, OMRON, SIEMENS, ALLEN-BRADLEY Rockwell, MATSUSHITA, DELTA, FATEK enz. Ze kunnen ook bepaalde industriële besturingsapparatuur bewaken en besturen via specifieke protocollen, zoals MODBUS RTU / ASCII, HOSTLINK en andere eigen protocollen.

Het I/O-stuurprogramma van elke PLC of elk apparaat is een apart bestand: bij het aanmaken van een project kiest u dus gewoon de juiste PLC of het juiste apparaat, zonder verdere ingewikkelde programmering. CommandHMI is de configuratiesoftware van de HMI's van de HM-serie en geeft met eenvoudige configuratiehandelingen toegang tot alle soorten registers en relais van de meeste PLC's en apparaten. Er zijn drie bedrijfsmodi: alleen lezen, alleen schrijven, en lezen en schrijven, voor alle eisen van de industriële besturing.

Om de aansluiting op verschillende apparaten te vergemakkelijken, ontwikkelt CommandHMI op verzoek stuurprogramma's; daarvoor is alleen het protocoldocument van het betreffende apparaat nodig. Neem contact op via de gegevens aan het einde van deze handleiding.

Door de HMI's van de HM-serie ondersteunde PLC's:

|                                                         |                                                |                                     |                                          |
|---------------------------------------------------------|------------------------------------------------|-------------------------------------|------------------------------------------|
| **Fabrikant (merk)**                            | **Model**                                      | **Communicatieprotocol**          | **Verbindingswijze**                      |
| [AIBUS](drivers/aibus.md)                               | AI-serie                                      | AIBUS-protocol                      | Directe verbinding (seriële poort)          |
| [Allen-Bradley](drivers/allen-bradley.md)               | MicroLogix-serie                              | DF1-protocol                        | Directe verbinding (seriële poort)          |
| [Can_communication](drivers/can_communication.md)       | Can                                            | Can                                 | Directe verbinding (seriële poort)          |
| [Delta Corporation](drivers/delta.md)                   | DVP-serie                                     | Eigen protocol van Delta       | Directe verbinding (seriële poort)          |
| [Emerson Network Power](drivers/emerson.md)             | EC-serie                                      | Eigen protocol van Emerson     | Directe verbinding (seriële poort)          |
| [Fatek Automation Corporation](drivers/fatek.md)        | FB-serie                                      | Eigen protocol van Fatek       | Directe verbinding (seriële poort)          |
| [Fuji Electric Corporation](drivers/fuji.md)            | NB-serie                                      | Eigen protocol van Fuji        | Directe verbinding (seriële poort)          |
| [GE Corporation](drivers/ge.md)                         | GE SNP-X/CCM                                   | Eigen protocol van GE          | Directe verbinding (seriële poort)          |
| [Haiwell Technology Corporation](drivers/haiwell.md)    | E/S/H-serie                                   | Eigen protocol van Corporation | Directe verbinding (seriële poort)          |
| [Hitachi Industrial](drivers/hitachi.md)                | E/EH-serie                                    | Eigen protocol van Hitachi     | Directe verbinding (seriële poort)          |
| [HollySys Group](drivers/hollysys.md)                   | LM-serie                                      | Eigen protocol van HollySys    | Directe verbinding (seriële poort)          |
| [IDEC Corporation](drivers/idec.md)                     | FC4A/FC5A-serie                               | Eigen protocol van IDEC        | Directe verbinding (seriële poort)          |
| [Inovance Technology Corporation](drivers/inovance.md)  | H1u/H2u-serie                                 | Eigen protocol van Inovance    | Directe verbinding (seriële poort)          |
| [Invt](drivers/invt.md)                                 | IVC1,IVC1L,IVCIS,IVC2L,IVC3                    | Eigen protocol van Invt        | Directe verbinding (seriële poort)          |
| [Keyence Corporation](drivers/keyence.md)               | KV-1000/700 KV-L20(R), KV-/40 KV-P16           | Eigen protocol van Keyence     | Directe verbinding (seriële poort)          |
| [Koyo Electronics](drivers/koyo.md)                     | SN-serie                                      | Eigen protocol van KoYo        | Directe verbinding (seriële poort)          |
| [LG Industrial Systems](drivers/lg.md)                  | Master-K-serie                                | Eigen protocol van LG          | Directe verbinding (seriële poort)          |
| [Matsushita](drivers/matsushita.md)                     | FP-serie                                      | Eigen protocol van Matsushita  | Directe verbinding (seriële poort)          |
| [Mitsubishi](drivers/mitsubishi.md)                     | Melsec-FX/FX2N/FX3U/FX3G，Melsec-Q_C24N-serie | Eigen protocol van Mitsubishi  | Directe verbinding (seriële poort)          |
| [Modbus](drivers/modbus.md)                             | RTU/ASCII-apparatuur，RTU TCP/IP-apparatuur      | Modbus-protocol                     | Directe verbinding (seriële poort/Ethernet) |
| [Modicon Corporation](drivers/modicon.md)               | NEZA/TWIDO/M218-serie                         | Modbus-protocol                     | Directe verbinding (seriële poort)          |
| [Nanda Auto Technology](drivers/nanda.md)               | NA-200/NA-400-serie                           | Eigen protocol van Nanda Auto  | Directe verbinding (seriële poort)          |
| [Omron](drivers/omron.md)                               | C/CPM-serie，CS/CJ-serie                     | Eigen protocol van Omron       | Directe verbinding (seriële poort)          |
|                                                         |                                                |                                     |                                          |
| [Siemens](drivers/siemens.md)                           | S7-200(PPI)，S7-300(MPI), S7-1200              | Eigen protocol van Siemens     | Directe verbinding (seriële poort)          |
| [TaiAn Technology](drivers/taian.md)                    | TP03-serie                                    | Eigen protocol van TaiAn       | Directe verbinding (seriële poort)          |
| [TaiLing Electric](drivers/tailing.md)                  | DX-serie                                      | Eigen protocol van TaiLing     | Directe verbinding (seriële poort)          |
| [Techwayson Technology](drivers/techwayson.md)          | V-serie                                       | Eigen protocol van Techwayson  | Directe verbinding (seriële poort)          |
| [Vigor Electric Corporation](drivers/vigor.md)          | V/VH/VB/M-serie                               | Eigen protocol van Vigor       | Directe verbinding (seriële poort)          |
| [Xinje Electronic](drivers/xinje.md)                    | XC/XCM-serie                                  | Eigen protocol van XinJe       | Directe verbinding (seriële poort)          |
| [Yokogawa Electric Corporation](drivers/yokogawa.md)    | FA-M3-serie                                   | Eigen protocol van Yokogawa    | Directe verbinding (seriële poort)          |
| [ZhengHang Electronics](drivers/zhenghang.md)           | A4/A5-serie                                   | Eigen protocol van ZhengHang   | Directe verbinding (seriële poort)          |

• Pintoewijzing COM1/COM2 van de HMI HM-serie

De HMI's van de HM-serie hebben een 9-polige stekker; de verbindingskabel moet dus een 9-polige bus hebben. Pintoewijzing:

|                             |     |
|-----------------------------|-----|
| **HMI HM-serie COM1/COM2** |     |
| **1**                       |     |
| **2**                       | RX  |
| **3**                       | TX  |
| **4**                       | KZ  |
| **5**                       | GND |
| **6**                       | RX- |
| **7**                       | RX+ |
| **8**                       |     |
| **9**                       |     |

• RX: RS232, ontvangen

•  TX: RS232, zenden

• KZ: stuurpoort

• GND: massa

• RX-: RS422, ontvangen -

• RX+: RS422, ontvangen +

• TX-: RS422, zenden - / RS485 B

• TX+: RS422, zenden + / RS485 A

<img src="../drivers.files/image002.gif" width="761" />

Opmerking

·Aansluitingen 2/3/5 bij RS232-communicatie;

·Aansluitingen 6/7/8/9 bij RS422-communicatie;

·Aansluitingen 8/9 bij RS485-communicatie.

<img src="../drivers.files/image003.gif" width="761" />

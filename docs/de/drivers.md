# Gerätetreiber

Dieses Kapitel beschreibt die Geräte, die mit den HMI der HM-Serie von ACE AUTOMATION kompatibel sind.

Die E/A-Einstellung des Gerätetreibers ist für die Projektierung wichtig. Die HMI der HM-Serie kommunizieren mit SPS, Mikrocontrollern, Frequenzumrichtern und anderen Industriegeräten, darunter den meisten SPS: CommandHMI, MITSUBISHI, OMRON, SIEMENS, ALLEN-BRADLEY Rockwell, MATSUSHITA, DELTA, FATEK usw. Über bestimmte Protokolle wie MODBUS RTU / ASCII, HOSTLINK und andere benutzerdefinierte Protokolle lassen sich auch weitere Industriegeräte überwachen und steuern.

Der E/A-Treiber jeder SPS bzw. jedes Geräts ist eine eigene Datei; bei der Projektierung muss nur die passende SPS bzw. das Gerät gewählt werden, ohne aufwendige Programmierung. CommandHMI ist die Projektierungssoftware der HM-Serie und erschließt durch einfache Projektierung alle Register und Relais der meisten SPS bzw. Geräte. Drei Zugriffsarten stehen zur Verfügung: nur lesen, nur schreiben, lesen und schreiben – für alle Anforderungen der Steuerungstechnik.

Um die Anbindung weiterer Geräte zu erleichtern, entwickelt CommandHMI Technology Co., Ltd auf Anfrage Gerätetreiber; dazu genügt die Protokolldokumentation des Kommunikationsgeräts. Wenden Sie sich über die Kontaktangaben am Ende dieses Handbuchs an das Unternehmen.

Von den HMI der HM-Serie unterstützte SPS:

|                                                         |                                                |                                     |                                          |
|---------------------------------------------------------|------------------------------------------------|-------------------------------------|------------------------------------------|
| **Hersteller (Marke)**                            | **Modell**                                      | **Kommunikationsprotokoll**          | **Verbindungsart**                      |
| [AIBUS](drivers/aibus.md)                               | Serie AI                                       | AIBUS-Protokoll                      | Direktverbindung (seriell)              |
| [Allen-Bradley](drivers/allen-bradley.md)               | Serie MicroLogix                               | DF1-Protokoll                        | Direktverbindung (seriell)              |
| [Can_communication](drivers/can_communication.md)       | Can                                            | Can                                 | Direktverbindung (seriell)              |
| [Delta Corporation](drivers/delta.md)                   | Serie DVP                                      | Delta-Protokoll                      | Direktverbindung (seriell)              |
| [Emerson Network Power](drivers/emerson.md)             | Serie EC                                       | Emerson-Protokoll                    | Direktverbindung (seriell)              |
| [Fatek Automation Corporation](drivers/fatek.md)        | Serie FB                                       | Fatek-Protokoll                      | Direktverbindung (seriell)              |
| [Fuji Electric Corporation](drivers/fuji.md)            | Serie NB                                       | Fuji-Protokoll                       | Direktverbindung (seriell)              |
| [GE Corporation](drivers/ge.md)                         | GE SNP-X/CCM                                   | GE-Protokoll                         | Direktverbindung (seriell)              |
| [Haiwell Technology Corporation](drivers/haiwell.md)    | Serie E/S/H                                    | Herstellerprotokoll                  | Direktverbindung (seriell)              |
| [Hitachi Industrial](drivers/hitachi.md)                | Serie E/EH                                     | Hitachi-Protokoll                    | Direktverbindung (seriell)              |
| [HollySys Group](drivers/hollysys.md)                   | Serie LM                                       | HollySys-Protokoll                   | Direktverbindung (seriell)              |
| [IDEC Corporation](drivers/idec.md)                     | Serie FC4A/FC5A                                | IDEC-Protokoll                       | Direktverbindung (seriell)              |
| [Inovance Technology Corporation](drivers/inovance.md)  | Serie H1u/H2u                                  | Inovance-Protokoll                   | Direktverbindung (seriell)              |
| [Invt](drivers/invt.md)                                 | IVC1,IVC1L,IVCIS,IVC2L,IVC3                    | Invt-Protokoll                       | Direktverbindung (seriell)              |
| [Keyence Corporation](drivers/keyence.md)               | KV-1000/700 KV-L20(R), KV-/40 KV-P16           | Keyence-Protokoll                    | Direktverbindung (seriell)              |
| [Koyo Electronics](drivers/koyo.md)                     | Serie SN                                       | KoYo-Protokoll                       | Direktverbindung (seriell)              |
| [LG Industrial Systems](drivers/lg.md)                  | Serie Master-K                                 | LG-Protokoll                         | Direktverbindung (seriell)              |
| [Matsushita](drivers/matsushita.md)                     | Serie FP                                       | Matsushita-Protokoll                 | Direktverbindung (seriell)              |
| [Mitsubishi](drivers/mitsubishi.md)                     | Melsec-FX/FX2N/FX3U/FX3G, Serie Melsec-Q_C24N  | Mitsubishi-Protokoll                 | Direktverbindung (seriell)              |
| [Modbus](drivers/modbus.md)                             | RTU/ASCII-Geräte, RTU-TCP/IP-Geräte            | Modbus-Protokoll                     | Direktverbindung (seriell/Ethernet)     |
| [Modicon Corporation](drivers/modicon.md)               | Serie NEZA/TWIDO/M218                          | Modbus-Protokoll                     | Direktverbindung (seriell)              |
| [Nanda Auto Technology](drivers/nanda.md)               | Serie NA-200/NA-400                            | Nanda-Auto-Protokoll                 | Direktverbindung (seriell)              |
| [Omron](drivers/omron.md)                               | Serie C/CPM, Serie CS/CJ                       | Omron-Protokoll                      | Direktverbindung (seriell)              |
|                                                         |                                                |                                     |                                          |
| [Siemens](drivers/siemens.md)                           | S7-200(PPI), S7-300(MPI), S7-1200              | Siemens-Protokoll                    | Direktverbindung (seriell)              |
| [TaiAn Technology](drivers/taian.md)                    | Serie TP03                                     | TaiAn-Protokoll                      | Direktverbindung (seriell)              |
| [TaiLing Electric](drivers/tailing.md)                  | Serie DX                                       | TaiLing-Protokoll                    | Direktverbindung (seriell)              |
| [Techwayson Technology](drivers/techwayson.md)          | Serie V                                        | Techwayson-Protokoll                 | Direktverbindung (seriell)              |
| [Vigor Electric Corporation](drivers/vigor.md)          | Serie V/VH/VB/M                                | Vigor-Protokoll                      | Direktverbindung (seriell)              |
| [Xinje Electronic](drivers/xinje.md)                    | Serie XC/XCM                                   | XinJe-Protokoll                      | Direktverbindung (seriell)              |
| [Yokogawa Electric Corporation](drivers/yokogawa.md)    | Serie FA-M3                                    | Yokogawa-Protokoll                   | Direktverbindung (seriell)              |
| [ZhengHang Electronics](drivers/zhenghang.md)           | Serie A4/A5                                    | ZhengHang-Protokoll                  | Direktverbindung (seriell)              |

• Anschlussbelegung COM1/COM2 der HMI der HM-Serie

Die HMI der HM-Serie haben einen 9-poligen Stecker; das Verbindungskabel benötigt daher eine 9-polige Buchse. Die Anschlussbelegung:

|                             |     |
|-----------------------------|-----|
| **HMI der HM-Serie COM1/COM2** |     |
| **1**                       |     |
| **2**                       | RX  |
| **3**                       | TX  |
| **4**                       | KZ  |
| **5**                       | GND |
| **6**                       | RX- |
| **7**                       | RX+ |
| **8**                       |     |
| **9**                       |     |

• RX: RS232 Empfang

•  TX: RS232 Senden

• KZ: Steueranschluss

• GND: Masse

• RX-: RS422 Empfang -

• RX+: RS422 Empfang +

• TX-: RS422 Senden -/RS485 B

• TX+: RS422 Senden +/RS485 A

<img src="../drivers.files/image002.gif" width="761" />

Hinweis

·Pins 2/3/5 bei RS232-Kommunikation;

·Pins 6/7/8/9 bei RS422-Kommunikation;

·Pins 8/9 bei RS485-Kommunikation.

<img src="../drivers.files/image003.gif" width="761" />

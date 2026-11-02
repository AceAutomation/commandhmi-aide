# Device driver

This chapter details connected devices compatible with the HM series HMI of ACE AUTOMATION Technology Co., Ltd.

It is important for the configuration to set I / O of device driver. HM series HMI can communicate with PLC, MCU, inverter and other industrial equipment, including the vast majority of PLCs: CommandHMI, MITSUBISHI, OMRON, SIEMENS, ALLEN-BRADLEY Rockwell, MATSUSHITA, DELTA, FATEK, etc. Or it can also monitor and control certain industrial control equipment via specific protocol, such as MODBUS RTU / ASCII, HOSTLINK and some other custom protocols.

I / O driver of each PLC or device is made into a file, so it only needs to select the corresponding PLC or device when creating a configuration project without the necessity for engineers to perform other complex programming operation. CommandHMI is the configuration software of HM series HMI, which can realize functions of all kinds of registers or relays of most PLCs or devices through simple and convenient configuration operations. There are three operation modes: read only, write only, read and write, meeting various requirements of industrial control.

To facilitate connections to different devices, CommandHMI Technology Co., Ltd launches the service of developing device-driven according to the needs of users, simply with need of an appropriate protocol document of corresponding communication device. Users can contact Technology Co., Ltd. via the contact information provided at the end of this manual.

PLCs supported by HM series HMI:

|                                                         |                                                |                                     |                                          |
|---------------------------------------------------------|------------------------------------------------|-------------------------------------|------------------------------------------|
| **Manufacturer(Brand)**                            | **Model**                                      | **Communication Protocol**          | **Connection Mode**                      |
| [AIBUS](drivers/aibus.md)                               | AI series                                      | AIBUS protocol                      | Direct connection (Serial port)          |
| [Allen-Bradley](drivers/allen-bradley.md)               | MicroLogix series                              | DF1 protocol                        | Direct connection (Serial port)          |
| [Can_communication](drivers/can_communication.md)       | Can                                            | Can                                 | Direct connection (Serial port)          |
| [Delta Corporation](drivers/delta.md)                   | DVP series                                     | Proprietary protocol of Delta       | Direct connection (Serial port)          |
| [Emerson Network Power](drivers/emerson.md)             | EC series                                      | Proprietary protocol of Emerson     | Direct connection (Serial port)          |
| [Fatek Automation Corporation](drivers/fatek.md)        | FB series                                      | Proprietary protocol of Fatek       | Direct connection (Serial port)          |
| [Fuji Electric Corporation](drivers/fuji.md)            | NB series                                      | Proprietary protocol of Fuji        | Direct connection (Serial port)          |
| [GE Corporation](drivers/ge.md)                         | GE SNP-X/CCM                                   | Proprietary protocol of GE          | Direct connection (Serial port)          |
| [Haiwell Technology Corporation](drivers/haiwell.md)    | E/S/H series                                   | Proprietary protocol of Corporation | Direct connection (Serial port)          |
| [Hitachi Industrial](drivers/hitachi.md)                | E/EH series                                    | Proprietary protocol of Hitachi     | Direct connection (Serial port)          |
| [HollySys Group](drivers/hollysys.md)                   | LM series                                      | Proprietary protocol of HollySys    | Direct connection (Serial port)          |
| [IDEC Corporation](drivers/idec.md)                     | FC4A/FC5A series                               | Proprietary protocol of IDEC        | Direct connection (Serial port)          |
| [Inovance Technology Corporation](drivers/inovance.md)  | H1u/H2u series                                 | Proprietary protocol of Inovance    | Direct connection (Serial port)          |
| [Invt](drivers/invt.md)                                 | IVC1,IVC1L,IVCIS,IVC2L,IVC3                    | Proprietary protocol of Invt        | Direct connection (Serial port)          |
| [Keyence Corporation](drivers/keyence.md)               | KV-1000/700 KV-L20(R), KV-/40 KV-P16           | Proprietary protocol of Keyence     | Direct connection (Serial port)          |
| [Koyo Electronics](drivers/koyo.md)                     | SN series                                      | Proprietary protocol of KoYo        | Direct connection (Serial port)          |
| [LG Industrial Systems](drivers/lg.md)                  | Master-K series                                | Proprietary protocol of LG          | Direct connection (Serial port)          |
| [Matsushita](drivers/matsushita.md)                     | FP series                                      | Proprietary protocol of Matsushita  | Direct connection (Serial port)          |
| [Mitsubishi](drivers/mitsubishi.md)                     | Melsec-FX/FX2N/FX3U/FX3G，Melsec-Q_C24N series | Proprietary protocol of Mitsubishi  | Direct connection (Serial port)          |
| [Modbus](drivers/modbus.md)                             | RTU/ASCII Equipment，RTU TCP/IP Equipment      | Modbus Protocol                     | Direct connection (Serial port/Ethernet) |
| [Modicon Corporation](drivers/modicon.md)               | NEZA/TWIDO/M218 series                         | Modbus Protocol                     | Direct connection (Serial port)          |
| [Nanda Auto Technology](drivers/nanda.md)               | NA-200/NA-400 series                           | Proprietary protocol of Nanda Auto  | Direct connection (Serial port)          |
| [Omron](drivers/omron.md)                               | C/CPM series，CS/CJ series                     | Proprietary protocol of Omron       | Direct connection (Serial port)          |
|                                                         |                                                |                                     |                                          |
| [Siemens](drivers/siemens.md)                           | S7-200(PPI)，S7-300(MPI), S7-1200              | Proprietary protocol of Siemens     | Direct connection (Serial port)          |
| [TaiAn Technology](drivers/taian.md)                    | TP03 series                                    | Proprietary protocol of TaiAn       | Direct connection (Serial port)          |
| [TaiLing Electric](drivers/tailing.md)                  | DX series                                      | Proprietary protocol of TaiLing     | Direct connection (Serial port)          |
| [Techwayson Technology](drivers/techwayson.md)          | V series                                       | Proprietary protocol of Techwayson  | Direct connection (Serial port)          |
| [Vigor Electric Corporation](drivers/vigor.md)          | V/VH/VB/M series                               | Proprietary protocol of Vigor       | Direct connection (Serial port)          |
| [Xinje Electronic](drivers/xinje.md)                    | XC/XCM series                                  | Proprietary protocol of XinJe       | Direct connection (Serial port)          |
| [Yokogawa Electric Corporation](drivers/yokogawa.md)    | FA-M3 series                                   | Proprietary protocol of Yokogawa    | Direct connection (Serial port)          |
| [ZhengHang Electronics](drivers/zhenghang.md)           | A4/A5 series                                   | Proprietary protocol of ZhengHang   | Direct connection (Serial port)          |

• Pin definitions of HM series HMI COM1/COM2

HM series HMI employs nine-pin plug so that it should be nine-pin receptacle for the connection cable. Pin definitions are shown below:

|                             |     |
|-----------------------------|-----|
| **HM series HMI COM1/COM2** |     |
| **1**                       |     |
| **2**                       | RX  |
| **3**                       | TX  |
| **4**                       | KZ  |
| **5**                       | GND |
| **6**                       | RX- |
| **7**                       | RX+ |
| **8**                       |     |
| **9**                       |     |

• RX：RS232  Receiver of communication

•  TX：RS232 Sender of communication

• KZ：Control port

• GND：Ground terminal

• RX-：RS422 Communication receiving-

• RX+：RS422 Communication receiving +

• TX-：RS422 Communication transporting -/RS485 Communication B

• TX+：RS422 Communication transporting +/RS485 Communication A

<img src="drivers.files/image002.gif" width="761" />

Note

·Terminals of 2/3/5 in case of RS232 communication ；

·Terminals of 6/7/8/9 in case of RS422 communication；

·Terminals of 8/9 in case of RS485 communication.

<img src="drivers.files/image003.gif" width="761" />

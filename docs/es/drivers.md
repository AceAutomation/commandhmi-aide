# Controladores de equipos

Este capítulo describe los equipos compatibles con los HMI de la serie HM de ACE AUTOMATION.

La configuración de E/S del controlador del equipo es esencial en el proyecto. Los HMI de la serie HM se comunican con PLC, microcontroladores, variadores y otros equipos industriales, incluida la gran mayoría de PLC: CommandHMI, MITSUBISHI, OMRON, SIEMENS, ALLEN-BRADLEY Rockwell, MATSUSHITA, DELTA, FATEK, etc. También pueden supervisar y controlar ciertos equipos mediante protocolos específicos, como MODBUS RTU / ASCII, HOSTLINK y otros protocolos personalizados.

El controlador de E/S de cada PLC o equipo es un archivo: al crear el proyecto basta con elegir el PLC o equipo, sin programación compleja. CommandHMI, el software de configuración de los HMI de la serie HM, permite acceder a todo tipo de registros o relés de la mayoría de PLC o equipos mediante una configuración sencilla. Hay tres modos de acceso: solo lectura, solo escritura y lectura/escritura, que cubren las distintas necesidades del control industrial.

Para facilitar la conexión a otros equipos, se ofrece el desarrollo de controladores a medida según las necesidades de los usuarios; solo hace falta la documentación del protocolo del equipo de comunicación correspondiente. Los usuarios pueden contactar con nosotros mediante los datos de contacto que figuran al final de este manual.

PLC compatibles con los HMI de la serie HM:

|                                                         |                                                |                                     |                                          |
|---------------------------------------------------------|------------------------------------------------|-------------------------------------|------------------------------------------|
| **Fabricante (marca)**                            | **Modelo**                                      | **Protocolo de comunicación**          | **Modo de conexión**                      |
| [AIBUS](drivers/aibus.md)                               | Serie AI                                      | Protocolo AIBUS                      | Conexión directa (puerto serie)          |
| [Allen-Bradley](drivers/allen-bradley.md)               | Serie MicroLogix                              | Protocolo DF1                        | Conexión directa (puerto serie)          |
| [Comunicación CAN](drivers/can_communication.md)       | Can                                            | Can                                 | Conexión directa (puerto serie)          |
| [Delta Corporation](drivers/delta.md)                   | Serie DVP                                     | Protocolo propio de Delta       | Conexión directa (puerto serie)          |
| [Emerson Network Power](drivers/emerson.md)             | Serie EC                                      | Protocolo propio de Emerson     | Conexión directa (puerto serie)          |
| [Fatek Automation Corporation](drivers/fatek.md)        | Serie FB                                      | Protocolo propio de Fatek       | Conexión directa (puerto serie)          |
| [Fuji Electric Corporation](drivers/fuji.md)            | Serie NB                                      | Protocolo propio de Fuji        | Conexión directa (puerto serie)          |
| [GE Corporation](drivers/ge.md)                         | GE SNP-X/CCM                                   | Protocolo propio de GE          | Conexión directa (puerto serie)          |
| [Haiwell Technology Corporation](drivers/haiwell.md)    | Serie E/S/H                                    | Protocolo propio de Haiwell | Conexión directa (puerto serie)          |
| [Hitachi Industrial](drivers/hitachi.md)                | Serie E/EH                                    | Protocolo propio de Hitachi     | Conexión directa (puerto serie)          |
| [HollySys Group](drivers/hollysys.md)                   | Serie LM                                    | Protocolo propio de HollySys    | Conexión directa (puerto serie)          |
| [IDEC Corporation](drivers/idec.md)                     | Serie FC4A/FC5A                               | Protocolo propio de IDEC        | Conexión directa (puerto serie)          |
| [Inovance Technology Corporation](drivers/inovance.md)  | Serie H1u/H2u                                 | Protocolo propio de Inovance    | Conexión directa (puerto serie)          |
| [Invt](drivers/invt.md)                                 | IVC1,IVC1L,IVCIS,IVC2L,IVC3                    | Protocolo propio de Invt        | Conexión directa (puerto serie)          |
| [Keyence Corporation](drivers/keyence.md)               | KV-1000/700 KV-L20(R), KV-/40 KV-P16           | Protocolo propio de Keyence     | Conexión directa (puerto serie)          |
| [Koyo Electronics](drivers/koyo.md)                     | Serie SN                                      | Protocolo propio de Koyo        | Conexión directa (puerto serie)          |
| [LG Industrial Systems](drivers/lg.md)                  | Serie Master-K                                | Protocolo propio de LG          | Conexión directa (puerto serie)          |
| [Matsushita](drivers/matsushita.md)                     | Serie FP                                      | Protocolo propio de Matsushita  | Conexión directa (puerto serie)          |
| [Mitsubishi](drivers/mitsubishi.md)                     | Serie Melsec-FX/FX2N/FX3U/FX3G，Melsec-Q_C24N | Protocolo propio de Mitsubishi  | Conexión directa (puerto serie)          |
| [Modbus](drivers/modbus.md)                             | Equipos RTU/ASCII，equipos RTU TCP/IP      | Protocolo Modbus                     | Conexión directa (puerto serie/Ethernet) |
| [Modicon Corporation](drivers/modicon.md)               | Serie NEZA/TWIDO/M218                         | Protocolo Modbus                     | Conexión directa (puerto serie)          |
| [Nanda Auto Technology](drivers/nanda.md)               | Serie NA-200/NA-400                           | Protocolo propio de Nanda Auto  | Conexión directa (puerto serie)          |
| [Omron](drivers/omron.md)                               | Serie C/CPM，serie CS/CJ                     | Protocolo propio de Omron       | Conexión directa (puerto serie)          |
|                                                         |                                                |                                     |                                          |
| [Siemens](drivers/siemens.md)                           | S7-200(PPI)，S7-300(MPI), S7-1200              | Protocolo propio de Siemens     | Conexión directa (puerto serie)          |
| [TaiAn Technology](drivers/taian.md)                    | Serie TP03                                    | Protocolo propio de TaiAn       | Conexión directa (puerto serie)          |
| [TaiLing Electric](drivers/tailing.md)                  | Serie DX                                      | Protocolo propio de TaiLing     | Conexión directa (puerto serie)          |
| [Techwayson Technology](drivers/techwayson.md)          | Serie V                                       | Protocolo propio de Techwayson  | Conexión directa (puerto serie)          |
| [Vigor Electric Corporation](drivers/vigor.md)          | Serie V/VH/VB/M                               | Protocolo propio de Vigor       | Conexión directa (puerto serie)          |
| [Xinje Electronic](drivers/xinje.md)                    | Serie XC/XCM                                  | Protocolo propio de Xinje       | Conexión directa (puerto serie)          |
| [Yokogawa Electric Corporation](drivers/yokogawa.md)    | Serie FA-M3                                   | Protocolo propio de Yokogawa    | Conexión directa (puerto serie)          |
| [ZhengHang Electronics](drivers/zhenghang.md)           | Serie A4/A5                                   | Protocolo propio de ZhengHang   | Conexión directa (puerto serie)          |

• Asignación de pines de COM1/COM2 de los HMI de la serie HM

Los HMI de la serie HM tienen un conector macho de nueve pines, por lo que el cable de conexión debe llevar un conector hembra de nueve pines. Asignación de pines:

|                             |     |
|-----------------------------|-----|
| **HMI serie HM COM1/COM2** |     |
| **1**                       |     |
| **2**                       | RX  |
| **3**                       | TX  |
| **4**                       | KZ  |
| **5**                       | GND |
| **6**                       | RX- |
| **7**                       | RX+ |
| **8**                       |     |
| **9**                       |     |

• RX: recepción RS232

•  TX: emisión RS232

• KZ: puerto de control

• GND: tierra

• RX-: recepción RS422 -

• RX+: recepción RS422 +

• TX-: emisión RS422 - / RS485 B

• TX+: emisión RS422 + / RS485 A

<img src="../drivers.files/image002.gif" width="761" />

Nota

·Bornes 2/3/5 para la comunicación RS232;

·Bornes 6/7/8/9 para la comunicación RS422;

·Bornes 8/9 para la comunicación RS485.

<img src="../drivers.files/image003.gif" width="761" />

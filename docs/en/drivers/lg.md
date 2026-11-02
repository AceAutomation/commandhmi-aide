# LG device driver

The device driver is used for HM series HMI to read and write the data or state of LG Master-K series PLC register. The serial communication connection is established through the serial port on the touch screen and the serial port of LG Master-K series PLC, so as to operate LG Master-K series PLC. Prior to use of the driver, one shall carefully read related technical specifications of the chapter and LG Master-K series PLC.

How to establish connection with LG Master-K series PLC

**1.Hardware connection**

Connecting cable:

RS232-using CNet protocol<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> (serial port RS232 protocol)

|                                                                                                                    |     |                 |     |
|--------------------------------------------------------------------------------------------------------------------|-----|-----------------|-----|
| <span id="OLE_LINK60"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span>**HM series HMI COM1/COM2** |     | **LG Master-K** |     |
| 2                                                                                                                  | RX  | 7               | TX  |
| 3                                                                                                                  | TX  | 4               | RX  |
| 5                                                                                                                  | GND | 5               | GND |

<img src="lg.files/image002.gif" width="130" /><img src="lg.files/image003.gif" width="291" /><img src="lg.files/image004.gif" width="130" />

Terminal of HMI is DB9F, and that of LG Master-K series PLC is DB9M.

RS232-Employ KLoader protocol

|                                                                                       |     |                 |     |
|---------------------------------------------------------------------------------------|-----|-----------------|-----|
| <span id="OLE_LINK65"></span><span id="OLE_LINK66"></span>**HM series HMI COM1/COM2** |     | **LG Master-K** |     |
| 2                                                                                     | RX  | 3               | TX  |
| 3                                                                                     | TX  | 2               | RX  |
| 5                                                                                     | GND | 5               | GND |

<img src="lg.files/image005.gif" width="291" /><img src="lg.files/image006.gif" width="130" /><img src="lg.files/image007.gif" width="130" />

Terminal of HMI is DB9F, and that of LG Master-K series PLC is DB9M.

RS<span id="OLE_LINK51"></span><span id="OLE_LINK52"></span>485

|                                                          |     |                 |
|----------------------------------------------------------|-----|-----------------|
| <span id="OLE_LINK67"></span>**HM series HMI COM1/COM2** |     | **LG Master-K** |
| 8                                                        | D-  | B               |
| 9                                                        | D+  | A               |

 <img src="lg.files/image008.gif" width="157" /><img src="lg.files/image009.gif" width="130" />

Terminal of HMI is DB9F, and that of LG Master-K series PLC is two-wire terminal.

RS232-K10S1

|                             |     |                 |     |
|-----------------------------|-----|-----------------|-----|
| **HM series HMI COM1/COM2** |     | **LG Master-K** |     |
| 2                           | RX  | 4               | TX  |
| 3                           | TX  | 1               | RX  |
| 5                           | GND | 6               | GND |

Terminal of HMI is DB9F, and that of LG Master-K series PLC is MD6M.

|     |                                                 |     |                                                 |
|-----|-------------------------------------------------|-----|-------------------------------------------------|
|     |                                                 |     |                                                 |
|     |                                                 |     | <img src="lg.files/image010.gif" width="146" /> |
|     | <img src="lg.files/image011.gif" width="401" /> |     |                                                 |
|     |                                                 |     |                                                 |

**2.Software settings**

Select LG Industrial Systems in connection device service.

Select the corresponding item in connection device service according to the connected PLC model or supported protocol.

Ensure that the communication parameters in touch screen connection parameters and PLC station number are consistent with the PLC connected.

For settings of the PLC connected, refer to the technical documents of the LG Master-K series PLC.

Default connection parameters of HM series HMI

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Setting item**            | **Default parameter value** | **Setting scope**                            |
| **PLC type**                | LG Master-K Cnet            | LG Master-K Cnet/K Loader/K10s1              |
| **Communication port type** | RS232                       | RS232/RS422/RS485                            |
| **Baud rate**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Data bit length**         | 8                           | 7/8                                          |
| **Parity bit**              | NONE                        | EVEN/ODD/NONE                                |
| **Stop bit length**         | 1                           | 1/2                                          |
| **PLC station number**      | 0                           | 0~255                                        |
| **HMI station number**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Supporting function** | **Whether it is supported** |
| **Off-line simulation** | Yes                         |
| **On-line simulation**  | Yes                         |
| **Extended mode**       | Yes                         |

**3.Operational register and address range**

Operational address range of Kxxx series PLC:

|               |                |             |                                |
|---------------|----------------|-------------|--------------------------------|
| Register name | Address format | Input range | Remarks                        |
| P_Bit         | dddh           | 0~255f      | Bit: input/output area         |
| M_Bit         | dddh           | 0~255f      | Bit: auxiliary relay           |
| K_Bit         | dddh           | 0~255f      | Bit: protection relay          |
| L_Bit         | dddh           | 0~255f      | Bit: link relay                |
| F_Bit         | dddh           | 0~255f      | Bit: special relay             |
| P             | dddh           | 0~255f      | Word: input/output area        |
| M             | dddh           | 0~255f      | Word: auxiliary relay          |
| K             | dddh           | 0~255f      | Word: protection relay         |
| L             | dddh           | 0~255f      | Word: link relay               |
| F             | dddh           | 0~255f      | Word: special relay            |
| T             | ddd            | 0~255       | Bit: timer relay               |
| C             | ddd            | 0~255       | Bit: counter relay             |
| S             | dddd           | 0~9999      | Word: stepping register        |
| D             | dddd           | 0~9999      | Word: data register            |
| TV            | ddd            | 0~255       | Word: current value of timer   |
| CV            | ddd            | 0~255       | Word: current value of counter |

XGB CPU series PLC operable address range (via PLC RS232 download port communication)：

|                |              |              |                                   |
|----------------|--------------|--------------|-----------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                          |
| P_Bit          | ddddh        | 0-1023f      | Bit: input/output area            |
| M_Bit          | ddddh        | 0-1023f      | Bit: auxiliary relay              |
| F_Bit          | ddddh        | 0-1023f      | Bit: special relay                |
| L_Bit          | ddddh        | 0-2047f      | Bit: link relay                   |
| K_Bit          | ddddh        | 0-4095f      | Bit: protection relay             |
| D_Bit          | ddddh        | 0-10239f     |                                   |
| T              | dddd         | 0-1023       | Bit: timer relay                  |
| C              | dddd         | 0-1023       | Bit: counter relay                |
| TV             | dddd         | 0-1023       | Word: current value of timer      |
| CV             | dddd         | 0-1023       | Word: current value of counter    |
| P              | dddd         | 0-1023       | Word: input/output area           |
| M              | dddd         | 0-1023       | Word: auxiliary relay             |
| F              | dddd         | 0-1023       | Word: special relay （read only） |
| L              | dddd         | 0-2047       | Word: link relay                  |
| K              | dddd         | 0-4095       | Word: protection relay            |
| D              | dddd         | 0-10239      | Word: data register               |
| R              | dddd         | 0-10239      | Word: stepping register           |
| ZR             | dddd         | 0-10239      | Word:                             |
| S              | ddd          | 0-127        | Word: stepping register           |
| Z              | ddd          | 0-127        | Word:                             |
| U              | dd.dd        | 0.0-10.31    | Word：（read only）               |

Operational address range of XGB CNET series PLC:

|               |                |             |                         |
|---------------|----------------|-------------|-------------------------|
| Register name | Address format | Input range | Remarks                 |
| P             | dddh           | 0~127f      | Word: input/output area |
| M             | dddh           | 0~255f      | Word: auxiliary relay   |
| K             | dddh           | 0~2559f     | Word: protection relay  |
| L             | dddh           | 0~1279f     | Word: link relay        |
| F             | dddh           | 0~255f      | Word: special relay     |
| T             | ddd            | 0~255       | Bit: timer relay        |
| C             | ddd            | 0~255       | Bit: counter relay      |
| S             | ddd            | 0~127.99    | Word: stepping register |
| D             | dddd           | 0~5119      | Word: data register     |
| N             | dddd           | 0~3935      |                         |
| Z             | ddd            | 0~127       |                         |
| ZR            | dddd           | 0~1023      |                         |
| U             | d              | 0~7.31      |                         |

XGB TCP/IP

|                |              |              |                                   |
|----------------|--------------|--------------|-----------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                          |
| P_Bit          | ddddh        | 0-2047f      | Bit: input/output area            |
| M_Bit          | ddddh        | 0-2047f      | Bit: auxiliary relay              |
| F_Bit          | ddddh        | 0-2047f      | Bit: special relay                |
| L_Bit          | ddddh        | 0-4095f      | Bit: link relay                   |
| K_Bit          | ddddh        | 0-8191f      | Bit: protection relay             |
| T              | dddd         | 0-2047       | Bit: timer relay                  |
| C              | dddd         | 0-2047       | Bit: counter relay                |
| TV             | dddd         | 0-2047       | Word: current value of timer      |
| CV             | dddd         | 0-2047       | Word: current value of counter    |
| P              | dddd         | 0-2047       | Word: input/output area           |
| M              | dddd         | 0-2047       | Word: auxiliary relay             |
| F              | dddd         | 0-2047       | Word: special relay （read only） |
| L              | dddd         | 0-4095       | Word: link relay                  |
| K              | dddd         | 0-8191       | Word: protection relay            |
| D              | ddddd        | 0-19999      | Word: data register               |
| R              | ddddd        | 0-16383      |                                   |
| S              | ddd          | 0-127        | Word: stepping register           |
| Z              | ddd          | 0-127        |                                   |
| U              | dd.dd        | 0.0-11.31    |                                   |
| N              | ddddd        | 0-10239      | Word：（read only）               |

<img src="lg.files/image012.gif" width="595" />

Note:

d represents decimal system, input range is 0-9;

h represents hexadecimal system, input range is 0-9, a-f;

Word in the remarks: represents the register can only be used as word;

Bit in the remarks: represents the register can only be used as bit;

The names of the registers supported by different equipment model may be different, and the scopes may also be different.

For detailed name and scope, please consult related technical document of the connected device

<img src="lg.files/image013.gif" width="595" />
